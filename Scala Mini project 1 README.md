# SCALA Mini Project 

# 1. Furtune Game 

### -The Player will be given 5 Turns to guess a number lets say "X"
### -After Each Attempt Your Program will do:-
#### -If the player's entered number is less than the actual number X then show the output the player that his guess is less than the actual number X and show him the remaining guess out of 5.
#### -If the player's entered number is Greater than the actual number X then show the output the player that his guess is Greater than the actual number X and show him the remaining guess out of 5.
#### -If he has no tries left show output message player lost the GAME and show him the number X.
#### -If players entered number is equal to X then show output that he won and shoe him th number of tries taken.
### -The Number X will be Between - 0 to 100.


code- 
          
          import scala.io.StdIn.readLine
          import scala.util.control.Breaks._
  
          object Main{
          def main(args: Array[String]): Unit = {
          var X = 50
          var gamestatus = "Lost"
          breakable() 
          {
          for (w <- 1 to 5) 
          {
          var x = readLine("Enter Your Number")
          var guess = x.toInt


        if (guess < X) {
          println("Your guess is less than X")
          println(5 - w)
        } else if (guess > X) {
          println("Your guess is Greater than X")
          println(5 - w)
        } else {
          println("You guessed it Correctly!!")
          println(w)
          gamestatus="Won"
          break()
        }

      }
    }
         if(gamestatus == "Lost")
           println("you lost the Game ")

 
        }
        }


### -Output
### When Lost
![Lost](https://github.com/Reyyadav/scala/assets/153619494/55c0553c-c596-47ec-88d2-7e6258c69d14)

### When Won
![Won](https://github.com/Reyyadav/scala/assets/153619494/9610d462-f0be-4295-b9f1-4f108f135cc5)

When X Actual Number is Generated Randomly

                              import scala.io.StdIn.readLine
                              import scala.util.control.Breaks._
                              import scala.util.Random
                              
                              object Main {
                                def main(args: Array[String]): Unit = {
                                  
                                  var X = Random.nextInt(101)
                                  var gamestatus = "Lost"
                                  breakable() {
                                    for (w <- 1 to 5) {
                                      var x = readLine("Enter Your Number")
                                      var guess = x.toInt
                              
                                      if (guess < X) {
                                        println("Your guess is less than X")
                                        println(5 - w)
                                      } else if (guess > X) {
                                        println("Your guess is Greater than X")
                                        println(5 - w)
                                      } else {
                                        println("You guessed it Correctly!!")
                                        println(w)
                                        println(X)
                                        gamestatus="Won"
                                        break()
                                      }
                              
                                    }
                                  }
                                       if(gamestatus == "Lost")
                                       println(X)
                                         println("you lost the Game ")
                              
                               
                                }
                              
                              }


### Code

- ![Code](https://github.com/Reyyadav/scala-Mini-Project/assets/153619494/b173b7e1-6a56-42e5-a413-08229df4ac5c)

                              


## Code Explaination:-
Here's an explanation of the code:

### -import scala.io.StdIn.readLine: 
This imports the readLine method from the scala.io.StdIn package, which allows us to read input from the console.

### -import scala.util.control.Breaks._: 
This imports utilities for implementing breaks and continues in loops.

### -import scala.util.Random:
This imports the Random utility from the scala.util package, which we use to generate random numbers.

### -object Main { ... }: 
This defines the main object of the program.

### -def main(args: Array[String]):Unit = { ... }: 
This is the entry point of the program. It defines the main method, which takes an array of strings as input arguments and returns nothing (Unit).

### -var X = Random.nextInt(101): 
This line generates a random number between 0 and 100 (inclusive) and assigns it to the variable X. This is the number the player needs to guess.

### -var gamestatus = "Lost": 
This variable keeps track of the game status. It is initialized to "Lost" and will be updated to "Won" if the player guesses the correct number.

### -breakable() { ... }: .
This function allows us to break out of a loop early if needed. It defines a scope within which we can use the break() method to exit the loop prematurely.

### -for (w <- 1 to 5) { ... }: 
This loop iterates 5 times, representing the player's 5 attempts to guess the number.

### -var x = readLine("Enter Your Number"): 
This line prompts the player to enter their guess and reads their input from the console. The input is stored as a string in the variable x.

### -var guess = x.toInt: This line converts the string input x into an integer and stores it in the variable guess.

### -if (guess < X) { ... } else if (guess > X) { ... } else { ... }: 
This conditional block checks if the player's guess is less than, greater than, or equal to the random number X.

### -println("Your guess is less than X") and println("Your guess is Greater than X"): 
These lines inform the player whether their guess is too low or too high.

### -println("You guessed it Correctly!!"), println(w), println(X): 
If the player's guess is correct, these lines inform the player that they guessed correctly, display the number of attempts taken, and reveal the correct number X.

### -gamestatus="Won": 
This line updates the gamestatus variable to "Won" if the player guesses the correct number, indicating that the player won the game.

### -break(): 
This line breaks out of the loop early if the player guesses the correct number, preventing the loop from continuing unnecessarily.

### -if(gamestatus == "Lost") println(X) println("you lost the Game "): 
This conditional block checks if the game status is still "Lost" after the loop ends. If so, it prints the correct number X (revealed to the player since they lost) and informs the player that they lost the game.
