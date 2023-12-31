# Modulus

**Set of all integers mod 2, Z / 2**

- 0 mod 2 = 0
- 1 mod 2 = 1
- 2 mod 2 = 0
- 3 mod 2 = 1
- 4 mod 2 = 0
- 5 mod 2 = 1
- 6 mod 2 = 0
- 7 mod 2 = 1
- 8 mod 2 = 0
- 9 mod 2 = 1
- 10 mod 2 = 0
- {0, 1}

---

**Set of all integers mod 5, Z / 5**

- 0 mod 5 = 0
- 1 mod 5 = 1
- 2 mod 5 = 2
- 3 mod 5 = 3
- 4 mod 5 = 4
- 5 mod 5 = 0
- 6 mod 5 = 1
- 7 mod 5 = 2
- 8 mod 5 = 3
- 9 mod 5 = 4
- 10 mod 5 = 0
- {0, 1, 2, 3, 4}

---

- Both {0, 1}, and {0, 1, 2, 3, 4} are a Group, Ring, and Field

---

# Finite Field

- Is a field with a finite number of elements
- The number of elements in a finite field also known as a Galois field and is always a prime or a multiple of a prime
- Finite field exists for only p^m elements where p is prime and m is a positive integer
- GF(2) = GF(2^1) = {0, 1}
- GF(5) = GF(5^1) = {0, 1, 2, 3, 4}
- GF(81) = GF(3^4)
- GF(256) = GF(2^8) -> AES encryption uses this as its standard
- GF(12) is not a finite field

# Prime Field and Extension Field

- GF(p) is called a prime field when m = 1 {0, 1 ...p-1}
- If m > 1 then we have GF(p^m) these are called extension fields
- We are interested in GF(2^8) for AES
- The elements in this set are NOT integers they are polynomials

---

# Polynomials

- Polynomial (many terms)
- Terms have coefficient and variable raised to the power. These terms are connected by addition or subtraction 3x^2 + 2x - 3
- A polynomial can have any number of terms from 1 up but not infinite.

---

- GF(2) = {0, 1} = prime field
- GF(8) = GF(2^3) = mP^m>1 = Extension Field

---

GF(2^3) {

    - 0 0 0     ax^2 + ax + 1  -> 0
    - 0 0 1                    -> 1
    - 0 1 0     0 + x + 0      -> x
    - 0 1 1         x + 1      -> x + 1
    - 1 0 0     x^2 + 0 + 0    -> x^2
    - 1 0 1     x^2 + 0 + 1    -> x^2 + 1
    - 1 1 0     x^2 + x + 0    -> x^2 + x
    - 1 1 1     x^2 + x + 1    -> X^2 + x + 1

}

---

AES
GF(256) -> GF(2^8)

{

     0 0 0 0 0 0 0 0 0   -> 0
     0 0 0 0 0 0 0 1 0   -> x
     0 0 0 0 0 0 0 1 1   -> x + 1
     ...

     1 1 1 1 1 1 1 1 1   -> x^7 + x^6 + x^5 + x^4 + x^3 + x^2 + x + 1

}
