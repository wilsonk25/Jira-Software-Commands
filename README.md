# Jira-Software-Commands
How to install Jira Software,IT Service Desk with Gmail in ubuntu 16.04 or Linux
Requirements for Jira
1)Mysql 5.6
2)Ubuntu 16.04 latest version
3)Jira software-7.3.6(latest version)

sudo add-apt-repository 'deb http://archive.ubuntu.com/ubuntu trusty universe'

sudo apt-get update
sudo apt install mysql-server-5.6
sudo /etc/init.d/mysql start
mysql -u root -p
create database jiradb character set utf8;
create user 'jira'@'localhost' identified by 'jira123';
GRANT ALL Privileges ON jiradb.* TO 'jira'@'localhost' IDENTIFIED by 'jira123' with grant option;
flush privileges;
exit
wget https://downloads.atlassian.com/software/jira/downloads/atlassian-jira-software-7.3.6-x64.bin
chmod +x atlassian-jira-software-7.3.6-x64.bin
./atlassian-jira-software-7.3.6-x64.bin
it will ask few of the questions.
#sudo ufw enable
#sudo ufw allow 8181
#sudo ufw allow 8005
service jira stop
service jira start
http://dev.mysql.com/downloads/file.php?id=457912
wget https://cdn.mysql.com//archives/mysql-connector-java-5.1/mysql-connector-java-5.1.36.zip
sudo unzip mysql-connector-java-5.1.36.zip
sudo cp mysql-connector-java-5.1.36-bin.jar /opt/atlassian/jira/lib/
