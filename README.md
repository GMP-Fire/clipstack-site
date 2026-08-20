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

## The contact address

Both pages carry `support@clipstackapp.com`, chosen 2026-08-20.

**The address is on the pages before the domain exists**, deliberately: the
pages are otherwise finished and Apple needs the URL more than it needs the
mailbox on day one. It must receive mail before the app is submitted, because a
reviewer clicks it.

## The domain

`clipstackapp.com`, registered 2026-08-20 through Cloudflare.

`CNAME` was added only **after** the DNS was confirmed answering from outside
Cloudflare. GitHub Pages redirects the `github.io` address to whatever `CNAME`
names, so adding it first would have broken the working privacy URL — the one
thing here that must not break — for as long as the domain took to resolve.

The four apex A records point at GitHub's Pages addresses and are **DNS only,
not proxied**. Proxying them would put Cloudflare in front of GitHub, and GitHub
then cannot answer the challenge that issues the HTTPS certificate.
