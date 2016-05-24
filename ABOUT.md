##    INTRODUCTION
Asterisk version 12 and 13 have [ARI] (https://wiki.asterisk.org/wiki/pages/viewpage.action?pageId=29395573)

This is an example how to made conference between multiply users using ARI and nodeJS.

## Required
* Asterisk 12 or Asterisk 13
* nodeJS
* npm

## Install
* configure Asterisk: enable HTTP + configure ARI and dialplan (see examples of configuration files in "asterisk" directory)
* download project zip archive
* extract files to www folder (ex. /usr/local/www/conf)
* install nodeJS
```html
Debian: apt-get install nodejs
FreeBSD: cd /usr/ports/www/node && make install clean
```
* install nmp
```html
Debian: apt-get install npm
FreeBSD: cd /usr/ports/www/npm && make install clean
```
* install required javascript packages with npm
```html
cd /usr/local/www/conf/ws_server
nmp install ws
nmp install request
```
* edit file js/options.js (replace localhost with your FQDN where webp page will be located)
* edit file ws_server/ws_server.options.js (edit ARI info)

## Use
* start server
```html
Debian:
cd /usr/local/www/conf/ws_server
nodejs ws_server.js
FreeBSD:
cd /usr/local/www/conf/ws_server
node ws_server.js
```
* open web page http://yourFQDN/
* call to you conference exten
