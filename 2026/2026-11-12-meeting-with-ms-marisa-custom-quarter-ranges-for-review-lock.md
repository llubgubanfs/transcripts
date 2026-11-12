---
title: "Meeting with Ms. Marisa – custom quarter ranges for review lock"
date: 2026-11-12
type: meeting
tags: [meeting, growth-portal, gp-299, gp-300, performance-review, custom-range-lock]
participants: [Marisa, Lorenz, Victor]
source: "/home/yander/Videos/dsm/[meeting with miss marisa 4pm]screenrecording-2026-11-12_16-00-33.mp4"
transcriber: gemini
saved: 2026-11-12T16:56:44
---

# Meeting with Ms. Marisa – custom quarter ranges for review lock

## Executive summary

## TL;DR
- Performance reviews start next week; HR will announce the self-reviews. Ms. Marisa wants two changes to the review list lock (GP-299/300) shipped by the Thursday deploy, 2026-11-19 [00:25] [20:11].
- **Change 1, custom range per quarter:** when an admin (Sir Ed) locks a quarter, they set its start and end dates, e.g. Q4 = Sep 2 – Nov 15. Only data inside that range counts, including the 14-day assignment rule. The next Q1 might run Nov 16 to January/February [03:04]–[04:30] [10:20] [14:53].
- **Change 2, Custom reviews count:** a manager's Custom-period review inside the quarter's range should count as that quarter's manager review (Performance Analytics "manager review submitted" and the employee-manager matrix score), so managers don't rate the same person twice [04:30]–[09:37] [15:19]–[17:25].
- Why the ranges are custom: merit increases are prepared in November, and people take long leaves in December [12:56]–[14:21].

## Decisions
- Quarter labels stay (Q3/Q4/Q1), because executives only see the quarter, not the range [11:05].
- The custom range is set by an admin at lock time [14:53].
- Nothing changes on the employee side: employees still pick the current quarter, and their client assignment decides where they belong [18:06].

## Action items
- [ ] Team: decide tomorrow (Fri 11-13) who builds this and whether it can deploy Thursday 11-19; tell Ms. Marisa so she can warn managers [19:34] [21:34].
- [ ] Lorenz + team: break it down tomorrow, simulate the scenarios, check the logic, then raise open questions [21:24] [21:49].
- [ ] Team: send scope and level of effort by end of Friday [22:26].
- [ ] Everyone: tell Ms. Marisa availability for a team dinner before the Dec 5 party [23:04].

## Blockers / risks
- Lorenz: "medyo dako-dako jud nga change" (a fairly big change); he couldn't commit to 1–4 days [21:01].
- Deploying changes after the review period starts risks bugs while reviews are live [19:34].
- Victor asked why we don't just follow standard calendar quarters, since custom ranges overcomplicate things. Answer: the merit increase timeline [11:53]–[14:30].

## Open questions
- Where does Sir Ed's Sep 2 – Nov 15 range live? Rocks has unused settings `quarter.type` (Regular|Custom, selected Regular) and `quarter.custom` (per-quarter MM-DD ranges) on preprod; GP reads neither. Is the range per year or per lock?
- Ranges that cross calendar quarters: Sep 2 – Nov 15 overlaps Q3 (Sep). Rocks stores reviews per quarter. Which reviews and decisions belong to which label?
- What does the early Q4 lock hotfix (23b5953b) do now? Locking calendar Q4 (Oct–Dec) is the logic she called wrong [03:04].
- Speaker A (the person asking "kaya in the next 1 to 3 4 days?") is unidentified in the transcript.

## Transcript

[00:00] Marisa: seminar na mag-start?

[00:02] Lorenz: Abi nako'g 2:00 gani.

[00:05] Marisa: 2:00?

[00:07] Lorenz: 3:00 diay. 3:00 ang ending.

[00:10] Marisa: Ending diay. I'm not sure if na-coordinate nako properly kay mao man 'tong gisulti ni Sir Ed 3:00, but it seems like

[00:19] Marisa: ending na diay nang 3:00.

[00:24] Lorenz: Baliktad ang starting.

[00:25] Marisa: Yeah, baliktad. Anyways, um Sige, so I have I need to have an urgent call with you guys kay the performance review will happen next week na.

[00:39] Lorenz: Po?

[00:41] Marisa: So, HR will be broadcasting about uh you guys to do self-performance review.

[00:51] Marisa: Then uh somehow, ma-use na gyud ni ang kani. Mura'g ma-focus na gyud sa

[00:54] Marisa: inyahang updates for the performance review. Thank you, guys, diay for uh pushing this this week, no, nga mahuman siya. Though there could be some improvements based on the stakeholders' feedback.

[01:09] Lorenz: Okay.

[01:10] Marisa: But at least thank you for um thank you all for making sure na ma-deploy nato ang atoang uh performance review nga mga features. So, with that, uh nag-talk mi ganiha ni Sir Ed.

[01:23] Marisa: Um who could show the kuan? Ako na lang so I could also navigate myself. Ako na lang.

[01:34] Marisa: Share screen.

[01:50] Marisa: So, right now I tried to go to Q4. Um but kato, dili siya makita ang lock. Dili ni siya effective?

[02:02] Lorenz: Ah yes, Ms. Um nedidja, Ms., no? Naay lock pod sa next quarter.

[02:08] Marisa: Oo, but it will change. I think the logic will change siguro. Kay ang nahitabo diay, a quarter for us, which is ingon ta'g Q3 is July, August, September,

[02:22] Marisa: would not necessarily mean a Q3 for the performance review. Kay what will happen sa, for example, Q4, um, ka ingon siguro og Q4,

[02:35] Marisa: let's say naa tu siya katong lock, mahug man siya'g start, no? So, ang by default, when when you click lock, it means you're you're getting data from

[02:49] Marisa: July July 1st to November 12, is that correct?

[02:58] Lorenz: Yes, Ms., ang mga eligible sa for review on that quarter.

[03:04] Marisa: Mm. So, ang dili diay, it's it's a wrong uh uh logic. Kay ang ang mahitabo diay kung let's let's say mag-start ta'g Q4, uh we need to really set the start and end date

[03:17] Marisa: kay it will be kuan siya, kanang customizable. So, for example, for Q4, ang gibutang ni Sir is September 2. Why is it September 2 mag-sugod up to November 15?

[03:31] Marisa: Kay November 15 is the last is the kuan man siya, last date before ta mag-start officially. Onya, so that's, 'di ba, supposed to be Q4 is kuan man na siya,

[03:45] Marisa: uh October, November, December, no, ba, in in general. But whereas, dili siya mao. So, uh they have to set the range, so ingon siya, "Okay, lock Q4." And then mu-input siya nga, "Okay, get data from

[04:14] Marisa: September 2 to November 15." So, that's the range ra nga imohang basihan sa katong logic nga pila'y interns uh 14 days ang nga na-assign siya sa manager, ana-ana.

[04:30] Marisa: So, mao na siya ang first na change. Naa'y second is, naa'y times na managers would do uh customization of

[04:41] Marisa: kani, mag-customize sila og performance review. Where do you do that gani?

[05:01] Lorenz: Ah, kuan, Ms., like when mag-create ka'g anang custom lang nga like i-click ang employee, Ms., and then submit. And then submit manager review. Yeah. And like choice 3 to 6. Top.

[05:20] Marisa: Mm. So, kaning custom. Now, naa'y scenario nga, for example, ako, I have a an employee nga anaa under siya nako uh starting from

[05:32] Marisa: say November uh first week of uh first day of November to November 15. Niya para mura'g mu-advance siya og do og performance review para uh dili siya makalimot or, at the same time,

[05:46] Marisa: um whenever nga naa'y mubal- mawala niya nga member nga muadto sa client, iya na 'to i-record, put into record na nga, "Mao ni siya ang akong rating." So, ang uban ana mag-customize. So, 'di ba ingon ta

[06:01] Marisa: ang Q4 is from Novem- uh from September 2 to November 15, uh for example, kani siya. Now,

[06:14] Marisa: uh na-under siya nako November 1, niya muadto siya sa client inig November 16. So, apil gyud siya. Pero ako siyang gi-customize. Question, um do we do we already put into or kanyan, did we put this into record or account na kani siya nga custom is already my feedback for that quarter? Naa na ba na siya?

[06:47] Lorenz: Mura'g wala pa man. Paki-look at...

[06:51] Marisa: Wala pa, no?

[06:53] Lorenz: So, karon, Ms., kay ma-record siya as custom gyud siya nga kuan...

[06:55] Marisa: Custom, no? Dili siya maapil sa kani nga quarter. Pero dapat maapil siya. So, what happens, um

[07:05] Marisa: diri sa report, performance analytics, so mao 'to, dinhi, maapil siya inig lock nako. Kay kon ingon man ako'g September 2 to November 15, that custom quarter will also reflect nga

[07:20] Marisa: kana siya nga member is under me, at the same time, in the employee-manager matrix, na-record na siya nga natagaan na nako siya og kanang performance review.

[07:37] Lorenz: Nata. So, bali...

[07:41] Marisa: So, kung na-rate nako niya overall, for example, kay 2, mu-reflect na na siya. So, dili na ko pangayoon niya, 'di ba? Kani kung member nani nako siya, niya wala pa ko ni-score kay dash man ni, no? Kung member nako, add dash, dash, niya

[07:54] Lorenz: Yes, Ms.

[07:55] Marisa: So, dapat inig mu-start na ta sa katong performance review, niya nakahatag na ko'g custom, naa na koy score atoniya, so I don't have to re-do it. 'Cause I already gave my rating for that person.

[08:18] Lorenz: To ang kuan ana, Ms., is if custom kay ma-kuan kung which quarter?

[08:24] Marisa: Mm. So, ang custom dapat kuan gihapon tu siya, kaning...

[08:29] Lorenz: Considered gihapon...

[08:30] Marisa: yeah, considered as a rating nato for that quarter. Kay ang ang mahatag man gud ana, "Ah, nag-custom na ko, niya pangayoon pa gyud ko'g rating balik. Nga mana man ta'g-grade?"

[08:52] Marisa: So, mao na siya ang nahitabo sa uban kay muingon man ang manager nga, "I already did a custom. Ngano wala man na-account?"

[09:00] Lorenz: Possible pod na, Ms., na mag-grade ka sa custom and then sa quarter pod...

[09:06] Marisa: Mao nang ginabuhat sa uban kay ma-kuan man siya, ma-wa man siya'y, dili siya counted. So, mag-double iyang entries.

[09:14] Lorenz: Different, Ms., no?

[09:16] Marisa: Mm. So, mao na nga to somehow kanang remove that inconsistency or kanang duplication of rating, kay I would do the same rating ra man kay ang akong custom mao ra man gihapon sa akoang rating niya for that quarter, 'di ba?

[09:37] Marisa: So, mao na siya uh ni-change. Um So, mao 'to ang two major items. Now, akong next question ani, if wala mo'y question, kayap ra ba siya apason for next week?

[09:56] Marisa: Yes, Lorenz?

[09:57] Lorenz: Ah, yes. Ah, nang pa-clarify...
[10:00] Lorenz: Pa-clarify lang ko Miss sa katong nag-mention ka ganiha nga ah murag custom range nga ang ma-lock nga values, I mean kanang from September to November.

[10:13] Marisa: Yes, yes.

[10:15] Lorenz: So, murag sa kuan miss no kanang naay from quarter 3 ba in quarter 4?

[10:20] Marisa: Oh, so ang mahitabo ana example mag Q1 ta next year, meingon si ang i-set ni Sir Ed partner Q1 next year mag-sugod siya sa November 16 kay nag-lock man ta 15, di ba? 16 to let's say meingon siya mag-stop January, February or kanang January ana. So, regular gani siya dili siya the typical quarter that we thought of.

[10:50] Lorenz: Mm. So, ang kuan ana miss murag i-configurable na lang ang date range sa each quarter.

[11:00] Marisa: Mm, yes. Configurable siya.

[11:04] Lorenz: Mm.

[11:05] Marisa: Yes, Victor. But we need to kuan gihapon na, associate that nga that's for Q3, that's for Q4, that's for Q1 kay um on the executive side, their visibility is just the quarter not the actual range. Yes, Vic.

[11:23] Victor: So, uh naay question lang Miss. Um since bag-o man ko sa full scale uh last year, and then uh na-fold pod ko'g timingan nga kanang half way bitaw ending sa Q2.

[11:40] Victor: Can I... do we really need kanang dili na dyud ta mo-follow sa katong, I know uh just correct me if I'm wrong, or isulti ninyo. So,

[11:53] Victor: Nganong nganong... question lang ko, i-raise lang nako ah nganong dili nalang dyud ta mo-follow sa standard Q1 to Q4 which is Q1 starts from January and ends with um April, then May to kuan? Nganong, oh, or maybe question too much. Nganong dili nalang gani ta mo-follow sa kanang kuan? Or like nganong maabot sa custom? Kay

[12:20] Victor: Pwede man siya ma-tag, ah, if kuan man lang, kadiyot lang ha, kanang, it... kay ma-overcomplicate man gud siya. I know, I know dyud ma-possible siya. Pero ang logic behind ani ba, ah, nganong like unsa 'to, like the one you said nga ang Q3 nag-start ug something kuan, nya na-end ug November.

[12:45] Victor: So, should we tag that as part na lang sa Q4? Like, ah, throwing out questions lang. Um, feel free to kuan na lang.

[12:56] Marisa: Yeah, so to answer that, I think um trying to understand also on the logic why it should be like that, kay for example, ah so you know know nga the performance review, ang inyong performance review would greatly affect on the merit increase per year. Now, we do the merit increase, uh depende na siya sa executives, no? Dili man siya kanang naay jud tay increase every year, it doesn't mean that way, no? Pero naay chance nga ma-increasan ka.

[13:32] Marisa: We don't do that at the end of December. Nag-prepare na sila'g November pa lang. I-lay out na na nila. So, kanang performance nato from Q1 to Q4, na-kuan na jud dapat, na-butang na na siya sa system. So, they have more time to decide on what to do. Ana. So, it's more on the kuan siya, kanang...

[13:56] Victor: Make sense.

[13:57] Marisa: ...early merit, oo. Kanang...

[14:01] Victor: Kay ah na-timing-an pod to sa kuan, mao de'y to'ng giingon ni Mark Semblante last time nga Novem- around November naa to'y gi-announce for increase. So, mao diay ni siya'y purpose. For naay leeway. Pod di man kay ingong mo-drop ta by December. So, okay, okay, nakuha, nasabtan nako.

[14:21] Marisa: Oo, tsaka Paul said, everyone will have more vacation leaves, so dili na ka-makaperform or maka-one-on-one, ana so.

[14:30] Victor: Okay, okay.

[14:32] Marisa: Mao na siya.

[14:34] Victor: Okay, understandable. So, uh arranging na lang. Pero should we tag the range as putan nato um giingon man ka na custom range, kaning custom range asa na siya na-fall?

[14:47] Marisa: Yeah, so naay custom ha, custom...

[14:50] Victor: Unsay unsay naming ana? Like tag niya?

[14:53] Marisa: Oh, naay custom which is kaning sa pag-lock, um let's say lock Q3, we set at we let the admin, which is Sir Ed, do the custom range nga mao ni ang dates na kuhaon from sa or Q4, let's have the Q4, September 2 to November 15. So, we're gonna get data from those range only. Do not get data outside before or after.

[15:19] Marisa: Only those data nga na kanang included sa kana nga custom range. Now, ang kaning manager dashboard nga mu-do sila'g custom rating, it's another feature man ni siya.

[15:36] Marisa: So, some managers would do, dili sila mu-select og Q4, let's say wala pa nagsugod ang, mahitabo man gud ani, this usually happens when that kanang wala pa jud na-officially start bitaw ang kana nga performance review for that quarter. So, let's say ang official nato nga start is next week, but what if the manager would start na doing the custom kay para dili siya makalimot sad gani, nya mu-end man sad ang iyang member this week, so iyahang gi-start. So,

[16:12] Marisa: Kani, mao ni siya nga dapat ang katong custom nga gi-set, ah should still in that range nga gi-set didto sa Q3 or Q Q4, sorry. Para uh the same, consistent. So, Q4 dapat kuan 'ta siya, kung nag-set siya, "Oh, okay. I will have November 1 to November 12." Nya, di 'ta kaselect sa future, no? For this, so dapat dili na ako pangayoon. So, kani na-create naman ko'y Carmenstito, dapat diri sa kuan, ah performance analytics nako, under na nako. Yes, that's correct. He will be under me. Um, and dapat naa na diri butang, for example manager review submitted. Nya, bisan wala pa 'to ka-submit ang employee, that's okay, but the manager already submitted. At the same time, in the employee manager matrix, naa na koy score ato ni ah Carmenstito. So, kana siya nga duha.

[17:25] Victor: Ah, I see. Kay um previously sa ako uh na-end man gud sa September 16. Gi-pakuan man sad ko ni Mark ato daan. So, ah non- katong ako wala man ko naggamit og date range. So, mao to gi-assume nako, pangutana gi-assume pod nako nga follow ta sa strict Q1 to Q4. So, not aware aning range kay maybe siguro wala ko maka-agi, like I don't know how it works. Mmm, ana diay.

[17:56] Marisa: Ang employee ba maka-custom ba mo or mupili ra mo'g specific nga quarter?

[18:02] Victor: Sa akoa kay kuan, quarter nga naka-assign, kanang current nga quarter.

[18:06] Marisa: Ah, current? Oo, kana, which is okay lang. Like, it still fits our requirement man. Kung meingon tag Q3, nya ah under man ka sa kana nga range nga date nga from September 2 to November 15, then mura rag in the in the background, kuan na, murag no no changes sa employee nga side. Kay na-belong ra man gihapon ka. Ang imong client assignment ra man tan-awon ana.

[18:37] Victor: Ah, okay.

[18:43] Marisa: So, mao na. So, going back to my question, um unsa'y possibility nga pwede ninyo ma-deploy ang changes by next week?

[18:58] Lorenz: Mmm.

[19:02] Marisa: Okay. Who would be doing this? Possible? Possible nga mu-buhat ani?

[19:10] Victor: Si Lorenz kay katong nag-buhat man...

[19:13] Lorenz: Na-ilong?

[19:14] Victor: ...explore sa scope niya, Miss.

[19:16] Marisa: Ah, dili sa katong nagbuhat aning lock ug katong...

[19:20] Lorenz: Ah, for me, Miss, ah I think pwede ra akoa, Miss, since ako man ang nag-gama sad sa lock sad. But yeah, as Vic said, maybe i-explore pa sa ang scope kung unsa'y ma-hilamtan aning nga change.

[19:34] Marisa: Mm, okay. Sige. So, um I I want to get ikuan lang siguro, ug answer from you guys tomorrow. Yeah, i-decide lang sad ninyo kinsay mubuhat, nya possible ba nga ma-deploy nato ang changes kay basig magka-bug ta, nya nag-sugod na ra ba ang quarter, no? Nag-sugod na ang performance review ba. So,
[20:00] Marisa: So,
[20:02] Speaker A: How soon do you uh kuan, Marisa? How soon namely?
[20:06] Marisa: Next week.
[20:07] Speaker A: Like, which next week? Ana na lang.
[20:10] Lorenz: First week, Miss?
[20:11] Marisa: Ana. 'Di ba Thursday man inyo'ang deployment? Ah so, that's okay. Thursday is fine.
[20:18] Speaker A: Mm, okay.
[20:23] Speaker A: Sa kini ra man nga feature, 'no?
[20:25] Marisa: O, katong duha.
[20:28] Speaker A: Um, let me ask... Let me see, Lorenz, Leander. So,
[20:34] Speaker A: aware man sila aning nga changes kay most... Most of kuan... I don't want to dump everything ni Lorenz sad pod. Kana bitaw'ng mas naka-aware.
[20:44] Speaker A: Pero mangutana ko nimo, Lorenz, um
[20:49] Speaker A: kaya in the next 1 to 3 4 days?
[20:56] Lorenz: Um,
[20:58] Lorenz: I can't say for sure without...
[21:01] Lorenz: Yeah, I'll try. Medyo dako-dako jud nga change jud.
[21:07] Marisa: Pero pwede ra man kanang kanang unsa ninyo i-breakdown ninyo ang task ba. Pwede ra jud, but make sure lang nga morag daghang dependency, 'no? Mahuman.
[21:21] Lorenz: Mm-hmm.
[21:24] Lorenz: Ah yeah, we'll try to investigate lang sa karon, Miss, and then by tomorrow, basin naa'y mga open questions ani, and then we'll communicate with you.
[21:34] Marisa: Sige. Let me know lang unsay kuan decisions sa team so I can also give a heads up to the managers na
[21:43] Marisa: ah two weeks na lang or something.
[21:46] Lorenz: Okay, okay, Miss.
[21:48] Marisa: Mm.
[21:49] Speaker A: So try na lang nato um tomorrow, Lorenz, anaa na nato kinsa to'y mga kuan ganahan nimo
[21:58] Speaker A: check. Ah atong i-try ug simulate kung unsa nga scenario. I-breakdown nato siguro. Since murag wa ta maka-record ani,
[22:08] Speaker A: karon, so atong i-breakdown tomorrow. Kay karon naa pa tay utang ato AI something.
[22:16] Speaker A: So breakdown nato tomorrow um check nato logically before nato mag-open tag questions.
[22:26] Speaker A: Nya para at the end of the day Friday maka-buhat sila og kuan, Marisa, kanang
[22:34] Speaker A: scope and level of effort.
[22:38] Speaker A: So kana lang um I know Tila tabangan nato tabangan nato as much as possible we want to kuan cater aning nga scenario.
[22:54] Marisa: Sige, kato lang. Thank you kaayo ninyo.
[22:58] Lorenz: Thank you so much, Miss.
[23:00] Marisa: Ay, before we end, ay, sorry!
[23:04] Marisa: Ako na lang i-insert. Um we're going to have a dinner out, pero before siguro the December
[23:12] Marisa: uh party, December 5.
[23:15] Marisa: Puhon, hisgotan sad ninyo kana'ng uh nga available mo, ha?
[23:22] Marisa: Uh inform me kung madag tomorrow para ma-book nato daan.
[23:28] Marisa: Uh taga-Cebu ra man mo tanan, 'no?
[23:31] Speaker B: Si Harvey, Miss...
[23:33] Lorenz: Nga Medellin diay si RV, Miss.
[23:36] Speaker A: Ah, Medellin.
[23:38] Speaker B: Or Daanbantayan. Medellin...
[23:41] Speaker A: Si Lorenz diay.
[23:43] Speaker B: Naa ra sad sa Cebu.
[23:46] Lorenz: Naa ra man sa Cebu, pre.
[23:51] Marisa: Sige, hisgotan lang sad ninyo, but before lang unta December 5, if it's possible, kay basin mag-long break pod ang uban ba, so dili na hinuon ta magkita.
[24:04] Marisa: Okay. Bye-bye.
[24:07] Lorenz: Sige. Thank you, Miss.
[24:09] Speaker B: Thank you, Miss.
[24:10] Speaker A: Thank you, Miss. Thanks, everyone.
[24:12] Marisa: Bye.
[24:16] Speaker B: Yo!
[24:17] Lorenz: Naka-record ni?
[24:18] Speaker B: Naka-record, sir.
[24:21] Speaker A: Mao bitaw'g nag-kuan ko ganina, murag wa ni-recorder.
[24:25] Lorenz: Naka-record pod sa kuan, ay.
[24:27] Speaker B: Naka-record na sad ko.
[24:29] Lorenz: Botang-bota pod ko'g record, T.
[24:32] Speaker B: Pila'y...
[24:34] Speaker B: Wala lagi nako na-record ang Meet.
[24:36] Lorenz: Walay bayad man gud.
[24:40] Speaker B: Wala ra, unavailable.
[24:43] Speaker B: Wala ma-record sa Google.
[24:45] Speaker A: Kato na lang um sorry, Lorenz, oh, ikaw ang na-spotlight.
[24:50] Speaker A: Ako ra na'ng gi-kuan kay bisan ako naglibog nga, "Di ba ing-ana ba, maka-cause man ug kanang conflict or kanang overlapping man gud." Unya kanang
[25:00] Lorenz: Murag mo-supersede sa growth.
[25:01] Speaker A: O, mao bitaw'g ni ako jud gi-kuan, i-emphasize nga, "Ngano di man ta mo-follow sa Q1 to Q4?" Ngano naay mag- lami, lami kayo'ng, "Ngano naay magpa-special pod diha?"
[25:13] Speaker A: Ingana bitaw nga case.
[25:18] Speaker B: Ngano daw ngano, ngano diay kung mo-follow
[25:22] Speaker A: Bitaw, ngano'g naa may kustom-kustom?
[25:26] Lorenz: Na-fuck up na hinuon ang kuan, ang Gregorian Calendar.
[25:30] Speaker A: Mo-adjust na hinuon ang calendar sa March.
[25:34] Speaker A: Kasabot man ko nga kuan nga mag-increase na sila, maong paawion na lang tanan
