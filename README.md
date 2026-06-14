# Ceramic

Ceramic is a decentralized data network built on a protocol for mutable event streams anchored to Ethereum blockchain. It enables composable, verifiable data infrastructure for Web3 applications — supporting 400+ apps, 10 million streams, and 350 million events across the network.

## Overview

Ceramic organizes data as cryptographically signed events chained into streams. Decentralized Identifiers (DIDs) serve as the identity layer, letting users control their own data without central authorities. Global event ordering is achieved by periodically anchoring Merkle tree roots to Ethereum via the Ceramic Anchor Service (CAS).

## APIs

- **Ceramic HTTP API** — REST API for streams, events, interests, feed, peers, and node configuration (OpenAPI 3.0, v0.58.0)
  - `POST /ceramic/events` — Publish a new event to the network
  - `GET /ceramic/events/{event_id}` — Retrieve an event by CID
  - `GET /ceramic/streams/{stream_id}` — Get current stream state
  - `POST /ceramic/interests` — Register interest in a data model/stream
  - `GET /ceramic/feed/events` — Poll the ordered event feed with resume token support
  - `GET /ceramic/feed/resumeToken` — Get current highwater mark for the event feed
  - `GET /ceramic/config/network` — Get network info
  - `GET /ceramic/liveness` — Node health check
  - `GET /ceramic/version` — Node version
  - `GET /ceramic/peers` — List connected peers
  - `POST /ceramic/peers` — Connect to a peer

## Developer Resources

- **Documentation**: https://developers.ceramic.network/
- **GitHub**: https://github.com/ceramicnetwork
- **Discord**: https://chat.ceramic.network/
- **Forum**: https://forum.ceramic.network/
- **Blog**: https://blog.ceramic.network/
- **Twitter**: https://twitter.com/ceramicnetwork

## Infrastructure

Ceramic is a self-hosted protocol. Operators run their own ceramic-one Rust daemon (default port 5101) plus js-ceramic, Postgres, and an Ethereum RPC provider for anchoring. Estimated costs range from ~$106/month for small apps to ~$967/month for high-traffic deployments.

## Legal

- **Terms of Service**: https://ceramic.network/terms-of-service
- **Privacy Policy**: https://ceramic.network/privacy-policy

---

Maintained by [API Evangelist](https://apievangelist.com)
