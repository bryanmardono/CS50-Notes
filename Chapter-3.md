### Running Time
Some common running times:
- $`O(n^2)`$: Order of n squared, where the time to solve will be squared as the size of problem increases
- $`O(n log n)`$
- $`O(n)`$: Order of n, where the time to solve will be linearly increase as the size of problem increases. In the worst case, it will take n step to solve the problem.
- $`O(log n)`$: Order of log n, where the time to solve will eventually plateau as the size of problem gets bigger
- $`O(1)`$: Order of 1, where the problem will be instantly solved in 1 step
Ω is used to denote the lower bound(best case) of an algorithm, such as Ω(log n)
Θ is used to denote when the upper and lower bound are the same, such as when counting the number of people in a room.

### Search
```
#include <cs50.h>
#include <stdio.h>
#include <string.h>

int main(void)
{
    string names[] = {"Carter", "David"};
    string numbers[] = {"+1-617-495-1000", "+1-949-468-2759" };

    string name = get_string("Name: ");
    for (int i = 0; i<2; i++)
    {
        if (strcmp(name, names[i]) == 0)
        {
            printf ("The number is %s\n", numbers[i]);
            return 0;
        }
        else
        {
            printf ("Contact is not found\n");
            return 1;
        }
    }
}
```
In this code, we are utilizing the name in order to search for their phone number. They way the number is attributed is by placing the correponding number according to the name's placement in the first array. However, manually placing the information into 2 different arrays is not a good way to ensure that this code will always work.

### Data Structures
C allows us to create our own data type using the command *struct*.
```
#include <cs50.h>
#include <stdio.h>
#include <string.h>

//create a new data type that contains a stucture
typedef struct
{
    string name;
    string number;
}
person;

int main(void)
{
    person people[2];
    people[0].name = "Carter";
    people[0].number = "+1-617-495-1000";

    people[1].name = "David";
    people[1].number = "+1-949-468-2759";

    string name = get_string("Name: ");
    for (int i = 0; i < 2; i++)
    {
        if (strcmp(name, people[i].name) == 0)
        {
            printf ("The number is %s\n", people[i].number);
            return 0;
        }
        else
        {
            printf ("Contact is not found\n");
            return 1;
        }
    }
}
```
We define a new data type *person* using the command *struct*, and this data type contains two string elements, name and number.

### Sorting
https://cs50.harvard.edu/x/2023/notes/3/

### Recursion
Recursion is a concept in programming where a function calls upon itself.

