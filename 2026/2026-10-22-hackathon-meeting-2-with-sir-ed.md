---
title: "Hackathon meeting 2 with Sir Ed"
date: 2026-10-22
type: meeting
tags: [meeting, hackathon, relay-launch, judging, schedule, tokens]
participants: [Ed, Harvey, Clint, Ethan, Lawrence, Marycel]
source: "https://drive.google.com/file/d/15cuK3IfTQJoMvTKrc_mmjwm7x-JS0k8z/view"
transcriber: gemini
saved: 2026-10-22T10:26:11
---

# Hackathon meeting 2 with Sir Ed

## Executive summary

**TL;DR**
- Submission window is 3 PM to 6 AM, with scoring 6 AM to 3 PM the next day. Best-case dates are Nov 3 (PM), 4 (UI/UX), 5 (devs) and 6 (QA); fallback is Nov 10–13 [09:27, 16:23, 36:57].
- Sir Ed provides OpenRouter API keys: $20 for developers and $15 for other roles. Going over budget is a penalty outside the 100-point rubric [23:45, 33:01].
- Client brief candidates are DeskDay, Gear Desk and Ask HR. Sir Ed leaves the choice to the team [19:00, 23:45].
- A tiebreaker is decided by a human judge. A scorecard skill (AI score plus human adjustment) is to be prototyped this week [00:17, 07:01].

**Decisions**
- The third schedule option (3 PM to 6 AM) is chosen [09:27].
- The outside experts are converted to participants, and senior engineers or EMs judge about 1 hour a day [15:09].
- Roles are open: anyone can join as PM or UI/UX, announced on the Spartan channel [11:21, 12:44].
- Stack and model are unrestricted. Personal AI subscriptions are not allowed as a fallback. A leaked key is revoked rather than disqualified [27:53, 29:03].
- Token overage is a deduction (about 10–15) outside the 100-point rubric [33:01].
- Go or no-go for Nov 3–6 is decided day-to-day [38:52].

**Action items**
- [ ] Lent: circle back to people who declined because of night shift and get confirmations for PM and UI/UX [09:27]
- [ ] Harvey and Lawrence: build and test the scorecard skill (AI score plus human adjustment) end-to-end [07:01]
- [ ] Harvey and Lawrence: pick the client brief, and plan curveball delivery (automated email about 30 minutes in) [20:11]
- [ ] Team: dry-run the chosen app on OpenRouter to check that $20 is enough [24:39, 26:33]
- [ ] Clint: replace outside judges with senior engineers or EMs [15:09]
- [ ] Ethan: update the tech and AI rules (credits, penalty, key revocation) [29:17]
- [ ] Sir Ed: approve the $20/$15 token budget, and share OpenRouter credits for the dry run [26:33, 31:14]
- [ ] Team: update Sir Ed day-to-day on readiness for Nov 3–6 [39:08]

**Blockers / risks**
- Participant numbers are low: 1 UI/UX interested, PMs unconfirmed [10:17].
- Thirty minutes of scoring may not be enough if there are many developers [07:48].
- Ask HR depends on a funded API key through demo time [23:09].
- Production-ready and real-user validation checks are hard to verify at hackathon scale [02:19].
- The first week of November overlaps with PDUs; the following week the AI Accelerator program starts [17:17, 39:41].

**Open questions**
- Which client brief to run?
- How to automate the curveball delivery?
- Is $20 per developer enough? The rough total budget is about $1,000 [34:32].
- Nov 3–6 or Nov 10–13?
- Do the Accelerator staff assist while they have clients? (Marycel to check) [40:32]

## Transcript

[00:00] depending. So we need to identify those breakers, what will differ to the other, what make the other...
[00:07] So yeah. We have this uh judging logistics. With the demo flow, this is uh how I
[00:17] envision it to be. Tiebreakers, it should depend on like car development score and product planning score,
[00:24] but this would be uh on a judge's uh perspective on how
[00:31] they really liked the entire uh like the logic. Instead of like having AI, uh
[00:39] I wouldn't, because AI the tend- the tendency of using AI as their judge, and like the final judgment,
[00:46] uh it, because I built something like this. Uh it's a scoring of a contest and then
[00:53] most likely the judges are uh real life persons and it even caused a tiebreakers, like lots of tiebreakers because they didn't use decimal.
[01:03] So, uh what I had in mind was have a real like the judge itself
[01:10] uh decides the tiebreaker, like who decides it. Because sometimes AI would just like, "Oh yeah, this guy's good," and then if you like
[01:18] justify the other one, "Oh yeah, it's the same." So, it will always uh accept
[01:25] your point of view. So I think there's always a human intervention to decide the last
[01:31] and final scoring. Also, bonus points if it has the real user validation,
[01:37] if they wanted to demo it, like if they really wanted to showcase their
[01:43] items and also it's a production-ready deployment. Like it's not like
[01:48] deploy it in staging or deploy it in test just to show off, but I think
[01:54] if this is production-ready deployment, all those uh security measures, uh
[02:01] all those being set up, I think that's one of the bonus points that will also do the tiebreaker.
[02:10] Okay. So, yeah, yeah, like... regarding uh how how will you determine if it's a production-ready deployment uh once they submit it? So, yeah, or
[02:20] where users are able to validate it. There's real user validation. So for example, they're just going to submit everything, okay, the developer's done, tester's done, they submit everything.
[02:32] So the bonus points, how how are we going to identify that, okay, this one is production-ready or there's user- there's uh real user validation?
[02:42] So, I think uh this part um what I didn't uh reconsider is about the other uh let's see.
[02:52] Uh what was that? Like it's on top of the... Uh most of these are in developer's perspective.
[02:59] But uh for the real user validation, I think it falls under QA.
[03:05] And uh production-ready is both uh three guys. So,
[03:11] um for the production-ready deploy- deployment, it should have all those uh properly handled
[03:18] especially in the configuration side. If it's like a one-click deployment or if it has uh let's see.
[03:26] Because I need to think about uh this uh more. So, production-ready deployment should be able to like
[03:35] all being handled, uh domain is being handled, it's not using the test URL, it's not like being wrapped. I know this is quite expensive if we do that,
[03:45] but if there's a part of their uh change logs or maybe uh Readme.md file Markdown file,
[03:55] if they had I think that's one of the critical, if they had like the production-ready
[04:01] uh deployment, like it's not just test and also it differs from their environment variable.
[04:09] I think that would be the case, because if we're just like if they just deliver like for testing just for the sake of the uh hackathon,
[04:19] if uh if they just like had it that simple test environment variables, I think uh
[04:26] that is the cases to see if that's it's not a production-ready, because it's only for specified built for that. What if it's deployed to production base?
[04:37] So, I think also maybe we can have two deployments uh to validate, like if it really runs in production.
[04:48] But most likely, this is not the type of uh we might have, because it's just a hackathon.
[04:56] But uh because production-ready needs to be validated by more people to check on it
[05:05] without test data. So, is there real-life data?
[05:08] So, how about we'll just uh finalise, I mean, I'm okay with higher development score, higher product planning score, or it's really a a human uh choice. You guys, if Harvey, as I've said earlier, the the team here could be part of the judges, no? Uh one expert, or you could be the judges, uh and then see to it like what's your feel based on what you see, what you see in AI, what you see, because usually guys, when they develop this one, they're going to provide you the link that's running already. They they can uh uh push this on live environment already. That's what we experienced during the first hackathon that we have. Uh the application uh AI vibe coding that we have. So, our developers already uh put it, even some put it in the Google Play.
[05:56] Play Store or on Apple Play Store, so it really depends on our uh scope, where uh how well we define what's the end product, where it's going to be placed,
[06:09] uh and then our developers will will follow that one.
[06:13] Because of the time constraint as well, so I didn't because we only have a week and then if we like as Ed said regarding with uh deployment to Google Play or App Store, it might need some time like approving app.
[06:27] Yeah, approval, hm.
[06:29] Yeah, that's why uh I didn't just add that, because um I think that's another process and it's going to be like the scope's going to be getting larger.
[06:39] Mm. So we we could uh design it like, okay, uh just deploy it in a local localhost and give us access and then we're going to see,
[06:49] no? So, yeah, we need to to define the scope of the the application being uh, yeah, developed.
[06:57] Okay, so my request is if if you can
[07:01] uh try this one exercise, create some something like a You already have the rubric, uh no problem with that one. You you can decide based on your, yeah, and also come up with something like a scorecard where there's a a a score created by the your AI or your skill and then there's the human part who's going to add additional skills and to determine the final final score or the final ranking.
[07:28] So, if you have that uh within this time, to next week, try to create that skill or I don't know how you're going to implement it, and then somebody create something like end-to-end, like the plan, the kuan, and then let the skill uh score that one based on the rubric, and then see how it goes for you guys.
[07:48] 'Cause we only uh allocate- allocated 30 minutes for the scoring. So that should be smooth. I'm not sure if 30 minutes is enough, no? Depending on how how many, I mean, probably because if there we are only having like 3 or 5 uh uh contestants, probably 30 minutes is enough,
[08:07] no? But for the developer where we have a lot, I'm not sure if 30 minutes will be enough.
[08:13] Comparing the the deliverables, comparing the different kuan, no? So identifying like, okay, this is a tie.
[08:19] Their all their uh unit testing is uh passing or it's good, no? So, so, yeah.
[08:27] Okay, let's go back. Since we have the scoring already, so let's uh let's think about put in mind that we only have 30 minutes, we're going to adjust that one. So that will be part of our decision if we're going to choose from the 1 to 3 uh regarding the flexibility. So, if we're going to choose 6 to uh sor- uh what's that? 6:00 p.m. to uh 9:00 p.m. to 6:00 p.m.,
[08:52] is that correct? Or, sorry, uh what's that?
[08:56] Ah, 3:00 p.m., sir.
[08:57] Ah, yeah, 3:00 p.m. to 6:00 a.m. 3:00 p.m. to 6:00 a.m. 3:00 if we're going to choose 3:00 p.m. to to yeah, 6:00 a.m. When will you be, guys, be doing the scoring? How much time? So, possibly uh I think you have enough time, right? Because the the the the
[09:15] the window is 3:00 p.m. to
[09:19] 6:00 a.m. and then the following day you're going to score it. You have 6:00 a.m. to 3:00 p.m. to score it. So, I think that's enough,
[09:27] right? So, the reason I I'm like I'm leaning to that the third option, because there's a lot of people uh we want to cater. So, okay, let's do it. Uh we're going to give you the third option. So, going back to uh Lent, I think you need to circle back on the other guys who are asking for for the uh schedule, if it's on a night shift, they're okay to join. So, let's do that. Also circle back on those guys, get their confirmation so that we will have the number of the PM and
[10:00] UI/UX, okay? Based on the initial numbers right now, um do you think it's time, guys, to decide if we're going to merge that one or we're going to separate that one? So, what's the number, Harvey? Uh what's that, Clint?
[10:15] Edward?
[10:17] Uh yeah, it's me. Uh for the UI/UX sir, kay it's only one that is interested to join. Okay, so there are only three three UI/UX, but one
[10:30] one UI/UX wants to be a judge, so I think it will be possible to like a participant na lang siya, so that we have two participants for the UI/UX.
[10:42] Yeah, we can do that one, no? So, there's only two or uh we could um, ah yeah, two pa gihapon, or we can combine it with the other PMs ba?
[10:54] Oh, for the PMs sir, kay I came in at least three responded, but they are not interested, but uh only one says that it really depends on schedule.
[11:05] Mmm, so circle back on that one, give them the schedule that's flexible, 3:00 PM to 6:00 AM, and get your confirmation. Another option, are we limiting um uh those uh contestants to be at the same role?
[11:21] Some might be interested to become a PM, some might be interested to try UI/UX to join, no? So, have that have that survey, maybe you can add more participants.
[11:35] Okay, sir. Uh for all roles, sir?
[11:39] Um yeah. Uh para mag-isa na lang. So, move or be flexible ba. So, who wants to join, I mean, it's not necessary to be a a PM, or it's not necessary to be a a UI/UX. Who wants to join this kind of, be a contestant on this one, we're lacking contestants,
[11:58] and then if you are planning to try out or it's one of your career goals or career kuan, a dream, this is the time, no? So, this is the venue you can try it out with AI empowering you.
[12:12] I think this is the right moment to to to to test that one. There's nothing to, no? There's no uh nothing to lose. So, na- uh let this be an opportunity for for everybody.
[12:24] Basi'g na-a'y uban, cause I know some developers who who who said that, "How can I become a part like like a manager, something like that?" So, okay, okay. Uh we can give them those opportunity uh with this contest.
[12:38] Uh sir, is it okay to utilize the Spartan channel to for those broadcast announcements?
[12:44] Yes, yes. This is aligned with Spartan kuan, so use that one.
[12:47] Okay, sir. Thank you, sir.
[12:50] Mmm, mmm. So, okay. So, yeah, continue, Harvey.
[12:56] So, yeah, uh now let's uh go through uh Clint's initial proposal for the judges and judges. So, yeah, Clint.
[13:09] Hi, everyone. Uh so, these are the uh proposed judging panels, which um me suggested uh model na giingon ni Sir Ed. So, it would be a two uh internal team member,
[13:25] which uh composes the FastTrack team and also a one outside expert. So, I reached out to uh these potential judges, which is on the first, what we have
[13:42] uh either Kyren or uh Sir Dennis. So, I reached out to them and they are willing to serve as a judge, but they still need confirmation since we haven't had uh the official
[13:56] schedule, yeah.
[13:58] And same with uh UI/UX, we have Kara Radovic, which is confirmed by Clint Edward. So, Kara is uh is willing to serve as a judge for UI/UX.
[14:13] And the team member judge for this will be Louise and it'll be uh where am I getting uh For UI/UX, it'll be Josh Ryan Leander, and for QA,
[14:29] we have me and Louise, and for the outside expert, uh we have Mercia Alcos. Uh it still needs confirmation uh for time, same with the other.
[14:46] And also for the dev uh panels for judges, we have Vic and Bernard. So, I reached out to RJ, and uh unfortunately, uh he wanted to be participant,
[15:02] so I have to reach out to another expert for the dev, but if you guys have any suggestions
[15:09] Okay, here's my suggestion for you, Clint. Um if you can convert these uh outside expert into participants, that's fine. Um you can replace them with some senior uh engineers. Uh if try to talk to um try to talk to the engineering managers if some of them can join to to to score this one,
[15:32] no? Just give them a ask for like, "Sir, you only need to score together with us, and with AI that we created, to score uh this one for one hour a day." For example, we have UI/UX, we have PM, we have developer, we have QA.
[15:52] So, if you can get Harvey, Renato, Marisal, Lloyd to be one of those judges in one of those days, that's it. I'll rather convert this outside expert to be as contestant to have more participation.
[16:04] Ah, okay sir. Thank you, sir.
[16:06] Mm, so convince the EM to join one of these, and then arrange them accordingly based on their preference, no? And then, yeah. Uh let's do that one. Go back to the plan, Harvey. I think you mentioned about the the schedules, right? Um we're targeting... Unsa gani to nga petsa, kay?
[16:23] We need to be fast. We're targeting the dates we're targeting November the week of November 2 to November Nova November 6. So, November 2 is holiday. So, we our our window is 3, 4, 5 4, 5, 6, Tuesday, Wednesday, Thursday, Friday. Okay?
[16:44] So, right now, we need to finalize our contestants. We need to decide on the things that we need to decide, no? And then, probably next week, we need to prepare and market this hackathon uh to to the employees.
[17:01] And then, we're going to run Nov- November 3 for the PM, and then Nova November 4 for the UI/UX, November 5 for the developers, and then November 6 for the uh testers. That's my initial uh yeah. Best case here, if we can make it happen at that time, then that's the best case for me. 'Cause the following week, there's going to be another training regarding uh with regards to kuan uh level 3 to level 4 AI Accelerator.
[17:38] So, yeah. Uh Harvey, do you have some items in the spreadsheet that you've shown earlier?
[17:45] Yeah, so uh for the actual client brief, so see we'll we already have initial draft. For this one, yeah, Lawrence?
[17:55] Yeah, uh can you open the document?
[18:00] And so, um we prepared three client brief candidates for the relay launch, and we'd like your uh insights here, sir, on which one to run.
[18:14] So, um all three would follow the same rules. Uh each would be a responsive web app with about five functions and one main flow,
[18:24] and they use dummy data only and have no integrations. Um each would have a few deliberate gaps for the PMs to interpret,
[18:35] and one small curveball for developers, which is given about 90 minutes in. So,
[18:42] Yeah, we are keeping some hidden requirements and scope traps to check uh for each client brief.
[18:50] So, um let's try to go on each. Uh can you go to DeskDay tab?
[18:58] So, so this is the first uh candidate. It's called DeskDay, a hybrid office desk booking. So, it goes like this: so, the client is Anton, a workplace lead with 80 people and 40 desks. Mondays and Wednesdays are a scramble, and people book desks and never show up.
[19:17] So, participants would build a desk booking by day, a check-in, and a rule that releases unclaimed desks at 10:00 AM.
[19:25] So, in the client brief, some tempting extras are uh mentioned: floor plan map, Google Calendar sync, access cards, and parking.
[19:36] And PMs that cut those would be rewarded. And then for the curveball for this client brief is that a certain floor would close on a date, so its bookings are canceled with a notice.
[19:50] So, for this client brief, uh out of the three, it's the lightest build and it has good rules for QA to test. Uh the only weakness
[20:00] where this has no AI on the product and it's close to any capacity booking app. So, yeah, that's candidate number one for our client brief.
[20:11] I have a question regarding that one. You mentioned about the curveball, right? You're going to insert it 90 minutes within the... the when you set the requirements, right? Tama ba?
[20:23] Um, during the dev's time, sir.
[20:27] Dev's time, no? So... so we are providing them, um, 3:00 PM to 6:00 AM. Is it automated? Like, is it an email like first? Uh, if they're... if they're going to get the instruction from the devs, so anytime around 3:00 PM, okay, they're going to click something, send me, they're going to send an instruction. After 30 minutes from that, it's automated, they're going to, uh, receive another instruction, the curveball.
[20:53] Mm, um, we could do that, sir. We haven't really planned, but, uh, I think...
[20:58] Because if we haven't decided... we decided today, right? So, okay lang na. So... so, yeah, think of that one. How are you going to, kuwan, uh, automate the, kuwan, giving the... the material to them?
[21:09] Ah, yes, sir. Yes, sir.
[21:12] And yeah, uh, so for the next one, we have uh Gear Desk. So, this uh it's basically uh we have Joey, an office admin, has a cabinet of shared gear and nobody knows who has the projector.
[21:28] So, our participants will build the catalog with availability, requesting, hand out, return with a condition, and a who-has-what view with overdue items. So, the client brief contains traps like a barcode scanner, Slack reminders, a finance report, and meeting rooms.
[21:46] And the curveball for this is that uh the projector and ring lights are high value, so they need a reason and a one-day limit. So, our QA here would get very clear boundaries such as the last unit, damaged items, and overdue dates. Um,
[22:02] the weakness for this client brief is that it's it would be mostly lists and forms, so it's a bit less visual for our UI/UX participants. So, yeah, that's our candidate number two. And then lastly,
[22:18] um, we have Ask HR. So, this was actually based on what you uh tried to suggest from our uh first meeting, Sir Ed. Uh, it's an HR agent idea,
[22:30] which is kept bounded. So, we have Carla, the HR lead, answers the same policy questions all day. Participants will build an assistant that answers from a fictional handbook and cites the policy
[22:44] and passes sensitive or unknown questions to an HR queue. So, uh, there should be no there will be no vector database or multi-agent setup here. Uh, and a mock mode is the judge path, so scoring never depends on an API key.
[22:56] A working real AI, though, it would earn bonus credit through a fixed set of probe questions. And uh the curveball for this uh client brief is that uh a work from home policy is updated, policy is updated,
[23:09] and the assistant should save the or must reflect uh the updated policy. So, uh the risk for this would be that uh if they were be provided, for sure, an API key, it must stay funded
[23:23] because uh maybe during the time for submission or maybe for demo, they might um have no more usage. Yeah, that's the I think that's the concern for this one. So, uh yes, sir, those are the three candidates so far.
[23:45] Uh, with regards to this one, uh I'll let you guys be the author. You decide. It's a It's a decision you can make. Pili lang mo kung unsa'y inyong ganahan.
[24:06] Um, question, sir. Um, every participant uh should be provided ba with an API key, sir, no?
[24:14] Ah, for participants, e- yes, we should We should do that one, uh, no? Uh, question is, with this application, the same with kuwan, we need to scope how much uh kuwan, no? Uh uh, yeah. How much, uh, tokens needed or or yeah, the OpenRouter credits needed.
[24:39] Maybe we can try to do a dry run for this, sir, if something like that.
[24:47] Yeah, uh do a dry run, create the application, no? The application you chose. I think one of you guys have a have a OpenRouter, no? Pag-ama'a na paday. Paspas ra, so so I'm gonna give you an OpenRouter credits. Check if if it's enough, and then let's see how many kuwan day, how many, um, kuwan, contestants we have.
[25:13] Okay, okay, sir.
[25:14] Um, assuming if we're going to assume like there's going to be 30 contestants, sample lang, 30 contestants times times pila man? Um, no? Roughly, no? Uh, sorry, ha.
[25:48] Do you think maabot og 30? Pila gani atong UI/UX? Pila man ka-12 sang UI/UX, then developer, by pair, tester, naa pud 40, sample lang ha, yes.
[26:12] For two hours, no? Ah, for two to three ah two to three hours of of kuwan. Mm.
[26:33] Sige lang, I'll get that approved, Harve. Um, try sa mao nang kuwan, try to kuwan this one, mock this one. Uh, try it if it's enough for $20, so part of that challenge is limited tokens, uh, find you uh you have to discern what LLMs to use to how uh create skills, use skills that is token kuwan, what you've learned in the trainings. Part na na sa kuwan.
[27:21] Oh, so yeah, for that one, we have another uh last item we had for the Tech and AI Rules. Yeah, uh Ethan, go ahead.
[27:31] So, uh hello. For the Tech and AI Rules, uh let's just uh do it quickly. So, in a glance, uh the tech rules, the output is only a responsive web app, but they still have to provide a GDrive for the AI logs
[27:53] or any md files or documentations they want to uh get get judged. So, the brief says which screen must work on a phone, tablet, or laptop. So, they need to have a responsive web app. And for the stack, we opted to use any stack and any model or any tool, because we don't want to limit the participants or the contestants
[28:28] on what they learned on the AI or AI Accelerator Program. And for the API key, uh this was discussed earlier. Uh, it is decided that Sir Ed will uh provide the API keys, so er- uh before this meeting, we actually discuss if API keys are uh distributed to the participants, but in this tech AI rules, I opt out on allowing the participants to use their personal AI subscriptions as fallback.
[29:03] And if ever the company or the API key will be leaked, it is mentioned here uh the participant will be disqualified, but I think this is too harsh as a punishment. So, I think it's better to revoke the API key and the participant will just use their personal. And...
[29:26] And... So, unsa gani? How about this, guys? Um, check ha. Para fair sila, um, we give them credits, for example, $15. $15 credit, 'cause it's just 3 hours of live coding and and stuff, no?
[29:42] Give them $15 credits, no? If, makita ba nato, if the credits run out, they need to inform us. Every run out, uh, when if they got run out of credits, that's a minus to the total points.
[29:56] So, katong mag- uh, the candidate who can finish that job within that kuan will have this complete points. Na-gets?
[30:06] So, naay kuan, so kuan siya, balanced, 'di ba? Kay basin katong madaog gani katong unlimited credits nga nagamit ug kuan, Vable.
[30:17] Yeah, I'll just uh adjust these rules first, based on what we discussed.
[30:25] And yeah, I think that's all the rules uh mentioned here.
[30:33] Sige, sige, sige, kato, nga limited lang. Mu-tan-aw ko. Uh, I'm looking at $15 to, like, the Agentic AI nga training, they ask just for $15, kay kung sakto kuno mo-set ang tanan mga rules and stuff,
[30:47] dili mo-take ug mahal, no? Sakto ang mga rules, sakto ang mga mga scripts nga ipang-gamit. So, they only pay for $15 for the training for a 3-week training, imagine that one, no? So, mga maayo jud sila.
[30:59] Gamay ra kaayo'g pangayo. So, kani nga training, mga bag-o pa man ni, uh, 15 to 20, I'll I'll check if I can stretch to 20, $20, no? No? Ang ques- ang ako lang challenge ani,
[31:14] um, uh, I have budget for the tawag nato kanang uh prizes, no? Whatever, 'di ko ma-approve-an sa $20 akoang, makuhaan jud nako'ng budget sa prizes. Kay ako man gamiton ang budget sa prizes sa kaning tokens
[31:30] para mo-mo-mo-sponsor sa tokens. I'm hoping ma-approve lang ang katong kuan, ang akong request para ang to- ang budget sa prizes intact lang gihapon.
[31:41] Or I'll negotiate nga, "Gia-half-half lang nako'ng kani among budget sa prizes part of the program, and then I'll sponsor these tokens para nindot atong program."
[31:51] Ana. So, that's uh yeah, just to be transparent to you guys, ha. So, no? So, so kato part of the rules is the the tokens uh token management. Uh 'di sila mahutdan, then i-monitor nato ang token burn, makita sad nato unsay ilang LLM gigamit on that time frame. I have visibility, I have visibility pila sila. Kompleto, naa'y dashboard sa OpenRouter. Makita tanan unsay ilang gigamit. And then within the given time, pila ka actual cost, 'pag molapas, automatic ditso dayon nga, "Ase, lapas na ka." They can continue, but we have deduction already in the points. Question to you guys, pila ang deduction?
[32:28] Butang nato, perfect score is 100, no? No? Then kuan, molapas sya's token. Asa man nga scoring sa rubrics atong kuhaan nimo? Total ba? Specific criteria ba? Pila ma-, asa man nimo i-minus? Pila sad i-minus? So, define that one.
[32:52] Pwede naa'y kuan, sir, kanang separate criteria for token management, and then subtract lang whenever mag-kuan sila or...
[33:01] Mm. Sige. So, for example, katong gipakita ni ni ni kuan, ni Victor nga rubrics, no, naa man didto, no? So, ang token management, ibutang na lang didto. Dili sya, part gihapon sya sa kuan, pero minus sya. Molapas ka's token, minus sya pila, 15, 10, automatic. So, it's not part of the 100, but it's a deduction, penalty. Aron 'di ka mag-usab sa rubrics.
[33:23] So, it's partly challenging also. Uh, ako nakita nga dili kay maigo ani is katong tester, ug kanang kuan, tester ug kanang UI/UX and uh PM. Ang maigo ani, ang developer, kay, you know, daghan man. So, pwede ang developer, ha, let's try initially $20 $20 for developer token, and $15 lang sa the rest. Para dako-dako'g chance ma-approve ang atong peg. Sige, nag-assume ko nga, atoa'ng assumption nato na ha, around 10 ka PM, dili ta kaabot 10, but lesser than 10, around um 10 ka QA mu-appeal, ay yeah, less than gihapon, less than 10 ang UI/UX diay. UX, around 15 ka tester mu-appeal, and then, I don't know, 20 ka developer mu-appeal. I don't know, humot sa kuan nga numbers, ako'ng dreaming nga numbers. So, 65 people.
[34:32] 15 15 15 20 No? So, $1,000 na ayo. Di ba? Okay. Possible, that's around Pila man dollar karon, guys? Naa'y nakatultol na?
[35:46] 63. 63.38 man seguro.
[35:53] 63. 58? Wala na tay price ani? Ambot kay usag kalatas ang ref. Uy, 'di usag. Sige, mag-gamay lang ko'g kuan ana. Ah, sige. Uh, work on your side, I'll work on my side to get this uh kuan. 58.27 training gihapon ni. Uh, eh, eh, eh, eh, eh. So, dili sad ni actual tanan nga, dili ta kaabot ug 10 PM, dili ta kaabot ug 10 UI/UX, no? Ang testers, I'm not sure maabot ba ug 15 pod, ang developers, nuon, kana, impossible maabot ug 20 or I don't know. Sige, that's my problem. So, karon, I'll yeah, we already have some plan, no? Uh, may mga open question nato, kung pila nato ka-bug? Pila ka buok, no? Mga appeal, kay wala ma'y fallback, wa man ta...
[36:52] Oh, yeah. Wala silang rollback since kanang wala pa'y kanang Wala pa'y ingnan sa schedule. Okay, so ani na lang. Ang atong readiness karon dili pa jud 100% ready na tanan, naa pa tay pamaliton. So, naa tay duha ka schedule na lang. First schedule uh good to have November 3, 4, 5, 6. Inform the candidates about that one. Second schedule nato,
[37:13] no? Is kanang kuan 10, 11, 12, 13. That's our second schedule, no? No? Um Best case, we really need to do it in 3, 4, 5, 6 kay maigo na katong next program nato if muabot pod ta'g 10, 11, 12, 13. But inform katong mga members nga maglisod og apil nga naa na'y mga possibility nga schedules, mm. Mao 'ning first schedule i-gipass, no? And then,
[37:42] kanat ron, I'll let you guys decide inyong readiness base sa atong mga action items karon. Kung moingon man pod mo nga "Sir, pag-ugma or Lunes, Sir, murag ready na jud ta, Sir. Murag naa na'y nag-register diri. Nya ang atong gi-swayan ang kuan, Sir, ang ang katong application nga gi-na-pili nga application. Wala pa ta kapili sa application. Unsa'y ta-himo, which is kanang Ethan ba to? Imohan to Ethan?"
[38:06] Uh, Aliander.
[38:07] Aliander. So, Aliander, isettle pod ninyo. Unsa'y inyong ipahimo ato. Testingan pod ninyo and then padagan- gamiton pod ninyo ang katong skills ni ni Victor, nya plus with human, no? So, makasulay mo ah, see, okay ra, madala, no? And then, also, kisa ba to'y moduol sa EMs? Manghinay sa EMs. Kana. Onsa pa'y na-bilin? Wala pa na-decide-an.
[38:31] Uh, I think kay Clint, word
[38:34] Ah, Clint, main.
[38:36] Ah, yeah. Siya'y kuan sad.
[38:39] Mmm. Sige. So, mubalik ko ninyo seguro or balik ko, Harvey, sa status ana mga action items nato. Ug ma- day-to-day, day-to-day. I will let you guys decide nga, "Sir, let's go with November 3 to 6. Kaya!"
[38:52] No? Day-to-day, ha, day-to-day decision. Or ingon mo "Dili man kaya, Sir. Pwerteng ipit kaayo, Sir. Wala pa mi nakatestingan. Wala pa mi- Dili pa jud, Sir. Mura'g ma-law-awan tanan, Sir." And then, let's go for the next week. Mm.
[39:08] So, yeah. Mao lang 'tong i-work nato nga mga action items karon, Sir. And then, we'll update you day-to-day, no?
[39:14] Mm. Day-to-day ta mag-decide. Padhaba i-chat ta, Harvey, nya kamoy decide with the team. Mm. Unsa pa to'y lain wa nako, basin naay nkalimtan sa katong mga open items.
[39:23] I think wala na, Sir.
[39:25] So, guys, naa pa mo'y any action items?
[39:29] Yeah, non- non- non- non- non on my end.
[39:34] Yeah, so we'll just communicate with you na lang, Sir Ed, if if
[39:41] Sir, uh I have a kuan, Sir, ba. Is it better to be 2nd week sa November? Kay I think November first week is like kalag-kalag. Some might have a like nag-PDU or like that, some cases, Sir, ba.
[39:58] Katong, ang akong ang akong past
[40:00] Kial sunod, kinsay Marycel? Marycel, kumusta man 'to sunod nga program? Naa pa ba 'to TBIC?
[40:05] Yes, sir. Ah, unsa 'to katong ah
[40:09] accelerator ba? Accelerator, oo, 'di ba? We are planning to have 4 weeks, and then kung ma-delay ta, katong mga tao na-assigned didto,
[40:20] ang risk nato nga mawa sila, unya na magdagan ka, taas na pud. Sa bagay, kung December na, wala na siguro'y bag-ong client ning December 7, kuya, no? 7 to 11.
[40:32] Mm-mm. I think mo- Akoa lang sa i-coordinate ana, sir, kung unsa'y plan nila if, um, they will still continue to assist us, especially sa kuan lang,
[40:43] baka they are willing to assist us while they have client or ako lang i-ask sila, sir, about ana.
[40:49] Sige. Sige, sige. So, if if happen in November second week ta, ang imohang program nimo 16 mag-sugod, mo-end og December 11.
[41:01] Yes, sir. So, if ever mag-start ta'g second week, sir, for the Hackathon, um, sa November 4, naa gihapon ta'y session, masterclass ana.
[41:15] Mura'g ana lang. Kuan...
