



## nginx certbot
````
sudo apt install certbot python3-certbot-nginx -y
````

## apache certbot
````
sudo apt install certbot python3-certbot-apache -y
````

## request ssl nginx
````
sudo certbot --nginx -d app1.example.com -d app2.example.com
````

## request ssl apache
````
certbot --apache -d app1.example.com -d app2.example.com
````

## enable auto renew
````
systemctl enable certbot.timer
````

## restart
````
systemctl restart certbot.timer
````

## check status renew
````
systemctl status certbot.timer

root@app1:~# systemctl status certbot.timer
● certbot.timer - Run certbot twice daily
     Loaded: loaded (/lib/systemd/system/certbot.timer; enabled; vendor preset: enabled)
     Active: active (waiting) since Wed 2022-09-07 14:02:49 UTC; 3 weeks 4 days ago
    Trigger: Mon 2022-10-03 04:40:05 UTC; 26min left
   Triggers: ● certbot.service

Sep 07 06:18:53 app1.example.com systemd[1]: Started Run certbot twice daily.
Sep 07 06:19:12 app1.example.com systemd[1]: certbot.timer: Succeeded.
Sep 07 06:19:12 app1.example.com systemd[1]: Stopped Run certbot twice daily.
Sep 07 06:19:12 app1.example.com systemd[1]: Stopping Run certbot twice daily.
Sep 07 06:19:12 app1.example.com systemd[1]: Started Run certbot twice daily.
Sep 07 14:02:34 app1.example.com systemd[1]: certbot.timer: Succeeded.
Sep 07 14:02:34 app1.example.com systemd[1]: Stopped Run certbot twice daily.
Sep 07 14:02:49 app1.example.com systemd[1]: Started Run certbot twice daily.
root@app1:~#
````

## option

### check config apache

````
sudo apache2ctl configtest
````

### check config nginx
````
sudo nginx -t
````
