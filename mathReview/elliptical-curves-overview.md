# Types of Elliptical Curves

- Elliptical Curve is over a finite field
- Finite Field Examples
- GF(2), GF(5), GF(8) ...

- y^2 = x^3 + ax + b mop p
- Where a and b are no greater than p and,
- 4a^3 + 27b^2 mod p != 0

---

![Elliptical Curve Table](./table.JPG)

- points found (x, y):
- (0, 1), (0, 10), (1, 5), (1, 6), (2, 0), (3, 3), (3, 8), (4, 5), (4, 2), (6, 5), (6, 6), (8, 2), (8, 9)

---

# Check if a point falls on the curve

![Elliptical Curve Addition](./curve.png)

**Given a Set of Points**

- (0, 1)
- (0, 10)
- (1, 5)
- (1, 6)
- (2, 0)
- (3, 3)
- (3, 8)
- (4, 5)
- (4, 6)
- (6, 5)
- (6, 6)
- (8, 2)
- (8, 9)

**Check for point (3,8)**

- y^2 mod 11 = x^3 + x + 1 mod 11
- 8^2 mod 11 = 3^3 + 3 + 1 mod 11
- 9 = 31 mod 11
- 9 = 9
- Point is in the elliptical curve

# Addition of Two Points

**Let the points P = (x1. y1) amd Q = (x2, y2) be in the elliptic group Ep(a, b) and Q != -P**
**The rules for addition over the elliptic group Ep(a, b) is:**

- x^3 = λ^2 - x1 - x2 mod p
- y^3 = λ(x1 - x3) - y1 mod p

---

λ = { y2 - y1 / x2 - x1 mod p such that P != Q
