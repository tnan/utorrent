wget https://github.com/phpsysinfo/phpsysinfo/archive/v3.3.1.tar.gz -O phpsysinfo.tar.gz<br>
tar -zxvf phpsysinfo.tar.gz -C /var/www/html/<br>
mv /var/www/html/phpsysinfo-3.3.1 /var/www/html/phpsysinfo<br>
mv /var/www/html/phpsysinfo/phpsysinfo.ini.new /var/www/html/phpsysinfo/phpsysinfo.ini<br>
wget https://api.github.com/repos/DirectoryLister/DirectoryLister/tarball/2.7.1 -O directorylister.tar.gz<br>
tar -zxvf directorylister.tar.gz -C /var/www/html/<br>
mv /var/www/html/DirectoryLister-DirectoryLister-a85b063 /var/www/html/files<br>
mkdir /var/www/html/files/torrent<br>
mkdir /var/www/html/files/download<br>
rm /var/www/html/files/COPYING<br>
rm /var/www/html/files/README.md<br>
rm -R /var/www/html/files/web<br>
mv /var/www/html/files/resources/default.config.php /var/www/html/files/resources/config.php<br>
wget http://download-new.utorrent.com/endpoint/utserver/os/linux-x64-ubuntu-13-04/track/beta/ -O utserver.tar.gz<br>
tar -zxvf utserver.tar.gz -C /opt/<br>
mv /opt/utorrent-server-alpha-v3_3 /opt/utorrent<br>
chown root:root -R /opt/utorrent/<br>
ln -s /opt/utorrent/utserver /usr/bin/utserver<br>
apt-get -y update<br>
DEBIAN_FRONTEND=noninteractive apt-get -y install libssl1.0.0 libssl-dev apache2 php php-xml<br>
cd /opt/utorrent<br>
./utserver -settingspath /opt/utorrent -configfile /opt/utorrent/utserver.conf &<br>

utserver -settingspath /opt/utorrent/ &<br>
