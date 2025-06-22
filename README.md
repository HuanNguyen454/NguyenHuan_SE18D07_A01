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

## How to Run the Project

1. Clone the repository
2. Update the connection strings in both appsettings.json files as described above
3. Open file `NguyenHuan_SE18D01_A01.sln` with Visual Studio
4. Build the solution
5. Run the project NguyenHuanWPF using the command:
   
   ```
   dotnet run --project NguyenHuanWPF
   ```

## Login Information

### Admin:
- **Email**: admin@FUMiniHotelSystem.com
- **Password**: @@abc123@@




