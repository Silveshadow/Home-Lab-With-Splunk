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

I was able to access the splunk enterprise instance hosted on port 8000.

![Capture2](https://github.com/Silveshadow/Home-Lab-With-Splunk/blob/main/Step%204.png)

# Step 5

I was able to login with the credentials I created veryifing that the instance was operational.


![Capture2](https://github.com/Silveshadow/Home-Lab-With-Splunk/blob/main/Step%205.png)

# Step 6

I proceeded to configure data ingestion for endpoint monitoring by navigating to the Add Data section. Within this interface, I selected Forwarding and Receiving to establish a forwarder configuration for collecting logs from endpoint scanning solutions critical for centralized log aggregation, enabling comprehensive visibility into endpoint activity and facilitating SOC monitoring and threat detection workflows.

![Capture2](https://github.com/Silveshadow/Home-Lab-With-Splunk/blob/main/Step%206.png)

# Step 7

To continue the configuration of the endpoint data ingestion pipeline, I navigated to and selected Configure Receiving enabling the instance to accept incoming data from remote forwarders.

![Captureii](https://github.com/Silveshadow/Home-Lab-With-Splunk/blob/main/Step%207.png)

# Step 8

I specified a listening port 9997 for the instance to receive forwarded logs ensuring secure and structured data ingestion from remote endpoints.

![Capture;;](https://github.com/Silveshadow/Home-Lab-With-Splunk/blob/main/Step%208.png)

# Step 9

I went to my personal Windows workstation and deployed the Splunk Universal Forwarder. During installation, I created a dedicated forwarding account with administrative credentials to securely transmit endpoint logs to the Splunk Enterprise instance. This configuration establishes the foundation for continuous log collection and centralized monitoring, enabling enhanced visibility into endpoint activity and supporting proactive threat detection in the SOC environment.

![eee](https://github.com/Silveshadow/Home-Lab-With-Splunk/blob/main/Step%209.png)

# Step 10

I entered the deployment server IP address and port to ensure the forwarder could communicate with the central Splunk instance for configuration and management purposes.

![Capturedd](https://github.com/Silveshadow/Home-Lab-With-Splunk/blob/main/Step%2010.png)

#Step 11

I configured the receiving indexer IP address and listening port to align with the previously defined Splunk Enterprise receiving port. This configuration enables secure and reliable log forwarding from the endpoint to the central Splunk instance.

![Capturedd](https://github.com/Silveshadow/Home-Lab-With-Splunk/blob/main/Step%2011.png)

#Step 12

To enable the forwarding account to transmit logs effectively, I navigated to Add Data → Data Inputs within the Splunk Enterprise dashboard. This step establishes the connection between the forwarder and the Splunk data ingestion pipeline, allowing the endpoint to send logs for centralized monitoring, analysis, and threat detection in the SOC environment.

![Capturedd](https://github.com/Silveshadow/Home-Lab-With-Splunk/blob/main/Step%2012.png)


#Step 13

I navigated to the TCP/UDP input method and configured the system to listen on port 9997 ensuring that logs forwarded from endpoints are received through a dedicated and secure communication channel.

![Capturedd](https://github.com/Silveshadow/Home-Lab-With-Splunk/blob/main/Step%2013.png)

#Step 14

I defined the source type for the incoming endpoint data as “wineventlog”. Assigning the appropriate source type enables Splunk to parse and categorize Windows Event Logs accurately facilitating efficient indexing and search capabilities.

![Capturedd](https://github.com/Silveshadow/Home-Lab-With-Splunk/blob/main/Step%2014.png)

#Step 15

Finally, I created a dedicated index within the Splunk Enterprise environment to store the incoming endpoint logs, naming it “win_log”

![Capturedd](https://github.com/Silveshadow/Home-Lab-With-Splunk/blob/main/Step%2015.png)

