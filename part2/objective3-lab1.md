## Lab 1 - Using `Scanner`

### Overview
* Create a file called _Objective3Lab1.java_ in the _SDPre/Labs_ directory.
* Using the _Starter Code_ below add code to the commented area that would:
  * Take in a string from the user and store it in the `userInput` variable.
  * Print out what the user typed in.

### Starter Code
```java
public class Objective3Lab1 {
  public static void main(String[] args) {
    String userInput = "";
    Scanner input = new Scanner(System.in);

    System.out.println("Please Type a word: ");

    /*
      Your solution goes here
    */

    input.close();
  }
}
```
### Expected Input
```bash
>> javac Objective3Lab1.java
>> java Objective3Lab1
```
### Expected Output
```bash
Please Type a word:
Hello
Hello
```

<hr>

[Prev](objective3-README.md) | [Up](README.md) | [Next](objective3-lab2.md)

