# vpn
yum install gcc make rpm-build autoconf.noarch zlib-devel pam-devel openssl-devel -y
wget http://openvpn.net/release/lzo-1.08-4.rf.src.rpm
wget http://pkgs.repoforge.org/rpmforge-release/rpmforge-release-0.5.2-2.el6.rf.x86_64.rpm
rpmbuild --rebuild lzo-1.08-4.rf.src.rpm
rpm -Uvh lzo-*.rpm
rpm -Uvh rpmforge-release*
yum install openvpn -y
cp -R /usr/share/doc/openvpn-2.2.2/easy-rsa/ /etc/openvpn/
yum -y install nano
nano /etc/openvpn/easy-rsa/2.0/vars
