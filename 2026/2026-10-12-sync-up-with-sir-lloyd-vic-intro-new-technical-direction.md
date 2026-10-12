---
title: "Sync-up with Sir Lloyd – Vic intro, new technical direction"
date: 2026-10-12
type: meeting
tags: [meeting, growth-portal, leo, growth-framework, code-review, hackathon, gp-259, gp-261, gp-262, gp-263]
participants: [Lloyd, Victor, Harvey, Ethan, Bernard, Clint, Laurence, Kentward, Louise]
source: "~/Videos/dsm/[sync up meeting sir lloyd] screenrecording-2026-10-12_10-35-08.mp4"
transcriber: gemini
saved: 2026-10-12T11:57:08
---

# Sync-up with Sir Lloyd – Vic intro, new technical direction

## Executive summary

**TL;DR**
- Sir Lloyd introduced Victor (Vic), a seasoned .NET engineer, as the new technical lead for the Growth Portal team. Vic takes over all code review and approval, technical direction, and joins the daily stand-up [06:05–07:35].
- Context: Growth Portal moved from MS SQL to Postgres. It is being adapted for the new Growth Framework (employee upskilling) and LEO, a growth-coach chatbot that reads the user's level and roadmap from Growth Portal staging [00:47–05:40].
- Code reviews were the team's main blocker (floating PRs waiting on Harvey). Vic will review manually now; a Claude/GitHub code-reviewer agent is to be planned, but GitHub seats are limited to 2 [20:00–22:21, 25:05].
- LEO prototype is handed to the team (with Harvey) to continue; review set for Thursday afternoon [24:15–24:35].

**Decisions**
- Vic does all code review/approval and technical direction; included in all stand-ups [06:51–07:35].
- Big new projects and feature requests are parked and validated for ROI before entering the pipeline. Bug fixes can go ahead [09:23–11:29]. Goal: avoid new work in Growth Portal unless the impact is large.
- Growth Framework details (competencies, collaboration, technical requirements) come from Harvey, who also checks that LEO, Growth Portal and Growth Framework stay aligned [12:14–12:49].
- LEO reads from Growth Framework settings in Growth Portal; the team continues the prototype [23:45–24:35].

**Action items**
- [ ] Harvey: schedule a meeting with Ed (and Igor) for requirements gathering and the hackathon playbook, "maybe tomorrow"; include Sir Lloyd in the invite [08:45–10:31].
- [ ] Team: collect requirements from Ed and Igor; plan big projects as a breakdown/sprint plan before building [09:23–10:11].
- [ ] Team/Harvey: plan a code-reviewer agent (Claude GitHub plugin) and decide who runs it as a side project [20:00–20:26].
- [ ] Harvey: coordinate GitHub/Claude seats (only 2 left) and subscriptions Vic may need [21:26–22:21].
- [ ] Clint: ask Harvey to add Vic to the repo and the team channel; Sir Lloyd will follow up [30:21–30:53].
- [ ] Vic: add to all stand-ups; review PRs sent directly [20:00, 25:05].
- [ ] Team: LEO review with Sir Lloyd Thursday afternoon [24:30].
- [ ] Team: feature alignment session with Harvey tomorrow (time to be confirmed) [27:48].

**Stand-up updates [13:26–19:33]**
- Ethan: PR ready for GP-262, in review. Hackathon program flow finalized; needs meeting with Ed and Igor.
- Bernard: building CRUD for objective expectations; hackathon idea work.
- Clint: handed an urgent ticket to Laurence due to a blocker; employee proficiency enhancements deferred (lowest priority per Harvey).
- Laurence: GP-263 export failure fix is up for review (Harvey shared the exact prod error); waiting on review.
- Kentward: GP-259 (add objective enhancement) PR up, waiting on Harvey's review.
- Louise: wireframes for the employee action plan on the career growth objectives page, to show Harvey.
- Harvey: PR for GP-261 (filter tags by selected metrics) awaiting review; reviewed hackathon program and requirements-gathering prep.

**Blockers / risks**
- Floating PRs waiting on Harvey are the team's main blocker; reviews were taking beyond the 1–2 hour target [21:05, 29:34].
- Sir Lloyd's limited bandwidth was a bottleneck; Vic is the fix [06:21].
- Only 2 GitHub seats available; more are costly [22:04–22:15].
- LEO prototype accuracy depends on the level data in Growth Portal staging [22:26].
- Vic was removed from the repo last week and needs access again [30:24].

**Open questions**
- Hours/shift alignment with Vic (team 9–5, Vic usually 10–7); weekly alignment meets Mondays 10:30 [26:54–28:26].
- Who continues LEO development with Harvey, and whether more seats can be added [21:53–22:26].
- Weekly alignment time: team to decide preferred time with Vic [26:59].

## Transcript

[00:00] back here in PH, last year. So, joining with Full Scale. So, yeah. And also, not as a software engineer, I do also photography as a side hobby, an expensive side hobby, so...
[00:20] Yeah. That's for me.
[00:23] All right, thanks, Vic. Victor is a seasoned .NET, no? And our project is, I know this is going to be like on the spot, Vic, but
[00:33] the team is actually a FastTracker, so they are very, very fast. Very, very good, no? They had been with with me since like about two weeks na, or three?
[00:47] So, the project is more on the Growth Portal. So, we have that application Growth Portal, which is running on .NET. And then we converted that to database niya before was SQL, no? MS SQL. Now, it's updated to Postgres.
[01:08] So, the purpose, yeah, the purpose of this is to actually improve and adapt a new a new project that we are implementing.
[01:21] So, we will be having growth framework growth framework, which is going to be a upscaling framework for all of our employees that they can know where they are currently are, what are the areas needs to be improved,
[01:38] some sort of that direction. And then we have this Growth Portal. Growth Portal will handle all of those information that will that will be able to know an employee's current standing, their direction, the roadmap in terms of upscaling their skills, no?
[01:53] And then we have this new entity. We have not yet, ano, introduced this to the to the organization, only on only at the management level, no? So, we call it LEO. LEO is a chatbot that that will handle
[02:08] the growth. So, meaning, anything related to your growth, he will be a coach for us. So, for instance, if I log in to to LEO, I should be able to see Just Just to give you an idea Vic, no?
[02:26] So, LEO is like a chatbot. So, after, you know, if I log in, sign out Sign out sa ko, ha? So, if I log in as a new and first-time log-in member using sa katug hapon ROCKS account,
[02:45] I should be able to see my my current level. This level will be coming from Growth Portal, our application, no, sa Growth Portal. And then, if I look into that, I should be able to see what are my roadmap or my
[03:01] skill growth. So, this information comes from Growth Portal. So, we will be adding that, we will be optimizing that. So, this is already a proof-of-concept and an MVP
[03:13] that we have to continue working and continue testing it, ensuring that this actually is able to cater the the actual scenario for each user, no? Like I want to take the test, I want to No, there is no actual test for now. Ang process niya is that
[03:31] you log in, you will be able to see your what's your next item, and then you can start looking into it, and LEO will start to provide you a idea what what what needs to be done, what are the information resources that you can study, that you can start off. And then after that,
[03:53] so, sa at your at your own pace, you will you will have to learn from from that item, no, from that step for you to be able to come to a next level, no? So, once you're confident, you know already that that item, you will go back to LEO and you submit a narration of what you have did with this
[04:14] with this item, with this course item. It could be a course, it could be a a steps that you need to take, a learning step, a practical, or it could be a team collaboration, kay this is not only about technical, this is also include soft skills. So, it includes soft and hard skills. So, all of these are all placeholder for now, no? The information are are still at our Growth Portal staging environment.
[04:45] So, once once a person already is confident that they have tackled the item, they can submit a narration, and then LEO will submit a a claim in which our manager will be able to see that, and then they will conduct a one-on-one interview,
[04:59] and then that's the time you actually showcase to them like, "This is what I did. I I I did help a person in terms of managing the ticket." So, more on the collaboration or communication, or it could be a technical claim that you had, that you you know, "I learn I learn about this new tech.
[05:15] I want to claim this step from our career growth framework." And then, it re- ma-review na siya sa atong manager, they will then review it, and then they will see if it needs it needs more improvement, or they will approve it, and so forth, and so on. So, that's the usual routine for now.
[05:40] So, AI, si LEO is only about catering your current goal, information. There's no at this current phase, wala pa gyud siyang katong maingon nga, "Okay, I'll I'll validate you. Let's have let's have a validation test
[05:55] via the the chat." So, wala pa na siya. That's That's still our next next version, next phase. So, mao na siya, Vic. So, ang ang ang current nga situation karon, Vic,
[06:05] is that the team are actually very fast in terms of developing and and, you know, getting these requirements from different stakeholders. I want you to handle in terms of the technical direction sa team na to, Vic, so that they will be unblock in terms
[06:21] of technical difficulties, like organizing a a requirements gathering, so that kay karon man gud currently dili jud kay nako ma-handle in terms of full jud nga visibility, full support jud aning nga team, so naay time nga ma- ma-derail ko, and I don't want to be a a choke point, ba, to the team
[06:51] that will create a bottleneck. So, I want I want you, Vic, to do all the code review, approval, and if there is a need to kuan to do the direction needed for the team, technicalities
[07:05] nga madara nimo and the team together with Harvey, no, and the rest of the team, you collaborate and do your daily stand-up. That would also ensure the team's kanang fast kanang development, ba.
[07:22] So, is that something you're okay, Vic? I know this is on the spot.
[07:30] Ah, yeah. That's fine. Already talked about it yesterday.
[07:35] Yeah. So, guys, that's the new direction, no? So, any technical direction, all you need to do is coordinate with Vic. Vic should also be included in in your daily stand-up. I'll be joining every every week,
[07:49] or or if I can do it mo- more often or there is a need of urgents urgency, then I can join you, the team. But I'll I'll be very, you know, very confident and very
[08:05] you know, I I totally empower the team, no, to do the to do those to do this project and changes. So, which is had been proven naman. So, naa pod ni silay kuan, Vic, kanang
[08:21] kanang atong gitawag nga hackathon. So, we will finalize that kay we will be presenting it to the management. So, you, Harvey,
[08:33] Victor, and maybe the rest of the team can also join that. So, two i- I mean, three items, no? So, this is the new direction.
[08:45] And then the next one will be create a create a schedule, maybe tomorrow siguro, Harvey, together with Ed. Reach out to Ed unsa iyang available time, and the rest of the team also coordinate that and then we will discuss the the hackathon
[09:03] playbook that we had. So, we will explain it to them and then he will discuss it to us unsa iyang feedback kay madugay man gud ta kung magbalik-balik ta, so why not let him join para if he had more question, we can already address it right away. And the third item will be...
[09:23] Yeah, the last item I I remember already is continue sa katong kuan, no? requirements gathering, but still ayaw sa mo og do any kanang real project katong paminaw ninyo dako jud kaayo, but anything about about bug fixes, you do it and and go ahead and fix it.
[09:40] But anything a dako jud kaayo nga project, let's have a a kuan, no? A a plan siguro. Um
[10:00] Unsay term anang, e? Sprint planning? Kung unsa gyud 'to ang mga dako jud kaayo nga project. So, project breakdown?

[10:11] Yeah. Para... Kay sometimes man gud, some of these request coming, e... dawat lang ninyo ha? Pero wala ninyo kuan na ka ng inang, "We're not going to do this because because of that," and so forth. Dawat tanan ninyo nga mga requirements nga inyong nakuha from, from Ed, 'no? Schedule with Ed, and also Igor.

[10:31] And then, include me sa invite nimo, ah, Harvey, ha? So, ang target nato is to know unsa ilang challenges karon. So, we'll just have to take it, pero anything nga bag-o, we will do it. But anything dako jud kaayo nga project, requirements, and new feature,

[10:48] we will park it, we will have a plan if we are going to do this, if maybe... maybe gamay ra kaayo ang, ang kuan ani, ang affected, or iya ra na syang wish list, so, ato na syang i-validate, ato na syang i-review,

[11:00] kung dako ba na sya, na ba na syang ROI, sa atoang effort. So, we have to be very strategic in terms of providing. As much as possible, kung pwede wala tay buhaton sa growth, growth portal, mas maayo. Di ba? Mao na sya atong gain... atong goal. Pero, kung makita nato na this is actually a big impact to, to the organization, then, that's the time we will schedule that and put that in our pipeline.

[11:29] Nig-work ba gani gihapon sa growth portal? Kay last nako na-work is kuan, si Naka-work ko sa Timeclock og Growth, pero kuan na, padugay na kay 'to sa set-up sa caraang. So, while in progress, mm.

[11:45] Nabilin man gud ang kaining Growth. So, this new direction together with Leo, and, and Growth Framework, dako na jud sya og change, kay of course, ang mga tawo nato nagsige'g medyo pangita, "Unsa'y direction sa akoang career?" We do that, pero lisod kaayo sya i-handle kung walay first person nga mu-cater, which is mao na ni si Leo ang mu-handle ana nga, "Ah, mao ni imong level."

[12:14] So, anything, uh, Growth Framework information, katong mga details like katong competencies, collaboration, technical, viral nga technical nga, nga requirements, 'no? Those are will be coming from, uh, Harvey.

[12:32] Si Harvey will also give us a direction kung if Leo and Growth Portal and Growth Framework are aligned. So, mao na sya atong goal nga ma-align na sila, then we're doing the right, the right direction with that project.

[12:49] All right? Ah, is that clear? Any question?

[12:59] Guys? None, Kevin. All right. All clear. Nice. All right. Um... Again, uh, before you do that, uh... uh, mag-standup naman 'to. Introduce yourself again, meet meet Victor, and so that Victor will also have an idea of you guys. So, yeah, go ahead, uh, Harvey, take it over.

[13:26] Okay, team. So, let's have our quick update na lang, and then, please don't forget to introduce yourself since, uh, we have a new member joining today. Uh, Sir Vic, welcome to the team. And, yeah, let's start with Ethan.

[13:41] Uh, hello, team. Good morning. Uh, welcome, Sir Vic. So, yeah, I am Ethan Patrick and I was an intern here at Full Scale, and, yeah, I'm now a Fast Tracker. And I am part of the Rocks team, and Timeclock, and then, uh, this one, Growth. And

[14:01] yeah, I'm also based here in, uh, I'm also based here in Consolation, Cebu, so Yeah, that's all for my introduction. And for my updates, I have a PR ready, uh, for the GP-262. Uh, it's still in review and hopefully, someone can do code review on this already. And for the hackathon, yeah, uh, last week, I think we already finalized the program flow,

[14:31] but we still have to set a meeting with Sir Ed and Sir Igor to gather more information or requirements. So, yeah, that's all for my updates.

[14:41] Yeah. Thanks, Ethan. Bernard? Uh, hello. Uh, hello, everyone. Hello, uh, Vic. Uh, my name is Bernard J. Aurelio. I'm also an intern, uh, previously an intern here at Full Scale, and I'm currently in the Fast Track program. So, uh, I live in Talamban, Cebu City.

[15:06] So, yeah. Uh, for my updates, uh, I'll be implementing the CRUD for the expect- expectations for the objectives of the Growth Portal, and same as Ethan, uh, for the hackathon idea, and I think that's all. Thanks.

[15:25] Thanks, Bernard. Clint? Uh, hello, everyone. Uh, hello, Vic. Uh, welcome welcome to the team. I'm Clint. Uh, I'm also an intern here at Full Scale, uh, since the very first day my internship, I have I am already assigned

[15:42] in Growth Portal, and also one of the fast trackers. Uh, I al- I graduated in, uh, the University of Cebu, Main Campus. Uh, Bernard, and Ethan, and Harvey, and Laurence are my classmates. And,

[16:01] yeah, uh, welcome to the team, and we're looking forward to, uh, work with you here. And also, for my quick updates, uh, last week, I handed over my ticket to Laurence due to a blocker, since the ticket was urgent. So, I handed it to Laurence. And for the, uh, employee proficiency enhancements, I deferred it since Sir Harvey

[16:27] uh, mentioned that it's our least priority. I think that's it. Uh, thank you, everyone.

[16:35] Thanks, Clint. Uh, go ahead, Laurence. Uh, good day, team. And hello, Vic. So, same as everyone, I was also an intern

[16:44] here at Full Scale. And then, I was also lucky to join the Fast Track program. And, ah yeah, I am Leander Laurence Lubguban, you can call me Laurence. I'm originally from Mindanao, Zamboanga del Sur, but right now I am in Cebu City. So, quick updates from me: I was assigned to a bug fix for an export failure GP-263. Uh, we couldn't reproduce it locally or on staging, so we suspected it was bad data.

[17:15] So, that's why reach we reached out to Sir Lloyd if CloudWatch was set up so that we could pinpoint the error. Uh, anyways, it's sorted now since Sir Harvey shared the exact production error and a fix was made quickly. So, right now, the the fix for it is up for review. I'm waiting for anyone to code review it. I think the uh, the one I requested was Sir Harvey, still waiting on that. And, yeah, I think that's all for my updates.

[17:43] Yeah. Thanks, Laurence. Go ahead, Kentward.

[17:48] Um, hello, team. Uh, good morning. Um, hello, Victor. So, quick introduction about me, I'm also an intern here at Full Scale. I was assigned at Timeclock, and, luckily, I got also hired as a fast tracker. And quick update for me, I'm currently

[18:08] finish with the enhancement on the add objective, which is GP-259. I created a PR and still waiting for Sir Harvey's review. So, yeah, that's all for my update. Thank you.

[18:20] Yep, thanks, Kentward. Louise?

[18:23] Uh, good day, team. Uh, nice to meet you, Vic. My name is Louise Andrei Yoano. I am based in Lapu-Lapu. So, um, my current update is that I'm assigned to implementing the employee action plan

[18:41] in the career growth objectives page in the Growth Portal. I've finished creating wireframes so that I uh I could show it to Sir Harvey next alignment meeting, so that uh I could gather his thoughts on it and if he approves it. That's all for my update.

[18:57] Yep. Thanks, Louise. Uh, for me, uh, quick introduction, I am Harvey, and then, same as everyone, I'm uh previously intern here at Full Scale, and luckily, uh, joined the Fast Track program. And welcome to the team, Sir Vic,

[19:12] Vic. And then, uh, for my quick uh update: So, I recently created a PR for GP-261, which is the filter tags by uh selected metrics, and then, uh waiting for a code review, and also, reviewed the hackathon program

[19:33] and for the needed items in preparation for requirements gathering with Sir Ed and Sir Igor. And, yeah, that's all from me.

[19:49] All All right. Thank you. Thank you, Harvey. Uh, before I forget, though, um... add kuan, add Victor to all the kuan nato standup.
[20:00] And then, also, try to plan kung pwede ba mangita ta'g way to to find a code reviewer nga agent gani.
[20:12] Para dili dili mo madugay pod sa pag-review. At least ba, nakuha na siya na na-filter na ba, na nakuha na. So, plan it plan it out, try to see kinsay pwede mo mo-side side project ana sa team.
[20:26] And then, unsa pa?
[20:28] Naa naa man siguro, boy, regarding sa Claude nga kuan, kanang code reviewer na sa GitHub plugin. So, previously, mao na amo gamit para
[20:41] naa imohang code review ba. So, ug wala mi katong linter, it's either the GitHub katong Claude integrated, which is under organization man siguro.
[20:51] So, nindot pod katong imong review para dili bitaw... Right now, I think most of these guys kanang naka-floating ilang code review, that that needs to be addressed kay, um, for me
[21:05] bunalan mi last time ug dili... labi na'g depende sa severity, bunalan mi ug dili mi maka-code review in within 1 to 2 hours.
[21:14] Oh, so mao na, mao na nga kuan jud, na-bottleneck jud ko kay, you know, my responsibility. So, that's where you come in. You help them out with the code review.
[21:26] And also, if you need kanang mga subscription, mga permission, ah, Harvey, you contact Harvey Martus, ha?
[21:35] Ah, sige sige.
[21:36] Uh, and then, para ma-unblock mo in terms of technicalities, and then, kana gani, unsa pa may lain nato, Harvey, nga nakalimtan? Code reviewer...
[21:50] Katong work on sa Leo?
[21:53] Ah, yeah, ang work on sa Leo... ug kinsa katong i-chats? Duha ra jud ka seats ang pwede ato. Try to, kung pwede, estoryahi lang si Harvey
[22:04] kung pwede ba madugang og duha or upat, unsa katong ganahan nimog trabaho sa katong Leo ba.
[22:10] Kay ang available seats nga nakita nako, duha na lang.
[22:15] So, you know, expensive pod, a little bit expensive ba ang kanang GitHub seats?
[22:21] So, kana, i-coordinate lang siya, Harvey, ha, ni Harvey.
[22:26] Unnya, kung pwede, if more, unya, kamo ray sabot kinsay gusto nga mo-develop jud sa sa kang Leo, mo-continue sa kang Leo. Kay karon, naay sa prototype, it actually works, but the accuracy, the data it it gathers, ang reference nga mokuha siya sa iyang grade level, current grade level naa sa growth portal sa staging.
[22:48] So, in short jud, nya, ang ang direction ni Harvey
[22:51] og direction aning Leo
[22:54] mag-in sync jud sila.
[22:57] Para dili gani mag-duplicate nga ana. Naghimo pod og laing line of line of direction pero si Leo daw nag-focus ra sa laing information, which is naa sa settings.
[23:07] So, ah ah, akong ipakita.
[23:10] Diri naa si Leo... Unsa na ni akong mouse?
[23:14] Abap!
[23:15] E-uncheck man akong keyboard.
[23:18] May may iyang sister is online schooling, no?
[23:22] Gikuhaan og keyboard.
[23:26] Uh, okay na. Sige, akong i-share, no?
[23:31] Uh, kita mo sa akong screen, no? Dili ninyo kaybaw man jud mo kung asa ni?
[23:39] Uh, GP
[23:41] Ah, okay.
[23:45] So, naa siya diri sa settings.
[23:48] Mao ni siya ang gitan-aw lang ni Leo tanan, ha? Naa ra siya diri gatan-aw, growth framework.
[23:55] Diri ra sa tanan nagtan-aw.
[23:59] For your information.
[24:03] Ah, diri ang job uh kuan, so
[24:06] ang target nato is, in short, kung mao ba jud ni gusto ni Harvey.
[24:11] Harv, unsa man ingon? Sa kuwang ba ni ang naming? Sakto ba ang naming?
[24:15] And then, mao na, you you, I empower you to take take over of this project, na. Hey, this is already a prototype and seems to be working, so
[24:26] kamo na'y mo-continue and then we will have a
[24:30] maybe a review siguro sa Thursday afternoon
[24:35] kung unsa'y na-come up ninyo ni Harvey.
[24:39] All right. I know daghan jud kaayo.
[24:42] Daghan kaayo, Harvey, no?
[24:47] But yeah, so questions so far?
[24:50] Any, uh, risk that you are seeing right now?
[24:58] Or upcoming nga mga challenge?
[25:01] Oh so, ah, one thing diay, ah, for everyone, so,
[25:05] if, ah, na-unblock mo, you can send the code review to me, so I would be able to check it manually if wala tay kanang Claude checker
[25:13] para ma-unblock para ma-unblock mo 'nya maka-proceed mo. So, I can do... I can today I'm not sure if wala kay kuan god, so I'll have to do it. Ah, I'll have to manually check it rather than relying on the Claude while kay si Harvey, actually busy kini, dugay mo-reply, so, ah, I'll take it over sa mga kuan code review dayon.
[25:35] All right.
[25:37] So, ah, give access to kuan, no, Victor, kung you need. Reach out lang
[25:44] direct pod.
[25:48] Gawas og dili ta og AI.
[25:53] All right. AI na man jud karon. But at least they they are empowered gamit sa AI.
[26:00] So, they are very very fast. That's why they call they are called kanang fast tracker.
[26:07] Naana man gud ko sa kanang ancient type god nga mga karaan ba, so
[26:12] Nag-kuan gihapon AI pero...
[26:14] Ah, okay.
[26:17] Fast tracker ni. Kinaana gani minyo-unon na ni. Kinsa gani minyo-unon na ni nila?
[26:22] Si...
[26:23] Si Kobe? Mao na'y pang-angayong style.
[26:28] Fast tracker gani.
[26:31] All right, guys. I think that's it for me. So, if you can continue, unsa pa'y inyong gustong i-tackle,
[26:38] away, ah, wala na ako diha, so so that you can do it comfortably. I know you should be comfortable with me, but you do it comfortably at your own pace, at your own time.
[26:47] You do that and reach out for me if any other escalated problem, concern, or request nga black jud mo.
[26:54] Oh, puyde ko, By Lord, ah, regarding with the schedule, unsa'y schedule nato ani usually?
[26:59] Ah, kamo lay sabot. Kay ako, mo-join ra man ko every Monday. Ang Monday nato 10:30,
[27:05] naa jud ni siya kay alignment man.
[27:06] Monday weekly. Ah, weekly alignment.
[27:07] Mao, weekly, so naa na sa daily. Pero kamo lay sabot unsa'y inyong preferred time.
[27:12] Pero ang shift schedule ani kasagaran sa uban is
[27:15] Kuan ni siya, 9:00 to 5:00 ko, sakto, Harvey, no?
[27:20] Ah, 9:00 to 5:00, oo.
[27:22] Yeah.
[27:23] Sige, sige. Puyde ra pod mo moingong sayo de kay, um...
[27:27] Sige, kung mag-discuss pa mo, guys, ah, I'll I'll leave now and then you continue discussing with Victor and the rest of the team. All right?
[27:35] Thank you, guys.
[27:37] All right. Thank you.
[27:38] Have a nice Monday. All right.
[27:41] Sige, sir.
[27:44] So, wala ra mo'y concern sa kuan?
[27:48] Oh, just a uh just a reminder, guys, ah, we have a, uh, feature alignment session, uh, with Sir Harvey, tomorrow.
[27:56] Yeah, I think, ah, I will again check what time.
[28:01] And yeah, I'll just update the team.
[28:04] Pero mangutana ko ninyo, unsa man jud ang oras inyong ting-in jud
[28:08] para ma-sync ba. Kay, usually,
[28:11] musulod ko'g 10, so mao man pod gi-kuan sa Fullscale, 10 10 to 7.
[28:18] Ah, usually 9:00 to 6:00 man me, Sir.
[28:21] 9:00 to 5:00.
[28:22] 9:00 to 5:00. Same pod, ah, 10:00 to 7:00.
[28:26] Kay usually dako kay'g matak-an, matog gani gadlawon, mga 5:00.
[28:32] Busy.
[28:34] Sige'g kuan ba, kanang,
[28:36] random bitaw mag-
[28:38] mag-build og portfolio sa architectural level ba, so, mao na.
[28:44] Rang, side trip sa kaboang.
[28:46] Inag-ani.
[28:48] So, regarding ani, murag kamo man jud ang murag fast track, ah, kada-kada na lang, mga 5 minutes lang, ah, para maka-gauge pod ko'g asa mo. So,
[28:57] puro mo mga interns karon? Ah,
[28:59] unsa ba, or graduate na?
[29:01] Ah.
[29:02] Oo, graduate na.
[29:03] Graduate na, sir.
[29:04] Graduate na mi, sir.
[29:06] So, gi-kuan mo sa Fullscale last year? Ah, this year ba gi-kuan?
[29:11] This year, yeah. This year.
[29:14] July.
[29:16] So, US C tanan?
[29:18] Ah, US, San Carlos, US, USJR.
[29:22] Ah, sakto, sakto.
[29:25] Sige, murag mao ra man siguro to. Kung kuan 'nya, tanan code review, i-kuan lang para kun ganahan mo ma-unblock 'nya excited mo motrabaho sa lain nga task.
[29:34] Sir, mao jud na among kuan, sir, main blocker. Kanang floating nga mga PR, so dili kami maka-proceed.
[29:40] Kinsa diay tigg-PR, na-code review sa PR ninyo?
[29:43] Sir Harvey.
[29:45] Ah, dugay-dugay pod na.
[29:47] Kay even akong mga kuan 'nya sa session, mu-decide gani diri, matagad or dili ma-replyan, so,
[29:53] it's totally understandable. So,
[29:56] sige, og naa mo'y mga concern, PM lang jud. 'Nya ayaw jud mo'g magduhaduha.
[30:00] Okay. Nag-reply man ko. Kay gigama pod, nangita pod gihapon so i-send lang ninyo ang PR.
[30:10] Any concerns or questions before ta mag-kwan? Kung naay mga laing pangutana.
[30:17] None na sa akoa.
[30:18] Naa na ba ka sa position sir?
[30:21] Ha?
[30:21] Naa na ba ka sa repo sa atong portal?
[30:24] Wala pa. Gi-tanggal man ko last week.
[30:28] I-add lang ko.
[30:30] Na-add ba ta sir Hervey gihapon?
[30:34] Sir Hervey ha.
[30:37] Sa channel pod oh. Wala pod to sir.
[30:40] Ha, sa channel?
[30:41] I-add lang ko sa inyong channel ninyo or any updates para
[30:45] Ah Clint, pwede ra man ka ma-reach out kang Sir Hervey then i-add si kwan, si Vic, sa repo.
[30:50] Ah sige, ako lang i-message diha.
[30:52] Sige sige.
[30:53] Niya i-follow up lang pud nako ni Hervey in case nga dili ka replyan diha sa message ni kwan.
[30:59] Okay.
[31:00] Sige, mao ra to.
[31:05] Sige, thank you.
[31:07] Sige, thank you, thank you.
[31:08] Thank you, bye. Thank you, team.
