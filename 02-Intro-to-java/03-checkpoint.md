# Checkpoint

Verify your understanding of the introduction lessons with the
following exercise.

### !vimeo
* id: 256148737
### !end-vimeo

## Functional requirements

For this checkpoint you must build a command-line application that:

- Takes numbers as arguments.
- Prints out the sum of the positive numbers.

For example:

```
java -jar build/libs/SumOfPositivesCLI.jar -5 6 8 -3 0
# => prints 14

java -jar build/libs/SumOfPositivesCLI.jar 5 7 8 -7 -2
# => prints 20

java -jar build/libs/SumOfPositivesCLI.jar
# => prints 0

java -jar build/libs/SumOfPositivesCLI.jar -1 0 0
# => prints 0
```

See Read Command Line Arguments if you need a refresher on how to take command line arguments.

## Technical requirements

1. Define and declare the `main` method in the `SumOfPositivesCLI` class.

### !challenge

* type: testable-project
* id: 68030eb6-813f-4137-8f47-f87ac7624149
* title: Writing a command-line application
* upstream: https://github.com/gSchool/java-intro-checkpoint
* validate_fork: true
* standard_uuids: JAVA0100-V1
* points: 8

##### !question

### Instructions

1. Fork and clone [this repository](https://github.com/gSchool/java-intro-checkpoint.git).
1. Write code to complete the checkpoint.
1. Once you are satisfied with your solution, check your work:
  - Run `./assess-project` (just `assess-project` on Windows) locally and make sure the tests pass.
1. Commit and push your changes to _your_ fork.
1. Submit the link to your fork below.

##### !end-question

##### !placeholder
Github URL (without .git): https://github.com/<your-username>/java-intro-checkpoint
##### !end-placeholder

##### !explanation
##### !end-explanation

### !end-challenge

### !instructor
Solution to checkpoint at https://github.com/gSchool/java-intro-checkpoint-solution
### !end-instructor
