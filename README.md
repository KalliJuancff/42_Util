1. EJECUTAR NORMINETTE EN TODOS LOS FICHEROS FUENTES EN C, SALVO LOS MAIN Y MOSTRAR SÓLO LOS INCORRECTOS
find *.c *.h | grep -v "main*.c" | xargs norminette -R R| grep -v "OK\!"
