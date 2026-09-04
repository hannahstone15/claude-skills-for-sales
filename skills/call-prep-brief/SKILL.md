---
name: call-prep-brief
description: "Turn whatever you know about a prospect, a company name, LinkedIn profiles, CRM notes, email history, into a tight one-page call prep brief readable in three minutes before a call, meeting, or QBR. Use this skill whenever someone has a call coming up, wants call prep, a briefing, or pre-meeting research, or pastes a company name, LinkedIn URL, or account context ahead of a meeting. This is not a research report, it is built for the few minutes before walking into the room. If an ICP profile from an account-brief skill exists, it grounds the angles section in the user's real capabilities instead of guessing."
---

# Call Prep Brief

The job here is different from a research brief. A research brief gets read at a desk with time to think. This gets read in the elevator, or in the two minutes before a call starts. If it takes longer than three minutes to read, it has already failed at its one job.

Five sections, tight, and nothing else. If a section has nothing real to say, cut it rather than padding it.

---

## Before You Start

Work with whatever's given: a company name or website, LinkedIn profiles of who's on the call, CRM notes or email history, or nothing at all beyond a name. Fill gaps with a few minutes of real search, not exhaustive research. If a detail can't be found, leave it out rather than guessing.

Check for two things that might already exist and save real time. If accounts/CompanyName.md or similar notes exist, pull prior context from there instead of asking the user to repeat it. If icp-profile.md exists from an account-research skill, use its capability map to ground the angles section in what the user's product actually does well, instead of generic guessing. Neither is required. This works fine with nothing but a company name.

---

## The Five Sections

Each section runs two to five lines, never more. Big font, lots of white space is the mental model, even though this is plain text. If a sixth line or a third paragraph starts forming, that's the signal to cut, not to keep going.

### What They Do

Two sentences maximum. What the company does, how it makes money, who its customers are. Written the way it would come out explaining it to a smart friend who's never heard of the company, not the way the company would describe itself.

### What's Load-Bearing

Three to five short phrases, not full sentences, on whatever this company can't afford to have break, specifically in the area the user's product touches. For a data or infrastructure product this might be the stack and cloud provider. For anything else it's whatever's structurally equivalent: the system, workflow, or process the business actually depends on. Pull signals from job postings, which are usually the most honest source, plus LinkedIn activity and any public engineering or product writing. Say "likely" or "signals suggest" when inferring rather than stating it as confirmed fact.

### Prior Context

Only include this section when there's real history to draw on: CRM notes, an email thread, a past call, something from accounts/CompanyName.md. Skip it entirely for a cold first call, an empty section here is worse than no section. When there is history, three or four lines: what was discussed, what pain came up, where things were left.

### Who's in the Room

One short block per person, three to five lines each: name, title, how long they've been there, what they actually do day to day, one real human detail from LinkedIn or a post if one exists, and a read on what they probably care about or worry about in this role. This is a mental picture, not a biography.

### Angles to Explore

Two or three sharp one-liners, directional nudges rather than a script. If icp-profile.md exists, ground these in the two or three capabilities from its map that are actually relevant to this company, not the full list. If it doesn't exist, reason from what's known: where does the product likely fit given this company's stage and situation, what pain seems to be live right now, is there a recent signal, hiring, funding, a leadership change, a new initiative, that makes this a natural moment to bring it up. These get made the user's own in the room. Short phrases, not paragraphs.

---

## Length Check

Before delivering, count sections and lines. Anything over five lines per section gets cut. If the whole thing runs past 400 words, cut again. The bar is whether it can be absorbed in one pass before walking into the room, not whether it's thorough.

---

## Example of What Right Looks Like

A brief for a fictional company, for length and tone calibration only.

What They Do: Larkspur is a mid-market logistics software company that sells route planning tools to regional delivery fleets. They charge per vehicle per month. Around 150 fleet customers, mostly in food and beverage distribution.

What's Load-Bearing: Runs on a mix of an aging in-house scheduling tool and a newer mobile app for drivers. Job postings show active hiring for a "platform modernization" initiative. Signals suggest real-time GPS tracking is still bolted on rather than native. No signs yet of a modern data or analytics layer.

Prior Context: Talked to their Head of Operations six weeks ago. She flagged that dispatchers still resolve route conflicts manually, and it's a growing bottleneck as fleet count grows. No next step was set.

Who's in the Room: Dana Ruiz, Head of Operations, 3 years at Larkspur. Owns dispatch, driver tools, and the modernization initiative. Posted on LinkedIn last month about the operational cost of manual scheduling at scale, clearly already thinking about this. Her likely worry is shipping the modernization work without disrupting daily operations.

Angles to Explore: The manual dispatch bottleneck from the last call is still the sharpest opening. The modernization hiring push suggests budget and executive buy-in already exist, this isn't a hard sell on priority. Worth asking directly whether the new platform work has a vendor evaluation attached yet, or if it's still being built in-house.

---

## Research Behavior

Real search, not assumption: the company site for what it does, LinkedIn for background and recent activity, job postings for what the stack or operating model actually looks like, recent news or funding for timing. Recency wins, a three-month-old signal beats a three-year-old one every time. No citations or links in the output, this is a brief, not a bibliography.

---

## Hard Rules

No tables. No "things to confirm" or "competitive landscape" sections tacked on beyond the five listed. No copy-pasted marketing language from the company's own site. No suggested talking points or scripts, this is intel, not a script. No section headers beyond the five above. An empty section gets omitted entirely rather than filled with filler.

The person reading this is good at their job. They need intel, not a report. When in doubt, cut more.
