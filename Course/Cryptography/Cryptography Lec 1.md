Cryptography is a part of Cryptology.
Cryptology divides into:
- **Cryptography** is a science of devolving a protocols, in which this protocols should be secure and implement this protocols and deploy it.

- **Cryptoanalysis** is the opposite part of Cryptography, it tries to attack the devolved / implemented protocols and searching for bugs and broke it's security.

The goal of **Cryptoanalysis** is Ethical attacking for just making testing the security of the protocols **Or** maybe it's nonethical hacking from countries or companies between each others.

**Modern cryptography** started in 1970, the driven force behind Cryptography is the development of computational science.

let's take an example: (**Shift cipher**)
let's assume that the messages are written only from a to z.
each character have a special code. a -> 0, c- >2 etc.....
because any عمليه حسابيه we have to deal with numbers and we have to encode the text to numbers.
let's take a random character -> D  = 3
The probability of choosing a random character is 1/26
The encoding process:
every character will be shifted-> character + the random character (d) mod 26.
Ex: ( ( x + 3 ) mod 26 )

The problem of that (Shift cipher) it\`s too week cause you can broke it throw 26 try.

There is a little bit advanced one called (**substitution cipher**)
The mapped character will be random permutation.
If you wanna beak it you have to make 26! try !!!!!!!!!!!!!!!!!!!!!.
There is an elegant way to attack this system.
We could use the diagram of the most frequent character, this is a statistical analysis.

All of this ways (substitution cipher and Shift cipher) are **Ad Hok**.
Modern cryptography came to make this ways a scientific ways.

**Modern cryptography**:
- **Definitions**: We define in a mathematical form كل حاجه اي معناها, formal and regules, precies
- **Assumptions**: every thing should be based on assumption. explicit assumption.
- **Proofs**:  When saying my the system is secure, you could prove that mathematically using definitions and assumptions and what level of security against what type of attack.

