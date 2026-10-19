# Serialized Roll-Off Container Tracking & Yard Inventory Architecture

**Roll-off container tracking software** maintains real-time state allocation across every physical dumpster in a hauler's yard and active service territory so dispatchers and online checkout widgets never overbook a container size.

In [**RollOS**](https://rolloffdumpstersoftware.com/), fleets operating **1 to 25+ roll-off trucks** manage 10-yard, 15-yard, 20-yard, 30-yard, and 40-yard cans through a deterministic inventory state machine tied directly to the [**Visual Drag-and-Drop Dispatch Board**](https://rolloffdumpstersoftware.com/features/dispatch-board). For system-wide architecture, return to the [**dumpster rental management software**](../README.md) documentation index.

---

## Container Lifecycle State Machine

Unlike generic field-service calendars that only schedule time slots, roll-off logistics require tracking physical steel assets across multi-day and multi-week rental windows:

| Container State | Inventory Availability | Trigger Event | Operational Action |
| :--- | :--- | :--- | :--- |
| `IN_YARD_AVAILABLE` | Available for Online Checkout | Final pickup completed or new asset added | Ready for next dispatch assignment |
| `RESERVED_PENDING_DROP` | Locked for Date Window | Customer completes [**24/7 Online Booking**](https://rolloffdumpstersoftware.com/features/online-booking) or dispatcher logs phone order | Assigned to delivery truck route |
| `ON_SITE_ACTIVE` | Unavailable (Deployed at Job Site) | Driver uploads drop-off photo via [**SMS Magic Link**](https://rolloffdumpstersoftware.com/features/driver-routes) | Rental day counter tracks included days vs. extra-day fees |
| `SWAP_SCHEDULED` | Requires 1 Empty Yard Bin | Contractor requests dump-and-return or container exchange | Dispatches fresh bin + pulls loaded bin to landfill |
| `AT_LANDFILL_WEIGHING` | In Transit | Driver arrives at transfer station scale house | Scale ticket logged for [**Automated Tonnage Billing**](https://rolloffdumpstersoftware.com/features/tonnage-billing) |
| `MAINTENANCE_HOLD` | Excluded from Pool | Damaged rollers, latch repair, or weld inspection | Removed from booking capacity until cleared |

---

## Preventing Size-Specific Double-Bookings

A mid-size roll-off fleet running 8 trucks and 120 containers may have 40 twenty-yard bins completely deployed on roofing and remodeling projects while 15 thirty-yard bins sit empty in the yard.

1. **Size-Bucket Capacity Calculation:** RollOS evaluates availability per container size (`10yd`, `15yd`, `20yd`, `30yd`, `40yd`, or custom concrete washouts) across the requested delivery and pickup date range.
2. **Real-Time Checkout Cutoff:** When the final available 20-yard container is reserved for a specific delivery date, the online booking widget automatically marks 20-yard bins as sold out for that window and prompts the customer to select the next available size (e.g., 30-yard) or date.
3. **Elapsed Rental Day Alerts:** Containers exceeding their included rental period (e.g., 7-day or 10-day base window) are highlighted on the dispatch board for automatic per-day extension billing or pickup scheduling.

---

## Related Technical Specifications
* **Next Specification:** [**24/7 Online Dumpster Booking System & ZIP-Code Pricing Engine →**](./online-dumpster-booking-engine-spec.md)
* **External Resources:** [**Google Sites Resource Hub**](https://sites.google.com/view/rollos-dumpster-software/home) · [**LinkedIn Pulse: 7 Best Docket Alternatives**](https://www.linkedin.com/pulse/docket-alternatives-7-best-roll-off-container-management-platforms-n48dc) · [**RollOS Reviews on G2**](https://www.g2.com/products/rollos/reviews)
