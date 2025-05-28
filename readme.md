# olá, esse projeto serve para listar alguns comandos do git

## como criar um projeto no github

### primeiros passos

- instale o git  
- instale o vs code  
- faça uma conta no github
 
### criando repositório no github e o arquivo local (projeto)   

- crie um repositório no github (não marque nenhuma caixinha durante a criação)  
- copie o link https que foi gerado (exemplo): `https://github.com/seu-usuario/nome-do-repositorio.git`  
- crie uma pasta no seu computador   
- abra essa pasta com o vscode  
- dentro do vscode, crie um novo arquivo `.md` (exemplo: `readme.md`)  
- dentro do arquivo .md, escreva alguma mensagem (exemplo: testando git e github) 
- salve o arquivo (no vscode)

### sincronizando o arquivo local (projeto) no repositório github

- abra o git bash e digite os seguintes comandos:
- cd localdo/aquivo/
- git init
- git config --global user.email "seuemail@exemplo.com"
- git config --global user.name "Seu Nome"
- git add .
- git commit -m "primeiro commit"
- git remote add origin https://github.com/seu-usuario/nome-do-repositorio.git
- git branch -M main
- git push -u origin main
- abra a página do seu repositório no github, aperte **f5** e veja a mágica acontecer!

### modificando o arquivo e fazendo o segundo commit

- crie um arquivo novo ou edite um arquivo existente
- salve o arquivo (no vscode)
- git add .
- git commit -m "segundo commit"
- git push 
