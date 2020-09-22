# Simple commands


Make sure we installed dotnet ef tools as a global tool using:

```
dotnet tool install --global dotnet-ef
````


# To scaffold a DbContext in a seperate library.

- Open Command line in the projects directory (When you have Open Command Line extension installed and configured, just press alt-space)

```
dotnet ef dbcontext scaffold "Data Source=localhost;Initial Catalog=DBName;Integrated Security=True" Microsoft.EntityFrameworkCore.SqlServer -f -c DbNameDbContext
```