# Virtual Linux Security Lab

## Objective

The Virtual Linux Security Lab is aimed at creating a Virtual Machine environment and installing different operating systems within.

### Skills Learned

- Installing a Home Lab Linux Environment for Cybersecurity Projects.

### Tools Used
- Oracle Virtual Box
- Kali Linux
- Ubuntu
- Metasploitable

## Steps

### Download and install Oracle VirtualBox
VirtualBox can be downloaded at: <a href="https://www.virtualbox.org/">VirtualBox</a>

Select the package for your Operating System (MAC OS, Windows, etc...)

Follow the Installation Steps

### Create Host-Only Network
As soon as you start VirtualBox there will be a welcome page with no VMs installed yet:
![image](https://github.com/user-attachments/assets/03d95f89-e9dd-4b3b-9fc9-9efe7eeffc7c)

Select File -> Tools -> Network manager

Once the Network Manager is opened, click "create". This will generate a brand new virtual network adapter.
Click on "Properties", making sure its the configuration you want.
I would recommend manual to keep track of the IP address ranges.
(Optional) You can choose to enable DHCP, and create multiple Virtual Networks.
Make note of the network adapter you just created.
![image](https://github.com/user-attachments/assets/37d6043c-ad50-4d57-89e1-ab5ded7ddfde)

### Install Kali Linux
Kali come pre-packaged as a "VirtualBox Pre-Built Image" making instillation easy.
Download Here: <a href="https://www.kali.org/get-kali/#kali-virtual-machines">Kali Virtual Machines</a>

Select the section for Virtual Box (Not VMware) and choose a distribution that firs your current processor (newer computers are 64-bit, while older ones are 32-bit)
Download the file and note where its saved.

(Additional Steps) Once the downloaded the file extension may be .7z, if so download thus free opensource software <a href="https://www.7-zip.org/">7-Zip</a> to unzip the file. When completed you should have a new Kali file that contains the Kali VirtualBox image with file extention .vbox.
![image](https://github.com/user-attachments/assets/6e37e503-890a-434a-83f6-50e42f48f219)

In Oracle VirtualBox Manager, Go to "Add" -> Navigate to the unzipped Kali file and select the file with extention .vbox
![image](https://github.com/user-attachments/assets/41fd07e5-7118-468d-998b-d8870fac0b09)

Before starting the Virtual machine, be sure to review its settings and make any ajustments or changes based on your prefences.
Most importantly the Network Settings. If the network is attached to NAT, that means your virtual machine is connected to the internet.

Go to Network within the Virtual machine settings and change "NAT" to "Host-only Adapter".
Choose the Host adapter you created when you intsalled VirtualBox.
Since the Kali Linux mavhine will be used for scanning we will "Allow VMs" within "Promiscuoous Mode" in the settings.
Verify all these changes and click "OK".
![image](https://github.com/user-attachments/assets/83577a91-a597-4256-b84f-fc6010bb3ffb)

### Install Metasploitable
Metasploitable is a deliberately vulnerable Linux distribution designed for practicing cybersecurity skills. Due to its high level of vulnerability, it should never be connected to the internet!

Download Here: <a href="https://www.rapid7.com/products/metasploit/metasploitable/">Metasploitable</a>

For this installation once downloaded, navigate to VirtualBox -> Settings -> Storage and add attachemet "Hard Disk". The file extension should be .vmdk

![image](https://github.com/user-attachments/assets/5bcb012f-3d50-4009-b2de-7a4bd88cea20)

When added Click "New", Select Linus as Operatings System type
Go down to "Hard Disk" and Use an existing Virtual Hard Disk File, Select the Metasploitable Hard Disk you just installed.
![image](https://github.com/user-attachments/assets/8e1663af-b5b2-4842-9392-6c5807033d69)

Be sure to check the Network settings for Metasploitable and verify that its attached to Host-only adapter and on the same network as Kali Linux.

### Install Ubuntu
Ubuntu is not available as a pre-packaged appliance as it must be installed from an ISO file, which functions like a virtual CD/DVD.

Download Here: <a href="https://ubuntu.com/download/desktop">Ubuntu</a>

Since Ubuntu is not considered an "offensive" or "vulnerable" distribution, it is safe to keep it connected to the internet using the NAT option for the Network Adapter. However, if you intend to use Ubuntu as a target you should place it on the same "Host-based network" as Kali Linux.

After downloading Ubuntu, navigate to 

### (Optional) Install other Operating Systems
As long as you have a CD/DVD or an ISO file, you can install any other operating system using the same steps as you would for Ubuntu.

