# Firebase guides for DevDocs

[Firebase's guides](https://firebase.google.com/docs) (Authentication, Cloud Firestore, Cloud
Functions, Hosting and the rest) as a DevDocs doc pack: searchable and readable offline, and scraped
again every Monday.

**To add it:** in DevDocs (the [doc packs version](https://github.com/buggypather/devdocs/tree/main-custom-docs)),
open **Preferences → Doc packs**, paste `https://github.com/buggypather/devdocs-pack-firebase-guides/tree/pack`,
and click **Add**. Then tick **Firebase** in the list on the left and click **Apply**.

For the JavaScript SDK's API reference, add
[devdocs-pack-firebase](https://github.com/buggypather/devdocs-pack-firebase) too.

## How it's made

A GitHub Actions workflow (`.github/workflows/scrape.yml`) checks out the DevDocs fork, runs its
Firebase scraper (`lib/docs/scrapers/firebase.rb`) and publishes the result to the `pack` branch.
The scraper reads about four pages a second, to go easy on the site. To scrape now, open the
**Actions** tab, choose **Scrape Firebase guides** and click **Run workflow**.

## Licence

The guides are © Google LLC. Their text is licensed under the
[Creative Commons Attribution 4.0 License](https://creativecommons.org/licenses/by/4.0/) and their
code samples under the [Apache License 2.0](https://www.apache.org/licenses/LICENSE-2.0); each page
in the pack credits Google and links to its original. This repository's own files are under the MIT
licence.
