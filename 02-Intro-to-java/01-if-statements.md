# If Statements

### Learning Objectives

_By the end of this lesson, you will be able to:_

1. Write `if` statements
1. Make comparisons correctly with objects

### !vimeo
* id: 244913409
### !end-vimeo

### Using if statements

When you need to base the execution of code block on a condition,
you can use an `if` statement and optional `else` or `else if` statement(s).
Here is an example:

```java
boolean isItTrue = false;

if (isItTrue) {
    System.out.println("It is true.");
} else {
    System.out.println("It is not true.");
}
```
The above will print "It is not true." to the console.

### Comparing primitive types

If you need to compare two primitive types, such as `int`,
you should use `==`, `!=`, `<`, `>`, etc. Here's an example:

```java
int n = -5;

if (n < 0) {
    System.out.println("The number is negative.");
}
```
The above will print "The number is negative." to the console.

### Comparing object types

If the types you want to compare are objects (like type `String` or `List`),
you need to use the object's `equals()` method. Here's an example:

```java
String status = "leaving";

if (status.equals("arriving")) {
    System.out.println("Hello!");
} else if (status.equals("staying") {
    System.out.println("We are glad you are here.");
} else {
    System.out.println("Goodbye, and do visit again!");
}
```
The above will print "Goodbye, and do visit again!" to the console.

Complete the challenges below to verify your understanding of `if` statements:

### !challenge

* type: code-snippet
* language: java
* id: 701151d6-1771-44d3-874b-3dbb8007a393
* title: Single comparison

### !question

In the space given below, define and implement a method called `isActive`. It takes as input a `String` and returns `true` if the passed in string is "active", `false` if it is any other string.

_Note_: remember to attempt this challenge in your Java playground first and then paste your answer below. Do not write it directly in the editor.
### !end-question

### !setup

// [to allow student to submit simple statements, wrap the submission
//  using the !setup and !tests sections; example below]
class ChallengeSolution {

### !end-setup

### !placeholder
boolean isActive(String status) {
    // Implement your solution
}
### !end-placeholder

### !tests

}

public class SnippetTest {

    ChallengeSolution solution = new ChallengeSolution();

    @Test
    public void emptyStringReturnsFalse() {
        String input = new String("");
        assertEquals(false, solution.isActive(input), "For empty string");
    }

    @Test
    public void singleLetterReturnsFalse() {
        String input = new String("a");
        assertEquals(false, solution.isActive(input), "For single letter string");
    }

    @Test
    public void activeReturnsTrue() {
        String input = new String("active");
        assertEquals(true, solution.isActive(input), "For new \"active\" string");
    }

    @Test
    public void substringActiveReturnsFalse() {
        String input = new String("ctive");
        assertEquals(false, solution.isActive(input), "For substrings of \"active\"");
    }

    @Test
    public void activeSubstringReturnsFalse() {
        String input = new String("superactive");
        assertEquals(false, solution.isActive(input), "For input where a substring is \"active\"");
    }
}
### !end-tests

### !explanation

The data type being compared here is `String`. Since `String` is a type of object, you should use the `equals` method on it to compare it to another `String`.

### !end-explanation

### !end-challenge

### !challenge

* type: code-snippet
* language: java
* id: 33c5bb69-97b4-4c7d-be00-2cb7302bedbc
* title: Multiple comparisons

### !question

In the space given below, declare and define the method `grade`. This method takes as input a student score and returns a letter grade based on that score. The grade boundaries (inclusive) are as follows:

| Lower Bound | Upper Bound | Grade |
|-------------|-------------|-------|
|     90      |     100+    |   A   |
|     80      |      89     |   B   |
|     70      |      79     |   C   |
|     60      |      69     |   D   |
|      0      |      59     |   F   |

_Note_: remember to attempt this challenge in your Java playground first and then paste your answer below. Do not write it directly in the editor.

### !end-question

### !setup

class VariableChallenge {


### !end-setup

### !placeholder

String grade(int input) {
  // Implement your solution
}
### !end-placeholder

### !tests

}

// public test class name **must** be `SnippetTest` to match the generated file name
public class SnippetTest {

    VariableChallenge solution = new VariableChallenge();

    @Test
    public void zeroReturnsF() {
        int score = 0;
        assertEquals("F", solution.grade(score), "Grade for " + score);
    }

    @Test
    public void fiftyNineReturnsF() {
        int score = 59;
        assertEquals("F", solution.grade(score), "Grade for " + score);
    }

    @Test
    public void sixtyReturnsD() {
        int score = 60;
        assertEquals("D", solution.grade(score), "Grade for " + score);
    }

    @Test
    public void sixtyNineReturnsD() {
        int score = 69;
        assertEquals("D", solution.grade(score), "Grade for " + score);
    }

    @Test
    public void seventyReturnsC() {
        int score = 70;
        assertEquals("C", solution.grade(score), "Grade for " + score);
    }

    @Test
    public void seventyNineReturnsC() {
        int score = 79;
        assertEquals("C", solution.grade(score), "Grade for " + score);
    }

    @Test
    public void eightyReturnsB() {
        int score = 80;
        assertEquals("B", solution.grade(score), "Grade for " + score);
    }

    @Test
    public void eightyNineReturnsB() {
        int score = 89;
        assertEquals("B", solution.grade(score), "Grade for " + score);
    }

    @Test
    public void ninetyReturnsA() {
        int score = 90;
        assertEquals("A", solution.grade(score), "Grade for " + score);
    }

    @Test
    public void hundredReturnsA() {
        int score = 100;
        assertEquals("A", solution.grade(score), "Grade for " + score);
    }
}

### !end-tests

### !explanation

Since you are given multiple conditions that are all mutually exclusive, using the `if`/`else if`/`else` pattern is the desirable way to solve this challenge. Note that the order of the comparisons is very important.

### !end-explanation

### !end-challenge

### Resources

- [Java Tutorials: The `if-then` and `if-then-else` Statements](https://docs.oracle.com/javase/tutorial/java/nutsandbolts/if.html)
- [Java Tutorials: Equality, Relational, and Conditional Operators](https://docs.oracle.com/javase/tutorial/java/nutsandbolts/op2.html)
- [Java Tutorials: Expressions, Statements and Blocks](https://docs.oracle.com/javase/tutorial/java/nutsandbolts/expressions.html)
- [Java Tutorials: The `switch` Statement](https://docs.oracle.com/javase/tutorial/java/nutsandbolts/switch.html)
- [Java Tutorials: Branching Statements](https://docs.oracle.com/javase/tutorial/java/nutsandbolts/branch.html)
- [Java Tutorials: Questions and Exercises: Control Flow Statements](https://docs.oracle.com/javase/tutorial/java/nutsandbolts/QandE/questions_flow.html)
