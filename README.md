================================================================================
                    iBoooks - Online Bookstore
================================================================================

A modern, user-friendly online bookstore application built with ASP.NET MVC. 
Browse, search, and purchase books with ease. This project demonstrates 
professional web development practices, clean architecture, and responsive UI 
design.

================================================================================
                              FEATURES
================================================================================

FOR CUSTOMERS:

- User Registration & Authentication - Create a secure account and log in to 
  the bookstore

- Browse Books - Explore an extensive collection of books organized by 
  categories

- Book Details - View comprehensive descriptions, author information, and 
  customer reviews

- Search Functionality - Quickly find books by title, author, or keywords

- Shopping Cart - Add books to cart, modify quantities, and review selections

- Checkout & Orders - Complete purchases and track order history

- Responsive Design - Seamless experience across all devices and screen sizes


FOR ADMINISTRATORS:

- Book Management - Add, edit, and delete books from the catalog

- Category Management - Organize books into categories

- Order Tracking - Monitor customer orders and order status

- Inventory Control - Track book stock levels

================================================================================
                          TECHNOLOGY STACK
================================================================================

BACKEND
  .NET Core, C#, ASP.NET MVC

FRONTEND
  HTML5, CSS3, JavaScript

DATABASE
  SQL Server

ARCHITECTURE
  MVC, Entity Framework Core

================================================================================
                             REQUIREMENTS
================================================================================

- .NET 6.0 or higher
- SQL Server 2019+ (or SQL Server Express)
- Visual Studio 2022 (recommended) or Visual Studio Code with C# extensions

================================================================================
                          GETTING STARTED
================================================================================

1. CLONE THE REPOSITORY

   git clone https://github.com/JohnSnow46/iBoooks.git
   cd iBoooks

2. RESTORE NUGET PACKAGES

   dotnet restore

3. CONFIGURE DATABASE

   Update the connection string in appsettings.json:

   {
     "ConnectionStrings": {
       "DefaultConnection": "Server=YOUR_SERVER;Database=iBoooksDb;Trusted_Connection=true;"
     }
   }

4. APPLY DATABASE MIGRATIONS

   dotnet ef database update

5. RUN THE APPLICATION

   dotnet run

   The application will be available at https://localhost:5001

================================================================================
                          PROJECT STRUCTURE
================================================================================

iBoooks/
├── Models/              # Data models (Book, User, Order, Cart, etc.)
├── Controllers/         # ASP.NET MVC controllers
├── Views/              # HTML/Razor views
├── Services/           # Business logic layer
├── Data/               # Entity Framework DbContext
├── wwwroot/            # Static assets (CSS, JS, images)
├── Migrations/         # Entity Framework migrations
└── appsettings.json    # Application configuration

================================================================================
                             SECURITY
================================================================================

- ASP.NET Identity-based authentication
- Password encryption
- CSRF protection
- Server-side and client-side data validation
- SQL Injection prevention via Entity Framework Core
- Authorization checks on admin operations
- Secure payment processing

================================================================================
                              LICENSE
================================================================================

This project is licensed under the MIT License.