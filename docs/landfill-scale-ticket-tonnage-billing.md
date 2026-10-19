# Landfill Scale Ticket Reconciliation & Automated Tonnage Overage Billing

**Roll-off scale ticket software** reconciles transfer station weight slips against a customer's included container tonnage allowance to eliminate unbilled disposal overages.

In [**RollOS Tonnage Billing**](https://rolloffdumpstersoftware.com/features/tonnage-billing), small and mid-size haulers (**1 to 25+ trucks**) automate post-pickup overage calculations and settle excess weight and rental-day extensions directly against the customer's vaulted Stripe card on file. Return to the main [**dumpster rental management software**](../README.md) documentation hub.

---

## Overage Settlement Formula & Calculation Logic

When a driver completes a pickup and logs the landfill scale house ticket via their [**1-Tap SMS Magic Link**](https://rolloffdumpstersoftware.com/features/driver-routes), RollOS computes the final settlement invoice using the following deterministic formula:

```text
Net Debris Weight (Tons) = Gross Truck Weight (Tons) - Tare Weight (Tons)
Billable Overage Tons    = MAX(0, Net Debris Weight - Included Tonnage Allowance)
Tonnage Overage Charge   = Billable Overage Tons × Contractual Per-Ton Overage Rate ($/Ton)

Billable Extra Days      = MAX(0, Total Days On Site - Included Rental Days)
Extension Charge         = Billable Extra Days × Daily Extension Rate ($/Day)

Total Post-Pickup Charge = Tonnage Overage Charge + Extension Charge + Prohibited Item Fees
```

Haulers can generate itemized customer receipts using the built-in billing engine or reference the free [**Commercial Roll-Off Dumpster Invoice Template**](https://rolloffdumpstersoftware.com/templates/dumpster-invoice).

---

## Standard C&D Material Density Reference Table

To help dispatchers and customers estimate container weight before a haul, the [**RollOS Tonnage & Overage Calculator**](https://rolloffdumpstersoftware.com/tools/tonnage-calculator) uses standard construction and demolition (C&D) bulk density benchmarks:

| Debris Material Type | Average Weight per Cubic Yard (lbs/yd³) | Estimated 10-Yard Bin Weight (Tons) | Estimated 20-Yard Bin Weight (Tons) | Recommended Container Cap |
| :--- | :--- | :--- | :--- | :--- |
| **Household Junk / Estate Cleanout** | 250 – 350 lbs/yd³ | 1.25 – 1.75 Tons | 2.50 – 3.50 Tons | 10yd to 40yd |
| **Mixed Construction & Demolition (C&D)** | 400 – 600 lbs/yd³ | 2.00 – 3.00 Tons | 4.00 – 6.00 Tons | 10yd to 30yd |
| **Asphaltingle Roofing Tear-Off** | 700 – 850 lbs/yd³ | 3.50 – 4.25 Tons | 7.00 – 8.50 Tons | 10yd or 15yd (Weight-Limited) |
| **Dry Dirt, Topsoil & Yard Fill** | 1,800 – 2,200 lbs/yd³ | 9.00 – 11.00 Tons | *Exceeds Single-Axle Legal Limit* | 10yd Low-Boy (Half-Fill) |
| **Broken Concrete, Brick & Asphalt** | 2,400 – 4,000 lbs/yd³ | 12.00 – 20.00 Tons | *Exceeds Hoist/Axle Limit* | 10yd Heavy-Debris Can Only |

---

## Related Technical Specifications
* **Previous Specification:** [**← Zero-App Driver SMS Magic Link Routing & Proof-of-Service Protocol**](./driver-sms-magic-link-routing.md)
* **Next Specification:** [**2026 Waste Hauling Software TCO & Vendor Migration Matrix →**](./waste-hauling-software-pricing-matrix.md)
* **External Resources:** [**Google Sites Resource Hub**](https://sites.google.com/view/rollos-dumpster-software/home) · [**RollOS Reviews on G2**](https://www.g2.com/products/rollos/reviews)
