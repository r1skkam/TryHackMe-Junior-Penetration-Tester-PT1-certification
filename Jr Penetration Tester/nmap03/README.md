[Nmap Advanced Port Scans](https://tryhackme.com/room/nmap03)

## Task 9 - Summary

| Port Scan Type | Example Command |
|---|---|
| TCP Null Scan |	sudo nmap -sN 10.10.147.63 |
| TCP FIN Scan |	sudo nmap -sF 10.10.147.63 |
| TCP Xmas Scan |	sudo nmap -sX 10.10.147.63 |
| TCP Maimon Scan |	sudo nmap -sM 10.10.147.63 |
| TCP ACK Scan |	sudo nmap -sA 10.10.147.63 |
| TCP Window Scan |	sudo nmap -sW 10.10.147.63 |
| Custom TCP Scan |	sudo nmap --scanflags URGACKPSHRSTSYNFIN 10.10.147.63 |
| Spoofed Source IP |	sudo nmap -S SPOOFED_IP 10.10.147.63 |
| Spoofed MAC Address |	--spoof-mac SPOOFED_MAC |
| Decoy Scan |	nmap -D DECOY_IP,ME 10.10.147.63 |
| Idle (Zombie) Scan |	sudo nmap -sI ZOMBIE_IP 10.10.147.63 |
| Fragment IP data into 8 bytes |	-f |
| Fragment IP data into 16 bytes |	-ff |

| Option |	Purpose |
|---|---|
| --source-port PORT_NUM | specify source port number |
| --data-length NUM | append random data to reach given length |

These scan types rely on setting TCP flags in unexpected ways to prompt ports for a reply. Null, FIN, and Xmas scan provoke a response from closed ports, while Maimon, ACK, and Window scans provoke a response from open and closed ports.

| Option |	Purpose |
|---|---|
| --reason |	explains how Nmap made its conclusion |
| -v |	verbose |
| -vv |	very verbose |
| -d	| debugging
| -dd	| more details for debugging
