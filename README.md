                                                       Building a Basic Intrusion Detection Lab using Snort




1. Introduction:-

With the rapid growth of internet usage and digital systems, network security has become a critical concern for organizations and individuals alike. Cyber attacks such as unauthorized access, data breaches, and web-based exploits are increasing in both frequency and complexity. To address these threats, systems that can monitor and analyze network traffic in real time are essential. One such solution is an Intrusion Detection System (IDS), which helps in identifying suspicious or malicious activities within a network.
This project focuses on building a real-time IDS using Snort on Kali Linux. Snort is a widely used open-source tool capable of inspecting network packets and detecting potential threats based on predefined rules. In this implementation, the IDS is configured to generate instant alerts directly in the terminal, allowing users to observe attacks as they happen without relying on stored logs.
The system is designed to detect common types of attacks such as ICMP ping requests, port scanning, SQL injection, and cross-site scripting (XSS). These attacks are simulated in a controlled environment using tools like Nmap and Curl, making the project both practical and safe for learning purposes. By focusing on real-time monitoring and simplicity, the project provides a clear understanding of how intrusion detection works at a fundamental level.
Overall, this project serves as an introduction to network security concepts and demonstrates how a lightweight IDS can be implemented effectively. It also lays the groundwork for future improvements such as automated response mechanisms and advanced threat analysis systems.





2. Objectives:-

•	To design and implement a real-time Intrusion Detection System (IDS) using Snort on Kali Linux. 

•	To monitor network traffic continuously and identify suspicious or malicious activities. 

•	To detect common network attacks such as ICMP ping, port scanning, SQL injection, and cross-site scripting (XSS) using custom rules. 

•	To generate instant alerts directly in the terminal without relying on log storage. 

•	To simulate real-world attack scenarios in a controlled environment using tools like Nmap and Curl. 

•	To understand the working of rule-based detection systems and packet analysis. 

•	To build a lightweight and efficient IDS suitable for learning and demonstration purposes. 

•	To provide a foundation for future enhancements such as intrusion prevention systems (IPS) and automated alert mechanisms. 


3. Tools & Technologies Used:-
<img width="724" height="240" alt="Screenshot 2026-04-05 152449" src="https://github.com/user-attachments/assets/26bcc129-d048-468c-8430-f06cf9f3e398" />

•	Snort
Used as the core IDS engine to monitor network traffic and detect malicious activities based on predefined rules. 

•	Kali Linux
The operating system used for setting up the IDS environment, as it provides built-in tools for cybersecurity testing. 

•	Nmap
Used to simulate port scanning attacks and analyze how the IDS responds to suspicious network behavior. 

•	curl
Used to send HTTP requests for testing web-based attacks like SQL Injection and Cross-Site Scripting (XSS). 

•	Git
Used to manage and track changes in the project, as well as upload the project to GitHub. 

•	GCC
Used during the installation of Snort and its dependencies from source code. 

•	CMake
Used to configure and build the Snort 3 source during installation. 


4. Methodology:-

•	Update The Machine:
 
<img width="900" height="375" alt="image" src="https://github.com/user-attachments/assets/80c9b429-9a1f-4fd9-9380-8b6e83f1e5db" />
•	Installing SNORT and Requir ed libraries:-
 
<img width="900" height="573" alt="image" src="https://github.com/user-attachments/assets/13871e7e-6057-4489-a1d4-5c57b94e7583" />
<img width="900" height="510" alt="image" src="https://github.com/user-attachments/assets/91cf8657-e36a-474e-8ce1-33488eaf3170" />

•	Verify The SNORT Version:-
 <img width="900" height="284" alt="image" src="https://github.com/user-attachments/assets/257834c3-aa1b-41db-ba54-21c0a7cd29a1" />

•	Open The Required Directories:-
 <img width="900" height="191" alt="image" src="https://github.com/user-attachments/assets/84e01fdf-94aa-481b-a8ce-40560451c5d6" />

•	Update The local.rules using nano cmd:-
<img width="900" height="51" alt="image" src="https://github.com/user-attachments/assets/b6e28552-9063-4771-896d-379558d1edd3" />
<img width="900" height="174" alt="image" src="https://github.com/user-attachments/assets/abb36dc2-3f87-4d21-8e59-16a8f8906083" />
•	Then update The rules in snort.lua:-
<img width="900" height="41" alt="image" src="https://github.com/user-attachments/assets/75dd87fb-b64a-44c9-9050-f06ae80c38ed" />
<img width="900" height="160" alt="image" src="https://github.com/user-attachments/assets/e9fb5186-7656-47e6-8510-2888a6ac167a" />

•	Now Check the Network connection before running the snort cmd:-
 <img width="900" height="285" alt="image" src="https://github.com/user-attachments/assets/dd3de5e2-4c0b-48cb-b80d-c5a1d2d6c39c" />
Here we are using the eth0 network.

•	Now link the eth0 with the snort:-
 <img width="900" height="85" alt="image" src="https://github.com/user-attachments/assets/26544c31-dd54-450b-b68c-285296b9cabe" />

•	Then Execute the snort cmd:-
 <img width="900" height="195" alt="image" src="https://github.com/user-attachments/assets/daa42753-17da-4fe6-898e-b3539e5b14c5" />
After this the snort cmd starts the scan for the intrusion in the given ip.

•	Next we can ping the given ip to see the intrusion detection system:-
 <img width="900" height="361" alt="image" src="https://github.com/user-attachments/assets/a1fdf9d2-61e6-4389-9271-5c38587ddb0e" />
And we have got the desired outputs by running this command.
•	Next we can done the Same using the Nmap:-
 <img width="900" height="196" alt="image" src="https://github.com/user-attachments/assets/8874afba-9e9f-4d74-a206-33aff9814c0a" />
And I have also desired output for this.
•	Next,we are going to local web Server:-
 <img width="900" height="280" alt="image" src="https://github.com/user-attachments/assets/4f52f546-dd99-4e98-ad19-4d5b2499f1c4" />
•	Next we are attacking it using the web browser with the curl command:-
  rocess 
  <img width="900" height="491" alt="image" src="https://github.com/user-attachments/assets/6542988b-87a9-4ad2-a855-e4d22f290156" />

After running this the snort command automatically detects the intrusion in the given ip.And the outputs are shown in the upcoming contents.
According to the methodology I have done all the process and got the required outputs.


5. Findings :-

•	On giving the ping cmd this  is the snort results:
 <img width="834" height="594" alt="image" src="https://github.com/user-attachments/assets/8b5ddad3-ae78-4557-b871-f4507923ee3c" />
<img width="855" height="514" alt="image" src="https://github.com/user-attachments/assets/6965d428-870b-4e1f-a3b6-ec0bfbd2cb1b" />
<img width="900" height="385" alt="image" src="https://github.com/user-attachments/assets/256944a4-ad44-4a35-bb2b-a2015035c9c2" />

•	These are the findings of the scan using nmap:-
 <img width="920" height="511" alt="image" src="https://github.com/user-attachments/assets/8247aba3-4997-4790-b0dd-5a007f7019ee" />
<img width="900" height="283" alt="image" src="https://github.com/user-attachments/assets/f6c8fcd2-df5a-49d9-a925-2058e86e5146" />
<img width="900" height="546" alt="image" src="https://github.com/user-attachments/assets/6bf0c401-ebdd-4c70-ba11-fe7a9b3754ce" />

 These are the finding that I have got after doing the nmap scan.
•	These are the findings of the snort scan that I Done After the XSS Attack
<img width="824" height="608" alt="image" src="https://github.com/user-attachments/assets/d531c298-5d09-4bdb-97b1-bd2c4aa2c48f" />
 <img width="726" height="629" alt="image" src="https://github.com/user-attachments/assets/189e70ec-260d-4ed7-80e4-1e45ab75c317" />
<img width="900" height="256" alt="image" src="https://github.com/user-attachments/assets/4eda8f58-7d35-4798-99b7-9ca89005aa71" />
<img width="900" height="265" alt="image" src="https://github.com/user-attachments/assets/b561cebc-d557-41b0-a96b-811ce83cf770" />

These are the findings that I got using the XSS And I have Shown that the ping has been detected

6. Results:

The implemented Intrusion Detection System (IDS) was successfully tested in a controlled environment using Kali Linux. The system was able to monitor network traffic in real time and generate immediate alerts based on the predefined rules configured in Snort.
During execution, Snort was run in IDS mode on the loopback interface, allowing it to capture and analyze traffic generated within the same system. Various network-level attack scenarios were simulated to evaluate the effectiveness of the detection mechanism.
When ICMP traffic was generated using the ping command, the system successfully detected and displayed alerts indicating ICMP activity. Similarly, port scanning attempts performed using Nmap were identified, and appropriate alerts were triggered in the terminal.
One of the key outcomes of this project is the real-time alerting capability. All detected activities were displayed instantly in the terminal without any noticeable delay, demonstrating the system’s efficiency in live monitoring. Additionally, since no log files were used, the system remained lightweight and focused purely on real-time detection.
Overall, the results show that the implemented IDS is capable of detecting multiple types of network-level activities with good accuracy. The system performed reliably in identifying suspicious traffic and provides a simple yet effective solution for real-time network monitoring and intrusion detection.

7. Challenges Faced:

•	Installation Complexity
Setting up Snort 3 from source required installing multiple dependencies and resolving compatibility issues. The process was time-consuming and required careful execution of each step. 

•	Configuration Errors
Configuring the snort.lua file and linking custom rule files was challenging. Even small mistakes in syntax led to errors, which prevented Snort from running properly. 

•	Rule Syntax Issues
Writing custom rules required a clear understanding of Snort rule structure. Errors such as unsupported keywords (e.g., threshold) caused failures, and debugging these issues took time. 

•	Permission Problems
While editing configuration files (like /etc/snort/snort.lua), permission errors were encountered. These were resolved by using administrative privileges (sudo). 

•	Real-Time Traffic Capture
Selecting the correct network interface (such as lo) was important. Initially, incorrect interface selection resulted in no alerts being generated. 

•	Testing in a Single System
Since the project was implemented on a single Kali Linux machine, simulating real-world attack scenarios required additional effort using tools like Nmap and manual traffic generation. 

•	False Positives / Missed Alerts
Some rules either generated unnecessary alerts or failed to detect certain patterns, requiring multiple adjustments and testing to improve accuracy. 

•	Performance and Delay Concerns
During initial runs, there were slight delays in processing packets, especially when multiple rules were applied. Optimization was needed to ensure smooth real-time performance.

8. Conclusion:

This project successfully demonstrates the implementation of a real-time Intrusion Detection System (IDS) using Snort on Kali Linux. The system was able to monitor network traffic continuously and generate immediate alerts based on predefined rules, without relying on log storage. This approach made the system lightweight while still maintaining effective detection capabilities.
Through the use of custom rules, the IDS was able to identify network-level activities such as ICMP traffic and port scanning attempts. The real-time alerting feature proved to be efficient, as all suspicious activities were displayed instantly in the terminal, allowing quick observation and analysis.
The project also provided practical exposure to important concepts such as packet inspection, rule-based detection, and network traffic analysis. Challenges faced during installation, configuration, and testing helped in gaining a deeper understanding of how IDS systems function in real-world scenarios.
Overall, the project highlights how a simple and efficient IDS can be developed using open-source tools. It serves as a strong foundation for future enhancements such as intrusion prevention systems (IPS), automated response mechanisms, and advanced monitoring solutions.


9. References:
•	Snort Official Documentation
https://snort.org/documents 
•	Cisco Snort 3 User Manual
https://docs.snort.org 
•	Kali Linux Official Website
https://www.kali.org 
•	Nmap Official Documentation
https://nmap.org/docs.html 
•	curl Official Documentation
https://curl.se/docs/ 
•	GitHub Repositories for Snort Installation
https://github.com/snort3/snort3
https://github.com/snort3/libdaq














