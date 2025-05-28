# olá, esse projeto serve para listar alguns comandos do git

## como criar um projeto no github

- instale o git  
- instale o vs code  
- faça uma conta no github  
- crie um repositório no github (não marque nenhuma caixinha durante a criação)  
- copie o link https que foi gerado (exemplo):  
  `https://github.com/seu-usuario/nome-do-repositorio.git`  
- crie uma pasta no seu computador  
- abra a pasta com o vs code  
- no vs code, crie um novo arquivo `.md` (exemplo: `readme.md`)  
- dentro do arquivo, escreva alguma mensagem  
- salve o arquivo
- abra o git bash  
- verifique se o git está instalado:  
  `git --version`  
- acesse a pasta com o comando (exemplo):  
  `cd desktop\git`  
- inicialize o git na pasta:  
  `git init`  
- adicione os arquivos ao *staging*:  
  `git add .`  
- faça o primeiro commit:  
  `git commit -m "primeiro commit"`  
- conecte o repositório local ao remoto:  
  `git remote add origin https://github.com/seu-usuario/nome-do-repositorio.git`  
- defina a branch principal como `main`:  
  `git branch -M main`  
- envie os arquivos para o github:  
  `git push -u origin main`  
- abra a página do seu repositório no github, aperte **f5** e veja a mágica acontecer!
