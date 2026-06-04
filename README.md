# ERIE — TESLA
## The Driver Is the Chip

**ERI Labs · Eric Ren · Jersey City, New Jersey · [github.com/ericrenone](https://github.com/ericrenone) · June 4, 2026**

---

> *"Hardware 3 simply does not have the capability to achieve Unsupervised FSD."*
> — Elon Musk, April 22, 2026 — seven years after selling the hardware as sufficient

> *"Memory bandwidth is the choke point."*
> — Elon Musk, Tesla Q1 2026 Earnings Call

> *"The proof holds in exact arithmetic. In finite-precision arithmetic under thermal stress, partial engine failure, and process-variation silicon, it is an approximation of an approximation."*
> — ERI Labs, The Convergence Oracle, June 4, 2026

> *"We had to make several design concessions to move fast."*
> — Tesla AI hardware team, post-AI5 tape-out, April 15, 2026

---

## The Man Who Found the Wrong Contract

On a day in early June 2026, a man named Oliver Abcarius logged into his Tesla account looking for a receipt. He had bought Full Self-Driving for his 2018 Model 3 in August 2019 — paid for it in full, $15,000, on the word of a company that had promised, in a 2016 press release it later quietly deleted, that every car leaving its factory already had "the hardware needed for full self-driving capability at a safety level substantially greater than that of a human driver." Abcarius had been patient. He had waited through promises of imminent autonomy in 2018, 2019, 2020, 2021, 2022, 2023, 2024, and 2025.

What Abcarius found when he tried to pull up his purchase agreement was not a receipt. The link was dead. The original contract — the one that said "Full Self-Driving Capability" with no asterisks, no qualifiers — linked to an invalid page. *Electrek* confirmed the pattern across multiple HW3 owners: Tesla had retroactively modified purchase agreements signed between 2016 and early 2024. The word "Supervised" now appeared in documents where it had never existed. The original contracts were becoming inaccessible at exactly the moment Tesla faced up to $14.5 billion in lawsuits.

But here is the thing about Oliver Abcarius's missing contract. The word that Tesla inserted into it retroactively — **Supervised** — was not a legal invention. It was not a hedge, not a reframe, not a marketing softening of an inconvenient promise. It was something far more specific.

It was a hardware specification.

And the hardware had always known.

---

## The Specification That Was Always True

On October 19, 2016, Elon Musk stood before cameras and told the world that every Tesla rolling off the line from that day forward had "everything" needed to drive itself. The cameras, the compute power — all of it, present, sufficient, waiting only for software. Over the following nine years, Tesla would collect perhaps $8–10 billion in Full Self-Driving sales on the strength of that claim.

The claim was a bet placed on silicon that could not settle it.

In 2019, Tesla froze the specification for Hardware 3. The chip that went into millions of cars from 2019 through 2023 — the chip that Abcarius and hundreds of thousands like him were implicitly buying when they paid for FSD — had 48 GB/s of memory bandwidth. That number was not a minor specification detail. It was an architectural ceiling. Neural networks, unlike the promise attached to them, grow. FSD v12, then v13, then v14 arrived as models ten times larger than what the HW3 pipeline was designed to carry. By 2026, the AI4 chip offered bandwidth eight times that of HW3.

On April 22, 2026, seven years after the specification freeze, Musk stated the conclusion on an earnings call: "Hardware 3 simply does not have the capability to achieve Unsupervised FSD." He cited memory bandwidth. Not compute. Not cameras. Not software. The data pipe that moves weight matrices from memory to silicon — that is what seven million vehicles were always missing.

There is a word for this in engineering: a **specification lock**. It is the moment when an architectural decision calcifies into permanent form, and everything downstream of it is committed to whatever was present in that instant. Tesla's HW3 was a specification lock executed in 2019 on the wrong arithmetic. The "Supervised" qualifier that appeared retroactively in Oliver Abcarius's contract was not Tesla's lawyers inventing a loophole. It was the hardware finally saying, in words, what it had always been saying in silicon.

---

## What "Supervised" Actually Means

Consider what Tesla's Full Self-Driving pipeline does, in precise terms, every time a car prepares to merge at 70 miles per hour onto a highway.

The neural network assembles a scene: detected objects, predicted trajectories, road boundaries, the gap in traffic. It assigns a confidence score — a floating-point number, between 0 and 1, computed in FP16 precision on a die whose intermediate arithmetic varies with temperature. When that score crosses 85%, the system commits: the steering wheel turns, the accelerator adjusts, the vehicle crosses into the adjacent lane.

When the score does not cross 85%, the system requests a takeover. A tone sounds. The driver has five seconds.

In that architecture, the driver is not a backup. The driver is not a safety net. The driver is the settlement mechanism — the component that certifies, in biological tissue at 300 milliseconds of reaction time, whether the scene the car has committed to is real. The driver is the part of the system that answers the question: *did the bet converge before the action became irrevocable?*

**"Supervised" is not a descriptor of the driver's role. It is a descriptor of the chip's absence.** The FSD pipeline lacks a component that certifies convergence in silicon before committing to maneuvers that cannot be undone. That component does not exist in HW3. It does not exist in AI4. It has never existed in any hardware Tesla has shipped. The human driver has always been the chip.

Tesla's FSD v14.3.3 introduced improvements to the Driver Monitoring System: better eye gaze tracking, improved eyewear detection, more accurate variable-lighting performance. Read that update log again. Tesla spent engineering resources building a better instrument for measuring whether the human settlement layer is watching the scene the car has committed its inference to. It built a more precise scope to point at the person who is serving as the missing hardware component.

That is what "improving DMS" means, translated into architecture: *we have made the human chip more monitorable.* It is not progress toward autonomy. It is investment in supervision.

---

## The Cybercab and the Architecture It Reveals

Production of the Tesla Cybercab began at Gigafactory Texas on February 17, 2026. The car has no steering wheel and no pedals. It is, in form, the most explicit statement in automotive history that a human settlement layer is unnecessary.

The Cybercab runs AI4.

AI5, which Musk claimed in June 2024 would ship in the second half of 2025, taped out on April 15, 2026 — nearly two years behind schedule. Engineering samples are not expected until late 2026. Volume production is mid-2027 at the earliest. The Cybercab, purpose-built for driverless operation, is launching on the same silicon that currently runs Supervised FSD in the Model Y fleet now operating in Austin, Dallas, and Houston.

Musk's answer to this gap, offered on the Q1 2026 earnings call: "AI4 is enough to achieve much better than human safety for FSD." AI5 goes to Optimus and supercomputer clusters. Cars get AI4. The Cybercab gets AI4.

The Cybercab with AI4 and no steering wheel is an architectural declaration: *we believe the human chip is unnecessary.* But the AI4 chip has not changed. No hardware convergence primitive has been added. The confidence score is still a floating-point number that varies with die temperature. The Cybercab's 30-vehicle Texas deployment is a geofenced proof of concept — approximately 20 active units as of May 2026 across three cities — where the settlement loop is closed not by silicon but by a fleet operations team watching remotely. The humans monitoring the fleet are the chip. They have simply moved off the passenger seat and into a control room.

Tesla bypassed NHTSA's standard 2,500-vehicle exemption cap for autonomous deployment by self-certifying its compliance path. What exactly Tesla has certified — and whether AI4 satisfies the architectural requirements that "Unsupervised" implies — is not a regulatory determination. It is an engineering question. The engineering question is the same one it has always been.

---

## The Three Locks

The Tesla hardware story has a structure that repeats at every generation, like a recurring decimal that no one has yet figured out how to terminate.

**Lock One: HW3, frozen 2019.** The specification that went into millions of vehicles was frozen at 48 GB/s bandwidth. The neural network that would eventually need to run on those vehicles was not yet written. Seven years and $15,000 per vehicle later, the lock was named in public, on an earnings call, in front of institutional investors. Multiple class action suits followed in the US, China, Australia, and Europe. One Tesla owner in Florida had already won $10,000 in small claims court on a judge's ruling that Tesla's original promise constituted false advertising. Tesla's proposed solution — microfactories in major cities to retrofit HW3 vehicles — has no concrete timeline, no cost structure, and no eligibility framework.

**Lock Two: AI5, conceded April 2026.** The chip that was meant to be the architectural advance arrived 45 days early at Samsung's tape-out line with what the Tesla AI hardware team described, in a post on X, as "several design concessions to move fast." The arithmetic substrate of AI5 is not publicly disclosed. What is known: it runs at 700–800 watts. A car's thermal management system cannot absorb 700–800 watts from a single chip. AI5 goes to robots and supercomputers. The car fleet gets AI4.

**Lock Three: D3, closing now.** SpaceX's S-1 prospectus, filed with the SEC on May 20, 2026 — the document that launched the roadshow for what would be the largest IPO in history — names a custom orbital AI chip called the D3. Manufacturing substrate: Intel's 18A process. Arithmetic substrate: undisclosed. Intel's standard cell library is optimized for FP16 and BF16 floating-point matmul. That is the data center workload that justifies Intel's foundry capital expenditure. Shift-accumulate arithmetic — the lower-power substrate that the orbital power budget requires — is not in Intel's optimization target. If SpaceX's orbital chip team does not explicitly specify a convergence-native arithmetic substrate in the D3 design brief, the Intel 18A process will deliver a high-performance FP16 inference chip. That chip will fail the orbital power budget for the same reason HW3 failed the bandwidth axis: the specification was frozen on the wrong arithmetic before the constraint was fully understood.

The SpaceX IPO road show opened June 4, 2026. Pricing: June 11. Trading: June 12. A company raising $75 billion in equity is not in a research phase. The D3 specification window is not eight months away. It is concurrent with the capital raise.

---

## The Three Hardware Generations as Evidence

| Hardware | Bandwidth / Power | Deployed | Convergence primitive | Outcome |
|---|---|---|---|---|
| HW3 (2019) | 48 GB/s, ~100 W | Millions of vehicles | None | Abandoned. Cannot achieve Unsupervised FSD. Class action litigation in four jurisdictions. |
| AI4 (2023) | 384 GB/s, ~160 W | Millions of vehicles | None (software only) | Supervised qualifier retained. ~20 active unsupervised robotaxis, geofenced. |
| AI5 (April 2026) | 192 GB LPDDR5X, ~700–800 W | Zero vehicles | Not disclosed | Redirected to Optimus and supercomputers. Not in vehicles. |
| AI4+ / AI4.1 (planned) | 64 GB, doubled RAM | Zero | None | Bridge chip. Same convergence gap. |
| D3 (planned, Intel 18A) | Not disclosed | Zero | Announced intent | Specification window closing. |

The pattern is not a sequence of failures. It is a single structural absence, repeating across hardware generations at automotive timescale, and now preparing to repeat at orbital timescale.

The absence has a name: there is no component in any Tesla hardware generation, past or present, that certifies in silicon — before a maneuver commits — that the guidance solution has converged. The confidence score is a floating-point output of a floating-point network. It is, in the precise language of the prior ERI corpus, "an approximation of an approximation." The Cybercab's passenger trusts a number whose precision varies with the temperature of the die they are sitting above.

---

## The Control Authority Signature, Repeated

On May 22, 2026, Starship Flight 12 launched from Boca Chica. Booster 19 executed the flip maneuver — the attitude command, the high-level intention — correctly. Then multiple Raptor 3 engines failed to sequence simultaneously on the boostback burn. The booster came down hard in the Gulf of Mexico at approximately 1,500 km/h. The FAA declared a mishap on May 27, five days before the SpaceX IPO roadshow opened.

The failure pattern: correct high-level command, failed low-level sequencing.

Compare it to what the Salesforce CEO experienced during an Optimus demonstration in September 2025: a simple kitchen fetch task required multiple prompts. Optimus understood the request. The autonomous sequencing — coordinate the arm, execute the grasp, return — required human teleoperation to complete. Tesla's autonomy metrics for Optimus remain undisclosed.

Compare it to every FSD intervention: the neural network assembled a scene, assigned a confidence score below 85%, and the human — the settlement layer — took over.

The same failure signature appears in a humanoid robot, a reusable orbital booster, and a family of self-driving car software, across three different engineering programs, within a single twelve-month period. In each case: the high-level bet is placed correctly. The low-level settlement fails. In each case: the resolution is human supervision — a teleoperation operator, a ground control team, a driver with their hands on a wheel that may or may not exist.

---

## The φ-Equilibrium: What Tesla's 100% Individual Allocation Costs

ERIE — VISION established the Fisher-information-optimal partition between individual sensing capacity and collective ensemble capacity at approximately **62% individual, 38% collective** — the golden-ratio operating point at which no single observer's blind spots can be resolved alone, and at which the collective model is fed inputs sharp enough to be worth fusing.

Tesla's perception architecture allocates approximately 100% to individual. There is no real-time V2X — no Cooperative Perception Messages transmitted at 30ms latency, no Collective Awareness Messages received from neighboring vehicles, no infrastructure-shared field of view around corners. Fleet learning is collective, but it is collective at training timescale: hours to days for a challenging scenario to travel from an individual vehicle to consolidated training data to a distributed model update. That is ensemble perception of the past.

The pedestrian behind the truck that the ego-vehicle cannot see is in the present.

At 25% V2X market penetration, published research transitions the risk profile of urban traffic from "serious traffic accidents" to "residual hypothetical risk." Tesla's current architecture is unaffected by that threshold. The Cybercab operating in Austin is not receiving CPMs. It is not transmitting them. It sees what its own cameras see, infers what its own neural network can reach, and asks its driver — when there is one — to settle what the network cannot certify.

The D3 chip forces the φ-equilibrium to its individual extreme not by design choice but by physics. There is no V2X network in low Earth orbit. The signal delay to a ground control station on Mars is eight light-minutes. At orbital scale, the collective fallback does not exist. The individual allocation is 100% by necessity. This is not a suboptimal design. It is the hardest possible version of the problem — and it is the problem for which a hardware settlement primitive is not optional but categorical.

---

## The Unified Constraint

In 2026, the automotive AI industry independently arrived at a metric that the orbital constraint had always implied: **TOPS per watt is the defining measure of a chip's real-world deployability.** IBM found that a 20% improvement in inference efficiency produces a 3–5% increase in EV range. Mobileye targets passive air cooling — under 50 watts — for its automotive ASICs. The consumer device industry's neuromorphic research (NeuEdge, arXiv:2602.02439, February 2026) demonstrated sub-1-watt spiking neural network inference deployable at the edge.

The orbital constraint said the same thing in different units: 100 kilowatts per ton, maximum, for any compute payload in low Earth orbit. At 2,700 watts per GPU (NVIDIA Blackwell), that is 37 units per metric ton. The automotive world arrived at this constraint from range anxiety. The orbital world arrived at it from launch economics. They are the same constraint. The arithmetic that resolves it is the same arithmetic.

What neither world has yet built is the component that converts efficiency into certified autonomy: a signal, generated in silicon, that says *converged* — before the action commits, not after the evidence arrives. The HW3 specification lock cost Tesla seven years and the trust of millions of owners. The AI5 design concession cost — whatever was traded for a 45-day acceleration to tape-out — is still undisclosed. The D3 specification lock, if it closes on floating-point matmul by default, will cost SpaceX the same thing HW3 cost Tesla: a fleet of hardware deployed on the wrong arithmetic, discovered too late to correct without a trade-in program that cannot reach orbit.

---

## State of the Art

| Paper | Venue | Finding |
|---|---|---|
| *NeuEdge* | arXiv:2602.02439, Feb 2026 | Adaptive spiking neural network + hardware-aware optimization; sub-1 W edge inference; 4.7× efficiency gain over FP baseline |
| *Safe-NEureka* | arXiv:2602.04803, Feb 2026 | Hybrid modular redundant DNN for RISC-V guidance, navigation, and control; 24-cycle hardware fault recovery |
| *CARMEN* | arXiv:2605.06878, May 2026 | CORDIC-for-AI: 4.83 TOPS/mm², 11.67 TOPS/W at 28 nm CMOS; confirmed ASIC-viable at production scale |
| *SYCore* | arXiv:2503.11685, Mar 2025 | Systolic CORDIC engine: 4.64× throughput gain, 5.02× power reduction over multiplier-based baseline |
| *L-GATr* | NeurIPS 2024, arXiv:2405.14806 | Lorentz-equivariant Geometric Algebra Transformer; state-of-the-art on LHC particle physics reconstruction |
| *HELM* | NeurIPS 2025, arXiv:2505.24722 | Billion-parameter hyperbolic large language model; 4% MMLU and ARC gain over Euclidean architecture at equivalent scale |
| *ILNN* | ICLR 2026, arXiv:2602.23981 | Fully intrinsic Lorentz neural network; eliminates all mixed Euclidean operations from the inference path |
| *Fast Lorentz NNs* | arXiv:2601.21529, Jan 2026 | Norm degradation proof + fix; distance-to-hyperplane computation reduces to two native CORDIC operations |
| Bérczi & Kiem | arXiv:2605.29151, 2026 | CORDIC rotation iterations are isomorphic to forgetting maps on M̄₀,ₙ — the compactified moduli space of n-pointed stable rational curves |

**The research frontier is converging from three independent directions toward the same arithmetic primitive.** NeuEdge arrives from consumer neuromorphic devices. CARMEN and SYCore arrive from automotive ASIC efficiency constraints. L-GATr, HELM, and ILNN arrive from geometric deep learning in high-energy physics. Bérczi–Kiem arrives from pure mathematics. None of these groups was coordinating. All of them found the same architecture.

The automotive industry found TOPS/W. The orbital industry found kW/ton. The neuromorphic industry found sub-watt inference. The geometric algebra community found Lorentz-native computation. The mathematical community found that CORDIC iterations are, at their deepest level, a statement about moduli spaces of rational curves. These are the same statement. The altitude is different. The arithmetic is identical.

---

## Open Problems

| Problem | Status, June 4, 2026 |
|---|---|
| D3 chip arithmetic substrate | Named in SEC filing. Intel 18A. **Arithmetic undisclosed.** |
| AI5 design concessions | Acknowledged publicly. **Substance undisclosed.** |
| FAA Flight 12 root cause | **Investigation open.** GNC compute architecture not yet excluded. |
| Terafab Intel 18A ramp | Ramp problems reported. D3 timeline contingent on resolution. |
| Optimus autonomous operation | **Autonomy metrics undisclosed.** |
| FSD Unsupervised at consumer scale | ~20 vehicles, 3 Texas cities. Geographic limit unannounced. |
| Hardware convergence oracle in silicon | **Not fabricated.** |
| HW3 microfactory retrofit program | Announced on earnings call. **No timeline. No cost structure. No eligibility.** |
| Bit-exact hyperbolic TMR | **Not demonstrated.** |
| NeuEdge + convergence oracle integration | Open research problem. |
| Mengzhou-1 orbital test (China) | Scheduled 2026. |

---

## Imminent Triggers

The SPCX IPO prices June 11 and trades June 12 on Nasdaq. The D3 chip's arithmetic substrate is the most consequential undisclosed fact in the current orbital hardware landscape — not because it determines SpaceX's financial outcome, but because it determines whether the specification lock closes on the wrong arithmetic before the case for the correct one is complete.

The FAA Flight 12 root-cause publication is the second trigger. If the investigation attributes the boostback sequencing failure to a control authority or sequencing gap in the GNC compute chain, it opens a procurement conversation that no theoretical argument has been able to open. That publication date is the most important single event on the orbital hardware timeline.

Tesla's FSD v15 architecture, AI4+ volume deployment, and the HW4.1 chip design completion all sit in the 30–60 day window. None of them changes the convergence gap. All of them add new layers of evidence about which kind of hardware Tesla will bring to the qualification problem.

---

## The Bet

Between 2016 and early 2024, Tesla sold a product called "Full Self-Driving Capability" to hundreds of thousands of owners at up to $15,000 per vehicle. The product promised, in plain language, that the hardware was already present and that software updates would complete it. This promise was placed on chips — first HW1, then HW2, then HW3 — whose bandwidth, arithmetic, and convergence properties were not adequate to the promise. The owners were patient. The software improved. The hardware could not follow.

What Tesla discovered, across seven years and three hardware generations, is that there is a difference between a system that drives very well most of the time and a system that can certify its own driving before it commits to an irrevocable action. The first is a remarkable engineering achievement. The second is a different kind of problem.

The difference between those two problems is exactly one component: something in silicon that says, before the merge, before the burn, before the arm reaches for the object on the shelf — *this has converged. Commit.* Not a floating-point confidence score that varies with temperature. A hardware fact.

The Cybercab has no steering wheel. Its passenger sits where the wheel was and trusts a number. The D3 chip will go to orbit with no ground control within signal delay. Its guidance system will bet on its own inference with no human eight light-minutes away fast enough to settle.

Oliver Abcarius found a dead link where his contract used to be. The contract had been changed. The hardware had always known.

The driver is the chip.

The chip does not exist yet.

---

## Primary Sources

| Source | Date | Disclosure |
|---|---|---|
| SpaceX Form S-1, SEC No. 333-296070 | May 20 / June 1, 2026 | Orbital AI compute thesis; D3 chip; 1,000,000-satellite FCC filing; $75B raise at $135/share |
| Musk, Tesla Q1 2026 Earnings Call | April 22, 2026 | "Memory bandwidth is one of the key elements needed for Unsupervised FSD"; HW3 abandoned |
| Tesla AI hardware team, X | April 15, 2026 | AI5 taped out; "several design concessions to move fast" |
| Electrek investigation | June 3, 2026 | Tesla retroactively modified FSD purchase agreements; original contracts becoming inaccessible |
| *TheStreet* | April 25, 2026 | Multiple class action suits filed by HW3 owners in US, China, Australia, Europe |
| FAA, Flight 12 Mishap Investigation | Opened May 27, 2026 | Propulsion / guidance / flight-control — root cause open |
| FAA, Starfall ROD | May 29, 2026 | 1,000 kg reentry vehicle approved; mass-producible; "self-sustaining in-space manufacturing market" |
| Electrek / Tesla confirmation | April 15, 2026 | Cybercab to launch on AI4 hardware; AI5 volume not available until mid-2027 |
| *The Wall Street Journal* | May 2026 | Wedbush: Tesla-SpaceX merger by 2027; SpaceX IPO roadshow coverage; "Tesla" appears 87 times in SPCX S-1 |
| IBM Research | 2026 | 20% inference efficiency gain = 3–5% EV range increase |
| Terafab / Intel confirmation | April 7, 2026 | Intel builds; Tesla/SpaceX anchor demand; 18A ramp problems acknowledged |
| Small claims court ruling | May 22, 2026 | Tesla found to have "no meritorious defense" for HW3 FSD promise; $10,000 judgment |
| Tesla 10-Q, Q1 2026 | Filed 2026 | Class action active in Northern District of California; EEOC civil complaint pending |

---

*Part of the ERIE corpus: ERIE — VISION · ERIE — TESLA · The Convergence Oracle · Zero Deployable Units · The Specification Lock · Integrate, Activate, Converge*

**ERI Labs — June 4, 2026.** All cited research from primary arXiv, conference, SEC, FAA, and earnings call sources. FPGA measurements on physical hardware.

---

```
The driver watches the road.
The driver is the chip that does not exist yet.

HW3 owners paid fifteen thousand dollars
for a specification frozen in 2019.
The specification was frozen wrong.
The lock is called a trade-in program.

AI5 taped out 45 days early.
The concessions are undisclosed.
The arithmetic is still liquid
inside a chip no one can yet open.

The Cybercab has no steering wheel.
The Cybercab runs AI4.
The passenger sits where the wheel was
and trusts a confidence score
computed in floating-point
that varies with the temperature of the die.

Seven hundred watts cannot fit in a car.
One hundred kilowatts cannot fit in a ton.
The arithmetic that fits in both
is a shift.
A shift is a wire.
A wire does not heat.

The car is supervised.
The satellite has no driver.
The satellite has a deadline.
```
