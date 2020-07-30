Executed commands for reducing ram usage (this services are not used, disable yours in your server as needed)

1.- identify the running and unnecesary services (you can use htop to see running processes)
```
htop
```

2.- Stop the required services
```
sudo service php7.0-fpm stop
sudo service php7.2-fpm stop
sudo service php7.4-fpm stop
sudo service postfix stop
sudo service postgresql stop
sudo service memcached stop
```
3.- Disable from startup
```
sudo systemctl disable mysql.service
sudo systemctl disable php7.0-fpm.service
sudo systemctl disable php7.2-fpm.service
sudo systemctl disable php7.4-fpm.service
sudo systemctl disable postfix.service
sudo systemctl disable postgresql.service
sudo systemctl disable memcached.service
```
