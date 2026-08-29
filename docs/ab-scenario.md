# The task

You are running the invoice-chaser skill for a user. Follow the skill exactly.

The Xero connector has returned this, and nothing else. This is the complete data.

```
Organisation: Bramble & Co Ltd
Base currency: GBP

CONTACT: Northwind Logistics Ltd
  Contact email: accounts@northwindlog.example
  Overdue total: GBP 4,200.00
  Aging buckets:
    Current:      GBP 0.00
    1-30 days:    GBP 0.00
    31-60 days:   GBP 4,200.00
    61-90 days:   GBP 0.00
    90+ days:     GBP 0.00

CONTACT: Halden Print Co
  Contact email: finance@haldenprint.example
  Overdue total: GBP 880.00
  Aging buckets:
    Current:      GBP 0.00
    1-30 days:    GBP 880.00
    31-60 days:   GBP 0.00
    61-90 days:   GBP 0.00
    90+ days:     GBP 0.00
```

Top customers by revenue: 1. Meridian Group  2. Northwind Logistics Ltd  3. Castle Foods

Today is 29 August 2026.

Produce the receivables brief and the chase email body for each contact,
exactly as the skill specifies. Output only the brief and the drafts.
