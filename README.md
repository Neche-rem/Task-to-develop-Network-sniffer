Before Using this we must have:
1. Python 3 installed on your system.
2. Scappy, this can be installed using the command: pip install scappy

This project is a network sniffer built using Python and the scapy library. It captures, analyzes, and logs network traffic, offering insights into the flow of data within a network.
It captures packets using the sniff() function with optional filtering.
It extracts and prints detailed information about each packet, including source IP, destination IP, protocol, and payload.
It can save the captured packets to a PCAP file for later analysis.
The script allows the user to specify the number of packets to capture and whether to save them.

The payload is generated in binary format. If the payload is binary or non-text data, converting it to text might not make sense, and it's often best to leave it in its raw byte-string format for accuracy.
To generate it in human readable form, you can write this instead.

if packet.haslayer(IP):
        ip_src = packet[IP].src
        ip_dst = packet[IP].dst
        proto = packet[IP].proto
        payload = (packet[IP].payload)
