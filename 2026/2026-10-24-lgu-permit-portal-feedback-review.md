---
title: "LGU permit portal feedback review"
date: 2026-10-24
type: meeting
tags: [meeting, lgu-portal, epermits, uploads, roles, validation]
participants: []
source: "https://drive.google.com/file/d/1AnCAnx16p80fp9c3J2B-p_EY3d6Ryv5B/view"
transcriber: gemini
saved: 2026-10-24T20:58:03
---

# LGU permit portal feedback review

## Executive summary

**TL;DR**
- Review call on LGU building-permit portal feedback: field limits, lot-area validation, required-field highlighting, upload limits, role handling. [00:46–40:00]
- Attachment limit is now 500 MB per file (was 100 → 200 MB); PR is on staging. [15:42–16:32]
- LGU wants to go live next month, but the delivered network scanners are not yet configured or tested. [40:45–41:40]

**Decisions**
- Raise email, username, applicant name and representative name limits to 100 characters; the email domain counts toward the limit. [02:25–04:00, 31:20]
- Project lot area defaults to the property lot area and must be ≤ it; auto-correct if the property value is lowered, otherwise error out clearly. [10:00–11:36]
- Leave floor-area computation as is to avoid new complaints. [07:01]
- Add an "Others / supporting documents" slot for the subdivision approved plan / unified application doc and any other attachment. [26:50–27:30]
- Certificate of title goes under proof of ownership. [24:05]
- Handle slow uploads with a "still saving" UI state, not strict size limits (unless Azure blob limits require). [22:00–23:50]

**Action items**
- [ ] dev team: show field-specific validation errors instead of generic "Failed to register". [03:00–04:00]
- [ ] dev team: highlight empty required fields and/or focus the first empty field on Next. [11:40–14:20]
- [ ] dev team: surface attachment-size errors at select time, not only on submit. [18:42–19:08]
- [ ] dev team: allow image/PDF attachments on technical reviewer notes. [27:33–28:30]
- [ ] dev team: fix wrong time in Activity History (multi-hour offset, likely timezone). [30:05–30:36]
- [ ] dev team: admin/sysadmin "change password" action for users. [31:59–33:07]
- [ ] dev team: multi-role users (change-role dropdown or status-based role validation; roles as tick boxes on account creation); lowest-effort option to be decided. [33:15–39:00]
- [ ] LGU/OBO: configure and test network scan-to-computer for the delivered scanners. [41:05–41:40]
- [ ] LGU: shorter OBO link/domain on the purchased `.gov` domain. [40:17–40:40]

**Blockers / risks**
- Scanners delivered but unconfigured; go-live next month depends on testing. [41:05]
- Large scanned floor plans can't be compressed; latency/timeouts on upload. [16:00–16:25]

**Open questions**
- Exact timezone offset in Activity History (transcript heard "12:00 shows as 6:00 AM"; unconfirmed). [30:14]
- Whether Azure blob storage imposes a practical file-size limit. [22:10]
- Speaker labels in 20:00–28:30 may be swapped; ~28:30–30:00 missing from transcript.

## Transcript

[00:00]
[00:25]
Bale ako?
Oo, kwan na lang nimo, unsa gani, ang each item ba?
Ako lang i-share ang screen ha?
Oo, sige, sige.

[00:46]
Email, kani. So, naay na-encounter issue gihapon. Kani, bale sample@acquarter1...

[01:20]
So, kani, yeah.

[01:47]
So, 'pag lapas na, like kung mag-register ba?
Oo, ang kwan, register. Like kanang...
Ay, sa user.
Pero di ba pwedeng sad ta diri katong mag- inig apply kay kung wala pa...
Oo, in behalf sa kwan... sa user, pero like need ka katong kwan... katong admin gani, admin ba 'to?
Adto'g dashboard adto. Diri 'to, kani.
Oo, diha diri.

[02:25]
Kani, um, sa email, naay uban email tag-as.
Mhm.
Pila iyan current naka-set gani ron?
Ang current ani murag pila gani katong characters ba?
I think naa sa kwan...
20 rata, or...
20?
Oo. 20 characters.
Naa gihapon'g taas kaayo ug email?
Mhm.
So, need lang siguro nato na i-stretch out. Probably 100 characters kani nga kani nga field.
Mhm.
Kana siya. Um...

[03:00]
Applicant name, pa-double check lang pod ani nila kung pila iyang limit.
Oo, sige.
I think ang ang siguro ang handling kung kung inig register niya naay prompt barog kung over sa kwan...
Kay ang ang error man gud is kwan kaayo, kanang generic kaayo ba.
Generic, mhm.
Dili mahibaw-an sa gani kwan unless og ang amo gihimo gihapon is nag nag tan-aw mi sa logs, unya ang gi-mention is truncated.
Mhm, oo. Mao na siguro ang kwan, i-truncate.
Oo, so...
mao na siya kwan. Probably in relation sa katong isa ka ka-update ninyo nga i-highlight...
kana guro kung naay error, ma- ma- mapoint asa adapita nga field ang naay issue.
Mhm. Dili, sige, sige.
Or naay naay kuwang.

[03:55]
So, ang kaning uban fields, kaning mga applicant name, representative name, ang preferred na kanang character limit nini is 100 na lang pud?
Oo, 100 lang para kanang dili kaayo limited ba. On-process entries, good. Unless og pwede, mao na, kung other way, para mahibaw ang user nga naa diay iyang limit nga nga entry field, ma- ma- mamention if let's say inig register over diay siya, so mao na, ma-correct niya. Unlike sa karon nga inig error, "Failed to register" unya wala...
DB error.
Oo, walay detail ba nga "Nganong failed ba, nga sakto man akoang entry?"
Iga-ana. So...
Sa email sa email ba na-part, sir, ang apil ba ang it- at- @email.com ana sa 100 kwan characters?
Oo, pwede ra i-apil nimo.
Mhm.
Ang iyahang kwan, ang domain, domain.

[04:51]
Kana. Unya, I think same pud sa... ariya, ako lang i-loss. So, let's say...

[05:28]
Katong lot number... I mean, lot lot size.
Mhm. Mao na siya katong kwan sa item 3.
Aah.
Oo, kani.
Kung inig apply, either simple or any type sa kwan...
category...
Let's say kung mo-mention siya og kwan diri...
Kani, say 500.
Niya katong sa next...

[06:14]
Supposedly floor area kay kwan, pwede ra man siya, depende man nila. Like kung two-story, mas mudako siya sa lot area.
Kani guro, need sad ni i-control, bai. Like kung poy-an...
Check man daw.
Kay ma-total... di dapat dili ni siya musobra... unya moingon siya diri og kwan, "Ngano per floor? Per story man ni. Dili man siya..."
Ah, bale i-compute ang kwan?
Murag ang kwan lang ani, let's say two-story, unya let's say 50 per kwan...
area...
Oo, pwede siya'g pa- unya i-times nimo, mao na siya ang total floor area.
Oo, total floor area.

[07:01]
Pero naa man pod'g uban gud nga walay apil ang...
Like say kanang ang ang front nila, lahi pud og kwan...
Siguro... Aray, i-leave-as-is lang kani lang atong i-focus-an, basin labaw'ng mag-reklamo sila.
Ang kaning lot area?
Oo, ka- supposedly kung let's say ang balay, duha ka 50, so 100 jud na. Pero naay instances...
Hello, hello.
Hello, hello.

[08:07]
Kani mga naay pula, i-
Aah, nawala, nawala ka, sir. Nawala, nawala.
Nawala ko?
Mhm.
Kadyot ra, pako-
Mawala ba 'share'?
Oo, okay na, okay na.

[08:22]
Um, katong part sa high- Kani, unsay mag- gamay kag screen diha?
Mhm.
Oh sige, scroll up and down, asa man ang kuwang?
A- bale ka- balik daw sa kwan, ka-user, sa katong lot area kay mur- pag- dito na pa- dito na part kay nawa man ang koneksyon, gi-redial ko.
Oo. Ang kwan sa kaning number of stories ug floor area, total area, ang akoang idea unta is murag i-compute, pero...
Oo.
basin gani naay other kwan nga ma- mo-more pa ni sa let's say computation, 100, supposedly. Unya basin naa pa nila in computation or mga gi-sokod apil ba. So, as is lang ni. Ang sa lot area lang ang gi-kwan ani.

[09:08]
Kay sa next tab ani, naa may lot area na pod. Unya mao man to ang reklamo gihapon, 'di magkapareha.
Mhm.
Mao ra to, dili lang i-control. Ang next item katong i-mention nimo is kaning highlight...
Ang siguro ang sa kaning lot- sa katong lot area dito na diri na page, Sir, kay kanang as is ra, dili ra siya i-kwan, derive?
Oo, as is lang, kana lot area 100.
Aah.
Inig next nato, naa na pod, naa na pod silag lot area.
Oo, oo, oo. So, dapat kwan-
So, dapat mag-sync up na ang duha.
Mhm.
Mao may problema. Sa pon nag-mention og 100 diri...
Mhm.
pero project possible man pod gud nga ang project scope nimo kwan,
dili nimo lukopon nimo ang tibuok property.
property.
Dili necessary mag-sync up ba. Kwan lang guro, either...
[10:00] equal or below ang kani. Parang i-default nimo sya inig next niya, kung niingon syag 100 dinhi, dapat automatic 100 imomg ibutang.
[10:07] Oo.
[10:08] But, dili sya dapat mo-more than.
[10:10] Ah, dili sya dapat mo-more than.
[10:12] Ang or... bale ang imohang basis is kani jud diri ang sakto. Nya...
[10:25] ...dwin sya diri ug 50 ra, nya didto sa pikas kay 100, dili ka ka-proceed. Imo ra i-error out nimo nga lot area, property lot area is lesser than project scope lot area.
[10:41] Kay... bale ang ang kuan ani, kani man ang existing property nimo.
[10:46] Mm-hmm.
[10:47] Let's say 50 ra na, nya mag-tukod ka 100, dili mao. Kay e- within ra ka sa imohang property area.
[10:58] So kung 50 ra ang limit ang sukod sa imomg property area, so 50 ra jud imohang project scope. Kung i-maximize jud nimo or lesser sa 50 square meter.
[11:08] Mm-hmm.
[11:09] So, kung niana sab sya diri lot area 100, so by default imo syang i-set ug 100.
[11:15] Oo.
[11:16] Pero kung gihapon usbon, let's say moingon na sya 50 ra man ang akong property area, dapat ma-correct ni sya. Kaning... lot area diri sa project.
[11:25] Mm-hmm.
[11:26] Dili sya mo-go beyond. So, either lesser sya sa property lot area or equal ang imohang project scope lot area.
[11:36] Mm-hmm mm-hmm mm-hmm.
[11:40] Na-kuha ra ba?
[11:41] Oo na-kuha na, na-kuha na.
[11:44] Nya I think sa highlight kaning sa number 2, so mao to concern gahapon. Unsa ba, ang screen nimo anas gagmay?
[11:54] Mm-hmm.
[11:55] Mag-sige'g scroll. Asa man nya kanang mag-wonder ba nganong dili pa enabled?
[12:00] So, na ba tay way nga mo-highlight nga "Oy, blangko pa ni." Example...
[12:07] Like kuan, kanang wala pa pala na-input-ti.
[12:09] Oo, na ba, ma-highlight sya ba nga "Oy..." naka, lage ha, atong gihisgutan nga...
[12:15] ...indicated nga required sya pero... na lage, dili kaayo techie ang ang user ba. Nya, gamay ka'y, gamay ka'y screen. Mag-sige'g, "Aas, asa man ni?"
[12:24] Mm, sige'g scroll.
[12:25] So, na ba tay way either i-highlight nato daan poa ang mga required para...
[12:33] ...makita dayon, or...
[12:35] Pwede pwede sad siguro ania if...
[12:37] Pwede man gani nang... naay way nga mo- ka- kanang ma-prompt sya nga kani kulang before sya ka-proceed, 'di ba? Disabled man jud ang ang button atong ani.
[12:45] Ma-disabled jud.
[12:46] So, maybe...
[12:47] Maybe scroll...
[12:48] So I think... kani na lang.
[12:51] Unsa ba'y... unsa'y mga bag-ong kuan ani?
[12:54] Naa siguro'y way ania if kanang i-scroll gani ang kanang kuan... dree pa-down, ana nya if dili ma-field ang igbao is pwede siguro'g naay kuan siguro or indicator, something.
[13:06] Like if if...
[13:08] Kani, mogbo man ang kuan, so, bisan ahno naay mga bag-ong pahi na or kato, kung pahi na sya, di kani box i- i-highlight na daan nga fill-an. So, ba ma- ma-kuan man jud nga let's say kung dili required, so aware sila nga kaning mga highlighted ba, kani ra ilang i-fill in.
[13:28] Mm-hmm. Sige, sige, pangitaon nato ang unsa'y pahi gihapon.
[13:31] Unless atong example, murag pareha atong sa register nga naka-enable na daan ang button, so inig-click ninyo'g ne- ne- kanang next barion nya naay kulang, mo-adto, mo-focus didto ang kuan.
[13:43] Mm-hmm.
[13:44] Ang... let's say ang cursor ba run? Or sa back, sa entry field nga empty ang... ang focus niya. Pero kani kay controlled man sya nga dili sya ka-proceed ug wala ma-fulfill.
[13:53] Mm-hmm mm-hmm.
[13:54] Unsa na lang i-way kay kani, gamay, 'di nga klaro sa ilaha ha, so maybe ang entire kuan entry field box may i-highlight ang mga required.
[14:10] Mm, sige sige.
[14:12] So, kung kani nga page, required man ni tanan, except aning kaning kuan. So, highlighted na sya, dapat ma-fill in nila.
[14:20] Mm-hmm. Nawala daw imong kuan sir, share screen sir.
[14:23] Ah, nawala diay, sir?
[14:25] Mm.
[14:31] Balik. Kana kana.
[14:39] Ah, kana.
[14:40] Mag-tab man gud ko.
[14:57] Um, so kana... Um, sa ika-tulo nga item...
[15:12] So, lot size, kuan diay... um, ang mga attachment, naay limit? 200?
[15:18] Oo, 200.
[15:20] Naay concern nganong dili ta ka-go beyond?
[15:25] Ah, I think wala ra, ah kuan ra jud, ah latency ra jud ana if kuan mo-bigger gani ang gihapon.
[15:32] Dako kaayo?
[15:33] Oo.
[15:34] Naa ba, naa ba may na-try before nga dako kaayo, nag-error or wala ka- wala ka-save?
[15:42] Kuan, ah kana jud, initially ang kuan ana jud kay 100 MB ra to. Nya, naay times na ni-kuan ni... gani na-am- na-abot ug limit katong gita-testing namo, so mao to amo nang gipasobraan to 200 MB.
[15:57] Total na na sa tibuok kuan?
[15:59] Mm.
[16:01] Nag-ana gihapon gi-try-an, nya mao lage to, namag dagg- gi-try jud sila ug kay naa man silay scanner nga dako so floor, mga floor plan dako man gud na ug kuan...
[16:09] Mm-hmm.
[16:10] ...dako ug file size ba. So, dako gani i-scan, 'di man pwede diperon nga murag imo i-compress iyahang i-scan niya, so dapat klaro man after scan.
[16:25] Sige, atoa pasab- kuan gi- mo-run na sa staging, gi- work on na gabeini kuan. Gihimo syang 500 MB.
[16:32] 500 MB ang usaka-submittan?
[16:35] Mm-hmm.
[16:40] Um, naay way nga unsa i- like ang mga ang I think akoang kuan ani sa mga prompt, klaro ang iyahang messaging sa unsa'y issue.
[16:49] Oo, ah dili ra generic ang kuan.
[16:52] Kay mao na, mag- mag-kuan man gud ang ang user, mag- mag-wonder ba unsa'y issue.
[17:05] Um, so, so 500 ang gi-kuan?
[17:07] Mm-hmm. So, atnan jud na attachment, sir, or per...?
[17:13] Per, unsa ba na sya? Kanang per attachment ang 200 or dili? Overall?
[17:17] Ah...
[17:18] Total sa, sa simple example sa kaning application...
[17:23] Kuan diay, per kuan diay na, per attachment 100. Nya karon sa bag-o na PR kay gi-kuan na sya, 500 na jud sya.
[17:33] So, dili per per file na sya, dili sya per the whole kuan?
[17:40] Like, ang a whole na jud na katong kuan i-submit.
[17:45] Ah, so, currently kay dili?
[17:47] Per i- per per file.
[17:49] M, per item.
[17:51] Pero ang inyong saving is upon submission, no?
[17:53] Oo, upon submission ang saving.
[17:55] Bale collated sya on the background unsa ang mga gi-pang-attach niya?
[18:01] Mm-hmm.
[18:04] Pero wala pa diay na sa kuan, wala pa na ma-write sa sa blog, gi-local ba?
[18:10] Oo, nya ang pod ana kay, na-gisinka pod sa like naa man ay limit i-select kay sa front end na part.
[18:17] Mm-hmm.
[18:18] Mm, ha katong initially kay gi-200 MB pod sa ditto. So, maybe pag-select ra, pag-select ra atong lapas 200 MB na file kay ni-kuan, ni-fail sa front end, wa pa kabut sa back end.
[18:33] So, naay tendency to naka-select ug file nga more than 200 MB ah dili 200, oh 200 MB.
[18:41] Mm-hmm.
[18:42] Ang ilang attachment?
[18:43] Oo, attachment, mm. Maybe sa front end to ni-fail, ana. Since naay limit sa front input.
[18:52] Kay nakita nila ang error dili during attachment, kay nag- gawas man sa front end nga na-attach niya.
[19:00] Na-attach.
[19:01] Pag-submit na niya, ditto nakita ang kuan...
[19:05] Ah, oo, sa kuan jud diay.
[19:06] ...ang error.
[19:08] Pag-submit na gi-ditto jud sa... Sige, i-look into further na amo na, sir.
[19:14] Especially kaning mga kuan kaning highly technical, dagko ni ug kuan kanang attachment.
[19:22] Mm-hmm.
[19:23] Additio- additional. So, so klar- ang kuan nato is 200 MB per attachment.
[19:31] Mm-hmm.
[19:34] Sige, sample diri, asa asa man diay sample gihapon, or wala to ma-proceed guro kay wa man ila ma-submit.
[19:47] Sige, ah, amo lang gihapon tatasan.
[20:00] Speaker 1: kuan man... So, kuan man pod sa kuan sa, Master Nuts, unsa gani to nakakita ato, nag-kuan gani sa encoder?
Speaker 2: Mm.
Speaker 1: Naa man gud reports kuan ah, mao to hitabo pad pad-submit kay kani man gud,

[20:17] Speaker 1: Ay, ang ang gi-explain ni Master Nuts, gi-compute niya. Naabot og... 200?
Gi-total man to niya, Master Nuts? 200 hinuon tanan attachment? Or are more than 200, mao man 'yung pagka, pagka-mention gahapon.

[20:45] Speaker 2: Kuan man guro ni, gi... No, gi-unsa man gani ni? Sige, i-ambush lang ninyo i-kuan sa...
Speaker 1: Gi-double-check lang gud whether, whether total uploaded files or kuan, per file. So, sa karon, base sa emong review, per file ang supposed to be 200, dili overall?

[21:15] Speaker 2: Dili. Dili pod giapon per file kay ang sa kuan sa PR kay ang description sa PR diri sa bag-o kay per file gi-increase gyud sya. Per file. Oo. Nya ang kuan, ang overall iyang gi-submit kay gi-2 gig.

[21:30] Speaker 1: Aso na naa, naa ba'y gi-sub, sa previous implementation, naa ba mo'y gi-set na nga, nga limit nian sa total? Kana'ng overall?
Speaker 2: Dili.
Speaker 1: Nag-check man gud mo.
Speaker 2: Sa overall gyud so? So, kuan ba dili pod guro ka, kuan pod guro 'y...
Speaker 1: Ah, kuan lang nga, mura'g ang kuan nato diha is as much as possible flexible lang gyud ba nga...

[21:50] Speaker 2: Flexible gyud sya. Mm.
Speaker 1: Dili ta kana gani'ng strict sa kuan, kana'ng pilay file size i-upload.
Speaker 2: Mm. So, wala ra gyud syay limit.
Speaker 1: Mm, ideally ingana unta gyud kay wala ta kahalo unsa'y ipang-attach diha gyud. So, as long as unless og kana'ng limitation gyud sa infrastructure, say katulad sa Azure nga dili gyud sila kasegure ingana nga file size sa sa blob then that's kuan gyud, diha na ka mag-limit. Pero allowed ra, ang concern na diha is ang pag-handle lang sa frontend nga in process pa sya sa pag save sa files nga kana gani'ng para dili mo time out emohang kuan, nga nag nag-write pa padulong sa sa blob sa mga attachment nimo.

[22:46] Speaker 1: Anyway, kuan ra man pod sya, government ra man pod na ang mosagay mag mag-process ana, dili pa man gyud ta ka-expect nga mga online applicant gyud ang mo-kuan ana sa ilahang requirements. Mao na ang kuan pod, ideal implementation nga even kana'ng applicants can apply online gyud ani, later. Pero sa karon, magsugod sila nga tanan encoding ah, ari mag magikans sa opisina, sa kay katulad sa mga plans, dili ta ka-expect ang mga user naay mga scanner nga dagko kayo nga makascan og mga floor floor plans ba.

[23:00] Speaker 1: So, naa man ni sa opisina ron sa OBO, so sila gyud ti-scan, na mao nang naa silay encoder.
Speaker 2: Mm.
Speaker 1: So, sa katon sa concern sa latency sa sa pagprocess sa upload, ang I think ihandle, mas kuan lang gyud is regardless sa unsa'y size sa file, or overall total sa katang attachment, ah, ma-handle lang sa UI nga nga nagprocess pa gihapon sya, saving pa gani, ana. Ma-visualize lang gyud sa user ba nga nag-save pa ka kay dagko kayo emohang file nga gi-attach.

[24:05] Speaker 2: Sige, sige.
Speaker 1: Okay. Uh... Kaning certificate of title, ah, okay na man ni. Niyong si Julie kay ari man daw i-attach sa kuan, kaning proof of ownership, diri man ni. Kaning subdivision approved plan, naa ba tay others nga option asa?

[24:44] Speaker 2: Sa kuan, upload sa kuan...
Speaker 1: Kani man, wa wa man pod content, supporting documents. Pwede ni diri, no?
Speaker 2: Supporting documents, I think sa kuan ni sya...
Speaker 1: Kaning, i-cover ninyo let's say, mga optional man pod sa division approved plan.
Speaker 2: Supporting documents...

[24:58] Speaker 1: Ah, diri, no. Pwede ra siguro unya diri.
Speaker 2: Nya ang... sa highly technical...
Speaker 1: Kani, mga clearance ninyo, specific in description. Kani, pa-mga-ani, mga lead request.

[25:28] Speaker 2: Specifications...
Speaker 1: Tax declaration, barangay...
Speaker 2: Big Barangay, uh...
Speaker 1: Mark, kani? Pwede guro diri, bai?
Speaker 2: Ah, pwede.
Speaker 1: Mag-add kag "Others" diri?
Speaker 2: "Others"?
Speaker 1: Oo. Nya, "Any" na lang ilahang i-upload para...
Speaker 2: Sa muapply na sa overall gyud sya? Sa simple sa complex og highly.
Speaker 1: Mm.

[26:50] Speaker 1: So, kaning sa number 4, kaning certificate of title, mao man pod giingon ni Julie nga ari under sa kuan, proof of ownership. Okay na na diha. Ang kanilang subdivision approved plan, unified application doc, wala man tay specific ana, so lisod kay magsige tag add og kuan. So, probability diri, sa supporting documents, I-specify gyud sya, sa unsa na, kaming subdi- subdivision approved plan, or "Others"? Dili. "Others" lang, then attach any.
Speaker 2: Ah. Sige, sige.
Speaker 1: So, attach dira, either kana'ng subdivision approved plan, unified app doc, diha na lang nato i-capture ang any, any additional attachment nila sa kaning, kaning nga application.

[26:50] Speaker 2: "Others" nya. Murag sa...
Speaker 1: Open, oo, open ra sya ba. Walay specific kuan, ah, unsa nga document iyang gipangita. Basta anything, any attachment nga wala ma-capture so far sa kaning mga naay, ah, supposedly slot specific nga attachment. Mm. So, kung naa pa silay mga additional documents nga need nila i-attach sa application, mag-add lang ta diri'g "Others" nya, "Other supporting documents" nya... or "Others" na lang, "Others" nya attach na, unsa'y gusto ninyo.
Speaker 2: Mm.
Speaker 1: And then...

[27:33] Speaker 2: Unsa pa kuan ba? Number 8?
Speaker 1: Ah, is it attachment? Oo. So, ang atong kastorya ani, ang technical, ang engineer...
Speaker 2: Mm.
Speaker 1: Naa daw silay, kay di ba naa silay mga discrepancy nga nakita-an sa application.
Speaker 2: Mm.
Speaker 1: So, mo- instead of kuan daw, or na- probably naay mga gamay nga wordings, and then para ma-highlight gyud kuno asa ang mausab nun, murag i-screen capture nila ang portion sa document nga asa naay problema. Nga mao'y i-attach nga kana'ng murag supporting...
Speaker 2: Mm.
Speaker 1: ... image sa ilahang note.

[28:17] Speaker 2: So, dili na sya i-text, or i-attach?
Speaker 1: Oo, mo- aside, aside sa text,
Speaker 2: Ah, oo.
Speaker 1: naay, naay image or mak-attach sya'g la- kana'ng specific, either pdf file ba ron nga naa didto ang naka-circle niya ang unsa'y ipa-correct nila.
Speaker 2: Mmm, sige sige.
Speaker 1: Mwana sa number 8. Mm.
[30:00] Ah kuwan pala, sorry.
[30:05] Kani daw bai dili sya kuwan number seven.
[30:14] So kuwan dili sya accurate?
[30:16] Mm, like gahapon nag- mga 12:00 mi ato, iyang gipakit kay 6:00 buntag. Sakto ra ang date?
[30:26] Oo, ang time kay kuwan
[30:27] Ang time kay dili.
[30:30] Mm, sige sige. I-take na kuwan puydi na ma-fix man pod ni.
[30:36] Mao na ang number seven.
[30:39] Naa sa staging.
[30:41] Mm. And then, I think search cold admin.
[30:56] Kuwan ni nakong ma-list.
[31:08] Kani, inig
[31:11] Ari diay, katong aba-sato.
[31:15] Then, kani, ah username?
[31:21] 20 na ba ang limit sa kani?
[31:26] Mm, sige. 100 lang pod.
[31:28] Ah.
[31:30] Then katong kuwan gihapon, um kung may error, specific lang unsa.
[31:42] Related ra pod ni sya kaining number one. Email ug username.
[31:50] Pa-double check lang pod diri kaining first name sa mga kuwan ani.
[31:59] Um, and then I think um next kuwan, kung makalimot sa kuwan bai password, pwede ba ta ang admin mismo maka-kuwan, maka-change password?
[32:16] I think naa man siguro na sa- ah wala pala no.
[32:18] Wala, manage role ra.
[32:20] Oh, role ra diay.
[32:21] Naa syay kuwan individual kanang mo-log in ka mismo pwede ka ka- ka-change pass. Pero naa gyud tendency makalimot gyud ang user.
[32:32] Ang user, so
[32:35] oh naa ba'y mag-add diri og action change password?
[32:38] Dili diay kani mag-kuwan ta kanang mag-involve og kanang legit gyud na email nila ba? Or
[32:49] Dili na kanang imo, as admin man ka. Admin man ang pwede pod mo-
[32:54] Ay, as admin ra diay.
[32:56] Oo, as admin.
[32:57] Ang admin ra na role, Sir, or apil pod ang ubang kuwan diri, encoder?
[33:01] Kani rang sysadmin.
[33:03] Sysadmin ra?
[33:04] Sige, lag- oo, kaning super admin siguro.
[33:07] Ah, sige sige. Super admin ang kuwan.
[33:15] Nya, ako last bai, naa dali ra ba ma- unsa gani? Maricor, final reviewer. Maricor, P-assessor. Maricor, initial-
[33:27] Multiple role.
[33:30] Multiple?
[33:31] Same ra na nga tao?
[33:33] Same ra sya na kuwan?
[33:35] Oo, ma-design ba nato nga let's say kung ako si Maricor-
[33:38] Dili to name ilang- ah same ilang kuwan, Sir? Username nila?
[33:42] Gi-lahi-lahi lang gyud to pero in actual
[33:46] usa ra ka tao.
[33:49] Dili, let's say kung ako si Maricor, naa koy initial reviewer one.
[34:02] Nya
[34:17] So, ang tendency, mana og review ko, mana ang encoder.
[34:22] Mm.
[34:23] Nya, okay na sa ako, ako i-complete, nya pasa sa technical.
[34:29] Mm.
[34:30] Nya, ihuman sa technical, mubalik man sa iyaha, nya human mo-proceed sa P-assessor.
[34:38] Mm.
[34:39] So, ang tendency ana, labi na procito P-computation.
[34:43] Ang tendency ani, ang next tao ani, sya gihapon. But, dili sya maka-perform ani kay currently log in man sya as initial reviewer.
[34:53] Ah.
[34:54] So, iyahang i-button log out sya.
[34:57] Nya kuwan sya, kanang log-in na pod sya og P-assessor.
[35:06] Pero, sya ra ni.
[35:08] So, atong i-fix kuwan na, Sir? E-multi-role or unsa?
[35:10] Mao na, ang- mag- ma-design ba nato nga like
[35:17] dili sya necessary mo-log out?
[35:20] Adto na lang ka sa sulod mo- murag naa syay drop down change- change role.
[35:24] Ah.
[35:26] Or, unsa may mas dali para ninyo? Para lang dili maguba ang design sa kuwan karon.
[35:33] Kanna siguro is
[35:35] mas dali siguro i-change ra or since 'di ba each role kay 'di ba lain man og UI gyud?
[35:41] Oo, lain-lain man og UI.
[35:43] Murag
[35:44] Para dili lang, dili na mo mag-redesign ba nga ah kani, enable ni- kung sya
[35:49] Oo.
[35:50] Or kuwan na siguro katong imong suggestion na i-drop down siguro change role if kanna sya allowed ra sa kanna na role nya ma-usab pod ang kuwan dayon iyang ipakita.
[35:59] Oo, ana na lang ako- ana lang akong ay, para lang dili lang ma-kuwan kay dako man og usbon nato og kuwan, i-allow gani ni sya nga ma- mag-P-assessor pod sya.
[36:10] So, murag naa ra syay kuwan nga diri ra gihapon sya, nya
[36:14] Oo, ma-un-part.
[36:15] either
[36:16] akoa or basta kanang ing-ana lang ang to- to process sa pag-address ani nga concern nga multi-role ang usa ka tao didto.
[36:24] Mm. So, So, mura- mao ra syay pina ka-kuwan pod.
[36:27] So, para kung mo-single sya, ah P-assessor ra ko. So, mo- mo-change pod diri, nya maka- based ani nga status, ma- kuwan na niya nga kuwan, ma- pwede na niya ma-mark as payment pending.
[36:43] Nya, kung mo-ingon na pod sya didto naa'y mag-pay or either mag-depende kung let's say iyang tan-awon nga status submitted, imo syang i-act as initial reviewer or
[37:01] kung for fee computation, imo syang i-assess, naa ba syay role as kuwan, wala lang tong drop down drop down para dili na lang pod labad, mag-base ra ka sa status?
[37:13] Mag-base sa status?
[37:14] Nya, inig-click nimo sa action, imo i-validate nga naa ba syay role as P-assessor para maka- ma-change ang kani nga kuwan, kani nga UI diri?
[37:27] Ah, kani ra man gyud ang babaw ang inyong gilabtan, 'di ba?
[37:30] Mm, kani ra gyud.
[37:31] Ang da-rest ani mao ra man gihapon, 'di ba?
[37:33] Mm. Sige, sige. I-will consider ana, Sir, kung unsa'y mas dili- dili hassle ba.
[37:37] Oo, wala na lang katong kuwan, lesser, lesser click sa user ba.
[37:42] I-kuwan na lang, ah si Maricor ra gihapon na, i-validate nako si Maricor maka- act ba sya as initial reviewer, act as kuwan.
[37:51] Um, but sa side sa pag-manage sa kuwan, sa account,
[37:57] unsaon man na sya kuwan, kuwan like
[38:02] Like sa pag-manage sa account?
[38:04] Need ba sya og ana-ana or inig inig-create sa account, i-check-check na lang pod diri?
[38:13] Pwede siguro. Like for example, ah katong Maricor, dug- dugay daw, nya pwede siguro i-display na siguro iyang
[38:22] mga allowed roles siguro diri.
[38:24] Murag naa kay i-list tanan, nya naa kay tickbox diri nga ah kuwan ni sya, ah initial reviewer, P-assessor, final reviewer.
[38:35] Mm.
[38:37] Kay karon individual man ni mag-create 'di ba, isa-isa?
[38:39] Individual. So, balid diri siguro sa UI, unang role na column kay i-display na siguro ilang kuwan diha, ilang allowed na roles.
[38:49] Kanna mao ma- mao na akong isa sa murag dako-dako trabahoon. Pero tan-awon, basig naa ra kay way ma- padali.
[38:58] Sige, mao ra pod na'y kuwan.
[39:00] Kay mao man pod kay kuwan gyud, actual na hitabo ra man. Usa ka tao didto, tulo iyahang role.
[39:06] Mm.
[39:07] Nya, so gikan sya initial reviewer nya naa'y gap isa ka stage kay ah technical, mag-buhat sya, pero
[39:14] after sa technical, initial reviewer ra gihapon. Nya, i-pasa sa P-assessor, which is sya ra gihapon. Nya inig human na og bayad, na-validate na ang bayad, mo-attach na sya sa mga ah resibo,
[39:30] pasa sa final reviewer, which is sya ra gihapon. So, ang tendency tulo iyahang account. So,
[39:38] medyo tedious sa iyaha nga, "Ay, mag-log out pa ako kay kuwan na pod ako karon."
[39:46] Mm, sige. Mao ra na iyahang kuwan, Sir.
[39:48] Mao lang na, wala na, mao na'y wala nako ma-list. Ha, kanto ra man siguro, so far.
[39:56] Naa'y naa'y kuwan? Naa'y wa ma-klaro?
[40:00]
Ah, wala. Naa, klaro ra tanan.
Dugay ani.
Ah, diha, diha.
Ah, oo.

[40:17]
Ah, okay.
Iyang gusto, anties obo consolacion.gov, niya ang napalit man gud nila nga domain is kani man gud diay.
So, obo kuan diha.

[40:31]
Obo niya lgu.
Mas mubo lang kaysa ani.
Tagaan og link niana.
Okay na ra ang number six.

[40:45]
Anus-a iyahang target na kuan diha, sir?
Kuan sila, murag ganahan sila mag-live next, unsa gani sa next month?
Karon nag-test sila.
Ang nakalangan nimo, ang scanner nila nadeliver na.
Unsa ba 'to? August or July ba 'to?

[41:05]
Problema ug mura ra gi-butang didto, wala gi-set up ba nga maka-scan ba, ma-save, kay mura man siya og kanang network scanner.
Mm.
Gi-butang ra ang scanner sa ga-deliver ba, niya wala gi-

[41:18]
gi-configure, gi-test nga maka- ma-save ang mga gipang-scan padulong sa computer, ing-ana gani? So,
huwat pa sa Buwan.
Langan kayo, niya
kani pag, pag-sa atong gihapon, mat- kanang
para ta mag-final, na-apanakit-an sila.

[41:40]
Mm.
Kani sa, ah, sa mga maka-lugar,
di ba mandomobisi ingon sa master nut, so mandomocliente ba?

[41:48]
Mura'g wala man, na-powa man sa kuan.
Karon kay gi-kuan man sa growth. Di ba naa man 'yung availability, no?
Ah, ingon sa, ingon mga internal app kuan ra, kanang MCP ra.

[42:00]
Ang, ang internal?
Kasi gi-pabilai update sa app mismo sa growth?
Oo, sige daghang og kuan, kanang changes bag-o karon sa UI/UX na side.
Kinsa nay dad-a, Harvey?

[42:15]
Oo, ah, previously, pag last week man siguro 'to, oay. Nya karon kay si Ms. Marissa na ang ga-handle sa internal.
Mm.
Di man daw mo, mo-tubag Harvey sa chat ninyo?
O, di, si Roy.

[42:30]
Unsa may, unsa may gi-busy-han ana nila kung mag- mag- sprint planning, o si Cherry man gyud ga-dala kuan no?
Mura'g karon kay sir, kay ako ra gyud nag-kuan atong kuan mi kagabii sa Fastrack, no.
Kinsa'y nagdala?
Akoi gani, kuan, ako'y nag-PM nila.

[42:48]
Atani kay wala man si Harvey.
Mura'g di, mo-reply na ug tag-next week na iyang reply.
Gahia sad anaa.
Ang ma-PR kay wala na kuan na, nag-luttaw na.
Iya gihapon na diha, ay?

[43:03]
Mura'g karon kay na-usab na man ang kuan, kay gi- si Ms. Marissa na.
Mura'g nag- nag-kuan man sila, mura'g nag- re-org sa ilang management. Mura'g people focus na silang Harvey, Renato, El. Nya si Marissa og si Lloyd sa technical.

[43:24]
Sa mga internal sila nang kuan.
Mm.
Pero ang time clock mura'g si MasterNut man gihapon ang nagdala, kay mao may ingon Daryl.
Mm.

[43:38]
Nya, kani rang, ah, i-engnan nako file-ang ing-ani.
Mura'g gi-atubang sad mi'y, gi-atubang sa milyon diha na sir, ha.

[43:46]
Unsa ta'y ngalan sa kuan? Iyang gi-pahi-Lores, Yalola?
O, Yalola. Tugpa'g sa Mindanaw karon.
Ah.
Nawala pa mo didto, so wa'y problema.
Mm.
Si Van, nag-resign ba si Van?

[44:03]
Si Van, nag-resign na?
Van Borja?
Wala ko kabantay ana sir.
Taha 'nia, murag naa ma'y hiring sa ilang kuan.
EI.
Ay, naa man ka'y atong Devops, sir, di ba?

[44:19]
Oo, Devops.
Wa 'to kay, ga- ga- daan na 'to nako atong sila Khael, kay wala na man.
Ah, gi-gi-operan atong atong gi-kuan si Khael, wa man, kay sakto ra padulong iyahang na-receive, dako-dako sad gyud.

[44:41]
Kanang, kumpan- kuan pa si kani, kanang, okay pa si Matinhon.
Aha, ikaw, pila ka kuan na ka? Kai wa pa man, wa pa man akoang rot nga nadawat, o-eng, sa puhon na lang.

[44:59]
Mandait pa mo'g two, two, two years na?
Mm, 2 years.
Ah, pag- pag-ahe na sad ug maayo. Pero siguro pod og ma-kuan na pod clients, pero karon nga time, unso'y kuan, piskal, mag-plano pa, budget pa, usually ana thing, higating draft karon, less ang

[45:19]
ang add, kay mag- mag-budget pa for, for next year, so expected na daghan gyud mo'g bench, arong nga time, first quarter.
Mo-kusog na 'g balik kung, mga first quarter kanang next year, kung naa na'y budget ang mga customer ug kuha'g developer.
Ang amoang gi-kuan, kay gamay, gamay ra man gyud 'yung UI/UX didto sa kuan.

[45:42]
Pila lang ta ka buok? Tulo ra man seguro 'to.
Oo, daghan man, pero, panang pangitaon ra man gyud nang sales as-a mo ma-assign.

[45:53]
Sige, bay. Naa pa kay ipangutana? Naa pa'y kuan?
Wa na man sad, ma-mo reach out lang nya mi, sir, og naa pa'y kuan.
Ah, sige.
Ing-ana lang sa ha?
A, sige, sir, nay-naya lang mi'g kuan, unsa lingaw karon.
Oo.

[46:08]
Sige, bay, salamat.
Sige, salamat, sir.
Bye-bye.
Bye-bye.
