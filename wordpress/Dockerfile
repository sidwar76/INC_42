# Dockerfile
FROM wordpress:latest

# Copy the custom WordPress configuration file to the container
COPY wp-config.php ./

# Install necessary packages
RUN docker-php-ext-install -y mysqli && \
    docker-php-ext-configure gd --with-gd --with-freetype --with-jpeg && \
    docker-php-ext-install -y gd && \
    docker-php-ext-install -y pdo_mysql && \
    docker-php-ext-install -y soap

# Expose the WordPress port
EXPOSE 80