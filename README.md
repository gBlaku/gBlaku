# Gent Blaku

Software Engineer in NYC.

Leading federal agency migrations off Sybase stored procedures to PostgreSQL and service APIs,
building the conversion tooling every engineering team now uses. Automated production
support with MCP orchestration across the database, ServiceNow and Jira, so routine tickets
resolve without a developer touching them.

## Polywhales

Market intelligence over Polymarket, polling every tradeable market since October 2025. As of
August 2026: **144,750 price movements across 14,276 markets**, plus bid/ask and spread on
12,000+ markets and a daily census of the ~39,000 market catalogue.

[@p0lywhales](https://x.com/p0lywhales) ·
[writeups](https://polywhales-tracker-production.up.railway.app/api-notes) ·
[findings](https://polywhales-tracker-production.up.railway.app/data-findings) ·
[dataset](https://polywhales-tracker-production.up.railway.app/dataset)

The writeups cover API failure modes that return valid-looking responses, and state where
coverage has holes. Two findings were retracted while writing them: a churn figure that was
measuring my own instrument, and a calibration result that was really a result about football.

## Robinhood Chain Index

Token attribution across Robinhood Chain, scanned from block 0. As of September 2026:
**635,501 tokens mapped to the 172,067 wallets that actually launched them**, with name, symbol
and supply on the 125,972 inside the metadata range.

[Robinhood-Chain-Index](https://github.com/gBlaku/Robinhood-Chain-Index) ·
[report](https://github.com/gBlaku/Robinhood-Chain-Index/blob/main/docs/REPORT.md) ·
[dataset](https://github.com/gBlaku/Robinhood-Chain-Index/blob/main/data/launchers_full.csv.gz)

Block explorers name the launchpad as a token's creator, because launchpads deploy through
`CREATE2`, so the person who launched it appears nowhere. Indexing the transaction sender
restores the lookup. ERC-4337 breaks the same assumption one layer up, where the sender is a
bundler submitting other people's operations, and my own index shipped with that defect until I
found it: 41,621 tokens across 137 bundlers, re-attributed. The README also covers reverse
engineering the endpoint's rate limiter, a per-IP bucket priced by method cost where parallel
connections make throughput worse.

## EDGAR AI Pivot Monitor

Real-time classification over SEC EDGAR. Polls for new 8-K filings, scores them against a
weighted keyword taxonomy, sends survivors to an LLM, and dispatches whatever clears a
confidence threshold.

[edgar-ai-pivot-monitor](https://github.com/gBlaku/edgar-ai-pivot-monitor). Archived, public as
a work sample.

## Working with

`Java / Spring Boot` · `TypeScript / Node` · `Python` · `Swift / SwiftUI` · `React`
`PostgreSQL` · `Sybase` · `AWS` · `Docker` · `Playwright` · `MCP`
