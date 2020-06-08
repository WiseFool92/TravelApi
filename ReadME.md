# _Travel API_

#### June 8th, 2020

## Description

_This Queriable Api will allow the user to GET & POST reviews of their travel destinations and associated experiences._

_This application is meant to be viewed in the browser & connected to a database to hold user information. It will need a .NET Core Sdk 3.1 or 2.2 & ASP.Net 3.1 or 2.2 download. It will need a mysql workbench 8.0 to be connected to it & have an Api key connected_

## Setup/Installation Requirements

_Make sure you have [git version control](https://git-scm.com/downloads) installed on your computer._

1. Click the green 'Clone or Download' button and copy the link / download the zip
2. Open terminal and type... or skip to #4 if you downloaded the zip

**Windows**

```sh
cd desktop
```

Mac & linux

```sh
cd ~/Desktop
```

3.  in terminal type '_git clone {link to repository}_ '

```sh
git clone {link to repository}
```
4. If you downloaded the zip then extract all onto your desktop
5. Open the folder with VSC or an equivalent
6. Install .NET Core using <a href="https://docs.microsoft.com/en-us/dotnet/core/install/runtime?pivots=os-windows">this</a> link
7. Then Run the code below in the terminal to confirm installation
```sh
dotnet -- version
```  
8. In the terminal enter to confirm the proper version installed 
```sh
dotnet tool install -g 
dotnet-script
```
9. Download _[ASP.NET Core](https://dotnet.microsoft.com/download)_ To enable live viewing on a local server
10. You will need to create a file in the root directory of the project run in powershell 
```sh
new-item appsettings.json
```
11. Once created populate this file with
{
  "ConnectionStrings": {
      "DefaultConnection": "Server=localhost;Port=3306;database=your_database_name;uid=root;pwd=YourSqlWorkBenchPassword;"
  }
}
11. Open project, navigate to the containing folder of the project & Run the code below to confirm build stability
```sh
dotnet run build 
```
12. Within that same containing folder Run _dotnet watch run_ To open a live server w/auto updated viewing
13. If you want to run tests navigate to the .tests containing folder and enter
```sh
dotnet test
```
14. Enjoy

## ReCreating MySql Database 
(Setup my vary slightly from system to system)

1. Open MySql Community Installer and reconfigure (legacy password, uncheck windows services)
2. Open MySql Workbench
3. On the bar at the top of the page with many options click Create New Schema in the connected server (it looks like triple stacked silicone wafers)
4. last_first (naming scheme)
5. Open the drop down for the database created
6. Right click and select create table
7. Your first collum name should be SalonId (make sure it is an int) & since this acts as your id key - check these three boxes: Primary Key, not null, & Auto Incrementing
8. Your next collum name should be StylistName (make sure it is a string (varchar) set to 255)
9. Your next collum name should be Specialty (make sure it is a string (varchar) set to 255)
10. Right click on tables and select create table
11. Your first collum name should be ClientId (make sure it is an int) & since this acts as your id key - check these three boxes: Primary Key, not null, & Auto Incrementing 
12. Next we will add three collums Name, Type, Contact (make sure it is a string (varchar) set to 255)
13. Tasks Complete

## Connecting to an API

1. 
2. 

## Specs

### Behavior Driven Development Spec List
#### Travel Api
|                          Behavior                          | Input  | Output  |
| :--------------------------------------------------------: | :----: | :-----: |
| The user can get all reviews about travel destinations. | 'http://localhost:5000/' | 'List of stylists' |
| The user can add a stylist to the hair salon | 'click add another stylist' 'Natural Hair Care Specialist' | 'Natural Hair Care Specialist' |
| The user can add clients to each stylist | 'select karen' 'Add Amanda to her clientel' | 'Amanda' |
| The user can add details to the stylist | 'Name, Type' | 'Betty' 'Colorist' |
| The user can add details to the patron | 'Name, type of work' | 'Sally' 'Dye Hair Blue' |

---
## Known Bugs

_N/A_ - 6/6/2020

## gh-pages

WiseFool92.github.io/TravelApi

## Support

_Email: watkins92@gmail.com_

---
## Built With

- [C#](https://docs.microsoft.com/en-us/dotnet/csharp/)
- [.NET Core 3.1](https://dotnet.microsoft.com/download/dotnet-core/3.1)
- [MSTest](https://docs.microsoft.com/en-us/dotnet/core/testing/unit-testing-with-mstest)

## Useful tools

- [free icons @ icons8](https://icons8.com/)
- [free icons @ fontawesome](https://fontawesome.com/)

---

- [Old School Gifs Search](https://gifcities.org/)
- [free images @ unsplash](https://unsplash.com/)

  - **_source.unsplash.com_ will return a random image at a desired size by simply calling the size after the url followed by a '?' and a keyword. Example below**

  - _https://source.unsplash.com/400x400/?cat_
  - http://unsplash.it/500/500 - This will just return a random image the size of 500x500

---

- [Flex-box Cheat Sheet](http://yoksel.github.io/flex-cheatsheet/)
- [CSS Grid Cheat Sheet](http://grid.malven.co/)

---

- [CSS Gradient BG Generator](https://mycolor.space/gradient)
- [CSS Basic Gradient Generator](https://cssgradient.io/)

---

- [CSS Dropshadow Generator](https://cssgenerator.org/box-shadow-css-generator.html)

### License

This project is licensed under the MIT License

Copyright (c) 2020 **_Nathan Watkins-Hoagland_**
