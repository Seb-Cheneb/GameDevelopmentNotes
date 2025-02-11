---

---
---

Adding the EF package
```powershell
dotnet add package Microsoft.EntityFrameworkCore.Design
```

Installing EF tools
```powershell
dotnet tool install --global dotnet-ef
```

Add a new migration
```powershell
dotnet ef migrations add NEW_MIGRATION_NAME
```

Update the database
```powershell
dotnet ef database update
```

Drop the database:
```powershell
dotnet ef database drop
```