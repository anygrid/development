**Installing and Configuring Zabbix Agent**

Edit apt source list to add the PPA:

sudo nano /etc/apt/sources.list

Add the following items at the end of the file:

deb http://ppa.launchpad.net/tbfr/zabbix/ubuntu precise main
deb-src http://ppa.launchpad.net/tbfr/zabbix/ubuntu precise main

Save&close&run.

sudo apt-get update
sudo apt-get install zabbix-agent

sudo apt-get update
sudo apt-get install zabbix-agent

Next, we need to update the configuration files:

sudo nano /etc/zabbix/zabbix_agentd.conf

Edit the "Server" property to reflect the IP Address of the Zabbix server. For the agent configuration on the Zabbix server, you can use "127.0.0.1":

Server=Zabbix.Server.IP.Address

Adjust the "Hostname" property to reflect the hostname of the machine being monitored.

Hostname=Hostname_Of_Current_Machine

Save and close the file.

Restart the agent software:

sudo service zabbix-agent restart


