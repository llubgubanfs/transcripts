---
title: "Team direction call with Sir Lloyd and Miss Marissa"
date: 2026-10-20
type: meeting
tags: [meeting, growth-portal, management, badges, sprint, leyo, performance-review, growth-framework]
participants: [Lloyd, Marissa, Harvey, Jhos, Victor]
source: "/home/yander/Videos/dsm/[9am call with sir lloyd and miss marissa]2026-10-20 09-05-19.mp4"
transcriber: gemini
saved: 2026-10-20T12:09:02
---

# Team direction call with Sir Lloyd and Miss Marissa

## Executive summary

**TL;DR**
- Team management changes: Miss Marissa now manages the team day to day (tasks, leave/PTO); Harvey stays in charge of the technical side; Victor remains primary PR reviewer [00:54, 02:38, 20:30].
- New intake rule: only bugs and showstoppers get immediate action; every other request is logged in the backlog and prioritized at the weekly sync [03:38–04:15].
- Badge admin CRUD (simple, built with AI) goes ahead now, ahead of the badge additions [07:54, 13:02, 15:02].
- Sprints become one week long, matching the weekly presentation to Matt [28:33].

**Decisions**
- Marissa takes over the day-to-day management; manager records and leave requests move to her. Sir Lloyd will change the manager records after talking to Marissa about the one-on-ones [02:38–03:27].
- Incoming requests are logged in the backlog and prioritized at the weekly sync. Requesters state urgency and give a short scenario. Delivery path: staging, guide or quick video, chase feedback, ship [00:11–05:54].
- Badges: build an admin CRUD instead of editing the database or sending HTTP requests by hand. Proceed without waiting for Harvey's CSM check. Badge additions follow, and are not urgent [07:54, 13:02, 14:56–15:07].
- Performance-review one-on-ones: a full review is deferred to Q4. If nobody raises a concern by Wednesday, Sir Lloyd confirms none are needed and the review criteria proceed [15:24–17:12].
- Leyo chatbot is paused and its server is deactivated; the growth framework embedded in the portal is the next big effort, probably last week of October [18:00–19:34].
- Sprints run one week [28:33].
- Bug fixes that fix something broken need no approval; feature improvements must go through Marissa and are only built with manager or executive approval [32:36–33:40].

**Action items**
- [ ] Harvey: clean up the Growth Portal board: move leftover tickets to the backlog and start Sprint 61 [27:21–31:24]
- [ ] Jhos / team: build the badge admin CRUD first, then the badge additions (AI leveling and the other request) [12:40–15:07]
- [ ] Harvey: list of names for AI/API keys, to be sent to Sir Ed (Full Scale emails) [12:08–12:28]
- [ ] Harvey: follow-up Hackathon session with Sir Ed, targeting the first week of November [09:00–10:51]
- [ ] Team: build a demo, approval and shipment cycle for the badge request [26:40–26:52]
- [ ] Team: set the sync-up and sprint cadence; Marissa leads, fewer than 5 priorities per week [06:27, 17:15–17:44]
- [ ] Team: find and file Growth Portal bugs when idle [23:04–23:53]
- [ ] Team: performance-review edit ticket: add simple logs or limit edit attempts, no complex workflow [24:12–25:15]
- [ ] Sir Lloyd: relay these updates to Victor [19:58]
- [ ] Sir Lloyd: change the manager records to Marissa [02:38–03:27]

**Blockers / risks**
- Stakeholder feedback is the usual bottleneck, so chase it right away [05:23].
- No AI tool or OpenRouter API key yet for this group; the Claude team subscription exempts RAX [11:15–12:31].
- The board looked empty because Sprint 61 hasn't started, and its old tickets need cleanup [27:08–27:53].
- Sir Lloyd would rather automate code review than rely on a costly reviewer long-term [08:31].

**Open questions**
- Sprint cadence was left to Marissa and the team [06:27].
- Who gets AI tools and API keys, and when (Sir Ed to provide them) [12:08].
- Exact date to change the manager records (Sir Lloyd said "March", probably a mishearing) [02:50].
- Transcript terms that Gemini may have misheard: "CRUD L" (likely "CRUD"), "PAI acceleration program", and the chatbot name (Leyo / Leo / Leyo.ai).

## Transcript

[00:00] ...is a urgent matter that needs to be taken action, 'no? Na dili na siya need to wait for another week or next week to do it. So know that,
[00:11] identify, for example, kung naay request ninyo o feature, identify gyud, when do you need this? Is this blocking you? Is this something nga very urgent to you?
[00:26] And then i-butang sad ninyo iyahang gravity sa ilahang request, if it is really of high priority, o 'nya estimation nila kanus-a nila need ni siya nga feature.
[00:39] So mao na siya. And then we get the details. Most ang details doesn't need to be very detailed, 'no? Kanang kuan lang gihapon, murag overview, maybe i-scenario, 'no, of that request.
[00:54] So that sa sync up meeting nato sa weekly, we will have to identify that. And then we will promote that if this is going to be part of our pipeline or later pa na siya, and so forth.
[01:12] Alright. Is that something clear to the team? Alright. So, unsa pa?
[01:23] So, other than that, naa pa moy commitment sa other item ni Harvey?
[01:34] Sa karon, sir, is wala pa. Ang gi-focus-an nako karon na week kay katong concern ni kuwan, Ms. Marissa. Katong performance review na improvement.
[01:44] Ah, okay. Yeah, so I think that's the part, item nato nga buhaton. So, still same, 'no? Si Victor gihapon ang mo-review
[01:52] and then Ms. Marissa will be assuming, manage sa inyong team, 'no? Sa atoang team, Harvey. And then anything nga i-escalate nato, we need to decide something, then that's the time
[02:08] we'll talk over with Marissa and even include you, or Victor, or other subject matter, 'no, nga i-include nato, like for example, ang nag-develop kay si Louise. So we will include Louise in the topic for that item, for that task, if he needs to
[02:24] to decide something on it. Okay? That's one. What else?
[02:38] So now, the kuan diay, so any leave ninyo, moving forward, i-change na nato siya towards Marissa na. So anything na inyohang request for leave,
[02:50] Marissa will handle all the day-to-day ninyo nga task and even inyohang PTOs, and so forth. And currently karon, naa man sa akoa, so I think we have to change that March, 'no? Kung when, kanus-a na siya.
[03:07] Ako na ani i-change ang manager diri, sir?
[03:18] Yeah, i-change tanan, tanan nilang manager, pero hold on, ha, kay murag mo-review para ba kuwan, one-on-one ani nila.
[03:25] Ah, okay. Later na lang.
[03:27] So, after ani nga call, I'll talk to them about sa kuan, 'no, sa one-on-one. And the performance review, para lain. So, karon, 'no, that's the new direction nato.
[03:38] So, ang technical side, we own it. We are going to own it. So, anything request from different areas, like it could be coming from Harvey, not only Harvey, but also kang Ed, sa HR,
[03:48] operations, CSM, etc. We will have to collect that, but don't act on it unless it is really a bug or a showstopper sa atoang application.
[04:00] You log it sa backlog. And then, if it needs to prioritize, you right away inform us that we have to talk about it, and then we'll see if it is really
[04:15] kanang need to be work on, like i-sulod dayon sa atoang pipeline. Other than that, we'll have to do a weekly sync up to prioritize, organize what needs to be done, what needs to be added into Growth Portal.
[04:29] So, as soon as we have that feature, like for example, gisulti ni Harvey, 'no, "I have I want to have this feature," and then we agree nga we will do this. Ang atoang buhaton is that we will develop it, of course, and then we will deploy that to the staging,
[04:47] and then we will probably give that stakeholder, that customer, we will treat them as customer, we will provide them a guide how to actually review it and test it. So, it could be coming from a text, 'no, with a detailed process, procedure, 'no, how to do it, how to
[05:08] how to arrive to that feature or bug fixes. Or we could also share a quick video recording. I think quick recording will be very easy, and then we submit it to them.
[05:23] And then once we submit it to them, we will have to ask them, "Is this what you need? Do you have any feedback?" We have to actually, you know, follow up them. Kay ngano? This is going to be always the bottleneck, 'no? Ang feedback nila dugay jud kaayo sila mo-feedback. So, as much as possible, kuhaon jud ninyo dayon ang feedback nila.
[05:40] Once they have the we have the feedback, if it needs to be updated, etc. etc., or ipa-check pa jud nato balik, if it is that big, mobalik sa atoa sa video, pa-record, pa-review. Once they approve it, then that's the time we ship it.
[05:54] Alright? Questions with that kanang process?
[06:23] Yeah, oo, sir.
[06:25] Sige.
[06:27] Kuan, sir, na-define na ba ang duration sa atong sprints?
[06:29] With that said, I think we'll leave that with Marissa, 'no, kung how she will do that. So, you talk to as the team, 'no, to handle that kung unsa. But that's actually what I expect. That is what the goal is for this team,
[06:47] and expectation pod sa team. So, whatever you do it, unsa inyohang cadence to do this, you do it at your own, you know, at your own side, 'no, to discuss that further. And then agree and disagree on what needs to be
[07:00] the process you will have. Alright, other question? Okay, all good na? So,
[07:18] yeah, I think, unsa pa may lain? Before I forget.
[07:34] Sir, ang database na access ani nila is kinsay nag-hold? Ikaw, sir, or si Sir Harvey?
[07:44] Akoay nag-hold sa database. Naa sa AWS.
[07:52] Awn, awn. Oo.
[07:54] Can I request atong badge, pero kuan, 'no, himuan lang siya ug admin UI for that, ah?
[07:58] Yeah, I don't think that's ideal, 'no, to do a kuan ba, to HTTP request to handle that. Kay ang badge man gud, that might change, add, you know, increase as we go along. So, why not add it? So, I think that's going to be just a simple CRUD L,
[08:14] simple lang, ayaw lang kayo i-complicate. Use AI mo, ha? Kanang, most of the time. If also, if what what are your tools nga need ninyo, raise that up and then we will discuss it kung unsa'y maayong buhaton diha. So,
[08:31] Alright, still the same, ha, si Victor will also have to do the code review. And then, I would suggest to create those kanang code reviewer, 'no, nga dili sad siya mo, you know, in a sense nga costly siya in the long term, ba. So, find a way how we can how we can do and automate the code review.
[08:48] And also, yeah, I forget. Kanang, unsa'y kuan nato sa kuan, need nato nga action, Harvey, sa sa unsa ni, sa Hackathon?
[09:00] Currently, sir, is ga-work pa ko sa action items ni Sir Ed sa previous kuan nato, sync up. So, probably, later this week, kay maka-create me ug another schedule for follow-up na kuan na session.
[09:16] Oh yeah. Unsa'y details didto? Do you need me, or do you need if if makaya ra sa inyo ha, makaya ra ninyo?
[09:25] Yeah, sir. For now, sir, is kanang ma-handle na namo, since ga-kuan pa mi, ga-collect pa mi sa individual na item. So, if ever na need...
[10:00] ug unsa iyang, sir, i-small approach lang gihapon ni minyo. Kong unsa iyang thoughts, no?
[10:04] Oh, yeah. Um, so I think I can do this nga part, Marisa, no? Kay murag kuan man 'ni siya, kanang ad hoc nga...
[10:13] yeah
[10:14] effort, oh.
[10:15] I-kaila lang na, sir, uh...
[10:16] Ako lang gani, ha. So sa day-to-day operation, Marisa will be assuming the management team, ha? So, be good, no, Marisa?
[10:27] So, sa kuan pud na sir, kay before mi mo-set up og another session with Sir Ed, kanang pwede amo sa siya i-kuan nimo? I-consult nimo?
[10:37] Yeah. Yeah. Yeah, pero ayaw pod dugaya, Harvey, kay I think ang atong target is...
[10:41] dapat unta mid of this week, I mean mid of this month na unta to, pero I think ma-move na nato to November.
[10:51] First week of November, pero kanang kuan lang, action-i lang to ninyo. If if if possible, sayo-sayo this week ma-kuan na nato, ma...
[11:02] you know, ma-process na ba.
[11:05] Yes, sir.
[11:06] All right. Um, so unsa pa man? Mao na to akoang item.
[11:15] So, kuan pud na, sir, kanang regarding gani sa AI tool, sir? So, kinsa ba'y i-map-force ana, sir, or sa among own nga kuan among gamiton?
[11:24] Um, I think mag-discuss lang si Marisa sa kuan, sa internal tools, kay I think sa RAX, naa may account.
[11:36] So, later on, unsaon na siya pag-handle. Wala, siguro... nakalimot ako giunsa ninyo, Mars, no, sa kuan, sa RAX?
[11:46] Uh, naa mi Claude subscriptions, or team subscription, but kuan man pod siya, kanang exempted ang RAX to use that one.
[11:55] But for this group, I think OpenRouter, wala man gani tagaan pa og OpenRouter nga API key.
[12:03] So, katong kanang kuan, Miss, PAI nga acceleration program?
[12:08] Uh, we should be providing you guys. So, give me a list of names lang, Harv.
[12:14] Yes, Miss.
[12:16] Para atong i-send ni Sir Ed. Sir Ed will give us the API keys.
[12:23] Ang full scale email ba, Miss?
[12:25] Oo, full scale email.
[12:28] Sige, sige.
[12:31] All right. Question pa, um, guys?
[12:38] Uh, Jhos, sige, Jhos.
[12:40] Uh, going back sa katong badge, sir. So, since we'll be proceeding with the CRUD implementation,
[12:47] does that mean uh I will just defer the uh badge addition request, katong uh AI leveling and katong
[12:58] uh atong duha ka request nila, sir?
[13:02] Um, if ma-mabuhat nimo ang CRUD L uh the soonest, then i-add dayon nato ang badge.
[13:12] So, ang priority ana, di man kay na siya kuan gyud, di man kay na siya urgent.
[13:18] So, kuan lang, kanang unaha lang sa ang katong CRUD L.
[13:23] Yeah, regarding pud ana, sir, ga- ang one of our kanang team member is ga-propose na na ka Sir Harvey.
[13:29] Sa katong UI for CRUD, giingnan si Sir Harvey na kanang mo- mo-iya pa daw ipangutana sa uban CSMs
[13:37] regarding sa atong UI sa CRUD for badges.
[13:41] Yeah. So, so ing-ana nga approach gani, kuan, naa gani ing-ana nga issue or ing-ana nga request,
[13:48] i-identify ninyo nga is it something nga mag-segic-recurr?
[13:53] Or is it safe? Is it is it good? Is it is it creating delay, no, to to add, even just to add like kanang a new item for badge, too?
[14:03] So, which is actually is the case nga mo-himo gyud siya og bottleneck.
[14:08] And then, creating that manually is also a problem kay if if as much as possible, we don't have to access the database directly
[14:16] and add that and update or etc., or even adding that via e- kuan, no, HTTP request,
[14:23] kay it's not ideal. So, if it is kanang something nga moving forward,
[14:29] the badge will always be there, badge will update, will evolve, then we'll have to add a management to that.
[14:38] Yeah. I think I don't think that's going to be a big kanang kanang kanang effort, no?
[14:47] Uh, utilize AI, and AI will help us out uh doing the CRUD L for that easily. Yeah.
[14:56] Kanang, should we proceed na ba sa katong CRUD implementation ato, sir, or mag-wait pa mi sa kuan ni Sir Harvey?
[15:02] Uh, dili. Proceed na ta. Proceed na ta sa CRUD L, ha.
[15:07] Sige, sir.
[15:08] Yeah.
[15:11] Uh, other, other item? Harvey, uh...
[15:16] Ang one-on-one day nato, so going back to the one-on-one, you have already reviewed the kuan, no, the feedback that I have.
[15:24] So, um, to streamline this, but I know this is... I know we have only been working for about 2 to 3 weeks, maybe a month.
[15:35] So, dili gyud kay siya ing-ana kadako gyud og kuan ba.
[15:40] So, I think it's safer to to do the to do the review maybe full ba in para fair sa tanan in the 4th quarter na gyud.
[15:50] But right now, for formality sake, uh based on my review sa inyoha team,
[15:55] do you have any concern? Are there any items nga
[16:00] uh you are not uh satisfied?
[16:04] Uh let me know directly, ping me, and then we will discuss it one-on-one.
[16:08] Other than that, if wala koy ma- ma- ma-madungog nga
[16:13] raise of concern of the one-on-one,
[16:16] um maybe by tomorrow,
[16:18] I'll assume that everyone is good with the criteria, and I will
[16:23] uh confirm that uh no need to have one-on-one, we can we can
[16:28] uh we can uh go ahead and move forward with the performance uh review that we had.
[16:38] Sounds good ba na sa tanan? Or, yeah, if you have gyud nga something to talk to me, you raise to something,
[16:45] uh please reach out to me, no, directly, and then we'll talk about it.
[16:50] There's no kuan, hey, there's no judgment. We'll have to talk, and if you need guidance, let me know, and then we'll talk, talk over also.
[17:01] All right? So, Wednesday, if wala, I'll I'll continue I'll kuan to, I'll
[17:07] I'll automatically confirm that no need for one-on-one.
[17:12] All right? Sige. So,
[17:15] that's good. Um, so I think you you also have to kuan, no? You also have to
[17:22] uh create a a schedule siguro kung kanus-a mo mag-
[17:27] mag-sync up meeting, and maybe around I may be there,
[17:32] but Marisa will take charge to that, and then prioritize lang nato. As much as possible, if we can just have
[17:38] kanang less than 5 items nga makakita ta nga priority for this week,
[17:44] we do that. We don't have to add so much in our plate.
[17:49] As much as possible, kung naa tay puyde'ng walay buhaton, mas maayo.
[17:53] We'll just have to focus on what is the the next thing to have with our uh GP.
[18:00] And by the way, also just to give you a heads up,
[18:03] we will be pausing, no, ni Leyo as our chatbot.
[18:08] So, we will pause that, and then uh wait for the
[18:13] wait for the uh next step to to do on the growth framework uh implementation.
[18:23] So, as soon as that uh mao na'y pinakadako nato nga effort, no? Ang growth framework nga i-embed nato sa growth portal.
[18:31] Which will probably be happening maybe, you know,
[18:35] last week, maybe, you know, last week of of this month.
[18:40] But uh we'll see. We'll we'll give you a heads up on that.
[18:47] All right. So, think of any any future feature nga valuable to the team,
[18:52] to the people, and uh, you know, still continue um researching and, of course,
[18:59] um learn, continuous learning gyud na.
[19:04] All right?
[19:07] Uh, Jhos, sige, Jhos.
[19:10] Uh, related to Leyo.ai, sir, um there's actually
[19:14] a bug. Uh, I think it's only reproducible on my account,
[19:19] because when I log in using my full scale email, lahi nga profile ang mogawas, sir.
[19:25] Ah, yeah. That's a placeholder ra man pod na siya, Jhos.
[19:30] So, don't worry about kuan, Leyo, for now. We'll We'll have to park it.
[19:34] So, right now, I deactivated the the server. So, but uh later on, if we really need that, we can easily uh spawn it.
[19:45] Okay?
[19:47] All right. Uh,
[19:51] yeah, what else? Unsa pa man? Uh, naa na si Victor?
[19:56] Wala pa, sir.
[19:58] So, relay this
[20:00] ako kuan ha, with Victor.
[20:01] Yes, sir.
[20:02] And then that's it. Mars, do you have something to say?
[20:07] Yeah, maybe I will kuan set, sir, kuan stay with them and just give them some guidance lang.
[20:16] Sige, I'll go ahead na. So guys, thank you and until our next sync-up meeting. Thank you, guys.
[20:24] Yep, thank you, sir.
[20:25] All right. Thank you, sir.
[20:27] Thank you, sir.
[20:30] Sige, hello. So that's officially kuan, no? Ka-nang
[20:37] saying that I would be managing you guys. And for any... I think mag-meet ba gyud mo regularly with Sir Harvey?
[20:48] Or kuan lang sya, ad hoc lang na meeting?
[20:51] Every week, kuan, once a week ra, Miss, kay Sir Harvey.
[20:56] Okay, so I think ma-kuan na na sya, ma... it will be kuan siguro, stop starting this week because of our new direction.
[21:09] But, so let's set some expectations.
[21:13] Okay, so again, Harvey would be managing you guys, no? For the technical... So how does technical review happen, man?
[21:25] Have you gone through that or how do you do the technical review with
[21:33] Victor, right?
[21:36] Ah yes, Miss. Currently, kay si Victor among primary na reviewer, PR.
[21:45] Ah, pero naka-kuan na gyud, you're able to do that cycle with Victor.
[21:51] Ah yes, Miss. For sa past tickets, yeah, si Victor.
[21:58] Okay, so the... your standup is kuan, no? 1:30 to
[22:04] 1:30.
[22:05] Yes, Miss, 1:30 PM.
[22:09] So I will... I might be kuan, joining you maybe Monday or Wednesday,
[22:17] or it could be Thursday. Basta murag twice a week lang ko mo-meet ninyo, anytime during or any day during your standup meeting. But the Wednesday and Thursday I need to be there kay
[22:32] we need to report something man to Matt.
[22:37] But if kuan lang, wala kayo tay dako nga ticket to report to him, but at least I know your kuan, ka-nang, your assignments, no? Daily assignments.
[22:53] Now, since Growth doesn't have much request man, except for this week lang, katong mga request.
[23:04] If one of you murag you feel na
[23:08] na-bored na mo sa research if naay gi-pa-research sa inyo, then I would suggest na find some bugs that you can fix sa Growth because
[23:22] when we kuan, when we... unsa na? Ang nindot na product is even if mga gagmay nga bugs niana, you're able to catch it and fix it,
[23:35] naa na syay ma-accumulate na sya, no? And that would compound na whenever user use Growth,
[23:42] kuan gi-sya, ka-nang, bugs-free, and that means nindot sya gamiton.
[23:48] So, I would encourage everyone, if wala pa moy task,
[23:53] kuan, if you found a bugs in Growth, file a ticket, then you can discuss with the team na this is the bug that I saw, I will work on this one, and
[24:05] So, ka-na. And then, ang i-prioritize lang ninyo ang kato lang jung mga feature requests.
[24:12] So, performance review nga edit. But I'm also thinking, by the way,
[24:18] don't be just ka-nang ticket grabbers. You need to think of the business logic behind the ticket, for example, katong mag-edit sya sa performance review.
[24:31] We... I'm thinking na dapat butangan siguro sya'g ka-nang... I'm not sure if history ba gyud, pero I don't want to complicate things.
[24:43] Kuan siguro, ka-nang, murag logs ba nga nag-edit sya aning nga time or kaning nga day, ka-na or kapila sya nag-edit, something.
[24:54] You can think of kuan lang siguro, unsa'y better approach to that, but somehow sa ako-ang side I want it to have some logs, but simple lang, don't make complicated na mga workflow, ha?
[25:10] Okay, logs or maybe a limitation and edit attempts.
[25:15] Yeah, pwede ra. But again, kuan lang siguro, work as a team, no? Think as a team on what's the best thing to do, but don't complicate things, ka-na lang.
[25:28] So kato, performance review...
[25:32] The other one is... Ah, yeah. Still performance review, but ang assignment, kato very kuan na sya ha, very
[25:41] critical na sya or a request na need sya sa management, ang katong correct assignment of the members. So, that's one.
[25:55] And then, ang kaining process ninyo nga demo, approval, shipment,
[26:03] were you able to have that cycle already?
[26:06] Or...
[26:08] O, wala pa man'g major feature.
[26:10] Currently, Miss...
[26:12] Ah, yeah.
[26:14] Pag internal, Miss, but during sa...
[26:18] Mm, kay currently karon, Miss, kay
[26:21] ang among na-kuan na work kay mostly bugs pa.
[26:28] So wala moy demo?
[26:30] So karon kay wala pa, Miss.
[26:33] Sige.
[26:34] Since wala pa may ka-nang dako gyud na feature na gi-push through.
[26:40] Mmm. So ka-nang inyong buhaton, katong gi-request nako o kaning sa badge,
[26:46] ah I think naa na syay demo dapat, no?
[26:49] Oh, yes, Miss. Dapat naa gyud na.
[26:52] Mmm. By the way, para mapaspas mo, wala diay moy kuan, wala diay moy AI tool?
[26:59] Ah tagai lang ko'g list kay it would help us really speed up things kani syang mga request nila ba.
[27:08] Nya ah ang pag... ang pag-create ug mga tickets ba, I'm seeing that Growth portal empty iyang board. Is this correct?
[27:21] Yes, Miss, kay wala pa gi-start ang sprint.
[27:26] And and then need pud sya...
[27:29] Ang gi-instruct sa amo-a ni Sir Harvey ato, Miss, katong mga tickets na bug fixing kay i-create sa sya sa
[27:37] backlog and then i-move dira sa
[27:42] pinaka-una if priority sya or gi-work-an na sya.
[27:47] Ang kaning Sprint 61 kay wala pa man sya gi-start, Miss, so mahong dili makita sya sa board.
[27:53] Can we start now?
[27:55] Na, I think, Miss, kay need pa syang i-clean up, Miss, ka-nang mga tickets dira kay pag-abot nako, Miss, naa na na sya'y
[28:02] mga existing tickets. Ana.
[28:06] Ah. What we can... Diani na lang, I will... How who will start the sprint diay?
[28:14] Pwede man ni nato sya ipang-move sila tanan dayon i-
[28:20] clean up the board na lang siguro. I think you can... Maka-click ba ka'g start, Harv?
[28:26] Wala pa so far kasuway ug click ug start, Miss, pero I think clickable man sya sa akong end.
[28:33] Okay, we can actually do this start sprint. We'll have the one week duration lang kay every week we have a presentation or kuan man, a discussion with Matt, so at least
[28:47] naa tay e-aim nga
[28:50] kuan,
[28:51] naa tay ma-present ni Matt. Now, for the tickets na dili... wala syay labot siguro, like create structured employee 1-on-1 notes in Growth,
[29:02] you can just remove that
[29:05] sprint here, I think this will kuan, automatic na sya'g move to
[29:18] Let's see if it moves.
[29:21] Out.
[29:26] What was the ticket?
[29:31] Ana, wala sya diri, so asa man to sya nabutang?
[29:36] Naa sya sa backlog.
[29:41] Let's try again.
[29:44] Ah,
[29:47] kaning mga bugs, unsa man ning mga bugs?
[29:55] Career growth grad for expectation. Unsa ni? AI
[30:02] Kani pod diay pod diay na feature na gi-differ, Miss, ni Sir Harvey.
[30:08] Sige, ato na sya i-remove. Unsa ni 62 272? Let's see where it goes.
[30:16] 272?
[30:19] Kani backlog.
[30:26] 61, it goes to 61. What is the current sprint?
[30:35] 61...
[30:39] Ah, 61 na diay sub...
[30:45] Ngano man nawala?
[30:51] Ah, nawala sya's board, but it shows up here.
[30:58] 272 man no? 270...
[31:01] Need ra i-refresh, Miss. Naa na sa backlog overall.
[31:04] Ah, okay. So, kana na lang buhaton, Harvs. You clean up lang.
[31:09] Remove the current sprint, so it doesn't... it goes to backlog, para ma-clean up ni sya tanan diri so that, and every week, we're gonna complete this sprint, ana. Limpyohan nato, okay?
[31:24] Yes, Miss.
[31:28] And then, on week sprint, bug fixing, yeah, find kwan, you play around with with per kwan with growth portal. Kay naa sad koy actually issue, but I will raise siguro after na lang sa some of your tasks or maybe next week, kay
[31:48] there are some instances nga dili ko... ah, wala ko kadawat ug performance review sa certain employee, but I just did it sa Rocks, kay it was not showing up on my board. So, but later na lang to sya. And then...
[32:04] I think na-fix na to sya, Miss.
[32:07] Ah, na-fix na to sya. Sige. Sige, i-show ang kapa unwork.
[32:12] Sige, kana lang. Any questions?
[32:18] Ah, hello, Miss. Ah, question lang, Miss, ba na...
[32:22] As we explore Growth, Miss, and then ah dili ra bug ang makita, Miss, if makita mi ganang ah improvement gani sya for like a feature improvement, Miss,
[32:33] Mmm.
[32:34] can we still create ticket for that, Miss?
[32:36] Yeah, I would encourage you to kwan siguro, and not... ah not sure with a tick- pwede ra ticket, but you need to raise those type of tickets to me before you implement that. Kay I need also to consult with the manager if that's a good to go,
[32:56] or it's a worth of our time, of our tokens to implement that. But I would encourage you guys to kwan, find ways lang pud to anang... ah improve growth, ana. Okay ra kwan, good ra ko. But don't in- kwan pod ha, do not implement unless the manager approves or the executive approves that feature. But for bug fixes lang gyud sya nga issue gyud sya, error gyud sya,
[33:22] if we will not fix it kay wala, guba gyud. Ang dili sya ka- kwan, move sa workflow, then you don't have... you don't need my permission.
[33:40] Sige, Miss.
[33:43] Uh-hum. Kay sayang sad kayo, no, na inyong brain cells dapat atong gamiton.
[33:51] So, kana. Those are my expectations. And again, um I I might be joining you guys, no, Monday, Wednesday, or Thursday. It depends. But um kwan lang, ah continue your cadence and
[34:07] inform me if naa'y mga critical issues or or things na you need to escalate.
[34:19] Okay.
[34:23] Sige. Ah, thank you!
[34:27] Thank you, Miss.
[34:29] Thank you, Miss.
[34:30] Thank you, Miss.
[34:31] Thank you.
[34:32] Thank you.
[34:33] Thank you, Miss.
[34:35] Bye-bye.
