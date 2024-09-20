# Locations API

This project is a simple API to manage locations using ASP.NET Core and Entity Framework Core.

## Requirements

- .NET SDK 8.0+
- PostgreSQL
- Postman (optional for testing)

## Installation

1. Clone the repository:
    ```bash
    git clone https://github.com/jjgonzalez64/locations-api.git
    ```

2. Navigate to the project folder:
    ```bash
    cd locations-api
    ```

3. Install the dependencies:
    ```bash
    dotnet restore
    ```

4. Update the connection string in `database.cs` to match your PostgreSQL instance.

5. Run the migrations and start the application:
    ```bash
    dotnet ef database update
    dotnet run
    ```

## Endpoints

- **POST /api/locations** - Create a new location
- **PUT /api/locations/{id}** - Update a location by id
- **DELETE /api/locations/{id}** - Delete a location by id
- **GET /api/locations/{id}** - Get a location by id
- **GET /api/locations/search?name=&address=&coordinates=** - Filter locations

## Testing

You can test the API using Postman or any other API testing tool. Here's an example JSON body for creating a location:

```json
{
  "name": "Central Park",
  "address": "New York, NY",
  "coordinates": { "x": -73.968285, "y": 40.785091 },
  "route": "..."  
}
```
