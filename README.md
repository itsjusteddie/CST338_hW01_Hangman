# Hangman

![Java CI with Gradle](https://github.com/cst338-fa26/hw01-hangman-sanchez-lopez-eduardo-itsjusteddie/actions/workflows/gradle.yml/badge.svg?branch=main)

> Requires **JDK 25**. CI (GitHub Actions) builds and runs the tests with Gradle on every push — check the badge above for current status.

## Getting Started

1. Clone your repo:
   ```
   git clone <your-repo-url>
   cd <your-repo-directory>
   ```
2. Run the tests locally:
   ```
   ./gradlew test
   ```
   (Windows: `gradlew.bat test`)
3. Implement the TODOs in `src/main/java/Hangman.java`. There is no work to do in `GameLoader.java`.
4. Commit as you go and push regularly — see [CONTRIBUTING.md](.github/CONTRIBUTING.md) for what "regularly" means here, and check the CI badge above after each push.

## Description

This assignment is designed to address several topics. It serves as an introduction to the Java programming language as well as version control (Git), build systems (Gradle), and unit testing (JUnit). The final result should pass all of the provided unit tests and produce the expected output.

## Acceptance Criteria

- All unit tests pass
- No unused imports
- No unused methods
- All classes and methods have Javadoc comments
- GameLoader must run
- All Hangman methods in GameLoader must be functional
- Formatting and style in adherence to the [Google style guide for Java](https://google.github.io/styleguide/javaguide.html)

## Prerequisites / Topics covered

### Basic language features

Java has many built in primitives, objects, and features that are used in this assignment. Including but not limited to:

- `int`
- `String`
- `boolean`

This assignment will also use the following keywords:

- `private`
- `final`

### [StringBuilder](https://docs.oracle.com/en/java/javase/18/docs/api/java.base/java/lang/StringBuilder.html)

StringBuilder is used throughout the project to create and update Strings. Unlike the built-in String class, String builder is not immutable. Because Java Strings are immutable it is discouraged to use them in loops as each iteration of the loop requires a new String to be created and new memory to be allocated. Additionally the old String must then be garbage collected.

### [List\<\>](https://docs.oracle.com/en/java/javase/18/docs/api/java.base/java/util/List.html)

List\<\> is a generic container in Java. A List\<\> has several methods that are used in this assignment. In the completed solution the following List\<\> methods were used:

- `contains`
- `add`
- `get`
- `Size`

### Field Details

- **secretWord**
  private [String](https://docs.oracle.com/en/java/javase/18/docs/api/java.base/java/lang/String.html) secretWord
  this is the word the user is trying to guess

## HangmanTest.java

### All tests pass

`HangmanTest` exercises the following `@Test` methods; all nine pass once `Hangman.java` is fully implemented:

- `constructorTest`
- `readFileTest`
- `testGetAllWords`
- `checkChooseWord`
- `testDisplayGameState`
- `checkLose`
- `checkWin`
- `hintTest`
- `checkPlay`

Current pass/fail status for all of them is always visible in the CI badge at the top of this page — no need for a static screenshot that would just go stale.

### Expected Output

```text
> Task :compileJava UP-TO-DATE
> Task :processResources NO-SOURCE
> Task :classes UP-TO-DATE
> Task :compileTestJava UP-TO-DATE
> Task :processTestResources NO-SOURCE
> Task :testClasses UP-TO-DATE
Making the file...
testWords.txt created!
adding: SQUARE
adding: CIRCLE
adding: FISH
adding: CAKE

adding: SQUARE
adding: CIRCLE
adding: FISH
adding: CAKE

HINT TEST!

Word chosen: CIRCLE
Hints remaining: 2
You chose: C
C was present!
Guessed Word: C__C__
Remaining Guesses: 5
Remaining hints: 1
Guessed Letters: [C]
Hints remaining: 1
You chose: I
I was present!
Guessed Word: CI_C__
Remaining Guesses: 5
Remaining hints: 0
Guessed Letters: [C, I]
adding: SQUARE
adding: CIRCLE
adding: FISH
adding: CAKE
adding: SQUARE
adding: CIRCLE
adding: FISH
adding: CAKE
Word chosen: CIRCLE
Checking CIRCLE
Word chosen: FISH
Checking FISH
Word chosen: SQUARE
Checking SQUARE
Word chosen: CAKE
Checking CAKE
adding: SQUARE
adding: CIRCLE
adding: FISH
adding: CAKE
Word chosen: FISH
You chose: L
L was not present!
You chose: R
R was not present!
You chose: K
K was not present!
Thanks for playing!
adding: SQUARE
adding: CIRCLE
adding: FISH
adding: CAKE
Word chosen: CIRCLE
You chose: V
V was not present!
Guessed Word: ______
Remaining Guesses: 4
Remaining hints: 2
Guessed Letters: [V]
You chose: W
W was not present!
Guessed Word: ______
Remaining Guesses: 3
Remaining hints: 2
Guessed Letters: [V, W]
You chose: M
M was not present!
Guessed Word: ______
Remaining Guesses: 2
Remaining hints: 2
Guessed Letters: [V, W, M]
You chose: F
F was not present!
Guessed Word: ______
Remaining Guesses: 1
Remaining hints: 2
Guessed Letters: [V, W, M, F]
You chose: R
R was present!
Guessed Word: __R___
Remaining Guesses: 1
Remaining hints: 2
Guessed Letters: [V, W, M, F, R]
You chose: D
D was not present!
Guessed Word: __R___
Remaining Guesses: 0
Remaining hints: 2
Guessed Letters: [V, W, M, F, R, D]
Thanks for playing!
Final score: 0
adding: SQUARE
adding: CIRCLE
adding: FISH
adding: CAKE
Word chosen: CAKE
You chose: K
K was present!
You chose: A
A was present!
You chose: E
E was present!
You chose: C
C was present!
Thanks for playing!
Final score: 4
adding: SQUARE
adding: CIRCLE
adding: FISH
adding: CAKE
Word chosen: CIRCLE
Checking CIRCLE
Guessed Word: ______
Remaining Guesses: 5
Remaining hints: 2
Guessed Letters: []
Guessed Word: ______
Remaining Guesses: 5
Remaining hints: 2
Guessed Letters: []
Word chosen: SQUARE
Checking SQUARE
Guessed Word: ______
Remaining Guesses: 5
Remaining hints: 2
Guessed Letters: []
Guessed Word: ______
Remaining Guesses: 5
Remaining hints: 2
Guessed Letters: []
Word chosen: FISH
Checking FISH
Guessed Word: ____
Remaining Guesses: 3
Remaining hints: 1
Guessed Letters: []
Guessed Word: ____
Remaining Guesses: 3
Remaining hints: 1
Guessed Letters: []
Word chosen: CAKE
Checking CAKE
Guessed Word: ____
Remaining Guesses: 3
Remaining hints: 1
Guessed Letters: []
Guessed Word: ____
Remaining Guesses: 3
Remaining hints: 1
Guessed Letters: []
adding: SQUARE
adding: CIRCLE
adding: FISH
adding: CAKE

adding: SQUARE
adding: CIRCLE
adding: FISH
adding: CAKE
testWords.txt removed!
> Task :test
BUILD SUCCESSFUL in 393ms
3 actionable tasks: 1 executed, 2 up-to-date
19:50:43: Execution finished ':test --tests "HangmanTest"'.
```

## GameLoaderTest.java

### All tests pass

`GameLoaderTest` exercises the following `@Test` methods; all three pass once `GameLoader.java` and `Hangman.java` are fully implemented:

- `fileCreated`
- `gameLoaderTest`
- `gameWinTest`

Current pass/fail status is always visible in the CI badge at the top of this page.

### Expected Output

```text
> Task :compileJava
> Task :processResources NO-SOURCE
> Task :classes
> Task :compileTestJava UP-TO-DATE
> Task :processTestResources NO-SOURCE
> Task :testClasses UP-TO-DATE
Making the file...
testWords.txt created!
SQUARE+
CIRCLE+
FISH+
CAKE+
Welcome to Hangman!
Current score: 0
Guessed Word: ____
Remaining Guesses: 3
Remaining hints: 1
Guessed Letters: []
Your options are:
	 1: Guess a letter
	 2: Get a hint
	 3: exit
Enter your choice:What is your guess: You chose: S
S was present!
Guessed Word: __S_
Remaining Guesses: 3
Remaining hints: 1
Guessed Letters: [S]
Your options are:
	 1: Guess a letter
	 2: Get a hint
	 3: exit
Enter your choice:You chose: F
F was present!
Guessed Word: F_S_
Remaining Guesses: 3
Remaining hints: 0
Guessed Letters: [S, F]
Your options are:
	 1: Guess a letter
	 3: exit
Enter your choice:Thanks for playing!
Welcome to Hangman!
Current score: 0
Guessed Word: ____
Remaining Guesses: 3
Remaining hints: 1
Guessed Letters: []
Your options are:
	 1: Guess a letter
	 2: Get a hint
	 3: exit
Enter your choice:What is your guess: You chose: F
F was present!
Guessed Word: F___
Remaining Guesses: 3
Remaining hints: 1
Guessed Letters: [F]
Your options are:
	 1: Guess a letter
	 2: Get a hint
	 3: exit
Enter your choice:What is your guess: You chose: I
I was present!
Guessed Word: FI__
Remaining Guesses: 3
Remaining hints: 1
Guessed Letters: [F, I]
Your options are:
	 1: Guess a letter
	 2: Get a hint
	 3: exit
Enter your choice:What is your guess: You chose: S
S was present!
Guessed Word: FIS_
Remaining Guesses: 3
Remaining hints: 1
Guessed Letters: [F, I, S]
Your options are:
	 1: Guess a letter
	 2: Get a hint
	 3: exit
Enter your choice:What is your guess: You chose: H
H was present!
Thanks for playing!
testWords.txt removed!
oneWord.txt removed!
> Task :test
BUILD SUCCESSFUL in 467ms
3 actionable tasks: 2 executed, 1 up-to-date
19:50:18: Execution finished ':test --tests "GameLoaderTest"'.
```
