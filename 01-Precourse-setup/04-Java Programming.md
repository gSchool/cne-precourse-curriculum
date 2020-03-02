# Step 3: Java Programming

## Objectives

By the end of this step you should demonstrate the ability to:

- Write and implement a Java Interface
- Write Java classes with:
  - private fields
  - constructors
  - getters and setters

## Running the code

As you write the code below, you can check your work with:

```
./gradlew test
```

Or you can run tests within your IDE.

## Address Class

Create a class named `Address` that has 4 private fields:

- `street` - String
- `city` - String
- `state` - String
- `zip` - String

Create a constructor for `Address` with 4 parameters that match the fields above.

Create getters and setters for all of the fields above.

Override the `toString` method to return the address in the format `<street>, <city>, <state> <zip>`, for example:

```
15 Main St, Cleveland, OH 44101
```

> _REFERENCE_:
  - [Getters and Setters](https://www.tutorialspoint.com/java/java_encapsulation.htm)
  - [Constructors](https://docs.oracle.com/javase/tutorial/java/javaOO/constructors.html)
  - [toString](http://www.javapractices.com/topic/TopicAction.do?Id=55)


## Addressable Interface

Create an Interface named `Addressable` with two methods:

- `getAddresses` - takes 0 arguments, returns a `List` of `Address` objects
- `addAddress` - takes an `Address`, returns void

> _REFERENCE_:
  - [Interfaces](https://docs.oracle.com/javase/tutorial/java/concepts/interface.html)

## Business Class

Create a class named `Business` that implements `Addressable`.

Create two private, final fields:

- `name`: String
- `addresses`: ArrayList of Addresses

Create a constructor for `Business` with a single parameter for `name` (a String).

Create a getter for `name`.

Implement `Addressable` such that if you call `addAddress` and pass it an address, then call `getAddresses`, the address you added should be in the list.

> _REFERENCE_:
  - [Lists](https://docs.oracle.com/javase/tutorial/collections/interfaces/list.html)

## Check your work

Run the following to ensure that your work is complete and accurate:

```
./gradlew test
```

## Add, Commit and Push

Make sure your changes are in Github.
