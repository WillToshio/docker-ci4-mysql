# Usar a imagem oficial do PHP com Apache
FROM php:8.1-apache

# Instalar dependências do sistema e extensões PHP necessárias
RUN apt-get update && apt-get install -y \
    libicu-dev \
    git \
    && docker-php-ext-install intl pdo pdo_mysql
#    a2enmod rewrite

# Configurar o diretório de trabalho para a aplicação
WORKDIR /var/www/html

# Copiar o código-fonte da aplicação para o container
COPY ./src /var/www/html/

# Garantir que a pasta writable e seus subdiretórios têm as permissões corretas
RUN chown -R www-data:www-data /var/www/html/codeigniter/writable && \
    chmod -R 775 /var/www/html/codeigniter/writable

# Definir o usuário padrão para o Apache
USER www-data

# Expor a porta 80 para o servidor Apache
EXPOSE 80

# Habilitar o mod_rewrite do Apache
# RUN a2enmod rewrite

# Definir variáveis de ambiente (se necessário)
# ENV PHP_INI_DIR=/usr/local/etc/php

# Configuração personalizada do Apache, caso necessário
# COPY ./docker/app/config/000-default.conf /etc/apache2/sites-available/000-default.conf

# Comando para iniciar o Apache
# CMD ["apache2-foreground"]