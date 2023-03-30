![alt text](https://marketplace-widget-landing-page.netlify.app/image/banner.png)

# Overview
vIRL Marketplace Widget is the fastest and easiest community-driven tools to fully unlock the potential of your digital assets. Which just a few simple steps to set up and embed it to your website, a fully functional NFT marketplace is ready to use. There’s no better time than now to onboard the NFT space, and build a brand that is ready for immense growth ahead.


# USAGE
## Install by CDN (Plain HTML)
### 1. Place embed in the body of your HTML
```javascript
<html lang="en">
  <head>
      <link rel="stylesheet" 
        href="https://widget.virl.com/lib/css/main.css">
      <script 
        src="https://widget.virl.com/lib/js/main.js"></script>
  </head>

  <body>
      <wax-marketplace collection='your-collection-name'/>
  </body>
</html>
```

### 2. Done
Iframes are not supported
Use of iframes is not supported as it has security concerns. We are working on other ways to embed.

## Install by Package
### 1. Install dependency

```javascript
npm install @waxio/widget-marketplace
```

### 2. Import the script (ES6)
```javascript
import WaxMarketPlace from '@waxio/widget-marketplace';
```

### 3. Place embed
```javascript
<wax-marketplace collection='your-collection-name' itemPerPage={12}/>
```
### 4. Done!


# Options
Options have placed the element as attributes with a value. which looks as follows:

```javascript
<wax-marketplace collections="your-collection-ids" itemsperpage="12"> </wax-marketplace>
```

Most attributes are optional except for the collections

Attribute | Value | Default | Description
--- | --- | --- | ---
collection (required) | your-collection-id | None | Set your collection name so the API knows which collection to send to the embed.
itemperpages | number between 1 and 100 | 12 | Set a value on how the maximum amount of NFT's to show per pagecollection (required) | your-collection-id | None | Set your collection name so the API knows which collection to send to the embed.
isshowfilter | true/false | true | To display filter or not.
network | Supported chains/networks | mainnet | Mainnet is the default network you can set it to testnet if you want to try it out first.
redirect | None | None | The redirect URL is optional and is a way for you to interact with a transaction that happened see the redirect URL, default behavior is to redirect the user back to the URL it came from with no extra params.

## Redirect URL
If a redirect URL is placed as an attribute after the user has signed the transaction, the user will be redirected to the redirect URL after the transaction has been completed. we will include a couple of attributes in the query string to help you with the process
- tx: the transaction hash
- status: the status of the transaction (executed or failed) this still needs to be validated as a successfully executed
- sale: the sale id
- assets: the asset ids as "12345,12345,12345"

while we provide some useful data it's still up to you to validate that the transaction is valid and the user did make the sale. Everybody can write to a URL so be careful.
# Styling
```css
:root {
  /* the primary color */
  --wax-primary-color: #ff8474;

  /* the secondary color */
  --wax-secondary-color: #583d72;

  /* the font-family for all text */
  --wax-font-family: Arial, Helvetica, sans-serif;
  --wax-font-size--large: 18px;

  /* the default font size (best kept as is) */
  --wax-font-size: 14px;

  /* the smaller font size (best kept as is) */
  --wax-font-size--small: 12px;

  /* border radius for all roundings of inputs, buttons, images */
  --wax-radius: 8px;
  --wax-radius-small: 4px;

  /* border radius for card */
  --wax-radius-card: 8px;

  /* border color for buttons, inputs */
  --wax-border: #353945;

/* border color for the cards (if none use same color as card background) */
  --wax-border-card: #23262f;

  /* border thickness */
  --wax-border-size: 1px;

  /* color primary text */
  --wax-text-color: #fcfcfd;

  /* colors for non primary text */
  --wax-text-color-secondary: #777e90;

  /* filter button, buy button in the card (highlight) */
  --wax-btn-primary-bg: #23262f;
  --wax-btn-primary-border: #ff8474;
  --wax-btn-primary--active: #23262f;
  --wax-btn-primary-bg--active: #ff8474;
  --wax-btn-primary-border--active: #ff8474;

  /* backgrounds */
  /* list background in filters (schemas) */
  --wax-bg-list-item: #141416;

  /* all inputs (filters) */
  --wax-bg-inputs: #23262f;

  /* card background */
  --wax-bg-card: #23262f;
}
```