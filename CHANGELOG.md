# Change log

## 13 October 2026

- Added an owner-reviewed winter window-servicing card after a live phone/category duplicate check; kept adjustment and seal replacement separate from unadvertised mosquito-screen services.

- Added two owner-reviewed cards from supplied images: window manufacturing with grouped phones, and home injections/infusions with the provider's doctor-prescription condition retained.
- Checked the chess club and flower-delivery contacts against the live directory and skipped existing entries.
- Added authenticated owner-only conditional imports that check the live phone/category before writing; preserved existing descriptions and grouped provider phones.
- Expanded explicit window/home-medical classification and verified 108 tests.

## 12 October 2026

- Added Telegram profile display names below user IDs in first-user and block/unblock event logs; kept names on one line and verified sender identity.

- Added the owner-selected Pivdenne welcome postcard and warm Ukrainian introduction on /start, followed by the main menu; /menu remains text-only.
- Added multipart photo delivery, included the image in the private application assets, updated all language guides and verified 105 tests.

- Linked @ID_BMI to the author’s Telegram profile in the final support section of all three user guides.

- Moved the Search button above category buttons in the main menu.

- Moved the project/author and support section to the end of the Ukrainian, Russian and English user guides.

- Added administrator-only editing buttons on published directory cards: description, grouped phones, category and confirmed withdrawal.
- Required a confirmation preview, preserved grouped-provider phone numbers and blocked existing-phone collisions and stale edits.
- Persisted before/after audit history with administrator identity and queued log-topic notifications; kept withdrawn cards out of search and future exports.
- Updated administrator instructions and public documentation; verified 103 tests.

- Added My announcements for the submitting Telegram user, description revisions and confirmed withdrawal through group moderation; the published version stays unchanged until approval.
- Retained history while excluding withdrawn versions from search, category counts and future exports; blocked older requests from changing newer shared-phone publications.
- Simplified new user submissions to one category, selected immediately before phone entry; preserved moderator multi-category support and existing publications.
- Updated all three language guides and public documentation; verified 100 tests.

- Added 1–3 distinct categories per submission, with optional additional choices, duplicate/max-three validation and atomic moderator publication across categories; preserved existing single-category requests.
- Added compact Ukrainian/Russian category hashtags to all cards and search matching; generated tags are excluded from all report formats.
- Updated multilingual help and verified all 97 tests.

- Localized all bot navigation, search prompts, result labels, submission category choices, export category labels, administrator panels and Telegram command descriptions into Ukrainian. Stored category identifiers and original provider text remain unchanged.
- Synchronized guide button names with the Ukrainian interface; verified 22 menu, submission, export and Telegram checks.

- Translated the main menu heading and empty-directory notice into Ukrainian.

- Rewrote Ukrainian, Russian and English Telegraph guides for the current search, result exports, submission workflow, phone matching, privacy and troubleshooting; removed outdated planned-feature statements.
- Updated public documentation for current administrator statistics, moderation, broadcasts and full-directory exports.

- Refined PDF styling with the bot avatar, a single-line directory title, larger service headings and phone numbers, and clearer spacing on every page.
- Fixed server installation of italic PDF fonts; placed the Ukrainian contact line in the Excel header, below the TXT search label and at the bottom of each PDF page.

- Added PDF and UTF-8 TXT downloads for filtered search results and administrator-only full-directory exports.
- Embedded Cyrillic fonts in PDF and added page numbers and a clickable italic Ukrainian contact footer on each page.
- Added the same footer in italic at the end of Excel files and as plain text at the end of TXT files.

- Added Excel downloads below search/category results, including all matching pages and preserving the current filter.
- Added a full directory Excel export restricted to the configured administrator.
- Added manual contact entry and a moderation topic shortcut to the administrator panel.
- Kept grouped phone numbers in one row, preserved full descriptions, and stored provider text as text rather than executable spreadsheet formulas.

- Added persistent user service submissions: category selection, normalized Ukrainian phone, description and confirmation preview.
- Added administrator moderation in a dedicated Telegram group topic: edit category/phone/description, publish or reject; repeated approval is idempotent.
- Prevented duplicate manual listings by matching phone and category before publication.
- Added first-user, block and unblock event logs in a separate group topic.

- Separated administrator and public command menus; removed internal command details from user help.

- Added Russian and English Telegraph help with a language selector, marked headings, bullet lists and bold highlights; retained Ukrainian help.

- Published editable Ukrainian help on Telegraph and added a Help button to the bot menu.

- Added Ukrainian welcome and project support text; updated the Telegram profile description.
- Reduced the category menu from 37 categories to 20 related navigation groups, with icons and two buttons per row.
- Combined veterinary care, grooming and pet boarding into Domestic animals.
- Restricted category listing counts to administrators; retained the administrator broadcast menu.
- Added explicit classification rules for reviewed cleaning, flower delivery, construction, pet boarding, skin lesion removal and installation advertisements.
- Kept results at 20 listings per page, with controls after the listings.
- Closed initial collection/review at the owner's request and removed scheduled automation. Complete historical coverage is not claimed.
- Created separate public English documentation while retaining the private application repository.

## Initial directory

- Imported reviewed text and image advertisements, using normalized Ukrainian phone numbers as the primary duplicate key.
- Preserved newer descriptions during historical imports and grouped multiple phone numbers when supported by the same provider advertisement.
- Established a separate Telegram bot, Railway service and database.

Upcoming features are listed in the README and are not described as released.

