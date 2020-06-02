## Lab 2 - Storing User Input

### Overview
* Create a file called _Objective3Lab2.java_ in the _SDPre/Labs_ directory.
* Using the _Starter Code_ below add code to the commented area that would:
  * Take in the user's name and store it in the `name` variable.
  * Print out `"Hello ***"` where *** is the value the user entered.

### Starter Code
```java
public class Objective3Lab2 {
  public static void main(String[] args) {
    String name = "";
    Scanner input = new Scanner(System.in);

    System.out.println("What's your name?");

    /*
      Your solution goes here
    */

    input.close();
  }
}
```
### Expected Input
```bash
>> javac Objective3Lab2.java
>> java Objective3Lab2
```
### Expected Output
```bash
Whats your name?
Andrew
Hello Andrew
```

<hr>

[Prev](objective3-lab1.md) | [Up](README.md) | [Next](objective3-lab3.md)

