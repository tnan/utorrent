wget https://github.com/phpsysinfo/phpsysinfo/archive/v3.3.1.tar.gz -O phpsysinfo.tar.gz
tar -zxvf phpsysinfo.tar.gz -C /var/www/html/
mv /var/www/html/phpsysinfo-3.3.1 /var/www/html/phpsysinfo 
mv /var/www/html/phpsysinfo/phpsysinfo.ini.new /var/www/html/phpsysinfo/phpsysinfo.ini
wget https://api.github.com/repos/DirectoryLister/DirectoryLister/tarball/2.7.1 -O directorylister.tar.gz
tar -zxvf directorylister.tar.gz -C /var/www/html/
mv /var/www/html/DirectoryLister-DirectoryLister-a85b063 /var/www/html/files
mkdir /var/www/html/files/torrent
mkdir /var/www/html/files/download
rm /var/www/html/files/COPYING
rm /var/www/html/files/README.md
rm -R /var/www/html/files/web
mv /var/www/html/files/resources/default.config.php /var/www/html/files/resources/config.php
wget http://download-new.utorrent.com/endpoint/utserver/os/linux-x64-ubuntu-13-04/track/beta/ -O utserver.tar.gz
tar -zxvf utserver.tar.gz -C /opt/
mv /opt/utorrent-server-alpha-v3_3 /opt/utorrent
chown root:root -R /opt/utorrent/
ln -s /opt/utorrent/utserver /usr/bin/utserver
apt-get -y update
DEBIAN_FRONTEND=noninteractive apt-get -y install libssl1.0.0 libssl-dev apache2 php php-xml
cd /opt/utorrent
./utserver -settingspath /opt/utorrent -configfile /opt/utorrent/utserver.conf &

utserver -settingspath /opt/utorrent/ &
