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



