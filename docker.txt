# Use a lightweight web server image
FROM nginx:alpine

RUN apt-get update


WORKDIR /app

# Copy the project files to the default Nginx public directory
COPY . /usr/share/nginx/html

# Expose port 80
EXPOSE 80

# Command to run the Nginx server
CMD ["nginx", "-g", "daemon off;"]
