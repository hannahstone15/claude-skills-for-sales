# claude-skills-for-sales

Claude Skills for account research and sales execution. Each skill is a self-contained folder any sales team can drop into Claude and run, not tied to one company or product.

## Why this exists

I'm an Account Executive at Databricks. These skills started as internal tools I built to speed up my own account research and deal prep, then rebuilt so any sales team can use them.

## What's here

Three skills are live. The first is an ICP fit and account intelligence brief generator: give it your ICP once and a target company, and it researches the company, scores the fit, and writes a one-page brief on how your product fits them. The second is a sales voice kit: it researches a prospect the way top sellers do, then drafts a first touch, a follow-up bump, or a compressed executive email, all written in your own voice instead of generic AI phrasing. The third is a call prep brief: turns whatever you know about a prospect into a tight one-pager you can read in three minutes before a call, meeting, or QBR (github.com/anthropics/skills has the full Agent Skills spec).

More skills are coming, starting with a signal-based account prioritization skill.

## How to use a skill

Download the SKILL.md for the skill you want from its folder above. Create a new folder on your computer named after the skill, for example sales-voice-kit, and put the file inside it. Zip that folder. In Claude, go to Customize, then Skills, then Add, and upload the zip, then enable the skill once it's uploaded. After that, just use it in a normal chat, give it a company name for the account brief skill, or ask it to draft or rewrite a message for the voice kit, and Claude invokes the skill automatically.

## Structure

```
claude-skills-for-sales/
  skills/
    skill-name/
      SKILL.md
      supporting-files
```

## License

MIT. Use these however you want.
