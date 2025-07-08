# Gift Carder for Telegram

This script is designed for automatically searching for and purchasing gifts in Telegram. The script authenticates the user, looks for available gifts, and automatically buys them if they meet the specified criteria.

## Functionality Overview

1. **Telegram Authorization**:
   - The script asks for the phone number and two-factor authentication code in Telegram.
   - After successful authentication, the script continues its operation.

2. **Gift Search**:
   - The script periodically checks for new gifts available in Telegram.
   - It filters the available gifts and checks if they meet the required conditions (e.g., price and availability).

3. **Automatic Purchase**:
   - When suitable gifts are found, the script automatically buys them using the Telegram API.

4. **Background Operation**:
   - The script runs continuously in the background, without requiring user intervention.
   - It continues searching for gifts and buying them if they meet the conditions.

## Installation and Setup

1. Clone the repository:

    ```bash
    git clone https://github.com/tinequara/lovlyapodarkov.git
    cd lovlyapodarkov
    ```

2. Install dependencies:

    ```bash
    npm install
    ```

3. Go to [my.telegram.org](https://my.telegram.org/auth) without a VPN, enter your phone number, then the confirmation code. Select **API Development tools**, create an app title, short name, and fill in the required fields, then click "Next". You will be given your `API_ID` and `API_HASH` that you will use in the next step.

4. Modify the `.env` file with the following settings:

    ```
    API_ID=your_api_id
    API_HASH=your_api_hash
    API_SESSION=your_api_session
    MAXIMUM_PRICE=100  # Maximum price for a gift
    MAXIMUM_SUPPLY=10  # Maximum number of available gifts for purchase
    ```

    **Note**: To obtain `API_ID` and `API_HASH`, create an app at [Telegram API](https://my.telegram.org/auth).

## How to Use

1. Run the script using `startscript.bat`.
2. Enter the password for the script, which you can purchase/get/exchange from [@beszpredel](https://t.me/beszpredel).
3. Enter your phone number with a "+" symbol (e.g., +1234567890).
4. Enter the two-factor authentication code sent to your Telegram.
5. Enter the 2FA password if required for your account. This is necessary for the framework to interact with your account.
6. The script will now run in the background, periodically checking for new gifts and automatically purchasing them.

## Notes

- The script uses the `gramjs` library to interact with the Telegram API.
- To work with the Telegram API, you need to obtain your `API_ID` and `API_HASH`.
- The script runs in the background without requiring constant monitoring.

## License

This project is licensed under the MIT License - see [LICENSE](LICENSE) for more details.
