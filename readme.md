# olá, esse projeto serve para listar alguns comandos do git

## como criar um projeto no github

1. instale git  
2. instale vscode  
3. faça uma conta no github  
4. crie um repositório no github (não marque nenhuma caixinha durante a criação)  
5. copie o link https que foi gerado (exemplo):  
   `https://github.com/seu-usuario/nome-do-repositorio.git`  
6. crie uma pasta no seu computador  
7. abra a pasta com o vscode  
8. no vscode, crie um novo arquivo `.md` (exemplo): `readme.md`  
9. dentro do arquivo, escreva alguma mensagem  
10. salve o arquivo (ctrl + s)  
11. abra o git bash  
12. digite `git --version` e verifique se o git está instalado  
13. no terminal do git bash, use o comando `cd` + o local da sua pasta (exemplo):  
    ```bash
    cd desktop/code/git
    ```  
14. inicialize o git na pasta:  
    ```bash
    git init
    ```  
15. adicione os arquivos ao staging:  
    ```bash
    git add .
    ```  
16. faça o primeiro commit:  
    ```bash
    git commit -m "primeiro commit"
    ```  
17. conecte o repositório local ao remoto:  
    ```bash
    git remote add origin https://github.com/seu-usuario/nome-do-repositorio.git
    ```  
18. defina a branch principal como main:  
    ```bash
    git branch -M main
    ```  
19. envie os arquivos para o github:  
    ```bash
    git push -u origin main
    ```
20. abra a página do seu repositório no github, aperte **F5** e veja a mágica acontecer!  