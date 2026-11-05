# 🎂 Faith Cakes & Bakes: ordering app

A mobile-friendly ordering app for a home bakery. Customers browse the menu, design a custom cake, pay an advance by UPI, and send the order to the shop on WhatsApp.

It's a single web page with no server or database, so it runs for free on **GitHub Pages**.

## Features

- **Menu** with categories, animated item cards and a **festival specials** banner
- **Custom cake builder**: size, tiers, flavour, filling, frosting and extras, with a live price
- **What to write on the cake** for every cake in the order
- **🌱 Eggless** option with an extra charge
- **📷 Reference photo**: customers add a picture of the design they want
- **Delivery charges by area or pincode**
- **UPI payment** with advance and balance: a pay-by-app button, a QR code and a transaction ID field
- **Orders sent on WhatsApp** with an order ID, or by email
- **🔁 Order again**, and the customer's details are remembered on their phone
- **📊 Google Sheet order log** (optional)
- **⚙️ Shop settings** locked with a PIN: menu, prices, WhatsApp number, UPI ID, delivery areas and more
- Works offline and can be **added to the phone's home screen** like an app

## Put it online with GitHub Pages

1. On GitHub, open this repository and go to **Settings → Pages**.
2. Under **Build and deployment**, set **Source** to **Deploy from a branch**.
3. Choose branch **`main`** and folder **`/ (root)`**, then click **Save**.
4. After a minute or two, the page shows the link to your app, for example:
   `https://YOUR-USERNAME.github.io/REPOSITORY-NAME/`

Share that link with customers on WhatsApp, Instagram or a QR code at the shop.

## First-time setup (shop owner)

1. Open the app link on your phone.
2. Tap **⚙️** (top right) and create a **PIN**.
3. Fill in:
   - **WhatsApp number**, where orders arrive. Tap **Send test message** to check it.
   - **UPI ID** and the **advance %**
   - **Delivery areas** with their pincodes and fees
   - **Menu items and prices**. Tap ☆ to feature an item in the specials.
   - **Shop details**: address, hours and ordering policy
4. Tap **Save changes**.

### Publish your changes to customers

Settings are saved only on the phone where you make them. To show them to customers:

1. In ⚙️ Shop settings, tap **Download updated app**. This saves a new `index.html`.
2. On GitHub, open this repository, then **Add file → Upload files**.
3. Upload the downloaded `index.html` and click **Commit changes**.
4. The live app updates within a couple of minutes.

You can also edit the `DEFAULTS` block near the bottom of `index.html` directly on GitHub (click the file, then the ✏️ pencil).

## Optional: Google Sheet order log

In ⚙️ Shop settings, open **📊 Order log → How to set it up**. It walks you through connecting a Google Sheet so every order is saved as a row. It takes about 5 minutes.

## Good to know

- **Payments:** the app can't check whether a UPI payment arrived. Match the transaction ID in your UPI app before confirming an order. If Google Pay blocks the pay button for a personal UPI ID, customers can scan the QR code instead, or you can use a business UPI ID.
- **PIN:** keeps customers out of the settings screen, but it isn't strong security. If you forget it, edit `index.html`, set `pinHash: ""`, and you'll be asked to create a new one.
- **Photos:** WhatsApp can't attach a photo from a link, so customers send the design photo as a second message right after the order.

## Files

| File | What it is |
|---|---|
| `index.html` | The whole app: page, styles, code and your shop settings |
| `manifest.webmanifest` | Lets phones install the app on the home screen |
| `sw.js` | Offline support |
| `icons/` | App icons |
| `.nojekyll` | Tells GitHub Pages to serve the files as they are |
