# PRIMEIROS COMANDOS

```bash
git init // inicializar git
git init --initial-branch=main // define qual vai ser a branch inicial
git status // fazer varredura e verificar atualizações feitas
git add nome_arquivo // adiciona arquivo
git add -A // adiciona todos os arquivos que não estão no git
git add . // adiciona todos os arquivos que não estão no git
git commit -m "comentário" // comentário para o push
git commit -am "comentário" // faz o commit para todos os arquivos
git remote // verifica repositório configurado
git remote -v // mais info do repositório configurado 
git remote add origin link_repo // adiciona repositório remoto
git remote rm origin // remove git remoto
git push -u origin nome_branch // empurra para a branch nome_branch -u é um atalho para "--set-upstream", com ele, salvamos a relação entre branch local e remoto
git push orign nome_branch // especifica a branch para empurrar
```


# CONFIG

```bash
git config --global user.name "usuário" // usuário global
git config --global user.email "e-mail" // e-mail global
git config user.name "usuário" // configura usuário para o repo
git config user.email "e-mail" // configura e-mail para o repo
git config user.name // verificar usuário sendo utilizado
git config user.email // verificar e-mail sendo utilizado
git config --system core.edito "editor de texto" // configura o editor de texto a ser utilizado pelo Git
git config -l // verificar dados gerais de info
git config -l --show-origin // lista os arquivos onde estão armazenadas as config
git config --global -edit // editar configurações globais
git config --local -edit // editar configurações locais
git config --system -edit // editar configurações do sistema git
git config --global -l // lista configurações globais
git config --local -l // lista configurações locais
git config --system --l // lista configurações do sistema git
git config --alias.c "commit -am" // cria um alias "c" para o comando "commit -am"
git config --system color.ui true // ativa coloração no git
```


# LOGS

```bash
git log // verifica o que foi commitado e qual branch está
git log -1 // último log
git log --oneline // menos detalhes
git log -p // mais detalhes
git log --raw // modificações de arquivo sem formatação visual
git log --pretty=full // nome do autor, e-mail e commits detalhados
git log --pretty=short // nome do autor e commits curtos
git log --graph // representação gráfica em árvore no log
git log -- arquivo // histórico de commits de um arquivo específico
git log --stat // número de linhas adicionadas/removidas
git log --author=autor // filtra e mostra commits feitos por autor específico
```


# BRANCH

```bash
git branch // lista as branches
git branch -m master main // renomeia a branch
git branch -M nome_branch // força a criação da branch
git symbolic-ref refs/remotes/origin/HEAD refs/remotes/origin/main // redireciona o apontamento para a nova branch local
git branch -a // lista todas as branches (local e remota)
git checkout -b nome_branch // cria branch local
git chechout nome_branch // altera para a branch nome_branch
git branch -D nome_branch // força o delete da branch local
git push -d origin nome_branch // remove a branch remota nome_branch
```


# MERGE

```bash
git merge nome_branch // vai mergear a branch que você está com a nome_branch
```


# RESET E REVERT

```bash
git reset arquivo // retira o arquivo que foi adicionado ao git
git reset // remove todos os arquivos do git no commit atual
git reset --hard // volta para o último commit apagando os mais novos
git reset --soft <commit> // volta 1 commit e prepara para commitar/mais indicado para trabalho de equipe
git reset --mix <commit> // volta 1 commit e precisa fazer add commit
git commit -amend // altera a mensagem do commit
git revert <commit> // revertendo para outro commit
git clean -n // verifica os arquivos que não estão no git
git clean -f // remove os arquivos que não estão no git
```


# DIFF

```bash
git diff HEAD // ver diferença para o último commit
git diff --cached // compara o que você tem com o que está adicionado ao git
git diff commit commit // compara as diferenças entre os commit
git diff branch branch // diferença entre as branches
git diff arquivo // verifica alterações feitas em arquivo específico
git diff // verifica alterações feitas em tudo
git diff --name-only // mostra somente o nome dos arquivos alterados
```


# USO GERAL

```bash
git restore --staged // restaurar encenada
git checkout branch_atual --arquivo // quando desiste em cima da hora de fazer alteração e deseja fazer alteração de apenas um arquivo.
git rm --cached // remove os arquivos commitados que não foram enviados para o repo remoto
git rm nome_arquivo // remove nome_arquivo do git
```
