# osTicket-Installation
This guide is for individuals using a macOS or Unix-based host who want to set up a Helpdesk ticketing system using osTicket on a Microsoft Azure Virtual Machine running Ubuntu.




## Technologies Used

Operating System: Ubuntu Linux

Web Server: Apache2

Database: MySQL (MariaDB)

Scripting Languages: PHP 8.1, Bash (Linux commands)

Ticketing System: osTicket

Cloud Provider: Microsoft Azure

Version Control: Git & GitHub


## Installation Steps
### 1. Create a new Azure Virtual Machine  

 #### Select your __Subscription__ then create a new __Resource Group__ for your VM. Create a __Virtual Machine Name__. Choose a __Region__  and select your Ubuntu __Image__.
  ![VM creation](images/createvm.png)  

          
***     




#### Once your VM is created, it should be in  a __Running__ state. Click __Connect__ then __Connect__ again.

 ![VM creation](images/connect.png)   



#### To access your Ubuntu VM select __SSH using Azure CLI__
 ![VM creation](images/cli.png) 



#### Now that your VM is open, you need to update and upgrade the system. Run this command:
`sudo apt update && sudo apt upgrade -y`


### 2. Install Required Software  
   `sudo apt install -y apache2 mysql-server php libapache2-mod-php php-cli php-mbstring php-xml php-common php-mysql php-imap php-gd php-intl unzip php-apcu php-curl`

   ### Start and Enable the Services
   `sudo systemctl start apache2
sudo systemctl enable apache2
sudo systemctl start mysql
sudo systemctl enable mysql`

###


### 3. Download and Install osTicket



4. Configure Apache for osTicket


5. Finalizing Setup

🚀 Successfully deployed osTicket on Azure!
