Used for learning correct program structure accorrding to Herout's coursebook language C.

Errors during creation: 

* an incorrect consonant in function "static double vyp_obvodu(void);" there was used "static double vyp_odvodu(void);" -> 

./kru_main.c:35:15: warning: ‘vyp_obvodu’ used but never defined
   35 | static double vyp_obvodu(void);

* forgot included stdio.h in the kru_io.c file -> 

./kru_io.c:14:1: note: include ‘<stdio.h>’ or provide a declaration of ‘printf’
   13 | #include "kru_main.h" /* natazeni symbolickych konstant, funkcnich prototypu globalnich funcki a globalnich typu spolupracujiciho modulu */
  +++ |+#include <stdio.h>
   14 | 
./kru_io.c:38:5: warning: incompatible implicit declaration of built-in function ‘printf’ [-Wbuiltin-declaration-mismatch]
   38 |     printf("\nZadej polomer kruznice (kladne realne cislo): ");
      |     ^~~~~~

correct command for compiler:

 -> gcc -o vypocet_kruznice ./kru_io.c ./kru_main.c