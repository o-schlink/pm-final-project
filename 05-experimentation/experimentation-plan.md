# A/B Experiment Brief, Riverty business-unit case

## Parameters
| Parameter | Decision |
|---|---|
| Feature under test | Financing Basis Summary before installment agreement confirmation |
| Persona | Responsible Payer: a parent or self-paying customer who is financially responsible for a service and needs to understand exactly what the installment agreement covers. |
| Expected outcome | Responsible Payers better understand what amount is financed, what is excluded, and what commitment they are making before confirmation, resulting in fewer manual contacts after agreement creation. |
| Primary success metric | Post-creation manual contact rate for installment agreements |
| Baseline rate | 14.6% overall baseline: 46.2K of 316K installment agreements have a manual contact attempt after creation. |
| Guardrail metric | Agreement completion / activation rate |
| Guardrail boundary | Synthetic target: completion / activation rate must not decrease by more than 1 percentage point versus control. Validate boundary with real funnel baseline before launch. |
| Second guardrail | Payment health must not worsen: direct debit return rate and extension rate must not increase versus control. |
| Minimum Detectable Effect | Synthetic target: 2 percentage point absolute reduction in post-creation manual contact rate, from 14.6% to 12.6%. |
| Sample size per arm | 5,166 agreements per arm |
| Traffic split | 50 / 50 between control and variant, if operationally acceptable. |
| Test duration | Run until each arm reaches at least 5,166 agreements and the full 30-day post-creation contact observation window is complete. Synthetic planning assumption: 4-6 weeks to enroll users, plus the observation window, depending on eligible traffic volume. |
| Significance threshold | p < 0.05, 80% power |

## Control vs. Variant
- **Control (A):** The current experience presents the installment agreement without a dedicated financing-basis summary before confirmation. The payer can see payment terms, but it is not made sufficiently clear whether the plan covers the full treatment cost, a single invoice, a co-payment, a reimbursement-adjusted balance, or another remaining amount. As a result, Responsible Payers may confirm without fully understanding what is financed, what is excluded, or what may change later, which can lead to post-creation manual contact.
- **Variant (B):** Add one pre-confirmation Financing Basis Summary screen. The screen clearly shows the financed amount, financing basis type, included and excluded amounts, monthly payment, duration, total repayment amount, and a plain-language explanation of what the installment plan covers. It also highlights that future invoices, treatment changes or expected reimbursements are not included unless explicitly shown.
- **Held constant (isolation check):** No changes to eligibility logic, risk decisioning, pricing, interest calculation, contract generation, payment collection, partner integration, onboarding flow, traffic source, reminder logic, post-creation servicing, or reminder communication. The only intended difference between control and variant is one added Financing Basis Summary screen before confirmation.

## Hypothesis
> I believe that adding one pre-confirmation Financing Basis Summary screen for Responsible Payers will reduce post-creation manual contact rate by improving payer understanding of what amount is financed, what is excluded, and what commitment they are making before confirmation.
>
> We will measure success as a synthetic target of 2 percentage points absolute reduction in post-creation manual contact rate, from 14.6% to 12.6%, with p < 0.05 and 80% power. We will protect agreement completion / activation rate and payment health throughout the test.

We will measure success as a synthetic target of 2 percentage points absolute reduction in post-creation manual contact rate, from 14.6% to 12.6%, with p < 0.05 and 80% power. We will protect agreement completion / activation rate and payment health throughout the test.

## Shipping criteria
> We will **ship** if the variant reduces post-creation manual contact rate by at least 2 percentage points versus control, from 14.6% toward 12.6%, with p < 0.05 and at least 5,166 agreements per arm observed through the full 30-day post-creation contact window.
>
> We will **not ship** if agreement completion / activation rate drops by more than 1 percentage point versus control, or if payment health worsens, measured by direct debit return rate or extension rate increasing versus control.
>
> We will **iterate** if the variant directionally reduces post-creation manual contact rate but the effect is below 2 percentage points or does not reach statistical significance, while guardrails remain healthy.
>
> We will **not scale yet** if manual contact rate improves but comprehension or contact-reason data does not support financing-basis confusion as the driver.
>
> We will **kill** if the primary metric shows no improvement or worsens, or if either guardrail is breached.
>
> The read date is fixed after both arms reach at least 5,166 agreements and the full 30-day post-creation contact observation window is complete. No results will be reviewed before this point.
