> **⚠️ THIS REPOSITORY IS OUTDATED**
>
> This project is no longer maintained and should not be used in production.
>  
> Please visit the new repository here: **[HYPERSWAP-TOKEN-LIST](https://github.com/HyperSwap-Labs/hyperswap-token-list)**.

# HyperSwap Token List

This repository is dedicated to the list of tokens registered on the HyperSwap exchange. It serves as the central place where tokens can be added, allowing them to be displayed and used on the DApp, including showing their logos.
If you're not familiar with github pull request system you can fill this form and an issue will be created : [List your token easily here](https://tally.so/r/3Nd5BN)

### Requirements

In order to be listed, you should meet at least the following conditions:

1. Transparency and Documentation
- The smart contract must be publicly accessible or accompanied by detailed technical documentation (e.g., whitepaper, GitHub repo, or official website).

- The token must be listed on reputable tracking platforms such as CoinGecko or DexScreener to improve visibility and trust.

- A token logo must be provided in high resolution (SVG or PNG preferred) for proper display across platforms.

2. Liquidity Requirements
- The associated liquidity pool must maintain a minimum Total Value Locked (TVL) of $10,000, ensuring baseline capital efficiency and market depth.

3. Community and Communication
- Projects should have an active and growing community on at least one major platform: Telegram, Discord, or X (Twitter).

- A minimum of 300 followers on X (Twitter) is required.

- Teams must provide transparent information about the token’s utility, tokenomics, and overall purpose.

- Maintaining consistent, honest communication with users and responding to community inquiries is expected to build trust and credibility.

## How to Add a Token

If you want to add a new token to the list, follow these steps:

1. **Fork and Clone the Repository**  
   Fork the repository then Clone it to your local machine:
   ```bash
   git clone https://github.com/HyperSwapX/hyperswap-token-list.git
   cd hyperswap-token-list
   ```
2. Modify the `tokens.json` File
   Open the `tokens.json` file in a text editor and add your token's information. Make sure to follow the existing format in the file.
   
   Here is the Token object model you must use to add your token to the list:
   ```typescript
   interface Token {
     name: string;           // Name of the token
     decimals: number;       // Number of decimals for the token
     symbol: string;         // Symbol of the token
     address: string;        // Contract address on the blockchain
     chainId: number;        // Chain ID where the token is deployed
     logoURI: string;        // URL of the token's logo image
     tags: string[];         // Tags associated with the token
   }
   ```
   ℹ️ Note: You can add the `websiteUrl`, `telegramUrl`, and `discordUrl` attributes, which are optional but will provide additional information about your project or token.

   The logo must meet the following criteria:
   - Size: 125x125
   - Please upload your image on the PR (any link will not be accepted).

   Here is an example with USDC token
   ```json
   
      {
            "name": "USD Circle",
            "decimals": 6,
            "symbol": "USDC",
            "address": "0x....",
            "chainId": 998,
            "logoURI": "https://assets.coingecko.com/coins/images/6319/standard/usdc.png",
            "tags": [
                "tokenv1"
            ]
        },
     
   ```

4. Submit a Pull Request
   After adding your token, commit your changes and push them to your forked repository. Then, create a pull request to the main branch of the `hyperswap-token-list` repository.
   ```bash
   git add tokens.json
   git commit -m "chore: add [Your Token Name] to tokens list"
   git push origin main
   ```
   Go to the repository on GitHub and click on "New Pull Request" to submit your changes.

## Pull Request Review

All pull requests will be reviewed and processed to ensure they follow the required format and standards. Once approved, your token will be added to the list on the DApp, making it available for users to interact with.

By adding your token to this list, it will be registered on the HyperSwap exchange, and its logo will be displayed alongside other tokens, enhancing its visibility.

We appreciate your contributions!

