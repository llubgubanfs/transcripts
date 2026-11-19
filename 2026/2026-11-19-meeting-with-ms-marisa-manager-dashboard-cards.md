---
title: "Meeting with Ms. Marisa – manager dashboard cards"
date: 2026-11-19
type: meeting
tags: [meeting, growth-portal, performance-analytics, grace-dashboard-tiles]
participants: [Marisa, Lorenz, Victor, Clint]
source: "/home/yander/Videos/dsm/[miss marisa 11:15 meeting]screenrecording-2026-11-19_11-21-24.mp4"
transcriber: gemini
saved: 2026-11-19T11:54:19
---

# Meeting with Ms. Marisa – manager dashboard cards

## Executive summary

Recording starts mid-meeting (the recording began at 11:21 for an 11:15 meeting). Transcript source: Gemini. "Rocks" appears as "raks" and a few phrases near the end are garbled.

**TL;DR**
- The "327 members" count on the manager review cards is the wrong number for a manager-level view, because one manager can have many members [00:01].
- Decision: the cards become pure totals of the table's own columns, so cards and rows agree [06:44].
- No new request and no priority ticket for next week. Unit tests next, then back to the training plan [13:53, 15:31].

**Decisions**
- Card values are summed from the table columns. Managers cross-check the cards against the rows in Excel, so the two must match [03:06, 13:06].
- Victor backed it: the table is the source of truth, and it also removes a separate endpoint call [05:17, 06:34].
- The "Members" label becomes "Submissions", counted as submitted over needed (e.g. 2 of 5 books) [10:32, 10:43].
- The Client submission column stays in as always 0 and is not removed. The client requirement ended after Q2 [11:09, 11:23].
- "Review complete" is a completion status, not a submission, because a manager can submit and still not have held the 1-on-1. Lorenz picks the wording [12:23, 12:55].
- Ships as a hotfix, Friday or Monday. It does not carry over to the next grid [11:47].

**Action items**
- [ ] Lorenz: create the ticket for the cards-follow-the-columns change [13:32]
- [ ] Lorenz: hotfix Fri or Mon [11:47]
- [ ] Lorenz, Clint: sort out Clint's point about Sir Igor's submissions among themselves [13:35]
- [ ] Team: unit tests next, then the training plan [14:46]

**Blockers / risks**
- Clint's figures (19.9%, 165 of 700, 327 vs 74) were muddled and set aside without a clear answer [08:18-09:37]. The total-from-columns approach should make them moot.

**Open questions**
- Whether the team joins Rocks work. Marisa wants to check the need first [15:10].

## Transcript

[00:01] Marisa: The 327 members supposed to be dili na siya maoy ang count, kay we can have multiple members man under a manager.
[00:13] Marisa: Naay I don't I kuan, I am thinking nasayup ang iyahang gibasihan ani. Dili 327 members.
[00:23] Marisa: Dapat Um.
[00:28] Lorenz: So ang kaning 327 man good miss, kay 'di ba mao mani ang number of members nga reviewable for this quarter man jud.
[00:38] Marisa: Hmm, pero kuan man siya dili man siya, mura siya, lahi siya nga perspective ba supposed to be. Kay ang employee, we understand na okay there are 327 employees. Ah, ang manager.
[00:52] Marisa: How many managers?
[00:58] Marisa: Mura'g ipakita siguro nato no? Let's say, 10 times, so 10 managers times pila ka number of Mmm, like, bali miss. Ah, as,
[01:10] Lorenz: there is a dialog miss, na may mga duplicate entries diri, if, uh, under, for example, ah, who was that? Harold, Harold Cuenco man to to.
[01:26] Lorenz: Cuenco, kani siya miss. Under siya ni Sir Igor og ni Sir Matt, so diri duha siya ka entry but gi-count na siya as one diri.
[01:36] Lorenz: So ang imung gipasabut ba miss kay bali duha?
[01:40] Marisa: Duha. Hmm. Mura'g, mura'g dako gyud ni miss. kay lahi siya, ang ka-perspective man good sa manager.
[01:47] Marisa: Mura bag, how many submissions? Or ako nga kanang Sir Ed, pila naman ka managers ang naka-officially submit. Supposed to be perspective ni siya sa manager, 'di ba?
[02:04] Marisa: So, this is another kuan siya, another point of view nga the count there should be the number of managers. Now, one manager, um, or a manager submission percentage man good siya.
[02:22] Marisa: Okay. What if, what if lang, we'll just So, mura man gud na siya'g total, supposed to be, or average supposed to be, nga naa sa manager submission column.
[02:40] Marisa: Ah, mura'g, kung imu, kung imu oh, mura na siya'g kanang, if we're gonna compare ba, 'di ba? Supposed to be.
[02:48] Marisa: And mura'g in, in simple way, Um, so, So, that should be the the case.
[02:58] Marisa: Mura siya'g average, 'di ba?
[03:00] Lorenz: Kung inana sad siya miss, should we apply it to this other cards miss?
[03:06] Marisa: Yeah, so akoa, ha? Because that's how it is supposed to be done. Kay mura bag, we'll not complicate things. Mao may na ang naa sa data karon, nga naa sa mga columns.
[03:18] Marisa: Akong akong kanang assumption, each column, naaman siya'y different values per row. Pero that mura'g the total of it. Kung mangutana ko, pila naka book employees ang na-submit? Okay, there are kuan, ah 20 something percent. Pila naka manager submission ang nahibulhat na karon? Pila ang kay, and then I can I can kuan kanang cross check that on on those columns.
[03:49] Marisa: 'Di ba karon, 'di man siya ma-cross check, 'di man siya ma-marelate?
[03:58] Lorenz: Yeah, I think kana nga approach okay ra gud na miss. Atong i-pure total diri siya.
[04:04] Marisa: Ma, nakuha ko kuan sige yes Victor.
[04:07] Victor: Um, originally, asa dini gibasihan kanang employee submission, kanang sa babaw sa card? Asa gyud dini siya nag originate? Naa na siyay separate query or unsa ni siya?
[04:19] Lorenz: Ah query gyud ni siya, Vic. Kay kani mga submission sa rocks man.
[04:24] Victor: Sa rocks ni siya. Nya kani sa ubos, sa Growth Portal?
[04:28] Lorenz: I think most of the data gyud diri, Vic, kay from rocks gyud.
[04:33] Victor: Ah, rocks. Okay. So, uh, kuan na. Uh, akoa, in my own perspective sad, um, ako lang ni i-open, I would also check, kay 'di ba, tanan, kanang diha, kanang naa sa table,
[04:52] Victor: naa naman diha tanan employee, 'di ba? Like tanan employee under to their respective managers.
[04:59] Victor: Uh, i-klaro lang nako, sakto ba ko, Lorenz?
[05:03] Lorenz: Yes, Vic. Sakto na.
[05:04] Victor: So, ani na lang. Um, sakto tong giingon ni Marisa.
[05:10] Victor: Og unsay naa diha sa entire column, mao pud sa babaw for mo-reflect for consistency.
[05:17] Victor: So, kana, also maka-reduce na og call kay as far as, uh, I know, lahi ni og Since lahi man og number sa babaw, so it will it is a different endpoint nga nag-tawag.
[05:31] Victor: So, kani, ma-lessen pud ang endpoint call kay dritso ra ka mo-total.
[05:36] Victor: And since kuan man ni, um, ingana na lang siguro for me kay for consistency lang sa tanan.
[05:46] Victor: So, okay na ta ato, Marisa, sa kato nga kuan. Approch I would kuan sad.
[05:50] Victor: Kato nga approach para 'di bitaw mag-libog kay 'di ba bitaw may ta Like, in a user perspective, 'di lang ta mag-hunahuna nga developer perspective or QA perspective.
[06:00] Victor: Or data, ana kuan.
[06:02] Victor: Mo ana lang ta nga, oh, normal ra ko nga user. Normal ra ko nga manager know-how on something.
[06:08] Victor: So ana na lang siguro para, ah, oo, kuan na day, kanang dapat equal na Mo Mo man gud yung mo-pop up sa UI.
[06:17] Victor: Even though kato ako gi-suggest ganiha, katong question mark, um, mura'g mas better siguro.
[06:26] Victor: Correction, kay amo man koy kuan gud kanang idea sa source of truth, asa'y tinuod sa babaw or sa ubos.
[06:34] Victor: So, ato lay basis sa ubos kay naa naman gyud diha ang total counts sa table sa managers.
[06:39] Victor: Kato na lang siguro.
[06:44] Marisa: Yeah. So, if no one would disagree, let's have that implementation kay um kuan man na siya. Mura'g dapat mo-jive ang naa sa cards ug ang naa sa rows, 'di ba? Mura'g siya kay mao man na ang mura man na siya'g kanang uh, somehow a total or a highlight of what's in each row ba. So, it should jive.
[07:12] Lorenz: How about ang kuan miss? Ang kaning label nga members? Would it still make sense ba?
[07:17] Marisa: Dili siguro kay kani, I think ang ilang gi-kuanan diri ba kay gibasihan gyud nila ang members.
[07:23] Marisa: Nya, lahi man ni nga perspective. Sa employee, pila ka employees, manager, pila gyud ang na-submit na manager, 'di ba?
[07:32] Marisa: Pila naka-percent ang naka-submit, sa client pila naka-percent. Actually ang client gani is dili kay na nato siya need kay wala man nag-require.
[07:41] Lorenz: Wala na ni siya from Q3 sad.
[07:44] Marisa: Wala na na siya. So, ang one-on-one discussion, well if if, kanang another query. That's it. Or base lang gihapon siya 'di ba, dira sa column kay.
[07:56] Lorenz: Oo, miss miss.
[07:58] Marisa: So, kana, make it consistent. Yes, Clint.
[08:04] Clint: As a kuan miss ba, like Ibalik gyud ni sa Q4. Ang akong POV ani miss sa kaning kay Sir Igor nga mga submissions, ang kanang naa sa submission kani nga hard break, 'di ba, sa babaw.
[08:17] Lorenz: Ah, kani?
[08:18] Clint: So, mahog nga ang 19% .9% kay kay Sir Igor pa na siya nga submission.
[08:28] Marisa: Ah gi-filter ba nimo Sir Igor?
[08:31] Lorenz: Wala, all rani.
[08:34] Clint: If ang Sir Igor lang ma-hundred ra na siya.
[08:36] Marisa: Ah.
[08:37] Marisa: Yeah, that's correct.
[08:39] Marisa: Kay Sir Igor ay, pasum, kuan siya divided by
[08:44] Lorenz: Number of managers ba?
[08:46] Marisa: Number of managers, man no?
[08:48] Clint: Yeah, so if ang Sir Igor ra makita, raha siya'y iyaha ra gyud.
[08:52] Clint: Like ma-fit ra siya ba nga sakto ra gyud if i-filter nato kay Sir Igor ba, but if all nato, so basically sakto ra to ang computation niya.
[09:05] Marisa: Di, per member mani.
[09:09] Marisa: Sumani? 19.9%. So 165 of 700.
[09:17] Lorenz: Oh 327 nalang gi.
[09:18] Marisa: 327 na lagi.
[09:19] Lorenz: 327 raman miss.
[09:20] Marisa: Ah 327, 327.
[09:24] Clint: Ang 327 man, 'di ba?
[09:26] Lorenz: Ang akoa siguro kay 74 man diay ang kay Sir. Sige sir, sige, sige. Sayop si Clint.
[09:32] Lorenz: 74 diri.
[09:34] Clint: 74 naman di diri, ano? Tunga to kay 65.
[09:37] Clint: Okay, ignore na lang may kuan, is. Thank you.
[09:40] Marisa: Sige.
[09:44] Marisa: Kuan siguro no, I think um, so looking at the members ba, so ang members diri 36+2, nianaon ba ninyo?
[09:56] Marisa: 36+2+15, mag-lisod na sad og
[10:00] Marisa: wait, wait. Unsa na mag-wait mo or? Straight to the point na lang ni siya.
[10:06] Lorenz: Pointed na ra siya miss, nga kani basically, ma-add ra man gyud ni diri, kani mga of, nga values kay.
[10:16] Lorenz: or bisag diri inig tuplok sa dialogue, naa pa gyud 'yung mga duplicate entries diri per employee, so, e-count na lang gyud na, one by one. Mao na ang e-display diri.
[10:26] Marisa: Um, yeah.
[10:30] Marisa: Yeah.
[10:30] Lorenz: So,
[10:32] Lorenz: Maybe kuan miss, or, an-diri in-side members, kay submissions na lang.
[10:36] Marisa: Mm-hm.
[10:39] Marisa: Pwede na gyud.
[10:43] Marisa: Kay ako, for example, lima ka book akong need, 'nya duha ra akong na-submit.
[10:49] Marisa: 'nya
[10:50] Marisa: ang other.
[10:52] Marisa: So, as a whole, 2 over the overall number of submissions needed, 'di ba?
[10:58] Lorenz: Mm-hm.
[11:04] Marisa: Sige, kana.
[11:07] Marisa: I'm good with that.
[11:08] Lorenz: Okay.
[11:09] Lorenz: Pero, you mentioned miss, nga wala na kiniy gamit ning client submission?
[11:12] Lorenz: Kani pud, kani nga column?
[11:14] Marisa: I zero na, always, no.
[11:16] Lorenz: Um, from Q3 miss, although, Q2 na 'to siya'y
[11:20] Lorenz: may submit.
[11:21] Lorenz: kani.
[11:22] Marisa: Ah, okay.
[11:23] Lorenz: Nalimtan na kinsa.
[11:23] Marisa: Ayaw lang na e-remove siguro.
[11:25] Lorenz: Okay, okay.
[11:32] Lorenz: Oh.
[11:32] Lorenz: So next grid na ba na siya ma-carry over, miss? Or e-kuan na siya karon?
[11:36] Marisa: If mad...
[11:37] Marisa: Uh,
[11:39] Marisa: dili madala.
[11:42] Lorenz: Murag, I think,
[11:45] Lorenz: dili gyud 'to.
[11:47] Marisa: Ani na, ani na lang. Matawag na siya'g hotfix, 'di ba?
[11:51] Marisa: Um.
[11:52] Marisa: So, maybe we can og dili na madala ra, maybe,
[11:56] Marisa: ugma.
[11:57] Marisa: or Monday.
[11:59] Lorenz: Pwede.
[12:00] Marisa: Uh pwede miss.
[12:01] Lorenz: Pwede ra guro, Friday or Monday.
[12:03] Marisa: Pwede man.
[12:10] Marisa: Sige.
[12:10] Lorenz: Ay.
[12:11] Lorenz: Oh, kani diri diay?
[12:14] Lorenz: Mo-make sense pa gihapon ang submission sa ni? Review complete.
[12:18] Marisa: Kani, importante ra ba na. Uh, review complete
[12:23] Marisa: kay, submission is different from complete nga, kuan 'di ba? Katong nag-click gyud sila'g complete.
[12:30] Marisa: Mm-hm.
[12:30] Marisa: Okay, so status na siya.
[12:32] Lorenz: Ah, so status no? Completion status?
[12:34] Marisa: Oh, mhm, okay, review complete, sa, to your manager.
[12:37] Lorenz: Ah, completed na lang.
[12:41] Marisa: Mm.
[12:43] Marisa: Kay pwede man siya mag-submit sa iyahang review, pero wala pa na, ka-1-on-1, wala pa na, 'no.
[12:53] Lorenz: Sige.
[12:55] Lorenz: Dali ra guro ma-kuan kung unsay appropriate term diri.
[13:00] Marisa: Mhm.
[13:01] Marisa: Basta katong inyong kuan, pure count na gyud siya diri, miss.
[13:05] Marisa: Yeah.
[13:06] Marisa: Dapat mag-kuan gyud siya, mag-drive ba, mag-consistent siya nga murag it's easier for managers to cross-check ba nga sakto na ba kanino?
[13:16] Marisa: Kay mao na man ni ilang basihan, kay dinhi na sila mag-excel, kay ang excel sayon ra biya 'to. Pila ka book, managers, oh, ana.
[13:24] Marisa: They're easy ra gyud to use, ba.
[13:32] Lorenz: Oh, amo na lang niya i-create ang ticket, miss.
[13:35] Marisa: Sige, talewok ko, nya you can discuss. Then naay gi-mention si Clint,
[13:40] Marisa: which we can discuss among ourselves.
[13:44] Lorenz: Uh, by the way miss, naa na ba'y kanang, kuan ba miss, kanang uh, priority task for next week,
[13:52] Lorenz: or wala pa?
[13:53] Marisa: Um,
[13:56] Marisa: wala pa.
[13:58] Marisa: So, kuan, sometimes,
[14:01] Marisa: ikaw kahimo, wala man sa'y kanang request karon from uh, managers,
[14:09] Marisa: nga new request, ba? Ang ila lang lang is to be able to use growth portal
[14:16] Marisa: 'nya 'to ilahang previous request, makita 'no.
[14:19] Marisa: So, for the priorities, you can decide among yourselves,
[14:24] Marisa: no question if naa pa ba'y tickets nga buhaton ninyo or gamay na lang?
[14:31] Lorenz: I think gamay na lang, since uh almost kuan na katong uh, last, our this week na priorities, and then I think ma-gear towards ma, uh unit test siguro muna, if wala'y kuan
[14:44] Lorenz: uh wala'y bag-o request.
[14:46] Marisa: Sige, unit test and then, go back siguro sa inyuha nga katong training plan? You all of you have, kuan man, 'di ba, training plans?
[15:00] Lorenz: Oh, yes, miss.
[15:03] Marisa: Although nay, pero raks manggud to.
[15:10] Marisa: Um, I'm thinking bitaw if ganahan mo mo-join sa raks?
[15:14] Lorenz: Uh-huh.
[15:15] Marisa: Pero ako sa, I-check kung
[15:19] Marisa: what's the need.
[15:22] Marisa: Para, murag daghan ra kaayo mga bright diri ba, so sayang inyong points, cells.
[15:28] Lorenz: Pwede ra mag-raks, miss.
[15:31] Marisa: So, kataraw lang, balik, for now, balik lang sa mo, so unit test, then balik lang sa mo sa inyong training plan para ma- ma-practice gyud ninyo. It's so hard na kanang makalimot mo'g coding, and
[15:46] Marisa: murag maka-mga different challenges, lahi man gyud na 'no. Kung tagaan mo'g task, murag maka-encounter mo'g different challenges. You can improve your judgments, technical skills, ana.
[15:58] Marisa: Pero, karon wala pa man gu'y lain request, so, go back to your training plan, and hopefully, in your training plan, it will help you improve or upskill yourselves.
[16:13] Marisa: Sige, so, see you tomorrow.
[16:16] Lorenz: See you tomorrow, miss.
[16:18] Clint: See you tomorrow, miss.
[16:19] Marisa: Bye-bye.
[16:20] Clint: Sige, see you tomorrow. Bye. Bye-bye miss.
[16:22] Lorenz: See you tomorrow.
