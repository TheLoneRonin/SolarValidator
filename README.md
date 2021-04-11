# Solar Validator

## Overview

- Validator issues `SOLAR` tokens. These tokens are minted in parity with the amount of new blocks on Solana Mainnet (10 `SOLAR` per block).

- Scanners (that use `SolarweaveBridge`) submit their Arweave address to the Validator using the Solana Contract.

- Upon uploading a new block. Said scanner receives a reward for uploading the block to Arweave.

    - The first address to upload said new block, receives the reward.

- Validator verifies that said address uploaded said block. Rewards the scanner with `SOLAR` tokens.

- The validator does a full chain scan of Solana Blocks on Arweave periodically

    - On a more frequent basis, it will scan the last 100,000 blocks.

    - Upon identifying a missing block, it adds said block to a list for scanners to review on the Smart Contract.

    - Posts a reward for identifying the missing block. This reward is larger (50 `SOLAR` tokens) than uploading newer blocks.