In solution folder  
```dotnet new sln```

```dotnet new nunit -o xyzTest```

Change to ```xyzTest``` folder  
```dotnet add package Selenium.WebDriver```  
```dotnet add package Selenium.WebDriver.ChromeDriver```  
```dotnet add package Selenium.Support```

Back in solution folder  
```dotnet sln add .\xyzTest\xyzTest.csproj```

To add `xyz` project reference to `xyzTest`, from solution folder  
```dotnet add .\xyzTest\xyzTest.csproj reference .\xyz\xyz.csproj```