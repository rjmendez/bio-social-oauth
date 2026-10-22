# bio-social-oauth

Public OAuth client metadata for a personal Bluesky posting job (photos from my own iNaturalist observations).
atproto OAuth identifies a client by the URL of its metadata, so these files must be public:

- `<bot>/client-metadata.json`: one confidential client per bot (`private_key_jwt`, DPoP-bound tokens, its own minimal scope)
- `<bot>/jwks.json`: that client's PUBLIC signing key (the private key never leaves the machine that runs the bot)
- `callback.html`: the shared sign-in redirect page; it shows the address to paste back into the terminal and sends nothing anywhere

Bots: `poster/` (create posts + upload images).

The bots use the `bsky-oauth` library (private), a thin wrapper around Bluesky's official `@atproto/oauth-client-node`.
