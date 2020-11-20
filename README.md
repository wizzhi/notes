# notes

* download resources:

  * Win7 iso mirrow: http://mirror.corenoc.de/digitalrivercontent.net/
  * Win10 official downlaod: https://www.microsoft.com/en-us/software-download/windows10

* echarts:
  * online coding: https://echarts.apache.org/examples/zh/editor.html?c=tree-basic
  * customize; https://www.cnblogs.com/zhaoweikai/p/9950691.html
  * embed into weChat https://juejin.im/post/6844903896043290631
 
* host maintain
  * swap space
  ```bash
  free -m
  dd if=/dev/zero of=/etc/swapfile bs=1024 count=500000
  mkswap /etc/swapfile
  swapon /etc/swapfile
  free -m
  ```
  * system update
  ```bash
  nohup yum update -y  --skip-broken &
  ```
  * system info
  ```bash
  lsb_release -a
  cd /var/www/html
  ```
  
