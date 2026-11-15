# SmartFlowSocial

A scheduler for Nostr. Sign posts with your own signer. They go out on schedule, even while you are
offline.

You sign with a NIP-07 browser extension, such as Alby or nos2x, or with a NIP-46 remote signer,
such as Amber or nsecBunker. The server stores that signed event and publishes it later. The
signing key stays in the signer.

The hosted service is [smartflow.social](https://smartflow.social). The same source runs on a server
you operate. The license is the [Unlicense](https://unlicense.org). The app is `0.1.0-alpha.1`.

## Repositories

| Repository | What it does |
| --- | --- |
| [smartflowsocial](https://github.com/smartflowsocial/smartflowsocial) | A scheduler for Nostr. Sign each post with your own signer. The server stores that signed event and publishes it on schedule, even while you are offline. The same code runs hosted at smartflow.social and self-hosted. Public-domain alpha (Unlicense). |
| [smartflowsocial-publisher](https://github.com/smartflowsocial/smartflowsocial-publisher) | HTTP publisher for SmartFlowSocial. A Cloudflare Worker that accepts signed Nostr events and publishes them to relays with retries, circuit breakers, and rate limits. |
| [smartflowsocial-blastr](https://github.com/smartflowsocial/smartflowsocial-blastr) | Broadcast relay for SmartFlowSocial. Accepts signed Nostr events, gates them by pubkey entitlement and relay policy, and fans them out to a curated relay set. |
| [smartflowsocial-blossom](https://github.com/smartflowsocial/smartflowsocial-blossom) | Blossom media gateway for SmartFlowSocial. Authenticates uploads, verifies blob integrity, stores media in Cloudflare R2, and commits uploads back to SmartFlowSocial. |
| [smartflowsocial-cache-worker](https://github.com/smartflowsocial/smartflowsocial-cache-worker) | Primal-compatible cache API for SmartFlowSocial. A Cloudflare Worker that reads NostrMash first, falls back to Primal Cache, and returns Primal EVENT frames. |

Scheduling uses the app and the publisher. Blastr, Blossom, the cache worker, and
[NostrMash](https://github.com/nostrmash) are separate services. The marketing site at
[smartflow.social](https://smartflow.social) is published from this organization.

## Start

- [Use the hosted service](https://smartflow.social)
- [Clone the app and follow the self-host quickstart](https://github.com/smartflowsocial/smartflowsocial/blob/main/docs/getting-started/quickstart.md)
- [Report a security issue](https://github.com/smartflowsocial/smartflowsocial/blob/main/SECURITY.md)
- [Read the contributor guide](https://github.com/smartflowsocial/smartflowsocial/blob/main/CONTRIBUTING.md)
