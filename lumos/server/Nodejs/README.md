Steps to get Lumos Server running

1. Run `npm install` in this folder
2. Run `npm install -g nodemon`
3. Copy `nodemon.json~` (it may be hidden by the file browser) to `nodemon.json` and update variables
4. If running Linux, go into `node_modules/chrome-launcher/dist/chrome-launcher.js` and search for `--disable-setuid-sandbox`. Remove the section setting this flag.
5. Run `npm test`

If using HTTPS, you can use OpenSSL to generate keys:`openssl req -x509 -sha256 -nodes -days 365 -newkey rsa:2048 -keyout privateKey.key -out certificate.crt`
