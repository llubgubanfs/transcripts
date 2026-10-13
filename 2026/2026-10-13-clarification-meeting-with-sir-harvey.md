---
title: "Clarification meeting with Sir Harvey"
date: 2026-10-13
type: meeting
tags: [meeting, growth-portal, growth-framework-3, operational-task, onboarding-checklist, expectations]
participants: [Harvey, Louis, Bernard, Victor, Clint, Lawrence]
source: "/home/yander/Videos/dsm/[clarification meet with sirharvey] [trimmed]screenrecording-2026-10-13_11-18-39_trimmed.mp4"
transcriber: gemini
saved: 2026-10-13T14:54:02
---

# Clarification meeting with Sir Harvey

## Executive summary

**TL;DR**
- The recording is trimmed and starts mid-discussion. Sir Harvey led a clarification session on Growth Framework 3.0 and the Growth Portal features (operational task, onboarding checklist, expectations CRUD).
- The operational task / onboarding checklist feature is not yet justified: only about 2 of 3–4 contacted people replied, and none seem to use the portal's onboarding or KPI objectives items. Harvey wants at least 10 interviews, recorded with transcripts, before building anything [14:04–21:01].
- Bernard's expectations CRUD (an alternative to uploading the Excel framework) is put on hold until there is a clear use case. Edits to job-grade expectations might happen only once a year or less [37:11–44:30].

**Decisions**
- Hold the expectations CRUD. Uploading the Excel file is simpler for now; revisit when a clear use case appears [44:17–44:24].
- Hold the proficiency item until the objectives discussion continues. Proficiency definitions (introduction / proficiency / expertise / mastery) exist in Growth Framework 3.0 but not 2.0 [44:36–45:32].
- Deployments should be announced in the announcement channel by Sir Lloyd or Harvey, not by individuals. Discuss a fixed deployment day per sprint, preferably in the afternoon since CSMs start late [46:15–47:34].
- Interview results go into a folder on Zoho WorkDrive for the Growth Portal, each with a ticket for traceability [48:28–49:45].

**Key points**
- Operational task is meant to equal the action plan. It is mainly useful for onboarding and offboarding (laptop wipes on offboarding); the CSM gives only a shareable document at onboarding, not a Growth Portal checklist [01:41–05:03].
- Existing KPI objectives under settings are mostly onboarding items (daily standups, three tickets, clone and run the repo) and appear unused [11:43–13:54].
- Louis asked regular employees: they rarely visit the Performance Review page, only each quarter [09:33–11:03].
- Harvey's rationale: with coding now taking minutes, the team should check whether features are actually used, and "What if we don't do this?" is the key product-thinking question. He also wants the transcripts to feed a "product wave"-style bet on features [16:11–19:55].
- Growth Framework 3.0 expectations are inconsistent: job-grade metrics mix wording ("team savvy problem identifier"), and unit testing disappears at grade 5 and returns at 6. Skill profiles also shift over time (cloud computing, CI/CD, AI moving down to junior levels) [25:55–37:59].
- Bernard has been implementing with his personal Claude account. AI accounts are not provided because Growth Portal members are not allowed to work on internal tools. Workaround is OpenCode; Harvey noted it as a follow-up [26:45–29:10].
- Growth Framework 3.0 is not finished (half of October gone). It should be implemented this year, ideally before the December party [50:13–50:48].
- Azure deployments are disabled; everything points at AWS staging and prod [47:51–48:07].

**Action items**
- [ ] Louis: interview at least 10 people (CSMs, plus bench via Harvey's suggestions) on onboarding checklists; record with transcripts; ask whether a checklist is needed and what it should contain (dev setup, documentation, communication plan, scope of work, leaves) [20:06–22:12]
- [ ] Louis: put interview results in the Growth Portal WorkDrive folder with a ticket [48:28]
- [ ] Harvey: send suggested bench people to interview [15:30–15:47]
- [ ] Harvey: review product wave info and AI account / OpenCode question [28:41–29:10]
- [ ] Bernard: hold the expectations CRUD [44:17]
- [ ] Bernard: raise a PR for the in-progress implementation by end of day [23:03–23:19] (the transcript says the PRs for items 1, 4, 5, 7 should be up [45:43])
- [ ] Lawrence: deploy the approved export priority fix after the meeting, and announce it [45:56–46:08]
- [ ] Team: define a deployment cadence per sprint [46:40–47:34]
- [ ] Everyone: create tickets for all work and keep documents in the Growth Portal folder [49:00–49:45]

**Blockers / risks**
- Few interview replies (about 1 of 3–4 responded; last CSM usage was last year) [14:04–14:21, 42:22–42:45].
- Growth Framework 3.0 is not final; some expectations are ambiguous.
- No official AI account for the team.

**Open questions**
- Is the onboarding checklist / operational task needed at all, and for whom?
- What is the real use case for editing expectations in the app?
- Names are Gemini's spellings (Louis/Luis, Bernard, Victor, Clint, Lawrence, Lloyd, Leyo); "Mark"/"Mat" and a few terms are uncertain. The recording starts mid-sentence and I haven't checked frames.

## Transcript

[00:00] or, um, application ba?
[00:05] So, wala siya ingon ana. And then, how we will assess ana, or how will you validate that that one. So, that's what we're trying to kuan, the risk, ah, newer version.
[00:17] Okay.
[00:18] So, I don't know, basaha sa ninyo balik ang 2.0. You will get what I mean.
[00:23] Kong unsa, like for example, sa inyong ang end,
[00:27] mostly mga naa mo sa junior level.
[00:30] Yeah, you have to read that one. Try to check katong usa ka slide didto related sa inyong job grade, and then try to understand kung unsa na ninyo pagkahibalo nga advance ka.
[00:40] Okay, or would you know nga naa ka sa mid nga level or intermediate imong nahibaloan, or yeah, basic lang.
[00:49] Okay. Now, going back, ani.
[00:52] So, I was looking at this one and then I realized nga si Leyo, mura bag gikaon na niya ang career objective ang learning, ug ang probably ang assessment pod.
[01:04] Kay akong clear pa didto is more on the career nga part, ug ang learning activity.
[01:10] I'm not sure if Leyo gyud is mukuha pod siya, mokaon aning, I mean, iyang i-take part pod ang assessment.
[01:19] Probably, he could.
[01:22] Yeah, relate it, kay si Leyo dapat naa na man gyud siyay copy atong growth framework, nga naa na didto sa growth framework ang unsay buhaton nga assessment.
[01:33] So, most likely kuhaon na niya, but 50-50 pa kuan na dira.
[01:37] Ang klaro lang is kaning career ug ang learning.
[01:41] So, what's left is kaning operational task.
[01:45] Ang pasabot aning operational task, this is equivalent sa inyong action plan.
[01:51] Everyone knows about your action plan.
[01:54] Or,
[01:56] okay.
[01:57] Di ba, Victor, na nakasulod naman 'to ang client, di ba?
[02:02] During your, kanang bitaw, pag-onboard sa imoha, na ba'y gihata sa imoha sa CSM like what are things to do?
[02:11] Let me correct, onboarding.
[02:14] Kuan ra, gitagaan ra ko og documentation nga kuan, uh,
[02:19] kuan, client overview, unsay tech stack,
[02:23] ingana ra.
[02:25] Kay pag-sulod nako sa client, ah, wala gyud ko kahibalo unsay akong buhaton, kay
[02:29] wala ko gi-orient, wala tanan, so, I have to find it for myself. So,
[02:34] mao na siya. So, it varies kay,
[02:37] um, ang uban kauban nako, katong mga late na sud pod, uh,
[02:43] katong usa si Yuriko, na-kuan nako kay mga a week rami ligas.
[02:49] So, mao to, naka-prepare na ko daan tanan documentation,
[02:52] and ang uban is gitagaan na og kuan, kanang, naa na'y mga orientation. So, mura og kami ang mura og na-pioneer bitaw nga mga unfortunate ones.
[03:03] Okay. Pero akong, okay, sige, akong i-segregate sa. So, ang nag-provide nimo og information, ang client or ang CSM?
[03:11] CSM, initial.
[03:13] Initial CSM.
[03:14] So, document lang siya, dili siya sa growth portal, like naa kay i-check-check didto sa imong objectives.
[03:21] Ah, dili.
[03:22] Wala.
[03:23] So, document lang gyud siya nga shareable document, okay, ang sa CSM.
[03:28] Pero pag-abot ni Yuriko,
[03:31] kuan na, ang kuan na tong documentation nga gibuhat, ug unsa akong nakuha sa one week.
[03:39] So, document pod gihapon.
[03:41] Oo, pero under kuan na 'to, kanang, gibuhat na nako.
[03:46] Kay, gas to man ko nga mag-track permi god, unya, kay nabaw-an man nako, gi-announce man ni Mark, semblante nga
[03:53] naay mo-sud.
[03:55] So, ana ko, sige, sakto ra kay naa na 'ko 'yoy gi-prepare nga documentation para di siya masaag ug di siya ma-delay og pila ka adlaw.
[04:02] So, mao na siya.
[04:04] Moro gyud na lang pata mag kuan ani. Mag interview og lain.
[04:09] Mga members. Okay. So, it could be inana imong case, 'no, Victor, sa imong end.
[04:15] Hmm.
[04:15] Mag-la-lai man daw, moingon nila.
[04:19] Oh.
[04:21] Which beg the question na sad 'no, um,
[04:26] Siguro sa FS learning, this is needed.
[04:29] Kong FS learning, yeah, I I we need the operational task, kay especially kung ma-offboard mo,
[04:36] um, typically man gud kanang, kanang bitaw mga source code ninyo, mga documents once you are offboarded from the client, dapat i-erase gyud na siya.
[04:45] Like literal format gyud na inyong,
[04:47] format gyud.
[04:48] Oo, i-format gyud ang laptop.
[04:51] Kuan man gyud na. Yes, mao na akong gi-perform recently nga total erase gyud.
[04:55] Mm, total erase gyud na siya.
[04:58] So, inyo gyud nang kalimtan.
[05:01] Oh.
[05:03] So, mahug dayon ang operational task will be, I mean, for now, use kuan gyud siya gyud, gamit diri sa FS learning, especially kanang ma-offboard.
[05:17] Okay. So,
[05:20] Okay, pwede ra man sad later on, atong i-require tanan, like tanan CSM, tanan project, ma-onboard gani project, dapat na'y operational task, anyway, na may naka-define didto.
[05:33] So, I guess naa siguro silay na-andan or anything, kay it could be sad base siguro sa atong interview, I mean, later on mag-interview man gud ta guys.
[05:44] Interviewhon gyud nato, before ta maghimo og mga kuan kanang mga features.
[05:50] Okay.
[05:51] So, whether it is worth it ba gamiton. Like for example, karon na naghimo silag mga objectives sa KPI didto sa growth framework niya,
[05:59] mura bag it turns out,
[06:02] I mean, base sa akong kuan, no, mura og wala ra kay nag-gamit ato.
[06:07] So, I would want to know pod ang uban nga CSM kung gigamit ba kaha to nila ang mga kuan katong mga items didto.
[06:16] Um,
[06:19] kanana.
[06:23] So, ang ending ani, mawa, like, for example, operational task na lang ni, wala na'y gamit siguro ang metrics.
[06:33] Siguro, in a way,
[06:36] yeah, naa na lang tay expectation and then the target date siguro, ana.
[06:43] Okay. Mm.
[06:48] Sige, ah.
[06:54] Mura bag ang question is,
[06:57] next question na ani ba, kanang bang pina-product thinking, kay I don't know if you have read the book, The Product Thinking. Nakabasa ba mo tanan?
[07:06] Nakabasa ba mo or wala?
[07:09] Wala pa sir.
[07:11] How about the others?
[07:13] Ah katong ka Mat?
[07:15] Oo, kanang. Ang product thinking, sir.
[07:17] Ah product thinking. Oo. Product thinking.
[07:22] Kabasa. Gamay.
[07:24] Human ninyo guys kay ngano. Dapat kay og ma-learn didto.
[07:29] Sa second part ra og ako 'to sir. Page 100.
[07:33] Oh, basta, basta balikan ninyo basa pod.
[07:37] Kay, mura bag
[07:39] imagine na lang guys, kanang si Mat, that's will, shall we say, millionaire na na siya.
[07:46] Di ba?
[07:47] Yeah, usually sa akong mantra man gud, motuo ko og mga millionaire or billionaire, kay sa kaning bitaw mag sige og istorya nga, "Uy, na koy gihimo in ani in ani," pero wala may na kuan, na-prove.
[07:58] Si Mat, naa na siyay na-prove.
[08:00] Okay.
[08:01] So, kanang mura bag kuan na na siya.
[08:04] You can think of kanang iyang libro as kuan niya, mura bag cheat sheet bitaw nato.
[08:11] On how to kuan jani.
[08:14] Sige, so naa koy gi-point, i-point lang didto sa product driven na book. Um,
[08:19] ang question didto is, "What if dili ni nato buhaton?"
[08:25] 'Di ba?
[08:28] Naa 'yusa ka question.
[08:29] Ah yes, oo, oo, kabasa kay kuan na, what if dili buhaton? Kay
[08:34] maybe redundant, maybe it wasn't really needed, or something along the line.
[08:42] Mm-hmm.
[08:43] So, mao na siya ang kuan.
[08:46] Usa na siya sa mga question, 'di ba?
[08:48] What if dili ni nato buhaton? Pero, sige lang.
[08:53] Karon, di pa nato na ma-answer. I mean, kung karon nga context, we could say nga, "Yeah, dili na nato ni need."
[08:58] Pero, what if naay, kanang kuan, kanang road framework? That's one thing pod.
[09:03] Yeah, we need to take into consideration.
[09:07] So,
[09:09] Sige, ah.
[09:19] Okay. Um, di ba, ah, Lewis?
[09:22] Di ba, I I I asked you to kuan, kanang,
[09:27] mangutana sa mga CS. Ikaw to akong gipangutana, or mga members bitaw, I asked you to kuan kung
[09:33] Ah, yes, sir. Um, naa koy gi-ask mga, not CSM, kanang mga regular employees ba.
[09:38] Ang akong na-gather nga input from them is
[09:42] kanang, panalagsa ra pod gyud sila mo-visit sa Performance Review Page, kanang
[09:49] every kuan, every performance review,
[09:52] performance review, ana na sila mo-check, pero,
[09:55] uh, when I asked them, "Oh, is it, uh, will it be helpful to implement AI?
[10:00] said oh yeah, useful rin naman, pero and then again, panalagsa ra man sad gyud sila mo visit sa page. So it, you know, it begs the question if worth it ba gyud ta lang nga mag invest og effort para sa ano, implement og AI. So yeah, Mark, [10:15] that's what I got from them. [10:18] Okay. [10:20] Ah, did you ask ba kanang when ma on board ba sila sa ilang project, kay mugamit ba sila ani? [10:26] Sa Growth portal? [10:28] Oo. [10:29] Ako ha, personally, [10:31] no. [10:32] Ah, [10:32] maunana-una na nako, if moingon si [10:36] Mark nga oy, palihog og tan-aw ani ninyo, ha. [10:40] Pero [10:41] 95% will check it. [10:45] Para sa ako lang. Uh, if mangayo mo og input from [10:48] ah, naka onboarding na, ang naka kuwan. So, [10:51] rare gyud siya. Unless naay mga [10:54] Spartan training or needed gyud kaayo nga tan-awon or mag check lang sa mga assessment. Ana ra, koto ra gyud ya. [11:03] Mga quarterly lang. [11:07] Okay. [11:08] Kung sa ma onboard ya, mura'g rare. [11:12] I thought gyud nga kuan, um, maybe we'll have to ask siguro mga CSM, ani [11:19] kung gigamit ba pud nila ni. [11:23] Kay, pwede i-open sa Growth. Naa pa may access sa admin. [11:27] Kinsa'y naay access sa admin? [11:30] Naa pa kay access, Louis, sa admin? [11:32] Sa preprod sir. [11:34] Okay ra. Okay ra. [11:37] Oh, [11:37] sa Growth sir, no? [11:39] Ah, Growth. [11:40] Sa kanato kuan, ah, kani. [11:43] Kanang bitaw, adto mo sa settings, settings settings, settings, settings, [11:49] kanang objectives sa KPI, [11:53] kanang mga part ba. [11:55] Kanang siyang mga nag una dira is this is kuan kanang initial gyud ni nga mga date, I mean, information. Yeah, if you try to read it, [12:06] typically, ang naa dira is pang onboarding gyud siya gyud. [12:11] Ana o. [12:12] Daily standups, [12:14] mga clarify requirements, [12:16] unsay mga productivity complete at least three ticket. [12:20] Ang uban ani mora'g pang kuan siya, kanang, if you scroll down, [12:23] scroll down, naa'y part diri nga kuan like [12:26] kanang mga ownership of onboarding, [12:30] kanang mga interview, daan na na siya, kanang week one engineering ako ha na. [12:35] Ako may nag create ana, kay I was trying to experiment. Asa gyud nako na ibutang ang action plan diri, ba, or didto sa kuan, kanang excel sheet. [12:44] Oh, kanang collaboration and teamwork, daan na na diha. [12:49] So, [12:49] ang kuan lang ba is, wala gyud ni siya gigamit, kani. [12:55] If in ana man gani. [12:58] Oh, kani o, professional readiness requirement. Mora'g pang kuan man ni siya, o, kanang like, i-update, [13:04] oh, kanang masulod ka sa FS learning. [13:06] So, mao na. [13:10] Oh, naa pa gyud o, week one, kanang development set ako, kanang pang onboarding gyud na, sa client, kanang naa sa ubos, week one engineering foundations. [13:20] Yeah, you see da na, fix, oh. So [13:21] some development set up niya, mag fix daw ni og one bug. Okay. [13:26] Oh, successfully clone, oh kanang pang onboarding mo na, pull, build and run the project with without errors. [13:36] Hmm, kanang. Oh, scroll pa daw. Oh, unsa pa may mga items dira. [13:40] Ah, kanang mga environment setup naman. [13:42] So, kanang [13:43] pang FS learning. Mura'g ako na siguro ni naghimo ani, kaning kinalubsan. [13:48] So, [13:54] naunsa man ni siya nga dili kaayo gamiton. [13:58] I mean based lang sa kuan, no. [14:02] Hmm. [14:04] Pilay imong gi-interview, Louis? [14:07] Lima? [14:08] Ah, isa ra man sad ang, ang nitubag sir, ang uban wala man ni kuan, wala man ni [14:13] Pilay imong gi-sendan? [14:15] Ah, [14:16] 100? [14:17] Tulo, ah, tulo, ah, tulo [14:18] Ah, tulo o upat lang. [14:21] Mura'g [14:21] 33% r'ako kuan, 33%, daghan na. [14:25] [14:27] [14:27] Dili kuan lang, at least maka, kuan lang ka og kuan ba, kanang inside ba, kay you cannot get an inside [14:33] by just one person, og ikaduha ni si Victor, kulang pa ba. [14:38] So, [14:40] yeah we need more info gyud. [14:46] So, at least siguro, kuan na lang like tulo. [14:50] Three more. [14:52] O, [14:52] sige lang, Luis. [14:54] Kanang bang, i-i-i-try og kuan bitaw, like try to capture nga during pag-onboard ba nila, namba silay mga checklist or asa sila nag kuha og checklist, [15:05] sa ilang onboarding? [15:08] Kay, pwede man sad gyud ta makakuha og kuan ba, nga based anang nga information. [15:13] By the way, i- [15:14] unsa na, gi-chat ra ni mo? Or gi-interview gyud nga like inani ba nga nay video and kuan? [15:21] Um, chat lang, sir, kay busy man ang kuan, busy sila ba. [15:27] Okay, sige. [15:30] Pwede ko makasuggest ana, [15:32] kanang, Harvey, ah, regarding ana mag-interview. [15:36] Pwede ra ba nasa bench pud ninyong gi-interview? Or, [15:39] pwede ra sad, o, bench. [15:41] I can send you a kuan, mga suggestion nga tawo nga pwede ma-interview. [15:47] Ah, [15:48] nga totood na gyud ba, so [15:50] pila na ka client, so I can kuan [15:52] ako lang, i-provide. [15:53] O, [15:54] pwede ra, in-ana pali og ko, i-kuan. Kinahanglan siya recorded with transcript. [16:01] Oh. [16:02] Sige, ako sa'y nangutana to sila. [16:04] Ako lang i-heads up, Dan. [16:06] O. [16:11] Hey, ani man gud na siya guys, um, we are doing software development gyud, dili kay tagaan ra ta'g kuan requirements. [16:21] So mao ni'y buhaton, that was, [16:24] last year. [16:26] We are now in kuan na. [16:30] Kanang kani nga age bitaw, nga before we do so, I mean, [16:35] this is on the notion nga ang coding is 1 minute na lang mabuhat, dili parehas sa una ba nga moabot og two weeks. [16:43] Okay, karon one minute to two, or one minute to 5 minutes na lang. [16:49] So ang ato is trying to ensure nga gigamit ba ka ani, [16:55] gigamit ba gyud siya gyud, [16:57] or gamiton ba gyud. [17:03] So kanang, ganahan ko makahibalo kanang, yeah, [17:06] if they are actually using this. [17:09] If they are not using, [17:12] naa ba ta'y pwede ma-suggest, [17:15] or is it okay lang sa karon siguro, why not. What if dili na nato buhaton like okay na tong kuan documentation like kato'ng gi-ingon ni Victor. [17:26] Mas streamlined pa or anything, but I would suggest nga naa na siya. [17:33] Maabot na gyud siya diri sa Growth portal kay ngano, mao man na siya'y team island gyud nga nag-start ka na nga project pud. [17:40] Nga naay mga kuan gani, [17:43] kanang [17:45] confirmation nga [17:47] naa ka na nga project, nga na na ingnan ka nga uy na onboarded na namo, nami onboarding nga process. [17:55] Naa may kuan diri o, kanang, unsa na, kanang resibo. [18:00] Ito. [18:02] Kay karon, 'di ba, kung let's say ma-onboard ka unya, [18:06] document ra nga, oh, kani mga lista na kuan ah, o, siguro [18:12] mag mag-iniha pay bitaw, later on, [18:17] basin i-kuan na ba [18:19] ma-scrutinize, [18:21] either ma-scrutinize, or pangitaan ba. [18:25] Sige. [18:27] So, kanang, um, try to interview pa [18:31] i-need pa, i-need na siya or sige, sir, sige, sir. [18:34] O. [18:34] Yeah, tagai lang ko sa transcript, kay atong kuanon if [18:40] na man gud mi'y gi, kuan pud nga [18:43] na gi-ingnan ba mo ni Lloyd pud about product wave? [18:48] Or wala? [18:50] About sa- sa sir? [18:52] Product wave. [18:54] Product, oh, wala sir. [18:56] Wala siya nag-hisgots. [19:02] So, let us discuss about ana nga product wave. [19:09] Sige, um, yeah, [19:10] i-kuan lang sa, i-try to get more information about ani. [19:14] O, na'y kuan, whether we will use. [19:17] Kay ang nganong nag-hisgot pud ko og product wave, I will want all those transcript, nya, amo nang i-feed didto, and then maghimo mi'g bet, [19:27] bet ba nga pusta. [19:29] Oh, pusta mi nga, if kani nga feature atong ning buhaton. [19:36] Ana gani, so na may mga kuan didto, like i- i-set out lang muna, I mean [19:42] kanang prompt and then mao ni ang feature, ani. [19:46] So, mohat i-ni, mohimo mi og bet [19:49] or pusta. [19:53] [19:54] Nakagets mo? [19:55] [19:55] Amo gi-pusta whether kani nga feature is mo-kuan ni, mo-work.
[20:00] Ah, mag-work ni siya base sa katong mga na-interview.
[20:06] Ah, sir, pila ang like, target? At least?
[20:11] The more the merrier, pero the more the merrier.
[20:16] Mga 5 lang siguro kay na.
[20:19] Ako na gi-inform si Yurico para interview.
[20:23] Ah, unsa to, sorry?
[20:26] Ah, sorry, go ahead. Go ahead, Luis.
[20:27] Ah, okay, okay. Ang target
[20:30] makatubag
[20:32] pila, sir, para naa koy kuan, goal,
[20:37] your kuan?
[20:40] Kung mag, kuan ka na
[20:42] 10, maybe,
[20:46] 10, mga 10 gyud.
[20:51] Bale, okay, 10 ha? At least 10.
[20:55] Ayan na lang 5 kay basin kulangan pa gyapon. 10 siguro at least naay kuan, grounds, ba.
[21:01] Ang imohang focus is about ani.
[21:06] Sige, sige. Oh, kanang
[21:09] having um a checklist, especially kung mag-onboard sa client,
[21:15] gamit ba na.
[21:17] And then, siguro pwede nimo i-expound nga
[21:21] if ever naay checklist,
[21:24] Unsa man si?
[21:25] I mean, siguro ang question is need ba gyud siya, ana, and then if naa gani checklist, unsa may ibutang pod sa checklist, unsa may mga kinahanglan, like unsa man development setup,
[21:36] or unsa kuan ang
[21:39] unsa gani na? Kanang mga documentation, unsay communication plan, scope of work,
[21:46] mga ingon ana. I don't know kung maka-relate mo nako. Probably si Victor ray maka-relate nako.
[21:52] mga scope of work, communication plan,
[21:55] mga leaves, mga ingon ana nga stuff.
[21:59] Oh.
[22:00] Kay actually, ang communication plan ang pinaka-importante diha.
[22:04] Kay, like for example, kung naay mga issue, kinsa man imohang kuanon?
[22:08] Kanang i-emailan or i-message? Ang CSM ba or ang client?
[22:13] Kana. Sakto gyud na. Kay ako kay na-member man gud ko sa 911 nga tawagan lang ko sa WhatsApp over Sunday, para i-fix lang.
[22:22] Ah, kung naay mga issue, kinsa may unang mosugat? Ang CSM ba, or ang Usually, kamo.
[22:28] Kay, walay may PM, typically, sa mga project.
[22:34] Wala.
[22:35] Oh, 'di ba? Unless kung naay moy PM, so PM ang mosagou na, siya'y mo-filter before niya ihatag sa Dev.
[22:42] So, mga ingon ana nga stuff, 'di ba?
[22:44] So,
[22:47] Kana.
[22:51] Sige, ah, next item.
[22:57] Sige, next.
[22:59] So, I think mao na to kang Luis. Nya, kang
[23:03] ang Bernard, is kanang, ya sugud, na ba ka og implement adto?
[23:09] Bernard, sir?
[23:10] Ah, yes, nag-start nako and then
[23:13] mag-refine lang ko later and possibly the end of the day kay
[23:18] mag
[23:19] create na og pull request.
[23:21] Okay.
[23:23] Unsa gani to imoha kuan?
[23:26] Ang katong expectation, sir.
[23:29] Oh, pwede ba, tan-awon nako to balik? Sorry.
[23:32] Ah, d'ra.
[23:35] Mhmm.
[23:38] Ah,
[23:44] crude nga expectations. Mao ba ni ang katong naay mga job grade 1?
[23:51] Sakto ba?
[23:53] Ah, yes sir, kanang.
[23:55] Ah, okay.
[23:59] Oh, my god.
[24:02] Morag mas ganahan ko ani kaysa AI, nya na lang siguro. Actually,
[24:08] I think last week morag nag-unahon na ko, nakahunahuna na ko ani after mi sa atong meeting, ana ko nga ngano kinahanglan gyud nato og crude, bitaw, para sa expectations.
[24:19] And then, I I, nyan, nag-unahon na ko ba nga
[24:23] naa ra man to sa excel sheet tanan.
[24:26] And then, ingon ra ko mag-upload,
[24:28] Over-engineered.
[24:31] Ingon nako mo-upload na lang ba?
[24:33] Nga, what if excel na lang gyud akong i-upload, why do I need this one?
[24:39] Pero, na sad sa akong atong back-up og akong unahunaon na mga
[24:47] what if naay, you know, kanang scenario is kuan na pod siya. Like, what if naay mga pressure threshold or like naay i-add, like, dayon.
[24:57] So morag ba, kani siya is more of like alternative, bitaw, aside sa pag
[25:03] upload og
[25:05] excel nga worksheet,
[25:07] nga pwede nako i-diretso na ang kuan,
[25:11] ang
[25:14] ang katong mga categories and skills.
[25:21] Yeah, what if wala sila, pero pwede naman sad sila mo-download nya i-upload.
[25:28] Pero mas nindot sad 'di ba kung naay visual representation pod? Kay ang excel is wala gyud siyay visual. Puro ra ni kuan, mga cells.
[25:36] Although naay drawing diri, ah sorry, ha. Nag-describe ra ko ron sa kuan na, kay 'di pa nako ni ipakita for now.
[25:43] Ang kuan, growth framework 3.0.
[25:46] 'Di pa ni siya kaayo, ah, I mean final, kay na pa may gi-review.
[25:51] But ang idea lang is that,
[25:55] um, yeah, kani ba, oh kani of course. Job grade 2, under nga metrics nga leadership. Mao ni gi-expect for a job grade 2, nga team savvy problem identifier and communicator. Oh, kana.
[26:08] So, sa karon,
[26:10] kana siya nga meaning diha, it's up for interpretation. Morag tag mga kuan ani ba, kanang mga attorney, bitaw, nga we're free to inter, morabag mo-interpret lang ta ani, but wala ta kay, unsa'y, unsa'y
[26:23] maka-ingon ka nga team savvy ka?
[26:26] Unsa nang savvy?
[26:29] Savvy problem identifier. Unsa ba na?
[26:35] So,
[26:37] Gibuhatan siya og
[26:40] kuan,
[26:45] By the way, daghan na ni'g token ang makaon, Bernard?
[26:51] Um, sir?
[26:53] Daghan token ani. Inig implement pa na nimo nga crude ba, daghan na'g token.
[26:59] Ah, currently sir, kay ako ang personal AI ang akong gigamit
[27:04] for implementation.
[27:05] Unsa nga AI?
[27:07] Ah, Claude sir.
[27:08] Claude?
[27:10] Ah, yes sir.
[27:11] Wala nimo gi-provide'an og kuan, like, katong sa open code?
[27:14] Wala.
[27:15] Open code? Wala, sir. So, kana pud ang isa, sir, kay personal ra tanan, sir.
[27:20] Mag-approach sa imoha, ana ni Sir Lloyd?
[27:24] Ingon si Sir Lloyd sa akoa, diay?
[27:26] Ah, moy na-mention niya yesterday, ah. Sakto to.
[27:30] Ah. Ah, naay may concern.
[27:33] Okay.
[27:36] Okay.
[27:40] Sige.
[27:41] I, ako lang na i-kuan na, kanang, kay ang
[27:49] kay tood gi-provide'an mo og kuan.
[27:53] Ay kay baw na ko.
[27:56] I know why. Morag okay ra siguro, kuan, open code siguro.
[28:02] og gamit.
[28:07] Ani mo god, ang kuan na, kanang morag context lang nga para sa uban. Ang, ang kanang, any member sa iFress Learning, dapat
[28:14] ani mag, dili pwede mag-work sa mga internal tools.
[28:18] Okay? So, mao na nga dili, yeah, this this might be the reason nga dili mo matagaan og Claude nga kuan, account, sa full scale.
[28:30] Oh, I remember.
[28:33] So, ang kuan na lang nato, possible nga work-around is katong sa open code.
[28:41] Mhmm, yeah, I, I'll try to kuan sa ana, kanang nga AI nga stuff, ha.
[28:48] Okay, wait, let me take a note ana, maka-limot ako.
[28:54] To on.
[28:57] Um, growth framework.
[29:00] about kuan
[29:02] AI account,
[29:05] passive, kuan, open code.
[29:10] Ma, sige.
[29:16] Ah.
[29:17] Moving back ani'ng crude.
[29:22] Mhmm.
[29:37] So, morag lain purpose ya. Ya, it admits, create and retire expectations.
[29:48] Ang word nga expectation 'no, kay mao ni ang sa growth framework na 'no? Ah, growth, growth portal 'no? Ang kanang expectation.
[29:58] Ah, yes sir, ang kanang sa
[30:00] kuan sa
[30:01] Okay.
[30:05] Expectations
[30:13] leadership siguro 'yung leadership is the functional
[30:18] oh yeah functional din, diretso na 'yun siya mga expectations.
[30:24] E-con pa 'yung p- pwede paligoag 'yung mga metrics sa kuan gani, technical gani.
[30:32] And then yeah okay, tan-awa ang job grade 1.
[30:36] Debugging is ano, 'di ba?
[30:41] M- okay, morag siya
[30:44] ang
[30:47] Okay, you have the competency, then functional
[30:52] competence
[30:53] okay
[30:54] siguro, I don't know unsa 'yung mo-ta, metrics siguro okay, let's say metrics and then we have the functional competency.
[31:02] Then more, introduction to, murag gisaagol man gud 'to.
[31:06] Maglibog na ta ba.
[31:09] Dapat unta ang ibutang ra dira 'yung unit testing and then naay ibutang diri nga kuan like,
[31:16] yeah expertise.
[31:17] Unsa may ipasabot expertise?
[31:20] So, unsa, tan-awa expertise of in unit testing.
[31:23] So, job grade 2, unsa may na sa job grade 2 sa about unit testing?
[31:30] proficiency. Okay.
[31:33] And then job grade 1.
[31:36] Unsa 'yung job grade 1?
[31:38] Wala?
[31:39] About unit testing?
[31:40] Murag introduction.
[31:42] introduction.
[31:44] Okay.
[31:45] So, basic unit testing then proficiency then expertise.
[31:51] And then, yeah, ato sa na, okay. Ang sunod sa job grade 4, unsa,
[31:58] expertise pod?
[31:59] O job grade 4, then 'yung kuan, oh. Oh.
[32:03] Wala na.
[32:06] Automated testing proficiency.
[32:10] Okay, automated testing proficiency.
[32:15] Kaysa
[32:16] mag-uni- actually automated naman siya in a way, pero sige. Ang job grade 5, unsa man, about unit testing?
[32:25] Wala na?
[32:27] Kay, dili?
[32:29] Wala na 'no, dili na siya mo-test kung naaka sa job grade 5.
[32:35] Oh.
[32:39] So, okay.
[32:41] Job grade 4, usually mga mid-level na.
[32:44] Job grade 6 wala, oh naana oh. Balik nasad, mastery.
[32:49] So nalapangan.
[32:52] So meaning, dili mag-unit test ang job grade 5, job grade 6, pwede.
[32:59] Sige, oh.
[33:00] Kit-anan ninyo ang kuan, oh isa sa mga problem, dia.
[33:05] Oh, kuan. So, again, that's kuan, yeah.
[33:09] So, medyo kuan siya.
[33:13] Kung ako, as kuan, kung maghimo ko ug mga like,
[33:17] kuan ana, maglibog gyud ko.
[33:21] Oh, e- [unknown] 'yung, accelerator.
[33:23] CI/CD strategy, CI/CD transformation leader, so unsa 'yung difference sa 'nong duha?
[33:30] So, na 'yung scalability architect.
[33:34] Oh, yeah, daghan kaayo 'g mga wording, mga kuan.
[33:41] 'Yung tan-awa sa job grade 7. Naa silay kuan oh, kanang solid principle application.
[33:48] My God.
[33:51] Di pa magamit ang solid principle, inig job grade 7 nimo.
[33:55] So, gusto bi, adto pa na didto sa kuan, sa job grade 1 pa lang daan.
[34:01] So, kana. But anyway, sige.
[34:05] Okay. Go.
[34:09] Murag nag-una-una ako, kaning bitong kuan ni Bernard ba kay
[34:17] ani man gud rona. Hanggang level bitaw kay igo ra gyud siya upload-an ug kuan kanang Excel file.
[34:23] Unya ma- ma-define niya unsa 'yung gina-expect kada job grade 1 and 2 and 3.
[34:28] So, if we are going to implement this one,
[34:33] Unsa na 'yung ni siya?
[34:36] Asa may mas- siguro 'yung question is asa may mas dali, 'yung mag-upload or naay tay crude?
[34:44] What do you think?
[34:47] Ang pangutana ninyo is how flexible are we?
[34:51] Naa ba tay lain sudlan nga taw, naa ba'y lain sudlan nga description, naa ba'y sudlan lain something?
[35:00] So dinha ma-boil down okay si crude.
[35:04] Mhm.
[35:05] And uh sa upload,
[35:08] pwede ra man sad kay dali ra in one go.
[35:11] Oh.
[35:12] Oh, muna,
[35:14] uh sige uh, Levi to Harvey Morgan. So this is, sige, sige.
[35:17] Sige, ikaw. Sige, sige. Go ahead.
[35:19] Okay, so
[35:20] so, if upload na sad 'yung katu Excel kay,
[35:23] uh, na ba siya capability or ma- maka-update sa ana ni?
[35:27] If wala 'yung crude,
[35:30] naay ability?
[35:32] capability if kuan 'yung e-update 'yung job grade gani?
[35:37] O mag-upload or fix na gitaw siya katong if upload pa?
[35:41] Dili.
[35:42] Dili. Um, ani siya ang kuan, kanang bitong mga kuan gani, mga competency is dynamic gyud na siya gyud by kuan, kay,
[35:51] like for example, kanang bitong cloud computing, kaning very basic sample gani.
[35:56] Sa una, ang cloud computing para ra gyud na siya sa kuan, kanang mga senior.
[36:03] Okay.
[36:04] Sa una, kung maghimo ka ug skill profile, ang cloud computing usually mugawas ra gyud na didto sa mga senior level.
[36:12] Karon, ang kuan cloud computing mugawas later on, na na-himong na siya for mid.
[36:17] Nya karon, murag gina-expect na na siya sa mga
[36:20] even kaning junior.
[36:24] Okay.
[36:25] CI/CD, another example. Sa una, senior ra na, oh mugawas na, kuan kay usually si senior
[36:32] si senior ang mo-kuan mo-deploy.
[36:35] Karon, pwede na siya i-expect sa mga junior.
[36:38] CI/CD.
[36:40] Yeah, uh, DevOps, yeah senior or DevOps, that's kuan,
[36:46] um, yeah, that was before, pero karon 'di ba gina-expect mo nga mo-deploy na mo sa Vercel.
[36:53] 'Di ba? Or GitHub Actions, may na na.
[36:57] GitHub Actions, may na na.
[36:59] Okay, so, pwede na na siya sa junior.
[37:02] But before, 'di ba daku ka kuan ang junior 'di na pa-deployon gyud. Ang senior ra gyud ang mo-deploy.
[37:09] Oh.
[37:11] Sige, so yeah to answer your question kung kuan, kanang
[37:17] unsa na, kanang ba ang capability is kuan siya kanang like immaculate? No.
[37:23] Dili siya immaculate.
[37:25] Ang mga items diha.
[37:28] There could be kuan, like for example, kanang bitong AI, before wala may AI nga skill,
[37:35] AI usage. 'Di ba?
[37:39] Karon, murag nagina-hinay naman siya mogawas sa mga skill profile.
[37:44] Ang AI.
[37:46] Yeah, 'di pa gyud lang sa senior,
[37:49] dala tanan.
[37:50] Oh.
[37:52] Murag tanang- tanang job roles, kung mahimo, dapat kabalo mogamit ug AI.
[37:59] Oh.
[38:01] So, balik ta ani.
[38:03] Sorry guys, nagbalik-balik ko.
[38:07] I'm trying to kuan, 'di ba unsa pay laing use case gani?
[38:12] Ang nakita lang gyud nako nga use case ani is that um murag
[38:16] alternative ra gyud siya nga kanang bitong naay e-change siguro like dinalian.
[38:23] I mean, kung wala siya'y copy atong kuan gani kanang
[38:30] kanang Excel file.
[38:33] And then, the only way is yeah, using aning crude, kuan ni Bernard nga pwede na ako e-edit didto.
[38:39] Ma-edit na ako.
[38:44] But ang
[38:49] Hello.
[38:51] Pwede ra man sad gyud nian,
[38:53] Inig-upload pwede sa nako e-download,
[38:57] murag siya ug kuan.
[39:01] rules engine.
[39:07] Okay.
[39:08] Pwede ra gyud siya gyud. Murag siya, rules engine gyud.
[39:17] Yeah.
[39:18] Uh, uh.
[39:24] Inig-upload,
[39:26] wala.
[39:28] And then, matawag man god siya'g, ma kuan Harvey, kanang ma-decouple sa business logic ba, kay imo man ni
[39:35] Murag matawag gyud siya'g katong imong giingon, rules engine, kay ma-decouple man siya, nya murag matawag ug stand-alone, nga dili part sa critical decision making sa
[39:45] core.
[39:47] Oh.
[39:52] O bitaw, o, sakto pod da, 'no? 'Di, kay.
[40:02] Morag ikuwan sa siguro ni nato ah
[40:20] Iya morag ikuwan sa siguro ni nato ah
[40:25] old lang sa
[40:27] old lang sa ang pag implement
[40:30] before yeah, kay karon wala ang ako lang gina kita na lang gyud ni iya nga kuan
[40:38] use case which is dili ra kay pud siya kuan gani like
[40:42] kuan man pud siya nga use case, kanang bitaw naay i-add, or naay i-add dinhi na like
[40:48] it might happen like
[40:50] once every year or once every 2 years
[40:57] yeah, eventually once you uploaded katong ng mga rules mahog
[41:02] katong growth framework,
[41:06] i-upload na lang ka, what if mag edit na lang ka nimo? I-download ra man siya, den i-edit nimo, den i-upload balik,
[41:12] den basahon balik ni kuan i-ay.
[41:18] And then inig kuan nimo
[41:26] okay.
[41:28] Hold lang sa.
[41:30] wala pa koy ma
[41:31] unless na kay nahuna-hunaan Bernard
[41:34] like
[41:37] nganong mag need ta, mag need na gyud ta ani?
[41:46] Okay, uh I think I think the old na lang siguro sir, since wala pa man sad naabot ang Growth Framework 3
[41:53] Oh.
[41:56] How about the address? Unsa may inyong panan-aw pud?
[42:03] Okay, you won.
[42:04] Aside ni Clee,
[42:08] like ni Kent, ward, ni Lawrence, ni kuan unsa may inyong kuan pud?
[42:15] What ba?
[42:16] ako
[42:17] ako ko sir morag
[42:18] dili man kay ingon nga kailangan pa kayo kay based sa
[42:22] pangutana nako sa mga CSMs kay
[42:25] ang uban ba po man ni reply, pero si Christian Arches kay ni reply,
[42:29] ang last niya gamit ana kay last year.
[42:34] Asa ani?
[42:36] Kani.
[42:37] Kani gyud na objectives. Kani, kani gyud na objective. Oh.
[42:41] Okay.
[42:44] So,
[42:45] pero sa,
[42:46] sa uban, dili gyud mo reply sir.
[42:49] Bisag unsa, follow-up.
[42:51] Sige lang.
[42:53] Okay na na guys, uh I ma-anad gyud mo ana, kanang bitaw, morag mo og mga kuan run kanang bitaw
[42:59] na malikay og kuan gani, kondo.
[43:02] Ma-anad gyud mo og kuan kanang i-
[43:08] i-declined.
[43:11] Kuan man gud ni siya, patibayan ang loob.
[43:16] Sige.
[43:17] How about the address, unsa may inyong panan-aw? Kanang bang
[43:23] given ang ato nga mga situation ba, like what if i-upload na lang,
[43:28] og mo mag change, nya kani morag
[43:33] yeah, it looks good.
[43:37] Hey, ani man gud guys, kanang kung dili sad nato ni pangutan-on ang mga question no, kay inig present nako ni ka ma'am no, kabalo ko unsa'y isagpa nako sa, unsa'y question niya. Una,
[43:48] what if kung dili na lang nimo buhaton?
[43:52] I-upload na lang diretso.
[43:56] So ingon ana ang kuan mga, istorya ba.
[44:01] Kay mas worse pa gyud to,
[44:03] kung si ma'am ang mo istorya ani.
[44:10] So sige, i-i-kuan lang sa nato Bernard,
[44:15] hold,
[44:17] hold lang sa, hold.
[44:19] Okay sir.
[44:20] Oh, i-hold sa nato, ah before naay makita gyud ani nga
[44:24] maayo nga use case gyud.
[44:30] Sige.
[44:32] Um, anything else, um, Harvey?
[44:35] Lolo, busy na man day.
[44:36] I think wala na pud sir kay katong kang Cleint na proficiency is i-hold na lang
[44:41] pod ni, I need na siya og further, diba Cleint?
[44:45] Uh, yes sir, hold sad gihapon sir, kay in connection ra ni gihapon sa objectives.
[44:49] Need pa og further discussion.
[44:52] Morag,
[44:54] O, proficiency sir.
[44:57] Ay oh. Yeah, yeah, yeah.
[45:00] Sige.
[45:01] Ah, wait, wait sa una ha,
[45:03] kay
[45:05] ang proficiency is actually part na siya sa mga framework, katong
[45:09] yeah, which na define na namo na sa kuan, sa Growth Framework 3.0.
[45:14] O, na na siya sa wala sa kuan, sa 2.0 wala ang proficiency. Unsa nang
[45:20] expertise, unsa nang mastery?
[45:23] Wala tay ingon ana nga definition.
[45:28] O.
[45:32] Yeah, i-mo balik na lang ta ana, mo balik ta ana.
[45:40] Dugay na kay ga kuan no.
[45:43] Yeah, so mao ra dayto ang sa kuan, Action Item sa plan, unya ang
[45:47] kaning item 1, 4, 5, 7 sir, i-
[45:50] i-up na ang mga PRs ani.
[45:52] Ah, okay.
[45:56] Yes Lawrence.
[45:57] Ah yes sir, sa akoa pud diay katong priority fix, katong sa export,
[46:02] ah na
[46:03] approve na man diay ang kuan, ang PR.
[46:06] Pale ko og kuan na, deploy.
[46:08] Ah yes sir, yes sir, ako na i-deploy after sa meeting.
[46:11] Ah, oh.
[46:12] I-deploy lang, um
[46:15] By the way guys, ah mag mag anad ta og kuan, kanang bitaw mag deploy bitaw ta, nga mag announce ta sa announcement.
[46:25] Hmm.
[46:25] Murag kanang ato lang i-pa announce ana, kay dili kamo ha, si lang, kuan lang,
[46:30] si Lloyd or ako.
[46:37] Sige lang.
[46:40] Cleint.
[46:42] Yes Cleint.
[46:43] Ah siguro sir, sa atong mga sprint sir, i-
[46:46] kanang, diba karon kay wala tay announcement sa mga deployments nato, so,
[46:50] siguro sa, the next nato nga sprint is,
[46:53] is,
[46:54] kanus-a, mag define ta sir, ba kanus-a ting deployment, or
[46:57] kanang naa jud day sir ba, kanus-a nato siya i-
[47:00] kuan tanan, let's say sa kani nga sprint, ana. Pareha pag last, sa,
[47:04] setup diri sa growth,
[47:06] set.
[47:07] Mm-hmm.
[47:08] Yeah.
[47:10] I think mas better kanang bundo, kay usually ang CSM gabi-i man na sila,
[47:15] sa akong pag kahibalo.
[47:16] Hapon, usually sa hapon mga,
[47:18] Hapon, mga
[47:19] 12, o mga 12 na sila mag sugud,
[47:22] 12 to 3,
[47:24] moana, moa start time.
[47:26] Ah sige, dapat mag kuan,
[47:28] kay diba basin naay activities karon nga kuan,
[47:38] kuan mo na, mo i-mo na ana nga, announcement.
[47:46] Pero ang kani, inig deploy ni-niyo no, diretso ni siya sa AWS?
[47:51] na side no?
[47:53] Dili ni siya sa kuan no, sa,
[47:57] katong
[48:00] Azure?
[48:02] Ah, naka disable na to tanan Azure deployment sir, right now tanan, mo point na sa AWS,
[48:07] staging mo og ang prod.
[48:09] Ah, okay. Sige, sige.
[48:13] All right.
[48:14] Sige, i-kuan na lang to, i-i-deploy.
[48:18] Okay, okay sir.
[48:20] Oh.
[48:25] Yes, kinsa man na? Yeah, Luis.
[48:28] Kuan sir, basta interview ang
[48:32] ang results sa interview, asa nako i-compile sir? And,
[48:36] i-
[48:37] i-send lang nako sa imo.
[48:39] Ah, i-palihog i-butang lang siguro sa WorkDrive or sa Zoho, bitaw?
[48:44] Naa pa may ingon ana, kanang Zoho WorkDrive ninyo?
[48:47] Ah, oo.
[48:48] Naa ra sir.
[48:49] I-
[48:50] bitaw, bitaw, para na og ticket sir?
[48:53] Ang unsa man?
[48:54] Ang katong interview ni Luis,
[48:56] what tanan dyan og ticket?
[48:58] Pwede naman, oo.
[49:00] Ah, ah,
[49:02] pa, ah, pa, unsa man?
[49:03] Ah, yes, yes, yes.
[49:04] Buhatan lang na og ticket kay para ma-kuan bitaw, kanang ma-track,
[49:08] meeting po mi.
[49:09] Again guys ah, tanan mga works ninyo, kanang mga kuan, buhatan og ticket ta kay para ma,
[49:16] later on inig basa-basa,
[49:18] na tay mga resibo tanan, para dili sad mo makalimot ba nga ay, di buhat diay ni nako.
[49:24] Unless na may kuan ba inyong diary,
[49:27] or journal.
[49:30] Oh.
[49:31] Pero yeah, buhatan lang ticket ana, mga kuan, and then, yeah, by the way pag himo lang og folder bitaw sa WorkDrive,
[49:39] kanang para sa Growth Portal para didto na mo magbagsak sa inyong mga documents.
[49:45] Sige sir.
[49:47] And everything.
[49:55] Sige.
[50:03] All right, anything else?
[50:08] Wala na, wala na.
[50:10] Okay. Sige.
[50:13] Ya, murag mo kuan lang, wa pami na human gyud sa growth framework ka, kanang 3.0. Ang pag-ginalit ron, kay murag unsa na ron, October, half na gyud sa October.
[50:26] And then, yeah.
[50:28] Pero pag pinala na to na siya, ma-implement within this year.
[50:34] Oh, ana.
[50:37] In time sa kuan before mag-December siguro, kanang party nato. Basin i-announce siya.
[50:48] Sige. So, yeah.
[50:51] Kana ra, guys. Sige, lunch na ta, guys.
[50:56] Wala na, wa. Kaon na ta.
[51:00] Thank you, everyone. Thank you.
[51:01] Bye. Thank you.
[51:02] Everyone. Thank you, thank you.
