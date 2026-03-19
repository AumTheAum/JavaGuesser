# JavaGuesser
## Time to guess java!

## before anything...
- import java.util.*;

## key rules for coding
- everything must be in a class
- capitalize when needed, java is strict
- scanner classes are needed for inputs


## instance
```
scanner input based on system.in
```
## static void main()
```
create an instance of the class
```
## constructor (acts like main)
```
Make boolean keepGoing
set response to empty string
while keepGoing
    call menu() put result in response
    if response is zero
        set keepGoing to false
    if response is one
        call humanGuesser()
    if response is 2
        call computerGuesser()
    if else
        tell user to type 0, 1, or 2
```
## String menu()
```
takes no parameters
print out menu
    0) quit
    1) human guesser
    2) computer guesser
ask for input
return input as a string
```
## void humanGuesser()
```
create int correct random between 1 and 100
create int guess, initialize to 0
create int turns, intialize to 0
(for now) print out correct answer for easier testing
create boolean keepGoing, initialize to true
while keepGoing is true:
    increment the number of turns
    get guess from input as a string
    convert to int, put in guess
    if guess is less than correct
        print "too high"
    if guess is equal to correct
        print "correct!"
        set keepGoing to false to exit loop
    if turns is less than seven
        player wins: print a win statement
    if turns is greater than seven
        player loses: print a lose statement
    if turns is equal to seven
        it's a tie. Print something appropriate
```
## void computerGuesser()
```
create int lower, set to 1
create int upper, set to 100
create in turns, set to 0
create boolean keepGoing, set to true
while keepGoing is true:
    increment the number of turns
    ask the user for "(H)igh, (L)ow, or (C)orrect" store in response
    if response is H:
        copy guess to upper
        get a new guess with the getMean method
    if response is L:
        copy guess to lower
        get a new guess with the getMean method
    if response is C:
        set keepGoing to false to exit loop
    if else:
        tell user to get smarter
```
## int getMean(int lower, int upper)
```
utility function
used in computer guesser
given ints for lower and upper bound, finds the integer mean of these values
create int mean
add lower + upper
divide the result by two
cast that result into an integer
return the result
not necessary, but good idea
```

