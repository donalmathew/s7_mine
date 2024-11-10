
**For lex and yacc:**
- [\n] is exempted from .
- argc and argv is for terminal word count
- yytext[0] returns a number, while yytext returns a pointer. Therefore atoi operation works with only yytext.
```c
/* All these patterns match a newline: */

[\n]        { lines++; in_word=0; }    /* Using character class */
\n          { lines++; in_word=0; }    /* Direct newline */
"\n"        { lines++; in_word=0; }    /* Quoted newline */
['\n']      { lines++; in_word=0; }    /* Character class with quotes */
```

