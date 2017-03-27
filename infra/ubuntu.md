## ubuntuで rails 

### env
- ubuntu 16.04
- rbenv

- mysql 5.6

```
sudo add-apt-repository 'deb http://archive.ubuntu.com/ubuntu trusty universe'
sudo apt-get update
sudo apt install mysql-server-5.6 * see note below if you get an error
sudo apt install mysql-client-5.6
sudo service mysql start
# check
mysql -uroot -p
```

- `sudo apt-get install redis-server`
