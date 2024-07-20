# Use the official PHP 8.2-FPM image with multi-platform support
FROM php:8.2-fpm-alpine

# Install necessary packages and dependencies
RUN apk add --no-cache \
    libzip-dev \
    unzip \
    && docker-php-ext-install zip pdo pdo_mysql mysqli

# Set the working directory
WORKDIR /app

# Copy application files and set ownership
COPY --chown=www-data:www-data . .

# Ensure the www-data user owns the /app directory
RUN chown -R www-data:www-data /app

# Expose the port
EXPOSE 9000

# Start PHP-FPM
USER www-data
CMD ["php-fpm"]
