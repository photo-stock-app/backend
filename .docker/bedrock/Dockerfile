# Use the official PHP 8.4-FPM image with multi-platform support
FROM php:8.2-fpm-alpine

# Install necessary packages and dependencies
RUN apk add --no-cache \
    libzip-dev \
    unzip \
    && docker-php-ext-install zip pdo pdo_mysql mysqli

# Set the working directory
WORKDIR /app

# Copy application files

COPY . .

# Expose the port
EXPOSE 9000

# Start PHP-FPM
CMD ["php-fpm"]