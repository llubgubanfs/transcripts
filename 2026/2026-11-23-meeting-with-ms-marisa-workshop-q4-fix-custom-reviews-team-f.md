---
title: "Meeting with Ms. Marisa - Workshop Q4 fix, Custom reviews, team feedback"
date: 2026-11-23
type: meeting
tags: [meeting, growth-portal, custom-ranges, workshop, probationary, hackathon]
participants: [Marisa, Lorenz, Victor]
source: "~/Videos/dsm/[3pm call with miss marisa] screenrecording-2026-11-23_15-36-16.mp4"
transcriber: gemini
saved: 2026-11-23T16:04:24
---

# Meeting with Ms. Marisa - Workshop Q4 fix, Custom reviews, team feedback

## Executive summary

**TL;DR**
- Workshop is missing from Annalou's and Mark's Q4 Project step because the form still resolves projects by calendar quarter, not the Q4 custom range (Sep 7 – Nov 15); Annalou's assignment under Mark was Sep 7–21 (14 days). Fix is ready (Bernard) and deploys today. [01:08]–[03:27]
- Custom reviews: Marisa will not restrict Custom to probationary employees, and will not add a "3rd or 5th review" step. [06:37]–[08:25]
- Moving forward, a Custom review is not tied to a specific quarter; current behaviour stays through Q4 and the rule applies from the next quarter. The ticket stays open and the decision comes after Q4. [09:22]–[10:20]
- Marisa suggested splitting the team into sub-groups (hackathon vs Growth Portal) with someone delegated to oversee. [11:45]–[13:49]

**Decisions**
- No probationary-only condition on Custom for managers or employees; the UI stays the same. [06:59]
- No extra step asking whether a Custom review is the 3rd or 5th performance review; Rocks has no field for it either. [07:39]–[08:11]
- Custom reviews will no longer belong to a quarter, from the next quarter. Do not enforce it now, to avoid disrupting existing reviews. [09:22]–[09:52]
- For a review that is really Q4, managers should use the quarter, not Custom. [05:40]

**Action items**
- [ ] Lorenz/Victor: deploy the Workshop Q4 fix today, then tell Marisa so she can inform Sir Mark. [03:24], [11:15]
- [ ] Lorenz: keep the Custom-not-tied-to-quarter ticket open for after Q4. [10:20]
- [ ] Lorenz/Victor: ship the days-assigned display in Performance Analytics, tomorrow or Wednesday. [10:56]
- [ ] Lorenz: take the sub-group and delegation suggestion to the next hackathon planning. [12:51]

**Blockers / risks**
- The Custom workaround can make a review count in Q3 because Q3 overlaps; avoid it until the fix ships. [02:35]–[02:59]
- Marisa wants to see that not everyone is excelling and does not want lack of opportunity to be the reason. [13:33]–[13:49]

**Open questions**
- Sir Ed's comment on the video: he is waiting to relay it to the team. [11:38]
- At [10:46] Gemini garbled "March"; probably "the hotfixes for Q4". Unclear.

## Transcript

[00:00] Victor: Miss?

[00:02] Marisa: Wala man... Wala man sad diri, Miss.

[00:08] Victor: Ikaw una, Lorenz, oh.

[00:10] Lorenz: Oo, pwede ra ako. Ako sa mag-defend sa atoa.

[00:23] Lorenz: Naa na, Miss.

[00:28] Lorenz: Ako na-admit, Miss.

[00:40] Victor: Good afternoon, Miss.

[00:43] Lorenz: Good afternoon, Miss.

[00:46] Marisa: Good afternoon.

[00:49] Victor: So yeah, I think naa pa'y

[00:52] Victor: concern si Lorenz regarding atong kuan.

[00:56] Lorenz: Ah yeah, katong matter ni Annalou og Mark, Miss. Let me share my screen.

[01:08] Lorenz: Yeah, so we've already filed a ticket for it, Miss. We'll...

[01:13] Lorenz: We'll go over lang sa cause and then ang amoang solution ato.

[01:18] Lorenz: So, on staging, we're signed in as Mark.

[01:22] Lorenz: The reason ngano'ng wala si... wala ang workshop nga project

[01:29] Lorenz: ni ni Annalou og ni Mark kay

[01:34] Lorenz: na-under si Annalou for September 7

[01:39] Lorenz: until September 21,

[01:42] Lorenz: but um, supposedly on the custom range kay kanang 14 days jud siya.

[01:49] Lorenz: But right now ang sa form man gud diri nga end sa Growth

[01:54] Lorenz: kay iyang gi-resolve using calendar quarters pa.

[01:59] Lorenz: Bale pag, inig mag-switch og quarter kay i-look up man niya ang unsa nga projects based on that range.

[02:06] Lorenz: And then on Quarter 4, diri kay under the hood, ang iyang gigamit pa kay calendar quarter.

[02:13] Lorenz: So maong wala nigawas si... si Workshop.

[02:18] Lorenz: So, a fix is on the way na ana, Miss. We're... kanang we're looking into kanang i-change na jud to

[02:24] Lorenz: the quarter na jud para ma-offer's i-workshop.

[02:27] Lorenz: So, it would be... it is expected na gawas na si...

[02:31] Lorenz: si Workshop for Mark and Annalou.

[02:35] Lorenz: And then, yeah, I'd like to kuan lang sad katong workaround sa custom

[02:40] Lorenz: i-avoid lang sa nato karon, Miss, kay there's a risk pala ato

[02:45] Lorenz: if we go through the custom workaround, naay chance nga

[02:49] Lorenz: ang review nga iyang ma-submit kay ma... ma-count siya sa Q3.

[02:54] Lorenz: Kay there's an overlap man gud right now sa Q3.

[02:59] Lorenz: So, yeah, um ma-kuan na nato siya, Miss, ma-fix na nato siya right away. Naa na si Bernard ato.

[03:07] Lorenz: And yeah, I think we can move on sa 330 katong probationary harps.

[03:18] Marisa: So, when's the deployment? Would be today or tomorrow?

[03:24] Lorenz: Ah we... Can we do today, Victor?

[03:26] Victor: Today, Miss.

[03:27] Marisa: Today, okay.

[03:31] Victor: So yeah, regarding sad aning 330, Miss, so naa na pod mi... na-file na ticket ani, and then up for open items pa siya.

[03:40] Victor: So yeah, ang permeyro na open item kay like sa custom, currently kay ang diba ang custom review is

[03:50] Victor: if mag-file og custom review kay ma-belong man jud siya sa specific na quarter,

[03:55] Marisa: Mm-hmm.

[03:55] Victor: current na quarter. So yeah, sa bag-o na request is ang kinsa'y makapili sa custom is like ang kuan ra ba, like ang mga employee ra ba na naa'y status na probationary

[04:08] Victor: or ang kuan na jud?

[04:10] Marisa: Ah okay. Kuan sa side sa manager, ang manager makaset man sila float.

[04:17] Marisa: Employee, yeah, for probationary na siya nga... nga iyahang... naay iyang target for the custom, so the employee when they do self performance review

[04:33] Marisa: and select custom, the same sila og UI sa manager, right?

[04:40] Victor: Mm-hmm.

[04:44] Marisa: So, 3rd and 5th per- performance, that is specific for probationary. Kay what happens daw karon is

[04:52] Marisa: um, so nagbutang sila'g custom, but not intended really for performance reviews sa 3rd and 5th. Murag siya'g

[05:02] Marisa: kuan... it's for any purpose. Like, pwede siya nga kaning nga Quarter 4 kay dili siya whole Quarter 4, so they set the custom range.

[05:15] Marisa: Nya, um for the 5th and 3rd performance, kay mao to wala ma'y laing option, custom range.

[05:22] Marisa: And then, what's happening right now, murag na-confuse sila cause

[05:28] Marisa: um we also, kanang, we need to know kung kani siya nga custom, is it for Quarter 4, 3rd performance review, or 5th performance. So,

[05:40] Marisa: what I suggested to the managers is kung Q4, for if for quarter jud na siya, i-quarter na lang jud. Kay anyways,

[05:52] Marisa: um we can set the or we can retrieve from the system man kung pila siya ka days

[05:59] Marisa: nga ni-tenure sa kaning quarter. So, that's why in relation to that in the performance analysis, you'll we need to display

[06:10] Marisa: the number of days nga na-assign siya ana nga client cause para mawala to siya ang idea nga mag-custom sila nya specific for that quarter.

[06:24] Marisa: Ah did I answer your question?

[06:28] Victor: Um Miss, unang ang kaning custom Miss for kuan ra ba jud, for probationary ra ba jud sa bag-o na requirement or?

[06:37] Marisa: Hm, pero I don't want siguro to limit the manager nga kanang or kanang ang options nga halimbawa ang custom mo- mo- unsa ba, mo-true ra na siya or enable if the employee is a probationary.

[06:55] Marisa: Mao na ang question, no?

[06:57] Victor: Mm yes, Miss.

[06:59] Marisa: Ah, for me, dili lang nato siya i-kuan, wala lang'y in-ana nga condition.

[07:05] Victor: Awalang. Okay.

[07:07] Marisa: Although, ang intention jud ana is for probi na siya pero kuan, kanang murag

[07:18] Marisa: ruling na lang siya namo, but we don't have to change the or add that logic.

[07:24] Marisa: Um pero question ani, if they, the manager or the employee selected the custom,

[07:31] Marisa: naa ba'y other step or next step which is to select whether it's a 3rd or 5th performance?

[07:39] Victor: Ah kana Miss kay wala pa na siya na-enforce, so kana usa pod sa open item pod oh.

[07:44] Marisa: Um, I'm thinking ba para kay kung magbutang ta ana kay mahug man gud siya'g mas-stricto ta and

[07:52] Marisa: sometimes ra ba kanang mo-change ang discussions ba around that. Nya I don't want to change the code necessarily to cater unsa'y na-change na decisions.

[08:04] Victor: Yes Miss, ang kuan pod ana sad, upon investigation pod sa Rocks kay wala po'y kuan field ana sa...

[08:11] Marisa: Oo, wala siya, oo. So, yeah moving on, um sige. So,

[08:18] Marisa: ako lang ingnon ang managers na the custom, ang intention jud niya is for the 3rd and 5th performance, but

[08:25] Marisa: uh we will not kuan na lang, kanang we will not have an option kung para ba jud siya sa 3rd and 5th, but the but we will not include the custom self-performance review under to a specific quarter.

[08:40] Marisa: Kay ang kanang specific quarter, kung for Q4 jud siya, dapat i-set siya'g Q4 and anyways we can retrieve the data man the the tenure, the number of days ni kuan na assigned na ang employee. So,

[08:55] Marisa: kana that would be my take for the custom, will not make it very strict, so it can still be used in any means they want,

[09:05] Marisa: but we will not include the custom na lang for a quarter.

[09:11] Victor: So, mawala to ang katong previous na requirement Miss na katong ang custom ma-belong siya sa specific na quarter?

[09:22] Marisa: Moving forward.

[09:24] Victor: Ah, okay.

[09:26] Marisa: Pero karon kay inyo man gi-kuan, diba? Gi-include man ninyo, okay ra man siya. Okay ra na kay ang uban ana ongoing man siya nya

[09:37] Marisa: ang kuan lang, ang for the next na quarter, kana mao na siya ang amoang sundon na rule.

[09:45] Victor: Hm kay ang problema man gud Miss kay i-enforce siya karon kay ah, unsay ta'g... unsa'y mahitabo sa katong existing na kuan...

[09:52] Marisa: Oo, magbalik-balik na pod sila. Ayaw na lang. Sa next na lang na. So, moving forward, ang kanang custom intended
[10:00] Marisa: duration na dili siya specific for a quarter.

[10:07] Lorenz: So, so kaning mga items is for future iteration ba gihapon ni siya, Miss, or dili siya ma-kuan karon?

[10:15] Marisa: Oh, if future na lang siya kay mag-conflict na siya, 'no?

[10:20] Marisa: Ma-i-Q4 ninyo. E-ready lang siya daan ang ticket para dili nato siya makalimtan. Basta inig human sa Q4 nato, mao na na siya ang desisyon.

[10:33] Lorenz: Sige, Miss.

[10:36] Marisa: So, kani nato ang pag-display sa number of days na-assign na siya ang employee, ongoing na siya?

[10:43] Lorenz: Ongoing na siya. Oo.

[10:46] Marisa: Pero dili pa siya ma-deploy as katong sa including the hotfixes, 'no, ang gihimo for March, dili pa. Okay ra.

[10:56] Lorenz: Medyo... maybe ugma siguro, Miss, or Wednesday na gyud siya ma-kuan...

[11:00] Marisa: Oo, yeah, yeah. You can test it lang.

[11:10] Lorenz: Yeah, I think mao ra to, Miss, sa kaning open items sa 3:30.

[11:15] Marisa: Mm. Okay, so let me know lang if na-fix na siya so we can inform Sir Mark.

[11:23] Victor: Okay, okay, Miss.

[11:26] Marisa: Okay. Thank you.

[11:27] Lorenz: Thank you, Miss.

[11:28] Victor: Thank you, Miss.

[11:30] Marisa: Ah, by the way, nakahatag na mo'g video ni Sir Ed?

[11:34] Lorenz: Ah, yes, Miss. Mao na, Miss.

[11:36] Marisa: Ah, unsa iyang comment?

[11:38] Lorenz: Ah, as of now kay magpaabot lang daw, Miss, sa kuan sa atong team kay iyang pa daw i-kuan didto, i-relay.

[11:45] Marisa: Okay. Naa lang koy suggestion ana ba as

[11:49] Marisa: I observe, 'no, daghan man mo, so what if kanang i-group gani ninyo? Like ah no, mana man sad no'on, but if naa'y

[12:00] Marisa: upcoming or naa gani kanang things to work for, ah unsay tawag ani, hackathon ba? Naa lang jud siguro specific

[12:10] Marisa: individuals na to focus on that. Naa sad pang growth portal, so everyone's talent and kanang ilahang initiatives and

[12:20] Marisa: whatever they can give back to the team kay mas ma-kuan jud siya, ma- maka-work on jud gani sila. Kay

[12:30] Marisa: um if kamo tanan man gud kay kamo tanan growth portal, kamo sad tanan hackathon, I don't think effective, 'no, in that sense nga

[12:42] Marisa: daghan ang nag-work ba, ang uban kay murag wala na lang kay wala na man sad silay matabang, ana.

[12:51] Lorenz: Oh yeah, I will take note of that, Miss, sa next.

[12:55] Marisa: Naa ra'y kanang sub-group ba pod nimo, Harz, nga ikaw mo-oversee sa tanan, o si Victor, ana. But naa kay kanang someone who could also act on behalf of you, ba.

[13:09] Marisa: Delegation, that's part of kuan sad, leadership skill.

[13:20] Marisa: Para makita nato ang kamaayo pod sa uban, 'no? Kay I'm I'm doing we will be doing performance review ba, yeah, yeah.

[13:33] Marisa: Um not all of you, I could Well, it's it's different siguro, 'no, kay dili man kamo tanan naa'y chance to really do your best or show your best, but I'm I'm seeing na dili tanan ni-excel.

[13:49] Marisa: Yeah, I don't want nga ang reason kay walay opportunities or daghan ra kaayo mo.

[13:59] Marisa: So, yeah. Anything else?

[14:11] Lorenz: Yeah, I think mao ra to na items, Miss.

[14:16] Marisa: Okay. Hopefully, nalingaw ra mo. Thank you for coming last Friday. And I can see your faces na. I can put a face on your names.

[14:33] Marisa: Sige, bye-bye.

[14:36] Lorenz: Bye, Miss. Thank you, Miss.

[14:38] Victor: Thank you, Miss.

[14:39] Speaker A: Bye, Miss. Thank you, Miss.
