# SCE Futures course voice and fact pass

Review target: 45 minutes. This packet covers task 0200's course structure work and task 0751's voice/fact pass. The branch is intentionally held for Alex's review.

## Start here

1. **3 minutes:** open [`0751-sce-course-voice-overview.svg`](0751-sce-course-voice-overview.svg).
2. **7 minutes:** review the fact lock and intentional code changes below.
3. **20 minutes:** use the rapid-scan table to sample every lecture in order.
4. **10 minutes:** open the built course and spot-check 00, 05, 11A, 11B, and 14.
5. **5 minutes:** complete the sign-off checklist.

## What changed

- The course now has 16 learner documents: lectures 00–14, with the former 10,000-word testing lecture split into 11A and 11B.
- Every learner document has objectives, a summary, self-check questions, and in-content previous/next navigation.
- The course home, README, navigation, headings, transitions, callouts, captions, summaries, and learner instructions received a voice pass.
- AQFP is explained through gradual switching near a local energy minimum. Energy-recovery, recycling, borrow/return, and returned-to-clock-network stories were removed.
- Device measurements, thermodynamic values, system models, and roadmap statements are now labeled as different evidence classes.

## Side-by-side samples by course module

| Surface | Before | After | Why it matters |
| --- | --- | --- | --- |
| Course entry / Lecture 00 | “The explosive growth of AI … has created an unprecedented demand for compute.” | “Modern AI systems turn electrical power into computation, memory traffic, communication, and heat.” | Starts from an engineering constraint instead of promotional urgency. |
| Part I, Foundations / Lecture 01 | A mixed technology chart treated a nominal cooling multiplier as a complete system comparison. | The chart compares the 0.040 zJ Landauer value with the published 1.4 zJ/JJ-cycle AQFP measurement and explicitly says the ratio is not a system advantage. | Keeps unlike boundaries from looking comparable. |
| Part II, Devices and Circuits / Lecture 05 | “Energy is recycled rather than dissipated.” | “The device remains near a local energy minimum through the transition, limiting dissipation.” | Conforms to D-0057 without inventing clock-energy bookkeeping. |
| Part III, Systems Integration / Lectures 11A–11B | One long testing lecture mixed method, troubleshooting, and vendor recommendations; several rules were stated universally. | 11A teaches method and measurement practice. 11B is a clearly labeled procurement starting guide whose values must be checked against current datasheets, quotations, grounding topology, and safety requirements. | Makes the teaching sequence usable and prevents examples from masquerading as specifications. |
| Part IV, Applications / Lecture 14 | Repeated “~100×” system advantage and generic “~1000× cooling” claims. | Names modeled corners: 6.4–8.5× packaged downside, 11.8–14.8× production, and 15.7–19.5× plant upside, with temperature and W/W assumptions. | Gives the reviewer the boundary, evidence state, and sensitivity instead of a slogan. |

## Fact lock used for this pass

These are the course anchors as of 2026-08-14. They are not interchangeable.

| Claim | Value | Evidence and boundary |
| --- | --- | --- |
| Landauer value | 0.040 zJ per irreversible bit erase at 4.2 K | Thermodynamic calculation. |
| Published AQFP reference | 1.4 zJ per Josephson junction per cycle at 4.2 K and 5 GHz | Measured 8-bit adder device result; Takeuchi et al., APL 114, 042602 (2019). |
| Production system model | 11.8–14.8× less wall energy | Modeled at 5 K and 400 W/W against host-inclusive NVIDIA B200, dense FP4. Outward shorthand is 12–15×. |
| Packaged downside | 6.4–8.5× less wall energy | Modeled at 5 K and 980 W/W on the same comparison boundary. |
| Plant upside | 15.7–19.5× less wall energy | Modeled at 5 K and 207 W/W on the same comparison boundary. |
| SFQ5ee stack | Eight superconducting metal layers | Process-stack fact, not a general count for every foundry. |

The system values are model results, not measurements of an integrated accelerator. The model charges the routed junction fabric each cycle and includes warm memory, I/O, scalar work, static cryostat load, and refrigeration.

## Intentional code and output changes

Seven notebooks contain evidenced code changes and were executed in full with zero error outputs:

| Notebook | Reason for code change |
| --- | --- |
| 00 | Replaced stale “~100×” and generic cooling-multiplier plots with current named model corners and evidence labels. |
| 01 | Replaced a dimensionally misleading cross-technology energy plot with the published device-scale anchor and Landauer reference. |
| 05 | Made the device/system boundary explicit in logic-family energy visuals and removed recycling language from the teaching model. |
| 08 | Labeled defect-density, layer-count, and area inputs as illustrative rather than measured foundry yield. |
| 10 | Scoped oxygen-monitoring language to the facility hazard assessment and local requirements. |
| 11A | Removed an unsourced process-improvement rate and labeled yield inputs and troubleshooting values by evidence state. |
| 14 | Replaced stale system numbers with current modeled corners and removed an unsupported total-power claim. |

Code sources and outputs in the other eight original notebooks are byte-for-byte unchanged from the branch base. Lecture 11B contains moved prose only and no code. All pre-edit URLs remain; three primary-source DOI links were added. The explicit pre-edit equations remain, including the kinetic-inductance scaling relationship.

## Rapid scan: one stop per learner document

| Stop | Review focus | Suggested anchor |
| --- | --- | --- |
| 00 | Evidence taxonomy and current system corners | “Quantitative anchors” |
| 01 | Superconductivity explanation and device-energy chart | “Device Energy Is Not System Energy” |
| 02 | Materials tradeoffs without canned transitions | Learning objectives and summary |
| 03 | DC/AC Josephson explanations and notation | Josephson relations |
| 04 | SQUID sensitivity and retained kinetic-inductance equations | “Kinetic-inductance scaling” |
| 05 | AQFP mechanism under D-0057 | “How AQFP switches” |
| 06 | Memory limitations and clocked-state framing | Summary and self-check |
| 07 | Timing, path balancing, and integration language | Pipeline balancing |
| 08 | SFQ5ee stack and illustrative yield model | “Yield considerations” |
| 09 | CTE, wiring, and signal-integrity guidance | Summary |
| 10 | Cryogenic safety and cooling-budget assumptions | “Cryogenic safety” |
| 11A | Measurement method, grounding, and failure isolation | “Practical measurement setup” |
| 11B | Vendor facts as starting points, not specifications | Procurement warning and final callout |
| 12 | Application maturity without unsupported superlatives | Application comparison and summary |
| 13 | Transformer dataflow, dimensions, and workload caveats | Attention and roofline sections |
| 14 | Modeled accelerator claims and evidence boundaries | Energy comparison and summary |

## Verification evidence

- Strict MkDocs build passes and renders all 16 notebooks.
- The rendered-site link audit reports zero broken internal links across 18 HTML pages.
- Seven code-changed notebooks execute completely with zero error outputs.
- Eight untouched original notebooks preserve code sources and outputs exactly.
- Notebook schema audit passes at nbformat 4.4 with no cell IDs introduced.
- All pre-edit external URLs are retained. Seven of eight current external links return HTTP 2xx in the automated check; the AIP DOI returns HTTP 403 to the bot but resolves to the indexed Takeuchi paper.
- Markdown pattern counts: “key insight” 12 → 1; em dashes 84 → 0; colon-form H2/H3 subtitles 57 → 10. This is a reduction check, not a zero-count style rule.
- D-0057 scan finds no energy-recovery, recycling, borrow/return, or returned-to-clock-network framing.
- Stale “11.8–14.7×,” “~100× system,” and generic “~1000× cooling” prose is absent.

## Reviewer sign-off

- [ ] AQFP mechanism is technically correct and does not imply clock-energy recovery.
- [ ] The device, system, and roadmap evidence states are clear.
- [ ] The three system-model corners and their boundaries match current AM canon.
- [ ] The seven intentional code changes are acceptable.
- [ ] Lecture 11A/11B is a better teaching split.
- [ ] Vendor and lab guidance is appropriately qualified.
- [ ] Voice feels like a precise, welcoming instructor across all four course parts.
- [ ] Rendered navigation, equations, figures, and callouts look correct.
- [ ] Approved to merge, or comments left on the PR.
