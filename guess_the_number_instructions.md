# Guess the number instructions

Guess the number is a simple game where your program tries to guess the number
you are thinking of between 0 and 100.

Your program should guess a number, if it is right it will exit and display a
success message. If it is wrong it should ask if the number you are thinking of
is higher or lower. It should adjust its guess based on this, and guess again
until it guesses the number correct.

Running the program should look something like this.
```
$ ./gtn
is the number 50? yes(y) no(n) n
is the number higher(h) or lower(l)?h
is the number 75? yes(y) no(n) n
is the number higher(h) or lower(l)?h
is the number 88? yes(y) no(n) n
is the number higher(h) or lower(l)?l
is the number 81? yes(y) no(n) n
is the number higher(h) or lower(l)?l
is the number 78? yes(y) no(n) n
is the number higher(h) or lower(l)?l
is the number 76? yes(y) no(n) y
your number is 76! and it took 6 guesses to find it
```

# Hints

One way of thinking about this problem is that there are to numbers the highest
(max. 100 to start) number are guess could be and the lowest (min. 0 to start).
When we guess a number, and it is too low we adjust the min to are guess because we
know the number is higher than it. When we guess, and it is high we adjust are
max, again because we know the number is less than are guess. This can be
repeated until we narrow down what the number is.

# Going farther

There is and optimization that can be added when there is only one number between
the min and max. this means that the number between min and max must be the
correct answer, and so we can exit with are success message.

This problem has an optimal solution which minimizes the number of guesses are 
program has to make. When guessing between 0 and 100 the program should not take
more than 6 guesses to find the number.
