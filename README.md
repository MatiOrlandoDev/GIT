push //Pasa a un repo de github
pull //Toma ese archivo

git --version //Saber que version tenemos
git --help //For commands 

ctrl + l //Hace un clear

Configurar GIT
git config (Enter) //Muestra opciones
git config --global user.name "Matu"
git config --global user.email "Matiorlando96@gmail.com
git config --global color.ui auto

git config -l //Nos muestra la configuracion que tenemos

mkdir (Create a new folder)
cd + name of the folder(it makes that we are now working into that folder)

Tenemos que incializar nuestro repositorio
git init .	//Lo hacemos con este comando	//Solo para nuevos proyectos
ahora podemos comenzar a hacer commits, adds, etc

Con touch + nombre del archivo que deseemos .js .css .java .html // we create a new file

git status give us the status of the changes that we have made

git add index.html //Esta funcion agregaria index.html para ser commiteada

git rm --cached index.html //Remueve la fila para ser commiteada
git rm -r --cached . //Removes all from the staging area

git add . // . means, add all the files from this current directory downwards

(Si me encuentro en una carpeta y uso git add . solo me va a pasar a la etapa de commit
lo que este en esa carpeta, no todos los archivos que tenga en las carpetas de la 
carpeta principal)

para ello utilizamos
git add -A

---------------------------Commits------------------------------------
(cd ..) (returns to the root folder)
git commit -m "Mensaje que se quiera poner al hacer el commit //Realiza el commit de todo
//Para ver los cambios
git log // Nos mostrara los datos del commit, incluido el hash
git log --oneline //better
git show + hash //Nos muestra todo lo del commit

vi index.js //press i. //Escribimos console.log("Hello git");
luego esc :wq //modificamos la carpeta index.js
cat index.js //CAT para ver lo que hay 
(Si ahora hacemos un status nos muestra que se produjeron cambios en la carpeta)

git diff //Nos muestra la diferencia de lo que tenemos en la carpeta ya commiteada y lo que modificamos
/* Ahora seguiria git add .
git commit -m "Mensaje para que se lea"
con un git log (Nos mostraria 2 commits ahora)

//PARA DESCARTAR LOS CAMBIOS QUE HAYAMOS AGREGADO, ANTES DEL COMMIT
git restore index.js (nombre de la carpeta)

//LOS MENSAJES QUE COLOQUEMOS DEBEN DE SER SIGNIFICATIVOS (MEANINGFULL MENSAGES)
//Para cambiar un mensaje
git commit --amend -m "Mensaje nuevo"

git commit --amend -m 
//el -m para mensajes


---------------------GIT HUB---------------------------------------
git push (it takes a copy from your local machine and then stores in the remote server)

in GitHub => settings => SSH AND GPG keys
Congif ssh keys //Need to generate a public and private key
Follow the steps

THEN.
Push an existing repository from the command line
git remote add origin https://github.com/MatiOrlandoDev/learning-git.git
git branch -M main	//change branch //con git branch puedo ver
git push -u origin main

(Also for creating a new file vi (name of the file.go (ej))
luego git add .
luego git commit -m "Mensaje"
-Esto estara en nuestra maquina virtual y todavia no en el repo de gith-
Para ello utilizamos GIT PUSH

con GIT PULL traemos algo del repo a nuestra maquina virtual

(recordatorio: each commit is identify by the hash)

------------------BRANCHS----------------------------------
main branch or master branch ere equals (They are the default branches)

The best practices said that u have to create a new branch and 
then merge with the main branch

git branch //branches in our local machine
git branch -r //in remote 
git branch -a //ALL branches
git branch -d (name of the branch we want to delete //delete a branch

git branch feature-a //in order to create a new branch use proper naming(no special chars, no spaces)

to switch branches: 
git checkout feature-a (nombre)

with git checkout - (we witch back to the previus branch)

PARA PONER LA NUEVA BRANCH A GIT HUB
git push (copiar el codigo que nos de, || git push -u origin (nombre del branch))

git checkout -b to-delete // en este caso creamos una nueva branch llamada to-delete y la usamos automaticamente todo en un paso)

---------------------MERGE----------------------------------
to feature-a to main 
 
git merge feature-a // to directly merge with the main, never do that, we need do this throw pull request

merge throw pull request in gitHub

-------------------
Too work pull the lastests changes from master/main down to u local machine
then create a new branch
(rebase your changes agains master)

-------------------
Conflictos quiza este trabajando con alguien en el mismo repo de git hub
si ese alguien modifica un archivo del repositorio
y yo trabajo sobre ese repositorio desde mi maquina virtual no me voy a enterar
luego si trato de hacer un push, saldra error ya que me dira que
hay cambios que no tengo localmente 

-------------------
merge conflicts
(VS HELP US TO RESOLVE CONFLICTS MUCH FASTER)
<<<<<<<<<<<<head
son nuestros cambios


we have to fix this conflicts before we can merge

(IN THE VI we can exit with :q!)

-----------------------GIT REBASE----------------------------------

We want to take the latest changes from the main or master branch and then add our changes 
on top of it
we have to resolver all the conflicts 		//Esc :wq in the vi and then vs code

git pull -r origin main /master
git rebase --continue
after all the conflicts are resolved
we can do git push normally
we have to do git push -f //force the push

we the people merge to master or main branch if you have 3 commits for example on your 
pull request 
when you are ready to merge to the main what we do is squash all this commits into one
commit and then u merge that in to the main or master branch. That way we have to resolve
only once
its easy insteed of fixing all the conflicts 1 by 1 per commit


--------------------------GUI CLIENTS
Github desktop
Sourcetree

--------------------------GIT POD
vs code in the cloud



