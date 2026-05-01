# Home Lab with Splunk

## Project Overview 

I downloaded Splunk Enterprise Linux (amd64) using the wget command-line utility. The package was retrieved directly from the official Splunk distribution repository, ensuring integrity and authenticity of the software.

![Step 1.png](https://github.com/Silveshadow/Home-Lab-With-Splunk/blob/main/Step%201.png)


# Step 2:

I executed a privileged command to extract the downloaded .tgz archive into the /opt directory. This step effectively deployed the Splunk Enterprise binaries and supporting files, preparing the environment for initialization.


![Capture](https://github.com/Silveshadow/Home-Lab-With-Splunk/blob/main/Step%202.png)

# Step 3

I started the Splunk daemon (splunkd), triggering the initialization process. During this phase, the system performed configuration checks, generated necessary certificates, and initialized default directories and services. Additionally, the Splunk web interface was enabled on port 8000, and initial administrative credentials were configured, allowing secure access to the platform for further monitoring and analysis tasks.

![Capture3](https://github.com/Silveshadow/Home-Lab-With-Splunk/blob/main/Step%203.png)

# Step 4

I accessed the Wazuh dashboard by navigating to the Linux host’s IP address over HTTPS (port 443), confirming secure connectivity to the SIEM interface.


![Capture2](https://github.com/Silveshadow/Home-Lab-With-Splunk/blob/main/Step%204.png)

# Step 5

Upon successful authentication, I reviewed the centralized dashboard, which provided visibility into security events, alerts, and identified vulnerabilities across the environment. The interface allowed me to monitor alert severity levels and gain insight into potential threats and system exposures in real time.


![Capture2](https://github.com/Silveshadow/Home-Lab-With-Splunk/blob/main/Step%205.png)

# Step 6

To extend endpoint visibility, I deployed the Wazuh Agent on a Windows system. After installation, I configured the agent to communicate with the Wazuh manager by specifying the manager’s IP address and importing the authentication key. This enabled secure registration of the endpoint.

![Capture2](https://github.com/Silveshadow/Home-Lab-With-Splunk/blob/main/Step%206.png)

# Step 7

During the initial deployment, the Wazuh agent failed to connect to the manager, as indicated in the log: the connection attempt to 192.168.86.209:1514 was unsuccessful. Upon investigation, it was determined that the authentication key configured on the agent was incorrect, preventing successful communication with the SIEM manager.

![Captureii](https://github.com/Silveshadow/Home-Lab-With-Splunk/blob/main/Step%207.png)

# Step 8

After retrieving the correct authentication key, the agent was reconfigured and successfully started.

![Capture;;](https://github.com/Silveshadow/Home-Lab-With-Splunk/blob/main/Step%208.png)

# Step 9

Cheching the logs confirmed that the agent established a connection with the Wazuh manager, and all relevant modules, including File Integrity Monitoring (FIM), initialized correctly. Policy evaluations and security configuration assessments executed as expected, indicating the agent is now fully operational and actively monitoring the endpoint.

![eee](https://github.com/Silveshadow/Home-Lab-With-Splunk/blob/main/Step%209.png)

# Step 10

I went back to my linux virtual machine and saw that the agent account was able to connect to the SIEM manager

![Capturedd](https://github.com/Silveshadow/Home-Lab-With-Splunk/blob/main/Step%2010.png)

#Step 11

Finally, I was able to review the most recent alerts demonstrating that the agent is actively collecting and forwarding security telemetry to the manager. The alert data includes detailed system and network activity, indicating that monitoring and compliance modules are functioning as expected.

![Capturedd](https://github.com/Silveshadow/Home-Lab-With-Splunk/blob/main/Step%2011.png)

#Step 12

Finally, I was able to review the most recent alerts demonstrating that the agent is actively collecting and forwarding security telemetry to the manager. The alert data includes detailed system and network activity, indicating that monitoring and compliance modules are functioning as expected.

![Capturedd](https://github.com/Silveshadow/Home-Lab-With-Splunk/blob/main/Step%2012.png)


#Step 13

Finally, I was able to review the most recent alerts demonstrating that the agent is actively collecting and forwarding security telemetry to the manager. The alert data includes detailed system and network activity, indicating that monitoring and compliance modules are functioning as expected.

![Capturedd](https://github.com/Silveshadow/Home-Lab-With-Splunk/blob/main/Step%2013.png)

#Step 14

Finally, I was able to review the most recent alerts demonstrating that the agent is actively collecting and forwarding security telemetry to the manager. The alert data includes detailed system and network activity, indicating that monitoring and compliance modules are functioning as expected.

![Capturedd](https://github.com/Silveshadow/Home-Lab-With-Splunk/blob/main/Step%2014.png)

#Step 15

Finally, I was able to review the most recent alerts demonstrating that the agent is actively collecting and forwarding security telemetry to the manager. The alert data includes detailed system and network activity, indicating that monitoring and compliance modules are functioning as expected.

![Capturedd](https://github.com/Silveshadow/Home-Lab-With-Splunk/blob/main/Step%2015.png)

#Step 16

Finally, I was able to review the most recent alerts demonstrating that the agent is actively collecting and forwarding security telemetry to the manager. The alert data includes detailed system and network activity, indicating that monitoring and compliance modules are functioning as expected.

![Capturedd](https://github.com/Silveshadow/Home-Lab-With-Splunk/blob/main/Step%2016.png)

#Step 17

Finally, I was able to review the most recent alerts demonstrating that the agent is actively collecting and forwarding security telemetry to the manager. The alert data includes detailed system and network activity, indicating that monitoring and compliance modules are functioning as expected.

![Capturedd](https://github.com/Silveshadow/Home-Lab-With-Splunk/blob/main/Step%2017.png)
