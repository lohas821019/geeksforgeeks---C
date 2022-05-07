# 題目連結
https://www.geeksforgeeks.org/output-of-a-program-set-2/

<br/>

# Q1 還需要深入了解一下正確寫法
## Predict the output of below programs.
```
#include<stdio.h>
char *getString()
{
	char str[] = "Will I be printed?";
	return str;
}
int main()
{
	printf("%s", getString());
	getchar();
}
```
此題會印出null，原因是return的值有問題 (需再看一看)

<br/>

# Q2 還需要深入了解一下正確寫法

```
#include<stdio.h>
int main()
{
	static int i=5;
	if(--i){
		main();
		printf("%d ",i);
	}
}
```

此題答案為 0,0,0,0

<br/>

# Q3 還需要深入了解一下正確寫法

<br/>
```
#include<stdio.h>
int main()
{
	static int var = 5;
	printf("%d ",var--);
	if(var)
		main();
}
```

此題答案為 5,4,3,2,1,

<br/>

# Q4

<br/>

```
#include<stdio.h>
int main()
{
	int x;
	printf("%d",scanf("%d",&x));
	/* Suppose that input value given
		for above scanf is 20 */
	return 1;
}
```

Ans = 1 ; 因為會讀入輸入的值20，&x是取20的記憶體位置進來處理，會return 1;


<br/>


# Q5 還需要深入了解一下正確寫法

```
# include <stdio.h>
int main()
{
    int i=0;
    for(i=0; i<20; i++)
        {
            switch(i)
            {
            case 0:
                i+=5;
            case 1:
                i+=2;
            case 5:
                i+=5;
            default:
                i+=4;
                break;
            }
            printf("%d ", i);
        }
    getchar();
    return 0;
}
```
Ans: 因為都沒有break，所以每一個都會執行 變成 5+2+5+4 = 16，然後從 16++ 變成17進入下一輪

下一輪為i+=4 所以變成21 ，因此Ans: 16,21





