FROM ubuntu:20.04

WORKDIR /app

EXPOSE 5000

ENV ASPNETCORE_URLS http://*:5000

RUN apt update; apt install wget -y;

RUN wget https://packages.microsoft.com/config/ubuntu/20.10/packages-microsoft-prod.deb -O packages-microsoft-prod.deb; \
    dpkg -i packages-microsoft-prod.deb

RUN apt-get update; \
    apt-get install -y apt-transport-https && \
    apt-get update && \
    apt-get install -y aspnetcore-runtime-3.1

COPY src/Otus.Teaching.PromoCodeFactory.WebHost/bin/Release/netcoreapp3.1/publish ./

CMD dotnet Otus.Teaching.PromoCodeFactory.WebHost.dll

