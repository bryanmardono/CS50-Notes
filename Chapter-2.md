### Debugging
Let this be a buggy code 
```
#include <stdio.h>

int main(void)
{
    for (int i = 0; i <= 3; i++)
    {
        printf("#\n");
    }
}
```
## 1. If we do not know where to start debugging, printf can be very useful
```
#include <stdio.h>

int main(void)
{
    for (int i = 0; i <= 3; i++)
    {
        printf("i is %i\n", i);
        printf("#\n");
    }
}
```
## 2. A second way to debug is by using a debugger
To utilize the debugger in vscode, set a breakpoint by clicking on the gutter on the left side of the environment. The red dot that appears will act as a stop sign, so that when you run the debugger the compiler will stop running the code before that stop sign.
You can then run debug.50 ./*file name*. You can then see what changes when each line of code is run 1 by 1.
