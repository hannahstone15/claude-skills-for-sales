---
name: icp-fit-account-brief
description: >
  Research a target company and produce a one-page account intelligence brief scored against
    your Ideal Customer Profile (ICP). Use this skill when someone gives a company name or URL
      and wants to know if it's a good fit, wants an account brief, a one-pager, or research before
        writing outbound or taking a first call. On first use, the skill asks a few questions to learn
          the user's ICP: what they sell, what their ideal customer looks like, the signals that predict
            fit, and how their product's real capabilities map to real problems. That profile is saved
              locally and reused on every company researched after that, so the questions only get asked once.
              ---

              # ICP Fit & Account Intelligence Brief

              This skill turns a company name or URL into a one-page research brief: what the company does,
              whether it fits your Ideal Customer Profile, and specifically how your product would help them.
              It's built for anyone doing account-based selling, not for one company or product. The only thing
              it needs from you is your ICP, defined once.

              ---

              ## Step 0: Define the ICP (one-time setup)

              Before researching anything, check the working directory for icp-profile.md.

              If it exists, load it and skip to Step 1. If the user says "update my ICP" or the profile looks
              stale, walk back through this step and overwrite the file.

              If it doesn't exist, this is a first run. Ask the user five questions before doing any research.
              They can answer in one message, in whatever order is natural, and it doesn't need to be formal.

              First, what do they sell, in two or three sentences: what problem it solves, and for whom.
              Second, what does a great-fit customer look like: industry, company size (employee range or
              revenue), and stage, such as funded startup versus mature enterprise. Third, what signals tell
              them someone needs this: tech stack, job postings, team structure, workflows, pain points, or
              trigger events like a funding round, a leadership hire, or a product launch. Fourth, and most
              important, what are their product's three to six real capabilities, and what specific problem
              does each one solve. This is what turns a generic brief into one that sounds like it was written
              by someone who actually knows the product. A weak answer is "we have great analytics." A strong
              answer is "our real-time alerting catches inventory mismatches before they hit the count, which
              matters most for teams running multi-warehouse fulfillment." Fifth, who are their main
              competitors, and what do they typically win or lose on.

              Write the answers to icp-profile.md in the working directory, structured under those five
              headers, so every future run in this project reuses it without re-asking.

              ---

              ## Step 1: Check for Existing Notes

              If the user already has research, CRM notes, or a past brief on this account, ask for it or read
              it if they point to a file, and use it as a starting base instead of researching from scratch.
              Still fill any gaps in the eight sections below with fresh research.

              If the user keeps a running notes file per account, an accounts/CompanyName.md convention works
              well, and this skill will check there automatically if that folder exists. This step is optional;
              skip it entirely if there's nothing to check.

              ---

              ## Step 2: Research the Company

              Research depth matters more than breadth. Understanding one company well beats skimming twenty
              pages about it.

              Core research targets: the company website (homepage, product pages, about or team page), recent
              news (funding, acquisitions, product launches, executive hires), job postings (especially roles
              that reveal how the company actually operates day to day, which are usually more honest than the
              marketing site), the LinkedIn company page (headcount, growth rate, org structure), review sites
              like G2 or Capterra if it's a software company (what real customers value), and GitHub if it's a
              developer-facing company.

              For fit signals, pull the list straight from icp-profile.md, question three above. Note which
              signals are present, which are absent, and anything ambiguous. Don't invent signals that aren't
              in the ICP profile. If research turns up something that seems relevant but wasn't listed, flag it
              as a possible addition to the ICP rather than silently treating it as a scoring factor.

              ---

              ## Step 3: Score ICP Fit

              Score the company 1 to 5 against the ICP profile from Step 0. Keep it simple, one clear reason
              per score, no double-labeled tiers.

              A 5 means the company matches the ICP closely: right industry, right size, multiple strong fit
              signals present. A 4 means a strong match with one or two gaps, such as the right signals but a
              smaller size than ideal. A 3 means a plausible fit, with some signals present but industry, size,
              or stage is a stretch. A 2 means a weak fit, mostly missing signals, and would need an unusual
              reason to prioritize. A 1 means not a fit at all: wrong industry, wrong size, or no signals
              present.

              Include the score and a one-sentence reason in the brief header. If the score is under 3, say so
              plainly rather than inflating it. A brief that's honest about a weak fit is more useful than one
              that oversells every account.

              ---

              ## Step 4: Build the Brief

              Eight sections. Write each one from the actual research, not from a template. Specific and
              slightly rough beats generic and polished. A vague paragraph that could describe any company in
              the industry is worse than a short one that couldn't apply to anyone else.

              ### 1. What They Do

              One tight paragraph. What problem do they solve, who's the customer, what's the core product.
              Write it as if explaining to someone who has never heard of the company. Avoid jargon, or define
              it if it's unavoidable.

              ### 2. Business Model

              How do they make money: subscription, usage-based, marketplace, transaction fees, services? Who
              pays, and roughly how much if that's known? What's the growth trajectory? If exact revenue isn't
              public, describe what is: funding stage, headcount growth, hiring pace.

              ### 3. How It Works (Technical)

              What does the product actually do under the hood, as best as can be inferred? What does it
              ingest, process, or serve? What does it integrate with? Rough, well-labeled inference, such as
              "likely a multi-tenant SaaS on AWS based on their job postings and stack mentions," is more useful
              than skipping the section.

              ### 4. Differentiators

              What makes them different from competitors: depth of data, proprietary technology, speed,
              integrations, vertical focus, price? List three to five real differentiators from the research,
              not marketing copy.

              ### 5. Why Customers Choose Them

              What specific pain does this company solve that customers couldn't solve elsewhere? Quote real
              customer language where it's available, from reviews, case studies, or testimonials. This section
              reveals what the company's own customers care about, which usually predicts what will land in a
              sales conversation with them.

              ### 6. Competitor Set

              Their three to five main competitors, what each competes on, and who tends to win. Useful for
              framing: if they're already winning against a competitor on some axis, that's often a lever for
              the "how we fit" section.

              ### 7. Proof Signals

              Evidence that this company is on a growth path or facing the kind of scale that makes your
              product relevant. Funding rounds, headcount growth (especially in the function your product
              serves), new product launches, expansion announcements, job postings, public statements about
              relevant challenges, or any signal of an existing tool they might be outgrowing or replacing.

              ### 8. How Your Product Fits This Company

              The most important section, and the one the whole brief exists to set up. The question to answer
              is: if you're on a call with the right person at this company, what problem are you solving for
              them, specifically?

              Structure it in four parts. First, their business and what depends on the problem the product
              solves: what's mission-critical to how this company operates or makes money, in the area the
              product touches, and what breaks if it's broken. Second, where the product creates leverage: pull
              from the capability map in icp-profile.md, question four, and use only the two to four
              capabilities that are genuinely relevant to this specific company, not the full list, naming the
              exact problem each one solves for them rather than a generic feature description. Third, the
              critical failure scenario: one or two sentences on what breaks for this company if the problem
              goes unaddressed, naming a real business consequence rather than a vague "issues could arise."
              Fourth, the recommended entry angle: given everything above, the single most compelling reason to
              bring this up with the company right now, in one sentence. This becomes the hook for outbound.

              ---

              ## Step 5: Deliver the Brief

              Default to a clean Markdown document. It reads well everywhere and doesn't depend on anything
              else being installed.

              If the user wants a polished, presentation-ready version and the docx skill is available, offer
              to build a styled Word document instead. Use letter size with 0.75 inch margins and a legible
              standard font throughout. Add a title banner with the company name, "Account Intelligence Brief,"
              and the ICP fit score. Give section headers a consistent accent color, using the user's brand
              color if they have one or a neutral dark navy and red pairing as a default. Give the "how your
              product fits" section slightly more visual weight, since it's the payoff of the whole brief. Keep
              it under two pages; if it's running long, tighten section 3 and section 6 first.

              Save output to briefs/CompanyName_Account_Brief.md (or .docx) relative to wherever the skill is
              being run, unless the user specifies a different location.

              If the user keeps an accounts/CompanyName.md notes file, as described in Step 1, append a short
              research log entry with the date and a one-line summary rather than overwriting anything already
              there.

              ---

              ## Quality Check Before Delivering

              Confirm that the "how it fits" section names specific capabilities tied to this company's actual
              situation, not generic product marketing. Confirm the ICP score is backed by specific evidence,
              not a gut feeling. Confirm the critical failure scenario names a real consequence, not just
              "problems could occur." Confirm the brief is under two pages; if not, cut section 3 and section 6
              down first. And if the fit score is 2 or lower, confirm the brief says so plainly instead of
              softening it.

              ---

              ## After Delivering

              Share the file. State the ICP score and the recommended entry angle in one or two sentences.
              Then offer to turn the brief into a first-touch outbound message.
              

              ---
              
