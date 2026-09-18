# highlevel ai employee: what the three plans really cost, where agencies get squeezed, and when CloseBot fits better

Most people typing this into Google are standing at one of two doors. Either you saw a number like "$97/month per location" and want to know what's actually inside, or you're already paying it across a stack of sub-accounts and the invoice stopped making sense a while ago.

HighLevel's AI Employee isn't one product with one price tag. It's an umbrella across Conversation AI, Voice AI, Reviews AI, Content AI and a handful of smaller tools, and it bills in three completely different ways depending on what you pick. Choose wrong for your volume and you can end up paying several times more than you needed to.

Here's the breakdown with the official numbers, the line items that inflate the bill quietly, and where a dedicated conversational AI layer like CloseBot makes more sense.

## What AI Employee actually covers

HighLevel's own pricing documentation lists three modes, all priced in USD and all billed per enabled location:

| Mode | Monthly fee | What's included | Fits |
| --- | --- | --- | --- |
| Pay-Per-Use | None | Everything at token cost, no included allowances | Low or spiky volume |
| AI Employee Growth | $50 per location | 1,000 Conversation AI responses, 100 Voice AI minutes, 100 Voice AI prompt optimizer minutes, unlimited Reviews AI and Content AI, 100 Managed Agent runs, Ask AI and AI Studio usage included | Mid-volume locations |
| AI Employee Unlimited | $97 per location | Unlimited Conversation AI, Voice AI (inbound, outbound and widget), Reviews AI, Content AI and Voice AI prompt optimizer, subject to fair use. 3x Ask AI and AI Studio usage, 1,000 Managed Agent runs | High-volume locations |

Two things sit outside all three plans and cause most of the confusion:

- **Agent Studio is never bundled.** It's pay-per-use on Pay-Per-Use, on Growth and on Unlimited alike. If Agent Studio is central to what you're building, the Unlimited plan doesn't protect you from those charges.
- **Phone charges always apply separately.** Unlimited Voice AI minutes still don't include telephony.

Rebilling adds a third constraint. HighLevel's documentation states that agencies need to be on the $497/month agency plan to rebill AI Employee usage to client locations. On a lower tier, these costs land on your own P&L instead of the client's.

## The line items that decide your real bill

### Voice AI pricing is not one number

Since May 20, 2026, the Voice Engine component runs at $0.045 per minute. On top of that you pay text-to-speech and LLM tokens.

| Component | Rate |
| --- | --- |
| Voice Engine | $0.045/min |
| OpenAI TTS | $0.015/min |
| Cartesia TTS | $0.015/min |
| ElevenLabs V2.5 | $0.035/min |
| ElevenLabs V3 | $0.170/min |

HighLevel's own worked example: a 10-minute call using OpenAI TTS costs about $0.60 in voice processing before LLM tokens and phone charges are added. Switch that same call to ElevenLabs V3 and the voice portion alone lands around $1.85.

Speech-to-speech models work differently. Google's live model is $0.10/min and OpenAI's realtime model is $0.20/min, all-in, with the agent prompt capped at 15K tokens.

### Conversation AI is billed in tokens, not messages

There's no flat "cost per message" figure for the pay-per-use track. Current model rates look like this:

| Model | Input / 1M tokens | Output / 1M tokens |
| --- | --- | --- |
| GPT-5 | $1.25 | $10.00 |
| GPT-5 Mini | $0.25 | $2.00 |
| GPT-4.1 | $2.00 | $8.00 |
| GPT-4.1 Mini | $0.40 | $1.60 |

HighLevel's example: a conversation using 100,000 input tokens and 25,000 output tokens on GPT-5 costs roughly $0.375. The same conversation on GPT-4.1 Mini would be a fraction of that.

Which means two conversations of identical length can cost very different amounts. Longer chat history, bigger knowledge bases and wordier replies all push the number up. If you're forecasting costs for a client, forecasting from message counts alone will be wrong in both directions.

### What the Growth plan's overage really means

Growth includes 1,000 Conversation AI responses and 100 Voice AI minutes. Past those, usage reverts to pay-per-use rates. Whether the AI keeps running or stops at the limit depends on the location's AI Usage Limit setting. On "Keep AI running, just notify", the agent keeps replying and you keep paying. On "Block AI at the limit", it stops mid-conversation, which is its own kind of problem if it happens to a hot lead at 9pm.

## Where the math turns against you

The per-location model is perfectly reasonable at two or three locations. It's at four and beyond that the multiplication starts doing damage.

| Locations | Growth ($50 each) | Unlimited ($97 each) |
| --- | --- | --- |
| 3 | $150/mo | $291/mo |
| 10 | $500/mo | $970/mo |
| 25 | $1,250/mo | $2,425/mo |
| 50 | $2,500/mo | $4,850/mo |
| 102 | $5,100/mo | $9,894/mo |

That last row isn't hypothetical. CloseBot published a case study of a 102-sub-account agency and priced the equivalent AI Employee Unlimited setup at $9,894/month. CloseBot is the vendor making that argument, so weigh the framing accordingly, but the multiplication itself is HighLevel's own published price, and you can run the arithmetic against your own location count in about ten seconds.

The honest counterpoint: **pay-per-use can be cheaper than Unlimited at low volume.** The case study example showed 468 monthly messages costing roughly $9 in HighLevel pay-per-use terms. If your locations are quiet, the subscription is the wrong choice. The trade-off is that you lose the included allowances and any predictability, and the bill scales linearly with success rather than being capped.

There's also a strategic wrinkle. If a big part of what you resell to clients is AI setting, and you're on the $97/location plan, your margin shrinks every time you add a client. That's a business-model problem, not just a pricing one.

## What you're buying, and what the native stack doesn't do

To be fair to HighLevel: this is a bundled suite inside a platform you're already paying for. Funnel AI, Workflow AI and Email AI are free or included, Ask AI and AI Studio are genuinely useful, and Reviews AI at unlimited is good value if you're managing reputations across locations. If your requirement is "answer leads reasonably well inside the CRM I already use," AI Employee does the job for $50 or $97 a location.

Where agencies tend to start looking elsewhere is conversational quality on actual sales conversations. The signals worth noting:

- A widely-read Reddit thread on GoHighLevel tools concluded that third-party options are generally better for conversational booking than the native bot, with one user in r/automation describing CloseBot as "way better than GHL chat AI. you can conversationally book appointments and reschedule."
- G2 reviews of CloseBot repeatedly cite the speed of setup and the quality of the conversations as the standout points.
- CloseBot published a side-by-side split test claiming roughly a 10% quality gap in booking conversations. That's a vendor-run test with a vendor's interpretation, so treat it as a claim rather than a study.

What's structurally different is the builder. CloseBot uses drag-and-drop job flows with reusable personas rather than one large prompt per location. That matters most when you're handling multiple services or calendar types in the same conversation, which is where prompt-only agents tend to forget questions or book to the wrong calendar.

If you want to see how that builder behaves before committing, 👉 [start on CloseBot's free plan](https://app.closebot.com/a?fpr=li87) and run a real conversation through it.

## CloseBot's plans, without the sales gloss

Prices below are from CloseBot's plans page and documentation.

| Plan | Who it's for | What's included | Price | Billing | Get started |
| --- | --- | --- | --- | --- | --- |
| Free | Testing the tool, very low lead volume | 100 monthly messages, 1 agent, 1 user seat, 1 MB knowledge storage, unlimited account connections | $0 | Free forever under the message cap | [Free plan](https://app.closebot.com/a?fpr=li87) |
| Core (Business) | Businesses running their own lead qualification | 500 monthly messages included at entry with price scaling by volume, 15+ templates (50+ on annual), human support, additional users at $5/seat, storage add-ons | $64/mo monthly; $53/mo equivalent on annual billing ($640/yr) | Monthly or annual | [See Core pricing](https://app.closebot.com/a?fpr=li87) |
| Agency | Agencies selling AI setting to clients | Rebill everything, including messages at $0.012 each; white-label client portal; unlimited account connections and agents; $5 per seat | $397/mo | Monthly (roughly $331/mo equivalent on annual billing per G2's listing) | [Get the Agency plan](https://app.closebot.com/a?fpr=li87) |
| Growth | Regulated or high-volume operations | HIPAA compliance, SLAs, quarterly audits, 99.99% priority uptime, priority support, 50+ templates | Custom | Custom | [Price out the Growth tier](https://app.closebot.com/a?fpr=li87) |

The pricing structure differs from HighLevel's in one meaningful way: on **business** plans, message costs are included in the base price rather than metered on top. On the **agency** plan you're billed $0.012 per message and can mark it up to whatever you want before it reaches the client, which is the whole point of that tier.

A few operational details worth knowing before you sign anything:

- **There are no refunds.** CloseBot states this plainly on the plans page. What you get instead is a free-forever plan under 100 messages a month and a 7-day trial of any paid plan before billing starts.
- **No credit card to start and no contract.** Plans run month to month, upgrade or cancel any time.
- **The free plan is genuinely capped.** One agent, one seat, 100 messages, 1 MB of storage. Fine for a test, not for running live campaigns.

## The limitation nobody puts in the headline

CloseBot doesn't connect to Instagram, WhatsApp or Messenger itself. It plugs into a CRM, and it answers the text channels connected there. Supported integrations are HighLevel, HubSpot, LeadConnector and custom CRMs.

That's fine if you already run GoHighLevel or HubSpot, which is most of the audience for an AI Employee question anyway. But if your entire pipeline lives in Instagram DMs and you don't run a CRM, CloseBot isn't a standalone purchase. You'd be adding a CRM first. Worth knowing before you compare it to DM-native tools.

## How to decide

**Stay on AI Employee if** you're running one to three locations, your conversational volume is modest, and you want everything inside the platform you already pay for. On a quiet account, pay-per-use is cheap and honest.

**Move volume onto a dedicated layer if** you're past four locations using Unlimited, your margin on AI services is being eaten by per-location fees, or conversational booking quality is the thing clients actually judge you on.

**Run the arithmetic before committing either way.** Multiply your location count by $97, then compare it against $0.012 per message plus a $397 agency plan at your actual monthly volume. For a 4-location agency with 2 appointments a day, the second number is dramatically smaller. For a single quiet location, the first one is.

## FAQ

**Is AI Employee included in my HighLevel subscription?**
No. It's billed monthly per enabled location on top of your plan, at $50 for Growth or $97 for Unlimited. Pay-per-use has no monthly fee but bills at token cost.

**Can I rebill AI Employee usage to clients?**
Only if your agency is on the $497/month plan, per HighLevel's documentation. Below that, the cost stays with you.

**Is there really an unlimited option?**
Yes, at $97 per location per month, with fair-use protections. Note that Agent Studio and phone charges are still billed separately on that plan.

**What does CloseBot cost for an agency reselling AI?**
$397/month plus $0.012 per message, both rebillable to clients at your own markup. The math that matters isn't the platform fee, it's whether your per-client message volume justifies it.

The short version: AI Employee is a solid bundle that competes on convenience, and its pricing punishes exactly the agency model it was designed to serve. CloseBot competes on conversational quality and per-message economics, and it requires a CRM underneath. Pick based on your location count and who's paying the bill.
