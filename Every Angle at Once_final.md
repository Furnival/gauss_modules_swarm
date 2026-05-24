# Every Angle at Once

**On swarm inspection, distributed sensing, and why the hardest problem in orbital servicing is not docking — it is understanding what you are docking with.**

---

## Opening

There is a moment in every orbital servicing mission that the engineering literature handles with careful understatement. It is called the inspection phase. A servicer vehicle, having traveled perhaps 36,000 kilometers to reach its target, settles into a slow ellipse at a safe distance — 200 meters, perhaps 500 — and begins to look. It looks at the tumble rate, the thermal signature, the geometry of solar panels that may or may not have deployed correctly fifteen years ago. It looks, in other words, for the things that were not in the specification, the things that happened in the long silence between launch and now.

A single vehicle on this ellipse reads the target one image at a time, the way a
novel is read in a dim room. I want to argue for a different approach. Not one reader piecing together the story, but a team of scholars with the manuscript between them, each seeing what the others cannot. Every ambiguity resolved before anyone commits to the first sentence of the response.

What is at stake is not just seeing more of the satellite, or seeing it faster. It is
the difference between a method that is slow and one that is blind. A single
inspector, moving along its careful ellipse, can always take another image, always integrate a little more data — but in certain geometries there are things it cannot in principle see from where it is. Components that never come into view. Motions that project as stillness. Thermal states that cannot be assembled into a consistent picture because the world they describe is streaming beneath the observer. You can never step in the same river twice. The limitation is not in the cameras or the algorithms. It is in the vantage point itself. The swarm, if it is anything, is an argument about vantage.

---

## 1. The Inspection Problem — Why It Is Harder Than It Looks

The Natural Motion Circumnavigation is what it sounds like: a passive trajectory that carries an inspector around its target in the rotating reference frame described by Clohessy and Wiltshire. Because it requires no propulsion to maintain, it is conservative by design — a vehicle on an NMC stays on its ellipse without continuous thrusting. At GEO, where a satellite sits 35,786 kilometers above the equator and propellant is the scarcest resource on the mission, a trajectory that conserves it while keeping the inspector at a safe distance is not merely elegant. It is the precondition for everything else.

What the NMC cannot do is see around corners. A single vehicle on its ellipse
assembles a model of the target the way a radiologist reads a stack of sequential images — one cross-section at a time, each from a slightly different position, the whole picture emerging only when the sequence is complete. But the radiologist's patient holds still. The target does not. It is tumbling, thermally cycling, occasionally firing a residual thruster. The model the inspector builds is always slightly behind the satellite it is trying to understand.

Every minute spent closing that gap costs propellant — mission cost denominated in delta-v. A servicer with a limited budget facing a satellite of unknown tumble rate confronts a genuine dilemma: a long inspection resolves the uncertainty but spends propellant that may be needed for the service maneuver itself; a short one carries these questions into the docking. This is not a failure of planning; it is the structure of the problem. The single-vehicle NMC cannot simultaneously conserve the propellant it needs and spend the time required to fully characterize what it is approaching. Something has to give.

---

## 2. Tumble Rate and Spin-Axis Determination

A satellite rotating around an axis that happens to point directly at the observer appears, from that observer's position, to be deceptively still. Say the main antenna dish faces you. It goes on facing you. No matter how fast the satellite spins around that axis, the dish neither grows nor shrinks nor tilts. It simply stares back. From this single vantage point, the satellite is indistinguishable from one that has stopped tumbling entirely — which would be the best possible news — or the opposite one spinning. A single observer can measure only the component of angular velocity projected onto the plane perpendicular to its line of sight. The component along the line of sight is invisible. This is not an instrument limitation. It is a geometric one.

Move the observer ninety degrees around the target and the spin becomes immediately visible — the body of the satellite rolling through its cycle. The satellite has not changed. The understanding has.

Three inspectors at 120-degree separations eliminate the degeneracy. Whatever axis the satellite is rotating around, at least two of the three observers will have a line of sight with a substantial perpendicular component. The spin vector — magnitude, axis, and phase — becomes reconstructible in minutes rather than over the full NMC ellipse. And that reconstruction is not merely geometric satisfaction. The docking window — the brief interval when a chosen attachment point presents itself at near-zero relative angular velocity — can be calculated only when the full spin state is known. Without it, you are waiting for a moment you cannot predict. Which is, in miniature, the
condition the satellite's designers never planned for either.

---

## 3. Structural Geometry — The Satellite as It Actually Exists

The drawings that defined a satellite at launch are the closest thing it ever has to a birth certificate. They describe hinge lines and panel spans, antenna booms and radiator faces, all in clean orthographic views. They do not describe what that satellite becomes after fifteen years in geostationary orbit.

GEO is quiet in one sense — no drag, no atmosphere — but twice a year, near each equinox, the spacecraft passes through Earth's shadow. Across fifteen years the slow accumulation of those eclipse seasons, each one a cycle of deep cold and fierce heat, works on every joint and hinge and bonded surface. Joints expand and contract. Deployable booms flex. Lubricants creep and outgas. Over thousands of cycles the differences between the as-designed geometry and the as-flown geometry accumulate quietly: a solar panel with a measurable twist, an antenna mast carrying on, slightly bent, after a micrometeoroid impact it survived but did not escape. To an engineer reading the launch drawings, small deviations. To a servicer looking for a place to
grab, the difference between a clean force path and one that pries on a weakened hinge.

The problem for a single inspection vehicle is that it never quite sees the satellite whole. It sees one face at a time, under one illumination condition at a time, building up an internal model the way a tourist assembles the memory of a building from a sequence of street views. Occlusion becomes fate. A failed hinge, a warped panel, or a bent antenna boom on the anti-Earth face remains invisible to a servicer that approaches from the Earth-facing side and never spends the propellant to maneuver around the back. The attachment point that looks nominal in the drawings and benign from the approach vector may be the most damaged part of the spacecraft.

A swarm breaks that occlusion by being in more than one place at once. Inspectors distributed around the target image all faces within the same orbital segment, under the same lighting conditions. One reads the Earth-facing bus, another the anti-Earth side, others the north and south faces and the full span of the solar arrays. Together they produce not a visual record but a diagnosis — which structural members are still taking load cleanly, which hinges show evidence of creep, which regions of the bus carry impact scars. Attachment point selection becomes a question answered with evidence rather than habit.

---

## 4. Thermal Mapping — Reading the Power State

Geometry tells you what the satellite has become physically. Its thermal signature tells you how it is living now. Power does not disappear; it turns into heat somewhere. Batteries that are being cycled hard run warm. Thruster valves leak a little energy into the plumbing even when they are notionally closed. A solar wing with a string of degraded cells runs cooler than its twin. Infrared sensors do not see "health" directly, but they see the map of
where power is generated, routed, and lost.

A single inspector can, in principle, build that map by flying its ellipse and stitching together images over time. In practice, the satellite is rotating, the orbit is carrying everything through shadow and sunlight, and the thermal environment is changing as quickly as the view. A hot patch on the sunlit face may be a genuine internal load — a battery pack, a reaction wheel cluster — or simply a piece of structure that has just emerged from eclipse and is still warming up. From one vantage point, assembled sequentially, those possibilities blur. You are inferring a living power state from a series of snapshots taken under different weather. The map is not merely incomplete. It is capable of being wrong in ways that look exactly like being right.

A swarm takes the same picture all at once. Inspectors placed around the satellite record its infrared signature from multiple sides within the same short interval, under the same illumination. One sees the battery deck and bus, another the thruster cluster, others the backs of the solar wings and the radiator fields. When those observations are fused, they produce a diagnostic — which cell strings are underperforming, whether any thruster shows residual warmth that suggests trapped propellant, whether the batteries are running hot in a way that implies limited remaining life.

The thermal map is how you find out before you commit. What you find determines whether you can lean on whatever attitude control authority the satellite has left, or whether you must assume from the moment of first contact that you are on your own.

---

## 5. Collision Avoidance and the Threat of the Unexpected

All of that careful reading assumes the satellite holds still long enough to be read.

The most dangerous assumption in orbital servicing is that the target will behave like a target. An end-of-life satellite is not a cooperative rendezvous partner. It may carry residual propellant in lines that have been closed for a decade but are not empty. A thruster valve that has been thermally cycled ten thousand times may open unexpectedly — not catastrophically, not a full burn, but enough to impart a sudden translation or rotation that an approaching vehicle did not plan for. The satellite does not intend this. It simply has not finished acting on the physics it accumulated over a long life.

For a single NMC vehicle, unexpected target motion is a mission-level threat. It must retreat immediately along a safe trajectory. While it retreats, it loses the observation it came to make. The inspection ellipse is broken. The carefully assembled model of the target's state must be set aside, possibly restarted. Time, propellant, and mission confidence all erode together.

The swarm responds differently, because it is already distributed across a volume of space. A sudden target motion that threatens one inspector's corridor does not threaten all of them simultaneously. Threatened units maneuver away while the others hold position and continue observing. The  inspection does not pause. The model continues to update. The swarm does not lose its understanding of the target simply because one of its members had to step back.

The single NMC vehicle stays safe by staying on its ellipse — safe by geometry, safe by design. The swarm stays safe by being in enough places at once that no single surprise can take everything away simultaneously. The risks are different in kind, not just in degree.

---

## 6. The Information Architecture — How the Swarm Thinks Together

A swarm is not just many sensors. It is a way of thinking about the target that no single vehicle can manage.

Each inspector has its own view — its own camera angles, its own range measurements, its own estimate of where it sits in the rotating frame. The completeness comes from how those views are combined. The combination is sensor fusion: simultaneous observations folded into a single estimate of the target's position, attitude, tumble, and surface condition. But the swarm also has a second navigation problem — each unit must know not only where the target is, but where its fellow inspectors are. The network that forms around the satellite is not hierarchical. Each unit carries its own filter, a running estimate of the world revised every time a neighbor shares a new measurement. It is less like flying a formation and more like scholars annotating the same manuscript. Each has read a different passage. Through comparison they arrive at a shared understanding of what the whole work says.

The autonomy requirement is not a flourish. At GEO, the round-trip light time to the ground is fast enough for routine commands but too slow for the real-time adjustment that proximity operations demand. By the time a control center has seen, understood, and responded to a change in the target's behavior, the docking window it cares about will have opened and closed. The swarm has to arrive at its own consensus about the target in situ. This is in contrast to target comprehension in LEO, which is typically largely informed from ground station tracking. 

If one inspector's sensor fails, the others reweight their estimates. The shared
picture becomes a little noisier, but understanding degrades gracefully rather than failing all at once. That is the promise, at least. The same autonomy that makes the swarm capable also concentrates risk inside it: inter-unit ranging that drifts, consensus that locks onto the wrong state, a collision between two inspectors that were meant to stay out of each other's way. A single vehicle on an NMC carries its risk in one place, where everyone can see it. A swarm spreads the risk out and hides some of it in the network. In an environment where the consequences of a mistake propagate outward, that trade — between more ways to know and more ways to be wrong — is the one that has to be made consciously.

---

## 7. From Inspection to Contact — The Coordinated Approach

At some point the inspecting ends and someone has to move.

In the single-vehicle model, the same spacecraft that performs the circumnavigation must eventually leave the safety of that ellipse and commit to a terminal approach. That moment is the most exposed in the mission. The inspector becomes the docker, carrying all the uncertainty it failed to resolve during the inspection phase into the moment of contact.

A swarm changes the sequence. The first unit leaves the inspection geometry and approaches the chosen attachment point while the others remain off the target, still watching. They are no longer merely inspectors. They become witnesses to the docking itself, updating the shared state estimate as the first vehicle closes. If the target's motion differs slightly from what the model predicted — or if the first attachment changes the dynamics of the satellite by even a small amount — the remaining units do not proceed on stale assumptions. They revise their approach plans in real time.

Once the first inspector is attached, and certainly once two are attached at separated points, the target is no longer simply a tumbling object to be captured. It is the beginning of a controlled system. Differential thrust can begin active detumbling before the remaining inspectors approach. By the time the final units make contact, they are docking not with an uncontrolled satellite but with a target already being steadied by those that arrived first.

Compare this with the Northrop Grumman MEV model: MEV-1 docked successfully with Intelsat 901 in February 2020, one approach, no second chance. It succeeded because its target was cooperative — tumble rate known, geometry well-documented from years of ground observation, propellant state understood. The question the swarm architecture asks is not whether single-vehicle docking can work under favorable conditions. It is what happens when the conditions are not favorable — when the tumble rate is uncertain, the geometry degraded, the thermal state unknown. That is not a hypothetical. It describes the normal condition of an end-of-life satellite that has been silent for years.

---

## 8. Implications for Mission Design and Regulation

The inspection phase has always been treated as a prelude — necessary, careful, but subordinate to the main event. What the swarm architecture makes visible is that this ordering has consequences. A servicer that docks with incomplete information is not performing a servicing operation. It is performing an experiment, with a very expensive piece of national infrastructure as the subject.

Consider the liability geometry. If a servicer attaches and a solar panel fails — a hinge already compromised, invisible from a single approach vector, cracked by fifteen years of thermal cycling — whose fault is the failure? The satellite operator will argue the servicer caused it. The servicer will argue the fault was pre-existing.
Without a complete pre-docking inspection record, the question may never be resolved. With one, it can be. The swarm's full characterization of the satellite before contact is not only a technical asset. It is a legal one.

Regulatory frameworks are beginning to catch up. As ESA, the FCC, and the ITU work toward standards for in-orbit servicing, questions of due diligence before contact will arise. Swarm inspection protocols may become what preflight checklists became in aviation — not a competitive advantage but a *minimum standard of care.*

The commercial case extends further. The complete characterization a swarm produces — thermal, structural, dynamic, all timestamped to the satellite's actual state — has independent value for insurance underwriters pricing end-of-life risk, for operators planning final maneuvers, for spectrum managers deciding whether a silent satellite poses a debris threat. The inspection is the product. A decade of swarm inspections across the GEO belt would constitute an unprecedented archive of how satellites actually age — what fails first, what holds longer than expected, what the drawings never predicted. That archive informs the design of every spacecraft that follows.

---

## Conclusion

There is a GEO satellite, launched in the early 2000s, that has been silent for
several years. Its operator knows roughly where it is. They do not know how fast it is tumbling, whether its solar wings are still symmetric, whether its apogee motor has vented or holds pressure. They know what it was. They do not know what it has become.

Somewhere in the engineering community, someone is planning a mission to find out. They will arrive at a safe distance and begin to look. What they learn in the first hours of inspection — before anyone touches anything — will determine everything that follows. 

They will either know what they are docking with, or they will not. The inspection is not the prelude. For that satellite, on that day, it will be the whole story.

---

*Note for development: This essay stands alone but connects naturally to "Small Forces, Patiently Applied" — the limpet swarm essay. Together they form a pair: the first argues for the swarm architecture on economic and resilience grounds; this one argues for it on epistemological grounds — what you can know before you act.*

*Image prompt for LinkedIn: A formation of five small identical spacecraft arranged in a loose ellipse around a large gold-foil GEO satellite, each unit emitting a narrow beam of sensor light toward the satellite's surface. The arrangement has the quality of scholars around a manuscript, or surgeons around a patient. Deep space background, Earth visible at distance. Clean, almost architectural composition.*
