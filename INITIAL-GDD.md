AI-use disclosure: AI helped organize and translate this draft from the student's selected cooperative questioning concept, develop the case, and inspect evidence dependencies. The student retains responsibility for the design decisions, claims, and final submission.

# Between Testimonies

## Initial Game Design Document

Version: G1 v0.1-en, November 15, 2026. Author and accountable owner: Yibo Wang (yw4626), Executive Producer and Creative Director. Status: concept and design proposal. There is no playable build, live-model experiment, or human playtest result for this project yet. This is an individual course project for a two-player game.

Between Testimonies is a small cooperative mystery. Two investigators examine space and time, question AI suspects about the same event, and jointly challenge testimony to build an evidence chain identifying the murderer. The first commitment requested at G1 is a complete cooperative questioning experiment, before expanding to a larger case.

Status labels: **[Selected direction]** identifies the student's chosen concept. **[Design proposal]** identifies rules proposed here but not implemented or validated. **[Open OQ-xx]** identifies unresolved decisions. **[To validate]** identifies hypotheses requiring implementation or observation.

Companion documents: [Initial Configuration Document](INITIAL-CONFIGURATION.md) and [Initial Project Plan](INITIAL-PROJECT-PLAN.md). This English edition preserves the v0.1 design and uses the terminology of the English G1 deck. Submission language is now English; the language of the eventual game remains open. The Chinese source documents are retained separately.

## 1 Game concept and player experience

**The X [Selected direction]:** Two investigators with different information cooperate to question AI suspects, test their accounts against time and place, and identify a murderer through a shared chain of evidence.

Target players **[Design proposal]** are two people who enjoy discussion, cooperative puzzles, and short mysteries, and are comfortable with text interaction. The target session length is 15–20 minutes. No professional investigative knowledge is required. The first playtest asks whether players understand the information split, rather than assuming the concept appeals to every mystery player.

The intended experience is that questions matter, a partner's discovery changes the next question, and both players can explain why the evidence supports their conclusion. Observable behavior includes actively sharing discoveries, using a partner's clue in a follow-up question, and jointly excluding alternative explanations.

The three design pillars are:

1. **Cooperation changes questions.** One player's discovery changes the other's next investigation step, rather than merely supplying an answer at the end.
2. **Free expression with stable facts.** Questions can be phrased in different ways, while world truth, character knowledge, and recorded commitments remain consistent.
3. **Evidence-based closure.** Naming the correct suspect, detecting a lie, or finding a motive does not independently win the game.

## 2 Concept selection and references

Three directions were compared during this project's brainstorming. They are not claimed as completed prototypes, and this comparison does not replace the November 9 classroom pitch and feedback, which have not yet been supplied.

| Concept explored | Core experience and AI role | Current decision |
|---|---|---|
| Two-player blackjack with an AI referee | Card decisions, with AI potentially interpreting rules or disputes expressed in natural language | Standard scoring and outcomes can be coded. A clear hypothesis for the additional player value of AI has not yet been established, so this is not the current priority. |
| Rule loopholes with an AI referee | Players propose actions that satisfy constraints, and AI interprets their proposals against the rules | Free-form solutions are appealing, but physical feasibility and fair adjudication are harder to bound. |
| Cooperative questioning | Players use different information to question AI suspects and test accounts of the same event | Selected by the student. A fixed case bounds character knowledge and supports a fair scripted comparison. The value of cooperation and free questioning still needs testing. |

The case, characters, and mechanics are proposals developed through student–AI ideation. The framework follows the [G1 assignment](https://courseworks2.columbia.edu/courses/258228/discussion_topics/1701307), [GDF reader Sections 5.1–5.2](https://github.com/columbia-university-ai-games/game-dev-f26/blob/main/docs/gdf.md), and [course syllabus](https://courseworks2.columbia.edu/courses/258228/assignments/syllabus), checked on November 15, 2026.

**Reference update for the G1 v0.2 presentation:** two official descriptions were reviewed on November 15, 2026. These are mechanic-level comparisons added during pitch revision, not a claim of personal playthroughs or the historical origin of the concept.

| Reference and source | Specific mechanism | Proposed adaptation |
|---|---|---|
| Steel Crate Games, [Keep Talking and Nobody Explodes: How to Play Remotely](https://keeptalkinggame.com/how-to-play-remotely/) | The defuser sees the bomb while experts use the manual, requiring communication across separate information. | Keep complementary private information, but split space and time investigation and let both players question suspects. |
| Sam Barlow, [Her Story: About / How does it work?](https://www.herstorygame.com/about/) | Typed search terms retrieve matching interview clips. | Keep player-directed testimony discovery, but replace archived retrieval with bounded questioning and persistent commitments. |

Reuse scope and terms: the documents paraphrase mechanisms and attribute their creators. No game images, footage, dialogue, manual text, assets, or source code are incorporated, and no third-party reuse license is asserted. Any later reuse requires separate permission/terms verification under **OQ-10**. The presentation cover is AI-generated decorative concept art, not gameplay or a precise sightline diagram; the prompt and provenance are retained with the presentation. The prototype is intended to use original diagrams and system fonts. The midterm project, Duskvault, supplies development experience only; no transfer of its code or experimental results is claimed.

## 3 Core loop and mechanics

**Act:** investigate and ask a question. **Response:** receive testimony or feedback from a scene operation. **Interpret:** assess whether the information is sufficient and consistent. **Next action:** share a finding and refine the next question. Joint challenges and evidence-based closure complete the loop.

### 3.1 Player actions

- **A, the scene investigator,** inspects room objects, asks suspects to identify positions, and produces sightline reconstructions.
- **B, the records investigator,** checks device event logs, asks about event order, and establishes time intervals.
- Both players can select suspects, enter questions, attach acquired evidence they choose to present, mark exact statements, request clarification, initiate a joint challenge, and submit an explanation.
- Testimony cards link back to the source dialogue. Shared cards retain their discoverer, event ID, and version. Private clues require an explicit sharing action.
- The prototype uses text input, buttons, and keyboard-accessible card connections. Evidence states use text and shapes as well as color. Text can be enlarged, and there is no forced countdown.

### 3.2 Testimony and facts

Testimony records what a character said; it is not automatically a world fact. Each important statement has a `speaker`, `event_id`, `claim_id`, and `revision`. Corrections preserve earlier versions. Players must examine the same event rather than joining statements from separate visits into a false contradiction.

NPCs cannot see private clues that players have not presented or the entire shared board. Repeated questions do not reset memory. Equivalent wording and different question orders should reach the same relevant facts without requiring secret keywords.

### 3.3 Joint challenges and progression

Players select a specific statement about one event, attach spatial and temporal evidence, and explain the conflict. The system checks the evidence and its connection to the statement. A valid joint challenge triggers an explicit correction of that statement. A suspect may admit entering the scene while continuing to deny murder.

This is a visible game rule: a valid, sufficiently supported challenge must produce clarification instead of endless repetition of a refuted account. **[To validate]** Whether this feels like credible questioning rather than collecting two cards to force an admission is a central risk.

## 4 First case: The Answer Through the Door

This section is a designer specification containing spoilers. Player clients and NPC contexts receive only their authorized subsets. Lin in the deck refers to **Lin Zhou**, the butler. The victim is **Shen Heng**; the other suspects are **Xu Lan**, a restorer, and **Shen Yue**, the victim's nephew.

### 4.1 True timeline

| Time or condition | World fact | How players can obtain it |
|---|---|---|
| Case boundaries | Shen Heng was attacked in the study and died there. There are three suspects, no accomplice, remote device, delayed fatal mechanism, or hidden passage. | The case briefing establishes these limits. They are rules of this fictional case, not assumptions about real investigations. |
| 21:00 | All three suspects had legitimately entered the study and seen Shen Heng. | Public background. Knowledge of the layout alone cannot identify the murderer. |
| 21:05–21:09 | Xu Lan inspected a picture frame, secretly took a decorative piece, and left. | Questioning and physical traces reveal this separate secret. |
| 21:13 | Lin Zhou entered the study. | An anonymous counter records one visitor entering, without identifying that visitor. |
| 21:14:00–21:14:10 | A ten-second test signal played. Shen Heng was still writing at his desk and briefly looked up in response to Lin, who was inside. | B has the timed signal record. Lin's commitments about the action and its timing must be elicited through questioning. |
| Around 21:15 | Lin argued with Shen Heng over accounts and attacked him. | The complete truth stays in the server-side case data. |
| 21:16 | Shen Heng was dead. | A reliable case examination card establishes a death window of 21:14–21:16. Its narrative justification still needs refinement; players are not expected to use medical knowledge. |
| 21:17 | Lin left. | The counter establishes that the victim and the same visitor were present throughout 21:13–21:17, with no other entry or exit. |
| 21:18 | Shen Yue entered, found the body, took a letter concerning himself, and left. | A separate anonymous visit record and questioning reveal this event after the death window. |
| 21:20 | The body was formally discovered. | Public starting information. |
| Fixed geometry | A narrow window is set into the closed door. A fixed screen blocks the chair and the seated person's upper body. The desk corner is visible from the corridor, but writing and nodding are not. | A reconstructs the sightline. Every permitted observation position must be checked in implementation. |

**“After the signal” is not a sufficiently bounded time claim.** A valid commitment must establish that the nod happened while the ten-second signal was still playing; otherwise a later observation remains possible. The spatial check must also establish the closed door, the claimed position, and the specific visible action.

### 4.2 Two-player information table

| Task | A's contribution | B's contribution | Why one side is insufficient |
|---|---|---|---|
| Specify the observation | Ask what action Lin saw, have him identify his position outside, and establish the door's state. | Obtain the statement's event ID. | Without timing, the observation may refer to an earlier legitimate visit. |
| Bound the same observation in time | Share the now-specific observation event. | Ask how the signal's start and end relate to the nod, bounding it to 21:14:00–21:14:10. | Without a spatial check, Lin may still claim to have observed from outside. |
| Test the observation | Produce a sightline record matching the position, action, and door state. | Verify that it refers to the same event and unchanged statement version. | Refuting one statement does not itself establish an actual position inside. |
| Make a joint challenge | Present the spatial evidence and explain why the action was not visible. | Present the timing commitment, excluding an earlier visit. | An explicit location correction is required; an ambiguous retreat is not an admission. |
| Close the case | Supply the corrected testimony and its sources. | Connect identity to the sole visitor's continuous occupancy. | Both players explain the evidence chain rather than only choosing a name. |

### 4.3 NPC specification table

| NPC | Private knowledge and secret | Initial strategy | Effective follow-ups and correction |
|---|---|---|---|
| Lin Zhou, butler and murderer | Knows that he was inside during 21:13–21:17 and knows the attack. Does not know the other suspects' private actions. | “I checked on him again later, then went to the kitchen.” Keeps location vague rather than volunteering the entire cover story. | Asked how he checked, claims to have seen writing and a nod. Asked where, claims the narrow window outside the closed door. Asked when, places the nod during the test signal. After a valid challenge using both evidence types, explicitly corrects the location and admits entering during that interval, while potentially denying the attack. |
| Xu Lan, restorer and innocent suspect | Knows she took the frame decoration and that Shen Heng was alive when she left. | Minimizes the inspection to avoid admitting the theft. | Physical traces and specific questions about her actions lead her to admit taking the piece. She cannot supply observations after leaving or reveal the murderer for the players. |
| Shen Yue, nephew and innocent suspect | Knows he took a letter after finding the body and did not promptly raise the alarm. | Emphasizes fear and a quick departure. | Questions about his actions during the visit and the missing letter lead him to admit taking it. He does not know the attack. His motive and dishonesty do not establish murder. |

Versioned state rules constrain commitments, permitted evasion, and correction conditions. The model cannot invent visitors, locations, evidence, or events that change the truth. The innocent suspects test whether players confuse lying with murder; their branches are not mandatory collection tasks.

### 4.4 Evidence dependencies and closure

| ID | Required conclusion | Evidence and acquisition | Insufficient substitutes |
|---|---|---|---|
| C1 | The same visitor's continuous presence covers the death window. | B's death window, anonymous counter, and sole-entry information. | Identity is still missing. |
| C2 | Lin places this observation within the ten-second signal. | B's precise follow-up about the same event plus the signal record. | “Later,” “afterward,” or the time of another event. |
| C3 | The claimed action could not be observed from the indicated outside position. | A obtains commitments about the action, position, and closed door, then reconstructs the sightline. | Suspecting poor visibility or checking a different position. |
| C4 | Lin explicitly corrects his location and admits entering during that interval. | Bind C2 and C3 to the same event, complete the joint challenge, and retain the correction. | A lie, silence, nervousness, or “perhaps I remembered incorrectly.” |
| C5 | Lin is the sole visitor during the death window. | C1 plus C4 and the continuous occupancy record with no additional entry or exit. | Presence during an earlier visit or motive alone. |
| Success | A complete identification and causal explanation. | Both players confirm the sources and connections for C1–C5. | Guessing the name does not pass; repeated guesses do not reveal whether a name is correct. |

C3 only refutes a statement; it does not logically establish a true location from a false observation. C4 is an explicit corrected statement produced by this case's challenge rule. The chain depends on the authored evidence and correction rules, whose credibility to players remains untested. Static materials, spatial information alone, or temporal information alone should not produce C4. Raw NPC prose must not automatically become case truth.

## 5 Dynamics, aesthetics, outcomes, and edge cases

**Mechanics:** complementary investigation, free questioning, versioned testimony, evidence presentation, joint challenges, and structured closure. **Dynamics:** information exchange, hypothesis formation and revision, coordinated follow-ups, and separating unrelated secrets from decisive contradictions. **Intended aesthetics:** shared discovery, agency in questioning, and satisfaction from an explainable conclusion.

Progress is represented by discoveries and testimony states, not affinity scores or a hidden persuasion score that controls truth. The initial design has no leaderboard or speed score. A correct evidence chain succeeds. An incorrect chain identifies a missing type of reasoning without revealing the culprit. Players may revise, pause, or leave. Reaching the service budget switches to a labeled scripted mode rather than forcing a loss.

**[Design proposal]** An early accusation does not unlock C4. Repeated questions preserve commitments. Pretending to have evidence does not create a card. Concurrent questions to one NPC are serialized by session revision. Either player may withdraw closure confirmation during disagreement. Disconnection pauses play and restores committed state. Story time does not advance with typing speed.

Balance work first addresses question clarity, information load, and evasion rather than adding clues. A key progression question may receive at most one bounded deflection; a second explicit follow-up should obtain a permitted substantive statement. This value is provisional. The proposed cap is 24 model turns shared by both players; the fallback remains able to finish the case.

## 6 AI hypothesis and playtests

**H1 [To validate]:** Compared with fixed question menus under the same case and character states, AI constrained by knowledge boundaries can interpret player-formulated follow-ups and multi-evidence challenges, supporting more questions prompted by a partner's discovery while keeping facts and testimony consistent.

The expected loss when replacing AI with scripts is the freedom to refine questions in the player's own wording and follow up on a particular statement. The scripted case must remain solvable. Weakening its evidence or rules would not be a fair comparison. If AI only paraphrases fixed lines without improving investigation, H1 is not supported.

Observe partner-triggered effective follow-ups, each player's contribution, correct binding of statements to the same event, misunderstandings of important facts, hints and fallback use, completion time, and the final explanation. Self-reported experience supplements these observations.

Start with one pair of players in a formative playtest, checking whether one directs the other to click. For the AI/menu comparison, prefer separate first-time pairs for the two conditions to avoid learning the same solution. If recruitment is insufficient, report formative observations only, without claiming AI superiority. Freeze the test questions, participant plan, and formal thresholds before collecting evidence; see the companion documents.

## 7 Scope and open questions

Retain one complete short case, two complementary roles, three suspects, evidence provenance and versions, a scripted comparison, server-side state, and deterministic fallback. The first experiment implements only Lin's joint-questioning chain. Cut voice, animation, additional cases, and decorative branches first, then shorten the innocent suspects' branches. Do not replace cooperation with an automatic answer reveal.

| ID | Unresolved decision or validation | Provisional approach and decision point |
|---|---|---|
| OQ-01 | Is the location correction credible, or too dependent on a forced admission? | Paper questioning and alternative-explanation review before G2; revise the case if necessary. |
| OQ-02 | Do both people actively reason? | Observe paired play. Complementary information alone does not prove two people are indispensable. |
| OQ-03 | Narrative source of the death window, sightline geometry, and case title. | Use an explicit examination card and a 2D sightline diagram provisionally. Freeze spatial and temporal facts before implementation; the title may change. |
| OQ-04 | Networked devices or local role handoff. | Validate locally first; select the smallest delivery approach by November 20. Networking is not implemented. |
| OQ-05 | Model, exact version, and deployment call path. | Candidate configuration in the companion document; confirm and test before the November 23 checkpoint. |
| OQ-06 | Game dialogue language. | English slides, script, and written submission documents are now requested and prepared. English-only or bilingual gameplay remains undecided. |
| OQ-07 | Available development hours and external players. | Approximately 25 hours to G2 are estimated, not a confirmed student commitment. Freeze the small prototype first. |
| OQ-08 | Do turn limits, latency, and cost targets support the experience? | Treat them as design targets and revise using actual tokens, timing, and player observations. |
| OQ-09 | November 9 pitch and feedback. | Not supplied. Add the actual material or explain the new direction; do not invent feedback or claim it has been addressed. |
| OQ-10 | Reference and asset attribution as the project develops. | Two official mechanic descriptions and adaptation/reuse boundaries are now documented for the v0.2 pitch. Future asset/code reuse and its terms remain open. |
| OQ-11 | Formal repository, deployment URL, and access permissions. | These English documents are local drafts; teacher-accessible repository links are not established. Submission language is now English. |
| OQ-12 | Conflicting reply dates. | G1 prose and the syllabus state November 19; the Course Summary row shows November 18. Plan internally for the earlier date and verify the platform. |

## 8 Decision requested at G1

Approve a prototype containing one suspect, two investigation operations, one joint challenge, and a complete evidence chain. Use the matching scripted version and external paired observation to test cooperation and free questioning before expanding to the full three-suspect case.

Proposed Hold conditions: the case relies on undisclosed facts; time and location do not support the sole-visitor connection; success requires an accidental model error; players can complete the reasoning without exchanging information; or deployment and budget are infeasible without an executable scope reduction. The instructor makes the gate decision; this document does not claim approval.
