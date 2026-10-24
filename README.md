# ExpenseTrackerAPI

A secure personal finance REST API built using ASP.NET Core Web API, C#, Entity Framework Core, and SQL Server. ExpenseTrackerAPI helps users manage their income and expenses, organize transactions by category, and track their financial position through dashboard analytics.

## Features

- **JWT Authentication:** User registration and login with token-based authentication.
- **User-Specific Data Isolation:** Restricts access to each user's own financial records.
- **Category Management:** Create, update, and soft-delete categories.
- **Income and Expense Management:** Manage financial transactions through RESTful API endpoints.
- **Dashboard Analytics:** Calculate total income, total expenses, and remaining balance.
- **Pagination:** Retrieve expense records in manageable pages, with limits on page size.
- **Global Soft Delete:** Exclude deleted records from normal queries without permanently removing them from the database.
- **Unit Testing:** Test application behavior using xUnit.

## Tech Stack

- **Language:** C#
- **Backend:** ASP.NET Core Web API (.NET 8)
- **Database:** SQL Server
- **ORM:** Entity Framework Core
- **Authentication:** JWT Bearer Authentication
- **Data Querying:** LINQ
- **Testing:** xUnit
- **API Tools:** Swagger / Postman
- **Architecture:** RESTful API with controllers, services, models, and DTOs

## Project Structure

ExpenseTrackerAPI/
├── Controllers/   # API endpoints
├── Models/        # Entity models
├── DTOs/           # Request and response objects
├── Data/           # DbContext and database configuration
├── Services/       # Business logic
├── Tests/          # Unit tests
├── appsettings.json
└── README.md


## Key Implementation Details

- Implemented JWT-based authentication to protect secured endpoints.
- Applied user-specific filtering to keep financial records isolated between users.
- Used Entity Framework Core for database operations and entity relationships.
- Implemented pagination with a maximum page-size limit to control the number of returned records.
- Used global query filters for soft-deleted records.
- Created dashboard calculations for income, expenses, and balance.
- Organized the application into separate components to improve maintainability and testability.

## How to Run Locally

### Prerequisites

- .NET 8 SDK
- SQL Server or SQL Server LocalDB
- Visual Studio or another .NET-compatible IDE

### Setup

1. Clone the repository:

   ```bash
   git clone <your-repository-url>
   cd ExpenseTrackerAPI
   ```

2. Configure your SQL Server connection string in `appsettings.json` or your local development configuration.

3. Configure the JWT settings required by the application. Use a secure secret and do not commit production credentials.

4. Apply the Entity Framework Core migrations:

   ```bash
   dotnet ef database update
   ```

   If the EF Core CLI tool is not installed, install it first. Ensure the project and startup project are configured correctly.

5. Run the API:

   ```bash
   dotnet run
   ```

6. Open the Swagger URL shown in the terminal, if Swagger is enabled in the current environment, to explore and test the API endpoints.

### Run Tests

Run the test suite from the solution or repository root:

```bash
dotnet test
```

## Learning Outcomes

Through this project, I gained practical experience in:

- Designing and implementing RESTful APIs using ASP.NET Core.
- Implementing authentication and authorization with JWT.
- Enforcing user-specific access to application data.
- Working with Entity Framework Core and SQL Server.
- Implementing pagination and global soft-delete behavior.
- Writing unit tests using xUnit.
- Structuring backend code for maintainability and easier testing.

## Future Improvements

- Add integration tests for API endpoints and database interactions.
- Introduce Docker-based development and deployment.
- Add CI/CD automation for building and testing the application.
- Improve API documentation and production deployment configuration.

