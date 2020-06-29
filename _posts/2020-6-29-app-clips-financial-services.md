---
layout: post
title: Building Micro-Moments in Financial Services
---

iOS 14 offers a new, streamlined experience that’s perfectly suited for transactional financial services.

--- 

Experts often argue that the future of financial services is invisible and embedded - banking will be a persistent layer across all of our daily interactions, almost unnoticeable by the user. You could argue that prior to modern smartphones, the physical debit / credit card was this layer, unlocking goods and services wherever we went. Smartphones shifted this decentralised layer to the centralised mobile wallet, with platforms like Apple and Google Pay aggregating (and potentially commoditising) a user’s payment mechanisms. The only real barrier to adoption now is the contactless limit, however most transactions fall well below this threshold.

![Bank diagram](/images/banks-to-user.png)
*The shift from card-led banking relationships to mobile intermediated banking releationships.*

But financial services hasn’t yet achieved this *persistent yet invisible* status. Features and functionality remain locked within the financial institution’s siloed app and most bank’s would rather aggregated a user’s external accounts than play nicely with an open ecosystem. What if instead they decided to embrace and extend the technologies provided by mobile platforms, starting with app clips?

Here I‘ll discuss what exactly app clips are, the opportunity they provide, and potential use cases across financial services.

## App Clips Explained

[App clips](https://developer.apple.com/app-clips/) are an upcoming feature of iOS 14 (likely coming in September) that allow users to temporarily use an app and all native device features (e.g. Apple Pay, camera, geolocation). App clips must be less than 10mb and are downloaded once a user scans a code, opens a URL, or taps an NFC tag - perfect for quickly unlocking a scooter or paying for parking. 

![Clip flow](/images/app-clip-explained.png)
*Apple’s explanation of an app clip user flow.*

App clips are given a few special system privileges that make them perfect for customer acquisition. Firstly, they are automatically able to send notifications to users within the first 8 hours of download, perhaps used to provide an order update or prompt them to keep the app installed. Secondly, user data created in the app clip can be transferred to the full app once installed.

## Breaking Through

I continue to think lightweight app experiences can give companies a momentary opportunity to breakthrough the constant App Store noise and deliver micro-moments of customer delight without directly competing with peers. [Mobile wallets](https://murdo.xyz/mobile-wallets/) have been a dormant opportunity for a number of years; I hope app clips aren’t the next untapped opportunity. 

These opportunities have been particularly overlooked within financial services. Many banks had to be forced to use Apple Pay, transaction notifications still aren’t commonplace, and I distinctly remember a UK bank creating an entire marketing campaign about being the first to launch Touch ID nearly a year after the functionality was released.

## Payment Loops

Thinking specifically about payments, there are two key implications of app clips: 
1. **Achieving default status in a user’s mobile wallet card becomes even more critical.** Design guidelines for app clips prioritise rapid interactions and use of device defaults above all else. The highly transactional nature of the experience increases the likelihood that each usage will be linked to a payment.
2. **App clips could drive a viral loop of acquisition and growth for peer-to-peer payments.** App clips can be triggered using URLs or QR codes; payment request user flows could generate app clip-based experiences that users can share using their messaging platform of choice. The receiving user can complete the payment and, if the micro-moment delivered delight, receive an immediate nudge to create an account.

I think this second implication is of particular importance for apps like [Square Cash](https://cash.app) and PayPal but shouldn’t be overlooked by the digital challengers like Monzo and Revolut.

![Cash app](/images/square-clip.png)
*A mock-up of a potential Square Cash app clip.*

Payment apps like Square can leverage the simplicity and interactivity of app clips to further kickstart their acquisition loops. Banks and other financial institutions should seek to identify their own micro-moments to do the same.

## Building a Micro-Moment for App Clips

The lowest friction, most highly transactional user engagements are obvious initial targets for financial institutions to leverage app clips.

A few potential use cases I’ve identified include:
- A **stock trading app** allowing users to share major market movements or economic news stories, prompting users of the app clip to sign-up and receive a free stock.
- A **traditional bank or building society** adds an app clip to each Apple Maps branch location allowing users to schedule an advisor appointment. The app clip can then be leveraged for the initial customer documentation collation and verification. 
- **Car insurers** add car sharing functionality so users can temporarily add a new driver for a pre-determined amount of time. The insurance confirmation can be shared using an app clip; the temporary driver is prompted to use *Sign in with Apple* and photograph the vehicle before and after their trip. 

![Concept app clips](/images/concept-clips.png)

Each of these simplifies and enriches an existing user need and, for the stock trading and car insurance concepts, creates an acquisition loop where existing customers personally introduce the proposition to their friends and family.

## Embrace and Extend

App clips provide another touch-point for financial institutions to embrace and extend. Their historically conservative approaches to mobile platforms has led to siloed apps and basic Apple / Google Pay integration. They could truly become *persistent yet invisible* if they accepted reality - that the relationship is actually between the user and their device - and adopted the extensive tools available to them (app clips, Siri / Google Assistant, widgets, messaging apps, and mobile wallets to name a few). If the incumbents don’t, it’s only a matter of time until someone else does