# Ejercicio práctico sobre la utilización básica de Git, GitHub y Markdown

+ Alumno: Héctor Soto Cadavid
+ Fecha: 21/05/2016

## Repositorio campusciff

1. Crear un repositorio en vuestro GitHub llamado campusciff.

![](\Users\Marina\Desktop\pantallazos\pantallazo0.png)
 


2. Clonar vuestro repositorio en local.

		$ git clone git@github.com:hefaso/campusciff.git
		Cloning into 'campusciff'...
		Warning: Permanently added the RSA host key for IP address 	'192.30.252.128' to the list of known hosts.
		warning: You appear to have cloned an empty repository.
		Checking connectivity... done.
    
## README

1. Crear (si no lo habéis creado ya) en vuestro repositorio local un documento README.md.

		$ touch > README.md
		touch: missing file operand
		Try 'touch --help' for more information.


## Commit inicial

1. Añadir al README.md los comandos utilizados hasta ahora y hacer un commit inicial con el mensaje commit inicial.

		$ git add README.md
		$ git commit -m "Commit inicial"
		[master (root-commit) 2a47dfe] Commit inicial
 		1 file changed, 0 insertions(+), 0 deletions(-)
 		create mode 100644 README.md


## Push inicial

1. Subir los cambios al repositorio remoto.

		$ git push origin master
		Warning: Permanently added the RSA host key for IP address 	'192.30.252.131' to the list of known hosts.
		Counting objects: 3, done.
		Writing objects: 100% (3/3), 220 bytes | 0 bytes/s, done.
		Total 3 (delta 0), reused 0 (delta 0)
		To git@github.com:hefaso/campusciff.git
 		* [new branch]      master -> master


## Ignorar archivos

1. Crear en el repositorio local un fichero llamado privado.txt.

		$ touch privado.txt
	

2. Crear en el repositorio local una carpeta llamada privada.

		$ mkdir privada

3. Realizar los cambios oportunos para que tanto el archivo como la carpeta sean ignorados por git.

		$ echo "privado.txt" > .gitignore
		$ echo "privada" >> .gitignore
		$ cat .gitignore
		privado.txt
		privada
		
 ## Añadir fichero 1.txt

1. Añadir fichero 1.txt al repositorio local.

		$ touch 1.txt
		$ git add 1.txt
		$ git commit -m "commit 1.txt"
		[master eda84c9] commit 1.txt
 		1 file changed, 0 insertions(+), 0 deletions(-)
 		create mode 100644 1.txt


## Crear el tag v0.1

1. Crear un tag v0.1.

		$ git tag V0.1
		$ git status
		On branch master
		Your branch is ahead of 'origin/master' by 1 commit.
  		(use "git push" to publish your local commits)
		Untracked files:
  		(use "git add <file>..." to include in what will be committed)

        .gitignore

		nothing added to commit but untracked files present (use "git add" to 	track)


## Subir el tag v0.1

1. Subir los cambios al repositorio remoto.
	
		$ git push origin master
		Warning: Permanently added the RSA host key for IP address 	'192.30.252.120' to the list of known hosts.
		Counting objects: 2, done.
		Delta compression using up to 4 threads.
		Compressing objects: 100% (2/2), done.
		Writing objects: 100% (2/2), 248 bytes | 0 bytes/s, done.
		Total 2 (delta 0), reused 0 (delta 0)
		To git@github.com:hefaso/campusciff.git
   		2a47dfe..eda84c9  master -> master


## Cuenta de GitHub

1. Poner una foto en vuestro perfil de GitHub.

![](\Users\Marina\Desktop\pantallazos\pantallazo1.png)

2. Poner el doble factor de autentificación en vuestra cuenta de GitHub.

![](\Users\Marina\Desktop\pantallazos\pantallazo3.png)

3. Añadir (si no lo habéis hecho ya) la clave pública que se corresponde a tu ordenador.

![](\Users\Marina\Desktop\pantallazos\pantallazo4.png)

## Uso social de GitHub

1. Preguntar los nombres de usuario de GitHub de tus compañeros de clase, búscalos, y sigueles.

2. Seguir los repositorios campusciff del resto de tus compañeros.

![](\Users\Marina\Desktop\pantallazos\pantallazo5.png)

3. Añadir una estrella a los repositorios campusciff del resto de tus compañeros.

![](\Users\Marina\Desktop\pantallazos\pantallazo6.png)

## Crear una tabla

1. Crear una tabla de este estilo en el fichero README.md con la información de varios de tus compañeros de clase:


| NOMBRE | 		GITHUB |
| ------ | -----:	 |
| Araceli| https://github.com/araceliMacia  |
|Anna    |https://github.com/annalawrenc  |
|Enrique |https://github.com/eserranom |

## Colaboradores

1. Poner a github.com/asanzdiego como colaborador del repositorio campusciff

![](\Users\Marina\Desktop\pantallazos\pantallazo7.png)


# Ejercicio práctico sobre la utilización avanzada de Git, GitHub y Markdown

## Crear una rama v0.2

1. Crear una rama v0.2.

		$ git branch V0.2
        
2. Posiciona tu carpeta de trabajo en esta rama.


    	$ git checkout v0.2
        
## Añadir fichero 2.txt

1. Añadir un fichero 2.txt en la rama v0.2.

    	$ touch 2.txt
        
## Crear rama remota v0.2

1. Subir los cambios al reposiorio remoto.

		$ git add -A
        $ git commit -m "2.txt incluida en la rama V0.2"
		[V0.2 d5ee4d6] 2.txt incluida en la rama V0.2
 		2 files changed, 1 insertion(+)
 		create mode 100644 2.txt

		$ git push --set-upstream origin V0.2

   
## Merge directo

1. Posicionarse en la rama master.

   		$ git checkout master
        
2. Hacer un merge de la rama v0.2 en la rama master.

		$ git merge V0.2 -m "Se realiza un merge en la rama master"
		Updating 4e8d823..d5ee4d6
		Fast-forward (no commit created; -m option ignored)
 		2.txt        | 0
 		README.md.md | 1 +
 		2 files changed, 1 insertion(+)
 		create mode 100644 2.txt
  
## Merge con conflicto

1. En la rama master poner Hola en el fichero 1.txt y hacer commit.

		$ echo "Hola" >> 1.txt
		$ git add -A
		warning: LF will be replaced by CRLF in 1.txt.
		The file will have its original line endings in your working directory.

		$ git commit -m "Se añade Hola a fichero 1.txt"
		[master warning: LF will be replaced by CRLF in 1.txt.
		The file will have its original line endings in your working directory.
		1feb4c5] Se añade Hola a fichero 1.txt
		warning: LF will be replaced by CRLF in 1.txt.
		The file will have its original line endings in your working directory.
 		1 file changed, 1 insertion(+)

   
2. Posicionarse en la rama v0.2 y poner Adios en el fichero "1.txt" y hacer commit.

		$ git checkout V0.2
		Switched to branch 'V0.2'
		$ echo "Adios" >> 1.txt
		$ git add -A
		warning: LF will be replaced by CRLF in 1.txt.
		The file will have its original line endings in your working directory.
		$ git commit -m "Se añade Adios en rama V0.2 en fichero 1.txt"
		[V0.2 warning: LF will be replaced by CRLF in 1.txt.
		The file will have its original line endings in your working directory.
		9b78440] Se añade Adios en rama V0.2 en fichero 1.txt
		warning: LF will be replaced by CRLF in 1.txt.
		The file will have its original line endings in your working directory.
 		1 file changed, 1 insertion(+)


3. Posicionarse de nuevo en la rama master y hacer un merge con la rama v0.2

		$ git checkout master
		Switched to branch 'master'
		Your branch is ahead of 'origin/master' by 2 commits.
  		(use "git push" to publish your local commits)
		$ git merge V0.2 -m "Se realiza un merge en la rama master desde V0.2"
		Auto-merging 1.txt
		CONFLICT (content): Merge conflict in 1.txt
		Automatic merge failed; fix conflicts and then commit the result.
		$ git status
		On branch master
		Your branch is ahead of 'origin/master' by 2 commits.
  		(use "git push" to publish your local commits)
		You have unmerged paths.
  		(fix conflicts and run "git commit")
		Unmerged paths:
  		(use "git add <file>..." to mark resolution)
        both modified:   1.txt
		no changes added to commit (use "git add" and/or "git commit -a")

## Listado de ramas

1. Listar las ramas con merge y las ramas sin merge.

		$ git branch --merged
		* master
		$ git branch --no-merged
  		V0.2

## Arreglar conflicto

1. Arreglar el conflicto anterior y hacer un commit.

		$ git add -A
		$ git commit -m "Cambios corregidos en 1.txt"
		[master d40345d] Cambios corregidos en 1.txt


## Borrar rama
1. Crear un tag v0.2

		$ git tag V0.2 -m "Se crea un tag para V0.2"



2. Borrar la rama v0.2

		$ git branch -d V0.2
        Deleted branch V0.2 (was 9b78440).

## Listado de cambios

1. Listar los distintos commits con sus ramas y sus tags.

		$ git list
		*   d40345d (HEAD -> master, tag: V0.2) Cambios corregidos en 1.txt
		|\
		| * 9b78440 Se añade Adios en rama V0.2 en fichero 1.txt
		* | 1feb4c5 Se añade Hola a fichero 1.txt
		|/
		* d5ee4d6 (origin/V0.2) 2.txt incluida en la rama V0.2
		* 4e8d823 (origin/master) Otro cambio
		* 9feb4cd Cambios a readme.md
		* 1e1edf8 Añadido .gitignore
		* eda84c9 (tag: V0.1) commit 1.txt
		* 2a47dfe Commit inicial


## Crear una organización

1. Crear una organización llamada campusciff-tunombredeusuariodegithub

Organización creada: campusciff-hefasoca

## Crear equipos

1. Crear 2 equipos en la organización campusciff-tunombredeusuariodegithub, uno
llamado administradores con más permisos y otro colaboradores con menos permisos.

Se han creado dos equipos: Administradores y Colaboradores.

2. Meter a github.com/asanzdiego y a 2 de vuestros compañeros de clase en el equipo
administradores.

Añadidos compañeros de clase:

+ eserranom
+ annalawrenc

Añadido profesor:
+ asanzdiego
3. Meter a github.com/asanzdiego y a otros 2 de vuestros compañeros de clase en el equipo
colaboradores.

Añadidos compañeros de clase:

+ amarino
+ juangarciaciff

Añadido profesor:
+ asanzdiego


## Crear un index.html

1. Crear un index.html que se pueda ver como página web en la organización.

Se ha creado el siguiente index: https://github.com/campusciff-hefasoca/github.io

## Crear Pull-requests

1. Hacer 2 forks de 2 repositorios campusciff-tunombredeusuariodegithub.github.io de 2
organizaciones de las que no seais ni administradiores ni colaboradores.
Se ha realizado un pull-request en amarino5 y juangarciaciff

2. Crearos una rama en cada fork.

Se ha creado una rama en cada fork: ramaNuevaHector

3. En cada rama modificar el fichero index.html añadiendo vuestro nombre.

Se ha creado un fichero y se ha realizado un commit en los 2 repositorios forkeados anteriormente: hefaso en repositorios de amarino5 y juangarciaciff


4. Con cada rama hacer un pull-request.
Gestionar Pull-requests

Se finaliza el ejercicio realizando pull-request para los ficheros creados anterioremente.

