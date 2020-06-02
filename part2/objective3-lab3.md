## Lab 3 - Calculate Birth Year

### Overview
* Create a file called _Objective3Lab3.java_ in the _SDPre/Labs_ directory.
* Using the _Starter Code_ below add code to the commented area that would:
  * Take in the users age using `input.nextInt()` and store it in the `age` variable.
  * Calculates what year the user was born in.
  * Prints out the calculated birthYear.


### Starter Code
```java
public class Objective3Lab3 {
  public static void main(String[] args) {
    int birthYear, age, currentYear;

    birthYear = 0;

    Scanner input = new Scanner(System.in);
    System.out.println("How old are you?");

    /*
    Your solution goes here
    */

    System.out.println("You were born in " + birthYear);
    input.close();
  }
}
```
### Expected Input
```bash
>> javac Objective3Lab3.java
>> java Objective3Lab3
```
### Expected Output
```bash
How old are you?
27
You were born in 1990
```

<hr>

[Prev](objective3-lab2.md) | [Up](README.md) | [Next](objective3-lab4.md)

