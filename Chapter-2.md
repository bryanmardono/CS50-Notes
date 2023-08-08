## Debugging
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
### 1. If we do not know where to start debugging, printf can be very useful
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
### 2. A second way to debug is by using a debugger
To utilize the debugger in vscode, set a breakpoint by clicking on the gutter on the left side of the environment. The red dot that appears will act as a stop sign, so that when you run the debugger the compiler will stop running the code before that stop sign.\
You can then run debug.50 ./"*file name*". You can then see what changes when each line of code is run 1 by 1.

## Arrays
Arrays are a way of storing data back-to-back in memory such that the data is easily accessible.
```
#include <stdio.h>

int main(void)
{
    int scores[3];
    scores[0] = 73;
    scores[1] = 72;
    scores[2] = 33;

    printf("Average: %f\n", (scores[0] + scores[1] + scores[2])/ (float) 3);
}
```
The command "int scores[3]" creates an array called scores with space for 3 *scores* inside it./

But inputting the scores one by one and having to do it by changing the source code is inefficient. Therefore, the code can further be optimized into
```
#include <stdio.h>
#include <cs50.h>

int main(void)
{
    int scores[3];

    for (int i = 0; i<3; i++)
    {
        scores[i] = get_int("Scores:");
    }

    float avg = (float) (scores[0]+scores[1]+scores[2])/3;

    printf ("Average : %f\n", avg);
}
```
The for loop lets us to obtain 3 values of scores without repeating ourselves on the code.

### Using a function that takes array as an input
```
#include <stdio.h>
#include <cs50.h>

const int n = 3;
float average(int array[]);

int main(void)
{
    int scores[n];
    for (int i = 0; i<n; i++)
    {
        scores[i] = get_int("Scores:");
    }

    printf ("Average : %f\n", average(scores));
}

float average(int array[])
{
    float sum = 0;
    for (int i = 0; i < n; i++)
    {
        sum += array[i];
    }
    return sum / n;
}
```
First, the size of the array (n) is declared as a global variable. The function *main* will take in the scores input from the user, then print the output from the function *average*. The function *average* takes array as an input and returns a float as the output. By implementing the global variable n, the size of the array can be changed dynamically throughout the whole code.
