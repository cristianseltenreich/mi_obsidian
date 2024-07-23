###  Splunk Installation on Linux

For this part, we will use an Ubuntu 22.04 Desktop computer. It will work with other distributions and a server one, but since I used the VM for other things it will be easier. 
  
### Installation via GUI

1- Go to the Splunk Site  
2- Create an account  
3- Download the .deb file

![[Pasted image 20240227185418.png]]

4- Go to your Downloads folder

![[Pasted image 20240227185446.png]]

5- Right Click on it > Open with Other Applications > Software Install

![[Pasted image 20240227185506.png]]

Click on the "Install" button and wait.

![[Pasted image 20240227185525.png]]

Then it will install successfully.

### Installation via CLI

1-Go to the Splunk Site  
2-Create an account  
3-When you try to download it, check the upper right corner

![[Pasted image 20240227185553.png]]

4-Click on "Command Linux Wget", it will give you the command you need to download it.  
5-For this section, I will use the tgz format

![[Pasted image 20240227185610.png]]

6-Open your terminal  
7-Go to your installation folder (/opt for me)  
8-Paste the command given a few steps ago  
9-Add "sudo" if needed

![[Pasted image 20240227185627.png]]

10-Go to root user  
11-Extract it with this command:

| tar xvzf splunk-9.0.1-82c987350fde-Linux-x86_64.tgz |
| --------------------------------------------------- |

12-Launch it: /opt/splunk/bin/splunk start --accept-license  
13-Answer the questions

![[Pasted image 20240227185656.png]]

14-Try to connect to the link given

![[Pasted image 20240227185709.png]]

![[Pasted image 20240227185717.png]]

15-Check The Splunk Installation

  

By default, Splunk on Linux doesn't run at the system startup. To make it start, run this command in root:

| /opt/splunk/bin/splunk enable boot-start |
| ---------------------------------------- |
![[Pasted image 20240227185734.png]]

Restart and check the status:

|/opt/splunk/bin/splunk status|
|---|
![[Pasted image 20240227185802.png]]

If you look at the output, Splunk started successfully.

Answers

![[Pasted image 20240227185953.png]]

![[Pasted image 20240227190029.png]]

