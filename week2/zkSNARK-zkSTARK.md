# ZK-SNARKs

- Zero-Knowledge: Allows one party (the prover) to prove to another party (the verifier) that they know a value x, without conveying any information apart from the fact that they know the value x.

- Succinct: The proofs are small in size and quick to verify, even for complex statements.

- Non-Interactive: The proof process does not require back-and-forth communication between the prover and the verifier. Once the proof is created, it can be verified without any further interaction.

- Argument of Knowledge: It is a computational proof that certain information is known by the prover.

- Working Mechanism:
  - Computation Encoding: First, the computation that needs to be proven is encoded into a polynomial equation.
  - Trusted Setup: Next, a trusted setup phase generates public parameters for creating and verifying proofs.
  - Proof Generation: The prover then generates a proof that they have inputs that satisfy the polynomial equation, without revealing the inputs themselves.
  - Verification: The verifier uses the public parameters from the trusted setup to check the proof.

---

# ZK-STARKs (Cairo)

- Zero-Knowledge: Similar to ZK-SNARKs, it enables proving knowledge of a secret without revealing the secret itself.

- Scalable: Designed to handle very large-scale computations efficiently.

- Transparent: Does not require a trusted setup phase, making the protocol more secure against certain attacks and more transparent.

- Argument of Knowledge: As with SNARKs, it's a proof that the prover knows certain information.

- Working Mechanism:
  - Arithmetic Circuits and Polynomials: The computation is transformed into a series of arithmetic statements and then into polynomial equations.
  - No Trusted Setup: Since there is no trusted setup, there are no secret parameters that could be compromised.
  - Proof Generation Using Cryptographic Hashing: STARKs use cryptographic hashing to create a proof. This involves creating a series of commitments to different parts of the computation.
  - Verification: The verifier checks these commitments against the final state of the computation.

---

---

# Setup Phase:

- ZK-SNARKs: Require a trusted setup phase. The credibility of the proof depends on the security of this setup. If the setup keys are compromised, it could potentially lead to fraudulent proofs.

- ZK-STARKs: Do not require a trusted setup. This removes the risk associated with the setup phase and makes STARKs more secure against certain types of attacks.

# Proof Size and Verification Time:

- ZK-SNARKs: Known for producing very small proof sizes and having fast verification times, which is beneficial for blockchain applications where space and speed are critical.

- ZK-STARKs: Generally result in larger proofs and can have longer verification times compared to SNARKs. However, they are still efficient and are getting more optimized over time.

# Quantum Resistance:

- ZK-SNARKs: Currently, they are not considered quantum-resistant. This means they could potentially be vulnerable to attacks by quantum computers in the future as they use elliptical curve cryptography.

- ZK-STARKs: Designed to be quantum-resistant, making them a more future-proof choice in the context of evolving quantum computing technologies as there is an argument that elliptical curve cryptography will be broken by quantum computing.

# Transparency and Complexity:

- ZK-SNARKs: The complexity of their construction and the need for a trusted setup can be seen as less transparent from a security standpoint.

- ZK-STARKs: Their lack of a trusted setup and quantum resistance adds to their transparency and security appeal, but the mathematical and computational concepts involved are more complex.

---
