# Tryhackme-Summit-Challenge

<h2>Introduction</h2>
I recently participated in the TryHackMe Summit challenge, a hands-on cybersecurity exercise simulating a collaborative purple team scenario. As a blue team member, I defended a network against a series of simulated malware attacks launched by a red team. This write-up details my approach to each challenge, showcasing the key security skills I utilized.

<br />

<h2>Key Skills demonstrated</h2>
<b> - Malware analysis and identification </b> <br/>
<b> - Firewall rule creation and implementation </b> <br/>
<b> - DNS filtering and configuration </b> <br/>
<b> - Sigma rule development for threat detection </b> <br/>
<b> - Network connection analysis and blocking </b> <br/>
<b> - Process monitoring and termination</b> <br/>


<h2>Challenge Walk-through</h2>

<h3>Questions</h3>
<p align="center">
<img src="https://i.imgur.com/A6K8Kog.png" height="80%" width="80%" alt="Summit challenge"/>

<h3>Task 1: Analysing Hashes</h3>

<b> - Objective: </b>
Identify malicious hashes from a provided sample file.<br/>

<b> - Action: </b>
Used PicoSecure to analyze the file, extracted hashes, and submitted them for verification. <br/>

<b> - Result: </b> 
Successfully identified and reported malicious hashes. <br/>

<p align="center">
<img src="https://i.imgur.com/5um6xL7.png" height="80%" width="80%" alt="Summit challenge"/>

In Image above, we got a mail from the Pentest team to analyse sample1.txt to analyse this executable file I use PicoSecure.

<p align="center">
<img src="https://i.imgur.com/r2VhIAB.png" height="80%" width="80%" alt="Summit challenge"/>

After analysing the sample1.txt we can see some Hash been generated, I now navigate to Manage Hashes to analyse the hash.

<p align="center">
<img src="https://i.imgur.com/rep4AiC.png" height="80%" width="80%" alt="Summit challenge"/>

After getting the hash, I submit the hash to get the first flag

<p align="center">
<img src="https://i.imgur.com/HizvRTE.png" height="80%" width="80%" alt="Summit challenge"/>

<h3>Task 2: Creating Firewall Rule</h3>

<b> - Objective: </b>
Block malicious network connections identified in the second sample. <br/>

<b> - Action: </b>
Analyzed the sample to identify suspicious network traffic, then created firewall rules to block the corresponding ports and protocols. <br/>

<b> - Result: </b> 
Implemented effective firewall rules to prevent malicious network access. <br/>

After getting the first flag, I am given the second executabele to analyse.

<p align="center">
<img src="https://i.imgur.com/lRxLKAs.png" height="80%" width="80%" alt="Summit challenge"/>

After analsying Sample2.txt, we can see there arec 3 TCP/UDP connectiosns and 1 HTTP(S) request. see the image below.

<p align="center">
<img src="https://i.imgur.com/6sn3QEU.png" height="80%" width="80%" alt="Summit challenge"/>

After seeing this, I am will need to craete a firewall rule usinging the Firewall Rule Manager

<p align="center">
<img src="https://i.imgur.com/GGV22zo.png" height="80%" width="80%" alt="Summit challenge"/>

After analysing sample2.txt, we are using the to create a firewall rule to get the second flag. See the image below that shows the second Flag
<br/>
<p align="center">
<img src="https://i.imgur.com/C2nCjbD.png" height="80%" width="80%" alt="Summit challenge"/>

<h3>Task 3: DNS Filtering</h3>

<b> - Objective: </b>
Prevent access to malicious domains identified in the third sample.<br/>

<b> - Action: </b>
Analyzed DNS requests, identified malicious domains, and configured DNS filtering to block them <br/>

<b> - Result: </b> 
Implemented DNS filtering to mitigate threats associated with malicious domains. <br/>


After getting the second flag, I am given the third executabele to analyse. After analysing I realise we have 2 DNS request which will be added to the DNS filter to deny access. See the image below.

<p align="center">
<img src="https://i.imgur.com/1f9VAIW.png" height="80%" width="80%" alt="Summit challenge"/>
<br />
<p align="center">
<img src="https://i.imgur.com/s3vwpJA.png" height="80%" width="80%" alt="Summit challenge"/>

Having discovered that there are 2 DNS request that are consodered malicious. Rules are created to deny these DNS connections and the Second flag is gotten. see the image below 

<p align="center">
<img src="https://i.imgur.com/iK4uird.png" height="80%" width="80%" alt="Summit challenge"/>
<br />
<p align="center">
<img src="https://i.imgur.com/ycMnCkW.png" height="80%" width="80%" alt="Summit challenge"/>

<h3>Task 4: Registry Modification</h3>

<b> - Objective: </b>
Detect and prevent malicious registry modifications.<br/>

<b> - Action: </b>
Used Sigma rule builder to create a rule targeting suspicious registry modifications, then implemented the rule using Sysmon event logs. <br/>

<b> - Result: </b> 
Successfully detected and prevented malicious registry changes that could compromise system security. <br/>


After getting the third flag, I am given the fourth executabele to analyse. After analysing I realise we have Registry activity which could be considered malicious, because the name says DisableRealtime Monitoring. See the image below.

<p align="center">
<img src="https://i.imgur.com/jBlx8QV.png" height="80%" width="80%" alt="Summit challenge"/>
<br />
<p align="center">
<img src="https://i.imgur.com/6qdQvdr.png" height="80%" width="80%" alt="Summit challenge"/>

After dicovering this malicous activity I used the sigma Rule Builder using Sysmon Event Logs, I use the Registry Modification to change the rule created see the Image below.

<p align="center">
<img src="https://i.imgur.com/y2GifbM.png" height="80%" width="80%" alt="Summit challenge"/>
<br />
<p align="center">
<img src="https://i.imgur.com/2DZu0Ea.png" height="80%" width="80%" alt="Summit challenge"/>

After applying this rule I got the fourth Flag. which bring about the fifth Flag.

<h3>Task 5: Network Connections</h3>

<b> - Objective: </b>
 Identify and block suspicious network connections.<br/>

<b> - Action: </b>
Analyzed network connection logs, identified anomalous patterns, and created rules to block malicious connections. <br/>

<b> - Result: </b> 
Implemented rules to prevent unauthorized network access and potential data exfiltration. <br/>


After getting the fourth flag, I am given the fifth executabele to analyse. After analysing the fifth flag we got a connection logs and the analysed data. From the analysed Data and the connection Log a rule is created to find the sixth flag. See the image below that shows the rule created in the Network connection.

<p align="center">
<img src="https://i.imgur.com/6IksIFb.png" height="80%" width="80%" alt="Summit challenge"/>

<h3>Task 6: Process Creation</h3>

<b> - Objective: </b>
Detect and terminate malicious processes.<br/>

<b> - Action: </b>
Analyzed process creation events, identified suspicious processes, and terminated them using appropriate tools. <br/>

<b> - Result: </b> 
Prevented malicious processes from executing and compromising system integrity. <br/>


After getting the fifth flag, I am given the sixth executabele to analyse. After analysing the sixth flag we got the analysed data, I found a malicious file Process and i created a rule to stop this process see the image below.

<p align="center">
<img src="https://i.imgur.com/WYkr8MF.png" height="80%" width="80%" alt="Summit challenge"/>

Here are the answers with the flags 
<p align="center">
<img src="https://i.imgur.com/p0i9l9g.png" height="80%" width="80%" alt="Summit challenge"/>
