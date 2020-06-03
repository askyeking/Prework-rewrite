## Lab 1 - Month Names

### Overview
* Create a file called _Objective5Lab1.java_ in the _SDPre/Labs_ directory.
* Using the _Starter Code_ below add code to the commented areas that would:
  * Given the `month` variable provided, write a switch statement that would print the appropriate String value representation of the month.
  * e.g. `6` -> `June`

### Starter Code
```java
public class Objective5Lab1 {
  public static void main(String[] args) {
    int month = 6;

    switch (month) {
      case 1:
        System.out.println("January");
        break;

      /*
      Your solution goes here
      */

      default:
        System.out.println("That is not a valid month");
        break;
    }
  }
}
```
### Expected Input
```bash
>> javac Objective5Lab1.java
>> java Objective5Lab1
```
### Expected Output
```bash
June
```

<hr>

[Prev](objective5-README.md) | [Up](README.md) | [Next](objective6-README.md)

