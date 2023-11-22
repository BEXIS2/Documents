<!--
    Author: Sven Thiel, David Schoene
    E-Mail: bexis Support <bexis-support@uni-jena.de>
    Date: 2023/11/22
    Version: 2.18.2
-->

# BEXIS2 Installation

## Table of contents
- [BEXIS2 Installation](#bexis2-installation)
  - [Table of contents](#table-of-contents)
  - [0. Requirements <a name="requirements"></a>](#0-requirements-)
  - [1. Prerequisites <a name="prerequisites"></a>](#1-prerequisites-)
    - [1.1. Windows Identity Foundation 3.5 <a name="prerequisites_wif"></a>](#11-windows-identity-foundation-35-)
    - [1.2. .NET Framework 4.5.2 <a name="prerequisites_netframework"></a>](#12-net-framework-452-)
    - [1.3. ASP.Net](#13-aspnet)
    - [1.4. Releated Database <a name="prerequisites_postgresql"></a>](#14-releated-database-)
  - [2. Preparation <a name="preparation"></a>](#2-preparation-)
    - [2.1 BEXIS2 Package <a name="preparation_bexis2package"></a>](#21-bexis2-package-)
    - [2.2. PostgreSQL <a name="preparation_postgresql"></a>](#22-postgresql-)
    - [2.3. IIS  <a name="preparation_iis"></a>](#23-iis--)
      - [2.3.1. Activate IIS7](#231-activate-iis7)
    - [2.3.2. Register .Net Framework 4.0 in IIS](#232-register-net-framework-40-in-iis)
  - [3. Deploy BEXIS 2 Web Application](#3-deploy-bexis-2-web-application)
    - [3.1. Configure server components](#31-configure-server-components)
    - [3.1.1.	Create Website](#311create-website)
    - [3.1.2.	Configure IIS](#312configure-iis)
    - [3.1.3. Create Empty Database](#313-create-empty-database)
    - [3.1.4.	Configure postgres](#314configure-postgres)
    - [3.2.	Install BEXIS 2 package](#32install-bexis-2-package)
    - [3.2.1.	Deploy Website (new installation)](#321deploy-website-new-installation)
    - [3.2.2.	Deploy Website (patch existing installation)](#322deploy-website-patch-existing-installation)
    - [3.2.3.	SMTP server configuration](#323smtp-server-configuration)
    - [3.2.4.	SSL Setup](#324ssl-setup)
  

## 0. Requirements <a name="requirements"></a>
Currently, BEXIS2 is limited to run on a Windows based operating system with support for IIS (Internet Information Service). At least Windows 10 is required. The following operting systems were tested and are supported:
- Windows Server 2016 - 2022
- Windows 10/11

Unfortunately, neither Linux nor MacOS are supported yet.

## 1. Prerequisites <a name="prerequisites"></a>
In this section we assume that you already have a server or a virtual machine. If not, please do so or get in contact with your system administrator.

Beside a Windows based operating system, BEXIS2 needs additional features and software. Within the following sections, we will explain what is needed, and how to install it.

### 1.1. Windows Identity Foundation 3.5 <a name="prerequisites_wif"></a>
The security system of BEXIS2 is based on the ASP.Net Identity 3. Therefore, an additional tool needs to be installed. Instead of an installation, it is also available as a Windows feature and can be enabled. 

### 1.2. .NET Framework 4.5.2 <a name="prerequisites_netframework"></a>
Depending on the Windows version you are using, this framework might be part of it already. Nevertheless, we show how the installation looks like. We demonstrate it on a Virtual Machine that runs Windows Server 2012R2. But it should be quite similar on other versions, e.g. Windows 7/8/10. 

1. Go to "Turn Windows features on or off"


> NOTE: You can also go to [Microsoft DotNet](https://dotnet.microsoft.com/download/dotnet-framework/net452) and download the Runtime directly.


### 1.3. ASP.Net
Unfortunately, having simply the IIS installed and running is not enough. Probably, you will need to install some further Windows features. There is a high chance, that at least some of them were added during the installation of the IIS (Internet Information Service) already. Nevertheless, we show how the installation looks like on a Virtual Machine that runs Windows Server 2012R2. But it should be quite similar on other versions, e.g. Windows 7/8/10.

- Press "Windows" key and type "Windows Feature".
- Select the suggestion "Turn Windows features on/off". ATTENTION: You will need administrative rights.
- Select "Internet Information Service" and press "OK".
> NOTE: You can also go to Microsoft DotNet and download the Runtime directly.

### 1.4. Database <a name="prerequisites_postgresql"></a>
- PostgreSQL 9.x -> 13

Because we are using PostgreSQL 13 by far the most, we recommend it to you as well. 

## 2. Preparation <a name="preparation"></a>

### 2.1 BEXIS2 Package <a name="preparation_bexis2package"></a>
-	First download the application package from: [BEXIS 2](https://github.com/BEXIS2/Core/releases) 
-	Unzip BEXIS2-v*.zip. 

![Bexis2 Folder Srtucture](https://raw.githubusercontent.com/BEXIS2/Documents/master/Guides/Installation/Images/bexis2_folder_structure.PNG) 

### 2.2. PostgreSQL <a name="preparation_postgresql"></a>
BEXIS 2 needs database management system to be available 
on your server. BEXIS2 developer team tested the PostgreSQL and we recommend it. If it not available already please follow the installation instructions below. 
From the following link http://www.enterprisedb.com/downloads/postgres-postgresql-downloads  select either the 32-bit or 64-bit version of PostgreSQL depending on your hardware and your installed operating system and install it. 

> NOTE: The Postgres version 13 is recommended. 

The installation of PostgreSQL is easy. It is enough to run the Installer and follow the steps. During installation, when asked, please
-	As user enter **postgres**
-	As password enter something and write it down
-	As port number enter **5432**.

Launch Stack Builder that is asked in the last step is not recommended.
When the installation is finished, run PgAdmin and add if not exist a connection to the server that you want to work on it.

- open **pgadmin**
- right click on **Server**
- create Server 

![Bexis2CreateServer1](https://raw.githubusercontent.com/BEXIS2/Documents/master/Guides/Installation/Images/pgadmin_create_server0.PNG) 
 
![Bexis2CreateServer2](https://raw.githubusercontent.com/BEXIS2/Documents/master/Guides/Installation/Images/pgadmin_create_server.PNG) 


### 2.3. IIS  <a name="preparation_iis"></a>
IIS is needed to host a website on the server. If your IIS is already activated and .NET framework is registered move on to section 4. If you don’t know if your IIS is activated or if .NET is registered, please follow the steps below.

#### 2.3.1. Activate IIS7

-	Open Control Panel > Programs and Features,
-	On the left side click the **Turn Windows features on/off** link.
 
-	First select **Internet Information Service*(IIS) and open this node
-	Open **Web Management Tools** and select/tick:
    -	IIS Management Console
    -	IIS Management Scripts and Tools
    -	IIS Management Service
-	Below IIS (Internet Information services) open **World Wide Web Services** > **Application Development Features** and select/tick all versions of:
    -	.Net Extensibility
    -   Asp
    -  	Asp .NET 
-	Below IIS open **World Wide Web Services** / **Common HTTP Features** and select/tick:
    -	Static Content
-	Click **OK** Button

### 2.3.2. Register .Net Framework 4.0 in IIS

First find **Windows** folder in your computer. It is probably in **c:\** and marked as **%windir%** in following steps.  
Register .Net Framework 4.0:
-	Find one of the following  paths in your computer direct in folders or through cmd as administrator
 -  %windir%\Microsoft.NET\Framework64\v4.0.30319\
    or
 - %windir%\Microsoft.NET\Framework\v4.0.30319\
-	Run aspnet_regiis.exe¬ir by double clicking or type as command.


## 3. Deploy BEXIS 2 Web Application
### 3.1. Configure server components
Perhaps some of the following configuration settings are already in place. But please check them out.

### 3.1.1.	Create Website
-	Open IIS (Control Panel / Administrative Tools)
-	Stop Default Website (Click it and choose “stop” on the right side)
-	Create a new Website (right click on sites and choose Add Web Site)
-	Enter your preferred Site name
-	Select Application pool  ASP .NET v4.0 (not Classic)
-	Select physical path of your website. It is inside the unzipped BEXIS 2 Package.
-	Confirm your selections by pressing the ok button
-	Stop your website (Click it and choose “stop” on the right side)

![IIS_AddWebsite](https://raw.githubusercontent.com/BEXIS2/Documents/master/Guides/Installation/Images/iis_addwebsite.PNG)  

### 3.1.2.	Configure IIS
- Configure application pool: 
  - Open IIS (Control Panel/Administrative Tools)
  - Select **Application Pools** and right click in **ASP .NET v4.0** and select **Set Application Pool Defaults…**
  - Change **General-Enable 32-Bit Applications** to **True**
  - Change **Process Model – Identity** to **NetworkService**

### 3.1.3. Create Empty Database
If you want to work with an empty database, you need to create it. 

Open pgAdmin. Double click on the **PostgreSQL…**. A popup window will open where you need to enter the password for user ‘postgres’. Please enter the password you defined when you installed PostgreSQL. 

Then in the Object browser section, Right click on “Databases” node and create a new database. Enter *BEXIS* as a database name.

![Create Database](https://raw.githubusercontent.com/BEXIS2/Documents/master/Guides/Installation/Images/createdatabase.png)  


### 3.1.4.	Configure postgres
BEXIS2 works with a DateTime format **mdy**. So Postgres need to setup with the same format.
-	Open postgres config file

![postgres config Database](https://raw.githubusercontent.com/BEXIS2/Documents/master/Guides/Installation/Images/postgres_config.PNG)  

-	Search for datestyle

![search in config ](https://raw.githubusercontent.com/BEXIS2/Documents/master/Guides/Installation/Images/search_in_config.PNG)  


-	Change it to “mdy”


### 3.2.	Install BEXIS 2 package
To install BEXIS 2 successfully, you need first unzip the BEXIS 2 package. Depends on it is a new or patch installation, follow steps bellow.

### 3.2.1.	Deploy Website (new installation)
-	Create a new folder and call it “Data” (in the BEXIS 2 unzipped package is recommended)
-	The IIS_IUSRS user needs full control permissions to the following folders:
    -	Workspace folder
    -	Data folder
-	Open configuration file (web.config) from the folder of your website inside unzipped BEXIS 2 package with a text editor. You mentioned it when you was selecting physical path of your website:
    -	enter (or adapt) database name in section connection strings
    -	set “CreateDatabase” to “true“ in section appSettings
    ATTENTION!! Define “true” value for “CreateDatabase” clears the database. 
    -	update “DataPath” in section appSettings
    -	update “SystemEmail” in section appSettings (some system activities will reported to this Email address)

### 3.2.2.	Deploy Website (patch existing installation)
-	Copy inside the *Website* folder from the BEXIS 2 unzipped package to the folder of Your_Websitename and overwrite existing files. 
-	If there are changes in the web.config, you will find in patch directory a web_update.config. From this file, the changes have to be taken. 
-	If there are changes in the Workspace, you will find a **Workspace** folder in the directory. The contents of the folder must be copied into the current Workspace folder.

### 3.2.3.	SMTP server configuration
SMTP server configuration is needed from the BEXIS2.11. You need to configure an SMTP server for the “SystemEmail”, which you defined in the web.config.
To find and set up SMTP parameters, open Credentials.config from **Workspace > General > Configurations**.

### 3.2.4.	SSL Setup
Nowadays, the demand of security in the internet is increasing tremendously. An important step to achieve that requirement is using *SSL (Secure Sockets Layer)*. With SSL it is possible to establish an encrypted connection between server (e.g. web server that is hosting the website) and client (typically a browser). That connection allows sensitive information (e.g. login credentials) to be transmitted securely through the web. Otherwise, that data would be sent as plain text between browsers and web servers – leaving you vulnerable to eavesdropping. If an attacker is able to intercept all data being sent between a browser and a web server they can see and use that information.

You are free to enable or even enforce SSL for your website inside IIS (Internet Information Service). Just use the following steps: 
