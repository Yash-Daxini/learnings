## Payment App Working

### Apple Pay: 
- One of the secure model. In apple pay model when first card added during setup, apple must authenticate card directly with issuing bank or card network like VISA or master card. Apple follows "on device tokenization model". Real card number is encrypted and sent and the bank validates the card.

- After validation process bank or card network issues a device account number or DAN, which apple securely store on device's "secure element". Secure Element is dedicated chip that ensures the protection of sensitive information. Once the token is generated its link to a device. It means it is useless without device. DAN and device specific token is used for all future transactions instead of original card number. Only DAN (tokenize) version is used for transactions. Apple pay design to work even without internet Ex: Tap to pay offline, so device must have everything locally. Achive network less payment via NFC.

- Only once real card goes to the bank at setup, after that payments happens through secure proxy DAN. So even server of e-commerce site or bank the only thing they see is DAN. So even if someone hacks the server, they will not get real card number. They get only DAN which useless without original device.

### NFC: 
- Near field communication. It is a short range wireless technology that allows two devices to communicate when they are within a few centimeters of each other. NFC is commonly used for contactless payments, where a user can tap their smartphone or smart card on a payment terminal to complete a transaction. NFC operates at 13.56 MHz and can transfer data at speeds of up to 424 kbit/s.

### Google Pay: 
- When you add your card to Google Pay, your credit card details sent to google pay secure servers in encyrpted form. Google communicates with banks or bank networks (like Visa or Mastercard) to verify the card. After verification google generates payment token. Also called virtual account number link to your card. But store in the cloud not on device. So instead of real card token is used during the payments. When make payment requests, phone requests a fresh token from google servers. This token is sent to a e-commerce server and that server forwards it to bank, bank matches the payment token and approves the transaction.

- Apple pay is secure and google pay is flexible.
