# olá, esse projeto serve para listar alguns comandos do git

## como criar um projeto no github:

### primeiros passos

- instale o git  
- instale o vs code  
- faça uma conta no github
 
### criando o repositório no github e o arquivo local (projeto)   

- crie um repositório no github (não marque nenhuma caixinha durante a criação)  
- copie o link https que foi gerado (exemplo): `https://github.com/seu-usuario/nome-do-repositorio.git`  
- crie uma pasta no seu computador   
- abra essa pasta com o vscode  
- dentro do vscode, crie um novo arquivo (exemplo: `readme.md`)  
- dentro do arquivo, escreva alguma mensagem (exemplo: testando git e github) 
- salve o arquivo (no vscode)

### sincronizando o arquivo local (projeto) com o repositório github

- abra o git bash e digite os seguintes comandos:
- cd exemplo/localdo/arquivo/
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
 
## lista de comandos git:

### 1. Inicialização, configuração de repositórios, staging e commit:

| comando                                                              | função                                                                                    |
| -------------------------------------------------------------------- | ----------------------------------------------------------------------------------------- |
| git init                                                             | cria um novo repositório git vazio no diretório atual                                     |
| git init --bare                                                      | cria um repositório sem área de trabalho (usado como servidor remoto)                     |
| git clone <url>                                                      | copia um repositório remoto existente para sua máquina                                    |
| git config --global user.name seu nome                               | define seu nome de usuário para todos os repositórios no sistema                          |
| git config --global user.email "seu@email.com"                       | define seu e-mail de usuário para todos os repositórios                                   |
| git config user.name seu nome                                        | define seu nome apenas para o repositório atual                                           |
| git config user.email "seu@email.com"                                | define seu e-mail apenas para o repositório atual                                         |
| git config --list                                                    | mostra todas as configurações definidas (globais e locais)                                |
| git remote add <nome> <url>                                          | adiciona um novo repositório remoto com um nome específico (ex: origin)                   |
| git remote remove <nome>                                             | remove um repositório remoto já configurado                                               |
| git remote set-url origin <nova-url>                                 | altera a url associada a um repositório remoto                                            |
| git add <arquivo>                                                    | adiciona um arquivo específico à área de preparação (staging)                             |
| git add .                                                            | adiciona todos os arquivos modificados e novos à área de preparação                       |
| git add -a                                                           | adiciona todos os arquivos modificados, novos e removidos à área de preparação            |
| git add -u                                                           | adiciona apenas arquivos modificados ou deletados (não inclui arquivos novos)             |
| git add -p                                                           | permite escolher partes (trechos) específicos de arquivos para adicionar ao commit        |
| git commit -m mensagem                                               | salva as alterações preparadas com uma mensagem descritiva                                |
| git commit -a -m mensagem                                            | adiciona e comita automaticamente todos os arquivos rastreados (modificados ou deletados) |
| git commit --amend                                                   | altera o último commit, substituindo o conteúdo e/ou a mensagem                           |
| git commit --amend --no-edit                                         | regrava o último commit sem mudar a mensagem                                              |
| git reset <arquivo>                                                  | remove o arquivo da área de staging, mantendo as alterações no arquivo                    |
| git reset --soft head\~1                                             | desfaz o último commit e move as mudanças de volta para o staging                         |
| git reset --mixed head\~1                                            | desfaz o commit e remove do staging, mas mantém as alterações no diretório                |
| git reset --hard head\~1                                             | desfaz o commit, o staging e também apaga as mudanças locais (destrutivo)                 |
| git clean -fd                                                        | remove arquivos e diretórios não rastreados (não versionados) do projeto                  |


### 2. branches e controle de versões

| comando                | função                                                               |
| ---------------------- | -------------------------------------------------------------------- |
| git branch             | mostra todas as branches locais                                      |
| git branch <nome>      | cria uma nova branch com o nome especificado                         |
| git branch -d <nome>   | apaga a branch se ela já foi mesclada                                |
| git branch -D <nome>   | apaga a branch mesmo que não tenha sido mesclada (força)             |
| git checkout <nome>    | muda para a branch especificada                                      |
| git checkout -b <nome> | cria uma nova branch e já muda para ela                              |
| git switch <nome>      | troca de branch (forma moderna de usar checkout)                     |
| git switch -c <nome>   | cria uma nova branch e já muda para ela                              |
| git merge <branch>     | une a branch especificada à branch atual                             |
| git rebase <branch>    | reaplica os commits da branch atual sobre outra base                 |
| git cherry-pick <hash> | aplica um commit específico (identificado pelo hash) na branch atual |

### 3. histórico, comparação e visualização

| comando               | função                                                                                             |
| --------------------- | -------------------------------------------------------------------------------------------------- |
| git status            | mostra os arquivos modificados, adicionados e não versionados                                      |
| git log               | exibe o histórico completo de commits do repositório                                               |
| git log --oneline     | exibe o histórico de commits de forma resumida (um por linha)                                      |
| git log --graph --all | mostra o histórico com representação gráfica de branches e merges                                  |
| git show <hash>       | exibe os detalhes de um commit específico (mensagem, autor, alterações)                            |
| git diff              | mostra as diferenças entre o diretório de trabalho e o último commit                               |
| git diff --staged     | mostra as diferenças entre a área de staging e o último commit                                     |
| git blame <arquivo>   | mostra quem fez cada modificação linha por linha em um arquivo                                     |
| git reflog            | mostra o histórico de movimentações de ponteiros (como head), útil para recuperar commits perdidos |


### 4. repositórios remotos e colaboração

| comando                               | função                                                                 |
| ------------------------------------- | ---------------------------------------------------------------------- |
| git remote -v                         | lista todos os repositórios remotos configurados                       |
| git fetch                             | busca alterações do repositório remoto sem aplicar                     |
| git pull                              | busca e aplica (merge) as alterações remotas na branch atual           |
| git pull --rebase                     | busca as alterações e as reaplica no topo da branch remota             |
| git push                              | envia os commits da branch atual para o repositório remoto             |
| git push -u origin <branch>           | envia a branch e define o upstream para facilitar os próximos pushes   |
| git push --force                      | força o envio mesmo que ele sobrescreva alterações remotas (perigoso)  |
| git fetch origin pull/id/head\:branch | baixa uma pull request específica do github como uma nova branch local |

### 5. depuração, correção e ferramentas avançadas

| comando           | função                                                                         |
| ----------------- | ------------------------------------------------------------------------------ |
| git stash         | guarda temporariamente mudanças não comitadas para limpar a árvore de trabalho |
| git stash pop     | recupera a última alteração guardada com stash e a remove da lista             |
| git stash list    | exibe todas as alterações guardadas com stash                                  |
| git revert <hash> | cria um novo commit que desfaz um commit anterior sem apagar o histórico       |
| git bisect        | ajuda a encontrar o commit que introduziu um bug usando busca binária          |
| git tag <nome>    | cria uma marca (tag) no commit atual, normalmente para marcar versões          |
| git tag -d <nome> | apaga uma tag localmente                                                       |
| git archive       | gera um arquivo compactado com o conteúdo do projeto                           |
| git gc            | realiza tarefas de limpeza e otimização do repositório                         |
| git fsck          | verifica a integridade dos objetos no repositório                              |
| git prune         | remove objetos órfãos do banco de dados (perigoso se usado incorretamente)     |
