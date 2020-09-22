# SuppliersErp
A project which has a CRUD operation (based on ASP.NET Web Api 2) for Suppliers and Supplier Categories and custom-made validations which front-end design was based in Angular 10 and Bootstrap 4 (https://github.com/apalasopoulos1986/erpuserinterface). 
It held the principle of Separation of Concern because the application is 
consisted of 3 layers (Database, Web Api 2 design and UI).

Scripts for generating database

create database SuppliersDB

//////////

use SuppliersDB
Create Table dbo.SupplierCategory(
SupplierCategoryId int identity(1,1) primary key,
Category varchar(80));

/////////

use SuppliersDB
Create Table dbo.Supplier (
SupplierId int identity(1,1) primary key,
SupplierCategoryId int references SupplierCategory(SupplierCategoryId),
FullName varchar(50),
AFM varchar(9),
Address varchar(100),
Email varchar(80),
Phone varchar(80),
Active bit
);
