from wordpress:4.9.2-php7.2-apache

RUN apt-get update && apt-get install -y sudo less mysql-server

# Add WP-CLI
RUN curl -o /bin/wp-cli.phar https://raw.githubusercontent.com/wp-cli/builds/gh-pages/phar/wp-cli.phar
COPY wp-su.sh /bin/wp
RUN chmod +x /bin/wp-cli.phar /bin/wp

# Cleanup
RUN apt-get clean
RUN rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*

# Setup DB
#COPY wp-db.sh /
#CMD "/wp-db.sh"
