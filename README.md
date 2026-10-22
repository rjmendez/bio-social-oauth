# bio-social-oauth

Public OAuth client metadata for a personal Bluesky posting job (photos from my own iNaturalist observations).
atproto OAuth identifies a client by the URL of its metadata, so these files must be public:

- `client-metadata.json`: the client (confidential, `private_key_jwt`, DPoP-bound tokens)
- `jwks.json`: the client's PUBLIC signing key (the private key never leaves the machine that posts)
- `callback.html`: the sign-in redirect page; it shows the address to paste back into the terminal and sends nothing anywhere

The posting code lives in a private repository and uses Bluesky's official `@atproto/oauth-client-node`.
