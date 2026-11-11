# Public demo sanitization

This release uses an explicit allowlist of static demo and product-summary files.

- All displayed users, organizations, documents, metrics and requests are synthetic.
- Excluded backend code, databases, credentials, environment files, logs, original archives and repository history.
- Excluded native design exports, private design links, cloud storage links, local machine paths and account screenshots.
- File selection disabled. No uploads, external actions, model calls, analytics or browser persistence.
- Browser content policy blocks network connections and form submission from demo code.
- Inputs affect the visible walkthrough only and are discarded when the page is refreshed. Avoid entering real information.
- Hosting requests and repository attribution are governed by GitHub.

The static walkthrough demonstrates design intent. It is not a production service or security certification.
