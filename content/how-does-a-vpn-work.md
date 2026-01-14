Title: How does a VPN work?
Date: 2026-01-14 10:14
Category: How-Tos
Tags: updates
Slug: how-does-a-vpn-work
Keywords: vpn, security
Authors: Colin Shevlin
Summary: I try to explain what a VPN does and why it's useful. 

### An introduction to the Internet's phone book. 

The Internet was built on older networks: namely, the phone network. In a phone network, you can call anyone who is connected so long as you have their phone number. Let's imagine a simple phone book: 

| Name    	| Phone number     	|
|---------	|------------------	|
| Picard  	| +33 76 43 23 45  	|
| Riker   	| +1 907 555 2384  	|
| O'Brien 	| +353 76 74 23 12 	|

If you call one of the numbers in this book, you get the person associated with that number. If you don't know someone's number, you can use this phone book to look the number up. 

The Internet also has a phone book. It's called the Domain Name System, or DNS. In DNS, each website is associated with a number: its IP address. An IP address is like a website's phone number. 

| Name          	| IP address    	|
|---------------	|-----------------	|
| google.com    	| 142.250.191.142 	|
| instagram.com 	| 157.240.245.174 	|
| wikipedia.com 	| 208.80.154.232  	|

On the Internet, there are DNS servers that store lots of records like the ones in the table above. When you type in a web address into your browser, your computer makes a request to a DNS server to find the IP address of the website you'd like to visit. It finds the record, and you can connect to the website by making requests to its IP address. 

### DNS and privacy

This system of making a request to a DNS server presents a privacy problem. DNS requests are largely unencrypted, so that means the websites you lookup with the DNS server are public to interlopers such as your internet service provider, any system in transit between you and the DNS server, or anyone on your Wifi network (think a Wifi network at a coffee shop). 

This means that any one of those parties can see what sites you go to and infer what you were doing. For example, if I was eavesdropping on DNS requests and I saw that a user was making a lot of DNS requests for sites on beekeeping, I could infer that they were getting into beekeeping (or already a beekeeper! Imagine!). When combined with location data such as where your network is physically located, these inferences can become very powerful. 

### What is a VPN?

A VPN stands for virtual private network. When you turn on a VPN, your computer connects to a private network and makes requests from that network instead of the network that you're connected to. 

This means that your DNS traffic looks different. Anyone monitoring your traffic, such as an interloper on the coffee shop Wifi network or your internet service provider, does not see your DNS requests. Instead, your requests get routed first to the VPN and then to the larger Internet. 

For example, let's say that your VPN provider allows you to select a VPN in Chicago. First, your device will establish a connection to this Chicago VPN. Once that connection is established, Internet traffic will appear to come from that address in Chicago rather than the Wifi that your device is connected to. This means that DNS requests are also sent from that VPN and are much harder to trace back to you. 

### Safety considerations

When using a VPN, you want to select a VPN provider you trust. If I wanted to get a lot of information about network traffic, I could create a virtual private network myself and advertise free VPN access. Then when users joined my VPN, I could save their device information and all their DNS requests, effectively duplicating the privacy problem they were trying to avoid by using a VPN. Be sure to only use VPNs from trusted providers like [Proton](https://protonvpn.com/download) or [NordVPN](https://nordvpn.com/country/usa/).