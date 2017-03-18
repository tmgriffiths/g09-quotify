Get Gaussian Quote
==================

This is a silly little script. Its only purpose in life is to extract the quote that is printed out at the end of a gaussian job. If does this by using awk to print out lines between the two strings `\\@` and `Job cpu`.

Usage
-----
    ./get_g09_quote < output.out

Output
------
As an example

    $ ./get_g09_quote < output.out
     A MAN SHOULD NEVER BE ASHAMED TO OWN HE HAS BEEN IN THE WRONG
     WHICH IS BUT SAYING IN OTHER WORDS,
     THAT HE IS WISER TODAY THAN HE WAS YESTERDAY.
    
                               -- JONATHAN SWIFT

Call on it in scripts, or make an alias to it on your system. Use your new-found wisdom wisely, or don't.

Known Bugs
----------
- Doesn't work perfectly with CBS-QB3 as it the quote in this case is not contained between the two search strings. Instead it is contained between the first , `\\@` and `Diagonal vibrational polarizability` so instead you get the quote followed by the output to the Complete Basis Set (CBS) Extrapolation data.
