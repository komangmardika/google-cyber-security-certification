<h1>Cybersecurity Incident Report</h1>
<div style="border: 1px solid #ccc">
  <p>Review the following scenario. Then complete the step-by-step instructions.</p>
  <p>You work as a security analyst for a travel agency that advertises sales and promotions on the company’s website. The employees of the company regularly access the company’s sales webpage to search for vacation packages their customers might like. </p>
  <p>One afternoon, you receive an automated alert from your monitoring system indicating a problem with the web server. You attempt to visit the company’s website, but you receive a connection timeout error message in your browser.</p>
  <p>You use a packet sniffer to capture data packets in transit to and from the web server. You notice a large number of TCP SYN requests coming from an unfamiliar IP address. The web server appears to be overwhelmed by the volume of incoming traffic and is losing its ability to respond to the abnormally large number of SYN requests. You suspect the server is under attack by a malicious actor. </p>
  <p>You take the server offline temporarily so that the machine can recover and return to a normal operating status. You also configure the company’s firewall to block the IP address that was sending the abnormal number of SYN requests. You know that your IP blocking solution won’t last long, as an attacker can spoof other IP addresses to get around this block. You need to alert your manager about this problem quickly and discuss the next steps to stop this attacker and prevent this problem from happening again. You will need to be prepared to tell your boss about the type of attack you discovered and how it was affecting the web server and employees.</p>
</div>
<hr />
<div style="margin-top: 20px;">
  <div>
    One potential explanation for the website's connection timeout error message is DoS attack specifically SYN flooding.
  </div>
  <div>
    The logs show that there are abnormal number of SYN requests coming in at a rapid pace.
  </div>
  <div>
    This event could be SYN flooding - one of DoS attack kind.
  </div>
</div>

<div style="margin-top: 20px;">
  <div>
    When website visitors try to establish a connection with the web server, a three-way
handshake occurs using the TCP protocol. 
    <ol>
      <li>A SYN packet is sent from the source to the destination, requesting to connect.</li>
      <li>The destination replies to the source with a SYN-ACK packet to accept the connection request. The destination will reserve resources for the source to connect.</li>
      <li>A final ACK packet is sent from the source to the destination acknowledging the permission to connect.</li>
    </ol>
  </div>
  <div>
    the flooding of SYN packet from attacker making visitors cannot establish or maintain a connection to the web server, the web server then stops responding.      
  </div>  
  <div>
    Explain what the logs indicate and how that affects the server:    
    the attacker begin to send more and more SYN request to server. There are 20 suspicious rows of log begins to reflect the struggle the web server is having to keep up with the abnormal number of SYN requests coming in at a rapid pace.
  </div>
</div>
