Notes:
The cypher itself is a grid of letters from A-Z. With the column on the Y axis descending and the row on the X axis 
Ascending.Depening on the position of the letter on the X axis, the letter corresponding to the Y axis will give us the
solution for the plain text. Think of a 1-12 times table, the numbers on the diagonal are ^2 the given number, on the
Vigenere Cypher, it is similar, except the numbers on the diagonal are the same as each of the corresponding numbers.
The rows of letters will always be alphabetical order. If the row reaches Z, it restarts at A.

The plaintext that you want to cypher, and the key that you encrypt the plaintext with should be the same length.
For example, if I have the word: "POSITIONNORTH" (13 letter), and the key is "WASHINGTON" (10 letters), the key will have to restart in order to fill
the empty space required to decipher it, making it "WASHINGTONWAS". this is called the keystream.

You encrypt each letter at a time to process which row you need to select for the mapping.

How I approached the code(before hand):
We can use a simple formula to encrypt a letter.

E=(R1+C1)%26

E being  the final encrypted letter
R1 is a letter from the first row
C1 is a letter from the first column

%26 representing mod(26)

We need to take the length of the the plaintext and the keystream, and use that amount to 
run our data through the formula.

in our example, we will need to loop it 13 times.

in order to fill out the formula, we need to assign each letter to a number, we can do this via dictionaries.

Each time it is run, we need to make our code to deceipher our letters into their numerical counterparts, add those to our 
formula, calculate it, then with the number we have, find the letter associated with it and add it to a string variable, 
which we will then print.

we can trigger our printing by printing IF it stops looping. 


Approaching code:(after hand)
There were multiple problems with my code after I implemented it. 
1. I could successfully code it to get the desired string, but the cipher's letters would be 1 behind
This could be for a plethora of reasons, I suspect its because of the way python reads lists and dictionaries,
but it could also be how the loop itself was programmed.
2. the code was very blocky
in hindsight, my code did work, but it was very blocky. I am new to programming, so I didnt utilize all of the modules and
other shortcuts I couldve used in order to make the code a little more readable.

I also made the code into a function instead of a stand alone program, so that anyone who comes across it can implement it into there program seamlessley.

After alot of research and math, I think I have found the best solution to my problem.
