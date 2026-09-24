## Install Java OpenJDK

Check version:

```
java --version
```

If missing:

```
sudo apt install openjdk-17-jre
```

## Increase TCP Connection Limits
To support Java threads, increase the open files limit by configuring soft and hard file handles in /etc/security/limits.conf (via a text editor or a single command string):

```
cat <HERE | sudo tee --append /etc/security/limits.conf > /dev/null
  *	soft nofile 32768
  *	hard nofile 32768
  HERE
```

## Install  PostgreSQL + PostGIS

Install the Linux Standard Base (LSB) query tool to detect your specific version of Ubuntu or Debian so that the correct database repository can be added:

```
sudo apt-get install -y lsb-release
```

Create a highly secure folder on your system to store security verification keys for third-party software repositories:

```
sudo mkdir -p /etc/apt/keyrings
```

Download the official GPG (GNU Privacy Guard) public security key for the PostgreSQL repository and save it directly to your system's keyring folder:

```
sudo curl https://www.postgresql.org/media/keys/ACCC4CF8.asc --output /etc/apt/keyrings/postgresql.asc
```

