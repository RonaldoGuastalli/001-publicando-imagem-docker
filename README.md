# Publicando Imagem Docker (code.education)

## 1. Configurar um ambiente Laravel utilizando o docker-compose com:

Nginx
PHP-FPM
Redis
MySQL

Lembrando que o volume do código fonte deve ser compartilhado com a App.

Após realizarmos a clonagem do repositório e executarmos: docker-compose up -d, poderemos ver a aplicação Laravel rodando com o erro de autoload na porta: 8000, uma vez que o docker-compose não executou o composer install do PHP, logo, não se preocupe com tal detalhe nesse momento. 

## 2. Após ter tido sucesso na etapa anterior, faça a configuração do framework Laravel seguindo as etapas (dentro do container):

execute composer install
crie o arquivo .env baseado no .env.example 
execute: php artisan key:generate 
execute: php artisan migrate
* Nesse momento, quando você acessar a aplicação no browser, finalmente, você deverá ver a página inicial do Laravel funcionando.

Baseado nessas últimas ações, gere o build da imagem desse container e faça a publicação em sua conta no Hub do Docker.

Lembre-se: Ao gerar o build da imagem, TODO o conteúdo incluindo arquivos como vendor, .env, etc deverão ser incluídos.

Adicione o endereço da imagem no seu dockerhub no README.md e faça o commit para um repositório público do Github.

Arquivos e códigos úteis para auxiliar no exercício incluindo nginx.conf e linha de comando para baixar o composer. Clique aqui.

* A imagem gerada encontra-se no seguinte endereço no dockerhub
  https://hub.docker.com/repository/docker/guastalli31/app-laravel 
