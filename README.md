# WantAce — Solutions Engineer Intern Submission

**Candidate:** Vamshi Vardhan  
**Repository:** https://github.com/vamshivardhan22/wantace-intern-submission  
**Website:** https://vamshivardhan22.github.io/wantace-intern-submission/

## Important status note
This repository was populated as a rapid publication scaffold because the referenced `wantace-submission.zip` was not available in the files I could access. Do **not** claim that every deliverable is complete. Part A fieldwork, genuine owner quotations and photos, Part D content based on your actual audit, and the Part E recording/evidence must be added by you if they have not already been completed. Never invent observations, figures, or recordings.

## Part A — Real-business audit (must be based on your actual visit/call)
Choose a business that makes, processes, or repairs products. Trace one order from enquiry through production, quality check, delivery, and payment. Record the actual tools used, recurring issue, frequency and impact where known. Include two genuine direct quotes and photos of tracking methods only with permission.

Fill these before submission:
- Business name/type and area:
- Owner/manager and date of interaction:
- Products and approximate order volume (only if confirmed):
- Workflow:
- Tracking tools actually seen:
- Biggest observed problem and confirmed impact:
- Two direct owner quotes in their original wording:
- Evidence/photos and permission status:

## Part B — Requirement document for Vardhan Steelware

### Problem statement
The available case notes suggest that the owner has difficulty seeing where orders are stuck and staff depend on separate updates. Start by solving traceability and status visibility. Do not treat AI forecasting or full ERP replacement as the first priority without evidence that the core workflow is reliable.

### Data-quality issues to validate against the original client pack
- Gupta Traders' 200-piece Kadai order appears twice with different statuses; establish whether it's a duplicate, split shipment, or history of a status change.
- Jain Crockery's 150-piece Kadhai order appears repeated; validate against the source.
- One order has no customer name.
- One pending order has quantity in kilograms but no rate.
- A customer/order is held due to older payment dues.
- A negative quantity appears to represent a return; capture it as a traceable return rather than silently overwriting the original record.
- Outsourced polishing notes mention 420 kg sent, 1,180 pieces returned, and a reported 6 kg shortage. Since units differ, reconcile only after confirming measurement/conversion rules and batch identity.

These are flags from the available case notes, not proof of deliberate errors. Validate them against the original documents before finalizing.

### Current process to confirm
Customer enquiry → order entry → production → external polishing → received-quantity reconciliation → packing → dispatch → accounts/payment tracking.

### Proposed Phase 1 scope (recommendations to confirm with client)
1. Central order register with immutable unique order IDs.
2. Customer and item details with required-field checks.
3. Simple stages/statuses with who/when updated.
4. Partial dispatches and returns as separate linked transactions.
5. Outsourced processing batches with sent/received quantity, unit, date, and exception reason.
6. Payment hold and missing-information flags.
7. Mobile-friendly order status and a small daily exception report.

**Defer initially:** AI sales forecasting, broad ERP replacement, and complex marketplace integrations until order data and staff workflows are validated.

### Initial entities and relationships
- **Customer:** customer ID, name, contact, payment status.
- **Order:** order ID, customer ID, order date, status, owner.
- **Order item:** line ID, order ID, product, quantity, unit, rate.
- **Processing batch:** batch ID, linked line/order, sent quantity/unit, received quantity/unit, shortage/variance, contractor, dates.
- **Dispatch:** dispatch ID, order ID, quantities dispatched by line, date, delivery reference.
- **Return:** return ID, original order/dispatch, item, quantity/unit, reason, date.
- **Payment:** payment ID, customer/order reference, amount, date, status/reference.

One customer may have multiple orders; an order may have multiple line items, dispatches, returns, and processing batches. Unit conversion, stock management, and accounting integrations require explicit client rules.

### Roles and daily reports
- **Suresh (owner):** high-level status, overdue orders, payment holds, exceptions.
- **Kunal (order coordination):** create and correct orders, monitor progress.
- **Ramesh (production/dispatch):** update production stage and dispatched quantities.
- **Munshi ji (accounts):** payment holds and financial reconciliation.
- **Contractors:** external access only if requested and permissions are agreed.

Useful daily reports:
1. Orders pending by stage and age.
2. Orders on hold, grouped by payment, missing data, or operational blocker.
3. Processing reconciliation: sent vs received quantities, by compatible unit, with unresolved exceptions.

### Questions for the next client call
1. Who has final purchasing and budget authority?
2. Who owns and edits the order sheet?
3. How are split orders and partial dispatches captured?
4. Why did the previous ERP fail to gain adoption?
5. What are the approved units and conversions for outsourced processing?
6. Who approves returns and record corrections?
7. What defines an overdue order?
8. Which report is most important each morning?
9. Which devices/users need access?
10. What deadline and measurable pilot success criteria should be agreed?

### Primary risk and mitigation
**Risk:** poor adoption if staff must enter the same details in multiple places.  
**Mitigation:** pilot a small mobile-friendly workflow with a limited set of live orders, keep updates minimal, train the actual users, and review feedback before expanding.

## Part C — Account Executive handoff
- **Core pain:** low visibility into order status and operational blockers.
- **Signals to investigate:** repeated-looking order rows, missing values, payment holds, returns, partial dispatches, and external processing reconciliation.
- **Possible objections:** previous ERP failure, complexity, rollout time, and uncertain value of advanced functionality.
- **Suggested next step:** conduct a workflow walkthrough with the owner, order coordinator, dispatch, and accounts staff; agree the smallest useful pilot, decision-maker, deadline, and success measures.
- **Positioning:** demonstrate a simple order-tracking workflow first. Avoid promising AI forecasts or broad integrations before the data and workflow are trustworthy.

## Part D — LinkedIn post and Meta ad
The assignment asks that public content be based on a finding from your own Part A audit and anonymized. Complete this after the audit. Use only a verified pain point; do not claim measurable savings or results unless measured.

**LinkedIn post template:**  
“During a recent conversation with a small [type of business], I noticed [specific verified workflow issue]. When order information is spread across [tools actually observed], it can be difficult to answer [question the owner actually struggled with]. A practical starting point is [small realistic change]. For growing manufacturers, better visibility often begins with a clear owner, consistent order ID, and a reliable status update—not a complex system on day one.”

**Meta ad draft (customize to evidence):**
- Primary text: “Still checking multiple places to find an order update? Start with a clearer view of order status, pending work, and dispatch exceptions. Built around the workflow your team already uses.”
- Headline: “Know Where Every Order Stands”
- Creative concept: a simple before/after illustration of scattered registers/messages versus one status board. Do not imply an actual customer result or endorsement unless permission and evidence exist.

## Part E — Demo and AI usage
Add the genuine recording link and the actual demo artefacts required by the original brief. Before recording, test all links in a private window and ensure the demo statements match what is implemented. Do not claim unperformed tests.

## AI usage disclosure
See `AI_Usage_Note.txt`. Edit it to match your real use of AI and all verification you personally performed.

## Publish using GitHub Pages
1. Open repository **Settings → Pages**.
2. Under **Build and deployment**, select **Deploy from a branch**.
3. Choose branch **main** and folder **/(root)**, then Save.
4. Wait for the Pages deployment, then verify the public website in a private/incognito window.
5. Ensure all required original evidence, demo recording and final deliverables are present before you submit.

## Final checklist
- [ ] Part A has real interaction, direct quotations, and permissioned evidence.
- [ ] Client-pack facts are checked against source files.
- [ ] Assumptions and recommendations are labeled, not presented as client-confirmed facts.
- [ ] Part D content reflects actual Part A findings and does not name Vardhan Steelware.
- [ ] Part E contains the required real demo recording and evidence.
- [ ] AI note accurately describes the tools used and human verification completed.
- [ ] Repository and Pages site are public and every link works.
