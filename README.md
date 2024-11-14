# Secure Express App with Helmet.js

This project demonstrates how to enhance the security of an Express.js application using **Helmet.js**. It configures a range of HTTP headers to protect against common web vulnerabilities such as cross-site scripting (XSS), clickjacking, and more.

## Features

- **Helmet.js Security Enhancements**: Uses Helmet to set HTTP headers that secure the app.
- **HSTS (HTTP Strict Transport Security)**: Forces browsers to connect via HTTPS.
- **XSS Protection**: Mitigates cross-site scripting attacks by setting appropriate HTTP headers.
- **Content Security Policy (CSP)**: Controls where resources can be loaded from.
- **No-Cache Header**: Prevents browsers from caching sensitive information.

## Table of Contents

- [Installation](#installation)
- [Usage](#usage)
- [Security Features](#security-features)
- [License](#license)

## Installation

To run this project locally, follow these steps:

1. Clone the repository:

   ```bash
   git clone https://github.com/Azaam86msn/secureWithHelmet.git
   ```

2. Navigate to the project directory:

   ```bash
   cd secureWithHelmet
   ```

3. Install the required dependencies:

   ```bash
   npm install
   ```

4. Make sure you have **Node.js** and **npm** installed. You can download Node.js from [here](https://nodejs.org/).

## Usage

1. **Start the server**:

   ```bash
   npm start
   ```

   This will start the Express app, and the security headers configured with Helmet.js will be applied automatically.

2. **Access the app**:
   - Visit `http://localhost:3000` in your browser.

3. **View App Info**:
   - Visit `http://localhost:3000/app-info` to view the stack of middlewares and security headers applied to your app.

## Security Features

The following security features are configured in this app using Helmet.js:

1. **`helmet()`**: Uses default security headers such as `X-Content-Type-Options`, `X-Frame-Options`, `Strict-Transport-Security`, etc.
2. **`helmet.hsts()`**: Enforces HTTPS for all subdomains for 1 year.
3. **`helmet.noCache()`**: Prevents the browser from caching sensitive data.
4. **`helmet.xssFilter()`**: Helps prevent cross-site scripting (XSS) attacks.
5. **`helmet.contentSecurityPolicy()`**: Mitigates the risk of XSS by restricting the sources from which resources can be loaded.

### Example of Helmet.js Headers Applied:

- **Strict-Transport-Security (HSTS)**: Ensures all connections use HTTPS.
- **Content-Security-Policy (CSP)**: Controls where resources (like scripts) can be loaded from.
- **X-Content-Type-Options**: Prevents browsers from guessing the MIME type.
- **X-Frame-Options**: Prevents clickjacking attacks by disallowing the app to be framed.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---
