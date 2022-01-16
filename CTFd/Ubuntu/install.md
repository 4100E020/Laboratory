# Ubuntu install CTFd
## 建立GCP
1. ![](https://i.imgur.com/hjUihln.jpg)
2. ![](https://i.imgur.com/rMT5SSP.jpg)
3. ![](https://i.imgur.com/fbWIcT9.jpg)
4. ![](https://i.imgur.com/VPLjIma.jpg)
## 裝CTFd
1. 更新apt
```shell
sudo apt update
sudo apt upgr 
```
2. 安裝所需套件
```shell
sudo apt-get install python3-pip -y
```
```shell
sudo python3 -m pip install Flask -y
```
```shell
sudo apt install mariadb-server -y
```
```shell
sudo apt install libmariadbclient-dev -y
```
```shell
sudo apt install nginx -y
```
```shell
sudo pip3 install uwsgi -y
```
```shell
sudo apt install uwsgi -y
```
```shell
sudo apt install redis-server -y
```
```shell
sudo apt install unzip -y
```
```shell
sudo apt install -y uwsgi-plugin-python3
```
```shell
sudo apt install -y docker
```
```shell
sudo apt install -y docker.io
```
3. 更改pip為pip3
```shell
sudo vim prepare.sh
```
4. 調整CTFd內參數
```shell
sudo sh prepare.sh
supervised no ==> supervised systemd
```
```shell
sudo vim CTFd/CTFd/config.py
REDIS_URL = 'redis://127.0.0.1:6379'
```
5. 建立資料庫
```shell
sudo mysql -u root -p
```
```sql
create database ctfd;
CREATE USER 'ksu'@'%' IDENTIFIED BY 'Ksu@0956327000';
GRANT ALL PRIVILEGES ON *.* TO 'ksu'@'%' IDENTIFIED BY 'Ksu@0956327000';
FLUSH PRIVILEGES;
exit;
```
6. 修改wsgi.py
```shell
sudo vim wsgi.py
sys.path.insert(0,'/home/ksu/CTFd') ==>改CTFd路徑
```
```shell
sudo vim /etc/uwsgi/apps-available/uwsgi.ini
chdir = /home/ksu/CTFd/ ==>改CTFd路徑
```
7. 連結uwsgi
```shell
sudo ln -s /etc/uwsgi/apps-available/uwsgi.ini /etc/uwsgi/apps-enabled/uwsgi.ini
```
8. 給予權限
```shell
sudo chown -R www-data:www-data /home/ksu/CTFd/
```
9. 移除default
```shell
sudo rm /etc/nginx/sites-available/default
```
10. 新增default
```shell
sudo vim /etc/nginx/sites-available/default
```
```
server {
        listen 80 default_server;
        listen [::]:80 default_server;
	root /home/ksu/CTFd; 
	index index.html index.htm index.nginx-debian.html;

        #server_name 120.114.62.218;

	location / {
             #try_files $uri $uri/ =404;
             root /home/ksu/CTFd;
             include uwsgi_params;
             uwsgi_pass unix:/tmp/uwsgi.sock;
             uwsgi_read_timeout 300s;
        }
	location /static {
               root /home/ksu/CTFd/CTFd/themes/core/static/; 
        }
	client_max_body_size 1000m;
        }
```
11. 重啟nginx
```shell
sudo service nginx restart
```
12. 重開機
```shell
sudo reboot
```
## 安裝CTFd
1. ![](https://i.imgur.com/rBaO6SS.jpg)
2. ![](https://i.imgur.com/jECGIS9.jpg)
3. ![](https://i.imgur.com/HqNc0ms.jpg)
4. ![](https://i.imgur.com/KMk3O72.jpg)
5. ![](https://i.imgur.com/wr126Jv.jpg)
6. ![](https://i.imgur.com/TL0sZBH.jpg)
7. ![](https://i.imgur.com/8tHVFxc.jpg)
8. ![](https://i.imgur.com/zKiYwRj.jpg)
9. 修改IP
```shell
UPDATE `challenges` SET `description` = replace(`description`, '原本IP', '目前IP');
```
