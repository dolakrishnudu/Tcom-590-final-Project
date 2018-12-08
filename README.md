# Tcom-590-final_project
Aim:- To configure interfaces and Routing Protocol using Ansible

1.All devices below are running Cumulus VX
2.by default username:- cumulus,Password:- CumulusLinux!
3.All the devices have 4 interfaces 
4.Management server has Dhcp configured which will be used to provide Ip's to eth0 and eth1 devices
5.eth0 is configured with dhcp by default
5.Make sure you are able to ssh to Switch 1 and 2 before you run ansible.
6.we will use ansible playbook to push interface, Routing Config and Restart services in the switches 


network topology

	11111111
	1      1
	1      1-----------
	1      1	  |
	11111111	  |
	Management	  |
	server      	  |
			  |
			111111111111
			|	   |
			|	   |
			/	    \
		      /		      \
		    /			\
		   |			 |
		1111111		      1111111
		1     1	Ospf area 0   1     1
	--------1     1---------------1	    1------------
	|	1     1		      1	    1		|
	|	1111111		      1111111		|
	|	Switch 1	     Switch 2		|
	|						|
	|						|
	|-------|				|-------|
	| Pc    |				| Pc    |
	|-------| 				|-------|

