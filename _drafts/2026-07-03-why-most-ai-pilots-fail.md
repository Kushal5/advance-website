---
title: "Why 95% of AI pilots fail — and what the other 5% do differently"
description: "MIT researchers found 95% of corporate AI pilots deliver no measurable return. The difference isn't the model — it's the engineering around it. Here's what the successful 5% actually do."
date: 2026-07-03 09:00:00 +1200
tags: [AI strategy, Data]
image: /assets/og-image.jpg
---

Everyone's talking AI. Budgets are approved, pilots are launched, demos look great.
Then, quietly, most of it goes nowhere.

MIT's Project NANDA put a number on it: across an estimated **US$30–40 billion** of
enterprise spend on generative AI, about **95% of pilots deliver no measurable
business impact**. Gartner points the same direction — it predicts organisations
will **abandon 60% of AI projects through 2026** if the data underneath them isn't
ready.

Those aren't reasons to sit AI out. They're a map of where the failures are — and
they're avoidable.

## It's usually not the AI

The models are good, and they're getting better every quarter. When a pilot dies,
the autopsy almost always finds the same things:

- **It started with a tool, not a process.** Someone bought licences and then went
  looking for a problem. Nobody could say which hours it was supposed to save.
- **It ran ungrounded.** A general-purpose chatbot answers from its training data,
  not from your prices, your stock, your history. When it doesn't know, it guesses —
  confidently.
- **The data underneath was messy.** Disconnected apps, spreadsheets on laptops,
  three versions of the truth. McKinsey's State of AI research keeps finding the
  same blocker: it's the organisation's own data and processes, far more often
  than the model.
- **Nobody owned it after launch.** A pilot that impresses in week one and has no
  owner in month six isn't a system. It's a demo.

## What the 5% do differently

**They start with one process that matters.** Not "adopt AI" — fix quoting, or
invoice handling, or the report someone rebuilds every Monday. One process, with
the hours counted before and after.

**They ground the AI in their own data.** Systems that answer from your documents
and your records, and show the source of every answer. Grounded systems don't
invent; they cite.

**They give it an engineering owner.** The MIT study found builds done with a
specialist partner reached deployment about **67% of the time, versus roughly 22%**
for internal-only attempts — a three-fold gap. The difference isn't magic; it's
architecture, security and maintenance being someone's actual job.

## A quick self-test

Before your next AI initiative, answer three questions:

1. Which single process is this meant to fix, and what does it cost you today?
2. Where does the data for that process live — and does the AI actually have it?
3. Who maintains the system in month six?

If any answer is fuzzy, that's the work to do first. It's cheaper to answer these
in a meeting than to discover them in a failed rollout.

## Common questions

### Do we need a big budget to start?

No. The failed pilots in the MIT study were mostly *big* budgets. Start with one
process, put real numbers on the saving before anything is built, and let the
first win fund the second.

### Our data is messy. Do we fix everything first?

Fix the slice that feeds the one process you're targeting. "AI-ready data" isn't a
two-year warehouse project — it's making sure the system you're building reads
from one reliable source of truth.

### Build in-house or bring in a specialist?

Both can work. The honest read of the numbers: internal-only builds fail more
often, usually at the integration, security and maintenance stages rather than
the AI itself. If you have in-house developers, a specialist can own the
architecture and work alongside them.

## Sources

- MIT Project NANDA, *The GenAI Divide: State of AI in Business 2025* —
  [report PDF](https://mlq.ai/media/quarterly_decks/v0.1_State_of_AI_in_Business_2025_Report.pdf) ·
  [Fortune's coverage](https://fortune.com/2025/08/18/mit-report-95-percent-generative-ai-pilots-at-companies-failing-cfo/)
- Gartner, [*Lack of AI-ready data puts AI projects at risk*](https://www.gartner.com/en/newsroom/press-releases/2025-02-26-lack-of-ai-ready-data-puts-ai-projects-at-risk) (press release, Feb 2025)
- McKinsey, [*The State of AI*](https://www.mckinsey.com/capabilities/quantumblack/our-insights/the-state-of-ai)

<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "FAQPage",
  "mainEntity": [
    {
      "@type": "Question",
      "name": "Do we need a big budget to start with AI?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "No. The failed pilots in the MIT study were mostly big budgets. Start with one process, put real numbers on the saving before anything is built, and let the first win fund the second."
      }
    },
    {
      "@type": "Question",
      "name": "Our data is messy. Do we fix everything first?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "Fix the slice that feeds the one process you're targeting. AI-ready data isn't a two-year warehouse project — it's making sure the system you're building reads from one reliable source of truth."
      }
    },
    {
      "@type": "Question",
      "name": "Should we build AI in-house or bring in a specialist?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "Both can work. Internal-only builds fail more often, usually at the integration, security and maintenance stages rather than the AI itself. If you have in-house developers, a specialist can own the architecture and work alongside them."
      }
    }
  ]
}
</script>
