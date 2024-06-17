<center><h1>Cybersecurity Incident Report</h1></center>
<div style="margin-top: 20px;">
  <div><b>Summary</b></div>
  <div>
    <p>tcpdump log indicates that a query sent in UDP packet for domain "www.yummyrecipesforme.com" and port 53 did not go through to the DNS server because no service was listening on the receiving DNS port. The message was "udp port 53 unreachable" and it being sent 3 (three times) with the same error. This may indicates a problem with DNS configuration </p>
  </div>
</div>

<div style="margin-top: 20px;">
  <div><b>Analysis</b></div>
  <div>
    <p>The incident occurs in the afternoon at 13:24:32 pm. Several customers reported that they were not able to access website www.yummyrecipesforme.com, and saw the error “destination port unreachable” after waiting for the page to load. I analyze DNS and ICMP traffic in transit using data from a network protocol analyzer tool and from tcpdump log, there are 3 (three) times a query in UDP packet failed to delivered from IP address 192.51.100.15 to www.yummyrecipesforme.com. From the log analysis I found from the log there was a problem with UDP port 53  where the UDP packet from 203.0.113.2 which is the IP address for "www.yummyrecipesforme.com" did not go through to the DNS server because no service was listening on the receiving DNS port.</p>
    <p>My next step is checking for Domain Name System (DNS) configuration as network security teams suspects there was misconfiguration in DNS network protocol </p>
  </div>
</div>
