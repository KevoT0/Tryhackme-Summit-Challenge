# Tryhackme-Summit-Challenge

<h2>Description</h2>
This is an hands-on cybersecurity challenge exercise that simulates a purple team scenario. In this challenge, I play a role of a blue team member, I was tasked with defending a network agaonist simulated malware attacks.
<br />

<h2>Key Aspects</h2>
<b> - Malware Detection </b> <br/>
<b> - Threat Prevention </b> <br/>
<b> - Pyramid of Pain  </b> <br/>

<h2>Challenge Walk-through</h2>

<h3>Questions</h3>
<p align="center">
<img src="https://i.imgur.com/A6K8Kog.png" height="80%" width="80%" alt="Summit challenge"/>

<h3>Task 1: Analysing Hashes</h3>
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

After geeting the first flag, I am given the second executabele to analyse.

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

After getting the fourth flag, I am given the fifth executabele to analyse. After analysing the fifth flag we got a connection logs and the analysed data. From the analysed Data and the connection Log a rule is created to find the sixth flag. See the image below that shows the rule created in the Network connection.

<p align="center">
<img src="https://i.imgur.com/6IksIFb.png" height="80%" width="80%" alt="Summit challenge"/>

<h3>Task 6: Process Creation</h3>

After getting the fifth flag, I am given the sixth executabele to analyse. After analysing the fifth flag we got a connection logs and the analysed data. From the analysed Data and the connection Log a rule is created to find the sixth flag. See the image below that showws the rule created in the Network connection.

<p align="center">
<img src="https://i.imgur.com/WYkr8MF.png" height="80%" width="80%" alt="Summit challenge"/>
