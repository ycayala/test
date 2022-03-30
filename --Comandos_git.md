--Comandos git
--limpiar ventana de git bash CTRL + L
--***comandos utiles consola de git
--crear un archivo vacio
touch nombre_archivo.txt
--editar archivo en visual studio code
code nombre_archivo.txt

--***listar configuracion disponibles para git
git config
--listar configurarciones predeterminadas
git config --list
--listar la ubicacion de los archivos de configuracion 
git config --list --show-origin 
--configurar usuario en git
git config --global user.name "ycayala"
--configurar email en git
git config --global user.email "camargo.ayala@gmail.com"

-- crear repositario en git
git init
-- estado de los repositorios
git status
-- agregar archivos a repositorio de git
git add .
-- agregar solo un archivo a repositorio de git
git add nombre_archivo.txt  
-- remover archivos de repositario
git rm nombre_archivo
-- remover archivos de cache
git rm --cached nombre_archivo
-- confirmar cambios
git commit -m "primer commit en git"
-- editar un archivo con vsCode
code nombre_archivo.txt
-- ver el historial de cambios realizados
git log
-- ver el historial de cambios de un archivo puntual
git show nombre_archivo.txt
--historial de cambios realizados en un archivo
git log archivo.txt
-- mostrar cambios
git diff
-- comparar cambios de dos commit(el codigo de commit se saca con el anterior archivo)
git diff codigo_commit_1 codigo_commit_2
-- volver a version anterior
git reset codigo_commit --hard
-- volver a version anterior sin perder cambios actuales
git reset codigo_commit --soft
-- revisar version especifica
git checkout codigo_commit nombre_archivo.txt
-- volver a version de master
git checkout master nombre_archivo.txt
--crear una nueva rama
git branch nombre_rama
-- cambiar de rama
git checkout nombre_rama
-- fusionar cambios de ramas (importante los merge siempre se recomiendan en la master como version final)
git merge nombre_rama -m "comentario de cambio"
-- listar nombres de ramas creadas 
git branch
-- realizar add y commit al tiempo a archivos sincronizados
git commit -am "comentario"
-- agregar un origen remoto
git remote add origin nombre_link
-- muestra los origin indexados
git remote -v
-- subir cambios a github 
git push origin master
-- bajar cambios de github rama master
git pull origin master
-- fusionar cambios de rama master local con rama remota master 
git pull origin master --allow-unrelated-histories
-- cambiar url de directorio remoto
git remote set-url origin nuevo_link
-- crear un alias en linux
alias ramas="git log --all --graph --decorate --oneline"
-- crear un tac para versionamiento
git tac -a nombre_de_tag -m "primera version de software" codigo_cabecera
-- ver todos los tag creados
git tac
-- ver en a que cabecera estan apuntando los tags
git show-ref --tags
-- subir cambios de un tag
git push origin --tags
-- eliminar un tag
git tac -d nombre_tag
-- borrar tac de repos
git push origin :refs/tags/nombre_tag
-- descripcion de ramas
git show-branch --all
-- enviar ramas creadas en local a remoto
git push origin development
-- crear una nueva fuente remota upstream 
git remote add <nombre_del_remoto> <url_del_remoto> 



--Generar una nueva llave SSH: (Cualquier sistema operativo)
ssh-keygen -t rsa -b 4096 -C "youremail@example.com"

--Comprobar proceso y agregarlo (Windows)
eval $(ssh-agent - s)
ssh-add ~/.ssh/id_rsa

--ignorar archivos de repositorios(generalmente binarios, es decir archivos que nos son planos) 
-- se crea un archivo .gitignore y dentro se ponen las carpesa con /<nombre_carpeta> y archivos. (comodin es *)



