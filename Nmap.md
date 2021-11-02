# Nmap

for ping sweep we use -sn as an example nmap 192.168.0.0/24

Nmap is the tool for the Network scanning

for class B networks the netmask is /16

# NSE(Nmap Scripting Engine)

____________________________________________________________

NSE written in Lua language. 

Work - Scanning for vulnerabilities to automating exploits for them.

Type - Recon

There are many category some useful are :

# Working with NSE :

for activating the NSE switch we use   - - script for the use vuln category  - -script=vuln

To run the specific script  - -script=<specific-script>

For the running multiple script   - -script=smb-enum-users, smb-enum-shares

some scripts require arguments     - -script-args 

The scripts are present in

```bash
									/usr/share/namp/scripts
# We read many scripts in scripts direcotry for know the script dependencies look at the 
	        dependencies{} 

# If you want to check what argument script uses
	 
							nmap --script-help <--script-name>
```

# **Firewall Invasion**

For Windows scan we use **-Pn** to bypass from Firewall .

-f is used to make it fragment (split into smaller pieces)  and making it less likely that packets are detected by the firewall or ids.

Alternatively to -f, but providing more control over the size of the packets - -mtu <number> the number is must be the multiple of 8.

- `-scan-delay <time>ms`:- used to add a delay between packets sent. This is very useful if the network is unstable, but also for evading any time-based firewall/IDS triggers which may be in place.
- `-badsum`:- this is used to generate in invalid checksum for packets. Any real TCP/IP stack would drop this packet, however, firewalls may potentially respond automatically, without bothering to check the checksum of the packet. As such, this switch can be used to determine the presence of a firewall/IDS.

j

[John Hammond](Nmap%208a7e82d7840b4a5197fa5fb9d2a17466/John%20Hammond%20e7204ba9d62d4fceb2ee6eab906b5857.md)