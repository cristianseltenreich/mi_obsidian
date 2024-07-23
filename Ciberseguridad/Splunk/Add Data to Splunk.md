### Add Data to Splunk

In Splunk, you can add data in different ways. Here we are going to see the forwarder installed on the Win10 computer and with the upload of a log file.  

### Add Data from Forwarder

- Go to Settings >Add Data

![[Pasted image 20240227191558.png]]

- Select "Forward" at the bottom
 
![[Pasted image 20240227191626.png]]

Add the computer to the selected host and give it a Server Class Name

Click "Next"

![[Pasted image 20240227191724.png|1000]]

Select what you want to monitor, in this case, we want to collect the local event log from this computer.

Select which log you want

Click "Next"

![[Pasted image 20240227191815.png|800]]

  
Select the index where the logs need to be put.

I choose to create a new one named "WinLog_clients". For this, click on "create a new Index"

Click Review to check and then submit.

  
Now, you can click "start searching" to try to find your last connection on the client's computer.
  
### Check Your Indexes

Go to Settings > Indexes

![[Pasted image 20240227191907.png]]

Search the index you create previously

![[Pasted image 20240227191931.png]]

As you see there is no incoming event, you are going to configure it now.  

### Add Receiver

Go to Setting > Forwarding and receiving

Click to add new receiving

![[Pasted image 20240227191958.png]]

Add the 9997 port (it's the default one, remember it in the previous document)

Wait a few minutes and check your indexes again, you will see new values

![[Pasted image 20240227192019.png]]

  
Try a quick search

![[Pasted image 20240227192109.png]]

### Add Data From Uploaded Logs

Go to Settings > Add Data

![[Pasted image 20240227192152.png]]

Select "Upload" in the bottom left corner

![[Pasted image 20240227192210.png]]

Push the file you want to upload, then click "Next"

![[Pasted image 20240227192226.png]]

Check how Splunk will read your file, then press Next if everything is okay

Select a host field value if needed, and the index which is going to be used (left default in the exercise)

Continue to the end, and start searching on it


![[Pasted image 20240227192255.png]]


ANSWERS

**How do I connect to Splunk?**  
  
1- Press the Connect button  
2- After the “Connect Issue” button appears, click it  
3- Open the address that says "Hostname" in the opened field from the browser. (If you can't access it, try again after 1 minute.)

![[Pasted image 20240227192606.png]]

![[Pasted image 20240227192612.png]]

4- Use the credentials we provide above (after clicking the "Connect Issue" button) to login.  
  
  
NOTE: If the Splunk server crashes, terminate and restart the machine.

---

  
NOTE: If the Splunk server crashes, terminate and restart the machine.  
  
 [Download](https://letsdefend.io/images/training/splunk/Images/tutorialdata.zip)