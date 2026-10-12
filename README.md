# Pivdenne Services Bot

A free Telegram directory of local services in Pivdenne, Ukraine.

**[Open the bot](https://t.me/PivdenneServicesBot)** · **[Contact the author](https://t.me/ID_BMI)**

Find local providers by service, category or phone number. This public repository contains documentation only. The application, collection scripts and operational configuration are maintained in a separate private repository.

**Telegraph help:** [English](https://telegra.ph/Pivdenne-Services--User-Guide-10-12) · [Русский](https://telegra.ph/Spravochnik-uslug-Pіvdennogo--instrukciya-10-12) · [Українська](https://telegra.ph/Dovіdnik-poslug-Pіvdennogo--іnstrukcіya-10-12)

## Using the bot

1. Open the bot and press **Start**. A Pivdenne welcome image and Ukrainian introduction appear, followed by the main menu with Search above categories. Use `/menu` to reopen the menu without the image.
2. Choose a category, or press **Search** and enter a service or phone number.
3. Contact the provider using the number in their listing. Confirm availability, prices and terms directly with them.
4. To offer a service, choose **Add your service**, select one service category, enter one Ukrainian phone number and a description, then confirm the preview. Local 10-digit numbers are converted to `+380`. The listing stays pending until the administrator approves it.

Search examples: `маникюр`, `ремонт`, `0631234567`, `+380631234567`. Search matches stored listing text and generated Ukrainian/Russian category tags. For example, уборка, прибирання and #прибирання_квартир find the cleaning category. This does not automatically translate every description or cover every synonym. Compact tags appear at the end of cards and are omitted from Excel/PDF/TXT.

Choose **Excel, PDF or TXT** below search results to receive all matching listings, including later result pages. The file includes categories, services, names, grouped phones and full descriptions. The current search/category filter is preserved. A **full directory** export in these formats is available only in the administrator panel. The Ukrainian @ID_BMI contact line appears in the Excel header, at the bottom of each PDF page and below the query in TXT. PDF uses the bot avatar, a single-line title, readable service cards and page numbers. The line is italic in Excel/PDF and plain text in TXT. Wait 30 seconds between successful downloads; if buttons expire or the bot restarts, repeat your search.

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

For user accounting and broadcasts, the bot stores Telegram chat/user identifiers, activity timestamps, subscription status and delivery status. Submitted listings and unfinished form steps are stored so moderation can survive a restart. Submission details and the submitter's Telegram ID are sent to the owner's moderation group. The owner can edit the category, phone and description, approve publication or reject the submission. Provider listings contain advertised phone numbers, service descriptions and names when explicitly stated. Search text is processed to return results; Telegram also processes messages under its own policies.

Bot credentials are kept in deployment settings rather than public documentation. The ingestion endpoint requires authentication. Administrative features check configured administrator identifiers. These controls reduce risk; they are not a guarantee of absolute security or an independent security audit. Private source code alone does not prove that a service is secure.

No password, Telegram login code or bank-card credentials are required to search the directory. Donations are optional. The directory does not verify professional credentials, endorse providers or guarantee work quality. Contact the author to report incorrect information or request review of a listing.

Contact the author for subscription and data-related requests. Telegram does not notify the bot when a user simply deletes their chat; blocking and unblocking can be detected from Telegram bot membership events. First-time interactions and those events are logged in the owner's designated group topic.

## Available features

Available: multilingual Telegraph help, category browsing, service/phone search, grouped provider phones, Ukrainian welcome and support text, administrator statistics and confirmed broadcasts, user-submitted listings with group moderation, user event logs in a separate group topic, Excel/PDF/TXT export of search results, administrator-only full-directory export, and manual contact entry through the same reviewed form.



## Submissions and moderation

- Choose one service category, then enter one complete Ukrainian phone and a 10–1800 character service description, then confirm the preview. Up to three requests may be pending per user. Publication requires administrator approval; users can cancel before submission.
- The administrator reviews the request in the **Service requests** group topic and can edit its category, phone or description before publishing or rejecting it.
- Users submit one category. Administrators can retain or assign up to three distinct categories during moderation; existing multi-category publications remain supported. Publication across moderator-selected categories is atomic. Publication checks the phone and category. An existing listing in the same category is updated even when its wording differs; a different category adds a service to the same contact.
- Drafts and pending requests persist in PostgreSQL. Repeated approval cannot publish a request twice.
- Requests remain saved if Telegram delivery is uncertain; the administrator can reopen pending requests in the designated moderation topic.

## My announcements

Choose **«Мої оголошення»** to see only your own approved submissions, ten at a time. A matching phone in the imported directory does not grant ownership. **«Змінити опис»** proposes a new description while preserving phone and categories; **«Зняти з публікації»** requests withdrawal with confirmation. Both go to the existing moderation topic. The current version remains visible until approval; rejection leaves it unchanged. Approved withdrawal hides that version from search and future reports while retaining history. Only one pending revision per announcement is allowed. Newer directory versions cannot be automatically overwritten or hidden by an older request.

## Editing published listings (administrator)

The configured administrator sees **«Редагувати»** below directory results, including imported and user-submitted listings. Description, grouped phones and category can be changed with a preview and explicit Save confirmation. Multiple numbers for the same provider remain together. The service title and other services of that contact are preserved. Existing phone/contact collisions are blocked rather than silently merged or duplicated. A stale preview cannot overwrite a newer listing.

Withdrawal also requires confirmation and hides the selected card from search, category counts and future exports while retaining its history. These buttons are unavailable to ordinary users, and callbacks check the administrator identity. Editing drafts and buttons expire after 30 minutes. Every committed operation records the administrator ID and before/after data, with a notification queued for the owner's log topic.

## Administrator workflow

The administrator panel is restricted to the configured owner. It provides unique-user statistics (total, active in the last 24 hours and seven days, and broadcast recipients), manual contact entry, all-directory Excel/PDF/TXT downloads, and confirmed broadcasts with delivery summaries. Manual entries use the same review workflow as user submissions.

In the moderation topic the owner can edit category, phone and description, then publish/update or reject. Separate logs report first interactions and bot block/unblock events. Ordinary chat deletion is not detectable. A broadcast requires preview and confirmation; ambiguous deliveries are marked for review rather than automatically resent.

## Troubleshooting

- No results: try a shorter word, Ukrainian/Russian wording or the complete phone number.
- Expired export button: repeat the search and use the buttons below the new results.
- Download cooldown: wait 30 seconds before choosing another format.
- Three requests already pending: wait for a moderation decision.
- Incorrect published contact: message [@ID_BMI](https://t.me/ID_BMI) with the phone and requested correction.

## Updates

See [the change log](CHANGELOG.md) for dated changes. Public documentation can be read without a GitHub account. Changes are maintained by the repository owner.

## Author and support

Author: **[@ID_BMI](https://t.me/ID_BMI)**. Questions, suggestions and corrections are welcome. Using the bot is free. Optional project support is available in the bot's **About and support** section.

© 2026 Pivdenne Services project.

