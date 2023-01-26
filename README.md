# pizza-shop-csharp-be-tut

A C# / ASP.Net Core tutorial creating an MVC Rest API .


# Notes

dotnet new gitignore => creates a template .gitignore file

dotnet --list-sdks => lists the dotnet sdk versions installed

dotnet tool install -g Microsoft.dotnet-httprepl => installs the httpRepl tool

dotnet build => builds a dotnet asp app

dotnet run --urls=https://localhost:5101 => launches the app and listens on port 5101
httprepl https://localhost:5101 => (in new terminal) conects to the listening api

ls => lists the endpoints
cd => switch to the endpoint e.g. Pizzas
pref set editor.command.default "C:\Users\my-user\AppData\Local\Programs\Microsoft VS Code\Code.exe" => Sets the default JSON editor

dotnet add package Microsoft.EntityFrameworkCore.Sqlite => Add SQLLite NuGet package

dotnet add package Microsoft.EntityFrameworkCore.Design => Add EF Core Tools NuGdt package

dotnet tool install --global dotnet-ef => Install EF Core Tools
dotnet tool update --global dotnet-ef => Update EF Core Tools if already installed


dotnet ef migrations add InitialCreate --context PizzaContext => generate a db migration
dotnet ef database update --context PizzaContext => Applies InitialCreate migration

dotnet ef migrations add ModelRevisions --context PizzaContext => as above
dotnet ef database update --context PizzaContext 


Scaffold entities from existing database =>
dotnet ef dbcontext scaffold "Data Source=.\Promotions\Promotions.db" Microsoft.EntityFrameworkCore.Sqlite --context-dir .\Data --output-dir .\Models
