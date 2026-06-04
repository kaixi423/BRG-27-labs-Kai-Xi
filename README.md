# BRG-27-labs-Kai-Xi

Session 1a: Setting up linux

Managed to create a new repository but was having some issues with cloning the repository to my local machine using Git, googled it and found "sudo apt update && sudo apt install git -".

However met some error when using that line, stated "error: The repository file :/cdrom resolute release" no longer has a release file"

Went back on google and found "sudo nano /etc/apt/sources.list" There was 0 files 

<img width="657" height="487" alt="image" src="https://github.com/user-attachments/assets/826c08c1-1ca9-4dd7-9c74-53048a854f35" />

Had to look inside the extra sources directory with "ls /etc/apt/sources.list.d/" , proceeded to show me a file named cdrom.sources

I then deleted the cdrom file with "sudo rm -f /etc/apt/sources.list.d/*cdrom*" and follow up with sudo apt update. After doing that my sudo apt install git -y worked.

<img width="662" height="528" alt="image" src="https://github.com/user-attachments/assets/efc81840-0d18-43e5-b4e7-efea61b788fa" />

Lab: Obtaining Linux on your PC - Install Ubuntu using Virtualbox/VMware Workstation

I used VMware workstation to create a new virtual machine and have configured the following

<img width="1369" height="901" alt="image" src="https://github.com/user-attachments/assets/22cdd41a-cad3-412b-986a-f679d37d97a4" />

Living system proof on running ubuntu

<img width="634" height="423" alt="image" src="https://github.com/user-attachments/assets/c709c998-c5fd-4cde-9720-79806beb8d8a" />


Lab: Familiarity with Ubuntu Linux – Basic command line navigation and utilities.

→ Practice using `pwd`, `ls`, `cd`, `mkdir`, and `touch`.

<img width="651" height="524" alt="image" src="https://github.com/user-attachments/assets/5b331549-e504-4507-99de-8014115dfdd2" />

→ Understand directory structure (`/etc`, `/var`, `/home`).

Navigating through "/etc"

<img width="601" height="826" alt="image" src="https://github.com/user-attachments/assets/cb58048b-fbdd-4067-8602-0200461a32ba" />


Navigating through "/var"

<img width="715" height="57" alt="image" src="https://github.com/user-attachments/assets/5ef3e85b-fb00-4363-9c83-120e28271873" />


Navigating through "/home"

<img width="220" height="78" alt="image" src="https://github.com/user-attachments/assets/5fbacd98-c1f8-451d-b4a5-7a9f37783131" />


→ Use `man` to explore Linux manual pages. 

<img width="1104" height="771" alt="image" src="https://github.com/user-attachments/assets/8bc24835-644c-4a6d-9765-40eded45364c" />



Session 1b: Exploring Linux
Lab: Linux Services – Understanding and managing background services.

→ List services using `systemctl list-units --type=service`. These are the list of services

<img width="1211" height="723" alt="image" src="https://github.com/user-attachments/assets/3a25a938-d80c-4a5b-96e3-7b43ca03c560" />

Checking the live status of a standard background network service such as the cron scheduler. 

<img width="1211" height="477" alt="image" src="https://github.com/user-attachments/assets/7a7fbd35-6dfd-47b1-bcce-0274e4f16982" />


→ Start/stop services with `sudo systemctl start|stop [service]`.

Tried to stop and restart the service, came across a warning "the unit file, source configuration file or drop ins of cron.service changed on disk, run "system-daemon reload" to reload units.


I did that and managed to stop the service alongside checking the status with "sudo systemctl status"

<img width="1193" height="648" alt="image" src="https://github.com/user-attachments/assets/78bd4715-b3e2-4fdd-b4f1-e3afeaa18499" />


Tried to start the service again and checked status of services using "sudo systemctl status"

<img width="1077" height="344" alt="image" src="https://github.com/user-attachments/assets/2c3e87f9-2611-426c-a1f9-620082c59304" />


Lab: Linux Permissions – Explore and apply file and directory permissions.

→ Use `ls -l` to view permissions.

Created a quick script file to experiment the permissions on. Using "touch perm_test.sh" and also viewed the default permissions using "ls-1" 

<img width="440" height="81" alt="image" src="https://github.com/user-attachments/assets/8c041922-291e-4ae5-af51-6695e9372b1c" />


→ Change permissions using `chmod` (e.g., `chmod 755 file.sh`).

Managed to change permissions to root

<img width="442" height="146" alt="image" src="https://github.com/user-attachments/assets/3a50b598-6e57-48cf-a22c-ae4163323cd8" />


→ Change ownership using `chown user:group file.txt`.

<img width="439" height="113" alt="image" src="https://github.com/user-attachments/assets/67001cb4-2d1f-4d1f-bf5a-3ab0069dec8e" />

Lab: Searching Filesystems – Use commands like `find` and `grep`.

<img width="325" height="72" alt="image" src="https://github.com/user-attachments/assets/7a96508d-1577-4ff1-8271-ace1f15e1f3a" />

→ Use `grep -r 'search-term' /path/` to search content.

Learned that the dot "." is a special Linux shortcut that means "the current directory I am standing in right now."

Used that to search right in my home folder and worked.

<img width="667" height="110" alt="image" src="https://github.com/user-attachments/assets/316f3049-cbb6-438e-8804-13c534764d2f" />


I also tried typing out my folder to see if the result would be the same, and it worked.

<img width="535" height="63" alt="image" src="https://github.com/user-attachments/assets/c96372f1-e5f6-41e7-8074-f61cbd57f486" />







Session 2a: Total cost of ownership 
Lab: Total Cost of Ownership – Apply TCO concepts in practical comparison.

→ Compare cloud vs on-prem cost (hardware, software, licensing). 
For this task, I will be using Dell, AWS and Azure for comparison.
For Dell I choose the Dell PowerEdge T160, a tower server designed for small to medium businesses. 
https://www.dell.com/en-sg/shop/cty/pdp/spd/poweredge-t160/pet16010a 

<img width="450" height="250" alt="image" src="https://github.com/user-attachments/assets/53238fa5-0f3f-4899-8060-755b973a5016" />


Below I have listed the specs I have chosen for the dell tower.
I did not choose a operating system as I will be using Ubuntu Linux Server Edition which is open source and has a $0 license fee. I will be using this OS for the cloud services to ensure that my comparison is fair. 

<img width="595" height="744" alt="image" src="https://github.com/user-attachments/assets/ea6f2645-f490-46a4-a9d9-282a7328bd72" />

 
I will be estimating $15 per month for electricity, cooling and possible battery wear over 3 years. I will be calculating 15x12 = 180 for 1 years cost and multiplying it by 3 to calculate the amount for 3 years which would lead to $540. I will be adding this $540 to the upfront cost to purchase the hardware (4104.04) which is $4644.04.
The 3 year TCO (Total cost of ownership) of owning your own on-premises server is $4644.04.

For Azure Cloud options, I will be choosing the Standard-B1s Virtual machine.
I have listed the specifications below:
 
<img width="375" height="545" alt="image" src="https://github.com/user-attachments/assets/04564394-7891-4cbe-a366-d69d869accda" />
 
<img width="385" height="618" alt="image" src="https://github.com/user-attachments/assets/db26c6b6-020a-4f77-a4c1-b9c79b7f35ff" />

<img width="378" height="169" alt="image" src="https://github.com/user-attachments/assets/7da25293-3c92-4628-819d-421d6ef96dfa" />
 
 
 
The baseline Azure Standard_B1s compute instance runs at an unmanaged rate of US$7.59/month. To create a functioning server environment, a 32 GiB managed boot volume (~S$2.20/mo) is added to the operational parameters, bringing the functional runtime entry point to roughly S$10–S$12.30/month.
I will be taking the higher end of the price to manage this cloud for comparison. 
12.30x36=442.8
The TCO for Azure cloud is $442.8 by year 3.


For AWS Cloud services, I will be choosing Amazon EC2 t2.micro instance.
I have listed the specifications below. 

<img width="886" height="293" alt="image" src="https://github.com/user-attachments/assets/bfd79295-520b-4e37-b977-242faba2169f" />

(I took the on-demand price/hr instead of their reserved instance effective hourly to ensure the comparison is as accurate as possible.)
The baseline hourly rate for an AWS EC2 t2.micro instance running ubuntu is US$0.0116 per hour. Which is USD$8.47 Per month which is around S$11.30/month.
I added a operating system storage volume of 32GiB gp3 block volume which is around S$3.50/month. So the total cost of running this server would be S$14.80 per month. Which means that the total cost of running this server would be S$532.80 for 3 years.
The TCO for AWS Cloud services is $532.80 for 3 years.




I have documented monthly and yearly costs here.

<img width="706" height="325" alt="image" src="https://github.com/user-attachments/assets/21d1ec9a-3367-45b1-8ca3-f2dad5c60a8c" />


Calculating ROI Metrics:
To calculate the ROI metric I will use the total cost of 3 Year cumulative cloud cost minus 3 year on prem TCO divided by initial upfront on prem capital expenditure and  multiply it by 100. 

Dell Poweredge T160 vs. Azure Cloud (Standard_B1s)
This metric calculates the return of investing in a local physical server instead of subscribing to Azure over a 3-year timeline.
•	Initial Upfront Investment (Dell CapEx): S$4,104.04
•	3-Year Total Cost of Baseline Alternative (Azure TCO): S$442.80
•	3-Year Total Cost of Selected Option (Dell TCO): S$4,644.04

 <img width="539" height="244" alt="image" src="https://github.com/user-attachments/assets/c7f32bc9-0205-4d61-9601-00576e85ff10" />



What this actually means:
Because the ongoing local utility power overhead to keep the physical server online (S$15/mo) is higher than the entire Azure monthly subscription (S$12.30/mo), there are no monthly operational savings. The physical server can never break even, resulting in a complete loss of capital efficiency (-102.4% ROI) over the 3-year track.

Dell PowerEdge T160 vs. AWS Cloud (t2.micro)
This metric calculates the return of investing in a local physical server instead of subscribing to AWS over a 3-year timeline.
•	Initial Upfront Investment (Dell CapEx): S$4,104.04
•	3-Year Total Cost of Baseline Alternative (AWS TCO): S$532.80
•	3-Year Total Cost of Selected Option (Dell TCO): S$4,644.04

 <img width="489" height="222" alt="image" src="https://github.com/user-attachments/assets/2bd7de97-8da7-4e48-998e-22c4c21dcbdb" />

 
What this actually means:
Similar to the Azure scenario, local utility run rates exceed the AWS subscription cost by S$0.20 per month, preventing an operational savings threshold from ever being achieved. The upfront Capital Expenditure premium results in a negative financial yield (-100.2% ROI).

Azure Cloud (Standard_B1s) vs. AWS Cloud (t2.micro)
This metric fulfills your assignment prompt to "Compare TCO across cloud providers." It evaluates the financial yield of selecting Azure instead of AWS Because both options are pure operating expenses with S$0.00 upfront costs, financial standards use the total 3-year AWS alternative cost as the denominator.
•	3-Year Total Cost of Baseline Alternative (AWS TCO): S$532.80
•	3-Year Total Cost of Selected Option (Azure TCO): S$442.80
•	Initial Upfront Investment: S$0.00 (Pure Operational Cost comparison)

 <img width="636" height="206" alt="image" src="https://github.com/user-attachments/assets/df74bf58-9f7a-4278-97af-312bd82d8584" />

What this actually means:
Under a standard on-demand model, Azure is cheaper than AWS from Day 1 onwards (S$12.30 vs S$14.80). Because Azure carries S$0.00 upfront and is cheaper every subsequent month, AWS will never hit a threshold to cross over or break even against Azure's TCO. Choosing Azure saves the business a flat S$90.00 over three years, improving infrastructure budget efficiency by +16.9%.

From these results:
1.	Hardware vs. Micro-Cloud TCO Imbalance:
Both hardware-to-cloud scenarios display a negative return on investment (~ -100%). From a strict financial perspective, dedicating S$4,104.04 of upfront capital to run a task small enough to fit within an entry-level 1GB RAM cloud slice is highly inefficient. The local utility power overheads alone surpass the monthly cost of a micro cloud instance.

2.	Cross-Cloud Provider Efficiency Winner:
Comparing the cloud hyperscalers directly reveals that Azure yields a +16.9% ROI advantage over AWS. While both platforms offer identical basic hardware allocations (1 vCPU, 1GB RAM), Azure's localized Southeast Asia region rates for compute runtime and standard storage are lower than AWS's legacy t2.micro pricing structure. This saves the business a flat S$90.00 over 36 months.


Architectural Disclaimer: Peformance and resource imbalance.
When analyzing the 3-year TCO metrics, the financial calculations heavily favor the public cloud providers due to a massive, deliberate mismatch in hardware resource scales. This comparison matches a heavy, physical on-premises server against the absolute smallest entry-tier virtual machines available in the cloud:
1.	The Processing & Memory Gap: The on-premises Dell PowerEdge T160 features a dedicated physical processor and 16 GB of DDR5 RAM. In stark contrast, the Azure B1s and AWS t2.micro instances only allocate a tiny slice of shared hardware containing 1 GB of RAM. A 1 GB virtual machine is highly restricted and would frequently crash or freeze if tasked with running production-grade corporate databases, heavy local file transfers, or modern business applications.
2.	The Storage Discrepancy: The physical Dell server includes a massive 2,000 GB (2 TB) local hard drive built directly into its system. The baseline Azure and AWS configurations only include a tiny 32 GB boot disk to hold the basic operating system.


Session 2b: Cloud services



