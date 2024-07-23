### Splunk Universal Forwarders

For the training, we are going to install the universal forwarder in the default configuration. Our goal is to send Windows logs to Splunk.

- Go to the Windows computer  
- Download the [setup file](https://www.splunk.com/en_us/download/universal-forwarder.html)

![[Pasted image 20240227190750.png]]

- Read the Splunk General Terms - Download the MD5

  ![[Pasted image 20240227190851.png]]
  
- Open the md5 file to have the checksum: at this time is: 83a09c64537832701320609e665e3e7  
- Check your MD5 with this PowerShell command "Get-FileHash .\splunkforwarder-9.0.0.1-9e907cedecb1-x64-release.msi -Algorithm md5" to confirm you've got the right installer.

![[Pasted image 20240227190916.png]]

Launch the setup  
Read the Licence Agreement

![[Pasted image 20240227190937.png]]

Accept the Licence Agreement  
Select "an on-premises Splunk Enterprise instance" because we have to install Splunk on an on-premise server.

![[Pasted image 20240227191101.png]]

Once again, we use the default configuration. Maybe in your company, you will use a service account to run the Universal Forwarder.

- Give a username to Universal Forwarder.  
- Give the server IP or Hostname and the port to the receiving indexer. I use the IP because I have no DNS in my lab. We don't have to change any configuration during Splunk installation so the port used is 9997
![[Pasted image 20240227191220.png]]

Why do we give IP in receiving indexer and not in the deployment server? Because we don't have a Deployment server. A deployment server is a server that can send a configuration for your universal forwarder.

- Launch the install
### Check Universal Forwarder for Windows Installation

- Go to services.msc  
- Check if "SplunkForwarder Service" is up.
- 
![[Pasted image 20240227191242.png]]

- Check if communication is open with Powershell command: "Test-NetConnection -Computername Splunk_IP -port 9997)"

![[Pasted image 20240227191302.png]]

Congratulation, you have installed Splunk!

### Check on Splunk

- Go to your Splunk Server  
- Go to Settings > Forwarder management

![[Pasted image 20240227191327.png]]

You must see your Windows Computer on this page.


![[Pasted image 20240227191354.png]]

  
If you don't see your computer after a few minutes, try to restart the Splunk Universal Forwarder service, and check if the connection between client and server is okay.


