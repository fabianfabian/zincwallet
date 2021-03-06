zincwallet
----------

A [BIP32](https://en.bitcoin.it/wiki/BIP_0032) deterministic bitcoin wallet for iOS

zincwallet is designed to be the most secure and user friendly bitcoin wallet for iOS. It is a "deterministic" wallet, meaning that all the bitcoin addresses and private keys are generated from a single "seed". If you know the seed, you can recreate the entire wallet including all balances and transaction history. This allows for a single convenient backup that will work forever.

Wallet seeds are securely stored on the iOS keychain, and never leave the device. They are never stored on any server. Your private keys are generated from your seed as needed and then immediately wiped from memory. Additionally, iOS keychain data persists even if the app is deleted. If you accidentally delete zincwallet and reinstall it, your wallet will be automatically recreated from the seed stored on the keychain. (Be sure to do a factory reset if you sell or give away your device!)

The seed is also encoded into a non-sense english phrase, which is your "wallet backup phrase". Never let anyone see your backup phrase or they will have access to your wallet. Write it down and store it in a safe place. In the event your device is damaged or lost you can restore your wallet on a new device using your backup phrase. Be sure to enable a passcode on your device and use [remote erase](http://www.apple.com/icloud/find-my-iphone.html#activation-lock) if it is lost or stolen. Future versions of zincwallet will also include a secondary passcode on the app itself.

Apple's app store rules currently prohibit apps that tansfer bitcoins. The app store build of zincwallet excludes this functionality and instead launches a mobile safari web app to send transactions. (the web app is entirely client side javascript, and sends transactions through the excellent blockchain.info web service. zincwallet.com will be launching it's own web service soon) No private keys or other sensitive data are transmitted to the web app, only public bitcoin transactions. If you build zincwallet from source without the app store build flag, or otherwise obtain a non-app store build, this restriction is removed.

zincwallet uses "simplified payment verification" or [SPV](https://en.bitcoin.it/wiki/Thin_Client_Security#Header-Only_Clients) mode for fast performance in a mobile environment.

Future planned features include support for [BIP70](https://en.bitcoin.it/wiki/BIP_0070) payment protocol, support for Electrum wallets, BIP32 [serialized](https://en.bitcoin.it/wiki/BIP_0032#Serialization_format) wallet import and export and watch only wallets, more detailed transaction information, support for mBTC and µBTC denominations, and exchange rates for multiple legacy national currencies.

zincwallet is open source and available under the terms of the MIT license. Source code is available at https://github.com/voisine/zincwallet
