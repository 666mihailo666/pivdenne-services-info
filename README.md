# Pivdenne Services Bot

A free Telegram directory of local services in Pivdenne, Ukraine.

**[Open the bot](https://t.me/PivdenneServicesBot)** · **[Contact the author](https://t.me/ID_BMI)**

Find local providers by service, category or phone number. This public repository contains documentation only. The application, collection scripts and operational configuration are maintained in a separate private repository.

## Using the bot

1. Open the bot and press **Start**.
2. Choose a category, or press **Search** and enter a service or phone number.
3. Contact the provider using the number in their listing. Confirm availability, prices and terms directly with them.

Search examples: `маникюр`, `ремонт`, `0631234567`, `+380631234567`. Search currently matches words in stored listings; automatic translation and every synonym are not supported.

Categories use compact buttons with icons. Related services share a section: veterinary care, grooming and pet boarding are under **Domestic animals**. Up to 20 listings are shown per result page, followed by navigation buttons. Listing counts beside categories are visible only to administrators.

## Where the listings come from

The initial collection targeted available community announcements dated **1 December 2025 onward**. It included text and saved advertisement images. The owner has closed this collection stage. This date describes the intended period, not a claim that every message was captured or that every saved image was published. Complete historical coverage has not been verified. Scheduled collection and review jobs have been removed.

Readable phone numbers and services are checked before publication. Local Ukrainian numbers are normalized to `+380XXXXXXXXX`. Phone numbers are the primary duplicate key. Multiple numbers for the same provider in one advertisement can appear together; recommendations of different providers remain separate. Historical imports preserve existing newer names and descriptions. A valid phone format does not establish that a number is active or that a provider is reliable.

## How the system works

- **Windows collection scripts:** read available content through the owner's Viber Desktop interface. They require the owner's local computer and Viber session, not a visitor's device.
- **Local OCR and review:** extract text from saved advertisement images. Exact image hashes help avoid repeated review. OCR can make mistakes, so uncertain digits are not guessed.
- **Rule-based classification:** assigns explicitly advertised services to categories. Unclear material remains for review.
- **Protected ingestion service:** receives reviewed records over HTTPS with an authentication key.
- **Separate database:** stores listings, source records and bot administration data on Railway.
- **Telegram interface:** provides menus, search and controlled administrator broadcasts.

The bot does not ask you to install collection scripts or give access to your Viber account. The application source code, secrets, database exports and collected screenshots are not published here.

## Privacy and security

For user accounting and broadcasts, the bot stores Telegram chat/user identifiers, activity timestamps, subscription status and delivery status. Provider listings contain advertised phone numbers, service descriptions and names when explicitly stated. Search text is processed to return results; Telegram also processes messages under its own policies.

Bot credentials are kept in deployment settings rather than public documentation. The ingestion endpoint requires authentication. Administrative features check configured administrator identifiers. These controls reduce risk; they are not a guarantee of absolute security or an independent security audit. Private source code alone does not prove that a service is secure.

No password, Telegram login code or bank-card credentials are required to search the directory. Donations are optional. The directory does not verify professional credentials, endorse providers or guarantee work quality. Contact the author to report incorrect information or request review of a listing.

Use `/stop` to unsubscribe from broadcasts; `/start` subscribes again. Unsubscribing does not itself erase stored records. Contact the author for data-related requests. Telegram does not notify the bot when a user simply deletes their chat; a blocked bot may be detected when sending a message.

## Implemented and planned

Available: category browsing, service/phone search, grouped provider phones, Ukrainian welcome and support text, administrator statistics and confirmed broadcasts.

Planned, not yet available: user-submitted listings with group moderation, manual administrator contact entry, spreadsheet/PDF export, editable Telegraph help and event logging to a group topic. These will be documented as they are released.

## Updates

See [the change log](CHANGELOG.md) for dated changes. Public documentation can be read without a GitHub account. Changes are maintained by the repository owner.

## Author and support

Author: **[@ID_BMI](https://t.me/ID_BMI)**. Questions, suggestions and corrections are welcome. Using the bot is free. Optional project support is available in the bot's **About and support** section.

© 2026 Pivdenne Services project.

