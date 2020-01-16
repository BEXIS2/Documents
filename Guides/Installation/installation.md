<!--
    Author: Sven Thiel
    E-Mail: sven.thiel@uni-jena.de
    Date: 2019/05/14
    Version: 2.12.3
-->

# BEXIS2 Installation

## Table of contents
0. [Requirements](#requirements)
1. [Prerequisites](#prerequisites)
    1. [Windows Identity Foundation 3.5](#prerequisites_wif)
    2. [.NET Framework 4.5.2](#prerequisites_netframework)
    3. [PostgreSQL](#prerequisites_postgresql)
2. [Preparation](#preparation)
    1. [BEXIS2 Package](#preparation_iis)
    2. [PostgreSQL](#preparation_postgresql)
    3. [IIS](#preparation_iis)
3. [Another paragraph](#paragraph2)

## 0. Requirements <a name="requirements"></a>
Currently, BEXIS2 is limited to run on a Windows based operating system with support for IIS (Internet Information Service). At least Windows 7 is required. The following operting systems were tested and are supported:
- Windows Server 2012R2
- Windows Server 2016 Datacenter
- Windows 7 Home
- Windows 10 Education

Unfortunately, neither Linux nor MacOS are supported yet.

## 1. Prerequisites <a name="prerequisites"></a>
In this section we assume that you already have a server or a virtual machine. If not, please do so or get in contact with your system administrator.

Beside a Windows based operating system, BEXIS2 needs additional features and software. Within the following sections, we will explain what is needed, and how to install it.

### 1. Windows Identity Foundation 3.5 <a name="prerequisites_wif"></a>
The security system of BEXIS2 is based on the ASP.Net Identity 3. Therefore, an additional tool needs to be installed. Instead of an installation, it is also available as a Windows feature and can be enabled. 

### 2. .NET Framework 4.5.2 <a name="prerequisites_netframework"></a>
Depending on the Windows version you are using, this framework might be part of it already. Nevertheless, we show how the installation looks like. We demonstrate it on a Virtual Machine that runs Windows Server 2012R2. But it should be quite similar on other versions, e.g. Windows 7/8/10. 

1. Go to "Turn Windows features on or off"
2. 

> NOTE: You can also go to [Microsoft DotNet](https://dotnet.microsoft.com/download/dotnet-framework/net452) and download the Runtime directly.


### 3. PostgreSQL <a name="prerequisites_postgresql"></a>
BEXIS2 is able to work with several DMBS. At least we tested:
- IBM DB2 9/10
- PostgreSQL 9.x
- MS SQL Server
- Oracle

Because we are using PostgreSQL 9.x by far the most, we recommend it to you as well. Therefore, this step and all others (that are related to the DBMS) will focus on PostgreSQL.

> NOTE: If you are going to use PostgreSQL, please stick to version 9.x. Otherwise, some features of BEXIS2 won't work properly. 

## 1. Preparation <a name="preparation"></a>
d

## Some paragraph <a name="paragraph1"></a>
The first paragraph text

### Sub paragraph <a name="subparagraph1"></a>
This is a sub paragraph, formatted in heading 3 style

## Another paragraph <a name="paragraph2"></a>
The second paragraph text