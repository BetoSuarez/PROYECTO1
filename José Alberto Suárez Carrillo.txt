Como hacer que GIT ingnore archivos al momento de hacer ´add *´

Al momento de hacer git add *.extencion agrega los archivos existentes con esa extención.
Por orden de prioridad, git busca patrones para excluir ficheros en los siguientes lugares:

En la línea de comandos: ciertos comandos, como por ejemplo git ls-files o git read-tree, permiten excluir ficheros a través de argumentos. Estos patrones tendrán la máxima prioridad.
En los ficheros .gitignore
En el fichero $GIT_DIR/info/exclude
En el fichero definido en la variable de configuración core.excludesfile
Todos los ficheros mencionados arriba incluyen en su interior un conjunto de patrones de ficheros que se van a ignorar. Cada patrón va en una línea. Por ejemplo, si incluimos la siguiente línea en alguno de estos ficheros:
*.jar
git ignorará cualquier fichero con extensión .jar en cualquier directorio.