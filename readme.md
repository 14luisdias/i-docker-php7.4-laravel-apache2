DOCKER APLICAÇÃO DO PCIGMA

primeiramente ná maquina a buildar tem de ter instalada a ferramenta Docker

 1. para criar a imagem execute:
     # sudo docker build -t i-php7.4-apache2:7.4 .
  obs: 
     => i-ap-php7_4-apache2 -> é o nome da imagem
     => :7.4 é o TAG da versão
     
 2. para criar o conteiner ir na pasta onde está localizado o código fonte:
    NO LINUX EXECUTE
    # sudo docker run -d --name c-ap-super-gestao -v $PWD:/code -p 7000:80 i-php7.4-apache2:7.4

    NO WINDOWS IR NA IMAGEM E CLICLAR EM RUN PREENCHA OS CAMPOS
   obs:
      - Optional Settings
      - Container Name -> c-ap-php8-2-apache2-laravel-alura
      - Ports:Local Host -> 7000 code
      - Volumes:Host Path -> selecionar a pasta onde está localizada o codigo fonte do curso
      - Container Path -> /code
      - i-ap-php-apache - > nome da imagem
      - RUN
vscode