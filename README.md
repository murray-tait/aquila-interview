# Developer Interview Exercise
## Task
Write a Java program that outputs a count of all the legal phone numbers that can be
generated by moving a chess piece around a standard telephone keypad.

A legal phone number has the following requirements:

* Must be 10 digits long.
* Must contain only digits (no * or #).

The telephone keypad layout is:

```
1 2 3
4 5 6
7 8 9
* 0 #
```

The program must take its input from the command line, accepting:
* The name of a chess piece (king, queen, bishop, knight, rook, pawn).
* A starting digit, 0 to 9.

For example, `java ChessPhoneNumbers queen 5`

The program should not return a list of the actual numbers generated; just the count of
them.

A legal move is defined as any move that is normally legal for the piece in chess, with the
following additions:

* Staying in place is a legal move for all pieces.
* When a pawn reaches the top row, it becomes a queen.

A pawn, starting on one of the bottom two rows (one of the digits 7, 8, 9 or 0), may move
either one or two spaces forward the first time it moves .

## Prerequisites

Install [Java JDK 8](https://docs.oracle.com/javase/8/docs/technotes/guides/install/install_overview.html)

The source code comes with [Maven wrapper](https://github.com/takari/maven-wrapper), therefore a separate [Maven](https://maven.apache.org/) installation is not required.

## Launching the program

Execute `java -jar target/aquila-interview-0.1.0-SNAPSHOT.jar queen 5` to run the program with a Queen starting on the 5 key.

This should return `963635092` as a count of the number of legal phone numbers.

## Building

Execute `mvnw.cmd clean package` (Windows) or `./mvnw clean package` (Linux and MacOS)  to build, run tests, and create jars.