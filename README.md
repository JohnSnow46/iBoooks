# 📚 iBoooks - Online Bookstore

> A modern, intuitive online bookstore application built with cutting-edge .NET technologies. Discover, explore, and purchase books seamlessly across all devices.

[![.NET](https://img.shields.io/badge/.NET-6.0+-512BD4?style=flat-square&logo=dotnet)](https://dotnet.microsoft.com/)
[![ASP.NET Core](https://img.shields.io/badge/ASP.NET%20Core-MVC-512BD4?style=flat-square)](https://dotnet.microsoft.com/apps/aspnet)
[![SQL Server](https://img.shields.io/badge/SQL%20Server-2019+-CC2927?style=flat-square&logo=microsoftsqlserver)](https://www.microsoft.com/sql-server)
[![License](https://img.shields.io/badge/License-MIT-green?style=flat-square)](LICENSE)

---

## 🎯 Overview

iBoooks is a full-stack web application that provides a comprehensive online bookstore experience. Whether you're a book enthusiast looking to browse thousands of titles or an administrator managing inventory, iBoooks delivers a professional, responsive, and secure platform.

Built with industry best practices, this project showcases:
- ✨ Clean Architecture & SOLID Principles
- 🔒 Enterprise-Grade Security
- 📱 Fully Responsive Design
- ⚡ High Performance
- 🎨 Modern UI/UX

---

## ✨ Features

### 👥 For Customers

| Feature | Description |
|---------|-------------|
| 🔐 **Authentication** | Secure account creation and login with ASP.NET Identity |
| 📖 **Browse Catalog** | Explore thousands of books organized by categories and genres |
| 🔍 **Smart Search** | Find books by title, author, keyword, or category instantly |
| 📖 **Book Details** | Comprehensive descriptions, author bios, customer reviews, and ratings |
| 🛒 **Shopping Cart** | Add/remove books, modify quantities, and save favorites |
| 💳 **Checkout** | Secure payment processing and order confirmation |
| 📋 **Order History** | Track all your purchases and delivery status |
| 📱 **Responsive UI** | Perfect experience on desktop, tablet, and mobile devices |

### 🛠️ For Administrators

| Feature | Description |
|---------|-------------|
| 📚 **Book Management** | Add, edit, delete, and manage book inventory |
| 🏷️ **Category Management** | Create and organize book categories |
| 📊 **Order Management** | Monitor, track, and update customer orders |
| 📈 **Inventory Control** | Track stock levels and manage availability |
| 👥 **User Management** | Monitor customer accounts and activity |

---

## 🛠️ Technology Stack

### Backend
```
.NET Core 6.0+
C# 10+
ASP.NET MVC
Entity Framework Core
```

### Frontend
```
HTML5
CSS3 (with responsive design)
JavaScript (ES6+)
Bootstrap (optional)
```

### Database & Infrastructure
```
SQL Server 2019+
Entity Framework Core (ORM)
```

### Architecture
```
MVC Pattern
SOLID Principles
Repository Pattern
Dependency Injection
```

---

## 📋 Prerequisites

Before you begin, ensure you have the following installed:

- **[.NET 6.0 SDK](https://dotnet.microsoft.com/download)** or higher
- **[Visual Studio 2022](https://visualstudio.microsoft.com/vs/)** (Community, Professional, or Enterprise)
  - OR **[Visual Studio Code](https://code.visualstudio.com/)** with C# extensions
- **[SQL Server 2019+](https://www.microsoft.com/sql-server/sql-server-downloads)** or SQL Server Express
- **[Git](https://git-scm.com/)** for version control

---

## 🚀 Quick Start

### Step 1: Clone the Repository

```bash
git clone https://github.com/JohnSnow46/iBoooks.git
cd iBoooks
```

### Step 2: Restore NuGet Packages

```bash
dotnet restore
```

### Step 3: Configure Database Connection

Edit `appsettings.json` and update the connection string:

```json
{
  "ConnectionStrings": {
    "DefaultConnection": "Server=YOUR_SERVER_NAME;Database=iBoooksDb;Trusted_Connection=true;"
  }
}
```

**Example configurations:**
- Local machine: `Server=(localdb)\\mssqllocaldb;Database=iBoooksDb;Trusted_Connection=true;`
- SQL Server Express: `Server=.\\SQLEXPRESS;Database=iBoooksDb;Trusted_Connection=true;`

### Step 4: Apply Database Migrations

```bash
dotnet ef database update
```

This creates the database schema and applies all pending migrations.

### Step 5: Run the Application

```bash
dotnet run
```

The application will start and be available at:
- **HTTPS**: `https://localhost:5001`
- **HTTP**: `http://localhost:5000`

---

## 📁 Project Structure

```
iBoooks/
│
├── Models/                 # Data models
│   ├── Book.cs
│   ├── User.cs
│   ├── Order.cs
│   ├── Cart.cs
│   └── Review.cs
│
├── Controllers/            # MVC Controllers
│   ├── HomeController.cs
│   ├── BooksController.cs
│   ├── CartController.cs
│   ├── OrderController.cs
│   └── AdminController.cs
│
├── Views/                  # Razor Views
│   ├── Home/
│   ├── Books/
│   ├── Cart/
│   ├── Order/
│   └── Admin/
│
├── Services/               # Business Logic Layer
│   ├── BookService.cs
│   ├── CartService.cs
│   ├── OrderService.cs
│   └── PaymentService.cs
│
├── Data/                   # Entity Framework
│   ├── ApplicationDbContext.cs
│   └── SeedData.cs
│
├── Migrations/             # Database Migrations
│
├── wwwroot/                # Static Assets
│   ├── css/
│   ├── js/
│   └── images/
│
└── appsettings.json        # Configuration File
```

---

## 🔐 Security Features

iBoooks implements comprehensive security measures:

✅ **Authentication & Authorization**
- ASP.NET Identity for user management
- Role-based access control (RBAC)
- Secure password hashing

✅ **Data Protection**
- CSRF (Cross-Site Request Forgery) protection
- SQL Injection prevention via Entity Framework Core
- Input validation on both client and server side
- XSS (Cross-Site Scripting) protection

✅ **Secure Communication**
- HTTPS/TLS encryption
- Secure cookie handling
- Authorization checks on sensitive operations

✅ **Payment Security**
- PCI DSS compliant payment processing
- Secure transaction logging

---

## 🗄️ Database Schema

The application uses the following main entities:

- **Users** - Customer and admin accounts
- **Books** - Book catalog with metadata
- **Categories** - Book categories and genres
- **ShoppingCart** - User shopping carts
- **Orders** - Customer orders and history
- **OrderItems** - Items within orders
- **Reviews** - Customer book reviews
- **Reviews** - Customer ratings and feedback

---

## 📦 NuGet Dependencies

Key packages used in the project:

```xml
<PackageReference Include="Microsoft.EntityFrameworkCore" />
<PackageReference Include="Microsoft.EntityFrameworkCore.SqlServer" />
<PackageReference Include="Microsoft.EntityFrameworkCore.Tools" />
<PackageReference Include="Microsoft.AspNetCore.Identity.EntityFrameworkCore" />
```

---

## 🔧 Configuration

### Application Settings (appsettings.json)

```json
{
  "ConnectionStrings": {
    "DefaultConnection": "Server=...;Database=iBoooksDb;..."
  },
  "Logging": {
    "LogLevel": {
      "Default": "Information"
    }
  },
  "AllowedHosts": "*"
}
```

### Environment-Specific Settings

- `appsettings.Development.json` - Development settings
- `appsettings.Production.json` - Production settings

## 📤 Deployment

### Deploy to Azure App Service

```bash
# Install Azure CLI
az login

# Create resource group
az group create --name iBoooks-rg --location eastus

# Deploy
dotnet publish -c Release
```

### Deploy Locally (IIS)

1. Publish the application: `dotnet publish -c Release`
2. Copy contents to IIS directory
3. Create new IIS Application
4. Configure Application Pool (.NET Framework v4.0)

---

## 🐛 Troubleshooting

| Issue | Solution |
|-------|----------|
| **Migration failed** | Ensure SQL Server is running and connection string is correct |
| **Port already in use** | Change port in `launchSettings.json` |
| **404 errors** | Verify routing configuration in `Startup.cs` |
| **CSS/JS not loading** | Run `dotnet build` and check `wwwroot/` folder |

---

## 📝 License

This project is licensed under the **MIT License** - see the [LICENSE](LICENSE) file for details.

---

## 🎓 Learning Resources

New to .NET? Check out these resources:

- [Microsoft Learn - ASP.NET Core](https://learn.microsoft.com/en-us/aspnet/core/)
- [Microsoft Learn - Entity Framework Core](https://learn.microsoft.com/en-us/ef/core/)
- [C# Documentation](https://learn.microsoft.com/en-us/dotnet/csharp/)
- [SQL Server Documentation](https://learn.microsoft.com/en-us/sql/sql-server/)

---

## 📊 Project Status

- ✅ Core features implemented
- ✅ Database schema designed
- ✅ Authentication system
- ✅ Shopping functionality
- 🚧 Payment integration in progress
- 🚧 Advanced analytics

---

## 🎉 Credits

- Built with ❤️ using .NET and ASP.NET Core
- Icons from [Feather Icons](https://feathericons.com/)
- Inspired by modern e-commerce practices