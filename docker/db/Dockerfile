# Usar a imagem oficial do MySQL
FROM mysql:8.0

# Copiar os scripts de inicialização (se houver) para o banco de dados
COPY ./docker/db/init.sql /docker-entrypoint-initdb.d/

# Definir variáveis de ambiente para a configuração do banco
ENV MYSQL_ROOT_PASSWORD=
ENV MYSQL_DATABASE=
ENV MYSQL_USER=
ENV MYSQL_PASSWORD=

# Expor a porta 3306 para a conexão com o banco de dados
EXPOSE 3306