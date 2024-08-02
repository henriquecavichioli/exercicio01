# exercicio01

a) No working dir, executar:
Comando: echo 01 > arquivo.txt
Saída: Cria um arquivo .txt com nome "arquivo" escrito "01".

b) Adicionar o arquivo no staging e conferir o status:
Comandos: git add arquivo.txt / git status
Saída: On branch main

No commits yet

Changes to be committed:
  (use "git rm --cached <file>..." to unstage)
        new file:   arquivo.txt

c) Commitar o arquivo do staging com a descrição "git add example - arquivo.txt“:
Comando: git commit -m "git add example - arquivo.txt"
Saída: [main (root-commit) 116b476] gid add example - arquivo.txt
 1 file changed, 1 insertion(+)
 create mode 100644 arquivo.txt

d) Sobrescrever o conteúdo do arquivo.txt:
Comando: echo 02 > arquivo.txt
Saída: arquivo.txt é sobrescrito com "02"

e) Verificar o diffing no arquivo:
Comando: git diff
Saída: diff --git a/arquivo.txt b/arquivo.txt
index 8a0f05e..9e22bcb 100644
--- a/arquivo.txt
+++ b/arquivo.txt
@@ -1 +1 @@
-01
+02

f) Adicionar novamente o arquivo no staging e conferir o status:
Comandos: git add arquivo.txt / git status
Saída: On branch main
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        modified:   arquivo.txt

g) Verificar o diffing no arquivo:
Comando: git diff
Saída: (em branco)

h) Sobrescrever o conteúdo do arquivo.txt:
Comando: echo 03 > arquivo.txt
Saída: arquivo.txt é sobrescrito com "03"

i) Verificar o diffing no arquivo:
Comando: git diff
Saída: diff --git a/arquivo.txt b/arquivo.txt
index 9e22bcb..75016ea 100644
--- a/arquivo.txt
+++ b/arquivo.txt
@@ -1 +1 @@
-02
+03

j) Fazer o restore do arquivo da área de staging e verificar o status:
Comandos: git restore --staged arquivo.txt / git status
Saída: On branch main
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   arquivo.txt

no changes added to commit (use "git add" and/or "git commit -a")

k) Realizar o commit do arquivo e verificar o log:
Comandos: git add / git commit -m "segundo commit" / git log
Saída 1: [main 21df146] segundo commit
 1 file changed, 1 insertion(+), 1 deletion(-)
 
 Saída 2: commit 21df146bd448b191dc218fb9248c9045386b3468 (HEAD -> main)
Author: henriquecavichioli <henriqueemann@gmail.com>
Date:   Fri Aug 2 01:57:08 2024 +0000

    segundo commit

commit 116b476bcb650bd163f6dfbbb72dc7986a8c56e7
Author: henriquecavichioli <henriqueemann@gmail.com>
Date:   Fri Aug 2 01:47:14 2024 +0000

    gid add example - arquivo.txt

l) Adicionar um arquivo gitignore com o seguinte conteúdo:
*.txt:
Comandos: echo *.txt > .gitignore
Saída: Cria um arquivo .gitignore com nome ".gitignore" escrito "*.txt".

m) Criar um arquivo novo.txt e verificar o status:
Comandos: echo > novo.txt / git status
Saída 1: Cria um arquivo .txt com nome "novo" em branco.
Saída 2: On branch main
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        .gitignore

nothing added to commit but untracked files present (use "git add" to track)
