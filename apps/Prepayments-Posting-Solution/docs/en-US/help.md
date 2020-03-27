In Customer/Vendor Posting Groups page, there's a new field **Prepayment Invoice Customer/Vendor Posting Group**.

User can specify a different Customer/Vendor group, that shall be used when solution corrects standard general ledger entries when Applying payments, other applications, removing applications.

Solution corrects the standard general ledger entry by posting additional entry to move debt amount to G/L account specified on field Prepayment Invoice Customer/Vendor Posting Group.

User must **add Job Que entries** with **CodeUnit 24013200** and **parameter** values "**CUSTOMER**" (for Customer prepayment invoices correction) and "**VENDOR**" (for Vendor prepayment invoices correction).

**On** Sales/Purchase **invoice** header **User must select manually** a different Customer/Vendor posting group.

**When posting Prepayment invoice from Sales/Purchase order**, then Customer/Vendor group specified on field **Prepayment Invoice Customer/Vendor Posting Group shall be automatically used**.
