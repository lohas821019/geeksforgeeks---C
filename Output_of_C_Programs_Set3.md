# 題目連結
https://www.geeksforgeeks.org/output-of-programs-set-3/?ref=lbp
<br/>

# Q1 

```
#include <stdio.h>
int main()
{
    printf("%p", main);
    getchar();
    return 0;
}
```
Ans:

這題會印出main的地址，函數名稱其實是一個指向函數的指針

```
struct 
{
   char *name;
   int (*funcptr)();
}
symtab[] = {
   "func", func,
   "anotherfunc", anotherfunc,
}; 
```

<br/>

# Q2 不確定正確解答

```
#include <stdio.h>
int main()
{
    printf("\new_c_question\by");
    printf("\rgeeksforgeeks");

    getchar();
    return 0;
}
```

Ans: 

ew_c_questionygeeksforgeeks

好像是因為\n,\b,\r,是換行符 因此 printf 時會省略


<br/>

# Q3 有難度要注意

```
# include<stdio.h>
# include<stdlib.h>

void fun(int *a)
{
	a = (int*)malloc(sizeof(int));
}

int main()
{
	int *p;
	fun(p);
	*p = 6;
	printf("%d\n",*p);
	
	getchar();
	return(0);
}
```
Ans:

It does not work. 

Try replacing “int *p;” with “int *p = NULL;” and it will try to dereference a null pointer.

https://stackoverflow.com/questions/1398307/how-can-i-allocate-memory-and-return-it-via-a-pointer-parameter-to-the-calling


<br/>

# Q4 考運算符優先順序

```
#include <stdio.h>
int main()
{
	int i;
	i = 1, 2, 3;		
	printf("i = %d\n", i);

	getchar();
	return 0;
}
```
Ans:

i = 1 ，the statement i = 1, 2, 3 is treated as (i = 1), 2, 3 by the compiler.

```
#include <stdio.h>
int main()
{
	int i;
	i = (1, 2, 3);		
	printf("i = %d\n", i);

	getchar();
	return 0;
}
```
Ans:

i = 3

<br/>


# Q5

```
#include <stdio.h>
int main()
{
	int first = 50, second = 60, third;
	third = first /* Will this comment work? */ + second;
	printf("%d /* And this? */ \n", third);
	
	getchar();
	return 0;
}
```

Ans:
110 /* And this? */ 

Compiler removes everything between “/*” and “*/” if they are not present inside double quotes (“”).




