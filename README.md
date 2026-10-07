# Hi, I'm Dávid Pörös

Backend engineer in Budapest, writing code professionally since 2013. I build high-traffic distributed systems and work in payments and compliance: a messaging channel sending millions of messages a day, billing and subscriptions, and KYC and AML at a payment orchestrator. I work remotely and in writing first, across time zones.

**Open to senior and staff individual-contributor roles.** Remote, async-first, EU time zone. I've been an engineering manager and a squad lead, and I do my best work building.

I write about what I build on [my blog](https://davidporos92.github.io).

Reach me on [LinkedIn](https://www.linkedin.com/in/david-poros/) or in [email](mailto:david.poros@proton.me).

---

## What I've built

### High-traffic messaging on a distributed platform

- Built an SMS channel from scratch on a queue-based microservice platform sending millions of messages a day, Black Friday peaks included.
- Wrote a Redis-based throughput rate limiter as an atomic Lua script, chosen over a Go version after running both in production.
- Added configurable Quiet Hours for campaigns and automations, so customers stay within US TCPA rules (fines of roughly $500–$1,500 per message).

`Node.js` `Go` `Redis` `MongoDB` `AWS` `Protobuf` `OpenAPI`

### Payments and subscriptions

- Owned the billing domain of a messaging platform: subscriptions, invoicing and usage-based message billing.
- Built Stripe payments, subscriptions and an in-app credit system as sole developer of my own B2B SaaS for darts tournaments, and onboarded 5–10 venues.

### KYC and AML at a payment orchestrator

- Owned both domains in a Symfony monolith. Promoted to squad lead within a year, leading a four-person squad.
- Moved identity-document field extraction to an LLM-based approach, validated against human-reviewed documents first and shipped in small, independently deployable slices.
- Built merchant-facing AML tooling: an audit report to search a person and export evidence for auditors, and a daily watchlist sync with alerting.

`PHP` `Symfony` `MySQL` `OpenSearch` `Docker`

---

## Writing

I build pet projects in the open and write up the decisions, the trade-offs and what broke, with tagged code for every post: **[davidporos92.github.io](https://davidporos92.github.io)**

- **[Building MarginCMS](https://davidporos92.github.io/posts/building-margincms-part-1-contract-first-code-later/)**: a small, contract-first CMS with a Go API generated from an OpenAPI spec. [Code on GitHub](https://github.com/davidporos92/margin-cms).

---

## Stack

| Area | What I use |
| --- | --- |
| Languages | PHP (Symfony), Node.js and TypeScript, Go, Bash |
| Data | MySQL, PostgreSQL, MongoDB, Redis, OpenSearch |
| Architecture | Message queues, event-driven design, microservices, OpenAPI, Protobuf |
| Infrastructure | Docker, AWS, CI/CD, logging and alerting |
| Domain | Payments and subscriptions, KYC and AML, TCPA and SOC 2 requirements |
| Frontend | Vue.js, React |
| AI tooling | LLM integration with evaluation first; Cursor and Claude daily, always followed by human review |

## How I work

- **Writing first.** RFCs for anything non-trivial, written status updates instead of weekly meetings, and messages with full context so nobody needs a round-trip.
- **Small, reviewable PRs.** I ship in stacked slices and review my own work (and run an AI review) before asking a person.
- **Hand-offs across time zones.** I name who takes over, and plan around the gap instead of staying up for it.
- **Understand the need first.** I ask what a request is for before I build it. The real constraint is often a regulation, a cost or a workflow nobody mentioned.
- **Careful with other people's money.** Repair commands are idempotent, paced and have a dry-run mode. Failures get alerting, not only logs.