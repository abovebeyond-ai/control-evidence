# Evidence of the control gateway

What the gateway of Above Beyond's Elixir hands wrote, mirrored daily so anyone can verify
it without asking us: the records per agent (`store/*.jsonl`), what sits beside each record
(`store/<agent>/{premises,action,outcome}/<step>.json`), the hardware attestation
(`store/attestation.json`, when the gateway attests on hardware), the signed checkpoints,
the anchor receipts (DigiCert RFC 3161 and Hedera), and `coverage.json`.

Issuer `https://portal.abovebeyond.ai/elixir/control`; public key `8d8c2fdc663a379290f681aa71cec120512e6b5b3d7121f578cd7964784c6f31`, resolvable through the
did:webvh log at https://abovebeyond.ai/.well-known/did.jsonl.

To verify, with the tooling at https://github.com/abovebeyond-ai/control:

    verify --store store --key 8d8c2fdc663a379290f681aa71cec120512e6b5b3d7121f578cd7964784c6f31 --anchors anchors --offline --attestation store/attestation.json

The standard is the Advanced AI Society's Proof-of-Control, draft v0.1. The conformance
statement is in the control repository under `conformance/`. This mirror is a copy; the
checkpoints and the anchors are what bind it.
