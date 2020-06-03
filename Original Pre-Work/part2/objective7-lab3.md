## Lab 3 - Menu Method

### Overview
* Create a file called _Objective7Lab3.java_ in the _SDPre/Labs_ directory.
* Using the _Starter Code_ below add code to the commented areas that would:
  * Write code in the `while` loop that would print out the menu with the provided `printMenu()` method.
    * Take a users input
    * Depending on the users choice, print out the correct message
    * Look back at your logic from [Objective6Lab5](objective6-lab5.md)

### Starter Code
```java
public class Objective7Lab3 {
  public static void main(String[] args) {
    Scanner scanner = new Scanner(System.in);
    int selection;

    while(true){
      /*
      Your solution goes here
      */
    }

    scanner.close();

  }

  public static void printMenu() {
    System.out.println("_____Menu_____");
    System.out.println("1: Say Hello");
    System.out.println("2: List My favorite foods");
    System.out.println("3: Exit");
    System.out.println();
  }
}
```
### Expected Input
```bash
>> javac Objective7Lab3.java
>> java Objective7Lab3
```
### Expected Output
```bash
_____Menu_____
1: Say Hello
2: List My favorite foods
3: Exit

1
Hello Human
_____Menu_____
1: Say Hello
2: List My favorite foods
3: Exit

2
Apples, Bananas, Coconuts
_____Menu_____
1: Say Hello
2: List My favorite foods
3: Exit

3
Goodbye
```

<hr>

[Prev](objective7-lab2.md) | [Up](README.md)

