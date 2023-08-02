# Compiler
Programmers write code in *source code*, but machines cannot read source code directly. There is a need to convert *source code* into *machine code*. Compiler is a software that can convert source code (programming language) into machine code (binary).

## Hello World
To create a new file, you can input "code <name>.c into the terminal"
 
```
  #include <stdio.h>
  
  int main(void)
  {
    printf("hello, world\n");
  }
```
The first line of the code tells the compiler that you'd like to use the library called *stdio.h*. This allows you to use the printf function.

The \n on the print line creates a new line after the command is run.

### Variables
You can assign value to a variable from an input.
 
```
string answer = get_string("what's your name? ");
```
The function get_string will take your input as the return value. Then the (=) will assign that value to the variable *answer* as a string.

Applying this to the Hello World,

```
  #include <cs50.h>
  #include <stdio.h>
 
  int main(void)
  {
     string answer = get_string("What's your name? ");
     printf("hello, %s\n", answer);
  }
```
%s is a placeholder telling the compiler that it should get a string to plug in there.

 ### While Loop
 
 ```
#include <stdio.h>
#include <cs50.h>

int main(void)
{
    int i=0;
    while (i < 3)
    {
        printf("meow\n");
        i+=1;
    }
}
 ```
 ### For Loop
 
```
#include <stdio.h>
#include <cs50.h>

int main(void)
{
    for (int i = 0; i < 3; i++)
    {
        printf("meow\n")
    }
}
 ```
### Forever/Continuous While Loop
```
#include <stdio.h>
#include <cs50.h>

int main(void)
while (true)
{
    printf("meow\n");
}
```                          
### Writing a Function
```
#include <stdio.h>
#include <cs50.h>

int main(void)
{
    // Get size of grid
    int n = get_size();
    
    // Print grid of bricks
    print_grid(n);
}
 
int get_size(void)
{
    int n;
    do
    {
        n = get_int("Size: ");
    }
    while (n<1);
    return n;
}
```
### Command Line Interface (CLI)
#### cd (change directory) : ]
Format: cd *target folder*/
cd ./ : stay in current directory
cd ../ : move to previous (parent) directory
cd / : move to root directory
cd ~ : move to user 's home directory
cd : move to user's home directory
#### cp (copy) :
#### ls (list) : list all of the files in the current folder
#### mv (move) : moves (pastes over) current file into target file. can be used for renaming files
Format: mv *current file* *target file*
#### mkdir (make directory)
#### rm (remove)
Format: rm *target file*
#### rmdir (remove directory)

### Mario 
![Alt text]https://github.com/bryanmardono/CS50-Notes/blob/main/image_2023-08-02_185859016.png
