# C2 Financing Basis Summary

> Helping Responsible Payers clearly understand what amount is financed, what is excluded, and what commitment they are making before confirming an installment agreement.

**Oliver Schlink · Product School PM Cohort · Oct 2026** · https://github.com/o-schlink/pm-final-project

Prototype: https://github.com/o-schlink/pm-final-project/tree/main/06-launch

---

## Final Project Deliverables

### Slide 5 · Strategy
- **Problem:** Customers cannot clearly tell whether a plan covers the full treatment cost, a single invoice, a co-payment, or a remaining balance.
- **Value proposition:** One clear pre-confirmation summary explains the financed amount, exclusions, monthly payment, duration, and total repayment.
Data-Backed Hypothesis
- **Hypothesis:** Because 14.6% of installment agreements have post-creation manual contact, we believe a clearer financing-basis summary can reduce manual contacts while protecting activation and payment health.
Key Signals
- Persona: Responsible Payer
- Primary signal: 14.6% manual contact baseline
- Synthetic target: 12.6%, a 2 percentage point absolute reduction
- Guardrail: activation rate and payment health must remain healthy

### Slide 6 · Research
- **Competitive analysis:** Responsible Payers rely on phone calls, emails, forwarded links, invoices, treatment plans and partner explanations to understand what they are paying for. The workaround is fragile because payer, service recipient and decision maker may differ, while invoices, co-payments and reimbursements happen at different times. Evidence gap: we still need to prove that financing-basis confusion is a top post-creation contact reason.
- **Journey map:** Receive payment option → Check payer vs. service recipient → Compare estimate, invoice, reimbursement and financed amount → Understand exclusions and future changes → Confirm only when the commitment is clear.

### Slide 7 · Blueprint
- **Roadmap:** NOW: C2 Financing Basis Summary, C3 Payment Commitment Preview, C12 Funnel & Contact-Reason Tracking. NEXT: plan-change impact preview, returned direct-debit resolution, partner-context communication. LATER: payer-role identification, adding later costs, plan-management hub. CUT: partner prefill and configurable rule-engine build until the clarity assumption is validated.
- **PRD highlights:** One pre-confirmation summary screen shows what is financed, what is excluded, the monthly payment, duration and total repayment. Out of scope: eligibility, risk, partner integration, payment collection and adding later invoices.
- **Prototype:** https://github.com/o-schlink/pm-final-project/tree/main/06-launch

### Slide 8 · Validation
A/B test one added pre-confirmation Financing Basis Summary screen against the current confirmation experience. Primary metric: post-creation manual contact rate within 30 days. Baseline: 14.6% overall, equal to 46.2K of 316K agreements. Synthetic MDE: 2 percentage point reduction, from 14.6% to 12.6%. Sample: 5,166 agreements per arm. Ship only if the contact-rate reduction is significant, guardrails remain healthy, and contact-reason data supports financing-basis confusion as the driver.

### Slide 9 · Launch
- **GTM:** Launch goal: Conversion. This is a targeted M-tier experiment for Responsible Payers in the installment confirmation flow, supported by Customer Support, partner-facing teams and selected pilot partners. Channels: in-flow product communication, internal enablement note and partner pilot briefing. The launch avoids broad awareness activity until the feature proves that clearer pre-confirmation information reduces manual contact.
- **Metrics:** Primary metric: post-creation manual contact rate within 30 days. Diagnostic metric: correct understanding rate and contact reasons tagged as financing-basis confusion. Guardrails: activation must not drop by more than 1 percentage point and payment health must not worsen. Bad signal: contacts fall while activation drops, payment health worsens, or help-intent / comprehension failures increase.

### Slide 10 · Story
- **Friction + aha:** The hardest part was separating real evidence from attractive AI-generated structure. AI helped us move fast, but it also smoothed over important tensions: payer clarity vs. partner workflow, vertical fit vs. scalable core, and contact reduction vs. healthy activation. The aha moment was realizing that the best first move is not the biggest platform solution, but a focused test of whether Responsible Payers understand what they are committing to.
- **Takeaways / next:** Good product work is less about generating features and more about making assumptions testable. Next, I would prove whether financing-basis confusion is a top contact driver with contact-reason tagging and comprehension checks before scaling the product bet.

---

Submitted to the Product Management Certification learning platform · Product School.
