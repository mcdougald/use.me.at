<p align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset=".github/assets/hero-dark.png">
    <img src=".github/assets/hero.png" alt="use.me.at landing page" width="880">
  </picture>
</p>

<h1 align="center">use.me.at</h1>

<p align="center"><strong>The equipment I use for programming, wireframing, making videos, and every day.</strong></p>

<p align="center">
  <img src="https://img.shields.io/badge/status-live-171717?style=flat-square" alt="Status: live">
  <img src="https://img.shields.io/badge/license-source--available-404040?style=flat-square" alt="License: source-available">
  <img src="https://img.shields.io/badge/part%20of-me.at-737373?style=flat-square" alt="Part of me.at">
</p>

<p align="center">
  <a href="https://use.me.at">Website</a> ·
  <a href="#features">Features</a> ·
  <a href="#how-it-works">How it works</a> ·
  <a href="#built-with">Built with</a>
</p>

Most uses pages are written once and left alone: retired gear lingers and product links quietly die. I built use.me.at as a uses page that stays honest: the hardware, editor and software I use day to day, from my laptop and accessories to my gaming PC build, homelab, coding tools and Mac apps. Every item is marked in use or retired, every outbound link is checked each quarter, and the whole page is also published as JSON for anyone who wants the list without the layout.

<p align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset=".github/assets/overview-dark.svg">
    <img src=".github/assets/overview.svg" alt="use.me.at at a glance: sectioned and counted, current and retired, machine-readable too, links that stay alive" width="880">
  </picture>
</p>

## Why use.me.at

| The usual uses page | use.me.at |
| --- | --- |
| Old gear and current gear in one list | Every item marked in use or retired |
| Dead product links pile up | Every external link probed each quarter |
| Only readable as a page | Also published as `/uses.json` |
| One long scroll | Sections with an index and per-section item counts |

## Features

- **Sectioned uses page**: laptop, accessories, gaming PC hardware, homelab, coding, development tools and software, with an "On this page" index showing per-section item counts.
- **In use vs. retired**: every item carries a status, so past gear stays documented without cluttering what is current.
- **`/uses.json`**: a machine-readable projection of the page (software and built-with lists), optionally enriched with coding activity from WakaTime.
- **Structured data**: the page emits `WebPage` and `ItemList` JSON-LD for search engines.
- **Link liveness checks**: a scheduled job probes every external URL on the page each quarter so dead product links get noticed.
- **Listing exports**: scripts generate submission copy for uses directories and StackShare from the same source.

## How it works

<p align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset=".github/assets/flow-dark.svg">
    <img src=".github/assets/flow.svg" alt="How use.me.at works: write, classify, render, project, probe" width="880">
  </picture>
</p>

The page is one MDX document rendered through the family's shared content components, with each item classified as in use or retired and the page emitting `WebPage` and `ItemList` JSON-LD. The same source is projected to `/uses.json`, optionally enriched with my WakaTime coding activity, and a scheduled job probes every external link each quarter. Submission copy for uses directories and StackShare is generated from that source too.

## Built with

<p>
  <img src="https://img.shields.io/badge/Next.js-16-000000?style=flat-square&logo=nextdotjs&logoColor=white" alt="Next.js 16">
  <img src="https://img.shields.io/badge/React-19-171717?style=flat-square&logo=react&logoColor=white" alt="React 19">
  <img src="https://img.shields.io/badge/TypeScript-5-262626?style=flat-square&logo=typescript&logoColor=white" alt="TypeScript">
  <img src="https://img.shields.io/badge/Tailwind%20CSS-4-404040?style=flat-square&logo=tailwindcss&logoColor=white" alt="Tailwind CSS 4">
  <img src="https://img.shields.io/badge/MDX-content-525252?style=flat-square&logo=mdx&logoColor=white" alt="MDX">
  <img src="https://img.shields.io/badge/Vitest-tested-737373?style=flat-square&logo=vitest&logoColor=white" alt="Vitest">
</p>

- Next.js 16 (App Router), React 19, TypeScript
- Tailwind CSS 4
- MDX content rendered through the family's shared content components
- WakaTime API (optional) for coding activity
- Vitest and Playwright

## Part of the me.at family

use.me.at is one of my [`*.me.at`](https://me.at) apps. They share one design system, account, and app shell. Development happens in a private monorepo; this repository is the project's public-facing home.

## License

Source-available. See [LICENSE](LICENSE).
