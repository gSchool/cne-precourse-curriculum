# Loops

### Learning Objectives

_By the end of this lesson, you will be able to:_

1. Write `while` loops
1. Write `for` loops
1. Compare and contrast `while` and `for` loops

#### !vimeo
* id: 242982548
### !end-vimeo

### Using `while` and `for` loops

A `while` loop runs as long as a given condition is met.
Here is an example:

```java
double x = 2.0;

while (x > 0.5) {
    // This will run twice.
    x = x / 2.0;
}
```

A `for` loop is similar, but its syntax is a little different.
The initial value of a variable is set, checked, and updated
in the `for` statement, itself, as follows:

```java
for (int i = 0; i < 100; i++) {
    // This will run 100 times.
}
```

Complete the challenges below on `while` and `for` loops:

### !challenge

* type: multiple-choice
* id: c9688947-e2d6-4d50-b554-2b00eb1e1e8e
* title: Capabilities of for vs. while loops

##### !question

Which is able to handle more scenarios &mdash; a `for` or a  `while` loop?

##### !end-question

##### !options

* A `for` loop
* A `while` loop
* They are equally able to tackle the same problems

##### !end-options

##### !answer

They are equally able to tackle the same problems

##### !end-answer

##### !explanation

Although details differ, `for` and `while` loops are equally capable.
You will find, however, that their differences usually make one or the
other more appropriate in a given situation.

##### !end-explanation

### !end-challenge

### !challenge

* type: multiple-choice
* id: d18885d9-ce5c-46c3-9ae7-cd0cd5b372df
* title: Differences between for loops and while loops

##### !question

How is a `while` loop different from a `for` loop?

##### !end-question

##### !options

* A `for` loop is more flexible when using complex conditions
* A `for` loop allows an initialized variable with only local scope
* A `for` loop can only be used with a simple counting variable
* A `while` loop is more concise when simple counting is desired

##### !end-options

##### !answer

A `for` loop allows an initialized variable with only local scope

##### !end-answer

##### !explanation

In a `for` loop, you can declare and initialize a variable to be used by the
condition test in the `for` statement, itself. The variable will then fall out of
scope when the loop ends. This is often desirable, and it is not possible with a
`while` loop.

##### !end-explanation

### !end-challenge

### !challenge

* type: code-snippet
* language: java
* id: 3c8d994c-2cd1-4de5-8b29-d8164e4920c8
* title: Using a while loop

### !question

Using a `while` loop, print the integers from 45 through 50 to the console.

_Note:_ remember to attempt this challenge in your Java playground first
and then paste your answer below. Do not write it directly in the editor.

### !end-question

### !setup

```java
import java.io.PrintStream;
import java.io.ByteArrayOutputStream;

// [to allow student to submit simple statements, wrap the submission
//  using the !setup and !tests sections; example below]
class ChallengeSolution {

    public static String run() {
        ByteArrayOutputStream baos = new ByteArrayOutputStream();
        PrintStream ps = new PrintStream(baos);
        PrintStream old = System.out;

        System.setOut(ps);
```

### !end-setup

### !placeholder

```java
```

### !end-placeholder

### !tests

        System.out.flush();
        System.setOut(old);

        return baos.toString();
    }
}

public class SnippetTest {

    @Test
    public void verifyLoopOutput() {
        assertEquals("45\n46\n47\n48\n49\n50\n", ChallengeSolution.run(),
                     "String produced by while loop");
    }

    @Test
    public void usedWhileLoop() {
        verifySourceContents(true, "while");
    }

    @Test
    public void notUsedForLoop() {
        verifySourceContents(false, "for");
    }

    private void verifySourceContents(boolean contains, String command) {
        String message = String.format("Solution uses '%s' loop", command);
        assertEquals(contains, RAW_SUBMISSION.matches("(?s).*\\b" + command + "\\s*\\(.*"), message);
    }
}

### !end-tests

### !explanation

The `while` loop successfully prints the integers from 45 through 50.
Nice job using `while` in a case that is more naturally done with `for`!
Also, you handled a counter correctly that does not start with zero.

### !end-explanation

### !end-challenge

### !challenge

* type: code-snippet
* language: java
* id: 887b5fc2-20d6-425c-a5d2-fe49030dd1e4
* title: Using a for loop

### !question

Using a `for` loop, print the _even_ integers from 2 through 6 to the console.

_Note:_ remember to attempt this challenge in your Java playground first
and then paste your answer below. Do not write it directly in the editor.

### !end-question

### !setup

```java
import java.io.PrintStream;
import java.io.ByteArrayOutputStream;

// [to allow student to submit simple statements, wrap the submission
//  using the !setup and !tests sections; example below]
class ChallengeSolution {

    public static String run() {
        ByteArrayOutputStream baos = new ByteArrayOutputStream();
        PrintStream ps = new PrintStream(baos);
        PrintStream old = System.out;

        System.setOut(ps);
```

### !end-setup

### !placeholder

```java
```

### !end-placeholder

### !tests

        System.out.flush();
        System.setOut(old);

        return baos.toString();
    }
}

public class SnippetTest {

    @Test
    public void verifyLoopOutput() {
        assertEquals("2\n4\n6\n", ChallengeSolution.run(),
                     "String produced by for loop");
    }

    @Test
    public void usedForLoop() {
        verifySourceContents(true, "for");
    }

    @Test
    public void notUsedWhileLoop() {
        verifySourceContents(false, "while");
    }

    private void verifySourceContents(boolean contains, String command) {
        String message = String.format("Solution uses '%s' loop", command);
        assertEquals(contains, RAW_SUBMISSION.matches("(?s).*\\b" + command + "\\s*\\(.*"), message);
    }
}

### !end-tests

### !explanation

The `for` loop successfully prints the _even_ integers from 2 through 6.
Great job handling a loop with an increment other than 1!

### !end-explanation

### !end-challenge

### Resources

- [Java Tutorials: The `while` and `do-while` Statements](https://docs.oracle.com/javase/tutorial/java/nutsandbolts/while.html)
- [Java Tutorials: The `for` Statement](https://docs.oracle.com/javase/tutorial/java/nutsandbolts/for.html)
