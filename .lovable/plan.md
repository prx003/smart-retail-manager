# Quick Run Command POS import and admin controls

## Goal
Bring the supplied grocery POS app into `/` and make the requested staff, invoice, GST, bill-editing, and product-offer controls administrator-only.

## Work
1. Import the public repository’s application code and existing visual design, excluding its `.env`, generated build output, dependencies, and repository metadata. Record missing source data and user exports as pending.
2. Establish the app’s existing Cloud schema, then tighten role access and add a protected server-side flow for administrators to create Cashier and Inventory Staff accounts. Keep role assignments in the dedicated roles table; remove self-service staff creation.
3. Complete the admin workflows for bill design settings, GST settings, editing saved bills, and setting product offers. Enforce the same restrictions in database access, not only by hiding controls.
4. Verify the preview, role-gated workflows where authentication allows, routes, and app behavior; hand off missing source records and user identities for later import.

## Technical notes
- Retain the repository’s TanStack Start, offline IndexedDB, and Cloud sync architecture; migrate its schema into Lovable Cloud.
- Do not copy the repository `.env` or expose privileged credentials in the browser.
- Existing customer, product, invoice, and user records were not included with the repository; request sanitized exports after the preview.
