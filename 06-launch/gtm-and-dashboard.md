# GTM Launch Plan, Riverty business-unit case

| Field | Value |
|---|---|
| Feature | Financing Basis Summary before installment agreement confirmation |
| Goal | Conversion |
| Launch tier | M, Targeted |

## Goal & Audience
- **Goal:** Conversion. The feature is intended to reduce post-creation manual contact by helping Responsible Payers understand what amount is financed, what is excluded, and what commitment they are making before they confirm the installment agreement.

- **Target audience:** Primary audience: Responsible Payers who are about to confirm an installment agreement and need to understand what the agreement covers. Secondary audience: Customer Support and partner-facing teams who need to understand the new summary screen, use consistent language, and monitor whether contact reasons decrease.

## Launch Tier
- **M, Targeted:** This is a targeted experiment for a specific flow and audience, not a broad market launch. The feature affects Responsible Payers during installment agreement confirmation and needs focused communication to internal support, partner-facing teams, and selected pilot partners. A larger multi-channel launch would risk over-investing before the experiment proves that the summary screen reduces post-creation manual contact.

## Channels
1. **Owned: In-flow product communication** — The Financing Basis Summary appears directly in the installment confirmation journey for eligible Responsible Payers in the experiment variant.
2. **Owned: Internal enablement note** — Customer Support and partner-facing teams receive a short explanation of the experiment, the screen content, approved wording, escalation rules, and contact-reason tagging instructions.
3. **Owned: Partner-facing pilot briefing** — Selected pilot partners receive a focused briefing on what the payer will see, what partners should and should not explain, and how to route questions without changing their onboarding or sales behavior.

## Enablement & Assets
Experiment brief, support FAQ, partner pilot one-pager, screenshot or demo of the Financing Basis Summary, approved payer-facing wording, escalation guidance, and a short contact-reason tagging guide for support teams.

## Ownership, Budget & Timeline
- **Ownership & budget:** Launch lead: Product Manager. Product Manager owns launch plan, experiment scope, success metrics and go/no-go recommendation. UX/Product Design owns summary-screen copy and interaction clarity. Engineering owns implementation, tracking and experiment setup. Data/Analytics owns sample-size validation, metric definition, readout and contact-reason analysis. Customer Support owns enablement, FAQ usage and consistent contact-reason tagging. Partner-facing teams own pilot partner briefing and feedback collection. No paid media budget; budget need is limited to team capacity and enablement assets.
- **Timeline:** Phase 1 — Pre-launch readiness: finalize screen copy, tracking, experiment population, support FAQ, partner briefing and QA. Phase 2 — Controlled experiment launch: release the Financing Basis Summary to the variant group only, with a 50 / 50 split where operationally acceptable. Phase 3 — Observation window: collect post-creation manual contact data for 30 days after agreement creation, plus activation and payment-health guardrails. Phase 4 — Readout and decision: analyze results after both arms reach at least 5,166 agreements and the full observation window is complete; decide ship, iterate, do not scale yet, or kill.

## Success Metrics
- **Metrics:** Primary success metric: post-creation manual contact rate for installment agreements, measured within 30 days after agreement creation. Diagnostic metric: correct understanding rate in a post-flow comprehension check, especially whether users can identify the financed amount and what is excluded. Guardrail metrics: agreement completion / activation rate must not drop by more than 1 percentage point versus control; payment health must not worsen, measured by direct debit return rate and extension rate versus control.
- **Bad signal to watch for:** Manual contact rate decreases, but agreement completion / activation drops, payment health worsens, or comprehension-check failures / help-intent clicks increase in the variant. This would suggest the screen may be creating hesitation, confusion or lower-quality commitments rather than solving the underlying problem.
- **Likely post-launch decision:** Ship only if the variant reduces post-creation manual contact rate significantly and guardrails remain healthy. Iterate if the contact rate improves directionally but the effect is below the 2 percentage point MDE, or if the diagnostic metric shows that users still do not reliably understand what is financed and what is excluded.
