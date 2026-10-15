---
title: "DSM and hackathon scoring rubric"
date: 2026-10-15
type: dsm
tags: [dsm, growth-portal, gp-263, gp-262, gp-258, gp-259, gp-273, hackathon, scoring-rubric]
participants: [Harvey, Ethan, Bernard, Clint, Lawrence, Joshua, Louise, Kentward, Vic]
source: "/home/yander/Videos/dsm/[dsm and hackathon insights] screenrecording-2026-10-15_13-32-55.mp4"
transcriber: gemini
saved: 2026-10-15T15:57:45
---

# DSM and hackathon scoring rubric

## Executive summary

**TL;DR**
- Stand-up [06:44–15:00]: GP-262 approved and merging, GP-263 closed on prod, GP-258 and GP-259 merged, GP-273 (two badges) awaiting review.
- After the stand-up, Vic presented a draft hackathon relay scoring rubric [16:07–29:00]. PM 35, UI/UX 25, Dev 35 (as spoken), QA 15, with per-role sub-criteria. The team approved it with changes: add AI-usage criteria.
- The rest was a hackathon rules discussion [29:10–48:00] and then off-topic chat about office, laptops and badges [48:58–55:00].

**Decisions**
- Rubric approved as the base; Vic will update it and share the link [27:35–28:19].
- Time box is 3 hours, to be marked "not final" until announced [47:26–48:53].
- Personal AI subscriptions are allowed as optional in the rules draft until Sir Ed decides whether API keys will be provided [40:13–40:40].
- Participants cannot also be judges [48:11–48:26].
- Submissions go through Google Drive, with a person in charge populating the folder [43:05–43:54].
- Every participant demos, as a recording; each role's deliverables include a hand-off brief [44:25–46:11].
- Joshua takes over the new badge task from Ethan [07:42–07:54].

**Action items**
- [ ] Vic: add AI-usage criteria to the rubric and share the doc link [28:20–29:04]
- [ ] Vic: add individual scoring basis if Sir Ed prefers team scoring [42:12]
- [ ] Ethan: upload the Tech and AI rules doc; reach out to Sir Michael about the new badge [07:20–07:35]
- [ ] Ethan: confirm with Sir Ed whether API keys are provided [38:16]
- [ ] Joshua: create the second badge; Vic to review the GP-273 PR [10:38–11:03]
- [ ] Kentward: send the headcount survey (UI/UX and PM only), add contestant-or-judge question if feasible [12:47, 14:35–14:53]
- [ ] Clint: continue reaching out to contestants and judges [09:22]
- [ ] Bernard: finalize the hackathon schedule draft [08:15–08:28]
- [ ] Lawrence: polish the client brief draft [10:00]
- [ ] Harvey: consolidate findings and prepare playbook V2 [14:02]; ask Maricel about mentors judging AI prompting [33:36]
- [ ] Harvey: raise Joshua's Leo bug at the next feature alignment [11:54]

**Blockers / risks**
- Joshua's GP-273 PR is waiting on Sir Harvey's review.
- API key provision is unconfirmed and may depend on headcount [38:16–39:49].
- No clear way to score prompting quality; options discussed were mentor judges, token usage via provided API keys, and structured MD profiles [30:35–35:30].

**Open questions**
- Will Sir Ed provide API keys, and which models are allowed?
- Should AI usage count in the criteria, and how would it be scored?
- Team or individual scoring (Sir Ed's call)?
- Judging logistics: demo length, tie-breakers, bonus points [23:52].
- "Q2 2026" in the transcript at [10:00] is probably the Q3 2026 export (GP-263); likely a misheard term.

## Transcript

[04:10] Hello team, good afternoon.
[04:15] Good afternoon.
[04:18] Good afternoon.
[04:22] Ah, let's wait for Clint a little bit.
[04:27] How about Vic?
[04:29] Ah, I think Vic won't be able to join. He's not responding also.
[06:16] Ah, just a minute. Vic responded that, responded that he will be able to join.
[06:44] Good afternoon, everyone. So, ah let's have our quick update. Let's start with Ethan.
[06:51] Ah hello, team. Good afternoon.
[06:55] So, updates for the GP-262. Ah Sir Lloyd finally replied and he also approved the PR.
[07:05] And ah Vic also approved the PR yesterday, so I'm merging it right now, and I'll be creating a PR to prod for it later on
[07:16] since it is just a documentation change.
[07:20] And right now, I'm working on the Tech and AI rules for the hackathon,
[07:26] the one I was assigned with, and I'll be uploading the Google Docs link for ah what I came up with.
[07:35] And I'll also reach out to Sir Michael regarding the new badge to add.
[07:42] Ah Joshua, ah would you like to take over the task on adding the new badge?
[07:51] Ah yeah, that'd be fine.
[07:54] Okay, okay. Ah thank you for that, Joshua. Ah that's all for my updates, team. No blockers.
[08:01] Thanks, Ethan. Bernard?
[08:04] Ah hello team. So for my updates, ah I've been exploring the LEO
[08:11] from the Growth Portal staging environment,
[08:15] and currently, I've been working on the ah my assigned task for the hackathon,
[08:21] which was the schedule, and I've created an initial draft for it,
[08:28] and I'll probably finalize it after ah Tentwords ah is finished.
[08:36] So, yeah. That's all from me. Thanks.
[08:39] Thanks, Bernard. Clint?
[08:43] Ah hi, hi everyone. Ah hello, everyone. Ah quick update on my end.
[08:49] Ah yesterday, I reached out to ah possible ah judges or either contes-- contestants
[08:58] for ah the respective roles for hackathon.
[09:03] Um the PMs already replied, but did ask on when
[09:09] will be the hackathon is held, or when it will start.
[09:16] And I replied to them that there's no exact date for this.
[09:22] And I'll continue um reaching out on to the other roles for today's work.
[09:30] And also, I merged the PR GP-258.
[09:37] It's for the um adjusting the wiki.
[09:43] And other than that, I think there's none to update. Thank you, everyone.
[09:48] Yep, thanks Clint. Lawrence?
[09:51] Ah good day, team. So for my updates, ah yesterday, I reached out to Sir Harvey regarding the status of
[10:00] GP263 in prod and he has confirmed that the Q2 2026 performance analytics export works already, so I've proceeded to close the ticket. And on my task on the hackathon, the client brief, I've made an initial draft. I have yet to polish it, so I'll continue to do that one. Other than that, yeah, that's all for me.

[10:34] Thanks, Lawrence. Joshua?

[10:38] Ah, hello team. So, for my updates, I already created a PR for my ticket GP273, which is the creation of the two badges. I requested a review from Sir Harvey, but he still hasn't responded. So, maybe I can request you, Vic, for a review?

[11:01] Oh yeah, sure.

[11:03] Yeah, then as Ethan mentioned, uh there's another badge to create, so I can also work on that. And then uh just a side note, uh in my PR, I also uh added a note in the description that uh Ethan has proposed before the UI or the badge creation, so hopefully if Sir Harvey takes a look at it, uh hopefully Sir Harvey can revisit the idea again.

[11:36] And then uh also shared a while ago that there's a weird bug in Leo, but I'm not sure if that belongs here since I'm not sure if independent ang Leo with global, but uh yeah, that's all. Thank you.

[11:54] Ah, thanks for that, Joshua. So, let's uh just raise that for uh our next feature alignment with Sir Harvey. And yeah. Uh, Louise?

[12:05] Hi, team. So, for my update, earlier, I just interviewed Angelo Gabisan. So, now I have one responder. And then uh today, I'll be continuing sending out messages and uh wait for responses. That's all for my update.

[12:25] Thanks, Louise. Kentward?

[12:28] Um hello, team. So, for my update, I merged and did the IT for the GP259. And I also reached out to Sir Harvey regarding his opinion for the UI changes, and he has comments for it, so I'll try to resolve those comments.

[12:47] And currently, um I'll be creating a survey for the headcount on how much will join on certain roles like UI/UX and PMs because they have smaller headcounts. And we'll probably send that later on. So, yeah. That's all. Thank you.

[13:07] Thanks, Kentward. Vic?

[13:09] Yeah, so uh yesterday, I had attended with the uh compound uh meeting and also um all the check all those PRs from the other guys already approved some of it. And all today I'll check on with uh Joshua's request regarding with the PR. I already reviewed that yesterday, but uh I was waiting for Harvey if he would like that uh specific image, but uh as for me, it it's totally okay.

[13:40] And today I'm wrapping up uh the scoring for the uh hackathon relay rubric, so I might have to sit with you, Harvey, regarding on this, so uh we can talk about it um after this call. Yeah, I think uh that's it for me.

[14:02] Ah, thanks, Vic. So, for me, update, so I'm just preparing for the for the consolidation of everyone's findings on the hackathon and preparing for the next version for the playbook V2 for the hackathon.

[14:16] And then, yeah, team, do you have any concerns? Kent?

[14:23] Um Kentward, have you already uh send out the surveys or yet to send pa?

[14:33] Yet, yet pa.

[14:35] Uh can you include a uh I think a one lang nga ibutang dito nga whether they want to be a uh a contestant or either they want to be a judge?

[14:49] Mm I'll try. Pero sa kuan ra ba na, sa UI/UX og sa PM ra man i-send.

[14:53] Ah okay okay okay. That's good. Thank you, Kentward.

[15:01] Does anyone have any concerns?

[15:05] Uh one thing. Um yeah, uh it's not a concern really. So, um after this, uh let's gonna have a quick discussion. Uh I'm not sure if everyone's wants to pitch uh join in. Uh if everyone's done. But I can share the documents here and then let's discuss about it.

[15:28] So, uh team, are you available for a discussion with Vic?

[15:33] Ah, yes. I'm available. I'm up for it.

[15:36] Yeah, yeah, yeah. I am.

[15:39] Uh I think that's one. Understood, team. Last, uh I reach out to you with sa inyong assigned nga katong giingon ni Sir Ed ba whether you'll be a judge sa PM and then I'll reach out to you if okay ra ba na. Is that good? Yep. Thank you, team.

[16:01] And yeah, uh Vic? So, maybe we can uh start the...

[16:07] Okay. Just a quick one. Um I just had to run. So, uh let me know if you can see my screen now.

[16:18] Ah, it's I'm not on my laptop machine, so... Yes, we can. Yeah. So, here's what I had. Um I had to check all those documents. I had also uh reviewed all of it and how and also the feedback that we had. So,

[16:36] here's I had I had to like check on this manually and then somehow feed it with most of my findings. So, here's what we come up. So, total score uh this is a relay, right? So, it goes from the PM to goes to the UI/UX to the development to the QA and then final launch as stated on the playbook. So,

[17:01] on the stage, there's the product planning or which uh which is the PM. So, they have the high impact direction uh especially because that they're the ones who uh break down the stories and also those like um ah uh like let's say uh metadata and also those models. So, uh it's somehow like really an architect side or maybe a I don't know, like

[17:31] the architect planner. So, they have the highest impact. They have the 35 points. Um I'm not sure you can just object it on this, Harvey. Uh this is my initial finding on what I found. Uh or everyone. So, UI/UX design, these ones uh translate plans into an experience, uh especially the UI. Development, they build the working product, and QA verifies the reliability and readiness. Uh why we had a 35 score on the development? Because they are the ones who is like the most stressed out in the entire development, because product planning, uh it can take just like a few hours. UI/UX design, they can just like scratch it out on a scratchpad, and development can take time because they need to do the logic, uh they need to translate all those business logic into uh to feed it on the AI because this is uh uh relying on the AI. So, we have sub criteria. Uh they have to deal with the problem definition and targets. Uh these are the corresponding points uh from 0 to 6. Uh this is uh ranging to uh it would result into 25 as a max score. MVP scope and prioritization, uh they would look how they handle it, acceptance criteria and user stories breaking down, and hand-off artifacts such as wireframes, API contracts, data models, and asset lists. And also they handle the risk mitigation and timeline, because uh of course, they're the project management team, so they would be able to see oversee uh the entire uh running scope. So, here's uh what the scoring notes we had. Uh high score, this is a clear problem, realistic MVP, measurable success metrics, complete acceptance criteria, and strong hand-off documentation. So, uh the low score should be the vague goals, missing criteria, unclear scope, or incomplete hand-off. So, I'm going to like summarize this in a bit. So, UI/UX design, they're the ones who done the designing, user flows and interaction mapping, uh high-fidelity screens and components. They handled all those UI mobile, desktop, or tabs. Also design hand-off quality, like uh specs, tokens, uh assets, and redlines. And also usability validation, because uh this needs to be a properly um well-rounded design. And also the accessibility. For...
[20:00] For those people who have like trouble handling computers, especially like if they have an hearing aid or something. So, we'll consider that as part of the UI UX. And also development.

[20:16] Core feature completeness, technical correctness and complexity, like how complex it is, the code quality, if it follows the DRY principle and the SOLID principle, if they're building on .NET.

[20:30] So, it should have that because that's how we scale or how we decide how robust and scalable the software is, and also how it is reusable in every scenario.

[20:44] And also the deployment and demo, should not should be able to like easily deploy this. Like how complex it is, do they need to have like Azure Bicep or it depends on how they would handle like the CI/CD.

[21:00] And also, especially the basic security and data handling. This is the one of the crucial parts because it needs to be secure. It's not like we can just like do the SQL injection on them or like breach out all those API.

[21:17] So, for the QA, it's really not that much because they would just like create a test plan and coverage, create an automated test. So, that's why, if you can see, the QA Quality Assurance have only 15 points

[21:33] because this is a relay. It's moving forward. So, what I've had in mind was the test plan coverage has the highest point because they would execute all those ones, also automated test,

[21:47] and also the bug reporting and reproducibility, and also stability and regression test. This is to ensure like all test points are covered, especially on the comprehensive test plans, automated smoke test, and clear bug reports reports.

[22:04] And also the demo stability, so that we would be able to, we won't see inconsistency during the test. For example, yeah, I work on this, and then the next time, it doesn't work because there's something wrong with the data or there's some inconsistency in handling, especially in the back end side.

[22:22] So, we have this the deliverables from project manager, one page brief, problem user, success metrics, prioritized acceptance criteria, so that we would have a limitation on where we would able to land.

[22:40] And also API and data contracts, required asset list. For the UI UX, annotated screen, interaction flows, component specs, exported assets, and validation summary.

[22:51] For the development, it's a runnable build or demo link, Readme with setup deploy steps, the one that we you guys recently worked with the, I think I think that was Clint and also Kentter regarding with the MD files. And also I forgot who created that AWS Azure to AWS. That was a pretty interesting document. So, had to check that one by one.

[23:19] So, so this is the one of the deliverables for development. QA will always have their test plans in place, automated test scripts and results, bug list with severity and repro steps.

[23:32] I think this is one of the highlights, like the severity one. Because how largely impacts that with the software. So, because we have in the real world, we have severity 5 7 1 to 6. 1 is the highest and 6 is the lowest.

[23:52] So, for this is just I haven't had any, let's see, any idea right now like the judging logistics, like how long would it take to do the demo flow,

[24:09] and also regarding with the tie breakers and the bonus points. Bonus points is just like how production-ready it is when you want to deploy without having a hiccups, and also a real user validation, not just from attacking on the unit test, attacking from the QA test, but a real user scenario.

[24:30] So, this is what I come up with regarding, I think you have assigned me to, Harvey, the dev and UI UX and PM and QA. So, this is what we come up. We can modify this one if you, somehow, you disagree with the others. I'm already I'm always open to suggestions so that we would be able to work on this one because this is one of the crucial steps on handling the scoring.

[25:01] So, any feedback? I really appreciate it if you have one.

[25:08] So, guys, what's what your thoughts regarding this, Vic?

[25:14] I might miss something because, somehow, I inputted this manually, and I had just AI verify it and then write a summary. So, I'm not sure if I miss something. So, this is what's on top of my mind since yesterday.

[25:33] So, Vic, are you aware that this is a individual, a individual activity, not a team?

[25:43] Yeah, that's a that's one of, uh, one of uh like, one of uh last time that we had a discussion with Ed. So, that's why I was thinking as this is a team first, and I can just like break it down because I don't know how it would look like. Because, as I saw, it was a relay. I'm not sure like how this project's been handling. So, I would be able to safely execute as individual on this. But is this a, as far as we discussed last time, correct me if I'm wrong,

[26:26] So, whoever wins with the PM, that would be the proposed UI for the next, right? UI UX. And then individual. And then who wins with the UI UX goes to the development, and who wins the development goes to the QA, right? QA, right?

[26:46] Yeah, right.

[26:47] Yeah. So, I had that in mind, like on the first build that I had. What I had is just like an initial draft because I can just easily execute this on an individual basis. So, this is what we would this is what our scoring logic would be. So, we can just like if this like on the paper points, I can just check this by individual. So, this is what we had in mind. Regarding with the criteria, please let me know if you have any questions or any concerns on that. Because we would just be able to, it's just the points. We can just check on the individual parts. But right now, this is what we had in mind.

[27:35] Yeah, thanks thanks for this, Vic. So, for me, this is already good. So, and then, Vic, can can you upload this, the link for this one in the--

[27:44] Oh, yeah. Yeah, I think I had this. This is just like, it's keep breaking down the design. So, I'll I'll also update this one. I already had this. I forgot to share with you, so I'll check it out.

[27:58] Ah, yeah. So, team, do you have any thoughts?

[28:06] No, no, man. I think this is good.

[28:10] Yeah, same same for me. I think this is a very thorough, actually. So, yeah. I approve this one.

[28:19] And

[28:20] Yeah, for me, I think, uh, should we include in the criteria for the AI usage since it's for the, uh, the academy?

[28:34] Mm, good question. Maybe because I was too old school that I don't really rely on AI too much. Thank you for that, Bernard. So, yeah, I think we can include that. It's just like this is one of the high level that I had to take without consideration of the AI usage. So, yeah. Must be getting old, getting caught up to me. So, yeah, I'll add that. I'll consider that, your options.

[29:04] So, team, does anyone have concerns?

[29:10] Kuan ba, regarding sa time frame ba. Is it okay if we have a fixed time frame length time frame lang like, Sir Ed double said nga the participants can pick a time to do the task, ba?

[29:24] So, for kuan na, Kent, kay--

[29:28] Ako ba'y nag-i-apply nga concern? Kana gung giingon nimo, Kent, kay di man ta kabaw pod nga kanus-a sila magsugod, ba?

[29:36] Eng, or like, kita'y mo-kuan ba, provide sa time frame kay mo-schedule. Amo na gi-Bernard gi-work-on na sa format sa schedule.

[29:46] Mao pod. So, kaning survey nako, murag di na lang guro nako i-include og kuan ay, kanus-a sila free. Kana na lang ay, kung kanus-a sila mag-start.

[29:56] Oh, pero within the time frame na gi-provide nato, kay para mo-provide
[30:00] sa katagon ba, kanus-a jud ang judging?
[30:04] For example, 8:00 AM to 7:00 PM. Maw na'y
[30:08] time nga dira sila mo-do sa task. Nya ang judging kay 8:00 to 9:00, ing-ana ba.
[30:13] Mm.
[30:15] pwedeng saktabo na
[30:17] initial jud nga time frame ba kung kanus-a jud. Maybe they can, maybe maka-adjust ba ron or what.
[30:22] Ana ba.
[30:24] Oo na, kun kanus-a sila magsugod kay dira mo-start ang timer.
[30:30] Kani pod diay question ni Clint ba. Ah sorry, kadiyot lang.
[30:35] Ah regarding sa scoring sa "how they prompt" ba.
[30:39] I'm not sure, everyone has their own techniques man, 'di ba?
[30:43] What are your thoughts on it? Kani kay ako,
[30:45] maglisod ko'g track, maglisod ko'g trace. Kay depende na unsa sila kabait mo-prompt, giunsa pagplano, unsa'y inclusion sa mga
[30:55] skills gi-add.
[30:58] Kay what if gi-add syag get shit done ug katong
[31:00] superpower sa Context7,
[31:04] mas mo-improve man gud. So, what if kanang lightweight or what if gi-andaman nya pareha sa atong gibuhat gahapon, tong compound
[31:13] development. What if gi-apply to? Kay
[31:15] gahapon nag-experimento man pod ko. Nagbuhat ko'g ana, kanang compound development with full TDD.
[31:22] And also ah kuan,
[31:25] so mao na,
[31:26] maka-improve sya
[31:28] if naana sya pod daan nga framework, which is
[31:30] how, I don't know unsaon pag-score ana kanang prompting.
[31:37] Unsa token-based ba? Pila ilang token na lagas during the development or during the PM
[31:45] or during the contest? Unsa may inyong idea ani?
[31:50] Ah sorry Kent, ha. Akoa, akoa te-ato balikon nato.
[31:53] Okay ra.
[31:55] Pero like
[31:57] kun mag-base ta sa prompt kay unsaon nato pag-kuan?
[32:00] Oo, kana. Mayo mo-prompt.
[32:04] Unsa man? What if naana syay superpower? What if naana syay, unya kabawo sa technique sa tao, lain-lain man 'di ba?
[32:11] 'Di ba mao na nisulod sa akong mind jud kay 'di ba sa AI Level Up Accelerator, gi-train ra ba tawon how to properly use the AI, ana.
[32:20] 'Di ba, and how we can maximize the usage of AI, so
[32:24] nakathink ko what if na-apply ba nila ang mga trainings nga gi-buhat sa AI Level Up Accelerator or sa mga
[32:31] or sa mga courses nga gi-hatag, like paghapon nga
[32:34] activity nga ato ba. So, that's why nakathink ko nga i-include sya.
[32:38] Good point jud na, pero
[32:41] wala ko kabawo unsaon pag-score ana.
[32:44] Naa sa cheat.
[32:45] Kay ako ha, to be honest,
[32:48] I-copy paste nila ang prompt.
[32:50] Ah what if ang mga mentors ang ato i-pakuan sa mga AI promptings? Like sila ato pa-judgeon.
[32:58] Since sila man sad ang nag-mentor jud sa kuan accelerator.
[33:04] Ako mentor ba kay sa accelerator,
[33:07] so mao pod before ko nabalhin diri. So ah
[33:12] lisod man sya. Oh non, katong mga pagka-mentor namo 'di man mang-reply ang mga tao. Ambot ngano na sila.
[33:19] Pero
[33:20] ah kanang no,
[33:22] good point, good point na ing-ana. Maybe, oo, mo-reach out ta sa mentor,
[33:27] pero ang pangutana mentor naa ba silay oras? Ah naa man silay oras, maka-PM ra man ko nila kay apil man ko sa ilang chat. Maybe we can ask
[33:36] them for help regarding on this. I'll ask ah Maricel siguro
[33:41] if maka-coordinate ba sila.
[33:44] Pero kana no, katong giingon ni Clint kanina, ah ambot, ambot lang.
[33:51] Kay
[33:52] oo, kay 'di ko maka-kuan og unsa jud kamayo mo-prompt ang tao. What if kanang
[33:58] structured lang jud sya, what if
[34:00] ga-rely na naa syay mga md daan nga mao ni i-follow kay ang Claude baya naa ma'y specific profile
[34:07] nga i-saksak nimo as a kuan para 'di na ka sa every prompt moingon pa ka "act as a senior kuan, nya mao ni imong kuan". Naa na baya na sa Claude na-set up. What if kanang gi-
[34:18] heavily abuse na iyang Claude ba for, depende nalang unsaba nga AI.
[34:24] Oo.
[34:25] Unsay thoughts ninyo ana?
[34:30] Kay ako man gud old school man, ah 'di man pod old school ha, kanang 'di kay ko tig-rely og AI.
[34:37] Kanang, to be honest lang ah 'di kay ko fan.
[34:41] Pero lingaw man gud mag-code. Kay mao mao nang
[34:45] mag-rely ra ko'g AI for additional research and verification. So,
[34:51] kana ba.
[34:52] Unsa inyong points ana?
[34:57] Tim, naay pod mini thoughts ana na kuan? Ah kuan sad diay, if
[35:03] ah in regards sa ilang magamit nga AI model sad ni, if provided ba or pwedeng ba ilang own
[35:11] maybe subscriptions?
[35:13] Kay 'di ba naa toy gi-ingon sila nga lower model, ah mo-taas, unsa 'to akong nabasa?
[35:16] Nag-suggest man 'to si Sir Ed nga
[35:18] Sir Ed.
[35:19] if tanan ba same model, Sonnet,
[35:22] or
[35:23] pwede ba silang mo-gamit og higher kuan,
[35:26] kanang higher intelligence nga models?
[35:29] Maybe ma if mag-provide ta'g API key, ma-track ba nato ang ilang
[35:33] Oo, kana. If mo-provide ta'g API key, sakto, sakto na Lawrence.
[35:38] Kay ah if kana man gud what if si kuan ah what if ah si PM nag-generate og,
[35:46] what if sya ni-gamit og higher model? Kay og mag-planning man gud ta sa AI, um always use higher models
[35:54] sa planning phase, unya lower model na sa tig-code
[35:58] para 'di kay lagas og kuan ba, token.
[36:01] Pero mao na sya ah
[36:04] asa or unsa ilang permitted nga magamit.
[36:20] So, ah I think we can have a further discussion ana na topic sa katong kuan,
[36:26] katong ilang AI,
[36:27] ilang prompting if e-need ba nato sya e-
[36:30] apil sa criteria.
[36:33] So, maybe we can have a research pa jud ana.
[36:37] Just to clarify
[36:42] Give me a time to check.
[36:49] I think Joshua set as a good point.
[36:55] So,
[36:56] Short baya tanan 3 hours, kana ing-ana ba ang time constraint, 'di ba?
[37:01] So, 'di ba 'to
[37:02] Kana, dinha, kana dinha na makita bitaw ang
[37:06] effectiveness.
[37:09] Siguro e-consider nato ang
[37:12] time execution, no?
[37:14] Pero naa man gud uban nga "Oh, trabahoan na kani, ah balikan lang nako in the next 5, 10 minutes kay naa pa ko'y gitrabaho," ana ba. Butang 'to
[37:22] ang PM
[37:24] mo-to-to og iyang gi-basa, nag-draft na sya,
[37:27] "Ah balikan lang nako kuan." Walay kanang bitaw'g straight bitaw'g prompting.
[37:31] Pero kana, makita na if mag-trace, as per Lawrence, atong ma-trace na na sya
[37:37] gikan sa API key.
[37:40] But I'm not sure how it would work.
[37:45] Oo, 'to.
[37:50] So, yeah. So, Tim, do you have any
[37:53] ah concerns pa or clarification?
[37:58] Um just to add lang, kana
[38:01] sa katong tech rule or tech and AI rule sad nga akong gi-create kay akong gi-decide or akong gi-butang didto nga
[38:09] gamiton jud ang katong dedicated ah API key per participant.
[38:15] Tapos
[38:16] ang akoa lang is kanang confirmed na ba jud nga mo-provide jud sila'ng Sir Ed
[38:23] og API key
[38:26] para sa kani nga event?
[38:30] I think if ato na syang e-raise jud na mo-provide sila kay
[38:33] since kuan man 'di sya kanang external jud na
[38:37] if internal na event kay I think mo-provide ra man pod guro sila if ato ginana syang e-pursue,
[38:42] ana, iji lang mo-provide.
[38:45] Mm.
[38:54] So, 'di pod pod ah sure na mo-provide jud, but
[38:59] Kay magduha-duha pod na sila gud kay last time, um
[39:04] nangayo, ah naa'y isa sa kuan namo,
[39:07] kana lage kanang mo-provide bitaw,
[39:09] nangayo ang isa one of ah us katong sa under sa mentor nako,
[39:14] nangayo og key,
[39:16] pero ila pasabtan. So, mao na'ng
[39:18] unsa na, ako na e-erase diri kay na-butang na, na-isgotan na man jud.
[39:24] Ambot og kanus-a na pod sila maka-provide if maka-provide ba dayon kay katong
[39:30] kung sa accelerator kay wala man ma-providan. Mura'g na-limit.
[39:35] Mm.
[39:36] Ah mao na, usab pod ug
[39:38] how how much would they be able to provide?
[39:43] Maybe mag-agad ra sad sa head count ana.
[39:46] Kana sad sa head count.
[39:49] So, mura'g kuhaon pa ang head count siguro sa mga tao.
[39:56] So, yeah. Uh another question pod, atong action item ni
[40:00] ...sunod na alignment nato.
[40:04] So, naa pa bay concerns sa inyong task?
[40:11] Alright, additions...
[40:13] For now, okay... Sorry, sorry. For now, kana, okay ra ba nga ako lang sa i-allow ang pag-use sa personal nga subscription nila for the rules lang sa atong hackathon?
[40:26] Kamo unsa man storya ninyo ana?
[40:33] I think pwede pa na karon, pero anyways, kuan pa man sad, draft pa man sad ang next draft so pwede ra man siya ma-soft...
[40:40] Keep it as optional lang sa siguro until ma-decidan nila ni Sir Ed if kuan ba, mag-provide ba gyud sila.
[40:49] Ah, in regards pud sa katong tools nga i-use bitaw, let's say katong na-mention earlier katong super powers o katong get shit done, atong i-limit ba sad ato? Also if i-limit nato, the good kay murag contradicting siya sa katong gitudlo sa AI accelerator.
[41:07] Kana, sakto. Mas maayo baya i-utilize jud nimo para part man gud siya, part na jud siya pero kana. Unsa pa ba sad ang kuan...
[41:21] So, mao lang na siya akong concern. For now, ako lang sa siguro i-allow and mo-kuan lang ko sa assessment ani sa next iteration.
[41:33] So yeah, so maybe we can do it that way sa Ethan, dayon... Ah, anything pa?
[41:39] Ah, goods na sa akong end.
[41:44] Agree ra ko atong iyang kuan, katong mas maayo i-utilize depende na sa technique sa tawo. Dinha maylhan og unsa imong kapabilidad paggamit sa AI.
[41:55] Oo pud kay bisag gamiton pa nimo ang pinakanindot na framework og di nimo...
[41:59] Dili gihapon ka kahibalo mo-use, wa gihapon.
[42:04] So, team, do you have any additions pa?
[42:12] Mo-provide lang ko unya Harvey sa kuan, katong update nga individually-based, pero kani kay in one, one go lang ni. Mura'g ana lang. Pero in case ha, og moingon sila, "What if? Moingon sila, "Ah, what if e-team lang nato kay... Kani ha, atola ni raise. What if moingon si Ed nga "Ah, i-team lang nato kay... Atto kay i-limit ra ang head count or basin ganahan silag by team, atong na i-add, 'nya mag-create na pud kog kana'g individual scoring basis. Para naa tay kuanan ba, basihan.
[42:45] Sige, sige.
[42:49] Sige, mao ra to.
[42:51] So, ah, does anyone have any additions pa? So yeah, I think mao ra to. So, kung naapa gani concerns...
[43:05] Unsa diay ba ang submissions? Unsay kuan sa submissions?
[43:09] Ang kuan channel...
[43:11] Submissions sa ilang output ba o ta's...
[43:14] Or ah platform? So... Kana, wala pa na-finalize.
[43:20] Ah, I think atong ginasabutan nga G Drive ba atong gamiton? Ah, I think G Drive, G Drive. G Drive sa atong gamiton, oo.
[43:29] Lain man G Drive kay basig mo-pick ang uban.
[43:34] Murag ang nasabutan is katong naay person of contact para mao ang submit-- submission.
[43:41] Naa. Ah, okay. Naay kanong kuan murag person in charge ato, 'nya sila ra'y mo-populate dito na kuan folder.
[43:54] So, yeah, so initially murag mao pa na'y nahibaw-an karon ang platform nga gamiton. G Drive and then... Yeah, so mao pa to. How about team, so naa pa'y lain?
[44:11] Ah, goods na ko.
[44:13] Goods na ko.
[44:16] Paspasa na puy paldo na. Nag-English-English man sad...
[44:23] Ah, pipaldo day.
[44:25] Franklin, ang demo nila ba, unsa diay paagi? Let's say, mupasahan sila, mo-submit, and then, i-demo ba nila each role ba or naa ra'y specific role ra ang mo-kuan?
[44:36] Like, ah, ig human...
[44:38] Unsa to? Unsa to? Unsa na, mo-demo si PM, mo-demo si UI/UX, 'nya mo-demo pud si developer? Mao bitaw'g gi-kuan nako to, Harvey, mao to'g gi-usab-usab na pud nako. Basin mao ang type of approach. Kay lain man, ayaw sa, mag-demo sa ko'g PM. Mao 'ni akong design, ha. Sige. Ah, okay. 'Nya sunod si UI/UX. Ah, oo. 'Nya sunod mo-balik na pud sa developer. Aw, kita na nako ana. Mu-ana ba.
[45:08] 'Nya sa mga rules sad nga daghan kaayo, daghan kay'ng mo-demo. Ayan, winning ba'y mo-demo or...
[45:16] Dili, i-demo man sila tanan.
[45:19] Demo sila tanan. Unsaon pag-judge ana og kinsay kuan, nindot ug...
[45:25] Kuan, recording ang kuan demo?
[45:28] Recording.
[45:29] Oo, ana, ana, ana.
[45:34] 'Nya panel-based man kaha ta? Unsa 'ni, ganang murag, murag tag nag-thesis ani?
[45:44] I think if wala gyud katong judges kay murag kita'y mahimong kuan siguro. Oo. Katong option ni Ed. Anyways, sa katong ilang delivery pud kay naa gyud toy kuan sa atong hand-off, hand-off brief kung unsa, unsa'y kuan nila, philosophy sa ilang gihimo. So, apil na siya sa katong deliverables each... role.
[46:11] Sa kuan diri PM deliver, ang kanang one-page brief kay under sa PM deliverable.
[46:18] Mm-mm.
[46:20] Sige, atong, atong, atong i-refine na. Tagaan na nato'g kuan, update.
[46:26] Sige, sige. 'Nya, team, naa pa'y lain concerns?
[46:38] All goods. Tan-awa, tan-awa ra to atong Google Form daw. I-send nako.
[46:47] Sige daw, asa daw na, bro?
[46:51] Naa sa chat. Sa UI/UX ra nag-PM. Isa pa man sad diay siya mag-present.
[47:26] Ah, decided na nga 3 hours? Ibutang lang og kuan, "not final", kulang ato. Not yet final.
[48:11] I-allow ba sad 'ni siya na a participant pwede pud siya mag-judge?
[48:18] Unsa? I-allow, i-allow ba 'ni siya? Ang participant pwede pud siya mahimong judge?
[48:24] Dili.
[48:25] Dili, so?
[48:26] Oo. Kanang either kay basin kuan 'ya ba. Ang kanang either kay basin naa'y duha ka buok mag-judge. 'Nya kailangan ra ta'g usab.
[48:37] Ah, okay.
[48:49] So, I think good na man ni. So, kanila kay atong i-announce pa man ni siya so, kay 3 hours.
[48:53] Oo, sige. Oo, ibutang nga dili pa final.
[48:58] Pero I think murag naa man sad i-kuan, katong sama sa giingon ni Sir Lloyd na ang participant kay naa'y token of appreciation siguro o ambot unsa ba kana siya.
[49:08] Awa, prizes na na. Mao na'y prize nila.
[49:12] Badge sa Growth Portal. Mao na'y prize. Badge...
[49:17] Lain sad pud badge sa Growth Portal. Kadtu-an lang sa opisina, pang-pangkahuag lata, dangan'g lata. Daghang Coke didto. Adtu-an ba mog opisina or dili? Or balay ra mo tanan?
[49:34] Balay ra tanan.
[49:35] Dili gyud.
[49:36] Except lang ni...
[49:37] Kamo diay mag-opisina? Ngano man, manguhag lata didto? Daghang bag? Manguhag, manguhag de lata, mga piattos. Mao na'y buhaton nako panagsa, adto-an nako nang opisina, kuha kog upat ka lata, lima. Panagsa ra man ko mag-opisina, panagsa ra man ko manguha. Okay ra man sila.
[50:00] Oo, katong kuan ba, 3rd month nato, na kailangan tamag adto. Katong medical. Di ba naa man to sa contract?
[50:08] Medical, APE?
[50:11] Kalimot ko, naa gi-mention nga 3 months kay patuon mi kay medical.
[50:16] Ah, wa man pod naka-apil og APE? Last...
[50:20] Di APE, unsa APE? Katong annual physical? Ah wala.
[50:24] Wala pa man, US July naman mi nakuang...
[50:27] Ah kuan pa na, next year pa na, next year pa na. Kanus-a gani ang ilaha, April, May?
[50:34] Layoo pa na.
[50:39] Takto, gikan snack paid to, sa mga ing-ana.
[50:43] Di, di na pud ko ganahan mo-adto sa opisina, natagam ko. Ikaw kay linog-an mas 25th floor, ganahan ba ka?
[50:51] Ako pa jud isa ra to, taya jud ato. Maingon ako nga di na ako mo-adto opisina. Buntag na.
[51:01] Kani, kani wala na ba kay ID sir nga kani physical jud? O ang amoha o-arm jud, soft copy.
[51:06] Wala, soft copy ra. Nya ang ID, ipakita man ang ID didto nya naka-kuan na me, kanang fing- naka-fingerprint man kaha mo?
[51:14] Wala, wala pa pud.
[51:15] Wala.
[51:16] Ah request lang mo ni kuan, o mo-adto mo, request lang mo ni James. Tagaan mo ana, i-register man.
[51:23] Mao ra man pod silag gibuhat. Sulod, tubangon mo, nga mangayo katong badge, nya abot sa taas, fingerprint.
[51:32] Katong sa gi-ali, gi-promise ko nga naadaw monitor.
[51:36] Moolla diay. Wa mo taga-i? Moolla. Nalang kulang sa duha ang equipment. Ang guba pa jud ka-client.
[51:46] Wala pa mo, wa mo taga-i og monitor? Unsay gihatag, laptop og headset?
[51:51] Oo. Oh, tapos bitaw, nya wala'y mouse, ning Wi-Fi router.
[51:57] Ah tong Wi-Fi, oo. Ako kay gibaligya pud nako ang Wi-Fi monitor. Pwede ra mo maka-request man didto og kinahanglan ninyo mao na.
[52:05] Ang kuan sir, ang ilang giingon kay nag-request ba sila sa supplier daw.
[52:09] Oo, kay wala pa daw, maski ang akong laptop kay di na man gani mo-siga halos.
[52:14] Sige nya ang akoang Mac, wala pa jud gihatag.
[52:17] Oo, mao pod, mao pod, nag-request Mac? Nag-order na man daw sila, nagkastorya kami ni James, ang giingon kay kanang nag-kuan pa sa supplier. Kay giplanohan man nila is either og Windows ka, Dell imoha,
[52:31] or og Mac ka, katong MacBook Pro. Nya ako man silang giingnan ngano mag-Dell man mo, pwede man mo mag-ROG, mas barato pa.
[52:41] Mahala sa Mac nya Dell ra diay sa Windows. Ngano mag-Mac?
[52:45] Ngano mag-Mac? Diba mag-Mac lagi, mao bitaw giingnan nako nila nga Dell, a Mac na lang pod ba?
[52:52] Kay ang akoa, ang laptop kay i-gamit nako kay murag may turbo. Oo,
[53:00] Mac speed! Naka-diesel! Pero pwede ra ka pa-replace ana og kuan. Ingna lang si James nga ingna lang si James nga kabungkagon na ako laptop, pamasin ma-replace-an.
[53:11] Nag-try ko sir, nya naa pa ko'y i-kuan nga steps ba nga buhaton nga i-check pa ang kuan ing-ana ing-ana.
[53:17] Ah oo.
[53:18] Tas wa ra man kayo. Ah okay. Na-send na nako.
[53:22] Kay gi-pasiyahan man atong refresh nga PC, PC refresh naka-sign up man mo ato?
[53:28] Oo.
[53:31] Oh, mag-orag? Oh, mga next month mo-start na to.
[53:35] Dawat na pud. But ang giingon ni sir Harvey ato kay ang dili daw priority ang kuan sa bench. Priority kay katong...
[53:45] Ako na i, ako na iingnon si James, be. Ingna di me priority? Bench ba diay ko? Mag-bench. Ah dili man diay pod.
[53:54] Pila, kapila na man pod si kuan god, reklamo nitong laptop na ko nga pailisan. Wa man pod niyo pailisi ba. Gi-gitgit na lang sa pilag akoang wire.
[54:09] Nya i-kuan na, istoryaan si James konus-a. Basta makadto ko sa opisina, ako ingnon nga konus-a diay ang refresh? Kay ang among laptop kay kuwang na lang usa ka tukmod, mo-aso na.
[54:24] Mao bitaw naa na ko sa akong personal machine ron gamit, di na ko ganahan mo-gamit sa laptop. Batia man pod.
[54:30] Same, same, same, same.
[54:32] Personal gyud tanan.
[54:35] Kundi ta mag-personal ba, unsa'y trabahoan? Di lang mag-saba.
[54:40] Mas motivated ko mo-gamit sa personal kay di ba barato ang computer, atay.
[54:55] Yeah, team, naa pa'y lain concerns?
[54:59] Wala na.
[55:01] Wala na, wala na. Ah I think goods na man ni Kent na-kuan.
[55:06] Continue work na lang sa inyoang kuan, individual items, and then yeah. Mao ra to. Maybe we can wrap this meeting up.
[55:16] Sige, thank you.
[55:18] Sige, sige, thank you, thank you. Thank you, bye.
[55:22] Thank you.
[55:31] Thank team.
[55:33] Thank you.
