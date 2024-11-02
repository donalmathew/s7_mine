
- Run the program: [[running lex program]]

OUTPUT

INPUT: input.c

int a,b,c;

c = a + b;

To execute the program: lex 11anaghasethu-p2.l

cc lex.yy.c

./a.out

  

  

OUTPUT: kwd id,id,id;

id op-equ id op-plus id;