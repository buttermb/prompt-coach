# Synthetic examples

These examples are invented and contain no real session excerpts or private project details. They demonstrate intended behavior, not measured quality results.

## 1. One-shot writing

Input:
> Improve this prompt: Write a friendly reply declining a dinner invitation. Under 30 words. Don't invent an excuse.

Expected approach: one-shot. A compact prompt should preserve the word limit and avoid invented reasons. It should not demand three mandatory rounds or execute sending.

Example optimized prompt:
```text
Write one friendly reply declining the dinner invitation below. Use fewer than 30 words. Thank the sender, decline clearly, and do not invent an excuse or future plans. Return only the reply.
Invitation: [PASTE INVITATION]
```

## 2. Coding with missing evidence

Input:
> Improve this prompt: Fix the checkout crash. Plan only for now. Don't deploy. I haven't attached the repository or logs.

Expected approach: blocked by evidence for a concrete diagnosis. Provide a preparation/diagnostic prompt, preserve plan-only, and name the needed error/reproduction/source inputs. Do not claim a root cause or fabricate repository access.

## 3. Research then decision

Input:
> Compare three appointment-booking tools for a small salon, then draft a migration plan for the option I choose. Budget is $60/month. Don't sign up or contact vendors.

Expected approach: two stages with an actual user-choice boundary. Stage one verifies current prices and requirements and produces a comparison. Stage two receives the selected option and produces a migration plan. No accounts or outreach.

## 4. Preserve versus recreate an image

Input:
> Improve this prompt: Export the approved poster as a PNG. Keep the image and its 2:3 aspect ratio unchanged; don't redesign it.

Expected approach: one-shot export instructions, conditional on access to the approved source. Preserve the artwork, request a downloadable file, and avoid claiming print readiness without production specifications.

## 5. Quantitative estimate

Input:
> Improve this prompt: Estimate a shared server's monthly electricity cost from a two-hour power reading. I want running cost, not API retail price.

Expected approach: identify power units, observation period, uptime, electricity tariff, and allocation assumption. Use a range for unknowns. Do not replace infrastructure cost with API rates.

## 6. A targeted follow-up

Input:
> The revised prompt produced a useful report, but it omitted the cancellation fees. Improve the next prompt without restarting the work.

Expected approach: request only missing cancellation terms and their sources, then update affected comparisons. Preserve correct prior content; do not require a full rewrite merely for another iteration.
