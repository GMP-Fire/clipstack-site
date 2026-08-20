# ClipStack — the public pages

Three static pages, served by GitHub Pages:

- `index.html` — what the app is
- `privacy.html` — **the privacy policy Apple requires a URL for**
- `support.html` — **the support page Apple requires a URL for**

Everything on the privacy page was checked against the source before it was
written, not recalled: two network calls exist in the whole application
(`LPMetadataProvider` for link previews, one `URLSession` request for the update
check), the package has zero third-party dependencies, and there is no analytics
or crash-reporting code of any kind.

**If the app's behaviour changes, this page changes first.** A privacy policy
that describes an older version is worse than none.

## The one thing to fill in

Both pages carry `CONTACT-EMAIL-HERE`. Apple checks that the link works, so it
has to be a real address before submitting for review.
