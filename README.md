# Notifi Instant Subscription Page

A minimal website that streamlines subscribing to a Notifi topic.

---

## Design Goals

- From a single URL (the URL of the website plus the appropriate parameters in the query string),
  you should be able to get a Notifi subscription card that you can link your wallet to and sign
  up for notifications for.
  - Essentially, it is the simplest possible integration of the
    [`notifi-react-card`](https://github.com/notifi-network/notifi-sdk-ts/tree/main/packages/notifi-react-card)
    React component.
  - The query string specifies the dapp ID, the card ID, the chain name, and any other necessary parameters
    (e.g. `https://subscribe.notifi.network/?dapp=123abc&card=abc123&chain=ETHEREUM`).
- We would like to be able to generate links to it from the [Notifi Admin Portal](https://admin.notifi.network),
  allowing Dapp owners to immediately subscribe to events that they create, without having to
  load a website with their Notifi card integrated. (This is especially important as the instructions
  for how to properly integrate with a Web3 signing interface is slightly different for each chain).
- We would also like to offer this site as an end-user subscription portal for basic use,
  so that Dapp owners can simply share this link directly with new customers (e.g. as a QR code
  on a business card).
