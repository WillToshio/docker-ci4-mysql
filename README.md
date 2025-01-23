# Estrutura do diretório
```
my-docker-project/
├── docker/
│   ├── app/             # Arquivos de configuração específicos do serviço (ex: Dockerfile do app)
│   │   ├── Dockerfile
│   │   └── config/      # Configurações específicas (se necessário)
│   └── db/              # Configuração do banco de dados
│       └── Dockerfile
├── src/                 # Código-fonte da aplicação
│   ├── app/
│   ├── public/
│   ├── system/
│   ├── tests/
│   ├── writable/
│   ├── .env
│   ├── composer.json
│   ├── LINCESE
│   ├── phpunit.xml.dist
│   ├──preload.php
│   ├──README.md
│   └──spark
├── .env                 # Variáveis de ambiente
├── docker-compose.yml   # Arquivo principal do Docker Compose
└── README.md            # Documentação do projeto

```

### Este projeto é próprio para o mysql


<!-- # *não há o que fazer não esqueça de rodar na linha de comando*
```
    docker exec -it app_container bash
```

## assim que abrir o bash insira o comando a baixo
```
cd /var/www/html/codeigniter

# Alterar as permissões para permitir leitura e escrita na pasta 'writable'
chown -R www-data:www-data writable
chmod -R 775 writable

```
-->

### Para rodar o projeto abra um terminal no diretório e digite o comando a baixo 
```
docker-compose build
docker-compose --env-file .env up -d
```

### Após alguma modificação apenas rodar o comando
```
docker-compose down 
docker-compose --env-file .env up -d
```

### Não esqueçam de cirar o arquivo .env com as informações 
*neste caso as informações do banco de dados*
