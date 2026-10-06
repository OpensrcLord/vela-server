# Wave preparation

Vela is an early open-source Stellar testnet payment prototype with an Expo client and NestJS backend. Its goal is contactless payment requests and self-custodial wallet access using NFC and passkeys.

## Submission description

> Vela explores NFC payment requests and passkey-protected wallets on Stellar testnet. The repositories contain native client flows, payload validation, wallet services, and backend authentication/payment modules. The web deployment is a UI preview. We are seeking contributors for shared protocol alignment, validation fixes, authentication failure handling and deterministic regression coverage. End-to-end transfers and native device behavior are not yet demonstrated, and client authentication integration remains incomplete.

Repositories:

- https://github.com/VelaPayments/vela-payments
- https://github.com/VelaPayments/vela-server
- Preview: https://vela-payments.vercel.app/

## Verified preparation

- Both repositories provide an MIT license; existing Expo attribution is retained in the client.
- Contributor setup, focused PR expectations and check commands are in CONTRIBUTING.md.
- The original single-case backlog was reviewed and consolidated into seven scoped candidates per repository. See [issue audit](issue-audit.md).
- Automated tests use mocks and fixtures. They establish regression coverage, not successful real-device payments or live transfer safety.
- Build-plan and architecture documents include planned functionality; the README project status records the current limits.

## Local verification — October 6, 2026

| Check               | Result                                                |
| ------------------- | ----------------------------------------------------- |
| Formatting and lint | Passed                                                |
| Type checking       | Passed                                                |
| Build               | Passed                                                |
| Unit tests          | 14 suites / 107 tests passed                          |
| End-to-end tests    | 4 suites / 29 tests passed with mocked infrastructure |

These results were recorded during preparation. Check the current GitHub Actions run for the latest remote result.

## First candidate set

Start with a manageable subset after maintainers confirm scope and dependencies. `wave-candidate` is a preparation label only; it does not enroll an issue in Drips.

- #17: TCP port validation — concrete configuration defect with boundary tests.
- #64: Authorization failure ordering — persistence/event regression coverage.
- #52: Memo byte limits and polling failures — deterministic provider mocks.

The shared protocol alignment task #3 requires coordination with the mobile maintainer. WebAuthn and JWT tasks should be reviewed by someone familiar with the authentication model.

## Apply through Drips

1. Log into [Drips Wave](https://www.drips.network/wave) with the maintainer GitHub account.
2. In Maintainers → Orgs and Repos, install the Drips GitHub app on VelaPayments and select these public repositories.
3. Apply to the Stellar program, respecting the application limits displayed in the app, and use the description above.
4. Wait for organizer approval. Repository approval is not guaranteed and has not been verified for Vela.
5. Only after approval, add a small reviewed issue set to the program and set honest complexity values. Review applications promptly and verify PRs against their acceptance criteria.

The project remains a testnet prototype. Production hosting does not make it a mainnet wallet. The RP domain, storage identifiers, NFC MIME type and app scheme migration remain deferred. No contributor should bypass these compatibility decisions to make a demo appear complete.

References: [maintainer participation](https://docs.drips.network/wave/maintainers/participating-in-a-wave/), [program rules](https://docs.drips.network/wave/terms-and-rules/), [Stellar program](https://www.drips.network/wave/stellar).
