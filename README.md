# claude-skills-for-sales

Claude Skills for account research and sales execution. Each skill is a self-contained folder any sales team can drop into Claude and run, not tied to one company or product.

## Why this exists

I'm an Account Executive at Databricks. These skills started as internal tools I built to speed up my own account research and deal prep, then rebuilt so any sales team can use them.

## What's here

The first skill is live: an ICP fit and account intelligence brief generator. Give it your ICP once and a target company, and it researches the company, scores the fit, and writes a one-page brief on how your product fits them (github.com/anthropics/skills has the full Agent Skills spec).

More skills are coming, starting with a signal-based account prioritization skill.

## How to use a skill

Once a skill is published here, drop its folder into Claude (Claude.ai, Claude Code, or the API) and point Claude at it. Each skill's own README covers the exact setup.

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
