This version of Tianxia has the first (very WIP) version of the Grace rework implemented. Localisation is very WIP, and AI logic is fairly non-existent in many locations. This version is NOT ready to be released in a public patch, but it might do for the Closed Alpha (though, as mentioned, this is still fairly WIP).

As far as I can tell (after running a test game playing as the EoC for about 2 years and running an observer game for 10 years), there is nothing causing a CTD and no blank events, so hopefully this version is playable, even if not final.

It is a bit uncertain if the AI can the Grace decisions at the moment (I don't notice any log outputs about it), but since it is set to only check them rarely and might not have the money/etc. during the 10 years I tested for it is possible that it can use things.

I have tried a few Grace decisions from various rulers other than the EoC and fired all the initial events for the EoC, and things seem to work, but something might have slipped through the cracks, so let me know if something appears to be broken.


It is fine to make changes to many files, but please leave the following files alone for now (it is fine to look at the code if you want to):
- jd_grace_decisions.txt
- tianxia_grace_decisions.txt
- jd_artifact_events.txt
- jd_china_succession_events.txt
- jd_chinese_diplomacy_events.txt
- jd_chinese_invasion_events.txt
- jd_chinese_status_and_policy_events.txt
- jd_chinese_war_events.txt
- jd_grace_decision_events.txt
- jd_kowtow_events.txt
- tianxia_grace_decisions_events.txt
- 00_scripted_effects.txt (only the China-related parts)
- 00_scripted_triggers.txt (only the China-related parts)
- 00_tianxia_grace_triggers.txt


Additionally, keep the following in mind:
- If you add/change any CBs, make sure that the blocker for Chinese Peace Deals is in place and that the EoC gets upset if you attack him. Check the existing CBs for this logic and shoot a message @Silversweeeper if you are unsure of how to do this.
- If you modify feudal_governments.txt, make sure that a (Taoist, at minimum) holder of e_china and his heir use the chinese_imperial_government
- Referencing offmap_china, e_china_west_governor, and offmap_currency should hopefully not cause a crash, but since these things are not in use and we'd have to replace these references with the proper ones in the future it is better to reference the proper Grace mechanic, and for now I'd like for it to be left alone so that I can do whatever I want with without breaking things
- If you want to make the events in jd_raiding_china.txt compatible, make sure you check for e_china (and/or worldchina) rather than "raiding" the offmap title


// Silverswee(e)per