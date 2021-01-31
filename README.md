# Akash
Linumiz Task
```c
#include<stdio.h>
#include<stdlib.h>

int string_length(char*);
void reverse(char*);

int main() 
{
   char string[100];
    int i = 0;
   printf("Enter a string\n");
   //code intead for gets(string)
   while(i<100)
   {
       scanf("%c", &string[i]);
       if(string[i] == '\n')
            break;
        
        i++;
   }
    
   reverse(string);

   printf("Reverse of entered string is \"%s\".\n", string);

   return 0;
}
void reverse(char *string) 
{
   int length, c;
   char *begin, *end, temp;

   length = string_length(string);

   begin = string;
   end = string;

   for ( c = 0 ; c < ( length - 1 ) ; c++ )
      end++;

   for ( c = 0 ; c < length/2 ; c++ ) 
   {        
      temp = *end;
      *end = *begin;
      *begin = temp;

      begin++;
      end--;
   }
}
int string_length(char *pointer)
{
   int c = 0;

   while( *(pointer+c) != '\0' )
      c++;

   return c;
}
```
