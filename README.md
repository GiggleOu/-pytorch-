-pytorch-在安装时出现错误：

An HTTP error occurred when trying to retrieve this URL. 
HTTP errors are often intermittent, and a simple retry will get you on your way. 
SSLError(MaxRetryError('HTTPSConnectionPool(host=\'mirrors.tun...

解决方法：
在目录下C:\Users\...,找到condarc文件
用记事本打开，更改为：
channels:
  - https://mirrors.tuna.tsinghua.edu.cn/anaconda/pkgs/main/
  - https://mirrors.tuna.tsinghua.edu.cn/anaconda/pkgs/free/
  - defaults
show_channel_urls: true
ssl_verify: false

关键是最后一行ssl_verify:要改为false。
