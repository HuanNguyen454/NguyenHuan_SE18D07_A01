# FU Mini Hotel System

A hotel management system developed as part of the PRN212 course. This WPF application allows for managing hotel rooms, customers, and bookings.

## Features

- Room Management (Add, Edit, Delete, Search)
- Customer Management
- Booking Reservations
- User Authentication
- Reporting

## Technologies

- C# WPF (.NET 6.0)
- MVVM Architecture
- Entity Framework Core

## Project Structure

- **BusinessObjects**: Contains the model classes
- **DataAccessObjects**: Data access layer
- **Repositories**: Repository interfaces and implementations
- **Services**: Business logic services
- **NguyenHuanWPF**: WPF UI application

## Database Configuration

This project requires SQL Server to be installed. You need to modify the connection strings in the following files:

1. `BusinessObjects/appsettings.json`
2. `NguyenHuanWPF/appsettings.json`

Update the connection string to match your SQL Server configuration:

```json
{
  "ConnectionStrings": {
    "HotelDB": "Server=YOUR_SERVER_NAME;Database=HotelManagementDB;User Id=YOUR_USERNAME;Password=YOUR_PASSWORD;TrustServerCertificate=True;MultipleActiveResultSets=True"
  }
}
```

Replace:
- `YOUR_SERVER_NAME` with your SQL Server instance name
- `YOUR_USERNAME` with your SQL Server username
- `YOUR_PASSWORD` with your SQL Server password

## Database Migration

This project uses Entity Framework Core Code First approach. To create the database and apply migrations, follow these steps:

### Using Command Line

1. Open a command prompt or PowerShell
2. Navigate to the project directory
3. Install Entity Framework Core tools (if not already installed):
   ```
   dotnet tool install --global dotnet-ef
   ```
4. Navigate to the BusinessObjects project directory:
   ```
   cd BusinessObjects
   ```
5. Create a new migration (if needed):
   ```
   dotnet ef migrations add InitialCreate
   ```
6. Apply the migration to create/update the database:
   ```
   dotnet ef database update
   ```

### Using Visual Studio Package Manager Console

1. Open Visual Studio and load the solution
2. Open Package Manager Console (Tools > NuGet Package Manager > Package Manager Console)
3. Set Default Project to "BusinessObjects"
4. Create a new migration (if needed):
   ```
   Add-Migration InitialCreate
   ```
5. Apply the migration:
   ```
   Update-Database
   ```

## How to Run the Project

1. Clone the repository
2. Update the connection strings in both appsettings.json files as described above
3. Create and update the database using the migration steps above
4. Open file `NguyenHuan_SE18D01_A01.sln` with Visual Studio
5. Build the solution
6. Run the project NguyenHuanWPF using the command:
   
   ```
   dotnet run --project NguyenHuanWPF
   ```

## Login Information

### Admin:
- **Email**: admin@FUMiniHotelSystem.com
- **Password**: @@abc123@@




