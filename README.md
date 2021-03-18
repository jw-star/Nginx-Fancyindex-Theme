# Nginx-Fancyindex-Theme
A responsive theme for [Nginx](https://www.nginx.org/) Fancyindex module. Minimal, modern and simple.
Comes with a search form, aims to handle thousands of files without any problems.

The fancyindex module can be found [here](https://github.com/aperezdc/ngx-fancyindex).

And Chinese manual(中文使用手册):[Nginx浏览目录配置及美化](https://lanffy.github.io/2017/12/27/Nginx-Browse-Folder-Config)

[![made-for-nginx](https://img.shields.io/badge/Made%20for-nginx-1f425f.svg)](https://www.nginx.org/)

## Install Fancyindex Module

> Reference: [Nginx-Browse-Folder-Config](http://lanffy.github.io/2017/12/27/Nginx-Browse-Folder-Config)

## Usage

1. Make sure you have the fancyindex module compiled with nginx, either by compiling it yourself or installing nginx via the full distribution (paquet ``nginx-extras``).
2. Include the content of [fancyindex.conf](fancyindex.conf) in your location directive (``location / {.....}``) in your nginx config (usually ``nginx.conf``).
3. Move the ``Nginx-Fancyindex-Theme/`` folder to the root of the site directory.
4. Restart/reload nginx.
5. Check that it's working, and enjoy!

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

## Examples
### Filter a list of directories (with search):
![Nginx-Fancyindex-Theme__example3](https://lanffy.github.io/images/posts/2017/2017-12-27-15143595456540.jpg)

---

### Dark and Light style for chose:
#### FancyIndex-dark
![FancyIndex-dark](https://lanffy.github.io/images/posts/2017/2017-12-27-15143595999553.jpg)
#### FancyIndex-light
![FancyIndex-light](https://lanffy.github.io/images/posts/2017/2017-12-27-15143595456540.jpg)


### :scroll: License ? [![GitHub license](https://img.shields.io/github/license/Naereen/Nginx-Fancyindex-Theme.svg)](https://github.com/Naereen/Nginx-Fancyindex-Theme/blob/master/LICENSE)
[MIT Licensed](https://lbesson.mit-license.org/) (file [LICENSE](LICENSE)).
© [Lilian Besson](https://GitHub.com/Naereen), 2016.

[![Maintenance](https://img.shields.io/badge/Maintained%3F-yes-green.svg)](https://GitHub.com/Naereen/Nginx-Fancyindex-Theme/graphs/commit-activity)
[![Ask Me Anything !](https://img.shields.io/badge/Ask%20me-anything-1abc9c.svg)](https://GitHub.com/Naereen/ama)
[![Analytics](https://ga-beacon.appspot.com/UA-38514290-17/github.com/Naereen/Nginx-Fancyindex-Theme/README.md?pixel)](https://GitHub.com/Naereen/Nginx-Fancyindex-Theme/)

[![ForTheBadge built-with-swag](http://ForTheBadge.com/images/badges/built-with-swag.svg)](https://GitHub.com/Naereen/)
[![ForTheBadge uses-js](http://ForTheBadge.com/images/badges/uses-js.svg)](http://ForTheBadge.com)
[![ForTheBadge uses-html](http://ForTheBadge.com/images/badges/uses-html.svg)](http://ForTheBadge.com)
[![ForTheBadge uses-css](http://ForTheBadge.com/images/badges/uses-css.svg)](http://ForTheBadge.com)
[![ForTheBadge uses-badges](http://ForTheBadge.com/images/badges/uses-badges.svg)](http://ForTheBadge.com)
[![ForTheBadge uses-git](http://ForTheBadge.com/images/badges/uses-git.svg)](https://GitHub.com/)
