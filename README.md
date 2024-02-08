find *.c *.h | grep -v "main*.c" | xargs norminette | grep -v "OK\!"
