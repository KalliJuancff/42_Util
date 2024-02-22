### 1. MOSTRAR FICHEROS QUE NO PASAN NORMINETTE (IGNORANDO LOS MAIN*.C):
~~~
find *.c *.h | grep -v "main*.c" | xargs norminette -R R| grep -v "OK\\!"
~~~
find *.c *.h |  xargs norminette -R R| grep  "Error\!"
find *.c *.h | grep -v "main*.c" | xargs norminette -R R| grep "Error\!" | awk -F : {print }

### 2. ORDENAR POR FECHA Y HORA LAS ENTRADAS DE UN DIRECTORIO
~~~
ls -la | sort -k 8

### 3. BUSCAR LOS #INCLUDE DE LOS FICHEROS *.C SIN DUPLICAR
~~~
grep "#include" *.c | sed 's/^[^:]*://' | sort | uniq
