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
- Metasploitable 3

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



### Install Metasploitable
### Install Ubuntu
### (Optional) Install other Operating Systems
