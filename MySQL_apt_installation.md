# MySQL APT installation using Ubuntu terminal

## Step 1: Downloading MySQL 8 APT Repositories

Ubuntu may not have access to MySQL repositories. To enable the repositories, we can download the latest version of the repositories from the officail MySQL website.

To check the latest repositories [Click here](https://dev.mysql.com/downloads/repo/apt/)

### To download the latest repositories, Execute the command


    wget https://dev.mysql.com/get/mysql-apt-config_0.8.26-1_all.deb 

### After executing the command the result will be 

<img src='https://github.com/geoost/MySQL-installation/blob/main/images/wget.png'>


## Step 2: Install  MySQL 8 APT Repositories

### To install MySQL 8 APT repositories, Execute the command

    dpkg -i mysql-apt-config_0.8.26-1_all.deb

### After executing the command the system will launch a configuration tool. It will present options to select the MySQL version that need to be install 
<img src='https://github.com/geoost/MySQL-installation/blob/main/images/package%20configuration.png'>

Leave the configuration setting to the default and click **Ok**

## Step 3: Refreshing the Repositories

The system should update repository listings to ensure you are installing the latest release.

In the terminal, enter the following:

    sudo apt-get update

<img src='https://github.com/geoost/MySQL-installation/blob/main/images/apt_update.png'>

## Step 4: Install MySQL 

To install MySQL, enter the following:

    sudo apt-get install mysql-server
<img src='https://github.com/geoost/MySQL-installation/blob/main/images/apt-get_install_mysql-server.png'>

### After executing the system will launch a tool to set the password to the **root** user.
<img src='https://github.com/geoost/MySQL-installation/blob/main/images/password%20setting.png'>

### To check the Status of the MySQL 

    systemctl status msyql




## Step 5: Set up MySQL Security(Optional)

By default, MySQL lacks many basic and important security features. Luckily, it comes with an installation script that walks you through the configuration.

To install the MySQL security script, enter:

    sudo mysql_secure_installation

<img src = 'https://github.com/geoost/MySQL-installation/blob/main/images/mysql_secure_installation.png'>

## Step 6: To login MySQL 

    mysql -u root -p

<img src='https://github.com/geoost/MySQL-installation/blob/main/images/mysql.png'>