# Rogo Deal Screener

I built this after spending a week going through Rogo's product, their Felix launch, and the Series D announcement.

The thing that stood out to me was a line from Gabriel Stengel's blog post: "The best dealmakers aren't constrained by gathering information. They're limited by the time it takes to turn that information into advice for a CEO or recommendation for an investment committee."

That's the problem this demo tries to solve. Not a chatbot. Not a search box. Something that takes a CIM and produces what an analyst would spend a full day building — in under two minutes.

---

## What it does

You pick a deal, hit Screen Deal, and two Claude API calls run back to back.

The first acts as a senior analyst. It reads the CIM, pulls every material financial metric, structures the customer profile, identifies the competitive moats, and cites exactly which section of the document each number came from.

The second acts as an MD writing for an investment committee. It produces five real comparable public companies with current EV/EBITDA and EV/Revenue multiples, an implied enterprise value range, a set of investment highlights, a risk matrix with severity ratings and mitigants, four prioritized diligence workstreams, and a direct IC recommendation — proceed, pass, or proceed with caution.

The whole output looks like something you'd actually hand to a partner before a management presentation.

---

## The three deals

I used real companies with verified public financials, not made-up scenarios.

**Verint Systems (VRNT) — Take-private** Verint is a $910M revenue enterprise AI company whose public multiple (around 6x EBITDA) is materially below where it would trade in a private transaction. The cloud transition is creating near-term revenue drag that public markets penalize but a PE sponsor with a 5-year hold can look through. This is exactly the kind of software take-private that's been active since 2022.

**Howmet Precision Structures — Aerospace carve-out** Howmet Aerospace (HWM) is a real NYSE company. The carve-out scenario is based on their Precision Structures segment, which produces titanium and aluminum airframe components for Boeing and Airbus. $1.24B revenue, 14% EBITDA margins, $4.8B order backlog. Carve-outs are technically complex — IT separation, stranded costs, real estate — and this scenario includes all of it.

**Waystar (WAY) — Secondary block trade** Waystar IPO'd in June 2024 at $21.50/share. The scenario is EQT Partners selling their remaining 22% stake in an accelerated bookbuild. $917M LTM revenue, 40% adjusted EBITDA margin, 108% NRR. SVB Leerink and J.P. Morgan ran the actual IPO, so the banking relationship is accurate too.

---

## Why I built it this way

I have four years of PM experience building AI systems inside Capital One and Optum. Both are heavily regulated, both have high-stakes output requirements, and both taught me that the gap between a good AI demo and something a professional will actually trust is enormous.

Rogo's product sits at that gap. The reason 35,000 bankers use it daily isn't the model — it's that the outputs look right, cite their sources, and don't make you second-guess every number before you put it in a deck.

I tried to build something with the same instinct. Every data point in the output traces back to a section of the CIM. The IC recommendation is direct, not hedged. The comp multiples use real 2024 market data, not placeholder ranges.

The role asks for someone who can build prototypes with AI tools, run demos with clients, and translate financial workflows into product requirements. This is my version of showing up to that conversation with proof of work rather than a cover letter.

---
