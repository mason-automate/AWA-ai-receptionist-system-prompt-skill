# AI Receptionist System Prompt Skill

A Claude Code Skill that generates production-ready system prompts for AI phone receptionists, built for home service businesses like plumbing, HVAC, restoration, and auto.

Give Claude Code the business details and it writes the full system prompt for you. Two tiers, fully templated, optimized for Trillet and portable to VAPI or Retell.

## Why this exists

Most local businesses miss a large share of their inbound calls, and the caller usually just dials the next business on the list. An AI receptionist answers every call, around the clock, in multiple languages, for a fraction of the cost of a human.

The slow part of deploying one is writing a good system prompt. Done by hand it takes hours, and the quality drifts every time. This Skill turns that into one step that comes out the same way every time.

## Who it's for

- Builders learning AI automation who want a real, working artifact to study and adapt.
- People starting an AI agency who need a repeatable way to spin up receptionist agents.
- Anyone deploying a voice AI receptionist for their own business.

You should already know what Claude Code is. You do not need to have built a voice agent before.

## What's inside

One file, `SKILL.md`, with two complete prompt templates:

- **Starter tier.** Answers FAQs, runs intake one question at a time, and texts an SMS booking link as the call to action. No live calendar, no transfers. Principle driven, so it is short and cheap to run.
- **Full tier.** Adds real-time scheduling (check availability, book, update CRM, notify the team), emergency dispatch, and warm or cold call transfers with business-hours gating and a message fallback. Built as deterministic, numbered task flows so it stays reliable on the high-stakes paths.

Every business-specific detail is a `{{VARIABLE}}` token, so one template works for any client in any industry. You also get a per-industry defaults table, a tool catalog, a validation checklist, and a platform portability section.

The templates are written Trillet first. The runtime and tool-call syntax is Trillet native, and a dedicated section maps every token to its VAPI and Retell equivalent.

## Prerequisites

**Starter tier** has no prerequisites beyond a Trillet account with the SMS booking link tool configured.

**Full tier** requires backend workflows already built and connected before the prompt will work. Most of these are Make.com scenarios (or similar no-code workflows) exposed to the agent as tools via a Make.com MCP server or webhook. You need those workflows built and the exact tool names registered in Trillet before running this Skill. The prompt references those tool names directly, and if they do not exist in your platform the agent will fail mid-call.

## How to use it

1. Drop `SKILL.md` into your Claude Code project. A `.claude/skills/` folder works, or anywhere Claude can read it.
2. Ask Claude Code to generate a prompt. For example:
   > Generate a Full tier AI receptionist prompt for a plumbing company called Acme Plumbing, persona name Ava.
3. Answer the questions it asks (industry, services, transfer numbers, emergency policy), then paste the result into your platform's agent config.

The Skill tells Claude what to collect and what to never guess, including transfer numbers, emergency policy, and anything safety related. You stay in control of those.

## Why Trillet

The templates run on any of the major platforms, but they are tuned for Trillet because Trillet is the best fit for running this as an agency:

- **White label.** Your client never sees Trillet. They see your brand and your logo.
- **Your own Stripe.** When a client pays their monthly fee, the money goes straight to you.
- **A separate sub-account per client**, so every build is isolated and clean.
- **Fast demos.** You can build a working demo from a business website in a few minutes and bring it to the first sales call.

If you want to start with Trillet, here is my affiliate link: https://www.trillet.ai/plans?via=automason

## Watch the full build

A start-to-finish walkthrough of how I build and sell these: https://youtu.be/XV4EIVMZZxg

---

Built by Mason at Automate What Academy. Join the free community at https://www.skool.com/automate-what-academy/about for more tools, templates, and tutorials.
