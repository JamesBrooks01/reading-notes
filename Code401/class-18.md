# Reading Assignment 18

## Cryptography

### Encryption, Decryption & Hacking & The Caesar Cipher

- One of the earliest encryption techniques was the Caesar Cipher that was invented by Julius Caesar to communicate messages to allies.
- It is a substitution cipher where each letter is paired with a different letter of the alphabet found by shifting the alphabet by a certain amount.
- Supposedly, Caesar always used a shift of 3 for his messages and thus, so long as the recipient had that number they could decode any message he sent.
- Now, to crack the cipher without knowing the shift amount you use one of three methods;
  - Frequency Analysis
    - Humans have a tendency to use certain letters more that others. For example the letter E is the most common letter in the english language.
    - Using this knowledge you could analyze a message and identify the letter you believe to be the shifted E and find the amount based on that.
  - Known Plaintext
    - If you have part of the message, it becomes simpler to crack the rest of the message.
  - Brute Force
    - In this example of a shifting substitution encryption based on the alphabet, there are only 25 possible shifts and thus, you could just decode the message 25 times until you got the one that worked.

### Cryptography Crash Course

- Cryptography is derived from the words Crypto and Graphy to mean Secret Writing
- When using Cryptography, you use a Cipher otherwise known as the algorithm you use to turn the plaintext into gibberish unless you have the cipher.
- The proccess is called Encryption to turn it into gibberish and Decryption to turn it back.
- On top of the previously described Substitution Cipher, another class of Cipher is the Permutation Cipher.
  - In a common example of a Columnar Transposition Cipher, you put the letters into a grid and then re-write them out in a different order;
    - Vertically perhaps or maybe diagonally.
- The most famous example of this is the German Enigma Machine used in WW2
- In 1977 IBM and the NSA created one of the earliest software ciphers called the Data Encryption Standard.
- DES was replaced in 2001 by AES when in 1999 it was discovered that a computer could theoretically crack all the possible keys for DES in 2 days.
- AES uses 128,192, or 256 bit keys and chops the data into 16 byte blocks then used a number of substitutions and permutations based on the key value plus some other processes to further obscure the message plus it does this 10 or more times per block.
  - The number 10 was chosen for performance reasons.
- In the modern age, Key Exchange is used for both sender and receiver of data to have the same key despite never communicating it.
- The Diffie-Hellman Key Exchange is one modern example that uses Modular Exponentiation which is taking a number to the power of another number and then taking the remainder when divided by a third number.
  - Computers often use numbers hundreds of digits long which makes finding the exponent prohibitively difficult.
