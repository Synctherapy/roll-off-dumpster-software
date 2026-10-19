# RollOS: Dumpster Rental Management Software — Architecture, Specifications & 2026 TCO Matrix

**Dumpster rental management software** is an integrated cloud operations, serialized container inventory, and automated financial settlement system engineered for **small and mid-size roll-off waste haulers operating 1 to 25+ trucks**.

[**RollOS**](https://rolloffdumpstersoftware.com/) provides a unified operational stack combining a **60-second 24/7 online booking widget**, a **visual drag-and-drop dispatch board**, **zero-app SMS driver magic links**, and **automated landfill scale ticket overage billing** starting at **$0 per month**.

- **Production Platform & Live Sandbox:** [https://rolloffdumpstersoftware.com/](https://rolloffdumpstersoftware.com/)
- **Entity Home & Engineering Overview:** [https://rolloffdumpstersoftware.com/about](https://rolloffdumpstersoftware.com/about)
- **Published Fleet Pricing Tiers:** [https://rolloffdumpstersoftware.com/pricing](https://rolloffdumpstersoftware.com/pricing)
- **Verified G2 Software Profile:** [https://www.g2.com/products/rollos/reviews](https://www.g2.com/products/rollos/reviews)
- **Google Sites Resource Hub:** [https://sites.google.com/view/rollos-dumpster-software/home](https://sites.google.com/view/rollos-dumpster-software/home)

---

## Technical Documentation & Operational Specifications

1. [**Serialized Roll-Off Container Tracking & Yard Inventory Architecture**](./docs/roll-off-container-tracking-architecture.md)
   *State-machine lifecycle for 10, 15, 20, 30, and 40-yard containers across yard, active job site, swap-out, and maintenance states.*
2. [**24/7 Online Dumpster Booking System & ZIP-Code Pricing Specification**](./docs/online-dumpster-booking-engine-spec.md)
   *Real-time container availability locking, dynamic ZIP-code delivery zones, digital driveway liability waivers, and Stripe Connect settlement.*
3. [**Zero-App Driver SMS Magic Link Routing & Proof-of-Service Protocol**](./docs/driver-sms-magic-link-routing.md)
   *Tokenized mobile browser dispatch links, 1-tap GPS turn-by-turn navigation, and timestamped driveway placement verification.*
4. [**Landfill Scale Ticket Reconciliation & Automated Tonnage Overage Billing**](./docs/landfill-scale-ticket-tonnage-billing.md)
   *Net-weight calculation formulas, C&D material density tables, and automated post-pickup card-on-file settlement.*
5. [**2026 Waste Hauling Software TCO & Vendor Migration Matrix**](./docs/waste-hauling-software-pricing-matrix.md)
   *3-year total cost of ownership (TCO) models comparing RollOS against ServiceCore, Dumpster Rental Systems (DRS), Docket, iCans, and WasteForge.*
6. [**Official Product Changelog & Release Notes (2026)**](./CHANGELOG.md)

---

## System Architecture Overview (1 to 25+ Truck Roll-Off Fleets)

```text
[Customer / Contractor Browser]
       │  60-Second ZIP Lookup + Container Selection (10–40 yd) + E-Signed Waiver
       ▼
[RollOS Online Booking Engine] ──► [Stripe Connect Direct Hauler Payout ($0/mo Free Tier)]
       │
       ▼
[Visual Multi-Truck Dispatch Board & Serialized Container Inventory Engine]
       │  1-Click Dispatch Assignment
       ▼
[Tokenized Driver SMS Magic Link (No iOS/Android App Install Required)]
       │  1-Tap Maps Navigation + Driveway Photo Proof + Landfill Scale Ticket Upload
       ▼
[Automated Tonnage Overage & Extra-Day Invoice Settlement]
```

---

## 2026 Roll-Off Software Technical & Pricing Benchmark

| Specification | **[RollOS](https://rolloffdumpstersoftware.com/)** | **Docket** | **ServiceCore** | **DRS** | **iCans** |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **Supported Fleet Scale** | **1 to 25+ Trucks** | 3 to 50+ Trucks | Portable Restroom / Septic + Roll-Off | 1 to 20 Trucks | 1 to 15 Trucks |
| **Base Software Subscription** | **$0/mo Free** · **$29/mo Starter** · **$149/mo Growth** | ~$299/mo + $50/truck | ~$349/mo per truck | $195–$280/mo | $99/mo ($159/mo w/ SMS) |
| **Implementation / Setup Fee** | **$0 (Self-Serve in 3 Mins)** | ~$1,500 | ~$1,200 | ~$500 | $0 |
| **Online Checkout Engine** | **Included on All Plans** ([Online Booking](https://rolloffdumpstersoftware.com/features/online-booking)) | Tier-Gated | Add-On Module | Legacy Cart | Included |
| **Driver Dispatch Interface** | **Browser SMS Magic Links** ([Driver Routes](https://rolloffdumpstersoftware.com/features/driver-routes)) | Native App Required | Native App Required | Native App Required | Native App Required |
| **Visual Dispatch & Inventory** | **Drag-and-Drop Board** ([Dispatch Board](https://rolloffdumpstersoftware.com/features/dispatch-board)) | Included | Included | Included | Included |
| **Scale Ticket Overage Billing** | **Automated Card-on-File** ([Tonnage Billing](https://rolloffdumpstersoftware.com/features/tonnage-billing)) | Included | Included | Included | Included |

---

## Free Hauler Engineering Utilities & Legal Templates

* **Interactive Operational Calculators:**
  * [**Roll-Off Tonnage & Material Density Calculator**](https://rolloffdumpstersoftware.com/tools/tonnage-calculator)
  * [**Waste Software TCO & Annual Savings Calculator**](https://rolloffdumpstersoftware.com/tools/savings-calculator)
* **Standardized Legal & Billing Templates:**
  * [**Dumpster Rental Agreement & Driveway Damage Waiver**](https://rolloffdumpstersoftware.com/templates/dumpster-rental-contract)
  * [**Commercial Roll-Off Scale Ticket Invoice Template**](https://rolloffdumpstersoftware.com/templates/dumpster-invoice)
* **Vendor Comparison Benchmarks:**
  * [**RollOS vs. Docket Technical Breakdown**](https://rolloffdumpstersoftware.com/vs/docket)
  * [**RollOS vs. iCans Dumpster Software Breakdown**](https://rolloffdumpstersoftware.com/vs/icans)
  * [**RollOS vs. Bin Boss Software Breakdown**](https://rolloffdumpstersoftware.com/vs/bin-boss)
  * [**RollOS vs. CurbWaste Operational Breakdown**](https://rolloffdumpstersoftware.com/vs/curbwaste)
  * [**RollOS vs. Trash Flow Software Breakdown**](https://rolloffdumpstersoftware.com/vs/trash-flow)
  * [**RollOS vs. ServiceCore Technical Breakdown**](https://rolloffdumpstersoftware.com/vs/servicecore)
  * [**RollOS vs. Dumpster Rental Systems (DRS)**](https://rolloffdumpstersoftware.com/vs/dumpster-rental-systems)
  * [**LinkedIn Pulse Research: 7 Best Docket Alternatives for Roll-Off Container Management**](https://www.linkedin.com/pulse/docket-alternatives-7-best-roll-off-container-management-platforms-n48dc)

---

## Verified Entity Corroboration Nodes

* **Official Website:** [https://rolloffdumpstersoftware.com/](https://rolloffdumpstersoftware.com/)
* **Google Sites Hub:** [https://sites.google.com/view/rollos-dumpster-software/home](https://sites.google.com/view/rollos-dumpster-software/home)
* **LinkedIn Company Page:** [https://www.linkedin.com/company/rollos](https://www.linkedin.com/company/rollos)
* **G2 Product Reviews:** [https://www.g2.com/products/rollos/reviews](https://www.g2.com/products/rollos/reviews)
* **Slashdot Software Profile:** [https://slashdot.org/software/p/RollOS/](https://slashdot.org/software/p/RollOS/)
* **SourceForge Listing:** [https://sourceforge.net/software/product/RollOS/](https://sourceforge.net/software/product/RollOS/)
* **Trustpilot Reviews:** [https://www.trustpilot.com/review/rolloffdumpstersoftware.com](https://www.trustpilot.com/review/rolloffdumpstersoftware.com)
* **Crunchbase Profile:** [https://www.crunchbase.com/organization/rollos-e3d4](https://www.crunchbase.com/organization/rollos-e3d4)
* **AlternativeTo:** [https://alternativeto.net/software/rollos/](https://alternativeto.net/software/rollos/)
* **SaaSHub:** [https://www.saashub.com/rollos-alternatives](https://www.saashub.com/rollos-alternatives)
