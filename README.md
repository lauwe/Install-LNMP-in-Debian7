# Install-LNMP-in-Debian7
Install Nginx, PHP and Mysql on Debian7 from source.
# See below for more information
# Update Debian7
	apt-get update
## Error
	Reading package lists... Done
	W: There is no public key available for the following key IDs:
	9D6D8F****57C906
	W: There is no public key available for the following key IDs:
	7638D0****90D010
## Fix it with
	apt-get install debian-keyring debian-archive-keyring
	apt-key update
## Re-update
	apt-get update
	......
	Reading package lists... Done
## Install Nginx
Add PGP key from nginx.org

	wget http://nginx.org/keys/nginx_signing.key
	apt-key add nginx_signing.key

Then, append the following to the end of the _/etc/apt/sources.list_ file.

	vi /etc/apt/sources.list

Add the following codes：

	deb http://nginx.org/packages/debian/ wheezy nginx
	deb-src http://nginx.org/packages/debian/ wheezy nginx

Then run the following commands:

	apt-get update
	apt-get install nginx

Now enter your ip in the browser, you will see the following content.
![](https://raw.githubusercontent.com/lauwe/Install-LNMP-in-Debian7/master/assets/20160406163156.png)

