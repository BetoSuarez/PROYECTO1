Como hacer que GIT ingnore archivos al momento de hacer �add *�

Al momento de hacer git add *.extencion agrega los archivos existentes con esa extenci�n.
Por orden de prioridad, git busca patrones para excluir ficheros en los siguientes lugares:

En la l�nea de comandos: ciertos comandos, como por ejemplo git ls-files o git read-tree, permiten excluir ficheros a trav�s de argumentos. Estos patrones tendr�n la m�xima prioridad.
En los ficheros .gitignore
En el fichero $GIT_DIR/info/exclude
En el fichero definido en la variable de configuraci�n core.excludesfile
Todos los ficheros mencionados arriba incluyen en su interior un conjunto de patrones de ficheros que se van a ignorar. Cada patr�n va en una l�nea. Por ejemplo, si incluimos la siguiente l�nea en alguno de estos ficheros:
*.jar
git ignorar� cualquier fichero con extensi�n .jar en cualquier directorio.