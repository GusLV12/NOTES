# Git y GitHub

## ASSETS

- [Comandos mas usados en github.](https://gist.github.com/chandzul/f06fee2120112e87831ce08f04af6563)
- [GITHUB ACCESS TOKEN.](https://www.youtube.com/watch?v=2nzOI-ynXF4&list=LL&index=3)
- [GIT guía de comandos.](https://rogerdudler.github.io/git-guide/index.es.html)

## Configuración

- **`git --version //Versión de git`**
- **`git config --global [user.name](http://user.name/) //Configuracion de usuario`**
- **`git config --global [user.email](http://user.email) //Configuracion de correo`**
- **`git config --global core.editor //Configuracion de IDE`**
- **`git config --global -e //Mostrar en IDE`**
- **`git config --global core.autocrlf true //Opcion windows`**
- **`git config --global core.autocrlf input //opcion linux`**

## Comandos

- **``ls //determina y enlista archivos y carpetas en un determinado directorio``**
- **``pwd //Saber donde nos encontramos ubicados``**
- **``cd //Movernos en los directorios (carpetas)``**
- **``cd .. //Retrocedes``**
- **``mkdir nombre_carpta//Crear nuevo directorio(carpeta)``**
- **``git init //Empezar un repositorio vacio``**
- **``git remote add <nombre del repo> “pagina web”``**
- **``ls -a //Muestra todo, incluso repositorios``**
- **``code .//Abre el IDE``**
- **``git status //Estado actual de nuestro repositorio``**
- **``git add//añade los archivos que querramos``**
- **``git add . //añade todos los archivos que querramos``**
- **``git commit -m “Nombre”//Comprometer los cambios``**
- **``rm Nombre_archivo //Eliminar archivo``**
- **``git rm Nombre_archivo //Eliminar archivos mas rapidos (saltando un paso)``**
- **``git restore Nombre_archivo //recuperas el archivo``**
- **``git mv Nombre_viejo Nombre_nuevo //Cambiar nombre``**
- **``git diff //Muestra los cambios visuales``**
- **``git diff --staged //Muestra todos los cambios obtenidos en el transcurso``**
- **``git log //Historial del repositorio``**
- **``git branch //Muestra rama``**
- **``git branch <nombrerama> //Crea rama``**
- **``git checkout -b nombre //Crear rama y nombre``**
- **``git checkout <rama que quiero cambiar>//rama que quiero cambiar``**
- **``cat nombre_archivo //Muestra el contenido del archivo``**
- **``git merge Rama_que_tiene_contenido //Añadir los cambios de una rama a otra``**

## Semantica para commits

![Imagen semantica](/public/img/git/semantica.png)
[Semantic Commit Messages.](https://gist.github.com/joshbuchea/6f47e86d2510bce28f8e7f42ae84c716)
