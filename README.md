# SVN
## SVN server installation on Ubuntu 14.04
```
$ sudo apt-get update
$ sudo apt-get install subversion
```
```
$ sudo mkdir -p /home/svn/<repo name>
$ 
```
```
$ sudo svnadmin create /home/svn/<repo name>
```
```
$ sudo vim /home/<repo name>/repository/conf/svnserve.conf
```
```
$ sudo vim /home/svn/<repo name>/conf/passwd 
```
## SVN client (RabbitVCS) installation on Ubuntu 14.04 Desktop
將 RabbitVCS 套件庫加進來並安裝 RabbitVCS
```
$ sudo add-apt-repository ppa:rabbitvcs/ppa
$ sudo apt-get update
$ sudo apt-get install rabbitvcs-cli rabbitvcs-core rabbitvcs-gedit rabbitvcs-nautilus3
```
重新啟動檔案瀏覽器以使 RabbitVCS 生效
```
$ nautilus -q
```  
在檔案瀏覽器中點選右鍵會出現 RabbitVCS SVN 選項  

## 參考資料
* Ubuntu 14.04下搭建SVN服务器（SVN Server） http://www.linuxidc.com/Linux/2016-08/133961.htm
* How to install RabbitVCS on Ubuntu 14.04? http://askubuntu.com/questions/464532/how-to-install-rabbitvcs-on-ubuntu-14-04/464535#464535
