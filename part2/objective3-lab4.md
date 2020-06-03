## Lab 4 - Storing Multiple Values

### Overview
* Create a file called _Objective3Lab4.java_ in the _SDPre/Labs_ directory.
* Using the _Starter Code_ below add code to the commented area that would:
  * Take in the users first name and stores it in the `firstName` variable.
  * Take in the users first name and stores it in the `lastName` variable.
  * Take in the users age name and stores it in the `age` variable.
  * Prints out all the received information in the following format:
  `First Name: John, Last Name: Smith, Age: 23`.

* **Hint** firstName and lastName are Strings, age is an integer. You cannot use `input.next()` to capture an int.

* **Hint** get the int last.

### Starter Code
```java
public class Objective3Lab4 {
  public static void main(String[] args) {
    String firstName;
    String lastName;
    int age;

    Scanner input = new Scanner(System.in);

    /*
      Your solution goes here
    */

    input.close();
  }
}
```
### Expected Input
```bash
>> javac Objective3Lab4.java
>> java Objective3Lab4
```
### Expected Output
```bash
What is your first name?
John
What is your last name?
Smith
How old are you?
23
First Name: John, Last Name: Smith, Age: 23
```

<hr>

[Prev](objective3-lab3.md) | [Up](README.md) | [Next](objective3-lab5.md)

