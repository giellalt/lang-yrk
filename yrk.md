


















* Sets for POS sub-categories





* Sets for Semantic tags





* Sets for Morphosyntactic properties






































































































































































* Sets for verbs


- V is all readings with a V tag in them, REAL-V should
be the ones without an N tag following the V.  
The REAL-V set thus awaits a fix to the preprocess V ... N bug.



* The set COPULAS is for predicative constructions







* NP sets defined according to their morphosyntactic features







* The PRE-NP-HEAD family of sets

These sets model noun phrases (NPs). The idea is to first define whatever can
occur in front of the head of the NP, and thereafter negate that with the
expression **WORD - premodifiers**.












The set **NOT-NPMOD** is used to find barriers between NPs.
Typical usage: ... (*1 N BARRIER NPT-NPMOD) ...
meaning: Scan to the first noun, ignoring anything that can be
part of the noun phrase of that noun (i.e., "scan to the next NP head")






* Miscellaneous sets





















* Border sets and their complements













* Syntactic sets




These were the set types.



## HABITIVE MAPPING


* **hab1** 


* **hab2** 

* **hab3** (<hab> @ADVL>) for hab-actor and hab-case; if leat to the right, and Nom to the right of leat. Lots of restrictions.



* **habNomLeft** 


* **hab4** 	



* **hab6** 

* **hab7** 

* **hab8** This is not HAB
* **hab5**  This is not HAB



* **habDain** (<hab> @ADVL>) for (Pron Dem Pl Loc) if leat followed by Nom to the right




* **habGen** (<hab> @<ADVL) hab for Gen; if Gen is located in the end of the sentence and Nom is sentence initial










































































* **spred<obj** (@SPRED<OBJ) for Acc; the object of an SPRPED. Not to be mistaken with OPRED. If SPRED is to the left, and copulas is to the left of it. Nom or Hab are found sentence initially.


* **Hab<spred** (@<SPRED) for Nom; if copulas, goallut or jápmit is FMAINV and habitive or human Loc is found to the left. OR: if Ill or @Pron< followed by HAB are found to the left.

* **Hab>Advlcase<spred** (<ext> @<SUBJ) for Nom; it allows adverbials with Ill/Loc/Com/Ess to be found inbetween HAB and <ext>.

* **Nom>Advlcase<spred** (<ext> @<SUBJ) for Nom; it allows adverbials with Ill/Loc/Com/Ess to be found inbetween Nom and <ext> @<SUBJ.

* **<spred** (<ext> @<SUBJ) for Nom; if copulas to the left, and some kind of adverb, N Loc, time related word or Po to the left of it. OR: if Ill or @Pron< to the left, followed by copulas and the before mentioned to the left of copulas. 

* **<spred** (<ext> @<SUBJ) for Nom, but not for Pers. To the left boahtit or heaŋgát as MAINV, and futher to the left is some kind of place related word, or time related word


* **<spredQst1** (<ext> @<SUBJ) for Nom in a typically question sentence; if A) Hab, some kind of place word, Po or Nom to the left, and Qst followed by copulas to the left. B) same as a, only the Qst-pcle is attached to copulas. C) Qst to the left, with copulas to its left, but not if two Nom:s are found somewhere to the right. D) copulas to the left, and BOS to the left. E) Loc or Ill to the left, and Loc or Hab to the left of this, Qst and copulas to the left. F) Num @>N to the left, Hab, some kind of place word, Po or Nom to the left, and Qst followed by copulas to the left. NOTE) for all these rules; human, Loc or Sem/Plc not allowed to the right.

* **<spredQst2** (@<SPRED) for Nom; in a typically question sentence; differs from <spredQst1 by not beeing as restricted to the right. Though you are not allowed to be Pers or human.

* **Nom<spredQst** (@<SPRED) for Nom; in a typically question sentence. Differs from <spredQst2 by letting Nom be found between SPRED and copulas



* **<spred** (@<SPRED) for A Nom or N Nom if; the subject Nom is on the same side of copulas as you: on the right side of copulas

* **<spredVeara** (@<SPRED) for veara + Nom; if genitive immediately to the right, and intransitive mainverb to the right of genitive

* **leftCop<spred** (@<SPRED) for Nom; if copulas is the main verb to the left, and there is no Ess found to the left of cop (note that Loc is allowed between target and cop). OR: if you are Coll or Sem/Group with copulas to your left. 

* **<spredLocEXPERIMENT** (@<SPRED) for material Loc; if you are to the right of copulas, and the Nom to the left of copulas is not a hab-actor


* **NumTime** (@<SPRED) for A Nom

* **<spredSg** (@<SPRED) for Sg Nom	

* **<spredPg** (@<SPRED) for Pl Nom	

* **<spred** (@<SPRED) for Nom; if copulas to the left, and Nom or sentence boundary to the left of copulas. First one to the right is EOS.

* **<spred** (@<SPRED) for N Ess

* **spredEss>** (@SPRED>) for N Ess; if copulas to the right of you, and if an NP with nom-case first one to your left.

* **HABSpredSg>** (@SPRED>) for Nom; if habitive first one to the left, followed by copulas.

* **GalleSpred>** (@SPRED>) for Num Nom; if sentence initial

* **spredSgMII>** (@SPRED>)

* **r492>** (@SPRED>) for Interr Gen; consisting only of negations. You are not allowed to be MII. You are not allowed to have an adjective or noun to yor right. You are not allowed to have a verb to your right; the exception beeing an aux.



* **AdjSpredSg>** (@SPRED>) for A Sg Nom; if copulas to the right, but not if A or @<SPRED are found to the right of copulas

* **SpredSg>Hab** (@SPRED>) for Nom; if you are sentence initial, copulas is located to the right, and there is a habitive to the right of copulas



* **Spred>SubjInf** (@SPRED>) for Nom; if copulas to the right, and the subject of copulas is an Inf to the right

* **spredCoord** (@<SPRED) coordination for Nom; only if there already is a SPRED to the left of CNP. Not if there is some kind of comparison involved.






* **subj>Sgnr1** (@SUBJ>) for Nom Sg, including Indef Nom if; VFIN + Sg3 or Pl3 to the right (VFIN not allowed to the left) 

* **subj>Du** (@SUBJ>) for dual nominatives, including Coll Nom. VFIN + Du3 to the right. 
* **subj>Pl** (@SUBJ>) for plural nominatives, including Coll and Sem/Group. VFIN + Pl3 to the right.

* **subj>Pl** (@SUBJ>) for plural nominatives


* **subj>Sgnr2** (@SUBJ>) for Nom Sg; if VFIN + Sg3 to the right.

* **<subjSg** (@<SUBJ) for Nom Sg; if VFIN Sg3 or Du2 to the left (no HAB allowed to the left).




















* **f<advl** (@-F<ADVL) for infinite adverbials

* **f<advl** (@-F<ADVL) for infinite adverbials



* **s-boundary=advl>** (@ADVL>) for ADVL that resemble s-booundaries. Mainverb to the right.




* **-fobj>** (@-FOBJ>) for Acc 

* **-fobj>** (@-FOBJ>) for Acc




* **advl>mainV** (@ADVL>) if; finite mainverb not found to the left, but the finite mainverb is found to the right.


* **<advl** (@<ADVL) if; finite mainverb found to the left. Not if a comma is found immediately to the left and a finite mainverb is located somewhere to the right of this comma.




* **<advlPoPr** (@<ADVL) if mainverb to the left.
* **advlPoPr>** (@<ADVL) if mainverb to the right.



* **advlEss>** (@<ADVL) for weather and time Ess, if FMAINV to the left.






* **advl>inbetween** (@ADVL>) for Adv; if inbetween two sentenceboundaries where no mainverb is present.

* **comma<advlEOS** (@<ADVL) if; comma found to the left and the finite mainverb to the left of comma. To the right is the end of the sentence.



* **advlBOS>** (@ADVL>) if; you are N Ill and found sentnece initially. First one to your right is a clause.


* **<advlPoEOS** (@<ADVL) for Po; if you are found at the very end of a sentence. A mainverb is needed to the right though.



* **cleanupILL<advl** (@<ADVL) for N Ill if; there are no boundarysymbols to your left, if you arent already @N< OR @APP-N<, and no mainverb is to yor left.











* **<opredAAcc** (@<OPRED) for A Acc; if an other accusative to the left, and a transtive verb to the left of it. OR: if a transitive verb to the left, and an accusative to the left of it.


### sma object









* **<advlEss** (@<ADVL) for ESS-ADVL if; FMAINV to the left
* **<spredEss** (@<SPRED) for N Ess if; FMAINV to the left is intransitive or bargat





## SUBJ MAPPING - leftovers

## OBJ MAPPING - leftovers


## HNOUN MAPPING
















* * *
<small>This (part of) documentation was generated from [../src/cg3/functions.cg3](http://github.com/giellalt/lang-yrk/blob/main/../src/cg3/functions.cg3)</small>
# Morphology
INTRODUCTION TO THE MORPHOLOGICAL ANALYSER OF NENETS

# Definitions for Multichar_Symbols@CODE@

## Analysis symbols
The morphological analyses of wordforms of the TUNDRA NENETS language are presented
in this system in terms of following the symbols.
(It is highly suggested to follow existing standards when adding new tags).
* **+WORK+TYÄ** WORK HAS TO BE DONE Do not remove, replaces +TYÄ
The parts-of-speech are:

* **+N**@CODE@****
* **+A**@CODE@****
* **+Adv**@CODE@****
* **+V**@CODE@****

* **+Pron**@CODE@****
* **+CS**@CODE@****
* **+CC**@CODE@****
* **+Adp**@CODE@****
* **+Po**@CODE@****
* **+Pr**@CODE@****
* **+Interj**@CODE@****
* **+Pcle**@CODE@****
* **+Num**@CODE@****



The parts of speech are further split up into:

* **+Prop**@CODE@****
* **+Pers**@CODE@****
* **+Dem**@CODE@****
* **+Interr**@CODE@****
* **+Reflreflexive** reflexive
* **+Recipr**@CODE@****
* **+Rel**@CODE@****
* **+Indef**@CODE@****
* **+Refradverbs** referential adverbs



Adv
* **+Manner**@CODE@****
* **+Refr(referential),** (referential),
* **+Temp**@CODE@****

The Usage extents are marked using the following tags:
* **+Err/Orth**@CODE@****
* **+Use/-Spell**@CODE@****
* **+Use/SpellNoSuggspeller** recognized but not suggested in speller

* **+Rushomograph)** (100% Russian homograph)


Dialects

* **+Dial/Wdialects),** (Western dialects),
* **+Dial/T),** (Taimyr dialect  ),
* **+Dial/Edialects),** (Eastern dialects),


The nominals are inflected in the following Case and Number

* **+Sg**@CODE@****
* **+Du**@CODE@****
* **+Pl**@CODE@****
* **+Acc**@CODE@****
* **+Gen(Genitive)** (Genitive)
* **+Abl**@CODE@****
* **+Dat**@CODE@****
* **+Loc**@CODE@****
* **+Nom**@CODE@****
* **+Pros(Prosecutive)** (Prosecutive)
* **+Tra**@CODE@****
* **+Abe**@CODE@****
* **+Adc**@CODE@****
* **+Ins**@CODE@****
* **+Apr**@CODE@****
* **+Ine**@CODE@****
* **+Ill**@CODE@****
* **+Ela**@CODE@****
* **+Egr**@CODE@****
* **+Prl**@CODE@****
* **+Predpredestinative** = predestinative

are these needed?:

* **+Appr**@CODE@****
* **+Advc**@CODE@****
* **+Ter**@CODE@****
* **+Pro**@CODE@****
* **+Car**@CODE@****
* **+Equ**@CODE@****

derivative suffixes before case endings
* **+Limlimitative** limitative


The possession is marked as such:


* **+PxSg1**@CODE@****
* **+PxSg2**@CODE@****
* **+PxSg3**@CODE@****
* **+PxDu1**@CODE@****
* **+PxDu2**@CODE@****
* **+PxDu3**@CODE@****
* **+PxPl1**@CODE@****
* **+PxPl2**@CODE@****
* **+PxPl3**@CODE@****

The comparative forms are:
* **+Pos**@CODE@****
* **+Comp**@CODE@****
* **+Superl**@CODE@****

Numerals are classified under:

* **+Attr**@CODE@****
* **+Card**@CODE@****
* **+Ord**@CODE@****

Verb moods are:

* **+Ind**@CODE@****
* **+Pot**@CODE@****
* **+Conj**@CODE@****
* **+Imprt**@CODE@****
* **+Opt**@CODE@****
* **+Hort**@CODE@****
* **+Mod/apprimperfective** approximative imperfective
* **+Mod/desdesiderative** desiderative
* **+Mod/futapprfuturitive** approximative futuritive
* **+Mod/hyphyperprobablitative** hyperprobablitative
* **+Mod/intinterrogative** interrogative
* **+Mod/narrnarrative** narrative
* **+Mod/necnecessitativee** necessitativee
* **+Mod/oblobligative** obligative
* **+Mod/repreputative** reputative
* **+Mod/supsuperprobabilitative** superprobabilitative
* **+Mod/perfapprperfective** approximative perfective
* **+Mod/perfprobprobabilitative** perfective probabilitative
* **+Mod/probprobabilitative** imperfective probabilitative


Verb tenses are:

* **+Aor**@CODE@****
* **+Prt**@CODE@****
* **+Prt1**@CODE@****
* **+Prt2**@CODE@****

Verb personal forms are:

Subject

One of the two following

* **+Sg1**@CODE@****
* **+Sg2**@CODE@****
* **+Sg3**@CODE@****
* **+Pl1**@CODE@****
* **+Pl2**@CODE@****
* **+Pl3**@CODE@****

* **+ScSg1**@CODE@****
* **+ScSg2**@CODE@****
* **+ScSg3**@CODE@****
* **+ScDu1**@CODE@****
* **+ScDu2**@CODE@****
* **+ScDu3**@CODE@****
* **+ScPl1**@CODE@****
* **+ScPl2**@CODE@****
* **+ScPl3**@CODE@****

Object
* **+OcSg3**@CODE@****
* **+OcDu3**@CODE@****
* **+OcPl3**@CODE@****

Other verb forms are

* **+InfImprf**@CODE@****
* **+InfPrf**@CODE@****
* **+PrcImprf**@CODE@****
* **+PrcPrf**@CODE@****
* **+PrcNeg**@CODE@****
* **+PrcFut**@CODE@****
* **+GerFin**@CODE@****
* **+Subord**@CODE@****
* **+Aud**@CODE@****
* **+Evas**@CODE@****
* **+Ger**@CODE@****
* **+ConNeg**@CODE@****
* **+ConNegII**@CODE@****
* **+Neg**@CODE@****
* **+ImprtII**@CODE@****
* **+PrsPrc**@CODE@****
* **+Sup**@CODE@****
* **+VGen**@CODE@****
* **+VAbess**@CODE@****


Abbreviated words are classified with:

* **+ABBR**@CODE@****
* +Symbol© = independent symbols in the text stream, like £, €, ©
* **+ACR**@CODE@****


## Symbols that need to be escaped on the lower side (towards twolc):
* **»7»**:  Literal »
* **«7«**:  Literal «
```
  %[%>%]  - Literal >
  %[%<%]  - Literal <
```

Special symbols are classified with:

* **+CLB**@CODE@****
* **+PUNCT**@CODE@****
* **+LEFT**@CODE@****
* **+RIGHT**@CODE@****

The verbs are syntactically split according to transitivity:

* **+TV**@CODE@****
* **+IV**@CODE@****

* **+Auxverb** auxilliary verb



Special multiword units are analysed with:

* **+Multi**@CODE@****

Non-dictionary words can be recognised with:

* **+Guess**@CODE@****

Question and Focus particles:

* **+Qst**@CODE@****
* **+Foc**@CODE@****

* **+Sem/ActActivity** Activity
* **+Sem/AmountAmount** Amount
* **+Sem/AniAnimate** Animate
* **+Sem/AniprodProduct** Animal Product
* **+Sem/BodyBodypart** Bodypart
* **+Sem/Body-abstrjierbmi** siellu, vuoig?a, jierbmi
* **+Sem/BuildBuilding** Building
* **+Sem/Build-partcloset** Part of Bulding, like the closet
* **+Sem/CatCategory** Category
* **+Sem/ClthClothes** Clothes
* **+Sem/Clth-jewlJewelery** Jewelery
* **+Sem/Clth-partsávdnji...** part of clothes, boallu, sávdnji...
* **+Sem/CtainContainer** Container
* **+Sem/Ctain-abstraccount** Abstract container like bank account
* **+Sem/Ctain-clth**@CODE@****
* **+Sem/CurrMoney** Currency like dollár, Not Money
* **+Sem/DanceDance** Dance
* **+Sem/DirGPS-kursa** Direction like GPS-kursa
* **+Sem/Domainactions)** Domain like politics, reindeerherding (a system of actions)
* **+Sem/DrinkDrink** Drink
* **+Sem/DummytagDummytag** Dummytag
* **+Sem/Eduevent** Educational event
* **+Sem/EventEvent** Event
* **+Sem/FeatÁrvu** Feature, like Árvu
* **+Sem/Feat-physfárda** Physiological feature, ivdni, fárda
* **+Sem/Feat-psychfeauture** Psychological feauture
* **+Sem/Feat-measrfeauture** Psychological feauture
* **+Sem/Femname** Female name
* **+Sem/FoodFood** Food
* **+Sem/Food-medMedicine** Medicine
* **+Sem/FurnFurniture** Furniture
* **+Sem/GameGame** Game
* **+Sem/Geomobject** Geometrical object
* **+Sem/GroupGroup** Animal or Human Group
* **+Sem/HumHuman** Human
* **+Sem/Hum-abstrabstract** Human abstract
* **+Sem/IdeolIdeology** Ideology
* **+Sem/LangLanguage** Language
* **+Sem/Malname** Male name
* **+Sem/Matthings** Material for producing things
* **+Sem/MeasrMeasure** Measure
* **+Sem/MoneyCurr(ency)** Has to do with money, like wages, not Curr(ency)
* **+Sem/ObjObject** Object
* **+Sem/Obj-cloCloth** Cloth
* **+Sem/Obj-cognCloth** Cloth
* **+Sem/Obj-elapparatus** (Electrical) machine or apparatus
* **+Sem/Obj-lingit** Object with something written on it
* **+Sem/Obj-ropeobject** flexible ropelike object
* **+Sem/Obj-surfcobject** Surface object
* **+Sem/OrgOrganisation** Organisation
* **+Sem/Partbealli** Feature, oassi, bealli
* **+Sem/Perc-cognperception** Cognative perception
* **+Sem/Perc-emoperception** Emotional perception
* **+Sem/Perc-physperception** Physical perception
* **+Sem/Perc-psychperception** Physical perception
* **+Sem/PlantPlant** Plant
* **+Sem/Plant-partpart** Plant part
* **+Sem/PlcPlace** Place
* **+Sem/Plc-abstrplace** Abstract place
* **+Sem/Plc-elevatePlace** Place
* **+Sem/Plc-linePlace** Place
* **+Sem/Plc-waterPlace** Place
* **+Sem/Posjob)** Position (as in social position job)
* **+Sem/ProcessProcess** Process
* **+Sem/ProdProduct** Product
* **+Sem/Prod-audioproduct** Audio product
* **+Sem/Prod-cognproduct** Cognition product
* **+Sem/Prod-lingproduct** Linguistic product
* **+Sem/Prod-visproduct** Visual product
* **+Sem/RelRelation** Relation
* **+Sem/RouteRoute** Name of a Route
* **+Sem/Ruleconvention** Rule or convention
* **+Sem/Semconconcept** Semantic concept
* **+Sem/Sign** Sign (e.g. numbers, punctuation) 
* **+Sem/SportSport** Sport
* **+Sem/State** 
* **+Sem/State-sickIllness** Illness
* **+Sem/SubstncWater** Substance, like Air and Water
* **+Sem/SurSurname** Surname
* **+Sem/SymbolSymbol** Symbol
* **+Sem/TimeTime** Time
* **+Sem/Toolthings** Prototypical tool for repairing things
* **+Sem/Tool-catchfish)** Tool used for catching (e.g. fish)
* **+Sem/Tool-cleancleaning** Tool used for cleaning
* **+Sem/Tool-itIT** Tool used in IT
* **+Sem/Tool-measrmeasuring** Tool used for measuring
* **+Sem/Tool-musicinstrument** Music instrument
* **+Sem/Tool-writetool** Writing tool
* **+Sem/Txtlávlla...)** Text (girji, lávlla...)
* **+Sem/VehVehicle** Vehicle
* **+Sem/WpnWeapon** Weapon
* **+Sem/Wthrground** The Weather or the state of ground





Semantics are classified with


Derivations are classified under the morphophonetic form of the suffix, the
source and target part-of-speech.

* **+V→N**@CODE@****
* **+V→V**@CODE@****
* **+V→A**@CODE@****
* **+Der/xxx**@CODE@****
* **+Der/MWNhead** modifier without noun head
* **+Der/Prmodalities** this is used with predication of nominals and deverbal modalities
* _+Der/CopDer/Pr_ This will replace the nominal conjugation Der/Pr


## Morphophonology

To represent phonologic variations in word forms we use the following
symbols in the lexicon files:
* **%{ая%}Pros** in Pros
* **%{оё%}+N+Sg+Nom+PxPl3** in +N+Sg+Nom+PxPl3
* **%{рл%}+N+Sg+Nom+PxSg2** +N+Sg+Nom+PxSg2
* **%{аяуюØ%}ханав** хан+N+Sg+Acc+PxSg1: ханув, ханав
* **%{увм%}+N+Sg+Pros** +N+Sg+Pros
* **%{вм%}+N+Sg+Nom+PxSg1** +N+Sg+Nom+PxSg1

And the following triggers to control variation:
* **{front}**@CODE@****
* **{back}**@CODE@****
* **%^SCSG2+V+Ind+Aor+ScSg2:%>н°%^SCSG2** this allows n2d +V+Ind+Aor+ScSg2:%>н°%^SCSG2
* **%^PLNOM+N+Pl+Nom+PxDu1+Der/Cop+Ind+Aor+ScPl3** disallows i2e +N+Pl+Nom+PxDu1+Der/Cop+Ind+Aor+ScPl3
* **%^PalVariationтар%{дˮØ%}%>д%{оё%}нзь** This allows for тар%{дˮØ%}%>д%{оё%}нзь

Protoletters for xfst:
* **%{ауоэØ%}schwa**  А1:а А1:у А1:о А1:э schwa
* **%{ауоэиыØ%}pros** before pros

This is the schwa or reduced vowel occurring after x in case endings

* **А2а** Alternating between zero and а

These are proto-glottals
* **%{дˮØ%}**@CODE@****
* **С1**@CODE@****
* **%{нңʼØ%}**@CODE@****
* **%{йнңъʼØ%}proto-glottals** = These are proto-glottals

* **Г1**@CODE@****
* **В1**@CODE@****
* **Е1**@CODE@****
* **Е2**@CODE@****
* **Ы1**@CODE@****
* **Д1**@CODE@****
* **Ы2rules** = These are for developing underlying morphology rules

## Triggers

* **%^A2Oa:o** Initially this is used for the noun "я" to enable a:o
* **%^A2Iпя** for я:и in пя
* **%^MLenitionм:б** м:в м:б
* **%^VowLowerу:о** vowel lowering ы:э у:о
* **%^VowRaiseо:у** э:ы о:у
* **%^VowLossform** stem-final vowel is lost in plural accusative form
* **%^StemVowFrontingхасава:хасев** хасава:хасев
* **%^VowFrontingхадась:хадэйнинзь** хадась:хадэйнинзь
* **%^PalLossloss** in combination with stem-final vowel loss
* **%^HardFrontingяля:ялэ** яля:ялэ

We have manually optimised the structure of our lexicon using the following
flag diacritics to restrict morhpological combinatorics:

* **@P.NeedNoun.ON@**@CODE@****
* **@D.NeedNoun.ON@**@CODE@****
* **@C.NeedNoun@**@CODE@****

Object conjugation

* **@P.CONJ.ObjAll@**@CODE@****
* **@R.CONJ.ObjAll@**@CODE@****
* **@C.CONJ@**@CODE@****


# The Root lexicon


The word forms in Nenets start from the lexeme roots of basic
word classes, or optionally from prefixes:

* **adjectives ;**@CODE@****
* **adpositions ;**@CODE@****
* **adverbs ;**@CODE@****
* **interjections ;**@CODE@****
* **nouns ;**@CODE@****
* **particles ;**@CODE@****
* **pronouns ;**@CODE@****
* **propernouns ;**@CODE@****
* **quantifiers ;**@CODE@****
* **verbs ;**@CODE@****


* **V_NEWWORDS ;verbs.** This is for feeding new verbs.
* **Punctuation ;**@CODE@****
* **Symbols ;**@CODE@****

* **CONJUNCTION ;**@CODE@****
* **SUBJUNCTION ;**@CODE@****
* **INTERJECTION ;**@CODE@****
* **POSTPOSITION ;**@CODE@****















* * *
<small>This (part of) documentation was generated from [../src/fst/root.lexc](http://github.com/giellalt/lang-yrk/blob/main/../src/fst/root.lexc)</small># Interjections
Nenets interjections...



**LEXICON æLEXNAME@ just goes to #




* * *
<small>This (part of) documentation was generated from [../src/fst/affixes/interjections.lexc](http://github.com/giellalt/lang-yrk/blob/main/../src/fst/affixes/interjections.lexc)</small>
# Symbol affixes

**LEXICON æLEXNAME@ 

**LEXICON æLEXNAME@ 

**LEXICON æLEXNAME@ 

**LEXICON æLEXNAME@ 

**LEXICON æLEXNAME@ 
* * *
<small>This (part of) documentation was generated from [../src/fst/affixes/symbols.lexc](http://github.com/giellalt/lang-yrk/blob/main/../src/fst/affixes/symbols.lexc)</small># Clitics inflection
Nenets clitics...



**LEXICON æLEXNAME@ optional +Qst 

**LEXICON æLEXNAME@ leads to #.


* * *
<small>This (part of) documentation was generated from [../src/fst/affixes/clitics.lexc](http://github.com/giellalt/lang-yrk/blob/main/../src/fst/affixes/clitics.lexc)</small># Descriptives
Nenets descriptives...



**LEXICON æLEXNAME@ adds the tag **+Descr**




* * *
<small>This (part of) documentation was generated from [../src/fst/affixes/descriptives.lexc](http://github.com/giellalt/lang-yrk/blob/main/../src/fst/affixes/descriptives.lexc)</small># Quantifier inflection
Nenets quantifiers ...

* **LEXICON NUM_МЯДО**@CODE@****

* **LEXICON NUM_ВАР**@CODE@****

* **LEXICON NUM_ҢУДИ**@CODE@****

* **LEXICON NUM_ҢОДИ**@CODE@****

* **LEXICON NUM_ТАРЕ**@CODE@****

 LEXICON NUM_ЕД  ед: 13 

* **LEXICON NUM_ЕД/ТИРЕ**@CODE@****

* **LEXICON NUM_ЕД/ХАНО**@CODE@****

* **LEXICON NUM_ҢОДИ/ТЁН**@CODE@****

* **LEXICON NUM_ТИРЕ/ХАНО**@CODE@****

* **LEXICON NUM_ХУСУВЭЙ**@CODE@****

* **LEXICON QNT_ХУСУВЭЙ**@CODE@****

we need to get away from these: NUM_VOW and NUM_CONS
it's done


* * *
<small>This (part of) documentation was generated from [../src/fst/affixes/quantifiers.lexc](http://github.com/giellalt/lang-yrk/blob/main/../src/fst/affixes/quantifiers.lexc)</small># Noun inflection

Nenets nouns inflect in cases.


**LEXICON æLEXNAME@ 
* **LEXICON N_ҢЭ-вна** ңэ:ңэ 1  ProsSg -вна
Yaml: **xo, ngaeTS**
**LEXICON æLEXNAME@ 

* **LEXICON N_ҢЭ-Pal/Var-вна** ңэ:ңэ 1  ProsSg -вна
Yaml: **nyeTS**

* **LEXICON N_Ё-вна** я:я 2 ProsSg -вна
Yaml: **ya, yaTS**



* **LEXICON N_ПИ-вна** пя:пя 3 ProsSg -вна
Yaml: **N-pyaTS**

* **LEXICON N_ТЫ-вна** ты: 4 ProsSg -вна
Yaml: **tyTS**




* **LEXICON N_ХАВО-вна** ха: 5 ProsSg -вна
Yaml: **tyTS**



* **LEXICON N_СЁЁ-вна** сё: 6 ProsSg -вна


* **LEXICON N_ИБЕ-вна** и: 7 ProsSg -вна

* **LEXICON N_ХАБИЕ-вна** хӑби:8ProsSg -вна

* **LEXICON N_ПАНЫ-(э)вна** пӑны:пӑн 9 ы!ProsSg -(э)вна


* **LEXICON N_ХУСУВЭЙ-ювна** хусувэй: 10 ProsSg -ювна


* **LEXICON N_ХАНО-увна** хӑн: 11P ProsSg -увна
Yaml: **xano**



* **LEXICON N_ТИРЕ-увна** тир: 12 ProsSg -увна

* **LEXICON N_ЕД/-ювна** ед: 13 ProsSg -увна /-ювна

* **LEXICON N_МАРАҢГЫ-вна** мӑраңга: 14PProsSg -вна




* **LEXICON N_ҢУДИ-вна** ңуда: 15 ProsSg -вна
Yaml: **N-ngudiTS**

* **LEXICON N_ЕСИ-вна** ая̆ха: 16PProsSg -вна
Yaml: **N-yaxaTS**


* **LEXICON N_ҢОДИ-вна** ңодя: 17 ProsSg -вна
Yaml: **N-ngodiTS**


* **LEXICON N_ЯЛЭ-вна** яля: 18 ProsSg -вна

* **LEXICON N_ХОБ-вна** хоба:хоба 19 ProsSg -вна
Yaml: **xob**

* **LEXICON N_ТЁН-вна** тёня:тёня 20 ProsSg -вна
Yaml: **tyon**

* **LEXICON N_ПИСЬ-вна** пися: 21 ProsSg -вна

* **LEXICON N_ХАСЕВ-вна** хасава: 22 ProsSg -вна

* **LEXICON N_ҢАНУ-вна** ңӑно: 23 ProsSg -вна
Yaml: **nano**

* **LEXICON N_ЯКЫ-вна** якэ: 24 ProsSg -вна


* **LEXICON N_ҢУВО-(м)на** ңумʼ:ңум 25 ProsSg -(м)на
Yaml: **yam, ngumhTS**

* **LEXICON N_НЮБЕ-(м)на** нюмʼ: 26  ProsSg -(м)на

* **LEXICON N_МУНО-мна** муʼ:му 27  ProsSg -мна

* **LEXICON N_ПОЁ-мна** поʼ:по 28  ProsSg -мна
Yaml: **poyo**

* **LEXICON N_ВЫҢО/-мана** выʼ:вы 29  ProsSg -мна /-мана


* **LEXICON N_ИЛЪЕ-мана** илʼ:ил 30   ProsSg -мана
Yaml: **ilje**
| --- 





* **LEXICON N_НЕНЭЦИЕ-мана** ненэцьʼ:ненэць 30   ProsSg -мана
Yaml: **nyenecyh**
| --- 

* **LEXICON N_ПАХАЁ-мна** пӑхӑʼ: 31   ProsSg -мна
| --- 

* **LEXICON N_СЕРО-мня** серˮ: 32   ProsSg -мана / -мня

* **LEXICON N_ТАРЕ-мня** тӑрˮ:тар 33   ProsSg -мня
| --- 

* **LEXICON N_МАНСО-мна** мӑнˮ: 34   ProsSg -мна


* **LEXICON N_МЯДО-мна** мяˮ:мя 35   ProsSg -мна
Yaml: **myadoTS**
| --- 


* **LEXICON N_ИДЕ-мна** иˮ: 36   ProsSg -мна
Yaml: **yidye**









* **LEXICON N_ҢЭ/ХАБИЕ-вна** ңэ:ңэ 1  ProsSg -вна
хӑби:8 ProsSg -вна


та:та 






* **LEXICON NMN_ҢУДИ-вна** ңуда: 15 ProsSg -вна
Yaml: **ngudi**
* **POSSESSA-PLURAL ;+Pl+Abl** +Pl+Dat, +Pl+Loc, +Pl+Abl

* **LEXICON NMN_ҢОДИ**@CODE@****
* **POSSESSA-PLURAL ;+Pl+Abl** +Pl+Dat, +Pl+Loc, +Pl+Abl



* **LEXICON NMN_ХОБ-вна** хоба:хоба 19 ProsSg -вна
Yaml: **xob**
* **POSSESSA-PLURAL ;+Pl+Abl** +Pl+Dat, +Pl+Loc, +Pl+Abl








* **LEXICON NMN_ПИСЬ-вна** пися: 21 ProsSg -вна
* **POSSESSA-PLURAL ;+Pl+Abl** +Pl+Dat, +Pl+Loc, +Pl+Abl


* **LEXICON NMN_ҢАНУ-вна** ңӑно: 23 ProsSg -вна
* **POSSESSA-PLURAL ;+Pl+Abl** +Pl+Dat, +Pl+Loc, +Pl+Abl

* **LEXICON NMN_ҢУВО** ңумʼ:ңум 25 
* **:ʼ POSSESSA-PLURAL ;+Pl+Abl** +Pl+Dat, +Pl+Loc, +Pl+Abl




* **LEXICON NMN_НЮБЕ26** нюмʼ: 26



* **LEXICON NMN_МУНО-мна** муʼ: 27  ProsSg -мна


No n2d







* **:%{йнңъʼØ%} SGNOMSUF ;** 
* **:%{йнңъʼØ%} SG-NOM-STEM ;** 
* **:%{йнңъʼØ%} POSSESSA-PLURAL ;+Pl+Abl** +Pl+Dat, +Pl+Loc, +Pl+Abl

Where is the variation?

* **LEXICON NMN_ТАРЕ-мня** тӑрˮ:тар 33   ProsSg -мня





* **LEXICON N_ВАР/ТАРЕ-мна** мяˮ:мя 35   ProsSg -мна

* **LEXICON NMN_ВАР-мна** мяˮ:мя 35   ProsSg -мна
Yaml: **waro**
* **:%{дˮØ%} POSSESSA-PLURAL ;+Pl+Abl** +Pl+Dat, +Pl+Loc, +Pl+Abl

* **LEXICON NMN_МЯДО-мна** мяˮ:мя 35   ProsSg -мна
Yaml: **myado**
* **:%{дˮØ%} SGLOCSUF_Хна ;мякна** мякна
* **:%{дˮØ%} POSSESSA-PLURAL ;+Pl+Abl** +Pl+Dat, +Pl+Loc, +Pl+Abl

Where is the variation?

Where is the variation?
* **:%{дˮØ%} POSSESSA-PLURAL ;+Pl+Abl** +Pl+Dat, +Pl+Loc, +Pl+Abl


* **LEXICON N_ТЮСЕ** тюˮ:тюсе 







* **LEXICON N_САВНЕ** 




* **LEXICON N_ПЕНЗЕРЕпензерˮ:пензер** пензерˮ:пензер

* **LEXICON N_САБЦЬсабць:сабць** сабць:сабць

* **LEXICON N_МЕРЁмерё:мерё** мерё:мерё


NMN


* **LEXICON NMN_ҢЭ-OLD-вна** ңэ:ңэ 1  ProsSg -вна
* **SG-ACC-STEM ;SGGENSUF** SGACCSUF, SGGENSUF
* **SG-NOM-STEM ;NOMINAL-CONJUGATION** SG/DAT,LOC, ABL,TRA,PRO; DU/NOM,ACC,GEN; PL/DAT,LOC,ABL,TRA; PX-s, NOMINAL-CONJUGATION
* **PLNOMSUF ;** 
* **PLACCSUF_Zero ;PL-ACC_STEM** => PL-ACC_STEM
* **POSSESSA-PLURAL ;+Pl+Abl** +Pl+Dat, +Pl+Loc, +Pl+Abl



* **POSSESSA-PLURAL ;+Pl+Abl** +Pl+Dat, +Pl+Loc, +Pl+Abl


9
* **:%^VowLower POSSESSA-PLURAL ;+Pl+Abl** +Pl+Dat, +Pl+Loc, +Pl+Abl

* **LEXICON NMN_ХУСУВЭЙ-ювна** хусувэй: 10 ProsSg -ювна
* **POSSESSA-PLURAL ;+Pl+Abl** +Pl+Dat, +Pl+Loc, +Pl+Abl



 * LEXICON NMN_ХАНО-OLD  11 хан:хан



* **LEXICON NMN_ТИРЕ-увна** тир: 12 ProsSg -увна
* **POSSESSA-PLURAL ;+Pl+Abl** +Pl+Dat, +Pl+Loc, +Pl+Abl

* **LEXICON NMN_ЕД/-ювна** ед: 13 ProsSg -увна /-ювна
Yaml: **yed**
* **POSSESSA-PLURAL ;+Pl+Abl** +Pl+Dat, +Pl+Loc, +Pl+Abl

## NOMINALS "NMN"
### THREE-SYLLABLE VOWEL-FINAL STEMS

* **POSSESSA-PLURAL ;+Pl+Abl** +Pl+Dat, +Pl+Loc, +Pl+Abl


























таˮ:та








варˮ:вар
Yaml: **N-tarTS**
| --- 

















The singular accusative stem









* **LEXICON SGLOCSUF_Хнамякна** мякна

* **LEXICON SGLOCSUF_Ханасеркана** серкана







Start Plural










What is assumed on the basis of the plural accusative
* **+Pl+Pros:%>ˮ%{увм%}А2на K ;хоˮомна** When does this take a vowel хоˮомна
















Possessor Indices




* **+Sg+Nom+PxSg1+Der/Cop+Ind+Aor+ScSg3:%>в K ;marking** 2013-10-22 Should this also have +ScSg3 marking



 * **LEXICON AFTER-OBLIQUE-SG-POSSESSA-COME-POSSESSOR-INDICES ** singular possessa in +Gen, +Dat, +Loc, +Abl share the same possessor indices

 * **LEXICON DV-OBLIQUE-SG-POSSESSA-TAKE-POSSESSOR-INDICES_TO-BE-FOLLOWED-BY-SG3-PRED-AOR/PRT1 ** singular possessa oblique possessor indices


SINUGLAR CASES







The next line in +Sg+Pros+PxDu2:%>%{увм%}А2нандиʼ must be removed



Dual possessa








Dual possessa









Plural Possessa






























 * **+PxPl1:наˮ K ; ** The morpheme boundary has been removed to indicate a distinct difference in phonological behavior.

















Conjugation of nouns and adjectives



## NEW




























































>>NEW-SG-LOC_Кна/Кана

























* * *
<small>This (part of) documentation was generated from [../src/fst/affixes/nouns.lexc](http://github.com/giellalt/lang-yrk/blob/main/../src/fst/affixes/nouns.lexc)</small>Adjective inflection
Nenets  adjectives.

**LEXICON æLEXNAME@ to #


* **LEXICON A_ҢЭ** ңэ:ңэ 1  

* **LEXICON A_ПАНЫ** пӑны:пӑны 9 

* **LEXICON A_ХУСУВЭЙ-ювна** хусувэй: 10 !!ProsSg -ювна


* **LEXICON A_ХАНО-увна** хӑн: 11 !!ProsSg -увна
[total=27]
хӑн xən°    хӑнӑн’ xənən°h        хӑнˮ xən°q     хӑно xəno


* **LEXICON A_ЕД/-ювна** ед: 13 !!ProsSg -увна /-ювна

* **LEXICON A_ҢУДИ-вна** ңуда: 15 !!ProsSg -вна


* **LEXICON A_ҢОДИ-вна** ңодя: 17 !!ProsSg -вна



* **LEXICON A_ХОБ-вна** хоба: 19 !!ProsSg -вна


* **LEXICON A_ТЁН-вна** тёня: 20 !!ProsSg -вна

* **LEXICON A_ПИСЬ-вна** пися: 21 !!ProsSg -вна

* **LEXICON A_ҢАНУ-вна** ңӑно: 23 !!ProsSg -вна
[total=57]
ңӑно ŋəno   ңӑнон’ ŋənon°h ңӑноˮ ŋənoq    ңӑну ŋənu

* **LEXICON A_ЯКЫ-вна** якэ: 24 ProsSg -вна

* **LEXICON A_ҢУВО-(м)на** ңумʼ:ңум 25 !!ProsSg -(м)на
ңум’ ŋum     ңумд’ ŋumt°h    ңувˮ ŋuw°q      ңуво ŋuwo


* **LEXICON A_НЮБЕ-Pal/Var26** нюмʼ:нюм 26
нюм’ nyum    нюмд’ nyumt°h   нювˮ nyuw°q     нюбе nyubye

* **LEXICON A_ВЫҢО** выʼ:вы 29  


Check this


* **LEXICON A_МЯДО-мна** мяˮ:мя 35   !!ProsSg -мна

LEXICON A_САБЦЬ-увна тир: 12 !!ProsSg -увна
What makes this different from N_ТИРЕ?

* **LEXICON A_САВНЕ** 







* * *
<small>This (part of) documentation was generated from [../src/fst/affixes/adjectives.lexc](http://github.com/giellalt/lang-yrk/blob/main/../src/fst/affixes/adjectives.lexc)</small># Pronoun inflection
Nenets pronouns inflection

**LEXICON æLEXNAME@ for the unclassified ones

**LEXICON æLEXNAME@ 

**LEXICON æLEXNAME@ etc.

**LEXICON æLEXNAME@ 

**LEXICON æLEXNAME@ 

**LEXICON æLEXNAME@ 

**LEXICON æLEXNAME@ 

**LEXICON æLEXNAME@ 

**LEXICON æLEXNAME@ 

**LEXICON æLEXNAME@ 

**LEXICON æLEXNAME@ 

**LEXICON æLEXNAME@ 

**LEXICON æLEXNAME@ 

**LEXICON æLEXNAME@ etc. 

**LEXICON æLEXNAME@ 

**LEXICON æLEXNAME@ 

**LEXICON æLEXNAME@  etc.

**LEXICON æLEXNAME@ 

**LEXICON æLEXNAME@ 

**LEXICON æLEXNAME@ 

**LEXICON æLEXNAME@ 

**LEXICON æLEXNAME@ 
 +Interr+Sem/Hum:  POSSESSA-PLURAL ;  +Pl+Dat, +Pl+Loc, +Pl+Abl

**LEXICON æLEXNAME@ 

**LEXICON æLEXNAME@ 

**LEXICON æLEXNAME@ 

**LEXICON æLEXNAME@ 

**LEXICON æLEXNAME@ 

**LEXICON æLEXNAME@ 

**LEXICON æLEXNAME@ 

**LEXICON æLEXNAME@ 

**LEXICON æLEXNAME@ 

**LEXICON æLEXNAME@ 

**LEXICON æLEXNAME@ 

**LEXICON æLEXNAME@ 

**LEXICON æLEXNAME@ 

**LEXICON æLEXNAME@ 

**LEXICON æLEXNAME@ 

**LEXICON æLEXNAME@ 


* * *
<small>This (part of) documentation was generated from [../src/fst/affixes/pronouns.lexc](http://github.com/giellalt/lang-yrk/blob/main/../src/fst/affixes/pronouns.lexc)</small># Nenets Verb inflection

**LEXICON V_** for unassigned verbs

## ONE-SYLLABLE STEMS WITH STEM-FINAL VOWEL
* **LEXICON IV_Еесь:е** есь:е

**LEXICON IV_МЭ** 

**LEXICON TV_МЭ** 

**LEXICON VR_МЭ** 

**LEXICON IV_МЫ** 

**LEXICON TV_МЫ** 

**LEXICON VA_НЁ** 

**LEXICON VA_НИ** 

**LEXICON IV_НИ** 

**LEXICON IV_НО** 

**LEXICON IV_НУ** 

**LEXICON IV_НУ-Pal/Var** 

**LEXICON VR_НУ** 

**LEXICON VR_НУ-Pal/Var** 

**LEXICON TV_НУ** 

**LEXICON TV_НУ-Pal/Var** 

**LEXICON IV_НУ/ТУ** 

* **LEXICON IV_ҢЭңэсь:ңэ** ңэсь:ңэ
**LEXICON IV_ҢЭ** 

**LEXICON IV_ҢЭ-Pal/Var** 


**LEXICON IV_ТУ** 

**LEXICON TV_ТУ** 

**LEXICON IV_ХО** 


**LEXICON TV_ХО** 

**LEXICON VR_ХО-Pal/Var** 

**LEXICON IV_ХЭ** 

## TWO-SYLLABLE STEMS WITH STEM-FINAL VOWEL

* **LEXICON IV_НАМДАнамдась:намда** намдась:намда
**LEXICON IV_НАМДА** 

**LEXICON TV_НАМДА** 

**LEXICON VR_НАМДА** 

**LEXICON IV_ВАДЮ** 

**LEXICON TV_ВАДЮ** 

* **LEXICON IV_ЯКУякась:яка** якась:яка

**LEXICON IV_ИЛЕ** 

**LEXICON IV_ИЛЕ-Pal/Var** Work needed for variation 2013-03-04

**LEXICON VR_ИЛЕ** 

**LEXICON VR_ИЛЕ-Pal/Var**  Work needed for variation 2013-09-05

**LEXICON TV_ИЛЕ** 

**LEXICON IV_НЕНЫ** 

**LEXICON IV_ҢЭСУ** 

**LEXICON TV_ҢЭСУ** 

**LEXICON IV_ПЭБЮ** 

**LEXICON IV_ПЭБЮ-Pal/Var** 

**LEXICON TV_ПЭБЮ** 


**LEXICON IV_ХАДАБАСЬ** 


**LEXICON TV_ХАДАБАСЬ** 


* **LEXICON IV_ХАДАхадась:хада** хадась:хада

* **LEXICON TV_ХАДАхадась:хада** хадась:хада

**LEXICON VR_ХАДА** 

**LEXICON IV_ЮХУ** 

**LEXICON TV_ЮХУ** 


### THREE-SYLLABLE STEMS WITH STEM-FINAL VOWEL
**LEXICON IV_ЛАХАНА** 

**LEXICON IV_ЛАХАНА-Pal/Var** 

**LEXICON VR_ЛАХАНА** 

**LEXICON TV_ЛАХАНА** 
 * **@P.CONJ.ObjAll@+TV:@P.CONJ.ObjAll@ V-NEW_ЛАХАНА       ; ** 3-syll

**LEXICON TV_ЛАХАНА-Pal/Var** 

**LEXICON IV_ҢЭДАРА** 
**LEXICON TV_ҢЭДАРА** 
**LEXICON VR_ҢЭДАРА** 

**LEXICON IV_СЯНАКУ** 

**LEXICON IV_ЯˮАВЛУ** 
* Yaml: **V-yaqwlasj**

**LEXICON IV_ЯˮАВЛУ-Pal/Var** 


**LEXICON TV_ЯˮАВЛУ** 

### ONE-SYLLABLE STEMS WITH STEM-FINAL CONSONANT
* **LEXICON IV_МАН** манзь:ма%{нңʼØ%} 
* Yaml: **manzj**

**LEXICON IV_МИН** 

**LEXICON IV_МИН-Pal/Var** 

**LEXICON TV_МИН** 

**LEXICON VR_МИН** 

**LEXICON IV_САС** 


 * LEXICON TV_САС  манэць:манэ







### TWO-SYLLABLE STEMS WITH STEM-FINAL CONSONANT
* **LEXICON IV_НЭКАЛ** 


* **LEXICON IV_ҢАДИМ/ҢАРАМ2013-12-16** 2013-12-16









## AFTER +TV, +IV, +Aux, +Refl
Not yet written.

## CONJUGATION BY STEM TYPE

### ONE-SYLLABLE STEMS WITH STEM-FINAL VOWEL

 *  PRC-NEG ; 	+PrcNeg +PrcFut

 *  PRC-NEG ; 	+PrcNeg +PrcFut
 * :%^VowRaise PRC-NEG ; 	+PrcNeg +PrcFut

V_refl 


 *  PRC-NEG ; 	+PrcNeg +PrcFut
 * :%^VowRaise PRC-NEG ; 	+PrcNeg +PrcFut

 *  PRC-NEG ; 	+PrcNeg +PrcFut

 *  PRC-NEG ; 	+PrcNeg +PrcFut

 *  PRC-NEG ; 	+PrcNeg +PrcFut

 *  PRC-NEG ; 	+PrcNeg +PrcFut

V_refl 2013-03-04


 *  PRC-NEG ; 	+PrcNeg +PrcFut

 *  PRC-NEG ; 	+PrcNeg +PrcFut

 *  PRC-NEG ; 	+PrcNeg +PrcFut

* Yaml: **V-xosj**
 *  PRC-NEG ; 	+PrcNeg +PrcFut

 *  PRC-NEG ; 	+PrcNeg +PrcFut


### TWO-SYLLABLE STEMS WITH STEM-FINAL VOWEL
 *  PRC-NEG ; 	+PrcNeg +PrcFut
 * :%^VowRaise PRC-NEG ; 	+PrcNeg +PrcFut


* **LEXICON V-01_ЯКУякась:яка** якась:яка
 *  PRC-NEG ; 	+PrcNeg +PrcFut


 * LEXICON V-01_НЕНЫ  2013-09-18 This is merely a copy of V-01_МЫ
 *  PRC-NEG ; 	+PrcNeg +PrcFut
 * :%^VowRaise PRC-NEG ; 	+PrcNeg +PrcFut

 * ** V_Fut_ҢГУ ; ** is this the stem to use for +Fut+Mod/prob
 *  PRC-NEG ; 	+PrcNeg +PrcFut

V_refl 2013-03-04
 *  PRC-NEG ; 	+PrcNeg +PrcFut

 *  PRC-NEG ; 	+PrcNeg +PrcFut
 * :%^VowRaise PRC-NEG ; 	+PrcNeg +PrcFut

* Yaml: **V-pewasj**
has vowel loss






* *яˮавла%^VowRaise%>ˮ*
* *яˮавлу0%>ˮ*
* *тенева%^VowLoss%>ˮ*
* *тенев00%>ˮ*



* Yaml: **V-xadabasj**
* *яˮавла%^VowRaise%>ˮ*
* *яˮавлу0%>ˮ*
* *тенева%^VowLoss%>ˮ*
* *тенев00%>ˮ*


 *  PRC-NEG ; 	+PrcNeg +PrcFut

V_refl 
 *  PRC-NEG ; 	+PrcNeg +PrcFut
 *  PRC-NEG ; 	+PrcNeg +PrcFut

 *  PRC-NEG ; 	+PrcNeg +PrcFut
 * :%^VowRaise PRC-NEG ; 	+PrcNeg +PrcFut

### THREE-SYLLABLE STEMS WITH STEM-FINAL VOWEL
а > э in Pl Oc 
 *  PRC-NEG ; 	+PrcNeg +PrcFut

V_refl 2013-03-04  а > ы (ъя before х)
 *  PRC-NEG ; 	+PrcNeg +PrcFut

 *  PRC-NEG ; 	+PrcNeg +PrcFut
 * :%^VowRaise PRC-NEG ; 	+PrcNeg +PrcFut

 * **LEXICON V-01_ЯˮАВЛУ ** яˮавлась:яˮавла
 *  PRC-NEG ; 	+PrcNeg +PrcFut
 * :%^VowRaise PRC-NEG ; 	+PrcNeg +PrcFut


### ONE-SYLLABLE STEMS WITH STEM-FINAL CONSONANT
* **LEXICON V-01_МАН** манзь:ма%{нңʼØ%} 
* Yaml: **manzj**
 *  PRC-NEG ; 	+PrcNeg +PrcFut

 *  PRC-NEG ; 	+PrcNeg +PrcFut



 *  PRC-NEG ; 	+PrcNeg +PrcFut

 * LEXICON V-01_САС  манэць:манэ

 * :С1 PRC-NEG_МАДАВЭЙ ; 	+PrcNeg +PrcFut


* **LEXICON V-NEW_ТИР**@CODE@****







V_refl 2013-03-04

 *  PRC-NEG ; 	+PrcNeg +PrcFut


### TWO-SYLLABLE STEMS WITH STEM-FINAL CONSONANT
* **LEXICON V-01_НЭКАЛнэкалць:нэкал** нэкалць:нэкал

 *  PRC-NEG ; 	+PrcNeg +PrcFut

 *  PRC-NEG ; 	+PrcNeg +PrcFut



V_refl 2013-03-04

Mutual verbal conjugation
* **LEXICON IND-AORDu3** All except Sg3 Du3




































Preterite 1 # This should be for ConjPrt and NarrPrt also.














 * +Ind:%>я IND-AOR-RCSG1	;  This should be schwa or something

Other moods
сь in 2nd, 4th etc non-final syllable 









 * **LEXICON V_PREC ** Hort

































 * **+Mod/des:%>рава MUTUAL-PERSON-NON-OCPL_NORAISING ; ** Sg3 and Pl3








































 * **LEXICON SG3-PRED-AOR/PRET1 ** V_AUD picks up possessor indices and comes here

Mutual person ending for nonindicative moods


















This need separating 2013-04-23























Object


Reflexive


Reflexive Preterite

Non-finites




* **+PrcFut:%>%{вм%}анда K ;**@CODE@****

* **+PrcFut:%>%{вм%}нда K ;2013-11-25** Should this form be here 2013-11-25


* **+PrcFut:%>%{вм%}нда K ;2013-11-25** Should this form be here 2013-11-25





no vowel loss in stem



* *яˮавла%^VowRaise%>ˮ*
* *яˮавлу0%>ˮ*
* *тенева%^VowLoss%>ˮ*
* *тенев00%>ˮ*



 * **LEXICON V-NEW_НАМДА ** намдась:намда schwa-final


* *яˮавла%^VowRaise%>ˮ*
* *яˮавлу0%>ˮ*
* *тенева%^VowLoss%>ˮ*
* *тенев00%>ˮ*





* *яˮавла%^VowRaise%>ˮ*
* *яˮавлу0%>ˮ*



* Yaml: **V-xosjTS**
 * **+Subord+PxSg1:%>бˮни K ; ** Do all odd-syllabled words need this?




◊_subj

◊_obj 





 * **+PrcFut+Pred+Nom+PxSg1:%>вндадав K ; ** Vowel removed
 * **+PrcFut+Pred+Nom+PxSg1:%>вндадув K ; ** Vowel removed
 * **+PrcFut+Pred+Acc+PxSg1:%>вндадав K ; ** Vowel removed
 * **+PrcFut+Pred+Acc+PxSg1:%>вндадув K ; ** Vowel removed

























◊_subj









◊_obj 



◊_obj 














 * **LEXICON V-NEW_BI-SYLL-MUTUAL-RAISE/NO ** raise/no


















































































 * **LEXICON IND-AOR/PRT1-OCPL3_ян ** ODD-SYLL



























 * **LEXICON MOD/INT-SC_бца ** ??
































 * **+PrcFut+Pred+Nom+PxSg1:%>вндадав K ; ** Vowel removed
 * **+PrcFut+Pred+Nom+PxSg1:%>вндадув K ; ** Vowel removed
 * **+PrcFut+Pred+Acc+PxSg1:%>вндадав K ; ** Vowel removed
 * **+PrcFut+Pred+Acc+PxSg1:%>вндадув K ; ** Vowel removed














* * *
<small>This (part of) documentation was generated from [../src/fst/affixes/verbs.lexc](http://github.com/giellalt/lang-yrk/blob/main/../src/fst/affixes/verbs.lexc)</small># Adverbs
Nenets adverbs...



* **LEXICON ADV_tag** to # without tag

* **LEXICON ADV-LOC_+Loc** to # with tag +Loc

* **LEXICON ADV-TEMP_#** adds +Temp and goes to #

* **LEXICON ADV-MANNER_**@CODE@****

* **LEXICON ADV-REF_conjuctions** Some are secodary predicates, conjuctions

* **LEXICON ADV-REF_Д1**@CODE@****




* * *
<small>This (part of) documentation was generated from [../src/fst/affixes/adverbs.lexc](http://github.com/giellalt/lang-yrk/blob/main/../src/fst/affixes/adverbs.lexc)</small>
# Adposition inflection
Nenets adpositions inflect in person (and some in local cases).

**LEXICON æLEXNAME@ 

**LEXICON æLEXNAME@ 

**LEXICON æLEXNAME@ 

**LEXICON æLEXNAME@ 


**LEXICON æLEXNAME@ 

**LEXICON æLEXNAME@ 

**LEXICON æLEXNAME@ 

**LEXICON æLEXNAME@ 



* * *
<small>This (part of) documentation was generated from [../src/fst/affixes/adpositions.lexc](http://github.com/giellalt/lang-yrk/blob/main/../src/fst/affixes/adpositions.lexc)</small># Proper noun inflection
Nenets proper nouns inflect in the same cases as regular
nouns, but with a XXX as separator.

**LEXICON æLEXNAME@ for bunclassified ones

### ONE-SYLLABLE VOWEL-FINAL STEM
**LEXICON æLEXNAME@ 

**LEXICON æLEXNAME@ 

### ONE-SYLLABLE CONSONANT-FINAL STEM
**LEXICON æLEXNAME@ 

### TWO-SYLLABLE CONSONANT-FINAL STEM
* **LEXICON PROP_ПАНЫ9** пӑны:пӑны 9


* **LEXICON PROP_ХАНО-увна** хӑн: 11P ProsSg -увна
Yaml: **xano**

**LEXICON æLEXNAME@ 

**LEXICON æLEXNAME@ 

**LEXICON æLEXNAME@ 

**LEXICON æLEXNAME@ 

* **LEXICON PROP_ЯЛЭ-вна** яля: 18 ProsSg -вна
/total=2/
яля yalya    ялян’ yalyan°h  яляˮ yalyaq     ялэ yale

**LEXICON æLEXNAME@ 

**LEXICON æLEXNAME@ 

**LEXICON æLEXNAME@ 

**LEXICON æLEXNAME@ 

* **LEXICON PROP_ХАСЕВ-вна** хасава: 22 ProsSg -вна
/total=1/
хасава xasawa        хасаван’ xasawan°h      хасаваˮ xasawaq хасев xasyew°
* **+N+Prop: POSSESSA-PLURAL ;+Pl+Abl** +Pl+Dat, +Pl+Loc, +Pl+Abl

**LEXICON æLEXNAME@ 

**LEXICON æLEXNAME@ 

### THREE-SYLLABLE VOWEL-FINAL STEM
**LEXICON æLEXNAME@ 

**LEXICON æLEXNAME@  Here we need some kind of vowel harmony




* * *
<small>This (part of) documentation was generated from [../src/fst/affixes/propernouns.lexc](http://github.com/giellalt/lang-yrk/blob/main/../src/fst/affixes/propernouns.lexc)</small># Nenets twol file

This file documents the [phonology.twolc file](http://github.com/giellalt/lang-yrk/blob/main/src/fst/phonology.twolc) 


## Letters of the alphabet
* **а б в г д е ё ж з и й к л м н ң о п р с т у ф х ц ч ш щ ъ ы ь э ю я** 
* **А Б В Г Д Е Ё Ж З И Й К Л М Н Ң О П Р С Т У Ф Х Ц Ч Ш Щ Ъ Ы Ь Э Ю Я** 

* **°:0vowel** Directly from Tapani Salminen extra short vowel

* **ә:аschwa** Directly from Tapani Salminen schwa



## Archiphonemes for vowels

* %{ауоэØ%}:аSCHWA  А1:а А1:у А1:о А1:э SCHWA
* %{ауоэиыØ%}:0pros before pros

 * А2:а  

 * Ы1:о   
 * Ы1:е  

 * Ы2:э  

## Archiphonemes for glottals

 *  %{нңʼØ%}:ʼ   
 *  %{нңʼØ%}:н   
 *  %{нңʼØ%}:0   
 *  %{йнңъʼØ%}:й   
 *  %{йнңъʼØ%}:н   
 *  %{йнңъʼØ%}:ң   
 *  %{йнңъʼØ%}:ъ   
 *  %{йнңъʼØ%}:ʼ   
 *  %{йнңъʼØ%}:0   
 *  %{дˮØ%}:ˮ   
 *  %{дˮØ%}:д   
 *  %{дˮØ%}:0   
 *  С1:ˮ   
 *  С1:с   
 *  С1:0   

 *  %{ая%}:а          in Pros
 *  %{оё%}:о          in +N+Sg+Nom+PxPl3
 *  %{рл%}:0	    +N+Sg+Nom+PxSg2

* **%{аяуюØ%}:0ханав** хан+N+Sg+Acc+PxSg1: ханув, ханав

* **%{увм%}:0+N+Sg+Pros** +N+Sg+Pros

* **%{вм%}:0+N+Sg+Nom+PxSg1** +N+Sg+Nom+PxSg1

## triggers

 *  %^SCSG2:0     this allows n2d +V+Ind+Aor+ScSg2:%>н°%^SCSG2
 *  %^PLNOM:0     disallows i2e +N+Pl+Nom+PxDu1+Der/Cop+Ind+Aor+ScPl3
 *  %^A2O:0      
 *  %^A2I:0        

* **%^PalVariation:0тар%{дˮØ%}%>д%{оё%}нзь** This allows for тар%{дˮØ%}%>д%{оё%}нзь

 *  %^MLenition:0  lenition
 *  %^VowLower:0  vowel lowering ы:э у:о
 *  %^VowRaise:0  vowel raising э:ы о:у
 *  %^VowLoss:0      stem-final vowel is lost in plural accusative
 *  %^StemVowFronting:0      хасава:хасев
 *  %^VowFronting:0      хадась:хадэйнинзь
 *  %^PalLoss:0      in combination with stem-final vowel loss тёня:тён
 *  %^HardFronting:0      яля:ялэ


## Boundary symbols

 *  %>      
hash




















# Rules




**к: -> г after nasal glottal**
* *му%{нңʼØ%}%>кʼ*
* *муң%>гʼ*

* *ил°%{йнңъʼØ%}%>к°ʼ*
* *илаң%>г0ʼ*



**к: to х after Vowels**

*ты%^VowLower%>да examples:*

*тэ0%>да examples:*

*ед°%>к%{ауоэØ%}на examples:*

*ед0%>хана examples:*

*намда%^VowLoss%>к%{ауоэØ%}в examples:*

*намд00%>хав examples:*

**nTod**

*му%{нңʼØ%}%^SCSG2%>нʼ examples:*

*мун0%>дʼ examples:*

*ңум%{йнңъʼØ%}%^SCSG2%>нʼ examples:*

*ңум00%>дʼ examples:*

*ңум%{йнңъʼØ%}%^SCSG2%>н°ʼ examples:*

*ңум00%>д0ʼ examples:*

**%{нңʼØ%}:н GlottalNasalToSurface**

*му%{нңʼØ%}%>нд examples:*

*мун%>0д examples:*

*му%{нңʼØ%}%>сь examples:*

*мун0%>зь examples:*


*му%{нңʼØ%}%^SCSG2%>нʼ examples:*

*мун0%>дʼ examples:*

**%{нңʼØ%}:ң GlottalNasalToSurface**

*му%{нңʼØ%}%>кʼ examples:*

*муң%>гʼ examples:*

**%{йнңъʼØ%}:ң GlottalNasalToSurface**

*ил°%{йнңъʼØ%}%>к°ʼ examples:*

*илаң%>г0ʼ examples:*

**%{йнңъʼØ%}:н GlottalNasalToSurface**

*ил°%{йнңъʼØ%}%^SCSG2%>н examples:*

*илан0%>д examples:*


*ила%{йнңъʼØ%}%>сиˮ examples:*

*илан%>зиˮ examples:*

*ил°%{йнңъʼØ%}%>н°ʼ examples:*

*илан%>д0ʼ examples:*

*ил°%{йнңъʼØ%}%>дмʼ examples:*

*илан%>дмʼ examples:*

*илан%>дув0 examples:*

*ил0н%>дув0 examples:*


**%{йнңъʼØ%}:ъ GlottalNasalToSurface**

*ил°%{йнңъʼØ%}е examples:*

*ил0ъе examples:*

**%{нңʼØ%}:0 GlottalNasalToSurface**

*му%{нңʼØ%}%>мд examples:*

*му0%>нд examples:*

*му%{нңʼØ%}%>м°н%{ая%} examples:*

*му0%>м0на examples:*


**%{йнңъʼØ%}:0 GlottalNasalToSurface**

*ил°%{йнңъʼØ%}%^SCSG2%>н examples:*

*илан0%>д examples:*



*ил°%{йнңъʼØ%}%>°ˮ examples:*

*ила0%>0ˮ examples:*

*ил°%{йнңъʼØ%}%>°ць° examples:*

*ила0%>0ць0 examples:*

*ил°%{йнңъʼØ%}%>м°н%{ая%} examples:*

*ил00%>мана examples:*

*ил°%{йнңъʼØ%}%>н° examples:*

*ила0%>н0 examples:*

*ил°%{йнңъʼØ%}%>%{рл%}° examples:*

*ила0%>л0 examples:*

*ил°%{йнңъʼØ%}%>мд° examples:*

*ила0%>нд0 examples:*

*ңум%{йнңъʼØ%}%>мʼ examples:*

*ңув0%>мʼ examples:*

*ңум%{йнңъʼØ%}%^SCSG2%>нʼ examples:*

*ңум00%>дʼ examples:*

*ңум%{йнңъʼØ%}%>0ць examples:*

*ңув0%>аць examples:*



**%{дˮØ%}:0 GlottalNonNasalToZERO LEFT**

*мя%{дˮØ%}%^SCSG2%>нʼ examples:*

*мя00%>тʼ examples:*

*мя%{дˮØ%}%>мд° examples:*

*мя0%>0т0 examples:*

*мя%{дˮØ%}%>д%{ая%} examples:*

*мя0%>та examples:*

*мя%{дˮØ%}%^SCSG2%>нась examples:*

*мя00%>тась examples:*

*тар%^PalVariation%{дˮØ%}%>°мʼ examples:*

*тар00%>0мʼ examples:*

*тар%^PalVariation%{дˮØ%}%>%{рл%}° examples:*

*та000%>л0 examples:*


*мя%{дˮØ%}%>мд° examples:*

*мя0%>0т0 examples:*

*мя%{дˮØ%}%>д%{ая%} examples:*

*мя0%>та examples:*

*мя%{дˮØ%}%^SCSG2%>нась examples:*

*мя00%>тась examples:*

*тар%^PalVariation%{дˮØ%}%>%{рл%}° examples:*

*та000%>л0 examples:*

*тар%^PalVariation%{дˮØ%}%>мд%{ая%} examples:*

*тар00%>0та examples:*

*тар00%>0тя examples:*

RIGHT ARROW ONLY %{дˮØ%}:0

*тар%{дˮØ%}%>ми examples:*

*тарˮ%>ми examples:*

*тар0%>ми examples:*

*тар%{дˮØ%}%>ни examples:*

*тарˮ%>ни examples:*

*тар0%>ни examples:*

**С1:0 GlottalNonNasalToZERO**

*таС1%>мд° examples:*

*та0%>0т0 examples:*

*таС1%>д%{ая%} examples:*

*та0%>та examples:*

*ман°С1%>мд examples:*

*мана0%>0т examples:*

*ман°С1%>дмʼ examples:*

*мана0%>тмʼ examples:*

*таС1%^SCSG2%>нась examples:*

*та00%>тась examples:*

*ман°С1%^SCSG2%>нʼ examples:*

*мана00%>тʼ examples:*



**С1:ˮ UnderlyingToGlottal**

*ман°С1%>0в examples:*

*манаˮ%>ам examples:*

**%{дˮØ%}:ˮ UnderlyingToGlottal LEFT**

*мя%{дˮØ%}%>%{ауоэØ%}л examples:*

*мяˮ%>ал examples:*

*вар%{дˮØ%}%>вна examples:*

*варˮ%>мна examples:*


*тар%{дˮØ%} examples:*

*тарˮ examples:*


*тар%{дˮØ%} examples:*

*тарˮ examples:*

RIGHT ARROW ONLY %{дˮØ%}:ˮ

*тар%{дˮØ%}%>ми examples:*

*тарˮ%>ми examples:*

*тар0%>ми examples:*

*тар%{дˮØ%}%>ни examples:*

*тарˮ%>ни examples:*

*тар0%>ни examples:*


**%{нңʼØ%}:ʼ UnderlyingToGlottal**


**с => ц affrication after Stop**

*мя%{дˮØ%}%>сь examples:*

*мя0%>ць examples:*


*ман°С1%>сиˮ examples:*

*ман00%>циˮ examples:*

**с => з after nasal**

*му%{нңʼØ%}%>сь examples:*

*мун0%>зь examples:*

*ила%{йнңъʼØ%}%>сиˮ examples:*

*илан%>зиˮ examples:*

*ил°%{йнңъʼØ%}%>сиˮ examples:*

*ил0н%>зиˮ examples:*

*ңум%{йнңъʼØ%}%>сиˮ examples:*

*ңум0%>зиˮ examples:*

**v To m **

*ман°С1%>0в examples:*

*манаˮ%>ам examples:*


**%{рл%}:л**

*ман°С1%>0%{рл%} examples:*

*манаˮ%>ал examples:*


**%{рл%}:р**

**%{рл%}:р**


**0:а in single-syllable**
* *ман°С1%>0в*
* *манаˮ%>ам*
* *ңум%{йнңъʼØ%}%>0ць*
* *ңув0%>аць*
**°:а at end of stem**

*ед°%^SCSG2%>нʼ examples:*

*еда0%>нʼ examples:*

*ил°%{йнңъʼØ%}%>мʼ examples:*

*ила0%>мʼ examples:*

*ман°С1%>мд examples:*

*мана0%>0т examples:*

*ман°С1%>0%{рл%} examples:*

*манаˮ%>ал examples:*

*ман°С1%>0в examples:*

*манаˮ%>ам examples:*

*ман°С1%^SCSG2%>нʼ examples:*

*мана00%>тʼ examples:*


*ил°%{йнңъʼØ%}%>кʼ examples:*

*илаң%>гʼ examples:*

**ʼ:н**





Second Vowel Center
**°:у in Pros LEFT**

**ә:у in extra short to у**



**ә:о in extra short to о**



**ә:и in extra short to и**



**ә:ы in extra short to ы**



**ә:э in extra short to э**

**ә:а in extra short to а**

*ил°%{йнңъʼØ%}%>кәд examples:*

*ил0ң0гад examples:*


**0:а in Pros**

*ма%>ˮ0н examples:*

*ма0ˮан examples:*


*ма%>ˮ0м°н%{ая%} examples:*

*ма0ˮам0на examples:*

*ман°С1%>0%{рл%}° examples:*

*манаˮ0ал0 examples:*

*ман°С1%>0м° examples:*

*манаˮ0ам0 examples:*

*ман°С1%>0%{рл%}° examples:*

*манаˮ0ал0 examples:*

*ман°С1%>0м° examples:*

*манаˮ0ам0 examples:*

*хан%>м° examples:*

*хан0в0 examples:*

**0:э in Pros**

*ңэ%>ˮ0м°н%{ая%} examples:*

*ңэ0ˮэм0на examples:*

**0:о between two glottals**

*хо%>ˮ0м°н%{ая%} examples:*

*хо0ˮом0на examples:*

*я%^A2O%>ˮ0м°н%{ая%} examples:*

*ё00ˮом0на examples:*

**0:и after glottal**

*си%>ˮ0м°н%{ая%} examples:*

*си0ˮим0на examples:*

**0:ы between two glottals**

*ңы%>ˮ0м°н%{ая%} examples:*

*ңы0ˮым0на examples:*

**0:у between two glottals**

*ңу%>ˮ0м°н%{ая%} examples:*

*ңу0ˮум0на examples:*



**0:у between two glottals**


**а:я VowelPalatalization left**


**%{ая%}:я VowelPalatalization left**

**%{ая%}:я VowelPalatalization right**

*тар%^PalVariation%{дˮØ%}%>к°н%{ая%} examples:*

*тар000кана examples:*

*тар000кна examples:*

*тар000каня examples:*

*тар000кня examples:*

*тар%^PalVariation%{дˮØ%}%>д%{ая%} examples:*

*тар000та examples:*

*тар000тя examples:*


**%{оё%}:ё VowelPalatalization right**

*ню%>д%{оё%}ʼ examples:*

*ню0доʼ examples:*

*ню0дёʼ examples:*

*тар%^PalVariation%{дˮØ%}%>д%{оё%}ʼ examples:*

*тар000тоʼ examples:*

*тар000тёʼ examples:*


The rule **%{ауоэØ%} <-> у**:

*ну%>к%{ауоэØ%}рт examples:*

*ну0хурт examples:*

The rule **%{ауоэØ%} -> о**:

The rule **%{ауоэØ%} -> а**:

*намда%^VowLoss%>к%{ауоэØ%}в examples:*

*намд000хав examples:*

*мя%{дˮØ%}%>%{ауоэØ%}л examples:*

*мяˮ0ал examples:*

*му%{нңʼØ%}%>к%{ауоэØ%}на  examples:*

*муң0гана examples:*

*ед°%>к%{ауоэØ%}на examples:*

*ед00хана examples:*

**%{ауоэØ%} -> а**

**%{ауоэØ%} -> а**

*хо%>сеты%>к%{ауоэØ%}ʼ examples:*

*хо0сеты0хыʼ examples:*

**%{ауоэØ%} -> а**

*пя%^A2I%>ˮ%{ауоэØ%}н examples:*

*пи00ˮин examples:*




## VOWEL LOWERING

**i2e StemFinalYToE LEFT**


**а:э in stem-internal position**

*хадаба%^StemVowFronting%^A2I%>н examples:*

*хадэби000н examples:*

**a:o in я**


**a:i in мараңгы**

*яˮавла%^A2I%>дмʼ examples:*

*яˮавлы00дмʼ examples:*


**a:i in ңуда**

*ңуда%^A2I examples:*

*ңуди0 examples:*

*хадаба%^StemVowFronting%^A2I%>н examples:*

*хадэби000н examples:*



**о:у word-final position**


**я:и word-final position**

*пя%^A2I examples:*

*пи0 examples:*

*ңодя%^A2I examples:*

*ңоди0 examples:*

**я:е in яха**

*яха%^A2I examples:*

*еси0 examples:*


**а:у яˮавла:яˮавлу LEFT**

**а:у яˮавла:яˮавлу RIGHT**

*яˮавла%^VowRaise%>ˮ examples:*

*яˮавлу00ˮ examples:*


**а:ю яˮавла:яˮавлу**

*пэва%^VowFronting%^VowRaise%>ˮ examples:*

*пэбю000ˮ examples:*
## VOWEL LOSS

**а:ю яˮавла:яˮавлу**



**а:ю яˮавла:яˮавлу**

**я:0 Stem vowel loss in plural accusative**

*тёня%^PalLoss%^VowLoss examples:*

*тён000 examples:*



## CONSONANT CHANGES

**mToV**

*хан°%>м° examples:*

*хана0в0 examples:*

*хану0в0 examples:*

*ңум%{йнңъʼØ%}%>0ць examples:*

*ңув00аць examples:*

*ңум%{йнңъʼØ%}%>°мʼ examples:*

*ңув000мʼ examples:*

*ңум%^MLenition%>о examples:*

*ңув00о examples:*




**m loss before Labial followed by nonglottal cons or vows **

*му%{нңʼØ%}%>мд examples:*

*мун00д examples:*

*по%{йнңъʼØ%}%>мд° examples:*

*пон00д0 examples:*

*мя%{дˮØ%}%>мд° examples:*

*мя000т0 examples:*

*ңум%{йнңъʼØ%}%>м°н%{ая%} examples:*

*ңу000м0на examples:*

**н loss after glottal before д: **

*му%{нңʼØ%}%>нд examples:*

*мун00д examples:*

*по%{йнңъʼØ%}%>нд° examples:*

*пон00д0 examples:*

*мя%{дˮØ%}%>нд° examples:*

*мя000т0 examples:*

*ил°%{йнңъʼØ%}%>нд%{ая%} examples:*

*ил0н00да examples:*

*илан00да examples:*







**н loss after glottal before д: **
**r To l after nasal glottal**

*сыр%>рхавы examples:*

*сыл00хавы examples:*

**r To 0 before glottal and р or л**

*тар%^PalVariation%{дˮØ%}%>%{рл%}° examples:*

*та0000л0 examples:*

*сыр%>рхавы examples:*

*сыл00хавы examples:*



**n to t after non-nasal glottal**

*мя%{дˮØ%}%^SCSG2%>нʼ examples:*

*мя000тʼ examples:*

*ман°С1%^SCSG2%>нʼ examples:*

*мана000тʼ examples:*

*сыр%{йнңъʼØ%}%>нарахав examples:*

*сыр00тарахав examples:*


*мя%{дˮØ%}%^SCSG2%>нась examples:*

*мя000тась examples:*

*тар%^PalVariation%{дˮØ%}%^SCSG2%>нась examples:*

*тар0000тась examples:*

*ман°С1%^SCSG2%>н°ʼ examples:*

*мана000т0ʼ examples:*

**d to t after non-nasal glottal**

*мя%{дˮØ%}%>мд examples:*

*мя000т examples:*

*ман°С1%>мд examples:*

*мана000т examples:*


*мя%{дˮØ%}%>д%{ая%} examples:*

*мя00та examples:*

*мя%{дˮØ%}%>дмʼ examples:*

*мя00тмʼ examples:*

*тар%^PalVariation%{дˮØ%}%>д%{ая%} examples:*

*тар000та examples:*

*тар000тя examples:*

**b to p after non-nasal glottal**

*сырˮ%>бˮ examples:*

*сыр00пˮ examples:*


**ң:0 Before в:м +Sg+Acc+PxPl1:%>ваˮ**

*илң%>ваˮ examples:*

*ил00маˮ examples:*

The rule **ъ:0 with Conj after vowels**:


In the first context ...

In the second context ...




**ˮ:0**

*сырˮ%>бˮ examples:*

*сыр00пˮ examples:*

*сыр%^SCSG2%>накы examples:*

*сыр00такы examples:*
## Realization of glottal stops

### SURFACE CONSONANT


**х:с in яха**

*яха%^A2I examples:*

*еси0 examples:*



**С1:с GlottalNonNasalToSurface**

*ман°С1%>°ць° examples:*

*ман0с0аць0 examples:*

**%{дˮØ%}:д GlottalNonNasalToSurface**

*мя%{дˮØ%}%>°ць° examples:*

*мя00аць0 examples:*


**%{дˮØ%}:д GlottalNonNasalToSurface**






**ь:0 with  GlottalNonNasalToZERO**




* * *
<small>This (part of) documentation was generated from [../src/fst/phonology.twolc](http://github.com/giellalt/lang-yrk/blob/main/../src/fst/phonology.twolc)</small>This is where new words are added as lexc entries before they are
added to the xml source files.
V_ "FinnishTRANSLATION" ;

CONTINUE BELOW

* * *
<small>This (part of) documentation was generated from [../src/fst/stems/verbs_newwords.lexc](http://github.com/giellalt/lang-yrk/blob/main/../src/fst/stems/verbs_newwords.lexc)</small>


We describe here how abbreviations are in Nenets are read out, e.g.
for text-to-speech systems.

For example:

 * s.:syntynyt # ;  
 * os.:omaa% sukua # ;  
 * v.:vuosi # ;  
 * v.:vuonna # ;  
 * esim.:esimerkki # ; 
 * esim.:esimerkiksi # ; 


* * *
<small>This (part of) documentation was generated from [../src/transcriptions/transcriptor-abbrevs2text.lexc](http://github.com/giellalt/lang-yrk/blob/main/../src/transcriptions/transcriptor-abbrevs2text.lexc)</small>
T U N D R A  N E N E T S  G R A M M A R   C H E C K E R









# DELIMITERS


# TAGS AND SETS



## Tags


This section lists all the tags inherited from the fst, and used as tags
in the syntactic analysis. The next section, **Sets**, contains sets defined
on the basis of the tags listed here, those set names are not visible in the output.




### Beginning and end of sentence
BOS
EOS



### Parts of speech tags

N
A
Adv
V
Pron
CS
CC
CC-CS
Po
Pr
Pcle
Num
Interj
ABBR
ACR
CLB
LEFT
RIGHT
WEB
QMARK
PPUNCT
PUNCT

COMMA
¶



### Tags for POS sub-categories

Pers
Dem
Interr
Indef
Recipr
Refl
Rel
Coll
NomAg
Prop
Allegro
Arab
Romertall


### Tags for morphosyntactic properties

Nom
Acc
Gen
Ill
Loc
Com
Ess
Ess
Sg
Du
Pl
Cmp/SplitR
Cmp/SgNom Cmp/SgGen
Cmp/SgGen
PxSg1
PxSg2
PxSg3
PxDu1
PxDu2
PxDu3
PxPl1
PxPl2
PxPl3
Px

Comp
Superl
Attr
Ord
Qst
IV
TV
Prt
Prs
Ind
Pot
Cond
Imprt
ImprtII
Sg1
Sg2
Sg3
Du1
Du2
Du3
Pl1
Pl2
Pl3
Inf
ConNeg
Neg
PrfPrc
VGen
PrsPrc
Ger
Sup
Actio
VAbess



Err/Orth



### Semantic tags

Sem/Act
Sem/Ani
Sem/Atr
Sem/Body
Sem/Clth
Sem/Domain
Sem/Feat-phys
Sem/Fem
Sem/Group
Sem/Lang
Sem/Mal
Sem/Measr
Sem/Money
Sem/Obj
Sem/Obj-el
Sem/Org
Sem/Perc-emo
Sem/Plc
Sem/Sign
Sem/State-sick
Sem/Sur
Sem/Time
Sem/Txt

HUMAN

HAB-ACTOR
HAB-ACTOR-NOT-HUMAN


PROP-ATTR
PROP-SUR



TIME-N-SET


###  Syntactic tags

@+FAUXV
@+FMAINV
@-FAUXV
@-FMAINV
@-FSUBJ>
@-F<OBJ
@-FOBJ>
@-FSPRED<OBJ
@-F<ADVL
@-FADVL>
@-F<SPRED
@-F<OPRED
@-FSPRED>
@-FOPRED>
@>ADVL
@ADVL<
@<ADVL
@ADVL>
@ADVL
@HAB>
@<HAB
@>N
@Interj
@N<
@>A
@P<
@>P
@HNOUN
@INTERJ
@>Num
@Pron<
@>Pron
@Num<
@OBJ
@<OBJ
@OBJ>
@OPRED
@<OPRED
@OPRED>
@PCLE
@COMP-CS<
@SPRED
@<SPRED
@SPRED>
@SUBJ
@<SUBJ
@SUBJ>
SUBJ
SPRED
OPRED
@PPRED
@APP
@APP-N<
@APP-Pron<
@APP>Pron
@APP-Num<
@APP-ADVL<
@VOC
@CVP
@CNP
OBJ
<OBJ
OBJ>
<OBJ-OTHERS
OBJ>-OTHERS
SYN-V
@X





## Sets containing sets of lists and tags

This part of the file lists a large number of sets based partly upon the tags defined above, and
partly upon lexemes drawn from the lexicon.
See the sourcefile itself to inspect the sets, what follows here is an overview of the set types.



### Sets for Single-word sets

INITIAL


### Sets for word or not

WORD
REAL-WORD
REAL-WORD-NOT-ABBR
NOT-COMMA


### Case sets

ADLVCASE

CASE-AGREEMENT
CASE

NOT-NOM
NOT-GEN
NOT-ACC

### Verb sets


NOT-V

### Sets for finiteness and mood

REAL-NEG

MOOD-V

NOT-PRFPRC


### Sets for person

SG1-V
SG2-V
SG3-V
DU1-V
DU2-V
DU3-V
PL1-V
PL2-V
PL3-V





### Pronoun sets

















### Adjectival sets and their complements




### Adverbial sets and their complements




### Sets of elements with common syntactic behaviour


### NP sets defined according to their morphosyntactic features








### The PRE-NP-HEAD family of sets

These sets model noun phrases (NPs). The idea is to first define whatever can
occur in front of the head of the NP, and thereafter negate that with the
expression **WORD - premodifiers**.





















### Border sets and their complements











### Grammarchecker sets








* * *
<small>This (part of) documentation was generated from [../tools/grammarcheckers/grammarchecker.cg3](http://github.com/giellalt/lang-yrk/blob/main/../tools/grammarcheckers/grammarchecker.cg3)</small>