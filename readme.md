Para crear un repositario vamos primero al Escritorio:  
cd Desktop  
Creamos la carpeta repo01:  
mkdir repo01  
Inicializamos un repositorio Git vacio en repo01:  
git init repo01  
Entramos en el repositorio:  
cd repo01  
Comprobamos que se ha realizado correctamente:  
git status  
Creamos un archivo readme.md  
Mandamos el fichero al staging area:  
git add readme.md  
Hacemos una snapshot (Commit) del fichero al repositorio local:  
git commit -m "Creo el fichero.md"  
El fichero se encuentra como Commited dentro del "File Status Lifecycle"  
Intentamos hacer un "git push" pero no funciona.  
Tampoco aparece nada si realizamos un "git remote -v", porque no tenemos un repositorio remoto vinculado  
Creamos un repositorio remoto y lo vinculamos con el local:  
git remote add origin https://github.com/RogerPuig1997/repo01.git  
Como ya esta vinculado ahora al realizar "git remote -v" aparecen como origin los inks de GitHub del repositorio remoto.  
Cambiamos la rama master a main  
git branch -M main  
Y hacemos un push en la rama main  
git push -u origin main  
Vamos al repositorio remoto y vemos que el fichero readme.md se ha subido