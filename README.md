# conversao-temperatura 
É aplicação web construída em NodeJS que realiza a conversão de valores de temperatura de Celcius para Fahrenheit e de Fahrenheit para Celsius.

# Ignorando arquivos desnecessários na criação da imagem
No diretório da aplicação podem existir arquivos indesejados e/ou desnecessários que seriam copiados com o comando COPY e que poderiam ser ignorados durante o processo de criação da imagem Docker.

Para isso foi criado no mesmo diretório onde se encontram os arquivos do projeto o arquivo .dockerignore que possui uma lista (com o mesmo padrão do arquivo .gitignore) com os diretórios/arquivos que serão ignorados no momento da execução da cópia dos arquivos para dentro da imagem.

Foi criado dentro do projeto um arquivo Dockerfile que  será utilizada para execução da aplicação em um container, como mostra abaixo:

![image](https://user-images.githubusercontent.com/96360563/154427605-ed35b3ec-47b4-456b-b0eb-46b9b71d9ea1.png)

# Para criação da imagem Docker foi executada, dentro do diretório da aplicação, a linha de comando:

docker build -t ferrarijose/conversao-temperatura:v1 .

Utilizando o comando docker build com o parâmetro -t para configurar o nome da imagem a ser criada

# Para testar a imagem criada, usamos o comando:

docker container run -d --name conversao-temperatura -p 8080:8080 ferrarijose/conversao-temperatura:v1

# Para acessar a aplicação é deverá usar a porta da aplicação 8080

http://localhost:8080
