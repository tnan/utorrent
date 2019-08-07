apt-get -y update<br>
DEBIAN_FRONTEND=noninteractive apt-get -y install libssl1.0.0 libssl-dev apache2 php php-xml<br>
wget https://github.com/tnan/utorrent/raw/master/home.tgz<br>
wget https://github.com/tnan/utorrent/raw/master/utserver.tar.gz<br>
tar -zxvf home.tgz -C /var/www/html/<br>
tar -zxvf utserver.tar.gz -C /opt/<br>
/opt/utorrent/utserver -settingspath /opt/utorrent &<br>
