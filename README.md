### 1. MOSTRAR FICHEROS QUE NO PASAN NORMINETTE (IGNORANDO LOS MAIN*.C):
~~~
find *.c *.h | grep -v "main*.c" | xargs norminette -R R| grep -v "OK\\!"
~~~
