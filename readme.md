-  ¿Qué comando utilizaste en el paso 11? ¿Por qué?

R: git reset --hard HEAD\~1, porque con el comando git reset HEAD\~1 me muevo al commit anterior
   y con el modificador --hard, le indico a git que modifique mi workf copy, ya que si no se lo indico
   git me deja los cambios en el working copy.

- ¿Qué comando o comandos utilizaste en el paso 12? ¿Por qué?

R: git reflog para ver el rastro de commits que he ido dejando. Observo el que me indica "moving to HEAD~1"
   que es la última referencia que tenía de cuando tenía los cambios en git-nuestro.md y me quedo, en este caso,
   con el commit anterior, que como el propio mensaje nos indica, "Modifico git-nuestro.md en styles", por lo tanto
   copiamos el commit de esa línea y ejecutamos git reset --hard CommitCopiado. Utilizamos nuevamente el --hard porque
   nos vuelve a interesar modificar nuestro working copy.


- El merge del paso 13, ¿Causó algún conflicto? ¿Por qué?

R: Git merge master.
   No. Porque en la rama master no se ha hecho ningún cambio, por lo tanto, no recibimos cambios.

- El merge del paso 19, ¿Causó algún conflicto? ¿Por qué?

R: Nos movemos al branch de styled y hacemos un git merge htmlify. En este caso sí que nos da 
   conflictos debido a que en la rama htmlify se han hecho cambios que no tenemos contemplados en la rama de styled
   y estos cambios ocurren en las mísmas líneas que se han tocado en la rama styled. Entonces git nos pregunta con qué cambios
   queremos quedarnos, puesto que git no entiendo de lenguajes de programación.


- El merge del paso 21, ¿Causó algún conflicto? ¿Por qué?

R: Nos movemos al branch de master y hacemos un git merge styled. En este caso no nos da
   conflictos debido a que en esta rama no se había vuelto a tocar el archivo git-nuestro.md. Por lo tanto nos hemos
   traido los cambios de la rama styled sin ningún tipo de problema.

- ¿Qué comando o comandos utilizaste en el paso 25?

R: git log --graph --pretty=oneline, también puede usarse git log --graph --oneline y vemos el commit abreviado.

- El merge del paso 26, ¿Podría ser fast forward? ¿Por qué?

R: git merge --no-ff title. Entiendo que sí podria ser fast forward ya que si representamos el diagrama de todo lo que hemos hecho
   del commit de title a master, el recorrido es lineal.

- ¿Qué comando o comandos utilizaste en el paso 27?

R: git reset HEAD~1

- ¿Qué comando o comandos utilizaste en el paso 28?

R: git checkout -- git-nuestro.md

- ¿Qué comando o comandos utilizaste en el paso 29?

R: git branch -D title
   git push origin --delete title

- ¿Qué comando o comandos utilizaste en el paso 30?

R: git reflog para ver el rastro de commits que he ido dejando. Observo que hay un registro donde el mensage me indica, "merge title" y como el
   único que hemos hecho ha sido en master copiamos el commit de esa línea y ejecutamos git reset --hard CommitCopiado

- ¿Qué comando o comandos usaste en el paso 32?

R: git reflog para ver el rastro de commits que he ido dejando. Observo en el primer commit (el de más abajo) que el mensaje indica:
   "creo git-nuestro.md", copiamos el commit de esa linea y ejecutamos git checkout CommitCopiado

- ¿Qué comando o comandos usaste en el punto 33?

R: git reflog para ver el ratros de commits que he ido dejando. Observo que una de las líneas en el mensaje contiene, "Añado un título a git-nuestro.md
   en title", copiamos el commit de esa linea y ejecutamos git checkout CommitCopiado
