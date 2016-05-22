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



