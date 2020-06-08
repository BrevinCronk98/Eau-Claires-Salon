# _Eau Claires Salon_

#### _This is a live web application build using C# and Entity and MySQL databases." May 29th, 2020_

#### By Brevin Cronk

## Description
#### The Purpose of this application is to further my understanding of databases in MySQL and implementing them into my program.

### Instructions for use:

1. Open Terminal (macOS) or PowerShell (Windows)
2. To download the project directory to your desktop enter the following commands:
```
cd Desktop
git clone https://github.com/BrevinCronk98/Eau-Claires-Salon
cd Eau-Claires-Salon (or the file name you created for the main directory of the download)
```
3. To view the downloaded files, open them in a text editor or IDE of your choice.
* if you have VSCode for example, when your terminal is within the main project directory you can open all of the files with the command:
```
code .
```
4. Create a file within the HairSalon.Solution folder named appsettings.json.
5. Add the following code:
```
{
  "ConnectionStrings": {
    "DefaultConnection": "Server=localhost;Port=3306;database=brevin_cronk;uid=root;pwd=PutYourSQLPASSWORDHERE;"
  }
}
```
* Make any other changes needed if you have an alternative server, port, or uid selected. These are the default settings.

5. If you need to install the REPL dotnet script enter the following command in your terminal: 
```
dotnet tool install -g dotnet-script
```
6. To install the necessary dependencies and start a local host, after replicating the database steps below run the following commands:
```
dotnet restore
dotnet build
dotnet run
```

#### If you need to install and configure MySQL:
1. Download the MySQL Community Server DMG file [here](https://dev.mysql.com/downloads/file/?id=484914) with the "No thanks, just start my download" link.
2. On the configuration page of the installer select the following options:
* Use legacy password encryption
* Set your password
3. Open the terminal and enter the command:
*'export PATH="/usr/local/mysql/bin:$PATH"' >> ~/.bash_profile
4. Download the MySQL Workbench DMG file [here](https://dev.mysql.com/downloads/file/?id=484391)
5. Open Local Instance 3306 with the password you set.

#### To create a local version of the database:
1. Open MySQL Workbench and Local Instance 3306.
2. Select the SQL + button in the top left of the navigation bar.
3. Paste the following in the query section to create the database:

```
CREATE DATABASE `brevin_cronk`;

USE `brevin_cronk`;

CREATE TABLE `clients` (
  `StylistId` int(11) NOT NULL AUTO_INCREMENT,
  `Description` varchar(255) DEFAULT NULL,
  `ClientId` int NOT NULL AUTO_INCREMENT,
  `ClientName` varchar(255) DEFAULT NULL,
  PRIMARY KEY (`ClientId`)
) ENGINE=InnoDB DEFAULT CHARSET=utf8mb4 COLLATE=utf8mb4_0900_ai_ci;

CREATE TABLE `stylists` (
  `StylistId` int(11) NOT NULL AUTO_INCREMENT,
  `Name` varchar(255) DEFAULT NULL,
  PRIMARY KEY (`StylistId`)
)  ENGINE=InnoDB DEFAULT CHARSET=utf8mb4 COLLATE=utf8mb4_0900_ai_ci;

```

4. Press the lightning bolt button to run this command.
5. If the database does not appear, right click in the schemas bar and select Refresh All.
atch run" if You Plan on Modifying Project. 




## Known Bugs
#### There are no Known Bugs Yet


## Specifications:

#### User Can See List of All Stylists
* Input: "Click Here to See List of Stylists!"
* Output: "Wendy, Sherry, Denise, and Sasha"

#### User Can Select a Stylist to Se Their Details and Clients
* Input: "Click on A stylist Name to See More Details"
* Output: "Sasha: Nice and Friendly. Clients: Bob, Jeff, Mary"

#### Add New Stylist to System
* Input "Click Here to Add a New Stylist"
* Output "You Have Successfully Added a New Stylist!"

#### Add Clients To a Specific Stylist
* Input: "Click on Denise to Add Clients"
* Output: "Successfully added Clients: Erik and Rolf"


## Technologies Used
* MySQL Workbench
* C#
* .NET Core
* Visual Studio Code
* Entity Framework

### License
This software is licensed under the MIT license.


Copyright (c) 2020 **_Brevin Cronk_**
