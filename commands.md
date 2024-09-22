# PRIMEIROS COMANDOS

```bash
git init // inicializar git
git add nome_arquivo // adiciona arquivo
git commit -m "comentário" // comentário para o push
git branch -M nome_branch // cria branch
git remote add origin link_repo // adiciona repositório remoto
git push -u origin nome_branch // empurra para a branch nome_branch -u é um atalho para "--set-upstream", com ele, salvamos a relação entre branch local e remoto
git push orign nome_branch // especifica a branch para empurrar
```


# CONFIGURAÇÃO

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


# USO GERAL

```bash
git status // fazer varredura e verificar atualizações feitas
git add -A // adiciona todos os arquivos que não estão no git
git commit -am "comentário" // faz o commit para todos os arquivos
git branch // pra listar todos os branchs
git reset [soft] numero serie commit // volta 1 commit e prepara para commitar/mais indicado para trabalho de equipe
git reset [mix] numero serie commit // volta 1 commit e precisa fazer add commit
git reset [hard] numero serie commit // apaga o commit
git checkout [nome do branch] // alterar o branch de utilização
git restore --staged // restaurar encenada
git diff // verificar alterações realizadas de todos os arquivos
git diff [nome_do_arquivo] // verificar alterações realizadas de arquivos especificos
git diff --name-only // verificar quais arquivos foram alterados
git checkout branch_atual --arquivo // quando desiste em cima da hora de fazer alteração e deseja fazer alteração de apenas um arquivo.
git branch -D nome_do_branch // deletar o branch
git remote rm // remover git remoto
```


|Transferir para o gitHub|

|1| git remote add origin |link do repositorio git| // Adicionar o repositorio remoto.
|2| git remote // verificar se há o servidor remoto adicionado.
|3| git push -u origin master // empurrar para o github
|4| git revert --no-edit [imei do log] // desfaz alterações, porem mantem as mesmas para verificar o que fez de errado
|5| git push -u origin :[nome_do_branch]  // para deletar branch do github
