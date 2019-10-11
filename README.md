# CiscoASAv
Install/Configure cisco asav981 and how to enable ASDM and how to access ASDM launcher on win10

Download link : https://mega.nz/#!wINQGCIT!B8ss0CMyemfV1WFdUe7GjMAxd1rEgb2QMJDf5x7NVuY 

In this Page you will learn how to deploy and Cisco ASAv on VMware esxi 6.7 and install ASDM and how to launch ASDM.

Login in to Esxi websphere client from your fav brower and Deploy a virtual machine from an OVF or OVA file.

Download the Files from the link provided.

and import it them to Esxi 6.7 and after the import it needs few configurations.





Initial configuration:

ASA will reboot after initilizating the system varialbes.

Hostname> enable

Hostname#show version
Hostname#sh ip
Hostname#config terminial  press option (A)
Hostname(Config)# init g0/1
Hostname(Config -if)# ip address  192.168.29.123 255.255.255.0
Hostname(Config -if)#  nameif inside
Hostname(Config -if)# no shutdown
Hostname(Config -if)# exit
Hostname(Config)# sh ip 
Hostname(Config)# 
Hostname(Config)# 

create a user and give it a highest privilage 15 
Hostname(Config)# username test password test privilage 15 

we get the ASDM preloaded on this version 

So enabling http access
Hostname(Config)# http server enable
Hostname(Config)# ssh 0.0.0.0 0.0.0.0 inside 
Hostname(Config)# http 0.0.0.0 0.0.0.0 inside 
Hostname(Config)# write memory 


Hostname(Config)sh run
