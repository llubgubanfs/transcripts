---
title: "Feature alignment (11 AM)"
date: 2026-10-19
type: meeting
tags: [meeting, growth-portal, performance-review, badges, career-objectives, action-plan]
participants: [harvie, ethan, luis, joshua, victor, lorenzo]
source: "~/Videos/dsm/[11 am feature alignment (partly garbled and low internet)]2026-10-19 11-04-20.mp4"
transcriber: gemini
saved: 2026-10-19T12:46:53
---

# Feature alignment (11 AM)

## Executive summary

**Source note:** Gemini transcript of a Google Meet recording (54:11). The recording was partly garbled (low internet). Nothing was captured for ~06:36–07:49 and ~11:07–12:22, and timestamps are compressed and unreliable in ~24:00–30:00 and ~47:44–52:56. Names (Kyle, Ethan, Louis, Lloyd, Marisa) are as Gemini heard them. Marisa and Lloyd were discussed but not on the call.

**TL;DR**
- Went through Marisa's performance review proposals. The lead (Harvie, presenting) wants "why not just use Save and Exit?" answered before anyone builds an edit-after-submit button [02:17–09:25].
- The lead's position on eligibility is to merge client-assigned and internal-project rules into a single "at least 2 weeks" rule. Marisa's "3 weeks to 1 month" for internal projects would defeat the purpose of the 2-week action plan [16:58–22:30].
- Ethan asked for a go signal on the Recognition Badge Management UI. The lead said he'd propose it to the engineering managers, with a PRD ready [23:45–34:02].
- Career-objectives interviews (Louis) show the page is optional in practice, and client-assigned people have little time. The lead has not decided how it relates to the action plan [34:34–43:42].

**Decisions / positions**
- Performance review eligibility: the lead's position is to consolidate items 1 and 2 into one rule, at least 2 weeks of assignment, for client-assigned, internal-project and bench-assigned employees alike [12:49, 22:30]. He said he'd accept 3 weeks to 1 month only if Marisa explains why [23:30].
- Item 3 (who conducts the review): the lead considers it clear already (CSM or EM) and not worth over-engineering. Revisit only if there's a double-review concern [22:00–22:30, 23:30].
- The eligibility fix probably belongs in the Rocks data (who is under whom per quarter), not Growth Portal. Check the Growth Portal source for its own query [19:10–20:15].
- Item 2 (edit submitted review): no go/no-go yet. First answer why Save and Exit isn't enough [04:41, 09:25].
- Recognition Badge Management UI: the lead will propose it to the engineering managers. Ethan is to have the PRD or equivalent ready [33:25–34:02].
- Level 4 training (advanced orchestration, a "1-man IT department") is already drafted [32:50]. Nothing exists beyond Level 4 yet [32:27].
- Growth framework 3.0: structure is OK, activities are being polished, and it moves to a rules engine fed from the Excel sheet. The lead will show it this week [44:22–46:10].

**Action items**
- [ ] team: Add to the review proposal "Why not use Save and Exit?" and confirm the original reason for submit-is-final (Kyle may know) [05:28, 06:21]
- [ ] team: Check the Growth Portal source for its own eligibility query (vs. the Rocks window view) [20:00]
- [ ] Ethan/lead: Follow-up with Marisa today on items 1–3, around 1:30–2:00 PM; proceed without her if she can't join [23:00–23:30]
- [ ] lead: Propose the Recognition Badge Management UI to the engineering managers [33:38]
- [ ] Ethan: Have the PRD or equivalent ready for the badge UI [34:02]
- [ ] Joshua: Deploy the onboarding badge (on staging). For the AI-labeling badge, wait for Sir Michael's icon approval. Give the client options plus a recommendation, don't hand over a single choice [24:00–31:00]
- [ ] Louis: Continue the action plan and career-objectives work. The lead will decide how it relates to career objectives [43:22–43:42]
- [ ] everyone: Update your action plans in Zoho WorkDrive. Only about 20% have updated them [47:44]
- [ ] lead: Show growth framework 3.0 this week [45:25]

**Blockers / risks**
- Client-assigned developers (100% allocation) barely engage with career objectives, action plans, talk sessions or AI mentoring. The page being optional means it is ignored [34:55–39:44].
- Action plan verification: files live in Zoho WorkDrive and the tally is manual. A cloud issue last month blocked pulling files. There is no real way to confirm that tasks such as environment cleanup were done [48:40–49:14].
- AI assessment may under-rate people whose clients forbid AI tools (placed at Level 1 or 2 despite knowing how) [39:47–40:15].
- Auto-save was raised as a fix for losing drafts but called expensive in API calls (the review is only done quarterly) [08:30–09:12].
- Marisa's items competed: client-assigned 2 weeks vs internal project 3 weeks to 1 month [22:30].

**Open questions**
- Why does Growth Portal make submitted reviews final, and what happens to an unsaved draft if the tab closes (auto-save)? [04:06, 08:04]
- Does the unwritten rule "under 2 weeks means 'no basis for review' and 'meets requirements'" need to be formalized? [14:08]
- How should the action plan relate to career objectives (quarterly vs years)? [43:22]
- Should career objectives and the action plan be enforced for client-assigned employees, and if so how? [35:54–37:55]
- How should the AI assessment treat people whose clients ban AI tools? [39:47]

## Transcript

[00:00] Speaker 1: ...first item, which he posted in the click chat, and then I believe it's also as an item to propose as well.
Speaker 2: Mm-hmm.
[00:08] Speaker 2: Yeah. Can we have kuan lang... Who will share? Ako ba or...?
Speaker 1: Ah, wait lang. I-present nako, sir.
Speaker 2: Okay.
[01:00] Speaker 1: Oh, I think mao na ni siya.
[01:14] Speaker 2: Ah okay, so just taking note of this proposal. One, row one, so "Improve Performance Review Eligibility Logic."
[01:28] Speaker 2: "Highlighting employee history." Ah okay, "then internal projects, more than three weeks to one month of assignment, clarify who will conduct performance review of this employee assignment."
[01:43] Speaker 2: Huh? Clarify? Or we will... Ah sige, pwede ra... I think we could suggest... for that clarification. And then the next one is "Allow managers to edit submitted..." Ah okay, this one is like straightforward. All right.
[01:54] Speaker 2: Sige. So unsa... which one will go first? The easiest or 1 or 2? 1 na lang?
[02:17] Speaker 2: Yeah, actually for number two is the easiest, no. Basically, the problem with kuan, no, with the current performance review, once we submitted it, like the submit na, not the save and exit...
[02:30] Speaker 2: ...we cannot edit it prior to the 1-on-1. So whatever there's some additional info or additional items that we would want to add, we cannot submit it. I mean, we cannot edit. What we are going to do is...
[02:44] Speaker 2: ...we will create another performance review. Like, going from square one. And then add our kuan, no, kato the the new info.
[02:59] Speaker 2: So, for number two, yeah, given the... I mean, giving the capability to allow edit, to edit the performance review, that will make it a bit kuan na lang, no. Much easier to...
[03:13] Speaker 2: ...and create performance review. So, basically, yeah, just add a edit button for this one.
[03:26] Speaker 2: But, I'm not sure if, I mean, with the current logic in kuan, in Growth Portal if there's also like a reasoning why they didn't allow the edit after we save... I mean, after we submit the performance review.
[03:39] Speaker 2: I know for the save and exit... it's more of a kuan lang, like, yeah, there's a capability to edit.
[03:51] Speaker 2: So, maybe the the question here will be, why not use save and exit? Right? So, maybe we have to understand...
[04:06] Speaker 2: ...unsa ba 'yung kuan, save and exit? Like, that Is that the intention to do the edit... on performance review?
[04:21] Speaker 2: And then, the other one, which is the submit button, which is to finalize na. So, kumbaga, you could argue that, yeah, why why submit it...
[04:33] Speaker 2: ...kuan right away when you can have it save and exit, 'di ba? So, here's a kuan naman, question.
[04:41] Speaker 2: Should we proceed on this one or not? What will happen if we cannot do it... we will not do it, 'di ba? Why not use save and exit?
[04:54] Speaker 2: Unsa... unsa inyong kuan dira... thoughts ani? I mean, number two, mao man 'yung easiest. Should we go or no go?
[05:20] Speaker 1: Tong gipost pud ni Ms. Marisa, anang once also kanang separate jud na... kuan na meeting.
[05:28] Speaker 2: Sige. Siguro, yeah, i-add lang na siya nga question, no. Why not use save and exit? I mean, the intention is that if you want to... if you're not yet clear with your performance review, I mean, whatever you're going to submit...
[05:36] Speaker 2: ...why submit it, like, finalizing it, 'di ba?
Speaker 3: Makes sense.
Speaker 2: 'Di ba?
Speaker 3: Oo. Okay, example ah... because, for example, ah...
[05:51] Speaker 3: ...the manager ah nag-try ug... like at the end of the day, and then, "Ah, okay. Wag muna na nako bataron. Ah, I'll just leave it there." Pero na-close ang kuan... session. So, it's either...
[06:06] Speaker 3: ...save as draft or save as submit. Ah, submit automatic, so dual purpose siya kay... ah, it can be just like they wanted to... Emergency. Like, "Oh, kuan, lakaw dayon." Yeah, they forgot to save it. Or submit na lang dretso or...
[06:21] Speaker 2: Submit na lang dretso. And then, later on, they found out naay additional info.
Speaker 3: Oo, kana. Oo.
Speaker 2: So, dapat save and exit. So, I'm not sure what was the kuan pud, no, intention before. Hopefully, naay... naa pa to si Kyle? Kay naa man jud siya'y mga explanation why why there was a save and exit, kuan, no.
[06:36] Speaker 2: But, so, what I can say is kuan jud siya, ana...
[07:49] Speaker 2: ...a question before we go that, no. Now, let's-- let's take for example, I have already created like my draft, but I didn't press the button like...
[08:04] Speaker 2: ...sa save and exit in the kuan, katong submit. What would happen if I just simply close it?
Speaker 1: Ah, let's try auto-save, sir. Just like writing an email, 'di ba, sir? So, you're writing an email and then you close it directly, sir. Automatically it it saves in your draft. Yes, sir.
[08:18] Speaker 2: Ah, okay. So, I guess the question now, why we need that is kuan lang...
[08:30] Speaker 3: And then, I think it's expensive, sir, kay you keep on calling ah API. But'ang 'to ah nagbutang ka ug, let's say, 15 seconds after inactivity or 10 seconds and then triggers auto-save. For example, I drafted like um...
[08:43] Speaker 3: ...5 minutes and then I stopped because I took a coffee. And then, auto-save triggers and then what if I come back again, I stop because I was just texting someone and then auto-save, like it's pretty expensive, for me, at that point. For ah because...
[08:58] Speaker 3: ...I don't know. Um... it's it's expensive to call API time and time... But it's a good thing, but I'm not sure if we ah have the luxury to have that expensive calls. Even though it's-- that idea is good.
[09:12] Speaker 2: Mm-hmm. Um, you could also argue that this is being done lang like... quarterly. It's not like every day.
Speaker 1: Yeah.
[09:25] Speaker 2: Um... Yeah, I I think that's the question for, I mean, for number two before we proceed on that edit submitted performance review. What's our advantage, ana. Like, why not use save and exit? 'Yun lang.
[09:41] Speaker 2: Next, number one. Okay, so "Improve performance review eligibility..." So, actually, this one is like...
[10:00] Uh, like a long, I mean, an old problem. We're trying to figure out. Because currently, no? Um, I mean, the way they I mean, the way that Growth Portal uh manages, uh not really like manages, like identify who are the members,

[10:22] kumbaga, like that will be eligible for performance review is, they don't have those kind of mechanism. As long as if that member is assigned to that project, like for example in the case of FS Learning, like myself,

[10:38] then automatically I will be do- I will be doing

[10:43] the performance review that in that batch, but in actual,

[10:54] realistics, well that's, um, actually that's not fine, no? I think the highest that I got is like 75% in actual.

[11:07] Um, but yeah, as I mentioned, itong 74 in my case is sample...

[12:22] ... kuan lang is that yeah, we need to fix this number, mga numbers dira. And at the same time, we need to

[12:32] at least kuan lang, like fix when a manager... I mean, like what's the trigger for a manager to give a performance review. So, initially ito 'yong mga kuan, oh. So, for client-assigned,

[12:49] if it's more than 2 weeks of assignment, then eligible. Yeah. All right, so more than 2 weeks.

[12:59] So, I think...

[13:00] Ah, wait. Ah, interested. Wala diay to katong rule na 7 days?

[13:04] Wala. No. No, there's not no such no such rule. So, actually if you have

[13:12] Yeah, if you if you are checking the kuan of team FS Learning, I I I did mention that even on the first day,

[13:20] even though you are only like 1 day in FS Learning, you should have the performance review. But actually, um the reason for that one is just to kuan lang muna, like

[13:29] Yeah, just give kuan lang while we're trying to kuan, um

[13:34] trying to solidify this na um...

[13:39] na, what I... Yeah, solidify this kuan, kanang... ruling.

[13:45] But um, there was like kuan lang, parang unwritten rules lang na as long as like

[13:53] less than 2 weeks, I mean, before ha, if you're less than 2 weeks in a project, okay, um, the CSM or EMs

[14:02] will simply like did kuan lang, like no basis of review,

[14:08] and then uh, "meets requirement" 'yong sa 10 na mga items doon na required. So, they will just put "no basis for review" and then "meets requirement".

[14:22] Kasi, ha...

[14:24] 'Yung ang mahirap po ma-godd kay kuan sila per... gukdon ni sa HR pod. Kay mō man ilang number pod daw ron.

[14:33] So, we will tend to, yeah, put "no basis for review" and then "meets requirement". Yeah.

[14:41] But, uh, yeah. Um, again, ang question na pod ana is that, um, how I mean how they are doing the kuan, the the the scoring. But that's another topic na pod.

[14:52] But for now, it kani pa, kani pa atong i-kuan, i-figure out. So,

[14:59] uh, kani siyang client-assigned employees or actually even bench pod, bench-assigned employees, no, as long as, uh, if they are more than 2 weeks,

[15:10] then, yeah, we will give, we can give na performance review.

[15:16] Naa pod'y usa pod nga kuan pod point of view.

[15:24] If naa siya sa bench, like once they are get assigned sa FS Learning, especially for those kuan gani kana naay, I mean, na na, unsa'y tawag ana? Ana na-dropped from the project, unsa'y term ana diri sa Fullscale? Kana na

[15:40] Na-dropped from the project.

[15:41] Na-dropped from the project. Regardless kung unsa ang situation, whether performance or kuan, project completion, or anything,

[15:50] that at least 1 week, naa naa'y performance review. Kay ang reason ana is that, kung dili siya, in 2 weeks pa nato,

[16:01] walay kwenta ang action plan. 'Di ba, ang sa action plan nato, I know all of you naa man mo'y mga action plan, 'di ba?

[16:08] Ang first week is like, yeah, you have to update your profile, do environment cleanup. Hopefully, you have done your environment cleanup, especially for Victor.

[16:21] And then, um, yeah, you have to update your profile and then complete 'yung mga AI courses, especially 'yung 'yung mga AI courses from the first quarter of this year.

[16:33] So, 'yun.

[16:36] So, that already cons- uh, constitute your kuan na, like your activity for the first week, 'di ba?

[16:44] But yeah, um, it looks like we will have... Yeah, we're having a consensus na na at least 2 weeks, okay, regardless if it's a client-assigned or naa sa bench, okay?

[16:58] Uh, yeah. Internal projects, yeah, this one is another kuan, oh. I mentioned 1 week, no? Ang ilaha pod diri is that more than 3 weeks or to 1 month of assignment. So, mao ni among kuan pod contention pod kay

[17:16] mura'g ang kani ma-god niya second nga item, 'di ba? Like, internal project, m- dapad like more than 1 week to 1 month of assignment before we will give kuan, kanang

[17:28] performance review. Mura'g mawa ang kuan ani, katong

[17:34] essence sa kuan, action plan. Kay pwedeman moingon nga, "Ah, dili pa to ku- kuan hinoon, mag-hope and pray lang ko nga ma-assign ko after 3 weeks. 'Di na ko ni buhaton ang kuan, ang environment cleanup, 'di ko mag-update sa akong kuan.

[17:51] Anyway, 'di pa 'to ko gradu-on." 'Di ba?

[17:56] I mean...

[17:57] Ah, makes sense.

[17:59] I mean, yeah, you could say na kuan, "Sir, 'di pud siguro oy." No, um, you do not kuan, you do not under- underestimate ang stupidity or kuan sa tawo. Okay?

[18:14] Bisan pa'g moingon ka na, "Yeah, buhaton na," dili na niya buhaton. You could not say.

[18:19] Naa man pud instance na, katō akoa, example, um pag-sulod nako 1 week, boutan ta o kana imong gi-point, Harvey, ah nasulod ko dayon sa client, kay katō wala pa man to'y kuan, wala pa man ning Fullscale learning stuff at that time. So, katō karon, example, naay bag-ong employee, for example, nga sulod na siya,

[18:44] diha, at the week dayon, like maybe Thursday or unsa ba na, ma-kuan na siya, ma-deploy na. So, mao na, mao usab pud na sa atong i-kuan, kay possibility pud kay na nga diretso siya usugod.

[18:58] Oo. Um, ang kana sad nga cases, no, kay naa man gud, actually, naa'y tima-ilhan jud sa kuan, sa RUX man jud ni siyang basis. Ah, actually, ang pag-fix ani is dili sa kuan, sa akong nakita, dili ni siya sa Growth Portal basihan. Adto ni ang fix ani sa RUX, actually.

[19:10] So, maybe mao na nga kuan, parehas ang kuan ani, no. But, akong nahibaw-an ani, ang ako sad gi-assume, dapat sa RUX ni siya nga fix. Kay ang pagkuha man gud kana ditong kinsa ang mga members na under nato, na-co or under sa mga CSM for that quarter, is that is given by kuan man gud, by RUX.

[19:25] So, I would assume na naa na'y kuan dito daan, like query or probably, um, unsa'y tawag ana nga query? Kanang window view, window view sa kuan dito sa RUX. Mura'g naa na'y ipas-
[20:00] ... out. And then basahon na lang diri ni ni kuan ni Growth Portal. Pero yeah, try to check na lang pud sa source code diri sa kuan sa Growth Portal. If naa ba jud silay ilaha jud nga query ani?

[20:15] nga basihan. Pero ang kuan lang jud ani no, kay mura ba'g wala pa hi- I will not I mean sa akong end ha, I will not agree kanang item number 2.

[20:30] nga kuan. Unsa gani? Uh for review in misplaced logic, works in progress, um yeah. Again, i-check lang jud ninyo. Like how how Growth Portal arrived ani nga total number of employees.

[20:45] Oo. Kay ang kani bitaw'ng item number 3, um actually dili na man jud ni siya i- like i-clarify or or anything para sa akong point of view no. As long as ang number ma-assign jud I mean, let's say for example, karon ha, October, ma-assign siya sa Growth Tra- I mean sa FS Learning na na-board- na-onboard siya.

[21:00] And then abot siya ug, let's say, a month, mm. So, bali eligible na siya. So, naa pod iyang tendency pod niya, let's say on probably mid-November ma-assign siya sa project. Okay?

[21:15] Although I'm not sure if naay kuan diri'y mga project nga 1 month ra or 2 weeks ra. And then, naa pod gihapong possibility nga kuan sad, let's say mid-November siya na-assign pod sa project and then na-offboard na sad siya by December kuan mid-December. So, mahulog siya'g like 1 month ra nga engagement and then that means offboard na pud siya, balik na pud siya sa FS Learning by December like 3rd week.

[21:30] So, mura ba'g mao na iyang i- ang kuan ang item number 2, oh I mean item number 3, kinsa ang mu-conduct sa performance review. So, ang kuan lang, ang question is naa ba'y ingon ana nga wherein like 1 week ra nga engagement, like actual client, although

[21:45] naa koy na kuan pod mura'g wala man sad to nadayon pod, like kato bitaw'ng kang kuan gani kang Loyd nga naa pod nay i- I mean naa'y project from a from a client, 'di ba nangita man to siya'g mga kuan like kinsa man to'ng mi- kuan sila Ethan ba to or si M? So, but I'm not sure if nadayon ba to or or what. But I don't think nadayon to. So, um

[22:00] So kana, uh mao na siya ang i- kuan ang item number 3, to clarify lang pud kinsa ang mu- kuan. But sa ako, klaro na man sad siguro na siya. Like, as long as you are within that logic nga eligible for kuan, kanang uh per performance review, then yeah, PM or no, not PM, CSM or an EM is pwede mu-hatag ana. So, mao na siya ang akong kuan ani.

[22:15] I think ang point 3 kay dili ra jud needed. Kay naa na man jud sa, naa na man jud sa logic Miss. Oo. Uh let's not overengineer lang siguro regarding ana nga logic kay maguba na nuon sa amo-

[22:30] Lagi. Mura'g ang ato, mm yeah yeah. I I would agree. Um Mura'g ang ato na lang gi-i-fix ani is kuan lang jud kanang ang ang in out lang jud siguro sa mga members within the projects. Ang i- ang i-klaro jud ani, kay karon ho, naa'y competing man jud ang kanang item 1 ug kanang item 2. So, client side, 2 weeks, pero diri sa internal project, it's more than 3 2 months. So, I would say, sa akong end, is dapat pareha na sila, 2 weeks. At least 2 weeks. Kay ang kanang action plan ninyo, ang first 2 weeks, mao jud na ang pinaka-importante. Ang kanang week 3 and beyond, is kuan na na, mao na na siya ang mga trainings na, kay upskilling. Basically, or kuan, um remapping or I mean i-kuan ninyo iyang mga skill gaps. So, kanang 2 and 3, I mean 1 and 2, that's that should be 2 weeks log. Okay?

[22:45] Now, ang So, hopefully naa na mo'y kuan, context ani no, nga kaning duha ka items ni Marisa. So, ang next nga question ani is, naa ba'y gi-set si Marisa nga kanga sa atong kuan ani? Istorya?

[23:00] Ah Ethan?
Wala pa, sir. But mu-set man mi ug meeting later on this day after ani nga meeting.
Ah okay. Yeah, need ko or kamo na? Okay na mo atong, basta mao to akong kuan ha, point of view.
Mm-hmm. Ah I think it would be better, sir, if naa pud ka.

[23:15] Ah, wala man ako'y problem kay yeah wala koy bakante ron. Uh hapon?
Yes, sir.
Wala. Mm. Maybe, wait lang ha. Mura'g ang pinaka-kuan lang diri is like, ah 1:30 to 2:00. 1:30 to 2:00 ra akong vacant. Ang next is 5:00 PM na. So,

[23:30] Ah, sir, ah Pagsato, makahimo ta'g ana?
I think uh if pwede ra if available si Miss Marisa pod ana nga time.
Yeah, I think I'll just uh inform her lang also if uh she can uh join that time.
Mm-hmm.
But if if dili jud, then I think uh mu-proceed lang siguro mi, sir, nga wala ka.
Ah, i-proceed lang. Oo. Basta kato ra akong kuan no, ang number 1 is um from the FS Learning nga point of view, ay i-kuan na lang ni i-consolidate na lang ni ang items 1 and 2. Dapat 2 weeks lang. As long as 2 weeks, go na ta ana. Pero kung naa'y kuan si Marisa ngano'g 3 weeks to 1 month, ah let me know lang kung unsa man gani. Para akong suggestion is kuan na lang na siya 1 I mean 2 weeks. Number 3, mu-align ra na siya kung kinsa ang mu-conduct sa performance review. Dili ra kaayo problem ana. Unless naa'y laing concern ani nga like duha ka performance review from CSM and EM siguro, mao'y ilang gitan-aw. Pero uh yeah, not sure about that. Pero kaning lang kuan. Ang number 2, kato akong gi-ingon, why not use one exit button. Oo. Kana.

[23:45] All right. Please take note na lang ana. Anything else?
Kuan pod, sir, uh 'di ba Ethan, naa kay i-propose na kuan? Kaning sa atong
Ah ah yes. Yes, ah I I had a feature proposed, the Recognition Badge Management UI. The purpose was to allow admins create, edit, remove badges in the Growth Portal without needing to like access the server-side codes. So yeah, ah I noticed that there's been a lot of um requests to add new badges. So, ah this feature was actually on hold because we was or we weren't able to like find out if this is actually uh being used and ah very ah in need for the managers. But uh since we now have a proof, ah is it okay, sir, or ah can I have a go signal from you ah to ah actually implement this ah feature?

[24:00] All right. Before that, um kamusta sa ako ni Joshua kato akong gipabuhat nga kuan? Okay na to? Onboarding badge?
Kuan, sir. Um naa pa siya sa staging, sir. I-deploy na ba dayon, sir? Or
Yeah. Yes.
Sige, sir.
Ang uh 'di ba naa pa'y another badge nga request? Or same ra?
Yes, sir. Kanang sa AI labeling, sir, uh nag-wait pa ko sa approval ni Sir Michael sa icon, sir.
Ah, so okay na ang text? Ang icon na lang?
Ah, yes, sir. Then, ako lang i-deploy as soon as possible, sir.
Ah, ultimatoma ha. Ultimatong kang kuan, Michael. Um, if okay ra siya ani nga mga design, hatagi na lang siya'g option, ah dili kanang usara ka buok pod.
Ah, yes, sir.
[30:00] Speaker 1: Sir, na- naka- Naka-hatag na ba ganina si Hordan?
[30:02] Speaker 2: Oo. Unsa unsa Oo. Ani ani siya, Josh kuan oh, try to give him an option then then unsa imong recommendation. Ana gani?
[30:13] Speaker 1: Sige, sir.
[30:14] Speaker 2: Kay para dali ang kuan nato ba.
[30:17] Speaker 2: Kay kung igo ra ka mohatag og bisan usa ka buok, oo unsa ba diha, kay ako as a client, ganina ra imong mahatag sa ako, wala kay lain option para nako. Oh, i- you have to give kuan gyud, options, and then unsa imong recommendations pud.
[30:36] Speaker 2: Oh, and ayaw lang pa- ah then do- kumbaga ayaw lang pagmao-od kung dili i-ko- kuhaon imong recommendations ha. At least you have given, 'no?
[30:46] Speaker 1: Ah, yes, sir.
[30:48] Speaker 2: Oo. 'Ta pa-ana jud na, mga ingon ana. Ana jud.
[30:53] Speaker 3: Butangay na lang "client is always right", 'no?
[30:56] Speaker 2: Oh, yeah. Actually, yeah, yeah, yeah. Ana jud na.
[30:59] Speaker 3: Oo.
[31:00] Speaker 2: Client is always right, so you can give a recommendations and options, okay? But ultimately the the client will choose for himself, 'di ba? So, ana lang.
[31:12] Speaker 2: Okay. Anyway, dili dili trivia ra man sad ni, nga kuan, dili man ni siya kanang architectural pud nga kuan, wherein you could kuan pud, push back.
[31:20] Speaker 3: Kana kanang ma-argued jud ba, kay kana kay kuan man na ilang preference lang.
[31:24] Speaker 2: Oo, preference lang.
[31:25] Speaker 3: You can make sound judgment if kana architecture side na, pwede jud ka, tahi ana, tahi ana kay naay pros and cons, so.
[31:32] Speaker 2: Oo.
[31:33] Speaker 3: Kana pwede, dili ra man ni kuan.
[31:34] Speaker 2: Oo, trivia ra man gyud siya. So dapat mag-anad mo ana guys, ha? Labina kani mga kuan, kani mga fast tracker, inana inana jud ang pag-deal sa client, okay?
[31:47] Speaker 2: All right. Yeah, I guess ang kuan na lang siguro ninyo is pag-identify when it is a trivia and when it is architectural decision. Okay, sige. So yeah, going back sa question ni kinsa gani? Kang Ethan or kang Edward? Sorry.
[32:03] Speaker 3: Ah, Ethan, Ethan.
[32:04] Speaker 2: Pareha man gud mog pangalan. Ah, Ethan. Okay. Okay, Ethan. Ah, whether we will pursue this or not. Okay. Ah, daghan pa man kaayong instances. Now wait, naa pa ba tay so- naa tay gi-expect pud. Okay, human na ang leadership, naa naay Level 3 and then naa pa pud padulong nga Level 4 and...
[32:27] Speaker 2: Actually, after sa Level 4, wala na koy hinumduman nga kuan, like wala pa'y ah wala nakuha anay pud nga another training pud. Unsa gani gihapon ni?
[32:38] Speaker 2: Sige. Um, however, by next year, murag bomba na sad ni og mga kuan nga training, so daghan og decouplings sad.
[32:50] Speaker 3: I think naka-draft pud me, ah last time, naka-draft pud me dha sa L4 with Joshua Paldo.
[32:56] Speaker 2: Ah.
[32:57] Speaker 3: Naa na, ka ba- na-kuan na, na-propose na nako, um, which is nindot, kanang more on advance orchestration, no? Bitaw, kanang morag 1-man IT department, so. I think kana man siguro suited for Level 4, kay if Level 5, I think, ah super advance na na, pero kanang Level 4, it's already advance, pero, ah I think worth it na, sa mga labi na sa mga naas training diri.
[33:25] Speaker 2: Oo. All right. Sige lang. Go, ah... Ang imoha gi- mangayo no, og signal no, Ethan?
[33:36] Speaker 4: Mm, yes, sir.
[33:38] Speaker 2: Ba- kuan sa ako ha, I- I'll ako sa siya i-propose sa mga EM pud.
[33:45] Speaker 2: Mm. Okay, mao ni ang problem karon. Anyway, ah I know naa, naa kay naka- handam diha, igo na lang na i-execute. So, ako sa i-propose sa kuan EM, and then sa kuan amoa pud. Ah, kay wala pa nimong badge, so.
[34:00] Speaker 4: Mm-mm, noted, sir.
[34:02] Speaker 2: Oo, so i-andam lang na diha. Ready lang ang mga PRD or unsa man na. Ingon sila dili na kuno uso ang PRD. Anyway.
[34:16] Speaker 2: Sige, um, anything else? Balikan nato ka, Ethan, anaa ha?
[34:22] Speaker 4: Mm, yes, sir. Yes, sir.
[34:24] Speaker 2: Sa badge, kay okay. Um, naa pa'y kuan, um, RV?
[34:29] Speaker 5: Ah, yeah, kang Luis, yeah.
[34:31] Speaker 2: Ah, Luis, sige.
[34:34] Speaker 6: Ah, yes, sir. Katong ilang akoa, sir, ang about tong implementing the action plan sa career objectives.
[34:42] Speaker 2: Okay.
[34:43] Speaker 6: Then, you asked me to kanang ah interview a couple employees. So, ah I managed to interview uh a couple.
[34:54] Speaker 2: Mm.
[34:55] Speaker 6: And then, ang ah ang from what I can gather, the ang ilang onboarding is mag- diff- ah magdepende ra jud siya sa client. So, others receive um checklist, documentation, or kanang may ah i-walkthrough gyud sila. Others had to like figure things out by themselves or pud just by communicating with the client.
[35:18] Speaker 6: And then, ang career objectives na page, gipabuhat sila like before, like ah this one person, he said like last time he visited the page was like last year or 2 years ago ba to. Um, basically, gipabuhat sila pero optional ra siya, so wala kayo gihapon nag-use, wala siya gi- enforce.
[35:40] Speaker 6: So, but wait, if I ask them if like if i- if, ana sila nga if i-enforce gyud, gamiton gyud daw nila. If kanang i-push gyud ba by management. So, mao ra to siya.
[35:54] Speaker 2: Ang kanang, sorry ha, ang kanang gi- i-enforce, unsa sana siya nga type? Ganina, sorry.
[36:01] Speaker 6: Ah, katong naay kuan, sir, kanang mu- mu-go through sa career objectives gani, like ilang i- i-accomplish tong mga nakabutang sa growth portal. But since, na-assign sila'g client, murag optional ra sa ila gani, like it's low prior lang. So, mao na ok ra siya.
[36:17] Speaker 2: Okay, when you say optional, kanang verbal lang na? Giingon silang optional?
[36:21] Speaker 6: Oo, yeah.
[36:23] Speaker 2: Okay, naa tay ambiguity. Okay. Na-suspect.
[36:31] Speaker 3: Ma-matawag bitaw syag optional, kay kato sa akoa nga end, um, si ah Mark, usahay kay, oo. Ingana man pod nga kuan, um, og naa moy time, buhata lang, pero it doesn't mean na necessary, kay mu- kami kay mu-object pud me sa amoa lang end. Mu-object me, kay tungod ka-busy sa amo, wala mi oras ani, 'di mi ka-, bisag even though gamay ra na, pero maglisod me og butang og oras. Kay kanang full 100% allocation kay ang client grabe maka-exp-. Maybe depende sa client. Akoa medyo kuan na jud tu, murag 100% around the clock. So, mao na, oo, mao na dili jud me ka-ic.
[37:18] Speaker 2: Around the clock.
[37:18] Speaker 3: Case to case, case to case basis ni siya. Pero naa may uban makabuhat gud pud. Like the other developers makabuhat man. Sa amoa 'di jud. Bisag bisag pag-attend og kanang mga kuan, unsa'y tawag ana, kanang mga talk session, dili pod ko motunga. Ang uban dili sa amoa dili motunga. Ako kay i-leave na lang nako diha, maminaw while ga-solve og mga problema. So, ing-ana ang kuan na namo. Pero ang uban 'di jud motunga. So, kana sa sa amoang point of view na. Sa amoang case.
[37:55] Speaker 2: Aha. Alright. So, mahulog nga kuan no, once you are in a client, no, maglisod jud mo og kuan kanang, like pasaka og level kay, like focus man mo diha, 'di ba?
[38:10] Speaker 3: Mao sad na ako na-experience sa mga under nako during AI mentoring, nga 'di halos mang-reply kay busy jud sila sa ilang client. Nya I asked one of them, ah nakalimot ko'g kinsa ing-ana to, AI rust daw, is pirte jud daw kuno bisya sa client deployment, all on those stuff. So, that's why kuan, so murag understandable ra jud kay kaseba'y ko kung how ah kanang...
[38:31] Speaker 2: Busy pod, oo.
[38:32] Speaker 3: Oo, busy. Nindot ang imong focus sa ilang client kay I mean client first man gud ba.
[38:39] Speaker 3: Okay, they expected 8 hours pud jud nga naa'y full activity, even though wala'y kanang screen recording or unsa pa na, but ah they expect it to resolve nya daghan jud og, dako jud og expectation unless okana nga client kay laid back ra pud kaayo.
[38:55] Speaker 2: Mm. So, siguro kung I mean, mu-side bit lang ta, with regards sa mga training, kung I mean kung demanding jud ang work, dapat dili na lang sila jud mu-proceed. Kay ang akoang kuan sad ana ba kay ang part pod sa mentor. Nga dili man pod kay ka-commit, so ngano padayon pa man ka?
[39:21] Speaker 3: Mao bitaw, kuan, na-disappoint gani ko kay akoang mga team kay sa naay mga client, nya kanang 'di mang-reply bisag kanang acknowledge lang. Tan-aw ko pwede ra man ta dili mu-commit. Ambot og unsa inyong agreement at first kay wala man ko sa week 1. So, I don't know unsa inyong agreement ngano gi-paapil mo'g ing-ani.
[39:40] Speaker 2: Mm. Dapat dili na lang sila ipa-apil, oy.
[39:43] Speaker 3: Bitaw, ing-ana.
[39:44] Speaker 2: Kung non-busy sila ana nga client, then yeah.
[39:47] Speaker 3: Tungod pod siguro sa AI assessment. Kay ibutang nato Okay. Ako, among client dili musugot og mugamit og AI. Ah ing-ana lang. Nya 'di ko kagamit og AI, nya for code lang, code lang. Nya mao tu nga na-
[40:00] ntagug na sila sa level 1 even though they know how to use it, or level 2. They don't know kuan, hatagan gani silag chance. So maybe kuwang atong pag-gauge anang nga part, anang assessment. Kana siguro.
[40:15] Kana pud, oo. Sila... Hmm. Alright, so going back atong kang Louis, so busy pud ang ilahang career. Kay ang... unsa ba gani ang point anang career? Usually ang career dili ra na sya ma-span for 1 year.
[40:35] Okay? Dili na sya ma-span for a quarter, or even 2 quarters, dili na sya 1 year. Usually kuan gani na sya like years. Okay? Dih...
[40:48] I don't think naay ma-himo dha nga job grade 3 later on, like from job grade 2 to 3 like next month or next year, wa lay ingon anaa. I mean, unless if you are very, very, very exceptional. Like ikaw gyud'y mohatag ug kuan kanang like 10 or 20% nga kuan kanang...
[41:03] revenue sa full scale. Kana, exceptional gyud na. Then yeah, you can be a job grade 3. Pero kung ang work ninyo is just kuan, like typical lang, what is expected gyud as a job grade 2, or 3, or 4, or 5...
[41:17] then, yeah. Mao man gud usahay gud ang notion ron, is that yeah, nag-gitagaan ra ka ug kuan, like dha sa imohang career objective, murag mag, ug gitagaan lang ka'g like 1 or 2 nga mga... track, or siguro like kuan kanang sa plural, plural site, then mag-expect na ka nga "Ui, ma-senior na ko".
[41:35] Ika-kanang kuan ang train. Okay, so dili sya ingon anaa, like... dili sya ingon anaa.
[41:57] Must have years of experience.
[41:59] Yeah, yeah, yeah. You need to have a must years, yeah.
[42:02] And also deals lots of BS every time.
[42:05] Oo, wala pa mo na- I mean, I don't know sa case pud ni Victor, no? Um, if nakasugat na ba syag client nga kuan gyud, kanang mga explicit ba nga mga kuan, mga istorya.
[42:18] Ah, oo! Last time, kanang client naku which is ni-argue jud ko nga, kana bitaw'ng point nga akong giingnan sya nga "Ah, sige'g panghilabot dha sa release, mao na'ng mga guba tanan." Nga develop- manager jud to sya. Ako jud syang gipanghan kay it's getting out of hand nga maka-cause ug like 50 bugs during release, and it's improper. That I had to speak out kay ako'y tig-fix sa mga issue. Mao to. Nga to nga point, oo. Naa, kay kusog man gud sya mo-mali kas. Like di man sya US, ah I think boss taga-Boston sya. Kusog, hilig kay sila og mga ing-ana nga mga explicit words.
[42:55] Kana mga kuan na, mga yeah European nakasugat pud ko ana. Kato gani makuha ka'g Indian.
[43:01] Ah, utro pud na sila.
[43:05] So, ang kuan lang is that kana... Sige, so... Anyway, sorry na-sidetrack ta didto, no? But... atong kang Louis. Iyon. Dapat siguro naa sya'y in-charge, so...
[43:22] Ang akong kuan usab, let's say for example, no? Kana'y kurso na gyud ni Louis, ba, kay... mura sya'g ma-cover in a way ni Leo. Pero not really the entirety, kay as I mentioned ang career, that's years. Ang kang Leo is more on ang iyang scope man gud is based sa kuan ra, kanang, probably like quarterly...
[43:42] or within the year. So, kana, tingnan naton na sya i- i-deep kuan pud, who and we will have our own career objective ug katong naa na'y action plan. i-butang sya sa action plan or career objective. Oo. Sorry, di- di pa ko ka-decide ron, Louis. Oo.
[44:18] Sige, sir.
[44:19] Oo.
[44:20] Ah, para naku ta discuss pud.
[44:22] Kagikan hapon, oo. Need pa ba'g kuan ba, I mean, additional discussion ana, okay? Very short. Siguro ganahan sad ko makakita pud sa kang Leo. Um, wala, um, mag-kuan pa kami ni Lloyd ani. I think na-okay na ang ski- I mean, katong growth framework. I mean, structural-wise, okay na sya.
[44:52] Um, nag-polish pa mi sa kuan, kanang mga activities around it. So, mao man na'y giingon nila. And, um, by the way, nag-meet na ba mo ni Lloyd or wala pa? Or when ba mo usually mag-meet ni Lloyd, ba?
[45:11] Ah, wala pa, sir.
[45:13] Ah, wala pa. Okay. Wala may set nga schedule, no?
[45:17] Wala pa, sir, kay this past kuan kay wala sya'y apil-apil sa among kuan kay mi- kanang meetings kay kuan daw, busy.
[45:25] Oo, yeah, yeah, yeah. I-clear pa, kuan mi ana, na collaborate pa mi ana with regards sa kuan na sya sa growth framework. So, siguro within this week, we I could pre- kuan, ipakita naku sa inyo, like kay mo'y una nga makakita, if ever,
[45:45] sa growth framework na 3.0, para naay idea. So, ang akong kuan na lang ani is kuan, ang implementation kay mahug na man gud sya nga kuan na, rules engine na. So, kato gina'g excel sheet, i-feed lang. Kuan na lang i-need i-kuan buhaton ang... Siguro ang... I don't know unsa'y mga kuan dha ipangbuhat, probably action plan, maybe.
[46:10] Part atong objective settings, na. So, o kanang mga badges, nya relate ma-relate na na sya, mga badges and then trainings. Mura'g ang ending ninyo, no, mura'g kuan, kanang, unsa ang mga topic, na, like unsa ang i-assess, how we will assess, unsa ang mga training or courses. Siguro dha na ninyo buhaton usab na sya.
[46:39] Course work. Yes, kinsa to'ng nag-kuan ni... Ah, wala man.
[46:43] Ah, ako, sir.
[46:44] Mm?
[46:45] Ah, I just have ah thoughts lang sa feature gani ni Louis, sir, sa katong action plan. Mm-hmm. Sa client-assigned employees kay, di ba, wala kaayo sila'y time doing the ah action plan. And for bench, sir, kay ah syempre kay bench, ah so, dako kay'g free time pirme. So, we can do it, sir, nga sa bench kay required jud kay sya sa action plan, sir, nga need jud na nimo amand or buhaton. But also to client-assigned, sir, required sya, but we can adjust kuan, sir, sa time nga given para mahuman na nila nga action plan. Like, kana lang, sir.
[47:27] Oo, you could I agree pud nga, yeah, katong gita murag optional sya. Kay ang gi-expect pud ni client pud, okay, nagbayad ko'g $10,000, assuming lang ha, $10,000, that's half a million na na sya per month.
[47:44] So, I would expect nga kaning guy is, mo- hatag na og result dayon. Wala na'y mga kimi-kimi kanang mga kuan, no. So, yeah. Um, sa fast learners, yeah, required gyud sya. Ang, actually, akong problem man gud sa action plan, no, kay maglisod ko'g monitor gyud ana kay ang kuan ana naa man gud sya sa Zoho. Naa sya sa Zoho WorkDrive. I-pull out pa nako na nga mga files. And then, i-tally pa sad nako ang mga files if na- naay lihok ba or wala. By the way, guys, i-update inyong mga action plan. Mura'g gamay ra ni-update, kay si... kinsa gani to, oy? Oo, mura'g naa ra sya sa 20%, but most of you, wala jud nag-update-update sa inyong action plan. Palihug ug update, at least especially katong sa training plan ninyo, na-huma naman mo ato. So, palihug ko'g update.
[48:40] Okay. So, ang kuan lang nato is ang pag-tally na. And then, ining tally nako, oo, dako kay'g files ninyo, like everything nga dili ma-pull. And then, it so happened like last month, nagka-issue ang cloud. Dili sya mo-pull og mga data or mga files gikan sa Zoho. Naay issue sya. Mao jud na-ahi akong mga kuan na, mga updates. But, nonetheless, ang kuan lang jud sa action plan, no, kay ang kana bitaw'ng pag-verify if nabuhat na ba na sya or wala.
[49:14] Mao jud akong kuan jud na kinahanglan ma-implement dha. Ang paglista, walay problema. Ang pag-kuan, like for example, kana bitaw'ng mag-environment cleanup, unsaon nako pagkahibalo nga na- tuman ba jud na sya? Kay currently, more on kuan ra man gud sya, kanang gi-checklist lang, and then, gi-unsay lang nga nahuman ba jud or dili. Ayna. Like, for example, katong sa kuan, kanang pag-update sa profile. So, currently, ang ginabuhat ana kay kuan ra, kanang naay monitoring si kuan, si Kier. So, giinglan nako "Oy, nahuman na ba sya sa profile niya ug video profile?" Naa na sya'y monitoring, so tan-awon pa pod nako ang file...
pod ninyo i-kuan, kana mo mag-kuan, mag-discuss sa mga logic pod. So, I will focus na lang sa kani kuan ron ni Miss Marisa. Oo, i-follow up lang kuan na, and then try to check lang pod ni Lloyd, pero I hope na okay ra ang muhatag pod ron si Lloyd para na-kuan. Sige.

[52:56] T-A, yeah, wala na'y dali-on pod ni, kay November na, unsa naman ron, 19? Grabe. 19.

[53:10] Mada- Mada-ong man og delayed, oy. Na- dapat naa na gyud karong nga week. Naa'y something na. Kay delayed na kaayo, moabot pa'g next week. Yeah. Sige.

[53:25] Mao na among kuan ron, kanang i-propose pod. Sige, guys. So, yeah. Alright.

[53:48] So, mao ra.
Thank you, Sir.
Thank you, Sir.
Thank you, Sir.
Thank you. Thank you. Ingat, team.
Ingat, team.
