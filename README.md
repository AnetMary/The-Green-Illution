# THE GREEN ILLUSION
### Dubai's Carbon Map: Construction, Food & Freight
## RESEARCH SUMMARY
Anet Mary George | Data Analyst, Dubai
Monte Carlo Simulation | Python 3 | 10,000 Simulations per Model
Primary Sources: Dubai Climate Action Plan 2021 · DEWA Annual Report 2023 · UAE Ministry of Climate Change &
Environment · Dubai Municipality Waste Reports 2022–2024 · USDA FAS Dubai 2024 · South Korea Ministry of
Environment
## EXCECUTIVE OVERVIEW
### What This Investigation Is — And Why It Matters
Dubai is a city of extraordinary ambition and extraordinary contradiction. Its December 2023 Climate
Action Plan; the first by a major Middle Eastern city formally aligned with the Paris Agreement;
commits to a 50% reduction in carbon emissions by 2030 against a 2018 baseline. The plan is real. The
targets are credible. But plans are only as strong as the gaps they acknowledge.
This investigation began from a simple, uncomfortable observation. Dubai's official climate accounting
assigns roughly 65% of city-scope emissions to electricity and cooling, 23% to transport,
and fragments the remaining 12% across industry, waste, and other categories. Three
major carbon contributors sit largely outside this accounting: the embodied carbon in construction
materials produced before a building opens; the full supply chain carbon of a city that imports 80–
85% of its food; the rapidly growing emissions from last-mile delivery logistics.
The methodology throughout is Monte Carlo simulation: every uncertain input is treated as a range
drawn from published literature, run 10,000 times, and reported as a distribution. This is more honest
than the single-point estimates that dominate official reporting — because the real world does not
operate at its median.
## METHODOLOGY
### How the Numbers Were Produced
### Monte Carlo Simulation — The Honest Accounting
Every input in this investigation is uncertain. Battery manufacturing carbon varies by factory and
country. Food waste rates shift seasonally. Construction volumes fluctuate with development cycles.
Standard analysis responds to this uncertainty by picking the most likely number and presenting it as
fact. This investigation responds differently.
For each uncertain variable, we define a plausible range anchored in published literature, then draw
from that range randomly across 10,000 independent simulations. The output is not a number; it is a
distribution. We report the median (the 50th percentile), the 10th percentile (optimistic), and the 90th
percentile (pessimistic). Where our conclusions hold at the 10th percentile, they are robust. Where
they only hold at the median or above, we say so.
## Data Sources and Hierarchy
Sources were evaluated in a strict hierarchy. Official city and national statistics (Dubai Climate Action
Plan 2021, DEWA Annual Report 2023, UAE Ministry of Climate Change & Environment, Dubai
Municipality Waste Reports 2022–2024) were treated as primary data. International benchmarks
(USDA FAS Dubai 2024, IEA UAE profiles, IPCC AR6, Poore & Nemecek 2018, World Steel
Association) were used to calibrate ranges. Case studies from comparable deployments (Seoul RFID
programme, Netherlands SCM cement standards, Paris micro-logistics hubs, Germany anaerobic
digestion data) were used to estimate alternative scenario effectiveness.
No input was assumed. Every range is cited. The full methodology, including all assumption ranges
and sensitivity tests, is documented in the accompanying computational notebook.
## Scope and Limitations
– This investigation covers Dubai city-scope emissions, not the UAE as a whole. Where UAE-level
data was the only available source, a Dubai-specific fraction was derived from population share
and economic weight.
– Food system carbon includes production emissions of imported food, transport, cold chain, and
waste decomposition. It does not include Scope 3 emissions from goods consumed beyond
food.
– Construction embodied carbon covers cement clinker and steel production. It does not include
downstream operational energy, which is captured in the electricity sector.
– All alternative scenario savings are conservative — calibrated to the lower end of documented
real-world outcomes from deployed programmes, not best-case projections.
## THE GAPS
### Where Dubai's Carbon Accounting Ends and the Real Numbers Begin
### Section 1 — Construction: The Carbon Before Opening Day
Dubai builds at a pace that few cities in the world match. The concrete and steel that constitute each
new tower, road, and metro line carry embedded carbon; CO₂ emitted during material production
before a single kilogram is mixed on site. This embodied carbon sits entirely outside Dubai's
operational emissions accounting.
Current State
15–25 Mt concrete/year (CBRE UAE
Construction Market 2023). Cement CO₂
intensity: 0.82–0.90 kg/kg clinker (IEA). Steel:
3–5 Mt/year at 1.8–2.2 t CO₂/t (blast furnace).
Combined: 3–6 Mt CO₂/year of embodied
carbon.
Alternative
SCM cement procurement mandate
(Netherlands: 70% GGBS standard; Germany:
40–50% fly ash). Green EAF steel powered by
renewables (Spain, Italy: dominant production
method). Potential saving: 0.5–1.5 Mt
CO₂/year. Dubai status: not in construction
specifications.
### Section 2 — Food System: The Primary Finding
This is the investigation's central analysis. Dubai imports 80–85% of its food supply (USDA FAS
2024). Every kilogram of beef, every litre of milk, every crate of vegetables carries embedded
production and transport carbon generated elsewhere — carbon that does not appear in any Dubai
sectoral emissions account.
The Dubai Carbon Centre of Excellence's own data points to a 38% daily food waste rate and 60%
during Ramadan. Applied to the full import volume, this means roughly 38% of all the carbon
embedded in Dubai's food supply chain is discarded before it provides any nutritional value. UAE
Ministry of Climate Change and Environment estimates 3.27 million tonnes of food wasted annually
nationally, worth $3.5 billion. Dubai's share is approximately 1.0–1.5 million tonnes.
The production-weighted carbon intensity of Dubai's food import basket (reflecting its high proportion
of meat and dairy) is estimated at 4.5–7.5 kg CO₂ per kilogram of food, using Poore & Nemecek (2018)
and Our World in Data supply chain data. The total food system carbon, including import transport,
cold chain energy on the DEWA grid, and waste decomposition — is modelled at approximately 1.5–
3.5 Mt CO₂ per year on the median, representing 6–13% of Dubai's city-scope baseline.
Against this, the alternative is specific, proven, and costed:
– South Korea's RFID weight-based food waste metering system, mandated nationally
from 2013, achieved a 10–30% reduction in food waste volume. Seoul alone eliminated
47,000 tonnes over six years. The system charges households by the weight of food discarded —
not restricting what is eaten, but making waste have a price. Cost to a four-person household:
approximately $6 per month.
– Institutional procurement policy, applying lower-carbon menu defaults to hotel catering,
airport lounges, and government canteens achieved 15–25% food service emission
reductions in Singapore's hawker centre programme (WRI Cool Food Pledge data).
Dubai's hospitality sector, one of the largest generators of food waste in the city, has no
equivalent policy framework.
### Section 3 — Last-Mile Freight: The Growing Gap
UAE e-commerce grew to $1.1 billion in online grocery in 2024 (+13% year-on-year, USDA FAS 2024).
Dubai's delivery vehicle fleet is estimated at 80,000–110,000 vehicles, growing at 10–
18% per year. At 0.22–0.32 kg CO₂/km per diesel van and 80–130 km of daily route, current annual
emissions are approximately 0.05–0.12 Mt CO₂, small today, but doubling within four years at current
growth trajectories.
Paris (2021) and Amsterdam (2020) introduced consolidated micro-logistics hubs in
urban cores, restricting diesel vans from designated zones and replacing them with
electric cargo bikes for final delivery. Paris documented a 30–45% CO₂ reduction in covered
zones. Dubai has no urban logistics strategy. The window to shape infrastructure before the fleet
doubles is narrow.
## THE STRUCTURAL PATTERN
### Who Pays, Who Benefits — and Why It Matters
Mapping every alternative against a single question — who bears the cost of implementation — reveals
a pattern that is consistent across all four sections of this investigation, and across the original Green
Illusion analysis of EVs and private aviation.
The alternatives that are not being implemented share a specific property: their cost falls on
institutions — government procurement officers who would need to specify SCM cement, hospitality
operators who would need to install food waste meters, municipality planners who would need to
commission anaerobic digestion infrastructure. None of them require a Dubai resident or tourist to
change their behaviour. None restrict what people build, eat, or purchase. The consumer experience is
unchanged; the systems within which consumption happens are different.
The alternatives that are being implemented, the EV programme, the Warsan Waste-to-Energy plant,
the solar park expansion are correct and valuable. But they are also visible, announcement-ready, and
consumer-facing. The gaps in this investigation are institutional, quiet, and difficult to feature in a
press release.
This is not a criticism of intent. It is an observation about incentive structures. The Ne'ma Initiative's
50% food waste reduction target by 2030 is exactly the right ambition. South Korea achieved it with a
mechanism: RFID weighing, accountability fees, and a national framework. Dubai has the target. The
mechanism does not yet exist.
### CONCLUSIONS AND RECCOMENDATIONS
# What an Evidence-Aligned Dubai Climate Policy Would Add
This investigation does not argue that Dubai's climate programme is failing. It argues that it is
incomplete and that the missing components are not technically difficult, financially prohibitive, or
socially disruptive. They are institutionally absent.
### Specific Actions Supported by the Evidence
– 1. Mandate commercial food waste measurement for all hospitality and food service businesses
with more than 50 covers, submitting data via Dubai Municipality's existing Montaji digital
platform. Measurement alone — without any reduction target — has been shown to reduce food
waste by 5–15% simply through the act of visibility. This is not a restriction. It is a mirror.
– 2. Pilot RFID pay-as-you-throw bins across 10 residential tower clusters in Dubai's highestdensity zones. The technology is proven; the infrastructure (building management systems,
digital payments) is present. Seoul's programme achieved a 7.3% reduction in food waste in
Year 1 at a cost of approximately $6/month per household.
– 3. Adopt SCM cement specifications in Dubai Municipality and Roads & Transport Authority
procurement contracts, requiring minimum 30% supplementary cementitious material
replacement for government-funded projects. This requires no new technology — GGBS and fly
ash are both available in the Gulf supply chain. It requires a procurement policy update.
– 4. Publish a food system carbon account as part of Dubai's annual climate reporting. The data
to construct this exists across DEWA, Dubai Municipality, and MOCCAE. The missing step is
connecting import volumes, cold chain energy, and waste decomposition into a unified sectoral
number with a reduction trajectory attached to it.
None of these four actions require a single Dubai resident, tourist, or business to reduce what they
consume. Each one changes the infrastructure, procurement, or accountability framework within
which consumption happens. The distinction matters: climate policies that are perceived as
restrictions generate resistance. Climate policies that change systems generate results.
\\\\
### Anet Mary George Data Analyst, Dubai | The Green Illusion
Sources: Dubai Climate Action Plan 2021 · DEWA Annual Report 2023 · UAE MOCCAE · Dubai Municipality Waste Reports 2022–
2024 · USDA FAS Dubai 2024 · Poore & Nemecek 2018 · Seoul Urban Solutions Agency · Korea Ministry of Environment · IPCC
AR6 · IEA UAE · CBRE UAE Construction Market 2023 · World Steel 
