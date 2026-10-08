# Sorogate

<img src="https://raw.githubusercontent.com/Sorogate/sorogate/main/docs/brand/social-preview.png" alt="A policy of three conditions worked out in order: it stops at the second and answers Denied with the reason BelowMinimum." width="640">

Reusable **access policies** for Stellar, stored in a Soroban contract and evaluated the same way from other
contracts and from TypeScript. A policy is a short list of conditions about an address (it holds at least some
of a token, it holds at least some items of a collection, the ledger time is inside a window). All of them must
hold, and a denial says why.

**Try it without installing anything:** the [playground](https://sorogate.github.io/sorogate/) works a policy out
in your browser, with no wallet and no network calls.

| Repository | The question it answers | Status |
| --- | --- | --- |
| [sorogate](https://github.com/Sorogate/sorogate) | "Does this address satisfy this policy right now?" The contract, the shared specification and test vectors, a TypeScript model and SDK, and the playground. | Early. A public development deployment on Testnet, described in [`docs/DEPLOYMENT.md`](https://github.com/Sorogate/sorogate/blob/main/docs/DEPLOYMENT.md). |
| [example-consumer](https://github.com/Sorogate/example-consumer) | "How does my own contract use a policy?" The smallest contract that depends on one: a gate that authenticates the caller, asks the policy, and enforces the answer. | An example, with tests and a recorded Testnet run. Not a product. |

## Where this stands

These projects are new. **Testnet only. Not audited. Not for real value.** Each repository says what has been
checked by a real run and what has not, with the evidence kept in `docs/evidence`. So far nobody outside the
project has built on it. Sorogate does not prove who is calling (a contract that acts on its answer must also
authenticate the caller), and it is not affiliated with or endorsed by the Stellar Development Foundation.

## Contributing

[`CONTRIBUTING.md`](https://github.com/Sorogate/sorogate/blob/main/CONTRIBUTING.md) has the setup and the pull
request flow, and [`ISSUES_BACKLOG.md`](https://github.com/Sorogate/sorogate/blob/main/ISSUES_BACKLOG.md) lists
scoped work for new contributors. Open an issue before starting anything large. Security problems go through
private vulnerability reporting, not a public issue (see [`SECURITY.md`](https://github.com/Sorogate/.github/blob/main/SECURITY.md)).
