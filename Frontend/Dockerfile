# FROM --platform=linux/amd64 node:16.17

# WORKDIR /app
# EXPOSE 80
# COPY . /app
# RUN npm install


# # Use the official nginx image as the base image.
# FROM nginx:alpine

# # Copy the index.html file into the nginx HTML directory.
# COPY index.html /usr/share/nginx/html/

# # Copy the js directory into the nginx HTML directory.
# COPY scripts /usr/share/nginx/html/scripts/

# # Expose port 80 to access the web server.
# EXPOSE 80




# Use the official nginx image as the base image.
FROM nginx:alpine

# Copy the custom NGINX configuration file into the container.
COPY nginx.conf /etc/nginx/conf.d/default.conf

# Copy the index.html file into the nginx HTML directory.
COPY *.html /usr/share/nginx/html/

# Copy the scripts directory into the nginx HTML directory.
COPY scripts /usr/share/nginx/html/scripts/

# Expose port 80 to access the web server.
EXPOSE 80
