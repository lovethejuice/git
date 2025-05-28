olá, esse projeto serve para aplicar e listar alguns comandos do git.

# projeto no github:

- instale git  
- instale vscode  
- faça uma conta no github  

- crie um repositório no github (não marque nenhuma caixinha durante a criação) 
- copie o link https que foi gerado (exemplo): `https://github.com/seu-usuario/nome-do-repositorio.git`  

- crie uma pasta no seu computador  
- abra a pasta com o vscode

- no vscode, crie um novo arquivo `.md` (exemplo): `readme.md`
- dentro do arquivo, escreva alguma mensaguem
- salve o arquivo (ctrl + s) 

- abra o git bash
- digite `git --version` e verifique se o git está instalado
- no terminal do git bash, use o comando `cd` + o local da sua pasta (exemplo): `cd desktop/code/git`

obs: foi criado um repositório no github e um arquivo local no computador, nos proximos passos o arquivo local será integrado ao repositório do github.

- git init
- git add .
- git commit -m `primeiro commit`
- git remote add origin `https://github.com/seu-usuario/nome-do-repositorio.git`
- git branch -M main
- git push -u origin main