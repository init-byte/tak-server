# TAK Server Installation
This is the core installation of the TAK Server software.

---


## Download required files
Download the `.key`, `.pol`, and `.deb` files from [tak.gov](https://tak.gov/products/tak-server) to the Downloads folder:
- takserver-public-gpg.key
- deb_policy.pol
- takserver_x.x-RELEASExx_all.deb

## Verify GPG signature to ensure package integrity
Install the `debsig-verify` utility:

```
sudo apt install debsig-verify
```

Create the system directories for the keyring and the verification policy with **your** GPG ID Key:
>🛈 Note: You must retrieve the unique GPG Key ID from your `deb_policy.pol` file (for example: 039FCDA2D8907527) and replace 039FCDA2D8907527 with your actual Key ID in all the commands before running them.     
```
sudo mkdir /usr/share/debsig/keyrings/039FCDA2D8907527
```
```
sudo mkdir -p /etc/debsig/policies/039FCDA2D8907527
```


Initialize the empty keyring file in the new directory:

```
sudo touch /usr/share/debsig/keyrings/039FCDA2D8907527/debsig.gpg
```

Navigate into your Downloads directory where the downloaded TAK Server key, policy, and installer files are located:
```
cd ./Downloads
```

Import the official TAK Server public GPG security key directly into the empty verification keyring file you created earlier:
```
sudo gpg --no-default-keyring --keyring /usr/share/debsig/keyrings/039FCDA2D8907527/debsig.gpg --import takserver-public-gpg.key
```

Copy your policy configuration file `deb_policy.pol` into the secure verification directory and rename it to `debsig.pol` so the system can read it:
```
sudo cp deb_policy.pol /etc/debsig/policies/039FCDA2D8907527/debsig.pol
```

Run the verification tool in verbose mode to scan the TAK Server Debian package and confirm its signature matches your imported security key and policy:
```
debsig-verify -v takserver_x.x-RELEASExx_all.deb
```
>🛈 Confirm signature verification by identifying the statement:
><br>debsig: Verified package from 'TAK Product Center' (TAK Server Release)


## Install TAK Server (single-server)

Navigate to your Downloads directory where the newly verified TAK Server installer package is located:
```
cd ./Downloads
```

Update your local package index to ensure your system has the most recent list of available dependencies and security patches before installing new software:
```
sudo apt update
```

Run the package manager to install the local TAK Server database application along with all of its required system dependencies without being prompted for confirmation:
```
sudo apt install ./takserver_x.x-RELEASExx_all.deb -y
```

Force the system to reload its background configurations so it recognizes any newly installed or modified TAK Server service files:
```
sudo systemctl daemon-reload
```
Configure the TAK Server service to automatically launch and run every time the operating system boots up:
```
sudo systemctl enable takserver
```

Start the TAK Server background process to bring your server online now:
```
sudo systemctl start takserver
```

View the active running state and recent diagnostic logs of the TAK Server to verify it successfully launched without errors:
```
sudo systemctl status takserver
```


