# Demo project to test dotnet publish issue from cli

1. clone the project
2. Within the root folder execute the following
    - `dotnet restore`
    - `dotnet build --no-restore -c Release`
    - `dotnet test --no-build -c Release`
    - `dotnet publish "Dotnet31ConsoleApp/Dotnet31ConsoleApp.csproj" --no-build -c Release -r win-x64 --self-contained true -p:PublishSingleFile=true -p:PublishTrimmed=true -p:ReadyToRun=true -p:ReadyToRunShowWarnings=true -p:Version=1.0 -o publish/win`

> Do not use VS publish option. If so delete the file from bin folder
