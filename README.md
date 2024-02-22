### 1. MOSTRAR FICHEROS QUE NO PASAN NORMINETTE (IGNORANDO LOS MAIN*.C):
~~~
find *.c *.h | grep -v "main*.c" | xargs norminette -R R| grep -v "OK\\!"
~~~
find *.c *.h |  xargs norminette -R R| grep  "Error\!"
find *.c *.h | grep -v "main*.c" | xargs norminette -R R| grep "Error\!" | awk -F : {print }


### 2. ORDENAR POR FECHA Y HORA
ls -la | sort -k 8
