 
- What is a mac address?
  - to uniquely identify a device in a network
  - contains hexadecimal digits (0-9 and A-F)
  - seperated by colons
  - operates at data link layer to ensure that data packets are delivered to the correct device on a local network.
 
- When is this MAC address used?: ff:ff:ff:ff:ff:ff
  - The MAC address "ff:ff:ff:ff:ff:ff" is a special MAC address known as the broadcast address. It is used in network communications to send data packets to all devices on a local network.
  - When a device wants to send a broadcast message, it sets the destination MAC address to "ff:ff:ff:ff:ff:ff". This indicates that the data should be delivered to every device on the network, rather than a specific individual device.


- Difference between ip and mac?
  - ip operated at network layer
  - mac operates at datalink layer
  - IP addresses are structured in a hierarchical manner and consist of two components: network address and host address. The network address identifies the network the device is connected to, while the host address identifies the specific device on that network.
  - IP addresses can change as devices move between networks or as network configurations are modified.
  - ip addresses consistes of 4 octets and mac consists of 6 pairs of hexadecimal digits


- What is ipv6?
   - IPv6 addresses are 128 bits in length, providing a significantly larger address space compared to the 32-bit addresses of IPv4. 
   - example 2001:0db8:85a3:0000:0000:8a2e:0370:7334
   - In this example, the IPv6 address consists of eight groups of four hexadecimal digits separated by colons. Each group represents 16 bits, and the address as a whole is 128 bits long.


- what is a subnet mask with example?
     - A subnet mask is a 32-bit value used in IP networking to divide an IP address into two parts: the network address and the host address. It helps determine which part of the IP address belongs to the network and which part belongs to the individual device or host within that network. <br/>
      - A subnet mask is represented using the same dotted decimal notation as an IP address, and it consists of four sets of numbers ranging from 0 to 255. Each set, like an IP address, represents 8 bits or one octet of the subnet mask. <br/>
      - For example, let's consider an IP address along with its corresponding subnet mask:
IP address: 192.168.1.100
Subnet mask: 255.255.255.0 <br/>
      - In this example, the subnet mask 255.255.255.0 indicates that the first three sets of the IP address (192.168.1) belong to the network, while the last set (100) represents the host within that network.
      - To understand it in binary: IP address: 11000000.10101000.00000001.01100100
Subnet mask: 11111111.11111111.11111111.00000000 <br/>
      - Here, the subnet mask has 24 leading 1s (representing the network portion) and 8 trailing 0s (representing the host portion).<br/>
      - The subnet mask is used by networking devices to determine whether a destination IP address is on the local network or needs to be routed to another network. By comparing the subnet mask with the IP address, devices can identify the network portion and make decisions accordingly. <br/>
      - In the given example, any IP address that starts with 192.168.1.x (where x represents any number from 0 to 255) would be considered part of the same local network. Devices on this network can communicate directly with each other without the need for routing. <br/>


- What is private ip? <br/>
       - Private IP addresses are assigned to the hosts in the same network to communicate with one another. As the name "private" suggests, the devices having the private IP addresses assigned can't be reached by the devices from any external network.










