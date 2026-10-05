# Vela Rebrand Implementation Plan

> **For agentic workers:** REQUIRED SUB-SKILL: Use superpowers:subagent-driven-development (recommended) or superpowers:executing-plans to implement this plan task-by-task. Steps use checkbox (`- [ ]`) syntax for tracking.

**Goal:** Align public-facing branding across the Vela mobile and server repositories.

**Architecture:** Update product copy, app display metadata, package metadata, and public documentation while preserving compatibility-sensitive NFC, deep-link, passkey RP ID, and SecureStore identifiers. Keep historical repository URLs and existing infrastructure identifiers intact.

**Tech Stack:** Expo 56, React Native, NestJS, Markdown, npm.

---

### Task 1: Rebrand the mobile app and public documentation

**Files:** Mobile README, Expo config, package metadata, in-app welcome and passkey display copy, current product/auth/NFC docs.

- [x] Replace user-facing Ding branding with Vela.
- [x] Set app display name to `Vela`, Expo slug and npm package name to `vela-payments`.
- [x] Preserve stable identifiers for installed clients and passkeys.
- [x] Check remaining brand references and review the diff.

### Task 2: Align server-facing public branding

**Files:** Server README, API docs, environment example, user-facing architecture/product documents.

- [x] Use Vela for visible product branding and API display names.
- [x] Keep the existing mobile GitHub URL and payment-request contract URI intact.
- [x] Check both repositories for stale visible branding and review diffs.

### Verification

- [x] Inspect `git diff` in both repositories and search public-facing files for old product branding.
- [x] Do not change payment, authentication, NFC, or persistence behavior.
