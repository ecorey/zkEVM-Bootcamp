# Optimistic Rollups (Inoccent till Proven Guilty):

- Mechanism: They assume transactions are valid by default and only run computation, in case of a dispute. This approach optimistically accepts transactions and executes them without immediate verification.

- Fraud Proofs: They rely on fraud proofs to ensure transaction validity. If a fraudulent transaction is detected, a fraud proof can be submitted to the main Ethereum chain to challenge it.

- Finality: Transaction finality in Optimistic Rollups is slower because of the "challenge period" – a waiting time for users to submit fraud proofs if necessary. 1 week till finality, but faster to process

- Compatibility: They are generally more compatible with existing Ethereum smart contracts.

- EVM Compatible

- Based on Game Theory, economic incentive, and fraud proof

---

# ZK Rollups (Guilty till Proven Inoccent):

- Mechanism: They use Zero-Knowledge Proofs (specifically, SNARKs or STARKs) to validate all transactions in a bundle and submit a single proof to the Ethereum main chain. This proof attests to the correctness of every transaction in the bundle.

- Validity Proofs: Unlike Optimistic Rollups, ZK Rollups validate transaction data upfront using cryptographic proofs, meaning transactions are verified before being finalized on the main chain.

- Finality: They offer faster finality compared to Optimistic Rollups, as there's no need for a dispute window, but are slower to process.

- Complexity and Compatibility: Implementing ZK Rollups is technically more complex, and they might have compatibility issues with existing smart contracts.

- Less EVM comapatibility

- Based on math and cryptography through validity proof

- Matter Labs (zk-SNARKs) vs Starkware (zk-STARKs)
