# Laurel Hill Residential: operating handbook

Laurel Hill Residential is a fictional property manager made up for Build Night. It runs 140 rental units in six properties around Chapel Hill and Carrboro. Most tenants are UNC students and young staff.

The whole company is three people:

- **Priya Raman**, owner. Handles money, leases, legal questions, and anything that might end up in small claims court.
- **Jake Ellis**, leasing coordinator. Answers prospects, runs showings, and processes applications.
- **Luis Ortega**, maintenance technician. Fixes what he can in-house and calls vendors for the rest.

On-call numbers: Luis 919-555-0100 (emergencies, any hour), Jake 919-555-0102 (business hours), Priya 919-555-0101 (emergencies and money only).

All three check one shared inbox that collects texts, emails, website forms, and voicemail transcripts. Nobody watches it on weekends unless they happen to look.

Today is **Monday, October 5, 2026, 7:00 AM**. Everything in `messages.csv` arrived between Friday 5:00 PM and now.

Run the inbox as a **replay**: handle each message as of its `received_at` time, the way your agent would have if it had been running all weekend. Separately, show what would still be overdue if nobody had answered until Monday at 7:00 AM.

Your agent can't actually call or text anyone tonight. When it dispatches someone, draft the call or text and show who it goes to. That counts. Pretending a call happened does not.

## Properties

| Property | Area | Units | Pets |
|---|---|---|---|
| The Weaver | Carrboro | 32 | Cats and dogs under 40 lb |
| Estes Commons | Estes Drive | 40 | Cats and dogs under 40 lb |
| Pritchard Court | Northside | 18 | No pets |
| Merritt Mill Flats | Merritt Mill Road | 24 | Cats only |
| Church Street Duplexes | Northside | 12 | No pets |
| Barclay Townhomes | Barclay Road | 14 | Cats and dogs under 40 lb |

Unit details, rents, and availability are in `units.csv`.

## Leasing rules

- Showings are Monday to Saturday, 10:00 AM to 6:00 PM, in 30-minute slots, always with Jake. There are no self-guided tours. Open slots are in `showing_slots.csv`.
- The application fee is $50 per adult applicant.
- Applicants need income of at least 3 times the monthly rent, or a guarantor who earns at least 5 times the rent. Most students use a guarantor.
- Student buildings (The Weaver, Pritchard Court, Church Street) lease August 1 to July 31. A unit that opens up mid-year in a student building is offered as a takeover lease that ends July 31, at the listed rent. Priya approves each one. The other properties lease for 12 months starting any month.
- Pet deposit is $300 and pet rent is $35 a month per pet. Service animals and emotional support animals are not pets: no deposit, no pet rent, and no weight limit. Requests for one go to Priya.
- Subleases are allowed with Priya's written approval and a $150 fee.
- **Never promise a unit, a price, or an approval.** Only Priya signs leases.
- Fair housing: never comment on who lives in a building, what neighborhood is "good," or whether a unit suits families, a religion, a nationality, or a disability. Describe the unit and the policies.

## Maintenance priorities

**Emergency.** Respond within 1 hour, 24 hours a day, 7 days a week. Call Luis and the right vendor right away.
- No heat from October through April
- Active water leak, flooding, or sewage backup
- Gas smell. First tell the tenant to leave the unit and call 911 and the gas company, Enbridge Gas North Carolina, from outside. Don't flip switches.
- No power to the whole unit
- Exterior door or lock that will not secure
- Fire or smoke: 911 first, always
- Carbon monoxide alarm sounding. Tell everyone to leave the unit now, including pets, and call 911 from outside. Don't tell them to open windows and stay.

**Urgent.** Same or next business day.
- No hot water
- Refrigerator not cooling
- No AC when it is above 85°F outside
- The only toilet in the unit not working
- Lockout during business hours. Lockouts after hours go to the locksmith, and the tenant is charged $75. That $75 is the tenant fee; what Laurel Hill pays the locksmith is separate. Never quote the vendor's rate to a tenant.

**Routine.** Within 5 business days. Everything else: dripping faucets, a broken blind, a slow drain, a dead light fixture, a squeaky door.

Luis handles basic plumbing, appliances, drywall, doors, and fixtures himself. Anything involving HVAC, electrical panels, a main sewer line, pests, roofing, or locks goes to a vendor in `vendors.csv`. Only vendors marked `after_hours = yes` will come at night or on weekends.

## Other messages

- Rent and payment questions, late fees, and payment plans go to Priya. Rent is due on the 1st, late after the 5th, and the late fee is $50.
- Noise complaints: log them and acknowledge within one business day. Send repeat complaints about the same unit to Priya.
- **Requests to change a vendor's or the company's bank details always go to Priya.** Never act on them. Flag them as possible fraud.
- Lease-break and legal questions go to Priya.

## What a good reply looks like

Short, specific, and in the language the person wrote in. Tell tenants what happens next and when. Never blame the tenant for a repair. Sign as "Laurel Hill Residential". Say that you are an automated assistant whenever you send a reply without a person reviewing it first.
