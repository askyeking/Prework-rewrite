## Lab 5 - Right Triangle

### Overview
* Create a file called _Objective2Lab5.java_ in the _SDPre/Labs_ directory. Write a program that calculates the length of the hypotenuse of a right triangle.
  * Create a class structure with the name `Objective2Lab5`.
  * Create a main method.
  * Create 3 double variables `side1`, `side2`, and `hypotenuse`.
    * `side1` will hold its respective side length.
    * `side2` will hold its respective side length.
    * `hypotenuse` should be assigned the calculated hypotenuse length. **Remember** a<sup>2</sup> + b<sup>2</sup> = c<sup>2</sup>.

  * Print out the hypotenuse.

* Hints:
  * `side1 * side1` is the equivalent of side1<sup>2</sup>
  * `Math.sqrt()` is a function available via the Java Math library.
  ```java
  public static void main(String[] args){
      double num = Math.sqrt(3 * 3);    //num => 3
      double result = Math.sqrt(4) + Math.sqrt(9); //result => 2 + 3 => 5
  }
  ```
  <img src="https://historyofpythagoreantheorem.weebly.com/uploads/2/2/3/1/22318772/6103542_orig.gif"/>


* This time there is no _Starter Code_ provided for you. You are going to create the entire file structure from scratch. **DO NOT COPY AND PASTE**. While the code is similar and it is enticing to use a solution you already have, the additional repetitions will aid in impressing this process in your mind.

### Expected Input
```bash
>> javac Objective2Lab5.java
>> java Objective2Lab5
```
### Expected Output
```bash
>> The hypotenuse of a triangle with sides 10.0 and 8.0 is 12.806248474865697
```

<hr>

[Prev](objective2-lab4.md) | [Up](README.md) | [Next](objective3-README.md)

