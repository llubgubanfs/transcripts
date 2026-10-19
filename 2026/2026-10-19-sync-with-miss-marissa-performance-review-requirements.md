---
title: "Sync with Miss Marissa – performance review requirements"
date: 2026-10-19
type: meeting
tags: [meeting, growth-portal, performance-review, badges]
participants: [marissa, joshua, glen, harvey]
source: "/home/yander/Videos/dsm/[5pm meet with miss marissa]2026-10-19 17-01-25.mp4"
transcriber: gemini
saved: 2026-10-19T17:53:04
---

# Sync with Miss Marissa – performance review requirements

## Executive summary

**TL;DR**
- Reporting lines are shifting: Miss Marissa and Sir Lloyd take over the technical side; Sir Ed, Sir Harvey and Sir Renato take operations. Final decision to be communicated [00:37–01:12].
- Requirement 1, performance review eligibility: interns are excluded from performance analytics, and a manager is required to review only after a minimum number of weeks under them. Both thresholds must be configurable without code changes [03:13–07:38].
- Requirement 2: managers can edit a submitted review (manager only, never the employee) so one-on-one outcomes get recorded [12:09–15:52].

**Decisions**
- Interns are not counted in performance analytics [03:32].
- Client assignments: reviewer required only if the assignment is longer than 2 weeks. Internal projects (Employee DB, Full Scale Learning/bench, Full Scale Training): roughly 3 weeks to 1 month, undecided. Both configurable [04:20–07:27].
- An employee can be under multiple managers in a quarter; each manager who meets the threshold must review [08:44–10:33].
- Manager edit applies to the manager rating or the review itself; the employee cannot edit. Edit is case by case, and originally submitted reviews should stand as much as possible [15:02, 27:39].
- Threshold storage: if Growth Portal has no existing condition in code, add a table/column in the Rocks database (Rocks team gets only the schema change) so there is a single source of truth [21:46–22:33].
- Badge data: message Marissa directly with context and queries; she adds it in production [17:01–17:58].

**Action items**
- [ ] Team: build the configurable minimum-weeks rule (client vs internal) and exclude interns from analytics.
- [ ] Team: check whether Growth Portal already has threshold logic in code; if not, agree a Rocks schema change with the Rocks team [21:46].
- [ ] Team: verify multi-manager eligibility is implemented correctly [10:33].
- [ ] Team: manager-only editing of submitted reviews.
- [ ] Team: filter or clean sensitive performance data out of staging [14:30].
- [ ] Team: fix the User Management filter bug (ticket created by Marissa) [20:26].
- [ ] Joshua: message Marissa directly for badge data/queries.
- [ ] Team: decide internal projects as one rule vs per project [07:27].

**Blockers / risks**
- User Management search/filter did not find the user ("You're not an employee"), blocking admin grant for Joshua [19:15–20:26].
- Staging exposes sensitive production-like performance data [14:30].
- Headcount of 74 includes future hires and past interns; fix via Full Scale Learning query plus override [23:10–25:15].

**Open questions**
- Final reporting arrangement (Lloyd vs Harvey) and meeting cadence with Marissa [01:12–01:34].
- Exact week thresholds, and whether internal projects get one rule or per-project rules.
- Whether the threshold belongs in Rocks (RUX) or Growth Portal code [20:34].
- Terms to verify (possible Gemini mishearing): "RUX" (likely Rocks), "TRACS", "Marisa/Marissa".

## Transcript

[00:00] Currently waiting sa katong growth framework. And then for this week, maybe kami focus-an kani among request... a, kuan... feature.
[00:12] Sige. So, you have HubCap tone, which is under ni Sir Lloyd, 'no? And then,
[00:23] you're waiting for this one, aside from the growth framework, which ang growth framework, you will receiving those instructions from Sir Lloyd also, tama?
[00:33] Ah, yes, yes. Sir Lloyd and ah, Sir Arvin.
[00:37] Sige. I think moving forward, ah, ang mo-handle ninyo, managing you guys would be me siguro, I... I finalize pa namo, but
[00:48] somehow, we have a diff- different ah directive or different direction from the management na um, me and Sir Lloyd would be taking over on the technical side. And then
[01:03] operational-wise would be Sir Ed, ah, Sir Harvey, and Sir Renato.
[01:12] Ah, I will inform you lang kung unsa'y final ah decision. But somehow, we would still be working with Sir Lloyd, not sure lang with Sir Harvey.
[01:22] Nya ang kuan nato um, wala pa ko'y gihuna-huna nga I'm gonna meet you once or how many times a week, but somehow
[01:34] kuan kanang I will be working kuan siguro, more closely with you guys than compare before. But sige, let's focus on the kuan,
[01:46] ah, the requirements here. So, first is improve performance review eligibility logic. So, right now,
[01:55] um, the HR, I think they're somehow kuan pa kanang manually editing
[02:08] our percentage of completion per quarter because if we compare um in Growth Portal, for example, sa akoang assigned, in HR, my
[02:22] my official number of employees to review for quarter four ah quarter three are four, but if you look ah kuan siguro, share-an ta.
[02:37] Log in diri.
[02:51] [screen sharing]
[03:13] Nya, so in here, my count was 5/9, but the official should be four. So, why is it nine? Nine because
[03:22] ah I transition the interns to be under me. But supposed to be ang intern should not be counted as part of the official list to be
[03:32] to be done ah to be kuan ah to have performance review. So, i-note na sya palihug, interns are not
[03:41] to be counted sa kaning performance analytics. Question?
[03:55] Okay, goods. So, nahimo sad sya, instead of So, let's say five, 'no? Kay mao'y official nako kay naa ma'y regular gyud sya nga employees. Ang kaning one was supposed to be not
[04:08] officially included, kay I think ah he was under me, so sa quarter three, that's July, August, September, right? October, November... Yeah. July, August, September. Pero na-under sya nako morag
[04:20] one week before nag-end ang Q3. So, there should be a logic, so mao ni ang gi-discuss pod sa managers
[04:31] nga maybe kung less than two weeks, it should not be counted if that assignment, ang iyang pag-assign gani under me, is is less than two weeks,
[04:41] dili sya, di ko required mo-do ug performance review. So, dapat ang naa gyud diri sa performance analytics, four ra gyud sya, ang official nako.
[04:51] Now, um, so that's why kung more than two weeks, diha pa sya morag officially required ang manager to do the performance review.
[05:08] But I have um, I think this could change sad depending on unsa gyud ang agreement. But what I can suggest to you guys, pwede ba sya configurable
[05:21] ang kani? Like, the number of weeks ba, pwede sya ma-configure without changing the code. So, in case ma-change na pod ang direction, we don't have to change the code, just change the value, configured here.
[05:36] Unya, kaning number two, um internal projects or internal clients, we call that clients man in in ROKS, 'no? But like for example, Full Scale Learning,
[05:50] dili man sya client-based, so dili gyud kaayo ingana kadaghang deliverables, compared to a client-based na assignment.
[06:03] Kani sad, pwede sad sya configurable, if possible, like ang ilahang giingon na more than 3 weeks siguro, diha pa sya mo-require ang kanang manager to rate
[06:16] that employee, pero again, configurable. So, as you can see, kuan sya kanang, more than 3 weeks to 1 month, so wala sya'y definite
[06:30] nga statement nga dapat mao gyud na sya ang number of weeks. So, pwede ba configurable sad ni sya, which is which can be good sad, 'no? So, lahi ang client assignment or external, lahi sad ang internal projects,
[06:46] na configurable, pero naa sila'y gi-mention na Full Scale Learning, so I'm not Maybe you need to kuan siguro, kanang debate among yourselves whether to have
[06:56] um naay internal projects, like Employee DB, is what ROKS, mao ni'y name sa ROKS database, Full Scale Learning is the bench. Um, we also have Full Scale Training, which is different pod sya. Is it configurable,
[07:12] ah kuan, ah per type of internal project? Kaning client assignment, per diri ra man i-ask. Whenever it's client assignment, kausa ra na sya i-configure. But for internal project,
[07:27] maybe you can debate among yourselves whether to kuan sya kanang for internal project as a whole, or individual, Full Scale Learning, lahi ang kuan. But make it simple lang. Ah, ang goal lang ani is kanang
[07:38] ah we don't want to bombard a manager who is having or or who's handling the bench to kuan, to be required nga mag-kuan gyud sya, mag-performance review sa tanan, kay daghan man god, gandoon man god ang Full Scale Learning.
[07:51] Mao na sya ang morag special case for Full Scale Learning. By the way, are you recording this para ma- if in case naay kuan, balikan, notes. Maayo gyud na naay inyong i-record.
[08:18] Nya, ah clarify should who should conduct the performance review based on the employee's assignment. So, kani sya, ah basically, the logic katong giingon, nga the number of weeks, depende gyud sya. Ah, number of weeks, na-assign na sya nimo,
[08:31] kung two weeks ang required, more than two weeks ang required, dapat required gyud ka mo- ah mo-do ug performance review. Now, question: Can an employee be
[08:44] ah under Sir Ed, and under Sir Harvey at the same time during Quarter 3, or a specific quarter? Pwede ba?
[09:02] What in logic? Pwede, yes or no?
[09:21] Like unsa miss, pwede ma-
[09:28] Can an employee be under Sir Ed who is training at the same time under ni Sir Harvey, during Quarter 3, for example? Pwede ba sya ma-under sa multiple managers?
[09:46] Um, base sa amoang kuan miss, yes. Like ah, an employee can have two assigned projects, so I think, yes miss.
[09:58] Yeah, that's correct, so...
[10:00] Ang number of employees diri, dili siya mo sum up jud sa actual nga employees. So, kani si, for example, si Ma'am Mac, na-under siya nako let's say for the, for July to August. Nya pag September, na-under na siya ni Sir Christian, but both of us are required to do performance review of Ma'am Mac because he meets the required kuan man, number of weeks nga ma-under siya or ma-perform, makadumog performance review.

[10:33] So, I think naa na na siya nga logic, please lang ko check ninyo kung correctly implemented ba siya. So, that's number one. Any question for the first requirement? Yes, Harvey.

[10:46] Ah, by the way, Miss, ah Sir Harvey already had an initial thought regarding anang first two item sa one. Kay, niana siya na if e-same na lang daw kuno og kuan, kanang weeks of assignment instead of three weeks ang sa internal projects,

[11:04] Mmm, okay.

[11:06] ...and then i-state nato ang iyang reasons. Pero it's much better siguro Miss sa kato imong version na naay e-pwede ra siya ma-configure.

[11:13] Mm, sige sige. Ah so, you did discuss the two items na already?

[11:18] Ah yes, Miss, recently with Sir Harvey.

[11:21] Mm, sige lang. We'll we'll try to kuan lang to align kung who's gonna do the meeting with you guys, ako ba or si... but again, um, just to give you a heads up na may realignment

[11:38] nga buhaton. Yeah, for number two, allow managers to edit submitted. So, you got the reason why we need to do this, right?

[11:55] Naka-kuan mo unsay context ngano gi-allow ni siya, ang edit?

[12:02] Wala pa, wala pa ko.

[12:04] Sa amo case, Miss, kay wala pa mi kabalo.

[12:09] Okay, sige. So, um, 'di ba when we, uh when we have performance review, kamo mo self review mo, the manager will do self review. Now,

[12:22] after that, mag-one-on-one man ang manager og ang employee, 'no? Right?

[12:28] Mm, yes, Miss.

[12:30] Okay, so naa'y mga kanang discussions nga sometimes lahi ang perspective sa manager, lahi pod ang perspective sa employee. Now, during that one-on-one discussion, there might be some agreements or disagreements between them. Now,

[12:53] naa'y chance na mo-argue ang employee nga, "Sir, dili man gud, Sir. Kanang naningkamot man gud ko. Dapat akong expected ani Sir, mas higher siya nga rate," ana, something like that. Now, for for the manager to somehow, example, naka-naka-kuan jud ang manager, 'di ba? "Oh, sakto man ang akong kuan employee." Or, the other way around, maka-realize ang employee nga, "Bitaw, 'no? Sakto man akong manager. Dapat man diay ko nagbuhat og ingon ani." So,

[13:25] when kuan, ang kaning edit, it's a way for them to write to change the overall, 'di ba naa ma'y overall rating. Um, ari ta sa sa dev lang. Naa ba'y dev ang Growth Portal?

[13:45] Staging.

[13:46] Staging, Miss. Staging.

[13:49] Staging? Staging, then Growth?

[13:52] Then GP, Miss. Then GP, then Growth, then full scale. Full scale then TRACS.

[14:01] Full scale.

[14:02] So, dapat mo-allow siya og edit para if in case naa silay na-agree nga wala bitaw nasulat at the first, 'di ba, first part sa paghimo og review, ma-kuan tu siya, ma-take into account, mao man tu'y importante. So, kung nakuan naa siya diri, mag...

[14:30] Mokita lagi ang kuan, ang actual sa staging. Sa production, allini ninyo gi-filter? Makit-an diay mo sa mga performance. Aso, inyo na siya tarungon, do. Inyo na siya i-filter, kay naay mga sensitive information. Kanang performance, very sensitive na. So, I think unsa, apil na sa inyong pipeline ha? Limpyuhan ninyo.

[15:02] Sige lang, ato lang na puhon, but kani siya, example kani, mao na akong gi-rate ni Charm, dili man ko ka-edit karon, tama?

[15:14] Yep.

[15:16] Mmm, dili ko ka-edit, so need ko mo-edit para kung unsa to'y among gi-agreehan nako nga kanang we are... nga mao na mi, bitaw, 'no? Or si Charm ba ron mo-agree sa akong gipangsulti, ma-record, put into record siya. Mao na siya ang goal ana, ma-put into record. So, ma-edit ni siyang manager rating or maybe the performance review itself, 'no, the actual jud siya nga performance can be edited by the manager, but not the employee, ha? It's only the manager who could edit.

[15:51] Ah, okay.

[15:52] Okay, so that's the context why. Gana. So, questions? Naay isa ka-away. All right. Ang katong mga mga request, goods na man ni siya, 'no? Kani sa Growth Portal na L3 computers, goods na ni siya. Uh, what else?

[16:23] Um, I think naa'y concern si Sir Joshua, Miss, katong need ang imuhang admin account.

[16:31] Sa asa gani?

[16:33] Ayy, kuan Miss, um it's regarding the adding of the badges, Miss, uh because right now uh only admins can add a badge or those with access to the production database because uh I asked Sir Lloyd about it if he could do the query for me, but he redirected me to you, Miss.

[16:57] Ah, just today?

[17:00] Ah, yes, Miss.

[17:01] Ah, so mao to'y akoang, yeah, moving forward, murag ako na jud mo-direct supervise ninyo, para, pero, so, ni-uh just kanang message me directly, Josh, kung unsay need, uh like query. Give me more context, na, so I can also give you what you want.

[17:25] Sige, Miss.

[17:26] Mm. So, that would mean ako ra'y mo-add ani sa production, kaning mga badges?

[17:35] Ang data lang, Miss, pero ang graphics ana, Miss, kay via sa TRACS, so naa, naa na ang, na-merge na ang PR for the graphics to main, pero ang data kay wala pa siya sa prod, Miss, kay need man og admin.

[17:55] Mm, sige. Uh, message me na lang.

[17:58] Sige, Miss. Thank you, Miss.

[18:00] Mmm, kuan. Kana. So, kana lang sa for now? Um, any questions? Ako na'y question. So, ang nag-handle ninyo, ang nag-PM ninyo is si Harvey, 'no?

[18:16] Both, uh, Sir Lloyd missed asked me to be a team lead sa kani na kuan.

[18:22] Team lead, okay.

[18:24] Sige, um, unsa inyong schedule jud? Naa mo'y daily stand-up meeting?

[18:31] Yes, Miss. Naa, Miss.

[18:32] What time?

[18:33] 1:30, Miss. 1:30 PM.

[18:35] Ah, 1:30. Sige.

[18:44] Ah, hello, Miss, ah katong pag-access ni Joshua sa admin, Miss, ba, pwede ra nimo siya tagaan og kuan, Miss, time-bound access sa GP para nimo syang admin for...

[18:58] How do I do that?

[18:59] Adto ka sa settings, Miss.

[19:02] Settings. Sige, let's do that now na lang.

[19:05] Employee...

[19:06] Employee... User Management?

[19:10] Ah, then search first name.

[19:15] Joshua... You're not an employee.

[19:23] (laughs)

[19:26] Bagsik ba.

[19:28] Ah Miss, i-kuan lang siya ang filter, Miss, kay bag-o na siya, Miss, ang kanang filter system.

[19:33] Remove filter? Unsa man na?

[19:35] Ah, change lang nimo siya, Miss, into something else.

[19:38] Okay. Role, unsa man ni? Regular? Nothing is happening. Wala.

[19:56] I think need koma-under nimo, Miss, I'm not sure.
[20:00] ... what is the logic?
Gigat man pod ka, no?
Ah, okay.
Uh, wait.

[20:10] Dili, o-o, kuan.
Kuan, naa sa web. Walay sa mobawas, no? Dapat ba naa, Dili?
Ah, yes, Miss. Dapat naa.
Dapat naa, Miss.

[20:26] Sige, so, created ticket.
E-fix ninyo.

[20:34] Also, Miss, question, Miss, ba?
Sa performance review gani, Miss, sa side? Uh, sa atong pag-configure nato atong 3 weeks, barog, anaa. Dili ba sya sa RUX nato sya i-kuan, Miss? Kay silbe ang performance review, sa RUX. Pero sya gikan nga kuan, then sa Growth, kay silbe UI lang sya?
UI, oo.

[20:58] Yeah, that can be one possible implementation, no? Pero, mahog man gud, RUX is where you're saving the data, right? Now, the condition between 2 weeks and 3 weeks, where are you getting that? How did you kuan, kanang, decide? When did you decide na tani is under niya, sa RUX, moana?
Sa RUX.

[21:30] Naa'y condition set sa Growth? No condition set?
Ah, wala pa kayo kuan gud, Miss, kanang context.

[21:46] Sige, e-double check daw. Okay, if there's no condition nga maka-, murag naa na'y in-control of this, ah, pwede ra nato ma-implement-, butangan og column lang siguro. Mag-add ta og Maka-write, maka-write man mo, no? Pero dili mo maka-create or maka-edit sa column, kay I don't want to kuan sad, e-hatag sya sa RUX, kay daghan sad silang trabahoon. Now, if we can somehow edit the kuan siguro, table, pero e-agree lang nato, we'll give them, ah, we'll give RUX

[22:08] the change, the schema lang, or kanang table na change, pwede ra. At least naa mo'y control, ba, over these things.
Okay, Miss.
But again, database lang sa RUX mag-gami, para usa ra atong basihan. E-kuan lang, e-check daw, naa ba mo'y control ani.

[22:33] Sige, naay logic sa inyong code.
Sige.
Yeah.

[22:58] Ah, by the way, Miss, Sir Harvey, I think is already here.
Hey. Hey, hello.
Hi, Sir Harv.
Hi, sorry, sorry, extended pa among meeting ni kuan, kanang, end. Sige, unsa'y kuan ani, naa-, I heard kanina nga dili na sa RUX, i-kuan, ari na sa Growth portal ang query?

[23:10] Oo, pero I need to kuan lang siguro, Sir, kanang, to check with the Growth portal team to see if the condition, is naa sya sa code? Otherwise, adto na lang sya, mag-butang lang ta, mag-change lang ta og table siguro adto sa RUX, e-save nato ang configuration, kung pila ka weeks na dapat ma-under ang kanang employee sa kaning manager, anaa.
Mm. Ay, naa pa diay ko'y i-add anaa, Marisa, I don't know kung na-cover ninyo. Ang kaning bitaw sa akong end bitaw, 74, naa'y na-add anii nga kanang bitaw, wala pa nasulod sa kuan, sa full scale, like hatag bitaw mga previous nga intern, nga-

[23:50] Mm, yeah, apil sad nang intern.
Oo, mura ba'g ang, ang fix nani bitaw, kanang dili apil ang kanang mga future nga employee.
Mm, apil.
Ma-apil man gud sya, like kanang padulong pa, like, karon bitaw nga di ba naay gi-kuan ron nga announcement nga bag-ong na-hire? Si kanang ma-hire diay.
Na-apil sya'g count.
Oo, apil na sya'g count, anang 74 karon.

[24:15] Yeah, sige.
So, kinahanglan na sya nga, mao na nga nag-thought ko nga ang kanang pod nga mga kuan, kanang nga query kay naa gyud na sya sa RUX. So, dapat naa'y kuan dito query sa RUX bitaw nga i-apil nga da- kuan, kanang, I think sa override man siguro na ang basihan anaa, or something, or something nga ma-, mura'g kinahanglan ang query kay FS learning plus override lang dapat, kay kung wala syay override, dili na, I think, ma-apil ang kanas- silang ma-hire, ma-to-be-now, og kanang mga future

[24:45] na employee. So, kanang tan-awa ninyo, kanang FS learning plus override.
Perang override kay kanang during sales man na sya, so naa'y mga employees pod na wala pa sila'y sales. Sige, tan-awon lang na sya.
Mm, e-tan-aw sya anaa, kanang nga query dapat kanang duha, mao ra'y ma-add sa akoa, ha? Dili kanang FS learning ra. Kay akong nahibaw-an, ang kani silang mga future employee, wala pa man sila'y override, kay dili pa man nato na ma-sell, kay kuan pa man sila, padulong pa.

[25:15] So, kanang akong kuanan, number anaa. Kay unusual kay ako'y pinakadaghan og employee dira. Ah, okay, ang next, ang kanas bitaw'ng ang, unsa na sya? Kanang, more than 2 weeks? Unsa ma'y inyong kuan anaa? More than 2 weeks sa client, and then internal budget kay more than 3 weeks?
Ah, kani sya, Sir, configurable ra man ni sya, so pwede ra gyud usbon ni, but again, wala man syay definite na number of weeks gyud. Especially kaning sa dira, o. Pwede ra ni sya i-usa.

[25:54] Unsa'y ngano'ng o, paha'g ngano'g configurable? I don't know ngano'ng diri sa Full Scale, karon pa gyud ko kuan, kanang Full Scale bitaw, mga ihon anii nga app bitaw, nga dili configurable. So, kina- yeah, nindot na nga direction, nga i-kuan sya as configurable.
Mm.
Yeah, sige, ako lang i-pa-kuan sad sila, Sir, pa-tan-aw kung kaya ba or naa ba'y logic nga na-apil gyud sa Growth ang kanang pag- as kuan ba, pag-require kung asa, or pag-assign asa ni sya nga employee dapat ma-belong during performance review. Otherwise, kanang, it's kuan gyud, kanang sila gihapon mo-buhat, but we're going to have some settings or, yeah, saved in RUX database to, to just query kato nga logic ba, kato nga configuration.

[26:46] Sige.
Sige, kana lang sa for now? Any questions?
None so far, Miss.
Wala ra sa akoa, Miss.
Sige, Glen?
About sa question, Miss, sa kuan sa performance review nga editable, Miss, ba?
Mm.
Ah, question lang, Miss, ha. Dili ba ma-compromise ang integrity sa review, Miss, if i-allow nato sya nga ma-edit?
Ah, actually, we, ah, we already had a thought on that, thought on that, pero, um, case-to-case basis sya. So, ah, it's actually kanang kuan gyud sya, kanang something na dapat ang manager should have this kanang murag naa na syay confidence ba nga mao gyud na iyang rating, but naa man gyud times nga murag ma-oversight nimo, ba. So, let's give them the chance lang to edit. But in terms of credibility, dapat naa gyud na sya daan. Meaning, as much as possible, what we already sent or save as a performance review for that employee, mao na gyud na sya unta dapat.

[27:39] Mm.
Sige, thank you, Miss.
Thank you. Katok lang. Thank you, guys.
Yeah, thank you, Miss.
Thank you.
Thank you, everyone.
Thank you, everyone.
