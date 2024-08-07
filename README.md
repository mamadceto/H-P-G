# Hamster Kombat Key/Promo Generator

This project is a web-based key generator designed specifically for the "Hamster" game on Telegram. In the "Hamster" game, players typically need to participate in various mini-games within the playground to earn keys. This project allows users to bypass the gameplay and generate keys directly through the interface.

## Features

- **Select Key Type:** Users can choose a key type from a dropdown menu.
- **Generate Keys:** Users can generate keys by clicking a button.
- **Responsive Design:** The layout is responsive and adjusts to different screen sizes.

## Demo

[Link to live demo](https://mamadceto.github.io/H-P-G/)

## Technologies Used

- HTML
- CSS
- JavaScript

## Installation

To run this project locally, follow these steps:

1. Clone the repository:
    ```sh
    git clone https://github.com/mamadceto/H-P-G.git
    ```
2. Navigate to the project directory:
    ```sh
    cd H-P-G
    ```
3. Open `index.html` in your browser:
    ```sh
    open index.html
    ```

## Usage

1. Open the `index.html` file in your web browser.
2. Select a key type from the dropdown menu.
3. Click the "Generate Keys" button to generate keys.

## API Usage

This project uses several APIs to handle the key generation process. Below are the details of these APIs and how they are used:

1. **Login Client API**
    - **Endpoint:** `https://api.gamepromo.io/promo/login-client`
    - **Method:** `POST`
    - **Description:** Logs in a client using the `appToken` and `clientId`, and returns a `clientToken`.
    - **Request Body:**
        ```json
        {
            "appToken": "your-app-token",
            "clientId": "generated-client-id",
            "clientOrigin": "deviceid"
        }
        ```
    - **Response:**
        ```json
        {
            "clientToken": "generated-client-token"
        }
        ```

2. **Register Event API**
    - **Endpoint:** `https://api.gamepromo.io/promo/register-event`
    - **Method:** `POST`
    - **Description:** Emulates progress by registering an event using the `clientToken` and `promoId`.
    - **Request Body:**
        ```json
        {
            "promoId": "your-promo-id",
            "eventId": "generated-event-id",
            "eventOrigin": "undefined"
        }
        ```
    - **Response:**
        ```json
        {
            "hasCode": true
        }
        ```

3. **Create Code API**
    - **Endpoint:** `https://api.gamepromo.io/promo/create-code`
    - **Method:** `POST`
    - **Description:** Generates a key using the `clientToken` and `promoId`.
    - **Request Body:**
        ```json
        {
            "promoId": "your-promo-id"
        }
        ```
    - **Response:**
        ```json
        {
            "promoCode": "generated-promo-code"
        }
        ```


## Customization

To customize the project, you can modify the HTML, CSS, and JavaScript files:

- **HTML (`index.html`)**: Modify the structure and content of the web page.
- **CSS (`styles.css`)**: Change the styles, colors, and layout.
- **JavaScript (`script.js`)**: Add or modify the functionality of the key generation process.

## Contact

For any inquiries or feedback, please contact [@mmdceto](https://t.me/mmdceto).
