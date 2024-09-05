# Blum Airdrop Bot

## Description

Blum Airdrop Bot automates interactions with the Blum airdrop platform. It includes functionalities to claim rewards, manage farming sessions, complete tasks, and play games automatically.

## Features

- **Claim Farm Reward**: Automatically claim rewards from farming activities.
- **Start Farming Session**: Begin a new farming session.
- **Auto Complete Tasks**: Automatically complete available tasks and claim rewards.
- **Auto Play and Claim Game Points**: Play games and claim game points automatically.
- **Claim Daily Reward**: Automatically claim daily rewards.

## Flows

### Default Flow

The **Default Flow** allows users to manually select specific tasks to perform. You can choose from:

1. **Claim Farm Reward**: Automatically claim farm rewards.
2. **Start Farming Session**: Begin a new farming session.
3. **Auto Complete Tasks**: Complete and claim rewards for available tasks.
4. **Auto Play and Claim Game Points**: Play games and claim game points.
5. **Claim Daily Reward**: Claim your daily reward.

After performing an action, you can choose to set up a cron job for regular automation or exit the bot if no automation is needed.

### One-time Flow

The **One-time Flow** runs a continuous sequence of tasks without manual intervention. This flow includes:

1. **Claim Farm Reward**: Claim the farm reward.
2. **Claim Daily Reward**: Claim the daily reward.
3. **Claim Game Points**: Play games and claim game points.
4. **Start Farming Session**: Begin a new farming session.

The One-time Flow will continuously execute these tasks, handling errors gracefully and attempting to restart after a specified delay (e.g., 12 hours) if issues arise.

## Setup

### Prerequisites

- [Node.js](https://nodejs.org/) (version 14 or later)
- [npm](https://www.npmjs.com/) (comes with Node.js)

### Installation

1. **Clone the repository:**

    ```bash
    git clone https://github.com/dante4rt/blum-airdrop-bot.git
    ```

2. **Navigate to the project directory:**

    ```bash
    cd blum-airdrop-bot
    ```

3. **Install dependencies:**

    ```bash
    npm install
    ```

### Configuration

1. **Create a `.env` file** in the root directory of the project.

2. **Add your `QUERY_ID` to the `.env` file**. Example format:

    ```env
    QUERY_ID=YOUR_QUERY_ID_VALUE_HERE
    ```

   - To find your `QUERY_ID`, follow these steps:
     1. Open [Web Telegram](https://web.telegram.org) in your browser.
     2. Open the [Blum Bot](https://t.me/BlumCryptoBot/app?startapp=ref_vTHusRz4j0).
     3. Open DevTools (right-click on the page and select "Inspect" or press `F12`).
     4. Go to the "Application" tab, then "Local Storage", and choose `https://telegram.blum.codes`.
     5. Find `QUERY_ID`, copy its value.

   - **Connection Issues?** If you can't open the Blum bot, you may need to use the following Chrome extension to bypass connection restrictions: [Ignore X-Frame-Headers](https://chromewebstore.google.com/detail/ignore-x-frame-headers/gleekbfjekiniecknbkamfmkohkpodhe).

## Running the Bot

To start the bot and choose a flow:

1. **Start the bot:**

    ```bash
    npm start
    ```

2. **Choose the script to run:**
   - **Default Flow**: Manually select tasks and optionally set up automation.
   - **One-time Flow**: Run a continuous sequence of tasks automatically.

## Donations

If you would like to support the development of this project, you can make a donation using the following addresses:

- **Solana**: `8Z2s41yUoMELEErJSqYE2LSiyJUGLPDKjJq7UwQC6pbc`
- **EVM**: `0xd4d1a60CFfd355A40234e5fb05741FB7a93d46F9`

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
