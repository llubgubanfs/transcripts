---
title: "Rocks stand-up: minimum assignment-duration setting and review edit"
date: 2026-10-21
type: meeting
tags: [meeting, rocks, performance-review, gp-285, gp-287, settings, review-edit]
participants: [Marisa, Carmencito, Ethan, Anjelo, Arnel]
source: "gdrive:leander_client_rocks_concern.mp4 (shared by Ethan)"
transcriber: gemini
saved: 2026-10-21T13:21:12
---

# Rocks stand-up: minimum assignment-duration setting and review edit

## Executive summary

**TL;DR**
- Ms. Marisa raised GP's minimum-assignment-duration request at the Rocks stand-up [00:32–02:18]. GP's 7 days is hardcoded and was only ever agreed verbally with Rocks. The goal is one shared rule for Rocks and Growth Portal.
- Sir Carmencito (Charm) is adding a configurable value to the Rocks settings table today, under `performance-review.general` [04:14–08:39]. GP reads it directly from the DB (read-only) instead of through the API [04:51–05:16].
- Rocks also hardcodes 7 days: below that, an employee isn't treated as assigned to the client and isn't part of its client history [02:53–03:11, 05:52–06:10].
- Clint's question about editing submitted reviews: an undocumented backend edit exists, limited to the overall rating [08:41–15:58]. A ticket will be created.

**Decisions**
- Store the threshold as a settings field, not a new column or table [02:18–02:27].
- Add it to `performance-review.general` now and sync it to all Rocks servers. It can be removed later if management decides otherwise [06:32–08:39].
- Value: Ms. Marisa said it's now 2 weeks (14 days), up from 7, because of the large number of bench reviews. Even 3 weeks was discussed [06:59–07:38].
- GP should query the settings table directly; the Rocks team doesn't want GP going through the API, which is slower [04:51–05:16].
- Ms. Marisa prefers not editing submitted ratings (credibility) and suggests recording agreements in the comment field [13:40–14:00].

**Action items**
- [ ] Sir Carmencito: add the minimum-days setting under `performance-review.general` and post it in the internal chat [06:32–08:39].
- [ ] Rocks team: implement the setting on the Rocks side as well [04:36–04:41].
- [ ] Sir Carmencito: an admin page that exposes the settings groups (pending DevOps task) [03:39–04:09, 06:46–06:56].
- [ ] Create a ticket for the review edit endpoint (limited to the overall rating; undocumented) [14:48–16:14].
- [ ] Anjelo: trigger today's Rocks deployment, so others learn the process [16:28–17:43].

**Blockers / risks**
- No per-client value or internal-vs-client split was discussed; it sounds like one global setting. Ms. Marisa's 10-19 requirement was 2 weeks for client work and 3 weeks to 1 month for internal, per client.
- Whether the rule should apply to internal projects only is still a management decision [07:42–08:04].

**Open questions**
- The final setting name: options floated included minimum client assignment days, and threshold vs days [05:31–06:31].
- Timeline: as soon as possible but not urgent; the next review cycle is around December [02:38–02:53].
- Gemini transcript: names and numbers are approximate (e.g. "RNeal/Neil", "RACS" = Rocks, "Kai Charm"). Verify before quoting.

## Transcript

[00:00] un-charm. So ang performance review is safe man sa database no, before going that ba, ako sa in-ang RNeal, Neil kana. [00:10] [00:11] i-paliog ko set up meeting maybe later this afternoon with Christine [00:17] para na gyud tay know how, unsa gyud ilang overall na process. Otherwise, hindi nato ma set up this afternoon, morning lang. [00:26] Para maingon nako si Matt na nagamit na gyud ta. [00:30] Okay. Thank you, Neil. [00:32] Sige. So ang kanang request sa growth charm [00:38] ang mahitabo karon. [00:39] 7 days, hardcoded, something. O, configuration? [00:44] O, we don't have configuration, that was verbally communicated man sa Rocks. [00:49] Um, pero yeah, that should be the proper way to handle it ana. [00:54] Kanang when can we consider an an a [00:58] candidate, a a talent or employee, ma na-assigned for a few days? [01:04] Kung when siya i-consider as assigned ana client, no? [01:07] Na may instance right now, nga one week lang, [01:10] I think na-ano, one week lang na-assigned siya sa client, then mura siya og proxy, no? [01:14] Tama ba? [01:16] Ah, one week no, siguro. Na'y chance. Pero [01:20] 1 month I think is mostly maoy may. [01:23] for billing. [01:24] Um, pero I've known someone, nga nag proxy lang for a few days. Pero unsa giunsa man na karon sa [01:31] admin pag-handle ang performance review niya? [01:33] Example, na-assign siya for 3 weeks. O, kuwan na siya. 2 weeks na ang supposed to be charm. [01:37] Minimum karon. Ang condition, no, minimum, para maka-perform ka og performance reviews. [01:42] Unsa man niya ang request? Ah, but the 7 is hardcoded. Our plan is to store the threshold [01:49] when Rocks create blah blah blah, do not check anything. [01:54] So unsa ni niya ang request? Morag kadtong hard kadtong lang 7 days miss nga dapat naa sa Rocks nga setting. [02:02] O, para ang So ang goal nato is to have the same logic [02:06] kung unsay naa sa Rocks og sa og sa growth. The same lang siya og basehan sa number of weeks kung dapat ba mag-do og performance review ang manager. [02:18] So ang mahog ana, charm, with either mag-add tag [02:24] column, or another table? Field settings lang, miss, akoang advice, oo. [02:27] Oo. Paliog ko advice. [02:30] Naa ta. [02:32] Unsa ni sila, need nila. [02:35] Naka-idea. Ay, kamo na gyud ang gahinapon nila. [02:38] Unsa ni deadline nila? [02:40] Um, kuwan. [02:42] As soon as possible, pero dili siya ingon nga inana ka-urgent, kay ang performance review [02:47] would happen kuwan pa man next quarter, o December. Hapit na, one month. [02:53] So ang wala ko basa, ang question sa ubos, pero ako lang gi-summarized na nan nga morag related siya configurable all in all. Ang 7 days [03:02] nga [03:03] right now, which is also hardcoded pud sa back-end, nga at least 7 days, [03:07] assigned ang employee para ma-consider siya active, no? [03:11] Um, hm. [03:12] Sige, sige. So, unsa man na, charm? Ako giingnan sila, "Puwede kamo lang sa'y focus ana." Mao na ang statement nila, kay para [03:20] kay ang Rocks ba, daghan gyud kaayo og buhatonon. So, if in case, na mo'y murag, ang database, ang database access lang ani, charm, so [03:28] ah. [03:29] Pwede na gi-prep sa kuwan. We can add [03:33] directly sa settings, mas ginana mas kis sa prod lang pud dayon. [03:39] We'll use kaning kuwan, miss, kay there should be a centralized settings man gyud sa Rocks nga [03:45] this is my pending dev ops task pud nga [03:49] dapat tanang settings details diri are exposed sa admin page. [03:54] That was the plan, supposedly, para we'll [03:57] make kuwan ba, kanang, clean look ang, ma-open man gani, clean look ang kato atoang site, [04:03] settings. [04:04] So, supposedly, the same UI ni siya as WordPress, kung mo-open man gani na ko ang na-unsana ni? [04:09] Naunsa na ni man ni, ay? [04:13] Ah, dira. [04:14] We can add [04:15] uh, we can add that as kuwan under performance. [04:20] Hopefully, they understand our kuwan, configuration, [04:23] diri. Naa man siguro na'y performance nga group. [04:28] Under performance lang [04:30] for their [04:32] kuwan, problem. I-add na lang nato daan diri [04:36] ang configurable, pero need pa nato sa atong end, pud, i-implement na. [04:41] Performance review, no? [04:43] O, dira, we have performance review under performance rev, [04:47] review.general settings. [04:48] Naa pa man guro na diri uban? [04:50] Wait lang ha. [04:51] So, ang mahitabo ani, charm, they don't [04:53] need to, unsa ba, API atong [04:57] kuwan, i-query nila. They have direct access man. [05:00] Ah, okay. Mm-hm, read only. [05:02] So, they can just query lang our [05:06] settings, [05:07] kay we don't want them to use API, kay mas hinay biya ana, [05:11] diba? Mas struggle na. So, mag-add lang ko diri og [05:16] another field, sige. [05:17] Oo. Mura siya'g under performance [05:21] that [05:22] [05:23] add ani, ay? [05:24] Mo-ka-ba mo-add, mo-add sa akong guwi. Naa ko'y may gamit ani, ka-I, naga-add gyud. [05:30] Ah, [05:31] ang name ana, will be, kuwan na lang, no? Unsay tawag ana? [05:37] Unsay i-name nato ani? [05:40] Sa client history man gyud ni siya. O, ah, unsa na? [05:43] Kuwan na siya more on the perf minimum [05:47] or active performance review. [05:51] [05:52] Mean [05:54] Kuwan siya, consider siya as kuwan man gyud, kanang, [05:57] active sa client. Mao man ni ang policy. [05:59] Mao man ni ang original. At least naka-7 days lang siya, consider siya as assigned siya sa client. [06:05] Kung less than, dili siya considered. Dili siya ma-part sa client history, [06:09] sa [06:10] employee, nga na-assign siya ana client. Minimum, um, [06:15] client [06:17] assignment, pwede? [06:18] Threshold? Threshold bitaw na wa. [06:20] Dili man na threshold, no? [06:22] Days? [06:23] Uh, [06:23] o, pwede threshold. [06:25] Days? [06:26] Uh, days na lang, minimum. [06:28] Days lang in last part. [06:31] 7. [06:32] Ako na lang i-add [06:34] kani kani siya [06:35] daan didto sa tanan natong [06:38] database para dili kan-directly query lang ani atong settings table, [06:42] under group nga performance-review nga general. [06:46] Kay, I'll be planning to dynamically generate a page nga [06:51] mu-group aning settings nato ma-expose sa UI, [06:54] nga this will be the name and value. [06:56] So, 7 days mean client. [06:59] Ah, tagaye na ko og kuwan inyong suggestion if ever, but 'di siya. Pero [07:02] 2 weeks ang kuwan, charm. [07:04] Ang gibutang karon. O, gipa-2 weeks nila. [07:06] [07:07] O, sige, good. [07:07] Last, gipa-taas nila. [07:10] So, atong 2 weeks is, kuwan, kanang 14. [07:13] Pero ang, ang question, ang kuwan lang sad ana, [07:16] kanang that we need to consider, kay [07:18] ang nahog man gyud na-trigger ni siya tungod sa kadaghan bitaw og bench. So, ang bench man gud, daghan kay og performance review. [07:26] Nya [07:27] [07:28] So, mao to murag gipatas-an, either even gani 3 weeks, there was a conversation about that. So, mao to niingon ko nga, "Sige, let's just make it configurable," para if in case, ma-change [07:38] ang discussion, nga 3 weeks ba, 2 weeks. [07:42] Pero mahog siya og [07:44] um, kani sad nga question, "Should we be a, it should be applicable to internal projects or internal clients only?" [07:52] Mao na akoang question sad kay [07:56] unsa man siya, approve na na sa admin? [07:59] Kay, naa ra ba'y time [08:01] Ah, more on the management pa na siya nga discussion. [08:04] Pero ako lang lang i-add daan kay anyway, we can just remove this if if ever 'di siya valid. [08:09] Oo. [08:10] Para lang maka-start sa ilahang end ba. Kay they don't have to [08:14] kanang ask us nga mag-implement didto. [08:17] Pwede ra man ta mag-add directly kay [08:19] we'll use that settings lang, ah? [08:22] Mm-hm. Sige, go ahead. Thank you, charm. [08:25] I-synchronize ko ni sa tanang [08:28] sa ni? Server sa Rocks. [08:31] Ato lang, miss. Ako nang, [08:33] asa na ko i-share? [08:35] Ako na lang i-butang diri sa atong kuwan, internal. [08:39] Mmm, done? [08:41] Um, another thing pud, kanang si Sir Clint kay nag-ask siya if [08:47] sa kadtong performance review bitaw kay [08:51] kanang if naa bay /edit nga endpoint [08:56] kay para mao lang daw iyahang i-reuse. [09:00] Existing endpoint. [09:02] I think [09:04] kuwan siya, much better na-handle before sa developer sa Growth Portal ang pag-modify sa, wala diytoy i-modify performance review originally. [09:15] Ah, based sa amoa ang [09:17] na-investigate sa Rocks kay [09:20] once maka-review na ang manager, kay dili na ma-edit pud. So, nag-assume mi ana nga wala na'y edit. [09:27] Wala'y edit endpoint also. [09:30] Um, [09:31] wait lang, ha. Naa ba'y edit? [09:33] Dili ko, nakalimot man kuwan na gyud [09:36] sa [09:37] ah, ako i-check [09:39] sa Guwi sa Rocks if we provided [09:43] Asan to ang, tan-awon ko na ah. [09:44] [09:46] employees performance review. [09:49] Check nako, ha. Kay we can share your [09:52] we can share our API endpoint if ever na. [09:56] Naa ba? [09:57] Ako i-check ha. [09:58] Last quarter, ay, wa man.
[10:00] Naning edit diri oh. Naa sa pre-prod.
[10:05] Hmm.
[10:08] Di ba boy na'y mag-query sa amoang performance review na database?
[10:14] Aysa mag-edit man sad diay mo?
[10:16] Oo, mag-edit sila, Charm.
[10:18] Oo mag-edit... m- moa amoang i-implement sad isa sa mga...
[10:22] ...action items sa amo sa growth portal.
[10:24] Pero read only ra man sad ayy, nakalimot man ko. Uy, wala man diay edit diri.
[10:29] Wala xya. Kasa...
[10:32] Pila na?
[10:33] Nangita ta'g naay na-complete somewhere third... first quarter.
[10:36] Kung naa ba gani de- data diri.
[10:40] Wala man ay.
[10:41] I think wala may edit.
[10:43] Well, check lang.
[10:45] Mm-hmm.
[10:46] Pero,
[10:48] with scenario or sa workflow na we need to provide
[10:52] edit miss
[10:53] like nasayop ang client?
[10:55] So, kani xya,
[10:57] kani ang nahitabo Charm, during the performance review labi na sa kadaghan siguro depende sa manager ba, depend...
[11:05] naay mga managers nga daghan pud sila'g
[11:08] kanang
[11:09] team under them,
[11:11] during the one-on-one, naa'y mga agreements and disagreements
[11:15] between the members.
[11:18] So, my example kanang,
[11:20] kanang, "Sir, dili man ko ingon ana," "kanang, 'nagkugi man ko," ana ana.
[11:25] And then,
[11:26] siguro magkita sa manager bitaw, no? Kani, ana.
[11:29] So,
[11:30] naa'y ang una namong discussion was about notes na dapat mag-add lang ta'g one-on-one notes to document, to record what has been agreed
[11:39] among the manager and between the manager and the member.
[11:44] So, ang
[11:46] kana xya, now,
[11:47] ang question ana, "Should we add a note or can we just edit
[11:51] the performance review?"
[11:53] Mm, so murag i-question lang ang result sa evaluation. Okay.
[11:59] Yeah, somehow. Then add lang siguro, so naa man ta'y comment field no, pero
[12:04] So, naa xya. Sige, pwede ra dira butangan sa comment field na, "Mao ni ang na-agree
[12:10] sa manager og sa sa kuan member." Kay dako baya na xya nga factor,
[12:15] di ba, inyo performance review.
[12:17] Mm. Um,
[12:19] huwat ha, kay dili ko sure kung giunsa ni sa original developer.
[12:24] Ang original developer ani kaila nimo.
[12:27] Si Terrence.
[12:30] Okay.
[12:34] Um,
[12:35] giunsa ni? Wala ko pa man gi-trigger giunsa ni niya pag-design.
[12:39] Kadhan ba'g endpoint ani.
[12:41] Nakasubay ka ani, Bay Arnel?
[12:45] Naa ba ni edit? Kay wala man to na-include sa specs.
[12:49] Kay once gi-submit na, dili na pwede mabawi, i-delete na lang xya.
[12:54] Mao to last ako na-remember.
[12:56] That's what other managers are doing, pero
[12:59] murag dili sad xya ma-- I mean, di ba, mawala sad to.
[13:03] Mawala.
[13:04] Ang ilaha lang jud is murag to add more context or to add more...
[13:09] Aha. Sige.
[13:10] Ah, ang ilaha kay mag-- ah, ani na lang.
[13:15] Pero unsa man xya, were were going to allow managers or any clients to update, like for example, ang rating na naa didto is sa 1 to 3 lang, nabutang is 2,
[13:25] gihangyo nila i-3, ana? Ihangyo nato sila?
[13:29] Uy, i-allow jud xya. Or pwede xya ma-higher or pwede gani ma-lower kay in case nga murag dili man jud xya maminaw, ah, ato rang i-...
[13:40] I mean, for me ha, as much as I can, di jud ko ganahan mo-edit, no? Kanang...
[13:45] I... because of the... oh...
[13:48] kuan gani, kanang murag credibility-wise ba.
[13:52] You can add more comments siguro, pero
[13:54] not sure with other managers if they are going to change the rating itself, ha.
[14:00] Ah, naa xya edit Miss, pero wala lang xya na-document.
[14:05] Naa xya edit,
[14:07] pero wala lang gi-document.
[14:09] Akoa ni i-check, ha?
[14:12] Aha. Naa xya sa
[14:15] kanang implementation sa back end.
[14:18] Pero I think limited lang ni xya for
[14:21] rating overall?
[14:25] Base sa base sa kanang code, ha.
[14:29] Kay nakaglobalize man jud ni ang set up sa RACS.
[14:32] So if this is inherited, so naa ni xya by default edit.
[14:36] Pero as far as the code is concerned, ang ma-edit ani is kuan lang, overall rating sa manager clients, dili ang katong content nga
[14:45] um unsay gi-butang nga comments. But,
[14:48] Ato na lang create-an og ticket na lang. So subject, unsa na? Quarterly man gihapon no?
[14:54] Ato na lang create-an og ticket.
[14:56] So base sa code, naa xya pero limited lang ang edit. Wala lang nato gi-expose lang kay
[15:01] I-flag lang xya nga ticket, kinsay mag-ihog.
[15:04] unselective lang xya.
[15:06] Ako lang, kay I think ako ang naka-subay ani, ug do na-confuse pod ko unsa pag-implement, pero anyway,
[15:13] we have EI to review man.
[15:16] Mmm. Daghan man jud ni xya kuan... daghan kay we have two versions of of evaluation man jud sa RACS, if you can observe, Bay Ethan.
[15:25] We have peer evaluation before nga that was cut off
[15:29] kay supposedly ana ang implementation is
[15:32] your fellow developers can evaluate other developers ba, other than the managers.
[15:38] Mao toy purpose. Pero gitanggal man na, mao nang ma-confuse mo nga naa tay laing tables didto nga performance, something...
[15:45] Nalimot ko.
[15:47] Mm. Nakamatay man pod ko ana, Miss, no?
[15:50] Katong time pod nga evaluation.
[15:52] Sige.
[15:53] Kato ra xya, Miss. Naa pa man akoang matabang? Create ta'g ticket lang para dili kalimtan.
[15:58] Palihog ko.
[16:00] Thank you, Kai Charm.
[16:02] Sige, sige. Ako i-add ha? Katong sa- unsa to?
[16:06] Pana ako gi-chat diri.
[16:08] Para wa- wa ta'y huna-hunaon, later na lang implementation.
[16:14] Okay, na-add na.
[16:18] Sige, apel sa production.
[16:21] Sige, okay.
[16:22] Yeah.
[16:23] Dali ra pod tani kay dili man ni xya critical nga update.
[16:28] So, we'll schedule deployment karon. Kinsa'y gihangyo ninyo, Anjelo?
[16:35] Arnel? Arnel?
[16:38] Padagan.
[16:41] Ikaw?
[16:42] Anjelo lang sad xya.
[16:44] Si Anjelo lang sad hapon.
[16:46] Cge, cge. Busy man pod ko.
[16:49] Oo, kay para maka-leave pud either nato.
[16:51] I-call ninyo sad...
[16:53] Oo. Anjelo lang sa una ron. Sige.
[16:55] Oo. Siguro need need pod ninyo makabalik niining atong uban, si Edwell para in case sila na lang...
[17:01] unsa'y mahitabo, dapat naa'y senior. Pero in emergency situation,
[17:06] so aware sila asa or maka-instruct sila from someone nga who has access sa atong Jenkins ba.
[17:12] They can just kuan lang, kanang
[17:15] run the automation.
[17:17] Mmm.
[17:18] I-say, naa pa kay i-discuss, Miss, para kuan na lang nato ipa-trigger para at least kay
[17:21] Ah, goods na ko.
[17:22] maka-leave na...
[17:23] I'm good.
[17:24] Sige. Si Anjelo atong patrigger-on para
[17:26] Mmm.
[17:27] at least kung mag-leave, kabalo na mo asa i-click.
[17:30] Aysa, Anjelo man to last time?
[17:33] Kinsa gani to Anjelo, nalimot ko? Si Anjelo man to.
[17:36] Si Anjelo man to, uy. Dili, uy. Si Anjelo to.
[17:41] Mmm.
[17:42] Ikaw na sad.
[17:43] Ah, sige.
[17:45] O pareho tanan busy karon, nagdaghan sad akoa diri. Pero I have choice.
[17:50] Medyo mag-deploy man ta.
[17:51] Ah, by the way,
[17:53] kanang if ang inyong ticket ba, kay automation na man ta ron no? Nya wala ko nag-restrict bitaw nga dapat i-
[17:59] read-only na ako. The moment nga padulong na ta 4:00 PM, as much as we can,
[18:05] kindly restrict lang moving tickets nga
[18:10] merging for production emergency,
[18:13] kuan, after
[18:16] 2:00 PM ba dapat, sa imong tan-aw, Miss?
[18:19] Kay koyawan ko anang late kay ta mag-merge, nya
[18:23] nag-automate man jud ta, mabiyaan xya.
[18:25] Yeah, really.
[18:28] Oo, mag- mag- although wala na nako gi-butangan og restriction, ha, kay there are scenarios man jud nga need pod nato ipatapos, especially ang ticket nga typo lang, which is kaya ra na i-
[18:37] kuan sa EI testing under if you kuan lang minutes.
[18:41] Pero kanang dagko nga ticket ba, ah kung dagko xya, siguro i-hold lang siguro, i-tan-aw ninyo dili kaabot sa 4:00 PM
[18:49] nga deployment,
[18:50] para dili xya dili mabiyaan ang ticket ba, kay included na man jud sa automation right now is
[18:56] tanan from
[18:57] from start to finish, meaning
[19:00] mag-back
[19:01] mag-create sa PR, mag- after ana, mag-move sa ticket. Nya ang inyong ticket kung naa pa sa testing on staging, mabiyaan man tu xya.
[19:10] Although na-include na jud ang inyong source code,
[19:13] pero wala xya nabutang sa release candidate-- ah release notes.
[19:18] Ha?
[19:18] Yeah.
[19:19] Yes, sir.
[19:20] Free 3:00 PM.
