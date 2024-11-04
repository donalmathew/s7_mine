```
yacc -d exp.y

lex exp.l

gcc lex.yy.c y.tab.c -w

./a.out
```