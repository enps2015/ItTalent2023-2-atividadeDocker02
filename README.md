# ItTalent2023-2-atividadeDocker02
Este repositório faz parte do programa IT TAlent na atividade 02 de Docker. Onde foi criada uma imagem docker contendo uma aplicação web de minha autoria e disponibilizada aqui no github.

## Imagem Docker com aplicação web

Atividade Docker 02

Crie uma imagem Docker para uma aplicação de sua escolha, utilizando a linguagem de programação de sua preferência. Realize a etiquetagem (tag) desta imagem e faça o envio para o seu repositório pessoal no Docker Hub. Ao concluir esta tarefa, prepare um relatório que descreva o arquivo Dockerfile criado e inclua o link para a imagem publicada em seu Docker Hub. 


Para usar como aplicação web, tomei a liberdade de criar meu próprio site. Então criei um Blog do DevOps. Os arquivos usados no dockerfile foram:
- index.html
- style.css
- /img

O conteúdo do meu dockerfile foi:

FROM nginx:latest
COPY index.html /usr/share/nginx/html
COPY style.css /usr/share/nginx/html
COPY img /usr/share/nginx/html/img

Criado o dockerfile depois fiz o build da imagem docker:

- docker build -t aplicacao-eric .

![image](https://github.com/enps2015/ItTalent2023-2-atividadeDocker02/assets/84017071/f82cfe9e-88d7-4374-a290-c92b07dc799a)

  
Apos isso criei uma tag para minha imagem aplicacao-eric usando meu usuário docker 039532, com o comando:

- docker tag aplicacao-eric 039532/aplicacao-eric:eric1.0

E após feito isso subi a imagem criada com a devida tag para o meu repositório no docker hub:

- docker push 039532/apliacacao-eric:eric1.0

![image](https://github.com/enps2015/ItTalent2023-2-atividadeDocker02/assets/84017071/83bbdc10-6a0d-48cc-b942-bd78a4737453)

![image](https://github.com/enps2015/ItTalent2023-2-atividadeDocker02/assets/84017071/b96b4db8-6c1f-405b-a04e-41efc2538b13)

A imagem docker foi baixada e colocada pra rodar na minha máquina local:

- docker run -p 8080:80 039532/aplicacao-eric:eric1.0

![image](https://github.com/enps2015/ItTalent2023-2-atividadeDocker02/assets/84017071/635809cf-80ab-4f2c-a800-2fbcc6f4eb2e)


Docker hub:
https://hub.docker.com/r/039532/aplicacao-eric/tags

Github:
https://github.com/enps2015/blog-devops
https://enps2015.github.io/blog-devops/

Muito obrigado por você ter ficado até aqui!




