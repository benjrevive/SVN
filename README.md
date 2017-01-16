# SVN
https://github.com/benjrevive/svn  
*  [1](/README.md#SVN-plugin-for-Eclipse)  
  
## SVN server installation on Ubuntu 14.04
```
$ sudo apt-get update
$ sudo apt-get install subversion
```
查看 SVN 版本
```
$ svn --version --quiet
$ svnserve --version --quiet
```
```
$ sudo mkdir -p <SVN repo root>/<repo name>
$ sudo chmod -R 777 <SVN repo root>/<repo name>
$ sudo svnadmin create <SVN repo root>/<repo name>
$ sudo chmod -R 777 <SVN repo root>/<repo name>/db
```
啟用 SVN 密碼檔
```
$ sudo vim <SVN repo root>/<repo name>/conf/svnserve.conf
```
新增使用者帳號與密碼
```
$ sudo vim <SVN repo root>/<repo name>/conf/passwd 
```
啟動 SVN server 服務 (-d: 背景執行; -r: 後面接版本管理庫根目錄; --listen-host: 當伺服器有多個 IP 時，後面接 SVN server 服務所使用的 IP)
```
$ svnserve -d -r /home/svn [--listen-host X.X.X.X]
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

## SVN plugin for Eclipse
待補充<br />
3 種安裝方法<br />
開啟 Eclipse<br />
1\)<br />
點選 Help > Install New Software...1<br />
![install_new_software.png](/image/install_new_software.png)<br />
2\)<br />
3\)<br />
  
## 參考資料
* Ubuntu 14.04下搭建SVN服务器（SVN Server） http://www.linuxidc.com/Linux/2016-08/133961.htm
* How to install RabbitVCS on Ubuntu 14.04? http://askubuntu.com/questions/464532/how-to-install-rabbitvcs-on-ubuntu-14-04/464535#464535
* 【系統】SVN 筆記 - 基本指令 http://blog.xuite.net/chingwei/blog/25557142-%E3%80%90%E7%B3%BB%E7%B5%B1%E3%80%91SVN+%E7%AD%86%E8%A8%98+-+%E5%9F%BA%E6%9C%AC%E6%8C%87%E4%BB%A4
* Eclipse Subversive - Subversion (SVN) Team Provider http://www.eclipse.org/subversive/
