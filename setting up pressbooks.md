

https://pressbooks.org/user-docs/installation/

pressbooks still recommends php 7.4 but requires php 8

if you need to change wordpress version:
```
wp core update --version=6.0.3
```


```
cd /var/www/webroot/ROOT/wp-content/plugins/
wget https://github.com/pressbooks/pressbooks/releases/download/6.6.0/pressbooks-6.6.0.zip
unzip pressbooks-6.6.0.zip
rm pressbooks-6.6.0.zip
cd ..
mkdir mu-plugins
cp plugins/pressbooks/hm-autoloader.php mu-plugins/hm-autoloader.php

```
```
cd /var/www/webroot/ROOT/wp-content/themes/
wget https://github.com/pressbooks/pressbooks-book/releases/download/2.25.1/pressbooks-book-2.25.1.zip
unzip pressbooks-book-2.25.1.zip
rm pressbooks-book-2.25.1.zip

```
```
wget https://github.com/pressbooks/pressbooks-aldine/releases/download/1.18.1/pressbooks-aldine-1.18.1.zip
unzip pressbooks-aldine-1.18.1.zip
rm pressbooks-aldine-1.18.1.zip

```

## other dependencies 

we'll need java
```
sudo yum install java-11-openjdk -y
```

prince xml
```
wget https://www.princexml.com/download/prince-15.1-1.centos7.x86_64.rpm
sudo yum install prince-15.1-1.centos7.x86_64.rpm -y
```

epubcheck
```
sudo mkdir /opt/epubcheck && cd /opt/epubheck &&
 wget https://github.com/w3c/epubcheck/releases/download/v5.1.0/epubcheck-5.1.0.zip
unzip epubcheck-5.1.0.zip
sudo mv * /opt/epubcheck
```

xmllint - already installed

saxon-he
```
mkdir /opt/saxon-he
wget https://master.dl.sourceforge.net/project/saxon/Saxon-HE/9.7/SaxonHE9-7-0-10J.zip
unzip SaxonHE9-7-0-10J.zip
```

ghostscript
```
sudo yum install ghostscript
```

imagemagick - already installed

poppler-utils
```
sudo yum install poppler-utils
```

## eds notes on install pressbooks mathjax stuff
```bash
#Get the Pressbooks Mathjax files
wget https://github.com/pressbooks/pb-mathjax/archive/refs/heads/master.zip
unzip master.zip
cd pb-mathjax-master
# Install node.js - must be done as su
sudo yum -y update
curl -SL https://rpm.nodesource.com/setup_12.x | sudo bash -
sudo yum clean all && sudo yum makecache fast
sudo yum install -y gcc-c++ make
sudo yum install -y nodejs
# use npm to finish PB Mathjax installation
From the pressbooks directory
sudo npm install
sudo npm start
# install PM2 as sudo
sudo npm i -g pm2 
cd ~/code/github/pressbooks/pb-mathjax
sudo npm install --only=prod
sudo pm2 start bin/www --name pb-mathjax
```