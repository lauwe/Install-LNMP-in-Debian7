# Install-LNMP-in-Debian7
Install Nginx, PHP and Mysql on Debian7 from source.
# See below for more information
# Update Debian7
apt-get update
## Error
	Reading package lists... Done
	W: There is no public key available for the following key IDs:
	9D6D8F6BC857C906
	W: There is no public key available for the following key IDs:
	7638D0442B90D010
## Fix it with
	apt-get install debian-keyring debian-archive-keyring
	apt-key update
## Re-update
	apt-get update
	......
	Reading package lists... Done
## Install Nginx
