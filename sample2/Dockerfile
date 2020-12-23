FROM mcr.microsoft.com/dotnet/core/aspnet:3.1

WORKDIR /app

ENV ASPNETCORE_URLS=http://*:5000

EXPOSE 5000

COPY src/Otus.Teaching.PromoCodeFactory.WebHost/bin/Release/netcoreapp3.1/publish ./

CMD dotnet Otus.Teaching.PromoCodeFactory.WebHost.dll
