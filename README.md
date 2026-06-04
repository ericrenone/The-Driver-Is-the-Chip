# THE SETTLEMENT GAP

## What BYD's Xuanji, Huawei's Ten Billion Kilometers, Tesla's Supervised Qualifier, and SpaceX's Unnamed Arithmetic Say About the One Hardware Primitive the Global Autonomous Driving Industry Has Not Yet Built

**ERI Labs · Eric Ren · Jersey City, New Jersey · [github.com/ericrenone](https://github.com/ericrenone) · June 4, 2026**

---

> *"Hardware 3 simply does not have the capability to achieve Unsupervised FSD."*
> — Elon Musk, April 22, 2026

> *"Computing power utilization has doubled."*
> — BYD, Xuanji A3 launch, May 28, 2026

> *"Autonomous driving is an industry requiring long-term investment."*
> — Jin Yuzhi, Huawei Intelligent Automotive Solutions, April 24, 2026

> *"The proof holds in exact arithmetic. In finite-precision arithmetic under thermal stress, partial engine failure, and process-variation silicon, it is an approximation of an approximation."*
> — ERI Labs, The Convergence Oracle, June 4, 2026

> *"We had to make several design concessions to move fast."*
> — Tesla AI hardware team, post-AI5 tape-out, April 15, 2026

> *"Cooperative perception enabled by V2X communication can significantly improve the perception performance of autonomous vehicles beyond the limited perception ability of individual vehicles."*
> — V2X-UniPool, arXiv:2506.02580, June 2026

---

## The Most Revealing Insurance Policy in Automotive History

On May 28, 2026, BYD chairman Wang Chuanfu stood before cameras in Shenzhen and announced that the company would, effective immediately, cover all accident costs for any vehicle operating its God's Eye Urban Navigate-on-Autopilot system. Not liability-capped. Not geofenced. Covered. The company's 7,000-engineer chip team had spent years building the Xuanji A3 — China's first self-developed 4nm automotive-grade driving chip — and now BYD was putting financial liability behind it.

That same week, Tesla's FSD remained labeled Supervised. Its DMS update logged better eyewear detection. Its Cybercab fleet in Austin stood at approximately 20 vehicles, geofenced, monitored remotely by a fleet operations team whose presence was not publicly disclosed.

The contrast is not a story about two companies with different products. It is a story about two companies that have found different answers to the same engineering question — and about the fact that neither answer, looked at closely, is actually an answer.

BYD's Full Damage Coverage is a financial claim translated from a hardware confidence claim. It says: *we believe this chip is reliable enough to stake money on.* Tesla's Supervised qualifier is also a financial claim translated from a hardware confidence claim. It says: *we are not yet prepared to stake money on this chip alone.* Both companies are circling the same unanswered question from opposite sides of the same boundary. The question is not about TOPS, or process node, or even memory bandwidth. The question is: **when can a chip certify its own inference before committing to an irrevocable action?**

Nobody has built that chip. Not BYD. Not Tesla. Not Huawei. Not SpaceX. Not NVIDIA. Not Mobileye.

That is the settlement gap.

---

## Seven Chips, One Table, One Axis Nobody Passes

The global autonomous vehicle chip race of 2026 is being reported as a compute war. TOPS counts appear in headlines. Process nodes — 4nm, 5nm, 7nm — are invoked as competitive moats. Memory bandwidth, quietly, has become the metric that actually determines commercial deployability. And beneath all three, invisible in every press release, is the axis that determines whether any of it is enough.

| Chip | OEM | Node | TOPS (peak) | Bandwidth | Power | ASIL | Convergence-native | Unsupervised at scale |
|---|---|---|---|---|---|---|---|---|
| **Xuanji A3** (×3) | BYD | 4 nm | 2,100 | 273 GB/s | ~20% below peers | **D** | No | No — Full Damage Coverage, not oracle |
| **Shenji NX9031** | NIO | 5 nm | Not disclosed | Not disclosed | Not disclosed | Not disclosed | No | No — world model, fleet learning |
| **Mach 100** | Li Auto | 5 nm | 1,280 | Not disclosed | Not disclosed | Not disclosed | No | No |
| **Turing AI** | Xpeng | 7 nm | ~750 | Not disclosed | Not disclosed | Not disclosed | No | No |
| **Qiankun AI** (Huawei supply) | 25 brands | Not disclosed | Not disclosed | Not disclosed | Not disclosed | Not disclosed | No | L3 highway, Q4 2026 |
| **AI4 / HW4** | Tesla | 7 nm | 500 | 384 GB/s | ~160 W | Not disclosed | No | ~20 robotaxis, geo-limited |
| **AI5** (tape-out) | Tesla | 3–4 nm | ~4,000+ | 192 GB LPDDR5X | 700–800 W | Not disclosed | No | 0 in vehicles |
| **HW3** (abandoned) | Tesla | 14 nm | 72 | 48 GB/s | ~100 W | Not disclosed | No | 0 — retired |
| **Drive Thor** | NVIDIA | 5 nm | 2,000 | Not disclosed | Not disclosed | Not disclosed | No | No — supply only |
| **D3** (planned) | SpaceX | Intel 18A | Not disclosed | Not disclosed | Not disclosed | N/A | Announced intent | 0 fabricated |

Three facts stand out.

First, BYD's Xuanji A3 at 273 GB/s has already crossed the bandwidth threshold that retired HW3. Tesla abandoned HW3 because its 48 GB/s memory bandwidth — 1/8 of AI4's — could not sustain FSD neural network growth from v12 to v14. BYD's chip ships at a bandwidth that would have cleared that wall by more than five times. China solved Axis 1.

Second, BYD claims 20% less power consumption per unit of computation than comparable alternatives. IBM's 2026 study found precisely that 20% efficiency improvement produces a 3–5% EV range increase. These numbers are not coincidental; they are the same measurement expressed from different directions, by researchers in different countries, on different timescales. The bandwidth and power efficiency constraints that forced Tesla's hardware evolution are constraints BYD has incorporated into its chip design from the start. China solved Axis 2.

Third: not one chip in this table is convergence-native. BYD's ASIL-D certification — the highest automotive functional safety grade, which specifies that a chip's failure behavior is deterministic and bounded — is the closest any production chip has come to hardware-certified convergence. It is not the same thing. ASIL-D certifies that the hardware's failure mode is safe. It does not certify that the hardware's inference has converged before an irrevocable action commits. **ASIL-D is a safety boundary. A convergence oracle is a settlement signal.** These are architecturally different claims. BYD's insurance policy rests on the former. The settlement gap remains in the latter.

Nobody has solved Axis 3.

---

## Huawei's Bet and the Philosophy Behind It

Eighteen billion yuan — approximately $2.6 billion — is what Huawei's Intelligent Automotive Solutions division is spending on autonomous driving in 2026 alone. Jin Yuzhi, the division's CEO, said at the April 2026 Beijing Auto Show that this figure exceeds the combined annual investment of all other major autonomous driving solution providers. By May 2026, Huawei's Qiankun ADS platform had accumulated over 10 billion kilometers of real-world assisted driving data across 25 partner brands, installed in more than 50 vehicle models. The number is staggering. For comparison, Tesla has cited approximately 10 billion real-world *miles* in global training data — roughly 16 billion kilometers. Huawei, operating exclusively in China and a handful of partner markets, has reached the same training data scale in a fraction of the deployment window.

But here is the thing Huawei said, quietly, that matters more than the kilometer count: **Huawei explicitly rejected the VLA path.**

Vision-Language-Action models — the approach pursued by Li Auto, Xpeng, Deeproute.ai, Xiaomi, and much of the Chinese AD research community — treat autonomous driving as an end-to-end mapping problem: raw sensor input goes in, action comes out, and the network learns the intermediate representation from data. It is, in simplified terms, the Chinese parallel to Tesla's end-to-end neural network architecture for FSD. Richard Jin, CEO of Huawei's automotive division, was direct: "Companies on the VLA path think that language models like those developed by OpenAI have already mastered vast online information. Huawei won't follow that path."

Huawei's alternative — the WEWA framework — combines a structured world model with a separate action-planning layer. It is, architecturally, a separation of the col(F)/ker(F) boundary into an explicit two-stage structure: first, build a certified representation of the scene (the world model); second, plan actions against that representation. The world model is not the action. The action is not the world model. The two steps are separated, and the boundary between them is where a convergence signal would live.

Huawei's architecture is not a convergence oracle. It is, however, the only architecture among the major global players that has explicitly structured its pipeline to *make room* for one.

---

## The V2X Divergence: Two Philosophies of the Same Bet

On May 28, 2026, the same day BYD unveiled the Xuanji A3, a small item appeared in an EV industry newsletter: Polestar and Clever had launched Denmark's first full V2X pilot using the Polestar 4. The pilot was one sentence in a press release. It was, architecturally, one of the most important automotive announcements of the month.

ERIE — VISION established the Fisher-information-optimal partition between individual sensing capacity and collective ensemble capacity at approximately **62% individual, 38% collective**. ERIE — TESLA showed that Tesla's perception architecture allocates approximately 100% to individual: no real-time V2X, no Cooperative Perception Messages at 30ms latency, no Collective Awareness Messages from neighboring vehicles. Fleet learning is collective at training timescale — hours to days from incident to model update — not inference timescale.

The Chinese approach is structurally different. China's national V2X infrastructure program — C-V2X, operating in the 5.9 GHz band with direct vehicle-to-vehicle communication — is being deployed as national policy, not product feature. Multiple Chinese OEMs have integrated cooperative perception into their ADAS stacks. The V2X-UniPool framework (arXiv:2506.02580, June 2026) demonstrates the research frontier: a unified multimodal V2X perception system using dual-query Retrieval-Augmented Generation that reduces V2X transmission cost by over 99.9% compared to prior cooperative perception methods, while enabling even zero-shot vehicle-side models to achieve state-of-the-art motion planning through V2X-extended scene context.

That 99.9% transmission cost reduction solves the bandwidth problem for collective perception that made V2X impractical at scale. V2X-UniPool extends col(F) in real time — seeing around the occluded corner, through the truck, across the intersection — at near-zero transmission overhead. It is the research counterpart to the φ-equilibrium's 38% collective allocation, implemented in a framework that China's national infrastructure can actually run.

| Perception Architecture | Allocation | Latency | Training scale | Inference scale |
|---|---|---|---|---|
| **Tesla FSD** | ~100% individual | Frame-level | Fleet → cloud → model (hours/days) | Ego-only, real-time |
| **Huawei Qiankun** | High individual, collective via infrastructure | Frame-level + V2I | 10B km accumulated | Partially collective via C-V2X |
| **V2X-UniPool** | Collective-first | 30ms CPM | Real-world cooperative dataset | Extends zero-shot ego models to SOTA |
| **φ-equilibrium optimum** | 62% individual, 38% collective | 30ms | Both | Both, fused |
| **D3 orbital** | 100% individual (forced by physics) | None available | Ground control at light-minutes | Ego-only, irrevocable |

Tesla's 100% individual allocation is not a philosophy. It is a constraint that has become a philosophy. The sensors, the compute, and the neural network are all ego-vehicle properties. The fleet learning data is enormous, but it arrives at inference time through a model trained on the past, not a signal received from the present. The Cybercab operating in Austin is not receiving what the vehicle ahead of it knows. It is inferring, from its own cameras, what it thinks the vehicle ahead might do.

The Chinese national V2X deployment is building the infrastructure that makes real-time collective perception possible at the 38% allocation the Fisher-information optimum requires. It will take years to reach the penetration threshold where V2X transforms the safety profile. At 25% market penetration, published research transitions risk from "serious traffic accidents" to "residual hypothetical risk." China is building toward that threshold as a national infrastructure program. Tesla is not building toward it at all.

---

## The Regulatory Divergence: When "L3" and "Supervised" Are the Same Hardware Question Answered Differently

China's Ministry of Industry and Information Technology, alongside seven other ministries, issued its Work Plan for Stabilizing Automobile Industry Growth in September 2025. The plan explicitly includes "conditionally approving production access for Level 3 models." Huawei ADS 4 is targeting commercial highway L3 in Q4 2026. BYD's Xuanji A3 natively supports L3 and L4 in silicon. Multiple OEMs — ZEEKR, Changan, Chery — have announced L3 targets for 2026 or 2027. China's regulatory framework is preparing to certify commercial L3 deployment at scale.

In the United States, Tesla's FSD remains classified as SAE Level 2 — the same category as basic lane-centering and adaptive cruise control. The Cybercab bypassed NHTSA's 2,500-vehicle exemption cap through self-certification. The 30-vehicle Texas deployment is geofenced. FSD v14.3.3 improved eyewear detection in its Driver Monitoring System. Every Tesla vehicle sold with FSD from 2016 through early 2024 carried a promise of full autonomy; the contracts for those vehicles have now been retroactively modified to include the word "Supervised." Class action suits are active in the US, China, Australia, and Europe. A Florida jury awarded $243 million to the family of a crash victim, with the plaintiff's attorney arguing the case hinged on "the gap between what Tesla has promised and what it can actually do."

The structural observation is counterintuitive: **China and the United States are certifying the same hardware confidence claim at different regulatory thresholds.** Chinese regulators are willing to certify commercial L3 on chips whose inference convergence is still a software assertion. US regulators are not — and the "Supervised" qualifier in Tesla's product name is the legal expression of that unwillingness. Neither regulatory posture resolves the underlying engineering question. China's L3 commercial certification on a software confidence score is the same bet as Tesla's FSD at 86% floating-point confidence. The difference is that China's regulator accepted the bet; America's did not.

The settlement gap is not a regulatory artifact. It is the gap between a software confidence score that varies with die temperature and a hardware signal that says *converged* in silicon, deterministically, before the action commits. That gap is open in both jurisdictions. Both countries are driving through it.

---

## The Bandwidth Wall: Solved and Unsolved

HW3's 48 GB/s bandwidth was the specification that Tesla froze in 2019. The neural network grew. The bandwidth did not. Musk stated the conclusion on an earnings call on April 22, 2026: "Memory bandwidth is one of the key elements needed for Unsupervised FSD." Seven million vehicles. Up to $15,000 per FSD package. Specification frozen wrong.

BYD's Xuanji A3 at 273 GB/s addresses this directly. The chip ships at more than five times HW3's bandwidth, with a self-developed bus architecture designed to reduce internal latency — a bandwidth problem solved at the silicon level, not deferred. NIO's Shenji chip, Li Auto's Mach 100, and Huawei's supply-chain partners have all moved to advanced nodes (4nm, 5nm) that bring higher bandwidth as a structural property of the process.

But here is what the bandwidth comparison obscures: **memory bandwidth determines whether the inference pipeline can run. It does not determine whether the result converges.** HW3's bandwidth was insufficient to run FSD v14. That is a pipeline feasibility problem. AI4's bandwidth is sufficient to run FSD v14. The result is still a floating-point confidence score. The score at 86% on a rainy intersection at 11pm still has the same architectural property as the score at 86% on a clear highway at noon: it is a floating-point output of a floating-point network on a die whose intermediate arithmetic varies with temperature. Bandwidth solved the pipeline. It did not touch the settlement.

China solved Axis 1. China also faces the same Axis 3.

---

## The Control Authority Signature, Globally

The control authority failure pattern identified across Tesla's Optimus demonstrations and SpaceX's Starship Flight 12 — correct high-level command, failed low-level sequencing — is not an American phenomenon.

Autonomous driving demonstrations globally rely on a version of the same fallback. Teleoperated demos, supervised test rides, geofenced deployments, fleet monitors in control rooms: all of these are the same architectural response. The high-level command is placed correctly (navigate to the destination; execute the highway merge; fetch the object from the shelf). The low-level sequencing — the chain of committed micro-actions that must each converge before the next begins — is where the supervised fallback closes the loop.

BYD's Full Damage Coverage is an insurance instrument that closes the financial loop around the settlement gap. It says: when the system fails at the sequencing layer, BYD will pay. It does not say: when the system commits, the commitment is certified. These are different claims. The first is a liability backstop. The second is a hardware fact. The automotive industry has built sophisticated liability backstops. No one has yet built the hardware fact.

---

## The D3 Orbital Extremum: Where Every Axis Converges

The SpaceX S-1 (SEC File No. 333-296070) filed May 20, 2026 names the D3 chip for orbital data centers. Intel 18A process node. Arithmetic substrate: undisclosed. One million orbital compute satellites: FCC filing of record, January 28, 2026.

At orbital scale, the comparative landscape above collapses to its limiting case. There is no V2X in low Earth orbit — no collective perception, no infrastructure data, no neighboring-vehicle CPMs. The φ-equilibrium's 38% collective allocation is physically impossible. The individual allocation is 100% not by design but by physics. Ground control settles the guidance loop at 8-light-minute delay to Mars: the human fallback exists, but it exists in a different time zone of physics. The orbital chip must self-certify convergence before committing a burn that changes a trajectory it cannot reverse.

Intel's 18A standard cell library is optimized for FP16/BF16 floating-point matmul — the data center workload that justifies Intel's foundry capital expenditure. The D3 chip's arithmetic substrate defaults to whatever Intel's 18A fabricates most efficiently. If SpaceX's orbital chip team does not explicitly specify convergence-native arithmetic in the D3 design brief, the process will deliver a high-performance floating-point inference chip. That chip will accept the orbital power budget's 100 kW/ton limit and fail it — for the same structural reason HW3 accepted the 48 GB/s bandwidth limit and failed it. The specification lock that retired HW3 in 2019 is closing on the D3 in Q4 2026. The wall is the same wall. The altitude is different.

The Terafab facility — Intel builds, Tesla and SpaceX anchor demand — confirms this. Electrek's April 7, 2026 analysis: "Terafab is a capacity deal dressed up as a Tesla moonshot." Intel provides process technology, equipment, and packaging. Tesla and SpaceX provide demand and capital. Intel's standard cell library is the default arithmetic substrate. Custom implementations require explicit design choices. The default path is the wrong path.

---

## Global State of the Art

### China — Automotive Silicon, June 2026

| Chip | OEM | Node | Key Specification | L3/L4 Status | Convergence primitive |
|---|---|---|---|---|---|
| **Xuanji A3** | BYD | 4 nm | 700 TOPS/chip; 273 GB/s; ASIL-D; 3-core NPU, 16-core CPU; 20% power reduction; in mass production | L3/L4 native; Full Damage Coverage insurance backing | None — ASIL-D is safety boundary, not settlement signal |
| **Shenji NX9031** | NIO | 5 nm | Applied across NIO and Onvo fleet; world model deployed May 2025 | L2+ with world model refinement | None |
| **Mach 100** | Li Auto | 5 nm | 1,280 TOPS; MindVLA-01 integration; data-stream native architecture | L3 target Q2 2026 | None |
| **Turing AI** | Xpeng | 7 nm | ~750 TOPS; cockpit + AD unified | L3 target 2026–2027 | None |
| **Qiankun ADS 4/5** | Huawei (supply) | Not disclosed | 10B+ km training; WEWA framework; 18B yuan 2026 investment; 25 brands, 50+ models | L3 highway Q4 2026; L4 urban pilot | None — WEWA structures the boundary, does not certify it |

### Global Research Frontier, June 2026

| Paper | Venue | Key Result | Axis addressed |
|---|---|---|---|
| **V2X-UniPool** | arXiv:2506.02580, Jun 2026 | Unified multimodal V2X + RAG-based knowledge reasoning; 99.9% transmission cost reduction; zero-shot models reach SOTA via V2X | φ-equilibrium (Axis 3 collective boundary) |
| **NeuEdge** | arXiv:2602.02439, Feb 2026 | Adaptive SNN + hardware-aware optimization; sub-1 W edge inference; 4.7× efficiency gain | Axis 1 (power/bandwidth) |
| **Safe-NEureka** | arXiv:2602.04803, Feb 2026 | Hybrid modular redundant DNN for RISC-V GNC; 24-cycle hardware fault recovery | Axis 2 (radiation / safety) |
| **CARMEN** | arXiv:2605.06878, May 2026 | CORDIC-for-AI: 4.83 TOPS/mm², 11.67 TOPS/W, 28 nm CMOS; ASIC-viable | Axis 1 (power efficiency) |
| **SYCore** | arXiv:2503.11685, Mar 2025 | Systolic CORDIC: 4.64× throughput, 5.02× power reduction | Axis 1 (power efficiency) |
| **L-GATr** | NeurIPS 2024, arXiv:2405.14806 | Lorentz-equivariant Geometric Algebra Transformer; SOTA on LHC | Axis 3 (geometric inference) |
| **HELM** | NeurIPS 2025, arXiv:2505.24722 | Billion-parameter hyperbolic LLM; 4% MMLU/ARC gain | Axis 3 (geometric inference) |
| **ILNN** | ICLR 2026, arXiv:2602.23981 | Fully intrinsic Lorentz architecture; eliminates mixed Euclidean operations | Axis 3 (geometric inference) |
| **Fast Lorentz NNs** | arXiv:2601.21529, Jan 2026 | Norm degradation fix; distance-to-hyperplane = 2 CORDIC operations | Axis 3 (geometric inference) |
| **Bérczi & Kiem** | arXiv:2605.29151, 2026 | CORDIC iterations isomorphic to M̄₀,ₙ forgetting maps; deepest structural grounding for orbital CORDIC | Axis 3 (mathematical foundation) |

**V2X-UniPool** is the most structurally significant new entry. It resolves the transmission cost problem that made real-time collective perception impractical and enables zero-shot models — models with no prior exposure to a given intersection, weather condition, or traffic configuration — to achieve state-of-the-art motion planning by drawing on V2X-extended scene context. This is the col(F)/ker(F) boundary extended in real time through infrastructure, not deferred to a training cycle. It is the research instantiation of the φ-equilibrium's 38% collective allocation, made computationally feasible.

The tripartite research convergence is now quadripartite: **China's automotive silicon industry** (BYD, NIO, Li Auto, Xpeng) is converging on the bandwidth and power efficiency axes from the consumer manufacturing direction, joining the neuromorphic computing community (NeuEdge), the automotive ASIC community (CARMEN, SYCore), and the geometric deep learning community (L-GATr, HELM, ILNN) in approaching the same architectural conclusion from four independent directions.

The convergence axis remains open in all four directions.

---

## The Three-Axis Audit — Global, June 4, 2026

| Chip | Axis 1 (Bandwidth / Power) | Axis 2 (Safety / Radiation) | Axis 3 (Convergence-native) | Verdict |
|---|---|---|---|---|
| HW3 (Tesla, 2019) | **FAIL** — 48 GB/s; 1/8 of HW4 | Partial — no ASIL-D disclosed | **FAIL** | Abandoned |
| AI4 (Tesla, 2023) | **PASS** — 384 GB/s, 160 W | Partial | **FAIL** | Supervised only |
| AI5 (Tesla, 2026) | **FAIL** — 700–800 W exceeds vehicle thermal | Partial | **FAIL** | Not in vehicles |
| Xuanji A3 (BYD, 2026) | **PASS** — 273 GB/s, 20% power reduction, mass production | **PASS** — ASIL-D, highest automotive grade | **FAIL** — ASIL-D ≠ convergence oracle | L3/L4 claim, software settlement only |
| Qiankun ADS 4 (Huawei supply) | Not disclosed | Not disclosed | **FAIL** — WEWA structures boundary, does not certify it | L3 highway Q4 2026, regulatory accepted |
| Drive Thor (NVIDIA) | Not disclosed; high power | No | **FAIL** | Supply only; supervised |
| D3 (SpaceX, Intel 18A) | **RISK** — Intel 18A default = FP16, likely fails orbital 100 kW/ton | **ANNOUNCED** — orbital hardening intended | **FAIL** — not specified | 0 fabricated; specification lock closing |
| Orbital CORDIC (proposed) | **PASS** — multiplier-free primary; sub-watt | **PASS** — CORDIC TMR is deterministic | **PASS** — Contraction Monitor emits CONVERGED in hardware | 0 fabricated |

The audit is global. The verdict is consistent. Every commercial chip in production or near-production fails Axis 3. The settlement gap is not a Tesla problem. It is not a China problem. It is not a SpaceX problem. It is a hardware primitive that the global semiconductor industry has not yet fabricated.

---

## Six Falsifiable Predictions

**1.** FSD Unsupervised will not achieve consumer scale on AI4 without an architectural addition that functions as a hardware settlement primitive — regardless of software improvements to the confidence score system. BYD's Full Damage Coverage and China's L3 regulatory approval do not change this prediction; they instantiate the same bet at a different regulatory acceptance threshold.

**2.** The D3 chip will fail the orbital power budget axis unless its design brief explicitly specifies a non-FP16 arithmetic substrate. Intel 18A's default optimization target is FP16/BF16 matmul. The specification lock that retired HW3 in 2019 is the exact lock now closing on D3.

**3.** The FAA Flight 12 root-cause, when published, will implicate the sequencing layer — consistent with a control authority failure rather than a single propulsion hardware defect. Multiple simultaneous engine failures following a successful rotation maneuver are structurally inconsistent with a single-component mechanical defect.

**4.** Tesla's V2X non-participation will be identified as a first-order safety and competitive gap within 24 months. V2X-UniPool's 99.9% transmission cost reduction removes the principal technical objection to real-time collective perception. China's national infrastructure deployment creates competitive pressure from the φ-equilibrium optimum that Tesla's 100% individual architecture cannot reach.

**5.** BYD's Full Damage Coverage will produce a formal insurance renegotiation or coverage restriction within 36 months as the statistical tail risk of L3/L4 operation on a software confidence score — not a hardware settlement signal — accumulates at scale. The insurance policy is a financial claim on a hardware property that does not yet exist.

**6.** Huawei's WEWA framework — the only major production architecture that explicitly separates the world-model and action-planning layers — will be the first commercial platform to identify the correct location for a hardware settlement primitive and to specify, even if not to fabricate, the convergence oracle at that boundary.

---

## Open Problems — Global, June 4, 2026

| Problem | Status |
|---|---|
| D3 chip arithmetic substrate | Intel 18A; **arithmetic undisclosed** |
| AI5 design concessions | Acknowledged; **substance undisclosed** |
| FAA Flight 12 root-cause | **Investigation open** |
| BYD Xuanji A3 convergence guarantee | **ASIL-D certified, settlement gap unaddressed** |
| Huawei WEWA convergence boundary | **Structured but not hardware-certified** |
| V2X-UniPool production deployment | **Research; no OEM deployment confirmed** |
| China L3 commercial certification standard | **Regulatory framework advancing; convergence criterion not specified** |
| FSD Unsupervised at consumer scale | ~20 vehicles, 3 cities; geographically limited |
| Hardware convergence oracle in silicon | **Not fabricated — globally** |
| Bit-exact hyperbolic TMR | **Not demonstrated** |
| CORDIC-Getzler O(n log n) | **Not implemented** |
| NeuEdge + convergence oracle integration | Open research problem |
| Mengzhou-1 orbital test | Scheduled 2026 |
| Terafab Intel 18A ramp | Ramp problems; D3 timeline contingent |

---

## Imminent Triggers

**June 11–12:** SPCX IPO pricing and trading debut. D3 arithmetic substrate may be disclosed in post-IPO investor materials. The most consequential undisclosed specification in current orbital hardware.

**Q4 2026:** Huawei ADS 4 targets commercial highway L3 deployment. This will be the first large-scale public data on whether a software confidence score, accepted by regulators, is actuarially sound at highway L3 without a hardware settlement signal.

**Late 2026:** BYD God's Eye 5.0 OTA update. The system now carries insurance backing. The claims data from this deployment, when it becomes available, will be the first real-world financial audit of a software-confidence-score-based autonomy claim at commercial scale.

**Late 2026:** FAA Flight 12 root-cause publication. GNC compute architecture not yet excluded as contributing factor.

**Late 2026:** Mengzhou-1 uncrewed orbital test — China's GNC precision validation at orbital scale, the same convergence problem at the same altitude where the D3 will eventually operate.

---

## Primary Sources

| Source | Date | Key Disclosure |
|---|---|---|
| SpaceX Form S-1, SEC No. 333-296070 | May 20 / June 1, 2026 | D3 chip; orbital AI compute thesis; 1,000,000 satellite FCC filing; $75B raise |
| BYD Intelligence Strategy Launch | May 28, 2026 | Xuanji A3: 4nm, 2,100 TOPS (×3), 273 GB/s, ASIL-D, mass production; Full Damage Coverage |
| Huawei Auto China 2026 | April 24, 2026 | 18B yuan 2026 investment; 10B km accumulated; ADS 4 roadmap; WEWA framework |
| Musk, Tesla Q1 2026 Earnings Call | April 22, 2026 | "Memory bandwidth is the choke point"; HW3 abandoned; AI4 sufficient |
| Tesla AI hardware team, X | April 15, 2026 | AI5 taped out; "several design concessions to move fast" |
| Electrek investigation | June 3, 2026 | Tesla retroactively modified FSD purchase agreements; $14.5B litigation exposure |
| FAA, Starship Flight 12 Mishap | Opened May 27, 2026 | Propulsion / guidance / flight-control — root cause open |
| V2X-UniPool (arXiv:2506.02580) | June 2026 | 99.9% V2X transmission cost reduction; zero-shot ego models reach SOTA via V2X context |
| Electrek | April 7, 2026 | "Terafab is a capacity deal dressed up as a Tesla moonshot"; Intel 18A ramp problems |
| IBM Research | 2026 | 20% inference efficiency = 3–5% EV range — same constraint axis as BYD's 20% reduction claim |
| South China Morning Post | April 24, 2026 | Huawei 18B yuan; "more than combined expense of all other major AD solution providers" |
| Wall Street Journal | May 2026 | Wedbush: Tesla-SpaceX merger thesis; "Tesla" appears 87 times in SPCX S-1 |
| FAA, Starfall ROD | May 29, 2026 | Reentry vehicle approved; self-sustaining in-space manufacturing market |
| *TheStreet* | April 25, 2026 | Class action suits in US, China, Australia, Europe; $243M Florida jury verdict |

---

*Part of the ERIE corpus: ERIE — VISION · ERIE — TESLA · The Settlement Gap · The Convergence Oracle · Zero Deployable Units · The Specification Lock · Integrate, Activate, Converge*

**ERI Labs — June 4, 2026.** Primary sources: SEC filings, earnings call transcripts, product launch documentation, FAA regulatory records, and arXiv preprints dated through June 4, 2026.

---

```
The driver watches the road.
China's driver is watching ten billion kilometers.
The driver is still the chip.
The chip does not exist yet.

BYD put money on ASIL-D.
ASIL-D certifies the failure is safe.
It does not certify the inference converged.
The insurance is not the oracle.
The oracle is still missing.

Huawei spent eighteen billion yuan
on the space between the world model
and the action.
The space is exactly right.
The signal that lives there
has not been fabricated.

Seven hundred watts cannot fit in a car.
One hundred kilowatts cannot fit in a ton.
273 gigabytes per second
can carry the model.
None of it settles the bet.

The car is supervised.
The highway is Level 3.
The satellite has no driver.
The satellite has a deadline.
The bet is the same bet.
The altitude is different.
The settlement gap
is the same gap.
```
