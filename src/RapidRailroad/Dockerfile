# Base of your container
FROM microsoft/aspnet:1.0.0-rc1-final-coreclr

# Copy the project into folder and then restore packages
COPY . /app
WORKDIR /app
RUN ["dnu","restore"]

# Open this port in the container
EXPOSE 80
# Start application
ENTRYPOINT ["dnx","-p","project.json", "web"]