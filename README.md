# Nginx-Fancyindex-Theme
Nginx Fancyindex模块的响应主题。简约、现代、简约。带有一个搜索表单，旨在处理数千个文件没有任何问题。

ngnix添加 fancyindex 模块: [here](https://github.com/aperezdc/ngx-fancyindex).


## Usage

1. 确保您使用nginx编译fancyindex模块，可以自己编译它，或者通过完整发行版（paquet nginx extras）安装nginx。
   宝塔nginx安装fancyindex模块方式:[宝塔nginx安装方式](https://www.bt.cn/bbs/thread-48398-1-1.html)
2. clone项目到本地
3. 修改 nginx 配置文件 

```bash
  location / { 
          # include   /www/wwwroot/download.gojw.xyz/fancyindex/fancyindex.conf;
          include /www/wwwroot/download.gojw.xyz/Nginx-Fancyindex-Theme/fancyindex.conf;
          root /www/wwwroot/download.gojw.xyz/;
          charset utf-8,gbk; #解决中文乱码
  }   
```

5. Restart/reload nginx.
6. Check that it's working, and enjoy!

## Configuration

A standard config looks something like this (use `-light` for the default light theme, or `-dark` for a dark theme):

```bash
fancyindex on;
fancyindex_localtime on;
#时间格式 	2021-03-17 06:09:12
fancyindex_time_format "%Y-%m-%d %T";
#时间倒序
fancyindex_default_sort date_desc;

fancyindex_exact_size off;
# Specify the path to the header.html and foother.html files (server-wise)
fancyindex_header "/Nginx-Fancyindex-Theme/light-Theme/header.html";
fancyindex_footer "/Nginx-Fancyindex-Theme/light-Theme/footer.html";
#fancyindex_header "/Nginx-Fancyindex-Theme/dark-Theme/header.html";
#fancyindex_footer "/Nginx-Fancyindex-Theme/dark-Theme/footer.html";
# Ignored files will not show up in the directory listing, but will still be public.
fancyindex_ignore "dow.py";
fancyindex_ignore "fancyindex";
# Making sure folder where these files are do not show up in the listing.
fancyindex_ignore "Nginx-Fancyindex-Theme";
# Maximum file name length in bytes, change as you like.
fancyindex_name_length 255;

```


> Reference: [H5BP Nginx Server Config](https://github.com/h5bp/server-configs-nginx/blob/master/nginx.conf)

## 示例
### 已汉化标题，搜索栏、去掉底部的链接:
![主题已修改](https://i.loli.net/2021/03/18/ftVEJIDeKynrbTu.png)

---

### Dark and Light style for chose:
#### FancyIndex-dark
![FancyIndex-dark](https://lanffy.github.io/images/posts/2017/2017-12-27-15143595999553.jpg)
#### FancyIndex-light
![FancyIndex-light](https://lanffy.github.io/images/posts/2017/2017-12-27-15143595456540.jpg)


