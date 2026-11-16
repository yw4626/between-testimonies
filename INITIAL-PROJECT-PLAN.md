AI-use disclosure: AI assisted with organizing and translating tasks, risks, and budget assumptions from the student's selected concept and course schedule. Hours, parameters, and execution commitments remain subject to student review. No implementation or playtest records have been fabricated.

# Between Testimonies — Initial Project Plan

Version: G1 v0.1-en, November 15, 2026. Student owner: Yibo Wang (yw4626), Executive Producer / Creative Director. Gate approver: instructor. Status: initial G1 plan; no gate approval or Asana tasks established.

Related documents: [Initial GDD](INITIAL-GDD.md) and [Initial Configuration Document](INITIAL-CONFIGURATION.md). The three documents, English presentation, recording script, and edited presentation video are prepared. The final recording is 4 minutes 57 seconds at the original speaking speed. Today's G1 still requires instructor-accessible submission links and the discussion post.

## 1 The next commitment requested at G1

Request approval for a small experiment: one AI suspect, two complementary investigation operations, explicit time/location commitments, one joint challenge, and a complete evidence chain. Include a scripted version with the same case and rules. First test whether each player's discoveries change their partner's questions.

G2 success cannot be defined solely as “the AI answers,” “the model produces valid output,” or “the players guess the murderer.” It requires a playable core loop, reproducible factual boundaries, observations of external players, and a clear next scope. G3 separately judges whether remaining resources support production, even though the reviews occur together.

## 2 Official schedule and internal checkpoints

Sources: [G1 discussion](https://courseworks2.columbia.edu/courses/258228/discussion_topics/1701307) and [course syllabus](https://courseworks2.columbia.edu/courses/258228/assignments/syllabus), checked November 15, 2026. All dates are in 2026, interpreted in New York/course time. An unspecified time is not assumed to be 11:59 p.m.

| Date | Status | Requirement or plan |
|---|---|---|
| November 15, 11:59 p.m. | Official G1 submission | Discussion post with short deck, 3–5-minute video, Initial GDD, Configuration, and Project Plan; include the six-dimension Risk Profile and initial register in this plan. |
| November 16 | Official G1 class review | Selected students present live; others are reviewed through their recordings. |
| By November 17 | Official feedback arrangement | Instructor posts Approve / Hold on G1; student records the decision and revision tasks. |
| November 18 | Internal early target | Complete two specific Braintrust replies; see the platform date discrepancy below. |
| November 19, 11:59 p.m. | Reply deadline in G1 prose | Reply to two classmates, prioritizing posts with fewer than two replies. |
| November 23 | Official working checkpoint | Demonstrate a deployed model call, isolated session state, and forced-timeout fallback, live or through recorded evidence. |
| November 28 | Official G2/G3 recording | First-playable recording; exact submission time awaits the corresponding assignment page. |
| November 30 | Official combined G2/G3 review | Initial Playtest Log, updated GDD/Configuration, updated risks, and scope-lock plan; complete three Braintrust responses before review. |
| December 2 | Official Alpha | Accepted features implemented and integrated; known defects listed. |
| December 4 | Official Beta | Content complete and locked; focus on fixes, verification, and balancing. |
| December 5 | Official Gold recording | Complete post-Alpha external release playtesting, fix verification, and bounded model evaluation before recording; exact time awaits the assignment. |
| December 7 | Official G4 review | Gold, Final GDD/Configuration, harness, Update Playtest Log, and Braintrust. |
| December 12 | Official draft sharing | Draft AAR / showcase evidence. |
| December 14 | Official G5 closeout | Final game, AAR, Final Playtest Log, and archive; no extra gate recording. |
| December 17–23 | Official Finals window | Engineering & Design Retrospective, 8–10-minute walkthrough, and live presentation in the assigned slot; slot TBD. |

**Date discrepancy, OQ-12:** G1 prose and the syllabus state November 19 for the two replies, while the automatic Course Summary below the syllabus lists November 18. This conflict remains unresolved. Use November 18 internally and verify the submission interface. The November 15 first-post deadline is consistent.

## 3 Today's submission checklist

| Item | Current status | Next action |
|---|---|---|
| Initial GDD | English v0.1-en drafted; Chinese original retained. | Student reviews the concept, correction rule, and open questions. |
| Initial Configuration | English v0.1-en drafted; Chinese original retained. | Review configuration assumptions; do not claim code or tests exist. |
| Initial plan, Risk Profile, and Risk Register | English draft in this file. | Student confirms available time, scope cuts, and next commitment. |
| References and attribution | Two official game-mechanic descriptions, adaptations, and reuse scope documented in the GDD for the v0.2 pitch. | Review the comparisons; verify terms before any future third-party asset/code reuse. No personal playthrough claimed. |
| November 9 initial pitch and feedback | Not supplied. | Add actual material and explain the change in direction; do not fabricate class records. |
| Short deck | English v0.2 presentation prepared: nine visible slides and one hidden reference appendix, with a noir visual style. | Review and export/share it with working access permissions. |
| Recording script | Simple-English script prepared for the nine visible slides; speaker notes updated. | Retain as supporting material. The student's recording is complete. |
| 3–5-minute presentation video | Recorded and edited: 4:57, 2560 × 1440, original speaking speed; repeated takes and long pauses removed. | Upload the final MP4 and verify instructor access to its link. This is a concept presentation, not playable-game evidence. |
| Accessible repository/material links | Formal repository links not established. | Choose the repository/branch, upload, and verify instructor access. Local file links are not CourseWorks submission links. |
| G1 discussion post | Not submitted. | Post under the working title with video, deck, GDD, Configuration, and Project Plan links. |

G1 does not require completing the full game, implementing every production-agent role, or migrating to Asana today. Clearly marked open questions are appropriate in the initial drafts. Accessible material links and the actual submission remain to be completed.

## 4 Tasks and acceptance criteria through G2

Yibo Wang is the student owner of every task. Listed roles are proposed responsibilities. Dates are internal targets dependent on the G1 decision and actual availability; they are not confirmed commitments of student hours.

| ID / target date | Task and roles | Dependencies | Estimate | Observable completion criteria |
|---|---|---|---:|---|
| T01 — Nov 16–17 | G1 revisions and paper evidence chain; Design + Narrative. | Instructor feedback. | 2h | Fix case truth; list alternative explanations; establish the ten-second upper bound; no one-sided path yields complete C4; distinguish corrected testimony from merely disproving a claimed sightline. |
| T02 — Nov 17 | Formal repository and initial Asana tasks; Producer + Tech. | T01 and student-selected location. | 1h | Accessible repository, task dependencies, version convention, and recorded G1 decision; preserve the midterm submission. |
| T03 — Nov 18–19 | Authoritative state and complete scripted path; Tech + QA. | T01/T02. | 4h | Static, A-only, and B-only paths cannot close the case; A+B can. Reject event mismatches, retain correction history, and prevent wrong guesses from revealing the answer. |
| T04 — Nov 19–20 | Two views, sharing, and challenge interface; UX + Tech. | T03. | 3h | Role permissions, active sharing, evidence provenance, and joint confirmation work; choose local handoff or minimal separate-device interaction. |
| T05 — Nov 20–21 | NPC extension, context, and contract; Tech + Narrative. | T03/T04 and model decision. | 4h | Paraphrases map to allowed actions; commitments persist; unshared clues stay private; artifact manifest and named-failure tests run. |
| T06 — Nov 21–23 | Deployment, isolation, forced timeout, and cost logging; Tech + QA. | T05 and provider credentials. | 3h | Demonstrate a real deployed call; two sessions remain isolated; forced timeout switches to a playable scripted path within the 12-second total deadline; retain versions and logs. |
| T07 — Nov 24–25 | Small live-model suite and boundary regression; QA + BI. | T06 and explicit budget. | 2h | Freeze cases and preserve all failures, model/configuration versions, tokens, costs, and latency; fixtures are not live runs. |
| T08 — Nov 25–26 | External paired playtest and records; BI + Design. | T04/T06. | 2h | At least one pair experiences the cooperative loop; record consent, anonymous identities, build, actual observations, and hints; meet the course minimum of at least one external player. |
| T09 — Nov 26–27 | Evidence-led revision and verification; Design + Tech + QA. | T07/T08. | 2h | Verify at least one change supported by findings; if cooperation or factual boundaries fail, reduce scope and record a Hold recommendation. |
| T10 — Nov 27–28 | Updated documents, Playtest Log, recording, and G3 scope recommendation; Producer + Release. | T09. | 2h | Record the actual build; align all three documents with it; move the plan into Asana; state separate G2 and G3 requests. |

Estimated total through G2: **25 hours**, plus a recommended 5-hour buffer. This excludes today's deck/recording and reading/peer-feedback time. If availability is lower, preserve the complete one-suspect interrogation and shorten the other suspects' branches and visual work. Do not remove cooperation or factual boundaries to meet the schedule. Resolve OQ-07 before accepting a development commitment.

Critical path: coherent case → deterministic scripted loop → two-player operations → model contract → deployment/fallback → human observation → revision and recording. Validate this path before investing in extensive art or multiple cases.

## 5 Scope and playtests after G2

At G3, propose locking one case. Complete the two innocent suspects' limited branches only after the one-suspect experiment succeeds. Integrate accepted features by December 2 and lock content by December 4. Prioritize factual consistency, deployed fallback, two-player readability, and fixes grounded in external feedback.

Schedule distinct course-required encounters: an external core-loop test before G2/G3; a revised-encounter test between G2/G3 and G4 that connects findings to changes; and an external release test after Alpha and before Gold recording, followed by fix verification. Across G2–G4, involve at least two distinct players. For this cooperative game, prefer an external pair over having the developer act as a continuously coaching second player. No participant is currently confirmed.

Knowing the solution creates learning effects. For the initial AI/menu comparison, use different first-time pairs when feasible. If recruitment is insufficient, report formative observations only and disclose order and solution-knowledge limitations. Record each role's contribution, partner-triggered questions, testimony misunderstandings, hints, fallback, duration, and final reasoning; correct guesses alone are insufficient.

After G4, retain the approved Gold tag and document later patches, tests, and instructor approval under course requirements. Before G5, play three assigned classmates' games, collect showcase feedback, and archive the work. The exact Finals slot remains unscheduled in this plan.

## 6 Six-dimension Risk Profile

Ratings are current design judgments, not conclusions from completed tests.

| Dimension | Rating | Current basis | Mitigation and fallback |
|---|---|---|---|
| IP / Concept | High | The core depends on an explicit correction after a joint challenge; its credibility is untested. Mechanic references are now documented, while future asset reuse needs its own terms check. | Paper-test the interrogation; separate rebuttal from positive presence evidence; retain attribution and use original placeholder diagrams. |
| Business / Audience | Medium | The intended audience enjoys paired deduction, but this project has no playtest or recruitment commitments. | Recruit an external pair and observe actual role division/questions; make no market-size or willingness-to-pay claims. |
| Technology | High | Natural-language understanding, knowledge boundaries, isolation, deployment authentication, and costs are untested. | Deterministic facts, structured proposals, same-state fallback, and minimal deployment by Nov 23; restrict expression before relaxing critical facts. |
| Team | Medium | Student-led production; role coverage is planned and hours are unconfirmed. | Small handoffs with acceptance criteria; retain student decisions; demonstrate role work with configurations/logs. |
| Genre / Mechanics | High | Both players may not actively reason; the experience could become one-player leadership, exhaustive questioning, or card collection. | Test static/A-only/B-only paths and observe partner-triggered questions; revise information and challenge explanations. Do not claim mathematical enforcement of two human minds. |
| Timeline | High | Nov 23 deployment and Nov 28 recording are close; the core has no prototype. | Complete one NPC end to end first, limit UI/branches, inspect the critical path daily, and cut decoration, voice, extra cases, and networking complexity if delayed. |

The High ratings share a cause: **the untested joint-interrogation mechanic determines concept viability, response constraints, cooperation, and schedule.** The first investment should therefore be the T01/T03 experiment, rather than treating these risks as independent problems.

## 7 Initial Risk Register

| ID | Risk and trigger | Impact / likelihood | Responsible roles | Mitigation | Fallback and next check |
|---|---|---|---|---|---|
| R01 | By Nov 17, rebutting the lie remains indistinguishable from proving actual location. | High / Medium | Design, Narrative | Specify the source of C4 correction; check time bounds and alternative explanations. | Revise the case or narrow the claim; review after T01 without claiming a proven unique solution. |
| R02 | Model invents unauthorized facts or mixes events. | High / High | Tech, QA | Claim IDs, event IDs, role slices, and revision validation. | Canonical critical lines and menu fallback; recheck after prompt/role changes. |
| R03 | One player only follows the other's clicking instructions. | High / Medium | Design, BI | Complementary operations, active sharing, and records of question origins. | Adjust information and handoff timing; review at T08 and after revision. |
| R04 | Hosted model calls or isolation cannot be demonstrated by Nov 23. | High / Medium | Tech, Release | Validate the smallest deployment route before full art. | Prioritize hosted calls/state; follow course procedures for an alternative platform and report gaps accurately. |
| R05 | Latency or costs exceed §8 targets. | Medium / Medium | Tech, BI | Bound turns, context, and retries; reserve cost. | Label scripted fallback and preserve completion; revise from T06/T07 measurements. |
| R06 | Cross-session or cross-role clue leakage. | High / Medium | Tech, QA | Server identity and allowlisted context. | Disable the faulty model path, preserve logs, fix it, and run two-session tests before release. |
| R07 | No external players or insufficient available hours. | High / Medium | Producer | Resolve OQ-07 and recruit early; prioritize the one-NPC slice. | Reduce scope and report missing work without invented observations; review Nov 20. |
| R08 | Solution knowledge contaminates the AI/scripted comparison. | Medium / High | BI | Different first-time pairs and frozen questions/conditions. | With insufficient samples, report formative observations without causal claims; review before T08. |
| R09 | Accessible links or Nov 9 feedback remain missing. | Medium / Medium | Producer, Release | Check today's list and actual sources; two mechanic references are now documented. | Identify remaining gaps instead of claiming completion; review before G1 submission. |

Student owner for every risk: Yibo Wang. All risks are **Open**. Update them from measurements, instructor feedback, and student decisions; do not automatically mark planned mitigations as completed.

## 8 Latency, cost, and resource assumptions

These figures match the Configuration Document: a 15–20-minute session, at most 24 model turns across both players, at most two attempts per turn, and 48 total attempts. Each attempt allows at most 3,000 input and 240 output tokens. Normal-response P95 targets ≤5 seconds; total turn deadline is 12 seconds.

At hypothetical rates of $1 per million input and $5 per million output tokens, 24 normal calls cost approximately $0.1008; one retry on every turn costs approximately $0.2016. The session design target is ≤$0.25 with a $0.30 reservation cap. These are not provider quotes. Verify actual billing fields, thinking tokens, hosting, and storage after choosing the model, then freeze the configuration. The first live batch has a proposed $5 cap and has not been authorized or executed.

The largest uncertainties are extra clarification turns from free-form questions, context required by NPC state, real end-to-end latency, discussion time, and hosted authentication. Midterm automated-player costs and latency cannot be reused as this project's measurements.

## 9 Decisions and change record

Selected direction: the student chose two-player cooperative interrogation of AI suspects to identify a murderer through testimony contradictions, and requested G1 materials for that direction. The case, parameters, and schedule remain reviewable drafts; unconfirmed choices are tracked in the GDD's OQ table.

G1 Approve request: proceed with the small cooperative-interrogation experiment described by T01–T08 and use its results to decide the full three-suspect scope. Suggested Hold conditions: no explainable evidence chain; static evidence directly identifies the unique culprit; success depends on accidental model errors; the roles do not need to exchange information; or deployment/budget has no feasible route. The instructor makes the final gate decision.

After G1, move the plan into Asana with task IDs, student owner, GDF roles, acceptance criteria, dependencies, deadlines, PR/test links, weekly Progress / Plans / Problems, risks, and gate decisions. GitHub holds code, documents, and release versions; avoid a duplicate backlog. When configuration, case, or scope changes, record the reason, impact, and version so old evidence remains traceable.

**Submission preparation update, November 15, 2026:** the English v0.2 deck, simple-English recording script, and final 4:57 video are prepared. The presentation revision adds official mechanic references, clearer rubric coverage, and artwork without changing case rules, operating budgets, or milestone dates. The recording was assembled from the student's four takes, preserving the original speaking speed. Game implementation, deployment, paid runtime-model calls, human playtests, Asana changes, repository publication, and CourseWorks submission have not been performed. These updates do not establish design validation or gate approval.
