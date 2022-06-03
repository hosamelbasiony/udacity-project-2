 #!/bin/bash
apt-get update -y
apt-get install zip -y
apt-get install unzip -y
apt-get install git -y
apt-get install apache2 -y
systemctl start apache2.service
cd /var/www/html
rm -v index.html
wget https://my902248134218-bucket.s3.us-west-2.amazonaws.com/udacity-prj2-template.zip
unzip udacity-prj2-template.zip
cd /var/www/html/udacity-prj2-template
cp -a /var/www/html/udacity-prj2-template/. /var/www/html/
echo "Udacity Demo Web Server Up and Running!" > index2.html