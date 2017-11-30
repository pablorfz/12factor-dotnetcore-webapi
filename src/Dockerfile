# Use the standard Microsoft .NET Core container

FROM microsoft/dotnet

# Copy our published code from the “/app” folder to the “/app” folder in our container

WORKDIR /app

COPY /app /app

# Add environment variable to ensure web server doesn't just listen on localhost (needed since we are running this in a container, not locally)

ENV ASPNETCORE_URLS http://+:80

# Expose port 80 for the Web API traffic

EXPOSE 80

# Build and run the dotnet application from within the container

ENTRYPOINT dotnet dotnetcore-webapi.dll