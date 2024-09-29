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

After analysing the sample1.txt we can see some Hash been generated, I now navigate to <b>Manage Hashes<b/> to analyse the hash.

<p align="center">
<img src="https://i.imgur.com/rep4AiC.png" height="80%" width="80%" alt="Summit challenge"/>

After getting the hash, I submit the hash to get the first flag

<p align="center">
<img src="https://i.imgur.com/HizvRTE.png" height="80%" width="80%" alt="Summit challenge"/>


<h3>Task 2: Creating Firewall Rule</h3>

After geeting the first flag, I am given the secound executabele to analyse see 

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
