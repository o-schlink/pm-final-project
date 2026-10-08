# PRD & Prototype Sprint (Module 4)

## Pick & scope with MoSCoW
- **The “Now” feature I’m scoping (name + one-line core description):** C2 Financing Basis Summary — Shows Responsible Payers whether the installment plan covers the total treatment cost, a single invoice, a co-payment, reimbursement-adjusted amount, or remaining balance before they commit.
- **My finalized Must-Haves (after overriding the AI):** Show the financed amount clearly before commitment.
Distinguish total cost, invoice amount, co-payment and remaining balance.
Explain what is not included in the installment plan.
Show monthly payment, duration and total repayment amount.
Use partner/service context so the payer recognizes the agreement.
- **What I demoted from Must → Should/Won’t, and why:** I demoted future-cost change explanations from Must to Should because the first pilot should test basic financing-basis clarity before expanding into dynamic cost handling.

I demoted reimbursement and co-payment explanations from Must to Should because they are important for orthodontics, but not required for the feature to function across all pilot cases.

I demoted payer/service-recipient role highlighting from Must to Should because it is highly relevant, but could expand the pilot toward actor-model redesign if treated as core scope.

I moved partner integration, configurable rule-engine work, later-invoice support, eligibility redesign and payment servicing to Won’t-Have Now because they would turn the pilot into a platform build instead of a focused clarity test.

## Generate your Simplified PRD
- **One thing my PRD makes explicit that a vague brief would have missed:** The PRD makes explicit that the prototype is not about building a full installment-management platform, partner integration, eligibility logic or payment servicing. It focuses narrowly on testing whether Responsible Payers can understand what amount is financed, what is excluded, and what commitment they are making before confirmation. This prevents the team from turning a clarity hypothesis into a broad platform rebuild before validating the actual contact reasons.

## Prompt-to-prototype sprint
- **Where did the prototype reveal a gap in my PRD logic? (what I had to update):** The prototype revealed that the PRD needs clearer sample scenarios and field-level logic. It says the summary should distinguish total cost, invoice amount, co-payment and remaining balance, but it does not fully define which sample case is shown, how the selected basis is explained, or how exclusions and possible future changes should appear in the UI. I would update the PRD with one concrete pilot scenario, clearer labels, and acceptance criteria for whether the payer can correctly identify what is financed and what is excluded.
- **My prototype, as a link or a screenshot (publish or share from your tool; in Lovable that is Share → Share Preview, in Bolt Publish → Web. No share URL? Screenshot the working flow):** Prototype generated locally / screenshot added to deliverables.
