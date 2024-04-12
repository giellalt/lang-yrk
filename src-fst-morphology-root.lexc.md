
# Morphology
INTRODUCTION TO THE MORPHOLOGICAL ANALYSER OF NENETS

# Definitions for Multichar_Symbols

## Analysis symbols
The morphological analyses of wordforms of the TUNDRA NENETS language are presented
in this system in terms of following the symbols.
(It is highly suggested to follow existing standards when adding new tags).
* **+WORK** WORK HAS TO BE DONE Do not remove, replaces +TYÄ
The parts-of-speech are:

* **+N**
* **+A**
* **+Adv**
* **+V**

* **+Pron**
* **+CS**
* **+CC**
* **+Adp**
* **+Po**
* **+Pr**
* **+Interj**
* **+Pcle**
* **+Num**

The parts of speech are further split up into:

* **+Prop**
* **+Pers**
* **+Dem**
* **+Interr**
* **+Refl** reflexive
* **+Recipr**
* **+Rel**
* **+Indef**
* **+Refr** referential adverbs

Adv
* **+Manner**
* **+Refr** (referential),
* **+Temp**

The Usage extents are marked using the following tags:
* **+Err/Orth**
* **+Use/-Spell**
* **+Use/SpellNoSugg** recognized but not suggested in speller

* **+Rus** (100% Russian homograph)

Dialects

* **+Dial/W** (Western dialects),
* **+Dial/T** (Taimyr dialect  ),
* **+Dial/E** (Eastern dialects),

The nominals are inflected in the following Case and Number

* **+Sg**
* **+Du**
* **+Pl**
* **+Acc**
* **+Gen** (Genitive)
* **+Abl**
* **+Dat**
* **+Loc**
* **+Nom**
* **+Pros** (Prosecutive)
* **+Tra**
* **+Abe**
* **+Adc**
* **+Ins**
* **+Apr**
* **+Ine**
* **+Ill**
* **+Ela**
* **+Egr**
* **+Prl**
* **+Pred** = predestinative

are these needed?:

* **+Appr**
* **+Advc**
* **+Ter**
* **+Pro**
* **+Car**
* **+Equ**

derivative suffixes before case endings
* **+Lim** limitative

The possession is marked as such:

* **+PxSg1**
* **+PxSg2**
* **+PxSg3**
* **+PxDu1**
* **+PxDu2**
* **+PxDu3**
* **+PxPl1**
* **+PxPl2**
* **+PxPl3**

The comparative forms are:
* **+Pos**
* **+Comp**
* **+Superl**

Numerals are classified under:

* **+Attr**
* **+Card**
* **+Ord**

Verb moods are:

* **+Ind**
* **+Pot**
* **+Conj**
* **+Imprt**
* **+Opt**
* **+Hort**
* **+Mod/appr** approximative imperfective
* **+Mod/des** desiderative
* **+Mod/futappr** approximative futuritive
* **+Mod/hyp** hyperprobablitative
* **+Mod/int** interrogative
* **+Mod/narr** narrative
* **+Mod/nec** necessitativee
* **+Mod/obl** obligative
* **+Mod/rep** reputative
* **+Mod/sup** superprobabilitative
* **+Mod/perfappr** approximative perfective
* **+Mod/perfprob** perfective probabilitative
* **+Mod/prob** imperfective probabilitative

Verb tenses are:

* **+Aor**
* **+Prt**
* **+Prt1**
* **+Prt2**

Verb personal forms are:

Subject

One of the two following

* **+Sg1**
* **+Sg2**
* **+Sg3**
* **+Pl1**
* **+Pl2**
* **+Pl3**

* **+ScSg1**
* **+ScSg2**
* **+ScSg3**
* **+ScDu1**
* **+ScDu2**
* **+ScDu3**
* **+ScPl1**
* **+ScPl2**
* **+ScPl3**

Object
* **+OcSg3**
* **+OcDu3**
* **+OcPl3**

Other verb forms are

* **+InfImprf**
* **+InfPrf**
* **+PrcImprf**
* **+PrcPrf**
* **+PrcNeg**
* **+PrcFut**
* **+GerFin**
* **+Subord**
* **+Aud**
* **+Evas**
* **+Ger**
* **+ConNeg**
* **+ConNegII**
* **+Neg**
* **+ImprtII**
* **+PrsPrc**
* **+Sup**
* **+VGen**
* **+VAbess**

Abbreviated words are classified with:

* **+ABBR**
* +Symbol = independent symbols in the text stream, like £, €, ©
* **+ACR**

## Symbols that need to be escaped on the lower side (towards twolc):
* **»7**:  Literal »
* **«7**:  Literal «
```
 %[%>%]  - Literal >
 %[%<%]  - Literal <
```

Special symbols are classified with:

* **+CLB**
* **+PUNCT**
* **+LEFT**
* **+RIGHT**

The verbs are syntactically split according to transitivity:

* **+TV**
* **+IV**

* **+Aux** auxilliary verb

Special multiword units are analysed with:

* **+Multi**

Non-dictionary words can be recognised with:

* **+Guess**

Question and Focus particles:

* **+Qst**
* **+Foc**

* **+Sem/Act** Activity
* **+Sem/Amount** Amount
* **+Sem/Ani** Animate
* **+Sem/Aniprod** Animal Product
* **+Sem/Body** Bodypart
* **+Sem/Body-abstr** siellu, vuoig?a, jierbmi
* **+Sem/Build** Building
* **+Sem/Build-part** Part of Bulding, like the closet
* **+Sem/Cat** Category
* **+Sem/Clth** Clothes
* **+Sem/Clth-jewl** Jewelery
* **+Sem/Clth-part** part of clothes, boallu, sávdnji...
* **+Sem/Ctain** Container
* **+Sem/Ctain-abstr** Abstract container like bank account
* **+Sem/Ctain-clth**
* **+Sem/Curr** Currency like dollár, Not Money
* **+Sem/Dance** Dance
* **+Sem/Dir** Direction like GPS-kursa
* **+Sem/Domain** Domain like politics, reindeerherding (a system of actions)
* **+Sem/Drink** Drink
* **+Sem/Dummytag** Dummytag
* **+Sem/Edu** Educational event
* **+Sem/Event** Event
* **+Sem/Feat** Feature, like Árvu
* **+Sem/Feat-phys** Physiological feature, ivdni, fárda
* **+Sem/Feat-psych** Psychological feauture
* **+Sem/Feat-measr** Psychological feauture
* **+Sem/Fem** Female name
* **+Sem/Food** Food
* **+Sem/Food-med** Medicine
* **+Sem/Furn** Furniture
* **+Sem/Game** Game
* **+Sem/Geom** Geometrical object
* **+Sem/Group** Animal or Human Group
* **+Sem/Hum** Human
* **+Sem/Hum-abstr** Human abstract
* **+Sem/Ideol** Ideology
* **+Sem/Lang** Language
* **+Sem/Mal** Male name
* **+Sem/Mat** Material for producing things
* **+Sem/Measr** Measure
* **+Sem/Money** Has to do with money, like wages, not Curr(ency)
* **+Sem/Obj** Object
* **+Sem/Obj-clo** Cloth
* **+Sem/Obj-cogn** Cloth
* **+Sem/Obj-el** (Electrical) machine or apparatus
* **+Sem/Obj-ling** Object with something written on it
* **+Sem/Obj-rope** flexible ropelike object
* **+Sem/Obj-surfc** Surface object
* **+Sem/Org** Organisation
* **+Sem/Part** Feature, oassi, bealli
* **+Sem/Perc-cogn** Cognative perception
* **+Sem/Perc-emo** Emotional perception
* **+Sem/Perc-phys** Physical perception
* **+Sem/Perc-psych** Physical perception
* **+Sem/Plant** Plant
* **+Sem/Plant-part** Plant part
* **+Sem/Plc** Place
* **+Sem/Plc-abstr** Abstract place
* **+Sem/Plc-elevate** Place
* **+Sem/Plc-line** Place
* **+Sem/Plc-water** Place
* **+Sem/Pos** Position (as in social position job)
* **+Sem/Process** Process
* **+Sem/Prod** Product
* **+Sem/Prod-audio** Audio product
* **+Sem/Prod-cogn** Cognition product
* **+Sem/Prod-ling** Linguistic product
* **+Sem/Prod-vis** Visual product
* **+Sem/Rel** Relation
* **+Sem/Route** Name of a Route
* **+Sem/Rule** Rule or convention
* **+Sem/Semcon** Semantic concept
* **+Sem/Sign** Sign (e.g. numbers, punctuation) 
* **+Sem/Sport** Sport
* **+Sem/State** 
* **+Sem/State-sick** Illness
* **+Sem/Substnc** Substance, like Air and Water
* **+Sem/Sur** Surname
* **+Sem/Symbol** Symbol
* **+Sem/Time** Time
* **+Sem/Tool** Prototypical tool for repairing things
* **+Sem/Tool-catch** Tool used for catching (e.g. fish)
* **+Sem/Tool-clean** Tool used for cleaning
* **+Sem/Tool-it** Tool used in IT
* **+Sem/Tool-measr** Tool used for measuring
* **+Sem/Tool-music** Music instrument
* **+Sem/Tool-write** Writing tool
* **+Sem/Txt** Text (girji, lávlla...)
* **+Sem/Veh** Vehicle
* **+Sem/Wpn** Weapon
* **+Sem/Wthr** The Weather or the state of ground

Semantics are classified with

Derivations are classified under the morphophonetic form of the suffix, the
source and target part-of-speech.

* **+V→N**
* **+V→V**
* **+V→A**
* **+Der/xxx**
* **+Der/MWN** modifier without noun head
* **+Der/Pr** this is used with predication of nominals and deverbal modalities
* _+Der/Cop_ This will replace the nominal conjugation Der/Pr

## Morphophonology

To represent phonologic variations in word forms we use the following
symbols in the lexicon files:
* **%{ая%}** in Pros
* **%{оё%}** in +N+Sg+Nom+PxPl3
* **%{рл%}** +N+Sg+Nom+PxSg2
* **%{аяуюØ%}** хан+N+Sg+Acc+PxSg1: ханув, ханав
* **%{увм%}** +N+Sg+Pros
* **%{вм%}** +N+Sg+Nom+PxSg1

And the following triggers to control variation:
* **{front}**
* **{back}**
* **%^SCSG2** this allows n2d +V+Ind+Aor+ScSg2:%>н°%^SCSG2
* **%^PLNOM** disallows i2e +N+Pl+Nom+PxDu1+Der/Cop+Ind+Aor+ScPl3
* **%^PalVariation** This allows for тар%{дˮØ%}%>д%{оё%}нзь

Protoletters for xfst:
* **%{ауоэØ%}**  А1:а А1:у А1:о А1:э schwa
* **%{ауоэиыØ%}** before pros

This is the schwa or reduced vowel occurring after x in case endings

* **А2** Alternating between zero and а

These are proto-glottals
* **%{дˮØ%}**
* **С1**
* **%{нңʼØ%}**
* **%{йнңъʼØ%}** = These are proto-glottals

* **Г1**
* **В1**
* **Е1**
* **Е2**
* **Ы1**
* **Д1**
* **Ы2** = These are for developing underlying morphology rules

## Triggers

* **%^A2O** Initially this is used for the noun "я" to enable a:o
* **%^A2I** for я:и in пя
* **%^MLenition** м:в м:б
* **%^VowLower** vowel lowering ы:э у:о
* **%^VowRaise** э:ы о:у
* **%^VowLoss** stem-final vowel is lost in plural accusative form
* **%^StemVowFronting** хасава:хасев
* **%^VowFronting** хадась:хадэйнинзь
* **%^PalLoss** in combination with stem-final vowel loss
* **%^HardFronting** яля:ялэ

We have manually optimised the structure of our lexicon using the following
flag diacritics to restrict morhpological combinatorics:

* **@P.NeedNoun.ON@**
* **@D.NeedNoun.ON@**
* **@C.NeedNoun@**

Object conjugation

* **@P.CONJ.ObjAll@**
* **@R.CONJ.ObjAll@**
* **@C.CONJ@**

# The Root lexicon

The word forms in Nenets start from the lexeme roots of basic
word classes, or optionally from prefixes:

* **adjectives ;**
* **adpositions ;**
* **adverbs ;**
* **interjections ;**
* **nouns ;**
* **particles ;**
* **pronouns ;**
* **propernouns ;**
* **quantifiers ;**
* **verbs ;**

* **V_NEWWORDS ;** This is for feeding new verbs.
* **Punctuation ;**
* **Symbols ;**

* **CONJUNCTION ;**
* **SUBJUNCTION ;**
* **INTERJECTION ;**
* **POSTPOSITION ;**

* * *

<small>This (part of) documentation was generated from [src/fst/morphology/root.lexc](https://github.com/giellalt/lang-yrk/blob/main/src/fst/morphology/root.lexc)</small>
