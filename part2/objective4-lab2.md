## Lab 2 - String Equivalency

### Overview
* Create a file called _Objective4Lab2.java_ in the _SDPre/Labs_ directory.
* Using the _Starter Code_ below add code to the commented area that would:
  * Write an if/else statement that determines if `string1` is equivalent to `string3`.
    * Print out the findings. ie `Banana is equal to Banana` or `Banana is not equal to Banana`

* **Hint** Remember `.equals()`?

### Starter Code
```java
public class Objective4Lab2 {
  public static void main(String[] args) {
    String string1 = "Banana";
    String string2 = "Bacon";
    String string3 = "Banana";

    if(string1.equals(string2)) {
      System.out.println(string1 + " is equivalent to " + string2);
    }
    else {
      System.out.println(string1 + " is not equivalent to " + string2);
    }

    /*
      Your solution goes here
    */
  }
}
```

### Expected Input
```bash
>> javac Objective4Lab2.java
>> java Objective4Lab2
```
### Expected Output
```bash
Banana is not equivalent to Bacon
Banana is equivalent to Banana
```

<hr>

[Prev](objective4-lab1.md) | [Up](README.md) | [Next](objective4-lab3.md)

