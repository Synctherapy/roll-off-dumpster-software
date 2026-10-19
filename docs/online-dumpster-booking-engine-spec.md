# 24/7 Online Dumpster Booking System & ZIP-Code Pricing Engine Specification

**Dumpster booking software** enables residential homeowners and commercial construction contractors to check real-time container availability by ZIP code, select a bin size, e-sign a legal liability agreement, and pay upfront online in under 60 seconds.

The [**RollOS 24/7 Online Booking Engine**](https://rolloffdumpstersoftware.com/features/online-booking) deploys via a single line of embed code on any existing website (WordPress, Wix, Squarespace, GoDaddy, Webflow) or as a standalone hosted booking portal (`rolloffdumpstersoftware.com/book/yourcompany`). Return to the main [**dumpster rental management software**](../README.md) documentation hub.

---

## 5-Stage Checkout Pipeline Architecture

### 1. ZIP-Code Service Zone & Distance Tier Validation
Haulers configure approved delivery ZIP codes and optional fuel/distance surcharges. When a customer enters their job-site ZIP code:
* **In-Territory Match:** Displays real-time pricing and available delivery dates.
* **Extended Zone Match:** Automatically applies the hauler's configured out-of-zone mileage surcharge.
* **Out-of-Territory Reject:** Prevents out-of-area bookings before checkout.

### 2. Container Size, Included Tonnage & Rental Window Selection
Each container card displays transparent operational parameters so renters select the right bin without phone tag:
* **Container Dimensions & Capacity:** 10-yard, 15-yard, 20-yard, 30-yard, and 40-yard roll-off containers.
* **Included Weight Allowance:** e.g., 1 ton, 2 tons, or 3 tons included in the base haul rate, plus the exact per-ton overage rate ($/ton) for excess landfill weight.
* **Included Rental Duration:** e.g., 3, 7, 10, or 14 days included, plus the daily extension rate ($/day).

### 3. Debris Type & Prohibited Material Screening
Renters specify debris categories (household junk, roofing shingles, construction & demolition C&D, heavy dirt/concrete) and acknowledge prohibited hazardous materials (tires, wet paint, batteries, asbestos, appliances with Freon). Haulers can estimate heavy load weights using the [**Roll-Off Tonnage Calculator**](https://rolloffdumpstersoftware.com/tools/tonnage-calculator).

### 4. Mandatory Digital Driveway Liability Waiver (E-Signature)
Before payment is accepted, the renter must digitally sign the hauler's rental contract covering:
* Driveway, asphalt, lawn, and underground septic/sprinkler liability release.
* Overhead power line and tree branch clearance requirements.
* Fill-line level-load rules and landfill scale ticket overage authorization.
* *(Download the free starter agreement at [**Dumpster Rental Contract Template**](https://rolloffdumpstersoftware.com/templates/dumpster-rental-contract)).*

### 5. Upfront Stripe Connect Settlement & Card-on-File Vaulting
Payments process via Apple Pay, Google Pay, or credit/debit card through Stripe Connect:
* **Direct Bank Payouts:** 100% of the base rental rate deposits directly into the hauler's connected bank account.
* **Card-on-File Tokenization:** Securely vaults the payment method to settle post-pickup landfill scale ticket overages via [**Automated Tonnage Billing**](https://rolloffdumpstersoftware.com/features/tonnage-billing).
* **Flexible Fee Architecture:** On the [**$0/month Free Plan**](https://rolloffdumpstersoftware.com/pricing), the customer pays a flat $12 checkout reservation fee (or the hauler can toggle 1-click "Absorb Fee").

---

## Related Technical Specifications
* **Previous Specification:** [**← Serialized Roll-Off Container Tracking & Yard Inventory Architecture**](./roll-off-container-tracking-architecture.md)
* **Next Specification:** [**Zero-App Driver SMS Magic Link Routing & Proof-of-Service Protocol →**](./driver-sms-magic-link-routing.md)
* **External Resources:** [**Google Sites Resource Hub**](https://sites.google.com/view/rollos-dumpster-software/home) · [**RollOS Reviews on G2**](https://www.g2.com/products/rollos/reviews)
