## 建立虛擬機器
1. ![](https://i.imgur.com/YKOJENH.jpg)
2. ![](https://i.imgur.com/33VVVCE.jpg)
3. ![](https://i.imgur.com/cQFdRem.jpg)
4. ![](https://i.imgur.com/mATyX7w.jpg)
5. ![](https://i.imgur.com/BoBgWq8.jpg)
6. ![](https://i.imgur.com/ObsVDIP.jpg)
7. ![](https://i.imgur.com/xMpLPA7.jpg)
8. ![](https://i.imgur.com/jDNLr5w.jpg)
## 連線
1. ![](https://i.imgur.com/uYNPvDh.jpg)
2. ![](https://i.imgur.com/ATVFPfK.jpg)
3. ![](https://i.imgur.com/5U0RTIP.jpg)
4. ![](https://i.imgur.com/iMIYFVI.jpg)
## YUM更新
1. 更新
```shell
sudo yum update
```
## 安裝Apache
1. 安裝httdp Server
```shell
sudo yum install httpd
```
2. 設置開機啟用
```shell
sudo systemctl enable httpd
```
3. 開啟Apache
```shell
sudo systemctl start httpd
```
## 安裝php
1. 開啟Remi庫
```shell
sudo rpm -Uvh https://dl.fedoraproject.org/pub/epel/epel-release-latest-8.noarch.rpm
```
```shell
sudo dnf install -y https://rpms.remirepo.net/enterprise/remi-release-8.rpm
``` 
2. 列出可用PHP
```shell
sudo dnf module list php
```
3. 啟用PHP
```shell
sudo dnf module enable php:remi-7.4 -y
```
4. 安裝php
```shell
sudo dnf module enable php:remi-7.4 -y
```
## 安裝php擴展
1.  安裝php-mysqlnd
```shell
sudo dnf install -y php-mysqlnd
```
2. 查看MySQL是否有啟動成功
```shell
sudo php -m | grep -i mysql
```
3. 安裝php-zip php-gd php-init
```shell
sudo yum install php-zip php-gd php-init
```
## 安裝MariaDB
1. 安裝
```shell
sudo yum install mariadb mariadb-server
```
2. 開啟mairaDB
```shell
sudo systemctl start mariadb
```
3. 設置開機啟動
```shell
sudo systemctl enable mariadb
```
## 創建資料庫
1. 登入(root)
```shell
sudo mysql -u root -p
```
2. 建立資料庫
```sql
create database moodle;
```
3. 建立使用者及密碼
```sql
CREATE USER 'ksu'@'%' IDENTIFIED BY 'PASSWORD';
```
4. 給予權限(PRIVILEGES)
```sql
GRANT ALL PRIVILEGES ON *.* TO 'ksu'@'%' IDENTIFIED BY 'PASSWORD';
```
5. 刷新權限
```sql
FLUSH PRIVILEGES;
```
6. 離開
```sql
exit;
```
## 安裝Moodle
1. 進入Apache目錄
```shell
cd /var/www/html
```
2. 下載Moodle
```shell
sudo git clone https://github.com/moodle/moodle.git
```
3. 建立moodle資料位置
```shell
sudo mkdir ../moodledata
```
4. 給予權限
```shell
sudo chown -R apache:apache  ../html
```
```shell
sudo chown -R apache:apache ../moodledata
```
5.  重新啟動
```shell
sudo systemctl restart httpd
```
6. ![](https://i.imgur.com/S3hes53.jpg)
7. ![](https://i.imgur.com/SiopaQi.jpg)
8. ![](https://i.imgur.com/rRBOpqB.jpg)
9. ![](https://i.imgur.com/s7jFUFA.jpg)
10. ![](https://i.imgur.com/Twjqw2F.jpg)
11. ![](https://i.imgur.com/PPEbiwe.jpg)
12. ![](https://i.imgur.com/kkbeDFs.jpg)
13. ![](https://i.imgur.com/jFwry4E.jpg)
14. ![](https://i.imgur.com/3deNos0.jpg)
