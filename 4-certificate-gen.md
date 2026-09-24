## Certificate generation

Switch your terminal session to the dedicated `tak` system user to ensure all generated certificates are created with the correct file ownership and permissions:
```
sudo su tak
```

Open the metadata configuration file in a text editor to define your server's geographic and organizational identity settings (such as country, state, and organization name):
```
nano /opt/tak/certs/cert-metadata.sh
```

Navigate directly into the target certificates directory where the built-in certificate generation scripts must be executed:
```
cd /opt/tak/certs
```

Run the root authority script to establish your private, top-level Certificate Authority (CA) that will cryptographically anchor all other certificates on your network:
```
./makeRootCa.sh --ca-name <CAcommonName>
```
>🛈 Example:
><br>./make RootCa.sh –-ca-name TAK-ROOT-CA-01

Run the certificate script to generate a subordinate, intermediate Certificate Authority and link it to your newly created root authority:
```
./makeCert.sh ca <CAcommonName>
```
>🛈 Example:
><br>./make RootCa.sh –-ca-name TAK-ID-CA-01
