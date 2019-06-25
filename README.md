#include<stdio.h>
#include<string.h>
#define isvowel(ch) (ch=='A' || ch == 'a' || ch == 'e' || ch == 'E' || ch =='i'||\
ch == 'I' || ch == 'O'|| ch == 'o'|| ch == 'U' || ch == 'u')
int main()
{
char str[100];
int i, j;
scanf("%s", &str[0]);
for ( i = 0, j=strlen(str)-1;i<j;i++,j--)
{
if (isvowel(str[i])&&isvowel(str[j]))
{
char temp =str[i];
str[i]= str[j];
str[j]=temp;
j--,i++;
}
else if (isvowel(str[i]))
j--;
else if (isvowel(str[j]))
i++;
else
j--,i++;
}
puts(str);
return 0;
}
