Dynamic Host Configuration Protocol

Primarily use to assign IP addresses to host on a network.

DHCP client broadcasts itself to DHCP server to get an IP address. Then DHCP server responses and DHCP client configure itself according to this data.

Each IP is "leased" from the pool of IP addresses the DHCP server manages. The lease expiration time is configrable on the DHCP server. The client must reneve the lease if it wants to keep the address. If no renewal is received, the IP is available to other DHCP clients.

![[Pasted image 20220316163057.png]]

For configuring DHCP client in ubuntu: /[[etc]]/network/interfaces
