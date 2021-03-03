### Primeiros passos
 - Fazer o fork
 - git clone do seu repositório
```bash
git remote add upstream <Link do repositório original (forked)
```

### Atualizar upstream
```bash
git fetch upstream
git rebase upstream/master
```
 - Fazer isso na pasta raíz do projeto (jovens-talentos)

### Para fazer alterações
 - Criar uma nova branch:
```bash
git checkout -b tema-x
```
 - Fazer as alterações necessárias nos arquivos
 - Adicionar os arquivos:
```bash
git add .
```
 - Para conferir se os arquivos corretos foram adicionados:
```bash
git status
```
 - Mandar as alterações:
```bash
git commit -m "Tema X"
git push origin master
git push 
git push git push --set-upstream origin tema-x
```
 - Fazer PR no github
 ```bash
git checkout master   
git fetch upstream 
git merge tema-x
```

### Se o PR precisar de alterações
 - No mesmo branch em que foi mandado o  PR
 - Fazer as alterações
 - Conferir se as alterações foram identificadas
 ```bash
git status
```
 - Adicionar as alterações
```bash
git add .
git commit -m "mensagem"
git push origin <nome da branch> 
``` 
 - Exemplo <nome da branch> = tema-x
 - Feito isso, as alterações irão aparecer no seu PR

## Se o PR for aceito
 - Sair da branch atual para a master
```bash
git checkout master
git pull upstream master
git push origin master
```

### Como enviar um novo tema
 - Sair da branch do tema anterior
```bash
git checkout master
git fetch upstream
git rebase upstream/master
git push origin master
```
 - Criar uma nova branch
```bash
git checkout -b tema-y
```
 - Faz o novo tema e quando terminar, volta para o passo de alterações
 - Quando terminar, dar um pull request no github
