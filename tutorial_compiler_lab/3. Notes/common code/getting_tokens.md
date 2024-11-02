1. open files
2. initialize buffer to store data
3. get strings from iput file one-by-one
	1. check for comments
	2. print each character from the buffer by considering special character and a normal character seperately
	3. jump to newline in output file
4. close the files 


```c
#include<stdio.h>
#include<string.h>


int main(){
    // 1.open files
    FILE *inputfp,*outputfp;
    inputfp=fopen("input.txt","r");
    outputfp=fopen("output.txt","w");

    // 2.initialize buffer to store data
    int i;
    char buffer[1024];

    // 3.get strings from iput file one-by-one
    while(!feof(inputfp)){
        i=0;
        fscanf(inputfp,"%s",buffer);

        // 3.1 check for comments
        if(buffer[i]=='/'){continue;}
        
        // 3.2 print each character from the buffer by considering special character and a normal character seperately
        while(buffer[i]!='\0'){

            if(buffer[i]=='/'){break;}

            if(buffer[i]=='#'||buffer[i]=='<'||buffer[i]=='>'||buffer[i]=='"'||buffer[i]==';'||buffer[i]=='('||buffer[i]==')'){
                fprintf(outputfp," %c ",buffer[i]);
            }
            else{
                fprintf(outputfp,"%c",buffer[i]);
            }
            i++;
        }
        // 3.3 jump to newline in output file
        fprintf(outputfp,"\n");
    }

    // 4 close the files 
    fclose(inputfp);
    fclose(outputfp);
}
```