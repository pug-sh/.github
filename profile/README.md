<div align="center">

<img alt="Pug" src="https://app.pug.sh/logo.svg" width="96" height="96" />

### Analytics you own, built in the open.

See how people use your product with trends, funnels, retention, and user flows. Cookieless by default: visitors are counted, not identified, until they opt in.

Self-host the whole stack, or start free on **Pug Cloud**. The same code runs both.

[**pug.sh**](https://pug.sh) · [**Live demo**](https://demo.pug.sh) · [**Docs**](https://docs.pug.sh) · [**Discord**](https://discord.gg/kDNHDWcBHP) · [**Main repo**](https://github.com/pug-sh/pug)

<br/>

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/pug-sh/pug/main/docs/assets/overview-dark.webp" />
  <img alt="Pug's overview page: visitors, sessions, page views, bounce rate and traffic sources, built from your events" src="https://raw.githubusercontent.com/pug-sh/pug/main/docs/assets/overview-light.webp" />
</picture>

</div>

---

## Why Pug

**Your data stays yours.** The whole product is open source under AGPL-3.0. Self-host it and every event stays on your servers. Pug Cloud runs the same code.

**Private by default.** The browser SDK starts cookieless. Events flow from the first page view, and nothing is written to the device until a visitor says yes. Erasing a person hard-deletes their events and profile.

**Every feature on every plan.** SSO included. Pricing is by events alone, with no per-seat or per-project fees. Pug Cloud is free up to 100k events a month, and self-hosting is free forever.

## What you get

- **Web analytics**: visitors, sessions, page views, bounce rate and traffic sources, built from your events with nothing to set up.
- **Live view**: every visitor on a real-time world map, down to the person and the event they just sent.
- **Profiles**: one timeline per person, with their anonymous history merged in at sign-in.
- **Insights**: trends, funnels, retention, segmentation, user flows and top K, filtered and broken down by any property.
- **Dashboards**: pin insights and notes as tiles on a grid that shares one time window.
- **MCP server**: ask your analytics from your editor. Twelve read-only tools give an AI agent the same numbers your dashboard shows.
- **SSO**: Google Workspace, or your own identity provider over OIDC.

## Repositories

<table>
<tr>
<td width="50%" valign="top">

### [pug](https://github.com/pug-sh/pug)

The server: ingestion, insights, profiles, dashboards and the MCP server. One Go binary on PostgreSQL, ClickHouse and NATS.

`go` `clickhouse` `nats` `AGPL-3.0`

[![stars](https://img.shields.io/github/stars/pug-sh/pug?color=3C68D9&labelColor=172646&logo=github&style=flat)](https://github.com/pug-sh/pug/stargazers) [![release](https://img.shields.io/github/v/release/pug-sh/pug?color=F8EBD9&labelColor=172646)](https://github.com/pug-sh/pug/releases)

</td>
<td width="50%" valign="top">

### [app](https://github.com/pug-sh/app)

The dashboard. React and TypeScript, talking to the server over Connect RPC.

`react` `typescript` `AGPL-3.0`

[![license](https://img.shields.io/github/license/pug-sh/app?color=F8EBD9&labelColor=172646)](https://github.com/pug-sh/app/blob/main/LICENSE)

</td>
</tr>
<tr>
<td width="50%" valign="top">

### [sdk-browser](https://github.com/pug-sh/sdk-browser)

Web SDK. Autocapture, sessions and cookieless consent for any site or web app.

`@pug-sh/browser` `MIT`

[![npm](https://img.shields.io/npm/v/@pug-sh/browser?color=3C68D9&labelColor=172646&logo=npm)](https://www.npmjs.com/package/@pug-sh/browser)

</td>
<td width="50%" valign="top">

### [sdk-flutter](https://github.com/pug-sh/sdk-flutter)

Flutter SDK. Events, identity, sessions and batching for mobile and desktop apps.

`pug_flutter` `MIT`

[![pub](https://img.shields.io/pub/v/pug_flutter?color=3C68D9&labelColor=172646&logo=flutter)](https://pub.dev/packages/pug_flutter)

</td>
</tr>
<tr>
<td width="50%" valign="top">

### [sdk-android](https://github.com/pug-sh/sdk-android)

Android SDK. App lifecycle, screen views and installs tracked automatically, for Kotlin and Java apps.

`sh.pug:android` `MIT`

[![maven](https://img.shields.io/maven-central/v/sh.pug/android?color=3C68D9&labelColor=172646&logo=apachemaven)](https://central.sonatype.com/artifact/sh.pug/android)

</td>
<td width="50%" valign="top">

### [sdk-node](https://github.com/pug-sh/sdk-node)

Node.js SDK. Trusted server-side events, plus profile and insight reads.

`@pug-sh/node` `MIT`

[![npm](https://img.shields.io/npm/v/@pug-sh/node?color=3C68D9&labelColor=172646&logo=npm)](https://www.npmjs.com/package/@pug-sh/node)

</td>
</tr>
<tr>
<td width="50%" valign="top">

### [sdk-ruby](https://github.com/pug-sh/sdk-ruby)

Ruby SDK. Server-side events plus profile and insight reads, for Rails or plain Ruby.

`pug-sh` `MIT`

[![gem](https://img.shields.io/gem/v/pug-sh?color=3C68D9&labelColor=172646&logo=rubygems)](https://rubygems.org/gems/pug-sh)

</td>
<td width="50%" valign="top"></td>
</tr>
</table>

No SDK for your stack yet? The [HTTP API](https://docs.pug.sh/api/) works from any language.

## Get started

```bash
npm install @pug-sh/browser
```

```ts
import { init, identify, track } from '@pug-sh/browser'

init('your-project-id', { apiKey: 'pub_your_key' })
// Page views, clicks, scrolls and form interactions are captured from here on.

identify('user_123', { plan: 'pro' })
track('order_completed', { amount: 49.0, currency: 'USD' })
```

[**Create a free project**](https://app.pug.sh) · [Self-host it](https://docs.pug.sh/self-hosting/) · [Every SDK](https://docs.pug.sh/sdks/)

## Where this goes

- **A rock-solid analytics core first.** Events, profiles, insights and dashboards you can trust.
- **More SDKs.** Native iOS and React Native, plus server SDKs for Go, Rust, Java and Python.
- **DPDP hardening.** Consent records, data-principal rights and breach notification for India's privacy law, on top of the erasure that ships today.
- **Customer engagement.** Campaigns built from the profiles and events you already track, sent by push, email, SMS, WhatsApp or webhook.

The full picture lives in the [**Roadmap**](https://docs.pug.sh/roadmap/).

## Build it with us

Pug is built in the open. Ask questions and share what you're building on [Discord](https://discord.gg/kDNHDWcBHP), start a [discussion](https://github.com/pug-sh/pug/discussions) to shape what comes next, or pick up a [help wanted](https://github.com/pug-sh/pug/labels/help%20wanted) issue. [CONTRIBUTING.md](https://github.com/pug-sh/pug/blob/main/CONTRIBUTING.md) covers the setup, and you sign the [CLA](https://github.com/pug-sh/pug/blob/main/CLA.md) once by commenting `/sign` on your first pull request.

---

<div align="center">

[![Discord](https://img.shields.io/badge/Discord-join%20us-5865F2?style=for-the-badge&labelColor=172646&logo=discord&logoColor=white)](https://discord.gg/kDNHDWcBHP)
[![Live demo](https://img.shields.io/badge/demo.pug.sh-try%20it-3C68D9?style=for-the-badge&labelColor=172646)](https://demo.pug.sh)
[![Docs](https://img.shields.io/badge/docs.pug.sh-read-F8EBD9?style=for-the-badge&labelColor=172646)](https://docs.pug.sh)
[![Reddit](https://img.shields.io/badge/r%2Fpug__sh-follow-FF4500?style=for-the-badge&labelColor=172646&logo=reddit&logoColor=white)](https://www.reddit.com/r/pug_sh/)

`open source` · `self-hostable` · `cookieless by default` · `AGPL-3.0 server` · `MIT SDKs`

</div>
