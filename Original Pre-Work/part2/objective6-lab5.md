## Lab 5 - Menu System

### Overview
* Create a file called _Objective6Lab5.java_ in the _SDPre/Labs_ directory. The following code simulates a menu system.
* Using the _Starter Code_ below add code to the commented areas that would:
  * Inside of the endless loop write if statements to determine if 1, 2, or 3 was selected.
    * If 1 was pressed print `Hello World`
    * If 2 was pressed print a String of your favorite foods `Apple, Banana, Coconut`.
    * If 3 was pressed `break` the loop.

### Starter Code
```java
public class Objective6Lab5 {
  public static void main(String[] args) {
    Scanner scanner = new Scanner(System.in);
    int selection;

    while (true) {
      System.out.println("_____Menu_____");
      System.out.println("1: Say Hello");
      System.out.println("2: List My favorite foods");
      System.out.println("3: Exit");
      System.out.println();

      selection = scanner.nextInt();

      /*
      Your solution goes here
      */
    }

    scanner.close();
  }
}
```
### Expected Input
```bash
>> javac Objective6Lab5.java
>> java Objective6Lab5
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

[Prev](objective6-lab4.md) | [Up](README.md) | [Next](objective7-README.md)

