# SuppliersErp
A project which has a CRUD operation for Suppliers and Supplier Categories
Based in ASP.Net 5 and Web Api2
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
