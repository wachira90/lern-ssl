# pfx-to-crt-key

## process convert .pfx to .crt and .key

````
D:\ssl\SSL_2022>openssl pkcs12 -in example.com.pfx -nocerts -out server-master.key
Enter Import Password: [PASSWORD PFX]
Enter PEM pass phrase: [YOUR OWN PASSWORD]
Verifying - Enter PEM pass phrase: [YOUR OWN PASSWORD]

D:\ssl\SSL_2022>openssl pkcs12 -in example.com.pfx -clcerts -nokeys -out server.crt
Enter Import Password: [PASSWORD PFX]

D:\ssl\SSL_2022>openssl rsa -in server-master.key -out server.key
Enter pass phrase for server-master.key: [YOUR OWN PASSWORD]
writing RSA key

````
