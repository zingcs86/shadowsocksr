ShadowsocksR
===========
[![owner1](https://img.shields.io/badge/Powered%20by-PW--Chen-blue.svg?style=flat)](https://github.com/PW-Chen)
[![Build Status]][Travis CI]

A fast tunnel proxy that helps you bypass firewalls.

伺服器 / Server
------
### 安裝 / Install

Debian / Ubuntu:

    apt-get install git
    git clone https://github.com/pw-chen/shadowsocksr.git

### 啟動 / Start

move to "~/shadowsocksr/shadowsocks", then run:

    cd ~/shadowsocksr/shadowsocks
    sudo python server.py -p 443 -k password  -m aes-256-cfb -O auth_sha1_v4 -o http_simple -d start

參數選項 (13種加密方式 7種協議（protocol）9種混淆（obfs） ):

| 	-m	 | 	 -O	 | 	-o	 |
| 	-----	 | 	-------	 | 	-----	 |
| 	none	 | 	origin	 | 	plain	 |
| 	aes-256-cfb	 | 	verify_deflate	 | 	http_simple	 |
| 	aes-192-cfb	 | 	auth_sha1_v4	 | 	http_simple_compatible	 |
| 	aes-128-cfb	 | 	auth_sha1_v4_compatible	 | 	http_post	 |
| 	aes-256-cfb8	 | 	auth_aes128_md5	 | 	http_post_compatible	 |
| 	aes-192-cfb8	 | 	auth_aes128_sha1	 | 	tls1.2_ticket_auth	 |
| 	aes-128-cfb8	 | 	auth_chain_a	 | 	tls1.2_ticket_auth_compatible	 |
| 	aes-256-ctr	 | 	auth_chain_b	 | 	tls1.2_ticket_fastauth	 |
| 	aes-192-ctr	 | 		 | 	tls1.2_ticket_fastauth_compatible	 |
| 	aes-128-ctr	 | 		 | 		 |
| 	chacha20-ietf	 | 		 | 		 |
| 	chacha20	 | 		 | 		 |
| 	rc4-md5	 | 		 | 		 |
| 	rc4-md5-6	 | 		 | 		 |

Check all the options via `-h`.

You can also use a configuration file instead (recommend), move to "~/shadowsocksr" and edit the file "user-config.json", then move to "~/shadowsocksr/shadowsocks" again, just run:

    python server.py

To run in the background / 背景運行:

    ./logrun.sh

To stop / 停止運行:

    ./stop.sh

To monitor the log / 查看log文件 :

    ./tail.sh


客戶端 / Client (Broken)
------

* [Windows] / [macOS]
* [Android] / [iOS]
* [OpenWRT]

Use GUI clients on your local PC/phones. Check the README of your client
for more information.

Documentation
-------------

You can find all the documentation in the [Wiki].

License
-------

Copyright 2015 clowwindy

Licensed under the Apache License, Version 2.0 (the "License"); you may
not use this file except in compliance with the License. You may obtain
a copy of the License at

    http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS, WITHOUT
WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied. See the
License for the specific language governing permissions and limitations
under the License.

Bugs and Issues
----------------

* [Issue Tracker]



[Android]:           https://github.com/shadowsocksr/shadowsocksr-android
[Build Status]:      https://travis-ci.org/shadowsocksr/shadowsocksr.svg?branch=manyuser
[Debian sid]:        https://packages.debian.org/unstable/python/shadowsocks
[iOS]:               https://github.com/shadowsocks/shadowsocks-iOS/wiki/Help
[Issue Tracker]:     https://github.com/shadowsocksr/shadowsocksr/issues?state=open
[OpenWRT]:           https://github.com/shadowsocks/openwrt-shadowsocks
[macOS]:             https://github.com/shadowsocksr/ShadowsocksX-NG
[Travis CI]:         https://travis-ci.org/shadowsocksr/shadowsocksr
[Windows]:           https://github.com/shadowsocksr/shadowsocksr-csharp
[Wiki]:              https://github.com/breakwa11/shadowsocks-rss/wiki
