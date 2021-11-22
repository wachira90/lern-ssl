# lern-ssl
lern-ssl

## normal

````
openssl req -x509 -newkey rsa:4096 -keyout key.pem -out cert.pem -sha256 -days 365
````

## add subject 

````
-subj "/C=US/ST=Oregon/L=Portland/O=Company Name/OU=Org/CN=www.example.com"
````
````
Country Name (2 letter code) [AU]:TH
State or Province Name (full name) [Some-State]:SATHORN
Locality Name (eg, city) []:BANGKOK
Organization Name (eg, company) [Internet Widgits Pty Ltd]:EXAMPLE COMPANY
Organizational Unit Name (eg, section) []:IT-ENGINER
Common Name (e.g. server FQDN or YOUR name) []:IT-DEPT
Email Address []:SAM@EXAMPLE.COM
````

## final 

````
openssl req -x509 -newkey rsa:4096 -keyout key.pem -out cert.pem -sha256 -days 365 -subj "/C=TH/ST=Sathon/L=Bangkok/O=Ecample Company/OU=IT Engineer/CN=www.example.com"
````
