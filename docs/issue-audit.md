# Contributor issue audit

Reviewed October 6, 2026. The initial 75 single-case tickets in this repository were compared with their referenced test suites and implementation. Existing coverage, incorrect assumptions and tiny duplicate scopes were consolidated into seven substantive tasks. Original issue bodies and links are retained on closed issues.

Examples of findings: The README already lists npm test; WebAuthn credential-limit and ownership cases, unknown contract fields, and transaction polling are already covered. PORT has no upper bound, and client/server payment type and timestamp representations differ.

| Issue                                                        | Reviewed task                                                         |
| ------------------------------------------------------------ | --------------------------------------------------------------------- |
| [#3](https://github.com/VelaPayments/vela-server/issues/3)   | Align the client NFC payload with the server payment contract         |
| [#17](https://github.com/VelaPayments/vela-server/issues/17) | Enforce valid TCP ports and cover environment validation boundaries   |
| [#27](https://github.com/VelaPayments/vela-server/issues/27) | Cover payment request normalization and persistence inputs            |
| [#37](https://github.com/VelaPayments/vela-server/issues/37) | Cover WebAuthn expired challenges and incomplete verification results |
| [#52](https://github.com/VelaPayments/vela-server/issues/52) | Cover Stellar memo byte limits and bounded polling failures           |
| [#64](https://github.com/VelaPayments/vela-server/issues/64) | Cover authorization failure ordering and event side effects           |
| [#73](https://github.com/VelaPayments/vela-server/issues/73) | Reject invalid JWT subject claims before user synchronization         |

These are preparation candidates only. Maintainers must confirm scope, dependencies and acceptance criteria before adding them to an approved Drips Wave Program. Completing a task does not guarantee a reward.
