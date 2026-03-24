# Web Application MVC Legacy
## Developed using Visual Studio .NET 2022 and MS SQL Server 2021
## Developer: Walter Hugo Arboleda Mazo

## SQL Server 2021 Database SampleDb and tables Categories and Products
<img width="477" height="262" alt="image" src="https://github.com/user-attachments/assets/f2f9049d-f30e-4f7d-b140-aa8edc8dfb52" />

## SQL Server 2021 Database Creation for SampleDb Database and tables Categories and Products

CREATE DATABASE SampleDb;

USE SampleDb;

CREATE TABLE Categories(
CategoryId INT IDENTITY(1,1) PRIMARY KEY,
Name NVARCHAR(100) NOT NULL
);

CREATE TABLE Products(
ProductId INT IDENTITY(1,1) PRIMARY KEY,
Name NVARCHAR(100) NOT NULL,
Price DECIMAL(18,2) NOT NULL,
CategoryId INT FOREIGN KEY REFERENCES Categories(CategoryId)
);

## SQL Server 2021 installed packages with the Nuget Manager:

Microsoft.Data.SqlClient

System.Data.SqlClient

Microsoft.AspNetCore.Mvc.TagHelpers

## References:
https://www.youtube.com/watch?v=0tWLmvk86FA&list=PL5bLncqubD6soGTTcNv4YGlIha-b5gBfy
