#See https://aka.ms/containerfastmode to understand how Visual Studio uses this Dockerfile to build your images for faster debugging.

# FROM mcr.microsoft.com/dotnet/core/runtime:2.1-stretch-slim AS base
# WORKDIR /app

# FROM mcr.microsoft.com/dotnet/core/sdk:2.1-stretch AS build
# WORKDIR /src
# COPY firstmacvsconsole/firstmacvsconsole.csproj firstmacvsconsole/
# RUN dotnet restore "firstmacvsconsole/firstmacvsconsole.csproj"
# COPY . .
# WORKDIR "/src/firstmacvsconsole"
# RUN dotnet build "firstmacvsconsole.csproj" -c Release -o /app/build

# FROM build AS publish
# RUN dotnet publish "firstmacvsconsole.csproj" -c Release -o /app/publish

# FROM base AS final
# WORKDIR /app
# COPY --from=publish /app/publish .
# ENTRYPOINT ["dotnet", "firstmacvsconsole.dll"]

FROM mcr.microsoft.com/dotnet/core/aspnet:2.1
COPY bin/Release/netcoreapp2.1/publish/ App/
WORKDIR /App
ENTRYPOINT ["dotnet", "firstmacvsconsole.dll"]