## 建立EC2主機
- 拉系統(centOS)  
1. ![](https://i.imgur.com/Q4SB1xJ.jpg)
2. ![](https://i.imgur.com/eWaNcWq.jpg)
3. ![](https://i.imgur.com/NaBfItq.jpg)
4. ![](https://i.imgur.com/vxl6EDW.jpg)
5. ![](https://i.imgur.com/fiemSLn.jpg)
6. ![](https://i.imgur.com/vnLplAB.jpg)
7. ![](https://i.imgur.com/tL5c2Jn.jpg)
8. ![](https://i.imgur.com/d91Acod.jpg)
9. ![](https://i.imgur.com/ikwR9f9.jpg)
10. ![](https://i.imgur.com/jexlANE.jpg)
- 連線  
1. ![](https://i.imgur.com/DEougnu.jpg)
2. ![](https://i.imgur.com/nqz2817.jpg)
3. ![](https://i.imgur.com/wWMpAQg.jpg)
4. ![](https://i.imgur.com/8eb9qab.jpg)
5. ![](https://i.imgur.com/c7EujzQ.jpg)
6. ![](https://i.imgur.com/64dwSug.jpg)
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
6. ![](https://i.imgur.com/VEBoHyd.jpg)
7. ![](https://i.imgur.com/EKnsVAb.jpg)
8. ![](https://i.imgur.com/kaffEYD.jpg)
9. ![](https://i.imgur.com/lOJSGfZ.jpg)
10. ![](https://i.imgur.com/GwHWlQP.jpg)
11. ![](https://i.imgur.com/FXM8g2N.jpg)
12. ![](https://i.imgur.com/KyxpGLp.jpg)
12. ![](https://i.imgur.com/wzblEBG.jpg)
13. ![](https://i.imgur.com/C6ICK05.jpg)
14. ![](https://i.imgur.com/wU848dk.jpg)
