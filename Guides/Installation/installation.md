<!--
    Author: Sven Thiel
    E-Mail: sven.thiel@uni-jena.de
    Date: 2020/07/01
    Version: 2.14.0
-->

# BEXIS2 Installation

## Table of contents
0. [Requirements](#requirements)
1. [Prerequisites](#prerequisites)
    1. [Internet Information Service](#prerequisites_iis)
    2. [Windows Identity Foundation 3.5](#prerequisites_wif)
    3. [.NET Framework 4.5.2](#prerequisites_netframework)
    4. [Relational Database](#prerequisites_rdb)
2. [Installation](#installation)
    1. [Site](#installation_site)
    2. [Workspace](#installation_workspace)
3. [Settings & Configurations](#settings)
    1. [IIS](#settings_iis)
    2. [PostgreSQL](#settings_postgresql)
    3. [BEXIS2](#settings_bexis2)


## 0. Requirements <a name="requirements"></a>
Currently, BEXIS2 is limited to run on a Windows based operating system with support for IIS (Internet Information Service). At least Windows 7 is required. The following operting systems were tested and are supported:
- Windows Server 2008
- Windows Server 2012R2
- Windows Server 2016 Datacenter
- Windows 7 Home
- Windows 10 Education

Unfortunately, neither Linux nor MacOS are supported yet.

## 1. Prerequisites <a name="prerequisites"></a>
In this section we assume that you already have a server or a virtual machine. If not, please do so or get in contact with your system administrator.

Beside a Windows based operating system, BEXIS2 needs additional features and software. Within the following sections, we will explain what is needed, and how to install it.

### 1. Internet Information Service <a name="prerequisites_iis"></a>
The IIS (Internet Information Service) is necessary to run .ASP-Net web-applications. It is similar to Apache, nginx or Tomcat, but they are not able to host BEXIS2. By default, IIS is not installed/activated. But you wouldn't need to download additional resources. You can install/enable the IIS by using "Turn Windows features on/off". If you need to install IIS, please proceed otherwise skip this part.

1. Press "Windows" key and type "Windows Feature".
2. Select the suggestion "Turn Windows features on/off". ATTENTION: You will need administrative rights.
3. Select "Internet Information Service" and press "OK".

For the installation itself, you don't have to do anything further. Windows will now install the IIS by itself. For additional configurations and settings, please take a look at the section [Settings & Configurations - IIS](#settings_iis).

### 2. Windows Identity Foundation 3.5 <a name="prerequisites_wif"></a>
The security system of BEXIS2 is based on the ASP.Net Identity 3. Therefore, an additional framework needs to be installed. Instead of an external resource, it is also available as a Windows feature and can be easely enabled. 

1. Press "Windows" key and type "Windows Feature".
2. Select the suggestion "Turn Windows features on/off". ATTENTION: You will need administrative rights.
3. Select "Windows Identity Foundation 3.5" and press "OK".

For the installation itself, you don't have to do anything further. Windows will now install the IIS by itself.

### 3. ASP.Net <a name="prerequisites_netframework"></a>
Unfortunately, having simply the IIS installed and running is not enough. Probably, you will need to install some further Windows features. There is a high chance, that at least some of them were added during the [installation of the IIS](#prerequisites_iis) (Internet Information Service) already. Nevertheless, we show how the installation looks like on a Virtual Machine that runs Windows Server 2012R2. But it should be quite similar on other versions, e.g. Windows 7/8/10. 

1. Press "Windows" key and type "Windows Feature".
2. Select the suggestion "Turn Windows features on/off". ATTENTION: You will need administrative rights.
3. Select "Internet Information Service" and press "OK".

> NOTE: You can also go to [Microsoft DotNet](https://dotnet.microsoft.com/download/dotnet-framework/net452) and download the Runtime directly.


### 4. Relational Database <a name="prerequisites_rdb"></a>
BEXIS2 is able to work with several relational DMBS. At least we tested:
- IBM DB2 9/10
- PostgreSQL 9.x/10.x
- MS SQL Server
- Oracle

Because we are using PostgreSQL 9.x/10x by far the most, we recommend it to you as well. Therefore, this step and all others (that are related to the DBMS) will focus on PostgreSQL.

> NOTE: If you are going to use PostgreSQL, please stick to version 9.x or 10.x. Otherwise, some features of BEXIS2 won't work properly. 

## 2. Installation <a name="installation"></a>
a

### 1. Site <a name="installation_site"></a>
b

### 2. Workspace <a name="installation_workspace"></a>
c

## 3. Settings & Configurations <a name="settings"></a>
d

### 1. IIS <a name="settings_iis"></a>
t

### 2. PostgreSQL <a name="settings_postgresql"></a>
s

### 3. BEXIS2 <a name="settings_bexis2"></a>
r