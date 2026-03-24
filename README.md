# 🚀 Creating an MVC Web App using Entity Framework (Database First)

**Author:** Mateo Isaza  

---

## 📖 Overview
This project demonstrates how to build an **ASP.NET Core MVC** application using the **Database First** approach with **Entity Framework Core** and **SQL Server**.

It includes:
- Database creation  
- Entity Framework configuration  
- Scaffolding models and DbContext  
- MVC structure (Controllers + Views)  

---

## Database Setup (SQL Server 2021)

---

Execute the following SQL script:

```sql
CREATE DATABASE SampleDb;
GO

USE SampleDb;
GO

CREATE TABLE Categories(
    CategoryId INT IDENTITY(1,1) PRIMARY KEY,
    Name NVARCHAR(100) NOT NULL
);
GO

CREATE TABLE Products(
    ProductId INT IDENTITY(1,1) PRIMARY KEY,
    Name NVARCHAR(100) NOT NULL,
    Price DECIMAL(18,2) NOT NULL,
    CategoryId INT FOREIGN KEY REFERENCES Categories(CategoryId)
);
GO
````

---

## 📦 Required Packages

Install via **NuGet** or **Package Manager Console**:

```powershell
Install-Package Microsoft.EntityFrameworkCore.SqlServer
Install-Package Microsoft.EntityFrameworkCore.Design
Install-Package Microsoft.EntityFrameworkCore.Tools
```

---

## ⚙️ Scaffolding (DbContext + Models)

Run this command to generate your models and DbContext:

```powershell
Scaffold-DbContext "Server=DESKTOP-GJDFMRJ\SQLEXPRESS01;Database=SampleDb;Trusted_Connection=True;TrustServerCertificate=True;" Microsoft.EntityFrameworkCore.SqlServer -OutputDir Models -ContextDir Data -DataAnnotations -Force
```

---

## 🧱 Project Structure

```
📁 Project
 ┣ 📁 Models        → Entity classes
 ┣ 📁 Data          → DbContext
 ┣ 📁 Controllers   → Business logic (CRUD)
 ┣ 📁 Views         → User interface (MVC)
```

---

## 🖥️ Features

* CRUD operations for **Categories**
* CRUD operations for **Products**
* Relationship handling (Products → Categories)
* Dynamic MVC views generated with scaffolding

---

## 🛠️ Technologies

* ASP.NET Core MVC
* Entity Framework Core
* SQL Server 2021

---

## 📌 Notes

* Uses **Database First** approach
* Make sure SQL Server is running before scaffolding
* Update the connection string according to your environment

---

## 📷 Screenshots

*Add your application images here (optional)*

```
```
