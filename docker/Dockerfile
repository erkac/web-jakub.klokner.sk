FROM nginx:alpine

# Copy the website files to nginx html directory
COPY web /usr/share/nginx/html

# Copy custom nginx configuration if needed
COPY docker/nginx.conf /etc/nginx/conf.d/default.conf

# Expose port 80
EXPOSE 80

# Start nginx
CMD ["nginx", "-g", "daemon off;"]