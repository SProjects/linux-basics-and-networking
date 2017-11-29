# Assessment 02 - Networking

This contains a list of questions to assess a fellows knowledge of the **Networking** Learning Outcome

## Questions

1. Display network interfaces

	```
  	ifconfig -a
  	```

2. Display network routing table

  	```
  	netstat -rn
  	```

3. Disable **ICMP** ping requests to your local machine

	```
	iptables -A INPUT -p icmp --icmp-type echo-request -j REJECT
	```

4. Use a subnet mask to allocate IP addresses on a network

  	Given the ip range **10.0.10.0/24**

  	```
  	minimum_ip_address="10.0.10.1"
  	maximum_ip_address="10.0.10.255"
  	```

  	Given the ip range **10.0.10.0/30**

  	```
  	minimum_ip_address="10.0.10.1"
  	maximum_ip_address="10.0.10.3"
  	```

5. Use `ssh` to forward port **2444** on remote machine **10.0.0.1** to local port **6333**

  	```
	ssh -L 6333:localhost:2444 10.0.0.1
  	```

6. Using `ssh` with authentication agent forwarded, connect to remote machine **10.0.0.1**

	```
	
	```

7. Using `ssh`, connect to remote machine **10.0.0.1** with the private key `private.key.pem`

	```
	ssh -i ~/.ssh/private.key.pem user@10.0.0.1
	```

8. Using `scp`, copy file `/home/user/file.txt` on remote machine **10.0.0.1** to your local machine

	```
	scp -i ~/.ssh/<private-key>.pem <user>@10.0.0.1:~/path/to/remote/file.txt /home/user/
	```

9. Using `scp`, copy local file at `/home/user/file.txt` to remote machine **10.0.0.1**

	```
	scp -i ~/.ssh/<private-key>.pem /home/user/file.txt <user>@10.0.0.1:~/path/to/remote/location/
	```

10. List all open ports on a system

	```
	netstat -lntu
	```

11. Block ip address from accessing all ports on your local machine using iptables

	```
	iptables -A FORWARD -p tcp -d <blocked-ip-address> -j DROP
	```

12. List differences between IPV4 & IPV6 addresses

	```
	1. An IPv6 address consists of 128 bits, while an IPv4 address consists of only 32.
	2. IPv6 has a lot more usable addresses compared to IPv4.
	3. IPv6 makes the router’s task more simple compared to IPv4.
	4. IPv6 is better suited to mobile networks than IPv4.
	5. IPv6 addresses are represented in a hexadecimal, colon-separated notation, while IPv4 address use the dot-decimal notation.
	6. IPv6 allows for bigger payloads than what is allowed in IPv4.
	7. IPv6 is used by less than 1% of the networks, while IPv4 is still in use by the remaining 99%.
	```

