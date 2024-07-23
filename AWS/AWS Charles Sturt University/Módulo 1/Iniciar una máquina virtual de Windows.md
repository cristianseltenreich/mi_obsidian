[https://aws.amazon.com/getting-started/tutorials/launch-windows-vm/?trk=gs_card](https://aws.amazon.com/getting-started/tutorials/launch-windows-vm/?trk=gs_card)

##### Step 1: Create an Amazon Lightsail account

Aplicable a cuenta gratuita
![[Pasted image 20240310123847.png]]
Luego del loguin, seleccionar Lightsail
![[Pasted image 20240310124302.png]]

##### Step 2: Create a Windows Server 2019 instance in Amazon Lightsail

a. Choose the **Create instance** button on the **Instances** tab of the Lightsail home page.

![[Pasted image 20240310124437.png]]

##### Step 3: Configure the instance

a. An AWS Region and Availability Zone is selected for you. Choose **Change Region and Availability** **Zone** to create your instance in another location

![[Pasted image 20240310124555.png]]

![[Pasted image 20240310124710.png]]

b. Choose the **Microsoft Windows** platform option, and choose **OS only** to view the operating system-only instance images available in Lightsail. Select the **Windows Server 2019** image.

To learn more about Lightsail instance images, see [Choose an Amazon Lightsail instance image.](https://lightsail.aws.amazon.com/ls/docs/en_us/articles/compare-options-choose-lightsail-instance-image)

![[Pasted image 20240310124832.png]]

c. (Optional) Choose **Add launch script** to add a PowerShell script that will run on your instance when it launches.
![[Pasted image 20240310124926.png]]

d. Choose your instance plan.

You can try the $8 USD Lightsail plan free for three months (up to 750 hours). We'll credit three free months to your account.

[Learn more on the Lightsail pricing page.](http://www.amazonlightsail.com/pricing/)

![[Pasted image 20240310125059.png]]

e. Enter a name for your instance.

![[Pasted image 20240310125155.png]]

f. (Optional) Choose one of the following options to add tags to your instance:

- (Optional) **Add key-only tags** — Enter your new tag into the tag key text box, and press **Enter**. Choose **Save** when you’re done entering your tags to add them, or choose **Cancel** to not add them.

- (Optional) **Create a key-value tag** — Enter a key into the **Key** text box, and a value into the **Value** text box. Choose **Save** when you’re done entering your tags, or choose **Cancel** to not add them.

Key-value tags can only be added one at a time before saving. To add more than one key-value tag, repeat the previous steps.

For more information about key-only and key-value tags, see [Tags in Amazon Lightsail.](https://lightsail.aws.amazon.com/ls/docs/en_us/articles/amazon-lightsail-tags)

![[Pasted image 20240310125402.png]]

g. Choose **Create instance.**

![[Pasted image 20240310125434.png]]

![[Pasted image 20240310125511.png]]

![[Pasted image 20240310125536.png]]

##### Step 4: Connect to your instance using the browser-based RDP client in Lightsail

a. On the Instances tab of the [Lightsail home page](https://lightsail.aws.amazon.com/ls/), choose the RDP icon, or the ellipsis (⋮) icon next to the Windows Server 2019 instance you just created and choose **Connect**.

Tuve que recargar nuevamente la página ya que no se habilitaba la opción Connect
![[Pasted image 20240310125802.png]]

b. The browser-based RDP client window appears. You can use and manage your instance without configuring a third-party RDP client.

![[Pasted image 20240310130057.png]]

### Step 5: Get administrator password for your Windows Server 2019 instance

a. Choose the name of the Windows Server 2019 instance on the Instances tab of the Lightsail homepage.

![[Pasted image 20240310145641.png]]


b. Select the **Connect** tab, scroll down to the **Default login credentials** section of the page, and choose **Retrieve default password.**

![[Pasted image 20240310145745.png]]
![[Pasted image 20240310145944.png]]
### Step 6: Clean up

a. On the **Instances** tab of the [Lightsail home page](https://lightsail.aws.amazon.com/), choose the ellipsis (⋮) icon next to the Windows Server instance you just created and choose **Delete**.


![[Pasted image 20240310150359.png]]

b. Choose **Yes, delete** from the prompt.
![[Pasted image 20240310150436.png]]

##### Conclusion

We used Amazon Lightsail to spin up and configure a Windows instance.

Amazon Lightsail is great for developers, web pros, and anyone looking to get started on AWS in a quick and cheap way. You can launch instances, databases, and SSD-based storage; transfer data; monitor your resources; and so much more in a managed way.

