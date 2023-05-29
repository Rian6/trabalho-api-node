# App Food - (Aplicação didática feita para aula de Web 2)
## Preparação do ambiente de desenvolvimento

### Requisitos

Node - https://nodejs.org/en

Docker - https://www.docker.com/

Insomnia (Opcional) - https://insomnia.rest/download

### Rodando projeto

Para instalar as dependencias do projeto entre na pasta raiz e use o comando:

```
npm install
```

O banco mongo precisar ser rodado em  um container docker, para rodar o banco use o comando:

```
docker run --rm -d -p 27017:27017 mongo
```

Esse comando vai repassar tudo que cair na porta 27017 do computador para a porta 27017 do container

E por fim para rodar a aplicação use o comando:
```
npm run dev
```

A aplicação vai rodar na porta 3000 por padrão

### Testando a aplicação

Para testar o servidor vamos usar o insomnia, você pode usar outra aplicação que envie requições http ou uma aplicação real, para o teste temos a seguinte rota que trabalha com uma tabela de alunos no mongo:
```
http://localhost:3000/alunos GET/POST
```
Abra o insomnia e você vai ver essa tela

![Alt ou título da imagem](img-1.png)


Para realizar um cadastro no banco precisamos trocar o tipo de requisição para post, colar a url selecionar o corpo para JSON e adicionar os dados, você pode usar esse JSON de exemplo para preencher a tabela de alunos:
```
{
	"nome": "",
	"sobrenome": "",
	"email": "",
	"datanascimento": "",
	"matricula": ""
}
```
O corpo da requisição deve ficar assim:
![image](https://github.com/Rian6/trabalho-api-node/assets/34445730/7b840490-cacf-419b-b59a-bd946ac8901c)

Para visualizar os dados salvos, você pode selecionar a opção GET e colar a mesma url.
