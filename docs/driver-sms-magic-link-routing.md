# Zero-App Driver SMS Magic Link Routing & Proof-of-Service Protocol

**Roll-off dispatch software** connects the office dispatch desk with CDL truck drivers executing daily container drop-offs, switches, dump-and-returns, and final pickups.

Instead of requiring native iOS or Android App Store downloads, password management, or background GPS battery drain, [**RollOS Driver SMS Routing**](https://rolloffdumpstersoftware.com/features/driver-routes) dispatches tokenized, expiring mobile web links directly via SMS. Return to the main [**dumpster rental management software**](../README.md) documentation hub.

---

## Architecture Comparison: Tokenized SMS Magic Links vs. Native Driver Apps

| Technical Attribute | **[RollOS SMS Magic Links](https://rolloffdumpstersoftware.com/features/driver-routes)** | **Legacy Native Driver Apps (Docket, ServiceCore, DRS)** |
| :--- | :--- | :--- |
| **Driver Onboarding Time** | **0 Seconds** (Tap text link in iOS Safari / Android Chrome) | 15–30 minutes (App Store install, account provisioning, login) |
| **Authentication Mechanism** | Cryptographically signed, time-scoped route token (`/driver/[token]`) | Username/password credentials prone to lockouts at job sites |
| **OS & Device Compatibility** | Universal (any smartphone with a mobile browser and camera) | Requires specific iOS/Android OS versions and app updates |
| **Navigation Handoff** | 1-Tap deep link into native Google Maps, Apple Maps, or Waze | Embedded third-party map SDK |
| **Proof-of-Service Capture** | HTML5 camera capture for driveway photos & landfill scale slips | App-specific photo upload queue |

---

## Daily Driver Route Execution Workflow

1. **Dispatch Assignment on the Visual Board:** The dispatcher drags a scheduled delivery, swap, or pickup onto a truck/driver column on the [**Visual Drag-and-Drop Dispatch Board**](https://rolloffdumpstersoftware.com/features/dispatch-board) and clicks **Send SMS Route**.
2. **Sequenced Stop Manifest:** The driver taps the SMS link to view their ordered daily stops, including container size (`10yd`–`40yd`), assigned bin serial number, customer gate codes, and specific driveway placement instructions (*"Place on left side of driveway on wood boards"*).
3. **Timestamped Driveway Placement & Condition Photos:** Upon arrival, the driver captures pre-drop or post-drop photos (documenting preexisting driveway cracks, blocked access, or overloaded debris above the fill line), which attach immediately to the customer's booking record.
4. **Landfill Scale Ticket Capture:** After tipping at the transfer station, the driver photographs the printed scale house weight ticket and enters the net tonnage, triggering [**Automated Tonnage Overage Billing**](https://rolloffdumpstersoftware.com/features/tonnage-billing).

---

## Related Technical Specifications
* **Previous Specification:** [**← 24/7 Online Dumpster Booking System & ZIP-Code Pricing Engine**](./online-dumpster-booking-engine-spec.md)
* **Next Specification:** [**Landfill Scale Ticket Reconciliation & Automated Tonnage Overage Billing →**](./landfill-scale-ticket-tonnage-billing.md)
* **External Resources:** [**Google Sites Resource Hub**](https://sites.google.com/view/rollos-dumpster-software/home) · [**LinkedIn Pulse: 7 Best Docket Alternatives**](https://www.linkedin.com/pulse/docket-alternatives-7-best-roll-off-container-management-platforms-n48dc) · [**RollOS Reviews on G2**](https://www.g2.com/products/rollos/reviews)
