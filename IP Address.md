
For a device on a network to communicate properly, it needs 3 pieces of information.
IP address, subnet mask and broadcast address.
Each of them are four seperated octets from 0 to 255
octet.octet.octet.octet

Ip consists of two parts:
Network address and Host address.
Each must be unique for proper routing.
Address classes are used to determine the network address and host addresses.

![[Pasted image 20220316151218.png]]

![[Pasted image 20220316151347.png]]

For class A first octet is for network and others for host addresses.
For class B first two octet is for network and others for host addresses.
For class C first three octet is for network and the last one is for host addresses.

For example the ip address 183.194.46.31 is a class B. 183 and 194 is the network portion of the address and 46.31 is the host portion.

Broadcast address is special logical address used to send data to all hosts on a given network.

![[Pasted image 20220316151827.png]]

---------------

CIDR - Classles Inter-Domain Routing
It allows network to be subdivided regardles of their traditional class.
Subdivided networks = Subnets.
![[Pasted image 20220316152334.png]]

![[Pasted image 20220316152610.png]]

-----------------

To show current ip address or to see ip addresses used on the current system:
*ip address*

Sample output:
![[Pasted image 20220316155344.png]]
You can see two listed devices.
lo device is called loopback device. It is a special network interface for linux to communicate itself. Ip address of this device is 127.0.0.1

The other one is an actual hardware network device.

*ifup* and *ifdown* commands are used to bring up and down the network interfaces:
*ifup eth0*

Another command to see ip address is *ifconfig* and it is deprecated.


-------------------------------


![[Pasted image 20220316163228.png]]

For assigning a static IP address on Ubuntu: /[[etc]]/network/interfaces


---------------------------------------


![[Pasted image 20220316163352.png]]

