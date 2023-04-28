|![Namma Yatri](https://nammayatri.in/logos/nammaYatrilogo.svg)  | ![Open Challenge](https://nammayatri.in/logos/OpenChallenge.svg) |
|--|--|

## Namma Yatri - Open Challenge

### About Us
**Our solution for Namma Yatri's auto booking platform is to leverage the power of messaging platforms like WhatsApp, Telegram and Voice Assistants like Alexa, Google Assistant, Siri and WebApp to enable users to book a ride without the need for installing an app.**

### Submission Files

Presentation : [https://docs.google.com/presentation/d/1VxkloKyagqp-ytae3LLctNn9OrdKvqKUrJF21fx10TE/edit?usp=sharing](https://docs.google.com/presentation/d/1VxkloKyagqp-ytae3LLctNn9OrdKvqKUrJF21fx10TE/edit?usp=sharing)

WhatsApp Bot Link : [https://wa.me/9966960618?text=Hi](https://wa.me/9966960618?text=Hi)

Telegram Bot Link : [https://telegram.me/namma_yatri_bot](https://telegram.me/namma_yatri_bot)

Bot Source Code : [https://github.com/pranavms13/cab-bot](https://github.com/pranavms13/cab-bot)

Alexa Skill Source Code : [https://github.com/sandeepkumarmhere/nammayatri-alexa](https://github.com/sandeepkumarmhere/nammayatri-alexa)

WebApp Figma Design : [https://www.figma.com/file/37rT2ixrGNIMR1BQnKkNvc/Namma-Yatri?node-id=13-87&t=hURhnCf2BmOSXY5z-0](https://www.figma.com/file/37rT2ixrGNIMR1BQnKkNvc/Namma-Yatri?node-id=13-87&t=hURhnCf2BmOSXY5z-0)

## Flow Diagrams

### WhatsApp / Telegram Bot

Booking Auto Flow :

```mermaid
sequenceDiagram
User->>Bot: Hi or /start
Bot-->>User: Choose option : Book Auto, List Nearby Autos, About Us
User->>Bot: *Book Auto*
Bot-->>User: Share Pickup Location
User->>Bot: Pickup Lat, Long
Bot-->>User: Share Drop Location
User->>Bot: Drop Lat,Long
Bot->>Namma Yatri Server: User Details, Pickup Location, Drop Location
Namma Yatri Server-->>Bot: Ride Fair Details and Price Breakdown
Bot->>User: Ride Fair Details and Price Breakdown [Accept/ Cancel]
User->>Bot: Accept
Bot-->>Namma Yatri Server: Book Ride
Namma Yatri Server->>Bot: Driver Details and Ride OTP
Bot->>User: Driver Details and Ride OTP
```

Listing Nearby Drivers Flow :
```mermaid
sequenceDiagram
User->>Bot: Hi or /start
Bot-->>User: Choose option : Book Auto, List Nearby Autos, About Us
User->>Bot: *List Nearby Autos*
Bot-->>User: Share Pickup Location
User->>Bot: Pickup Lat, Long
Bot-->>Namma Yatri Server: User Details & Pickup Lat, Long
Namma Yatri Server->>Bot: Drivers Nearby Data
Bot->>User: Drivers Nearby Data
```
