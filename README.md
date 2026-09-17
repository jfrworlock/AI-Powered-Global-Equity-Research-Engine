# AI-Powered Global Point-in-Time Equity Research Engine

A modular research pipeline for building **global, point-in-time fundamental equity datasets** across multiple markets and industries.

This repository contains:

- **V1** — the original automotive-focused end-to-end implementation
- **V2** (work in progress) — an ongoing redesign into a reusable, industry-neutral research engine

## Objective

The system is designed to take:

- A research theme, such as `Automotive` or `Robotics`
- A list of ETFs and/or individual stocks
- A historical start and end date

and build a global research database containing:

- Historical universe constituents
- Issuer, security and listing identities
- Point-in-time financial statement data
- Filing and amendment histories
- Harmonised accounting concepts
- Industry-specific operating KPIs
- AI-assisted semantic interpretation
- Machine-readable Parquet outputs
- Analyst-friendly Excel datasets

## V2 Architecture

V2 uses eight production blocks:

1. **Universe & Identity** — historical constituents, security master, issuer resolution and source routing
2. **Structured XBRL** — primarily SEC and other structured filing systems
3. **Europe** — ESEF and European filing sources
4. **East Asia** — Japan EDINET and Korea OpenDART
5. **China & Hong Kong** — CNINFO, HKEX and multilingual processing
6. **Residual Markets** — Australia and other smaller exchanges
7. **Industry Intelligence** — theme-specific operating KPIs
8. **Global Publisher** — harmonisation and final research dataset

A shared core provides common schemas, identity logic, OpenAI integration, caching, persistence and concept registries.

## AI-Assisted, Deterministic by Design

The **OpenAI API** is used where semantic interpretation is useful, including:

- Financial concept mapping
- Translation
- Document classification
- Industry/theme classification
- Custom taxonomy interpretation
- Industry-specific KPI extraction

Core database functions remain deterministic, including:

- Security and issuer IDs
- Historical universe membership
- Filing timestamps
- Point-in-time availability
- Version ordering
- Arithmetic and persistence

> **AI interprets semantics; deterministic code governs identity, time and database state.**

## Point-in-Time Research

The engine preserves historical filing dates, availability timestamps, amendments and fact versions so that research models can use only information that would actually have been available at the time.

## Current Use Case

The first implementation is:

> **Global Automotive PIT Research Database**

covering the broader listed automotive ecosystem.

The first intended modelling universe is:

> **Global Listed Automotive OEMs**

## Longer-Term Goal

The objective is to make the research theme configurable.

For example:

    Theme: Automotive
    ETFs: DRIV, CARZ, IDRV, KARS

could later become:

    Theme: Robotics
    ETFs: BOTZ, ROBO, IRBO

while reusing the same international data infrastructure.

The long-term goal is a reusable:

> **AI-Powered Global Point-in-Time Equity Research Engine**

for fundamental and systematic equity research across international markets.
