# Project Plan — RoomFinder Buddy v3.1

## Project Status

Planning and synthesis phase.  
Current goal: upgrade RoomFinder Buddy from v3.0 baseline to v3.1.

## Core Objective

RoomFinder Buddy v3.1 is an interactive housing-search assistant designed to support a solo UK restart strategy.

The app helps evaluate room listings, filter legal and practical risks, manage saved opportunities, prepare agency-friendly communication, and support fast but controlled decision-making for a late-May move-in target.

## Strategic Shift from v3.0 to v3.1

### v3.0 Focus

- Couple-friendly room search
- Max weekly rent logic
- M25 / outer London room-hunting support
- Scam avoidance and viewing checklist

### v3.1 Focus

- Solo applicant profile
- Company Director / self-employed professional positioning
- Uber London geofence-aware location strategy
- Agency-friendly application strategy
- Legal compliance checks
- Digital management from abroad
- Late-May move-in target

## Target User Profile

- Solo applicant
- Company Director / self-employed professional
- Uber / private hire driver background
- Long-term UK work and residence history
- Settled Status
- Right to Rent / Right to Work documentation available
- Low declared base salary may require careful affordability explanation

## Target Move-In Window

Late May 2026.  
Operational target: secure a practical room/base before or around 30 May 2026.

## Target Areas and Outcodes

### South West

- GU1
- GU2
- GU4
- GU21
- GU22

### West

- RG12
- RG40
- RG41
- SL1
- SL2
- SL3

### North West

- HP11
- HP12
- HP13
- HP15
- SL7
- RG9

### North

- WD17
- WD18
- WD6

### Airport / Logistics Nodes

- RH6
- TW6
- LU2

## Supported Platforms

- SpareRoom
- OpenRent
- Rightmove
- Zoopla

Agency listings are no longer excluded by default.

## Core Search Rules

- Maximum rent target: £700 PCM
- Shared house / HMO preference: all bills included
- Strong preference for rolling / periodic tenancy
- Practical access to Uber-compatible operating zones
- Fast digital referencing preferred
- No bidding above advertised rent

## Legal and Compliance Rules

The app should flag or reject listings where:

- admin fees are requested
- reference fees are requested
- illegal tenant fees appear
- holding deposit exceeds one week’s rent
- landlord or agent encourages bidding above the advertised price
- upfront payment requests appear legally questionable
- terms are unclear before payment

## Financial Strength Strategy

The app should not automatically recommend unlawful or questionable rent-in-advance offers.

Instead, it should support a legally compliant financial reassurance package:

- clear Company Director / self-employed explanation
- UK residence and work history summary
- Settled Status confirmation
- Right to Rent / Right to Work share code readiness
- ability to provide bank statements or savings evidence if requested
- fast response and fast document turnaround
- willingness to pay legally permitted holding deposit
- willingness to pay legally permitted first month rent in advance after signing

## App Structure — Four Pillars

### 1. Home

- Countdown to late-May move-in target
- Core strategy cards
- AI listing analyzer
- Saved listing pipeline
- Maybe / Approved / Rejected status handling

### 2. Data

- Location and area comparison
- Price-to-value scatter plot
- Uber geofence / logistics relevance
- Airport and outer-London access relevance
- Town-specific notes

### 3. Protocol

- Digital application checklist
- Holding deposit checklist
- Tenant fee red-flag checklist
- Right to Rent / referencing readiness checklist
- SitRep dilemma resolver

### 4. Templates

- Agency-friendly first contact message
- Follow-up message
- Holding deposit clarification message
- Reference / affordability explanation message
- Viewing or remote application request message

## Data Handling

- LocalStorage for saved listings and pipeline state
- Master report copy/export
- JSON export/import for backup and recovery

## v3.1 Must-Have Updates

- Replace couples-based logic with solo applicant logic
- Replace £150/week cap with £700 PCM cap
- Add target outcode list
- Add Rightmove and Zoopla as accepted platforms
- Add legal red-flag checks
- Update message templates
- Add agency-friendly communication mode
- Add digital-from-abroad workflow
- Add JSON export/import if not already stable
- Preserve v3.0 baseline before major changes

## Not In Scope Yet

- Backend
- User accounts
- Live scraping
- Automated Rightmove / Zoopla data extraction
- Live API integration
- Payment handling
- Legal advice automation

## Immediate Next Steps

1. Preserve current v3.0 code as baseline.
2. Update README to reflect v3.1 direction.
3. Update PROJECT_PLAN.md with this plan.
4. Add docs/CHANGELOG.md.
5. Add docs/COMPLIANCE_NOTES.md.
6. Start v3.1 implementation in small commits.
