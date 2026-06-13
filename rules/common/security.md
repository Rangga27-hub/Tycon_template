# Common: Security

- Never commit secrets, keys, or tokens. Use env vars; provide `.env.example`.
- Server-only secrets never imported into client code/bundles.
- Validate & sanitize all external input.
- Parameterize DB queries; enable row-level security where applicable.
- Least privilege for API keys and service accounts.
- Don't log sensitive data (PII, tokens, full payment details).
