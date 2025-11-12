# Nenets language model documentation

All doc-comment documentation in one large file.

---

## src-cg3-functions.cg3.md 



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

### HABITIVE MAPPING

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

#### sma object

* **<advlEss** (@<ADVL) for ESS-ADVL if; FMAINV to the left
* **<spredEss** (@<SPRED) for N Ess if; FMAINV to the left is intransitive or bargat

### SUBJ MAPPING - leftovers

### OBJ MAPPING - leftovers

### HNOUN MAPPING

* * *

<small>This (part of) documentation was generated from [src/cg3/functions.cg3](https://github.com/giellalt/lang-yrk/blob/main/src/cg3/functions.cg3)</small>

---

## src-fst-morphology-affixes-adjectives.lexc.md 

Adjective inflection
Nenets  adjectives.

**LEXICON æLEXNAME@ to #

* **LEXICON A_ҢЭ** ңэ:ңэ 1  

* **LEXICON A_ПАНЫ** пӑны:пӑны 9 

* **LEXICON A_ХУСУВЭЙ** хусувэй: 10 !!ProsSg -ювна

* **LEXICON A_ХАНО** хӑн: 11 !!ProsSg -увна
[total=27]
хӑн xən°    хӑнӑн’ xənən°h        хӑнˮ xən°q     хӑно xəno

* **LEXICON A_ЕД** ед: 13 !!ProsSg -увна /-ювна

* **LEXICON A_ҢУДИ** ңуда: 15 !!ProsSg -вна

* **LEXICON A_ҢОДИ** ңодя: 17 !!ProsSg -вна

* **LEXICON A_ХОБ** хоба: 19 !!ProsSg -вна

* **LEXICON A_ТЁН** тёня: 20 !!ProsSg -вна

* **LEXICON A_ПИСЬ** пися: 21 !!ProsSg -вна

* **LEXICON A_ҢАНУ** ңӑно: 23 !!ProsSg -вна
[total=57]
ңӑно ŋəno   ңӑнон’ ŋənon°h ңӑноˮ ŋənoq    ңӑну ŋənu

* **LEXICON A_ЯКЫ** якэ: 24 ProsSg -вна

* **LEXICON A_ҢУВО** ңумʼ:ңум 25 !!ProsSg -(м)на
ңум’ ŋum     ңумд’ ŋumt°h    ңувˮ ŋuw°q      ңуво ŋuwo

* **LEXICON A_НЮБЕ-Pal/Var** нюмʼ:нюм 26
нюм’ nyum    нюмд’ nyumt°h   нювˮ nyuw°q     нюбе nyubye

* **LEXICON A_ВЫҢО** выʼ:вы 29  

Check this

* **LEXICON A_МЯДО** мяˮ:мя 35   !!ProsSg -мна

LEXICON A_САБЦЬ тир: 12 !!ProsSg -увна
What makes this different from N_ТИРЕ?

* **LEXICON A_САВНЕ** 

* * *

<small>This (part of) documentation was generated from [src/fst/morphology/affixes/adjectives.lexc](https://github.com/giellalt/lang-yrk/blob/main/src/fst/morphology/affixes/adjectives.lexc)</small>

---

## src-fst-morphology-affixes-adpositions.lexc.md 


## Adposition inflection
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

<small>This (part of) documentation was generated from [src/fst/morphology/affixes/adpositions.lexc](https://github.com/giellalt/lang-yrk/blob/main/src/fst/morphology/affixes/adpositions.lexc)</small>

---

## src-fst-morphology-affixes-adverbs.lexc.md 

## Adverbs
Nenets adverbs...

* **LEXICON ADV_** to # without tag

* **LEXICON ADV-LOC_** to # with tag +Loc

* **LEXICON ADV-TEMP_** adds +Temp and goes to #

* **LEXICON ADV-MANNER_**

* **LEXICON ADV-REF_** Some are secodary predicates, conjuctions

* **LEXICON ADV-REF_Д1**

* * *

<small>This (part of) documentation was generated from [src/fst/morphology/affixes/adverbs.lexc](https://github.com/giellalt/lang-yrk/blob/main/src/fst/morphology/affixes/adverbs.lexc)</small>

---

## src-fst-morphology-affixes-clitics.lexc.md 

## Clitics inflection
Nenets clitics...

**LEXICON æLEXNAME@ optional +Qst 

**LEXICON æLEXNAME@ leads to #.

* * *

<small>This (part of) documentation was generated from [src/fst/morphology/affixes/clitics.lexc](https://github.com/giellalt/lang-yrk/blob/main/src/fst/morphology/affixes/clitics.lexc)</small>

---

## src-fst-morphology-affixes-descriptives.lexc.md 

## Descriptives
Nenets descriptives...

**LEXICON æLEXNAME@ adds the tag **+Descr**

* * *

<small>This (part of) documentation was generated from [src/fst/morphology/affixes/descriptives.lexc](https://github.com/giellalt/lang-yrk/blob/main/src/fst/morphology/affixes/descriptives.lexc)</small>

---

## src-fst-morphology-affixes-interjections.lexc.md 

## Interjections
Nenets interjections...

**LEXICON æLEXNAME@ just goes to #

* * *

<small>This (part of) documentation was generated from [src/fst/morphology/affixes/interjections.lexc](https://github.com/giellalt/lang-yrk/blob/main/src/fst/morphology/affixes/interjections.lexc)</small>

---

## src-fst-morphology-affixes-nouns.lexc.md 

## Noun inflection

Nenets nouns inflect in cases.

**LEXICON æLEXNAME@ 
* **LEXICON N_ҢЭ** ңэ:ңэ 1  ProsSg -вна
Yaml: **xo, ngaeTS**
**LEXICON æLEXNAME@ 

* **LEXICON N_ҢЭ-Pal/Var** ңэ:ңэ 1  ProsSg -вна
Yaml: **nyeTS**

* **LEXICON N_Ё** я:я 2 ProsSg -вна
Yaml: **ya, yaTS**

* **LEXICON N_ПИ** пя:пя 3 ProsSg -вна
Yaml: **N-pyaTS**

* **LEXICON N_ТЫ** ты: 4 ProsSg -вна
Yaml: **tyTS**

* **LEXICON N_ХАВО** ха: 5 ProsSg -вна
Yaml: **tyTS**

* **LEXICON N_СЁЁ** сё: 6 ProsSg -вна

* **LEXICON N_ИБЕ** и: 7 ProsSg -вна

* **LEXICON N_ХАБИЕ** хӑби:8ProsSg -вна

* **LEXICON N_ПАНЫ** пӑны:пӑн 9 ы!ProsSg -(э)вна

* **LEXICON N_ХУСУВЭЙ** хусувэй: 10 ProsSg -ювна

* **LEXICON N_ХАНО** хӑн: 11P ProsSg -увна
Yaml: **xano**

* **LEXICON N_ТИРЕ** тир: 12 ProsSg -увна

* **LEXICON N_ЕД** ед: 13 ProsSg -увна /-ювна

* **LEXICON N_МАРАҢГЫ** мӑраңга: 14PProsSg -вна

* **LEXICON N_ҢУДИ** ңуда: 15 ProsSg -вна
Yaml: **N-ngudiTS**

* **LEXICON N_ЕСИ** ая̆ха: 16PProsSg -вна
Yaml: **N-yaxaTS**

* **LEXICON N_ҢОДИ** ңодя: 17 ProsSg -вна
Yaml: **N-ngodiTS**

* **LEXICON N_ЯЛЭ** яля: 18 ProsSg -вна

* **LEXICON N_ХОБ** хоба:хоба 19 ProsSg -вна
Yaml: **xob**

* **LEXICON N_ТЁН** тёня:тёня 20 ProsSg -вна
Yaml: **tyon**

* **LEXICON N_ПИСЬ** пися: 21 ProsSg -вна

* **LEXICON N_ХАСЕВ** хасава: 22 ProsSg -вна

* **LEXICON N_ҢАНУ** ңӑно: 23 ProsSg -вна
Yaml: **nano**

* **LEXICON N_ЯКЫ** якэ: 24 ProsSg -вна

* **LEXICON N_ҢУВО** ңумʼ:ңум 25 ProsSg -(м)на
Yaml: **yam, ngumhTS**

* **LEXICON N_НЮБЕ** нюмʼ: 26  ProsSg -(м)на

* **LEXICON N_МУНО** муʼ:му 27  ProsSg -мна

* **LEXICON N_ПОЁ** поʼ:по 28  ProsSg -мна
Yaml: **poyo**

* **LEXICON N_ВЫҢО** выʼ:вы 29  ProsSg -мна /-мана

* **LEXICON N_ИЛЪЕ** илʼ:ил 30   ProsSg -мана
Yaml: **ilje**
| --- 

* **LEXICON N_НЕНЭЦИЕ** ненэцьʼ:ненэць 30   ProsSg -мана
Yaml: **nyenecyh**
| --- 

* **LEXICON N_ПАХАЁ** пӑхӑʼ: 31   ProsSg -мна
| --- 

* **LEXICON N_СЕРО** серˮ: 32   ProsSg -мана / -мня

* **LEXICON N_ТАРЕ** тӑрˮ:тар 33   ProsSg -мня
| --- 

* **LEXICON N_МАНСО** мӑнˮ: 34   ProsSg -мна

* **LEXICON N_МЯДО** мяˮ:мя 35   ProsSg -мна
Yaml: **myadoTS**
| --- 

* **LEXICON N_ИДЕ** иˮ: 36   ProsSg -мна
Yaml: **yidye**

* **LEXICON N_ҢЭ/ХАБИЕ** ңэ:ңэ 1  ProsSg -вна
хӑби:8 ProsSg -вна

та:та 

* **LEXICON NMN_ҢУДИ** ңуда: 15 ProsSg -вна
Yaml: **ngudi**
* **POSSESSA-PLURAL ;** +Pl+Dat, +Pl+Loc, +Pl+Abl

* **LEXICON NMN_ҢОДИ**
* **POSSESSA-PLURAL ;** +Pl+Dat, +Pl+Loc, +Pl+Abl

* **LEXICON NMN_ХОБ** хоба:хоба 19 ProsSg -вна
Yaml: **xob**
* **POSSESSA-PLURAL ;** +Pl+Dat, +Pl+Loc, +Pl+Abl

* **LEXICON NMN_ПИСЬ** пися: 21 ProsSg -вна
* **POSSESSA-PLURAL ;** +Pl+Dat, +Pl+Loc, +Pl+Abl

* **LEXICON NMN_ҢАНУ** ңӑно: 23 ProsSg -вна
* **POSSESSA-PLURAL ;** +Pl+Dat, +Pl+Loc, +Pl+Abl

* **LEXICON NMN_ҢУВО** ңумʼ:ңум 25 
* **:ʼ POSSESSA-PLURAL ;** +Pl+Dat, +Pl+Loc, +Pl+Abl

* **LEXICON NMN_НЮБЕ** нюмʼ: 26

* **LEXICON NMN_МУНО** муʼ: 27  ProsSg -мна

No n2d

* **:%{йнңъʼØ%} SGNOMSUF ;** 
* **:%{йнңъʼØ%} SG-NOM-STEM ;** 
* **:%{йнңъʼØ%} POSSESSA-PLURAL ;** +Pl+Dat, +Pl+Loc, +Pl+Abl

Where is the variation?

* **LEXICON NMN_ТАРЕ** тӑрˮ:тар 33   ProsSg -мня

* **LEXICON N_ВАР/ТАРЕ** мяˮ:мя 35   ProsSg -мна

* **LEXICON NMN_ВАР** мяˮ:мя 35   ProsSg -мна
Yaml: **waro**
* **:%{дˮØ%} POSSESSA-PLURAL ;** +Pl+Dat, +Pl+Loc, +Pl+Abl

* **LEXICON NMN_МЯДО** мяˮ:мя 35   ProsSg -мна
Yaml: **myado**
* **:%{дˮØ%} SGLOCSUF_Хна ;** мякна
* **:%{дˮØ%} POSSESSA-PLURAL ;** +Pl+Dat, +Pl+Loc, +Pl+Abl

Where is the variation?

Where is the variation?
* **:%{дˮØ%} POSSESSA-PLURAL ;** +Pl+Dat, +Pl+Loc, +Pl+Abl

* **LEXICON N_ТЮСЕ** тюˮ:тюсе 

* **LEXICON N_САВНЕ** 

* **LEXICON N_ПЕНЗЕРЕ** пензерˮ:пензер

* **LEXICON N_САБЦЬ** сабць:сабць

* **LEXICON N_МЕРЁ** мерё:мерё

NMN

* **LEXICON NMN_ҢЭ-OLD** ңэ:ңэ 1  ProsSg -вна
* **SG-ACC-STEM ;** SGACCSUF, SGGENSUF
* **SG-NOM-STEM ;** SG/DAT,LOC, ABL,TRA,PRO; DU/NOM,ACC,GEN; PL/DAT,LOC,ABL,TRA; PX-s, NOMINAL-CONJUGATION
* **PLNOMSUF ;** 
* **PLACCSUF_Zero ;** => PL-ACC_STEM
* **POSSESSA-PLURAL ;** +Pl+Dat, +Pl+Loc, +Pl+Abl

* **POSSESSA-PLURAL ;** +Pl+Dat, +Pl+Loc, +Pl+Abl

9
* **:%^VowLower POSSESSA-PLURAL ;** +Pl+Dat, +Pl+Loc, +Pl+Abl

* **LEXICON NMN_ХУСУВЭЙ** хусувэй: 10 ProsSg -ювна
* **POSSESSA-PLURAL ;** +Pl+Dat, +Pl+Loc, +Pl+Abl

* LEXICON NMN_ХАНО-OLD  11 хан:хан

* **LEXICON NMN_ТИРЕ** тир: 12 ProsSg -увна
* **POSSESSA-PLURAL ;** +Pl+Dat, +Pl+Loc, +Pl+Abl

* **LEXICON NMN_ЕД** ед: 13 ProsSg -увна /-ювна
Yaml: **yed**
* **POSSESSA-PLURAL ;** +Pl+Dat, +Pl+Loc, +Pl+Abl

### NOMINALS "NMN"
#### THREE-SYLLABLE VOWEL-FINAL STEMS

* **POSSESSA-PLURAL ;** +Pl+Dat, +Pl+Loc, +Pl+Abl

таˮ:та

варˮ:вар
Yaml: **N-tarTS**
| --- 

The singular accusative stem

* **LEXICON SGLOCSUF_Хна** мякна

* **LEXICON SGLOCSUF_Хана** серкана

Start Plural

What is assumed on the basis of the plural accusative
* **+Pl+Pros:%>ˮ%{увм%}А2на K ;** When does this take a vowel хоˮомна

Possessor Indices

* **+Sg+Nom+PxSg1+Der/Cop+Ind+Aor+ScSg3:%>в K ;** 2013-10-22 Should this also have +ScSg3 marking

* **LEXICON AFTER-OBLIQUE-SG-POSSESSA-COME-POSSESSOR-INDICES ** singular possessa in +Gen, +Dat, +Loc, +Abl share the same possessor indices

* **LEXICON DV-OBLIQUE-SG-POSSESSA-TAKE-POSSESSOR-INDICES_TO-BE-FOLLOWED-BY-SG3-PRED-AOR/PRT1 ** singular possessa oblique possessor indices

SINUGLAR CASES

The next line in +Sg+Pros+PxDu2:%>%{увм%}А2нандиʼ must be removed

Dual possessa

Dual possessa

Plural Possessa

* **+PxPl1:наˮ K ; ** The morpheme boundary has been removed to indicate a distinct difference in phonological behavior.

Conjugation of nouns and adjectives

### NEW

>>NEW-SG-LOC_Кна/Кана

* * *

<small>This (part of) documentation was generated from [src/fst/morphology/affixes/nouns.lexc](https://github.com/giellalt/lang-yrk/blob/main/src/fst/morphology/affixes/nouns.lexc)</small>

---

## src-fst-morphology-affixes-pronouns.lexc.md 

## Pronoun inflection
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

<small>This (part of) documentation was generated from [src/fst/morphology/affixes/pronouns.lexc](https://github.com/giellalt/lang-yrk/blob/main/src/fst/morphology/affixes/pronouns.lexc)</small>

---

## src-fst-morphology-affixes-propernouns.lexc.md 

## Proper noun inflection
Nenets proper nouns inflect in the same cases as regular
nouns, but with a XXX as separator.

**LEXICON æLEXNAME@ for bunclassified ones

#### ONE-SYLLABLE VOWEL-FINAL STEM
**LEXICON æLEXNAME@ 

**LEXICON æLEXNAME@ 

#### ONE-SYLLABLE CONSONANT-FINAL STEM
**LEXICON æLEXNAME@ 

#### TWO-SYLLABLE CONSONANT-FINAL STEM
* **LEXICON PROP_ПАНЫ** пӑны:пӑны 9

* **LEXICON PROP_ХАНО** хӑн: 11P ProsSg -увна
Yaml: **xano**

**LEXICON æLEXNAME@ 

**LEXICON æLEXNAME@ 

**LEXICON æLEXNAME@ 

**LEXICON æLEXNAME@ 

* **LEXICON PROP_ЯЛЭ** яля: 18 ProsSg -вна
/total=2/
яля yalya    ялян’ yalyan°h  яляˮ yalyaq     ялэ yale

**LEXICON æLEXNAME@ 

**LEXICON æLEXNAME@ 

**LEXICON æLEXNAME@ 

**LEXICON æLEXNAME@ 

* **LEXICON PROP_ХАСЕВ** хасава: 22 ProsSg -вна
/total=1/
хасава xasawa        хасаван’ xasawan°h      хасаваˮ xasawaq хасев xasyew°
* **+N+Prop: POSSESSA-PLURAL ;** +Pl+Dat, +Pl+Loc, +Pl+Abl

**LEXICON æLEXNAME@ 

**LEXICON æLEXNAME@ 

#### THREE-SYLLABLE VOWEL-FINAL STEM
**LEXICON æLEXNAME@ 

**LEXICON æLEXNAME@  Here we need some kind of vowel harmony

* * *

<small>This (part of) documentation was generated from [src/fst/morphology/affixes/propernouns.lexc](https://github.com/giellalt/lang-yrk/blob/main/src/fst/morphology/affixes/propernouns.lexc)</small>

---

## src-fst-morphology-affixes-quantifiers.lexc.md 

## Quantifier inflection
Nenets quantifiers ...

* **LEXICON NUM_МЯДО**

* **LEXICON NUM_ВАР**

* **LEXICON NUM_ҢУДИ**

* **LEXICON NUM_ҢОДИ**

* **LEXICON NUM_ТАРЕ**

LEXICON NUM_ЕД  ед: 13 

* **LEXICON NUM_ЕД/ТИРЕ**

* **LEXICON NUM_ЕД/ХАНО**

* **LEXICON NUM_ҢОДИ/ТЁН**

* **LEXICON NUM_ТИРЕ/ХАНО**

* **LEXICON NUM_ХУСУВЭЙ**

* **LEXICON QNT_ХУСУВЭЙ**

we need to get away from these: NUM_VOW and NUM_CONS
it's done

* * *

<small>This (part of) documentation was generated from [src/fst/morphology/affixes/quantifiers.lexc](https://github.com/giellalt/lang-yrk/blob/main/src/fst/morphology/affixes/quantifiers.lexc)</small>

---

## src-fst-morphology-affixes-symbols.lexc.md 


## Symbol affixes

**LEXICON æLEXNAME@ 

**LEXICON æLEXNAME@ 

**LEXICON æLEXNAME@ 

**LEXICON æLEXNAME@ 

**LEXICON æLEXNAME@ 

* * *

<small>This (part of) documentation was generated from [src/fst/morphology/affixes/symbols.lexc](https://github.com/giellalt/lang-yrk/blob/main/src/fst/morphology/affixes/symbols.lexc)</small>

---

## src-fst-morphology-affixes-verbs.lexc.md 

## Nenets Verb inflection

**LEXICON V_** for unassigned verbs

### ONE-SYLLABLE STEMS WITH STEM-FINAL VOWEL
* **LEXICON IV_Е** есь:е

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

* **LEXICON IV_ҢЭ** ңэсь:ңэ
**LEXICON IV_ҢЭ** 

**LEXICON IV_ҢЭ-Pal/Var** 

**LEXICON IV_ТУ** 

**LEXICON TV_ТУ** 

**LEXICON IV_ХО** 

**LEXICON TV_ХО** 

**LEXICON VR_ХО-Pal/Var** 

**LEXICON IV_ХЭ** 

### TWO-SYLLABLE STEMS WITH STEM-FINAL VOWEL

* **LEXICON IV_НАМДА** намдась:намда
**LEXICON IV_НАМДА** 

**LEXICON TV_НАМДА** 

**LEXICON VR_НАМДА** 

**LEXICON IV_ВАДЮ** 

**LEXICON TV_ВАДЮ** 

* **LEXICON IV_ЯКУ** якась:яка

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

* **LEXICON IV_ХАДА** хадась:хада

* **LEXICON TV_ХАДА** хадась:хада

**LEXICON VR_ХАДА** 

**LEXICON IV_ЮХУ** 

**LEXICON TV_ЮХУ** 

#### THREE-SYLLABLE STEMS WITH STEM-FINAL VOWEL
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

#### ONE-SYLLABLE STEMS WITH STEM-FINAL CONSONANT
* **LEXICON IV_МАН** манзь:ма%{нңʼØ%} 
* Yaml: **manzj**

**LEXICON IV_МИН** 

**LEXICON IV_МИН-Pal/Var** 

**LEXICON TV_МИН** 

**LEXICON VR_МИН** 

**LEXICON IV_САС** 

* LEXICON TV_САС  манэць:манэ

#### TWO-SYLLABLE STEMS WITH STEM-FINAL CONSONANT
* **LEXICON IV_НЭКАЛ** 

* **LEXICON IV_ҢАДИМ/ҢАРАМ** 2013-12-16

### AFTER +TV, +IV, +Aux, +Refl
Not yet written.

### CONJUGATION BY STEM TYPE

#### ONE-SYLLABLE STEMS WITH STEM-FINAL VOWEL

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

#### TWO-SYLLABLE STEMS WITH STEM-FINAL VOWEL
*  PRC-NEG ; 	+PrcNeg +PrcFut
* :%^VowRaise PRC-NEG ; 	+PrcNeg +PrcFut

* **LEXICON V-01_ЯКУ** якась:яка
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

#### THREE-SYLLABLE STEMS WITH STEM-FINAL VOWEL
а > э in Pl Oc 
*  PRC-NEG ; 	+PrcNeg +PrcFut

V_refl 2013-03-04  а > ы (ъя before х)
*  PRC-NEG ; 	+PrcNeg +PrcFut

*  PRC-NEG ; 	+PrcNeg +PrcFut
* :%^VowRaise PRC-NEG ; 	+PrcNeg +PrcFut

* **LEXICON V-01_ЯˮАВЛУ ** яˮавлась:яˮавла
*  PRC-NEG ; 	+PrcNeg +PrcFut
* :%^VowRaise PRC-NEG ; 	+PrcNeg +PrcFut

#### ONE-SYLLABLE STEMS WITH STEM-FINAL CONSONANT
* **LEXICON V-01_МАН** манзь:ма%{нңʼØ%} 
* Yaml: **manzj**
*  PRC-NEG ; 	+PrcNeg +PrcFut

*  PRC-NEG ; 	+PrcNeg +PrcFut

*  PRC-NEG ; 	+PrcNeg +PrcFut

* LEXICON V-01_САС  манэць:манэ

* :С1 PRC-NEG_МАДАВЭЙ ; 	+PrcNeg +PrcFut

* **LEXICON V-NEW_ТИР**

V_refl 2013-03-04

*  PRC-NEG ; 	+PrcNeg +PrcFut

#### TWO-SYLLABLE STEMS WITH STEM-FINAL CONSONANT
* **LEXICON V-01_НЭКАЛ** нэкалць:нэкал

*  PRC-NEG ; 	+PrcNeg +PrcFut

*  PRC-NEG ; 	+PrcNeg +PrcFut

V_refl 2013-03-04

Mutual verbal conjugation
* **LEXICON IND-AOR** All except Sg3 Du3

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

* **+PrcFut:%>%{вм%}анда K ;**

* **+PrcFut:%>%{вм%}нда K ;** Should this form be here 2013-11-25

* **+PrcFut:%>%{вм%}нда K ;** Should this form be here 2013-11-25

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

<small>This (part of) documentation was generated from [src/fst/morphology/affixes/verbs.lexc](https://github.com/giellalt/lang-yrk/blob/main/src/fst/morphology/affixes/verbs.lexc)</small>

---

## src-fst-morphology-phonology.twolc.md 

## Nenets twol file

This file documents the [phonology.twolc file](http://github.com/giellalt/lang-yrk/blob/main/src/fst/phonology.twolc) 

### Letters of the alphabet
* **а б в г д е ё ж з и й к л м н ң о п р с т у ф х ц ч ш щ ъ ы ь э ю я** 
* **А Б В Г Д Е Ё Ж З И Й К Л М Н Ң О П Р С Т У Ф Х Ц Ч Ш Щ Ъ Ы Ь Э Ю Я** 

* **°:0** Directly from Tapani Salminen extra short vowel

* **ә:а** Directly from Tapani Salminen schwa

### Archiphonemes for vowels

* %{ауоэØ%}:а  А1:а А1:у А1:о А1:э SCHWA
* %{ауоэиыØ%}:0 before pros

* А2:а  

* Ы1:о   
* Ы1:е  

* Ы2:э  

### Archiphonemes for glottals

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

* **%{аяуюØ%}:0** хан+N+Sg+Acc+PxSg1: ханув, ханав

* **%{увм%}:0** +N+Sg+Pros

* **%{вм%}:0** +N+Sg+Nom+PxSg1

### triggers

*  %^SCSG2:0     this allows n2d +V+Ind+Aor+ScSg2:%>н°%^SCSG2
*  %^PLNOM:0     disallows i2e +N+Pl+Nom+PxDu1+Der/Cop+Ind+Aor+ScPl3
*  %^A2O:0      
*  %^A2I:0        

* **%^PalVariation:0** This allows for тар%{дˮØ%}%>д%{оё%}нзь

*  %^MLenition:0  lenition
*  %^VowLower:0  vowel lowering ы:э у:о
*  %^VowRaise:0  vowel raising э:ы о:у
*  %^VowLoss:0      stem-final vowel is lost in plural accusative
*  %^StemVowFronting:0      хасава:хасев
*  %^VowFronting:0      хадась:хадэйнинзь
*  %^PalLoss:0      in combination with stem-final vowel loss тёня:тён
*  %^HardFronting:0      яля:ялэ

### Boundary symbols

*  %>      
hash

## Rules

**к: -> г after nasal glottal**
* *му{нңʼØ}>кʼ*
* *муң>гʼ*

* *ил°{йнңъʼØ}>к°ʼ*
* *илаң>г0ʼ*

**к: to х after Vowels**

* ты^VowLower>да examples:*

* тэ0>да examples:*

* ед°>к{ауоэØ}на examples:*

* ед0>хана examples:*

* намда^VowLoss>к{ауоэØ}в examples:*

* намд00>хав examples:*

**nTod**

* му{нңʼØ}^SCSG2>нʼ examples:*

* мун0>дʼ examples:*

* ңум{йнңъʼØ}^SCSG2>нʼ examples:*

* ңум00>дʼ examples:*

* ңум{йнңъʼØ}^SCSG2>н°ʼ examples:*

* ңум00>д0ʼ examples:*

**%{нңʼØ%}:н GlottalNasalToSurface**

* му{нңʼØ}>нд examples:*

* мун>0д examples:*

* му{нңʼØ}>сь examples:*

* мун0>зь examples:*

* му{нңʼØ}^SCSG2>нʼ examples:*

* мун0>дʼ examples:*

**%{нңʼØ%}:ң GlottalNasalToSurface**

* му{нңʼØ}>кʼ examples:*

* муң>гʼ examples:*

**%{йнңъʼØ%}:ң GlottalNasalToSurface**

* ил°{йнңъʼØ}>к°ʼ examples:*

* илаң>г0ʼ examples:*

**%{йнңъʼØ%}:н GlottalNasalToSurface**

* ил°{йнңъʼØ}^SCSG2>н examples:*

* илан0>д examples:*

* ила%{йнңъʼØ%}%>сиˮ examples:*

* илан%>зиˮ examples:*

* ил°%{йнңъʼØ%}%>н°ʼ examples:*

* илан%>д0ʼ examples:*

* ил°%{йнңъʼØ%}%>дмʼ examples:*

* илан%>дмʼ examples:*

* илан%>дув0 examples:*

* ил0н%>дув0 examples:*

**%{йнңъʼØ%}:ъ GlottalNasalToSurface**

* ил°%{йнңъʼØ%}е examples:*

* ил0ъе examples:*

**%{нңʼØ%}:0 GlottalNasalToSurface**

* му%{нңʼØ%}%>мд examples:*

* му0%>нд examples:*

* му%{нңʼØ%}%>м°н%{ая%} examples:*

* му0%>м0на examples:*

**%{йнңъʼØ%}:0 GlottalNasalToSurface**

* ил°%{йнңъʼØ%}%^SCSG2%>н examples:*

* илан0%>д examples:*

* ил°%{йнңъʼØ%}%>°ˮ examples:*

* ила0%>0ˮ examples:*

* ил°%{йнңъʼØ%}%>°ць° examples:*

* ила0%>0ць0 examples:*

* ил°%{йнңъʼØ%}%>м°н%{ая%} examples:*

* ил00%>мана examples:*

* ил°%{йнңъʼØ%}%>н° examples:*

* ила0%>н0 examples:*

* ил°%{йнңъʼØ%}%>%{рл%}° examples:*

* ила0%>л0 examples:*

* ил°%{йнңъʼØ%}%>мд° examples:*

* ила0%>нд0 examples:*

* ңум%{йнңъʼØ%}%>мʼ examples:*

* ңув0%>мʼ examples:*

* ңум%{йнңъʼØ%}%^SCSG2%>нʼ examples:*

* ңум00%>дʼ examples:*

* ңум%{йнңъʼØ%}%>0ць examples:*

* ңув0%>аць examples:*

**%{дˮØ%}:0 GlottalNonNasalToZERO LEFT**

* мя%{дˮØ%}%^SCSG2%>нʼ examples:*

* мя00%>тʼ examples:*

* мя%{дˮØ%}%>мд° examples:*

* мя0%>0т0 examples:*

* мя%{дˮØ%}%>д%{ая%} examples:*

* мя0%>та examples:*

* мя%{дˮØ%}%^SCSG2%>нась examples:*

* мя00%>тась examples:*

* тар%^PalVariation%{дˮØ%}%>°мʼ examples:*

* тар00%>0мʼ examples:*

* тар%^PalVariation%{дˮØ%}%>%{рл%}° examples:*

* та000%>л0 examples:*

* мя%{дˮØ%}%>мд° examples:*

* мя0%>0т0 examples:*

* мя%{дˮØ%}%>д%{ая%} examples:*

* мя0%>та examples:*

* мя%{дˮØ%}%^SCSG2%>нась examples:*

* мя00%>тась examples:*

* тар%^PalVariation%{дˮØ%}%>%{рл%}° examples:*

* та000%>л0 examples:*

* тар%^PalVariation%{дˮØ%}%>мд%{ая%} examples:*

* тар00%>0та examples:*

* тар00%>0тя examples:*

RIGHT ARROW ONLY %{дˮØ%}:0

* тар%{дˮØ%}%>ми examples:*

* тарˮ%>ми examples:*

* тар0%>ми examples:*

* тар%{дˮØ%}%>ни examples:*

* тарˮ%>ни examples:*

* тар0%>ни examples:*

**С1:0 GlottalNonNasalToZERO**

* таС1%>мд° examples:*

* та0%>0т0 examples:*

* таС1%>д%{ая%} examples:*

* та0%>та examples:*

* ман°С1%>мд examples:*

* мана0%>0т examples:*

* ман°С1%>дмʼ examples:*

* мана0%>тмʼ examples:*

* таС1%^SCSG2%>нась examples:*

* та00%>тась examples:*

* ман°С1%^SCSG2%>нʼ examples:*

* мана00%>тʼ examples:*

**С1:ˮ UnderlyingToGlottal**

* ман°С1%>0в examples:*

* манаˮ%>ам examples:*

**%{дˮØ%}:ˮ UnderlyingToGlottal LEFT**

* мя%{дˮØ%}%>%{ауоэØ%}л examples:*

* мяˮ%>ал examples:*

* вар%{дˮØ%}%>вна examples:*

* варˮ%>мна examples:*

* тар%{дˮØ%} examples:*

* тарˮ examples:*

* тар%{дˮØ%} examples:*

* тарˮ examples:*

RIGHT ARROW ONLY %{дˮØ%}:ˮ

* тар%{дˮØ%}%>ми examples:*

* тарˮ%>ми examples:*

* тар0%>ми examples:*

* тар%{дˮØ%}%>ни examples:*

* тарˮ%>ни examples:*

* тар0%>ни examples:*

**%{нңʼØ%}:ʼ UnderlyingToGlottal**

**с => ц affrication after Stop**

* мя%{дˮØ%}%>сь examples:*

* мя0%>ць examples:*

* ман°С1%>сиˮ examples:*

* ман00%>циˮ examples:*

**с => з after nasal**

* му%{нңʼØ%}%>сь examples:*

* мун0%>зь examples:*

* ила%{йнңъʼØ%}%>сиˮ examples:*

* илан%>зиˮ examples:*

* ил°%{йнңъʼØ%}%>сиˮ examples:*

* ил0н%>зиˮ examples:*

* ңум%{йнңъʼØ%}%>сиˮ examples:*

* ңум0%>зиˮ examples:*

**v To m **

* ман°С1%>0в examples:*

* манаˮ%>ам examples:*

**%{рл%}:л**

* ман°С1%>0%{рл%} examples:*

* манаˮ%>ал examples:*

**%{рл%}:р**

**%{рл%}:р**

**0:а in single-syllable**
* *ман°С1%>0в*
* *манаˮ%>ам*
* *ңум%{йнңъʼØ%}%>0ць*
* *ңув0%>аць*
**°:а at end of stem**

* ед°%^SCSG2%>нʼ examples:*

* еда0%>нʼ examples:*

* ил°%{йнңъʼØ%}%>мʼ examples:*

* ила0%>мʼ examples:*

* ман°С1%>мд examples:*

* мана0%>0т examples:*

* ман°С1%>0%{рл%} examples:*

* манаˮ%>ал examples:*

* ман°С1%>0в examples:*

* манаˮ%>ам examples:*

* ман°С1%^SCSG2%>нʼ examples:*

* мана00%>тʼ examples:*

* ил°%{йнңъʼØ%}%>кʼ examples:*

* илаң%>гʼ examples:*

**ʼ:н**

Second Vowel Center
**°:у in Pros LEFT**

**ә:у in extra short to у**

**ә:о in extra short to о**

**ә:и in extra short to и**

**ә:ы in extra short to ы**

**ә:э in extra short to э**

**ә:а in extra short to а**

* ил°%{йнңъʼØ%}%>кәд examples:*

* ил0ң0гад examples:*

**0:а in Pros**

* ма%>ˮ0н examples:*

* ма0ˮан examples:*

* ма%>ˮ0м°н%{ая%} examples:*

* ма0ˮам0на examples:*

* ман°С1%>0%{рл%}° examples:*

* манаˮ0ал0 examples:*

* ман°С1%>0м° examples:*

* манаˮ0ам0 examples:*

* ман°С1%>0%{рл%}° examples:*

* манаˮ0ал0 examples:*

* ман°С1%>0м° examples:*

* манаˮ0ам0 examples:*

* хан%>м° examples:*

* хан0в0 examples:*

**0:э in Pros**

* ңэ%>ˮ0м°н%{ая%} examples:*

* ңэ0ˮэм0на examples:*

**0:о between two glottals**

* хо%>ˮ0м°н%{ая%} examples:*

* хо0ˮом0на examples:*

* я%^A2O%>ˮ0м°н%{ая%} examples:*

* ё00ˮом0на examples:*

**0:и after glottal**

* си%>ˮ0м°н%{ая%} examples:*

* си0ˮим0на examples:*

**0:ы between two glottals**

* ңы%>ˮ0м°н%{ая%} examples:*

* ңы0ˮым0на examples:*

**0:у between two glottals**

* ңу%>ˮ0м°н%{ая%} examples:*

* ңу0ˮум0на examples:*

**0:у between two glottals**

**а:я VowelPalatalization left**

**%{ая%}:я VowelPalatalization left**

**%{ая%}:я VowelPalatalization right**

* тар%^PalVariation%{дˮØ%}%>к°н%{ая%} examples:*

* тар000кана examples:*

* тар000кна examples:*

* тар000каня examples:*

* тар000кня examples:*

* тар%^PalVariation%{дˮØ%}%>д%{ая%} examples:*

* тар000та examples:*

* тар000тя examples:*

**%{оё%}:ё VowelPalatalization right**

* ню%>д%{оё%}ʼ examples:*

* ню0доʼ examples:*

* ню0дёʼ examples:*

* тар%^PalVariation%{дˮØ%}%>д%{оё%}ʼ examples:*

* тар000тоʼ examples:*

* тар000тёʼ examples:*

The rule **%{ауоэØ%} <-> у**:

* ну%>к%{ауоэØ%}рт examples:*

* ну0хурт examples:*

The rule **%{ауоэØ%} -> о**:

The rule **%{ауоэØ%} -> а**:

* намда%^VowLoss%>к%{ауоэØ%}в examples:*

* намд000хав examples:*

* мя%{дˮØ%}%>%{ауоэØ%}л examples:*

* мяˮ0ал examples:*

* му%{нңʼØ%}%>к%{ауоэØ%}на  examples:*

* муң0гана examples:*

* ед°%>к%{ауоэØ%}на examples:*

* ед00хана examples:*

**%{ауоэØ%} -> а**

**%{ауоэØ%} -> а**

* хо%>сеты%>к%{ауоэØ%}ʼ examples:*

* хо0сеты0хыʼ examples:*

**%{ауоэØ%} -> а**

* пя%^A2I%>ˮ%{ауоэØ%}н examples:*

* пи00ˮин examples:*

### VOWEL LOWERING

**i2e StemFinalYToE LEFT**

**а:э in stem-internal position**

* хадаба%^StemVowFronting%^A2I%>н examples:*

* хадэби000н examples:*

**a:o in я**

**a:i in мараңгы**

* яˮавла%^A2I%>дмʼ examples:*

* яˮавлы00дмʼ examples:*

**a:i in ңуда**

* ңуда%^A2I examples:*

* ңуди0 examples:*

* хадаба%^StemVowFronting%^A2I%>н examples:*

* хадэби000н examples:*

**о:у word-final position**

**я:и word-final position**

* пя%^A2I examples:*

* пи0 examples:*

* ңодя%^A2I examples:*

* ңоди0 examples:*

**я:е in яха**

* яха%^A2I examples:*

* еси0 examples:*

**а:у яˮавла:яˮавлу LEFT**

**а:у яˮавла:яˮавлу RIGHT**

* яˮавла%^VowRaise%>ˮ examples:*

* яˮавлу00ˮ examples:*

**а:ю яˮавла:яˮавлу**

* пэва%^VowFronting%^VowRaise%>ˮ examples:*

* пэбю000ˮ examples:*
### VOWEL LOSS

**а:ю яˮавла:яˮавлу**

**а:ю яˮавла:яˮавлу**

**я:0 Stem vowel loss in plural accusative**

* тёня%^PalLoss%^VowLoss examples:*

* тён000 examples:*

### CONSONANT CHANGES

**mToV**

* хан°%>м° examples:*

* хана0в0 examples:*

* хану0в0 examples:*

* ңум%{йнңъʼØ%}%>0ць examples:*

* ңув00аць examples:*

* ңум%{йнңъʼØ%}%>°мʼ examples:*

* ңув000мʼ examples:*

* ңум%^MLenition%>о examples:*

* ңув00о examples:*

**m loss before Labial followed by nonglottal cons or vows **

* му%{нңʼØ%}%>мд examples:*

* мун00д examples:*

* по%{йнңъʼØ%}%>мд° examples:*

* пон00д0 examples:*

* мя%{дˮØ%}%>мд° examples:*

* мя000т0 examples:*

* ңум%{йнңъʼØ%}%>м°н%{ая%} examples:*

* ңу000м0на examples:*

**н loss after glottal before д: **

* му%{нңʼØ%}%>нд examples:*

* мун00д examples:*

* по%{йнңъʼØ%}%>нд° examples:*

* пон00д0 examples:*

* мя%{дˮØ%}%>нд° examples:*

* мя000т0 examples:*

* ил°%{йнңъʼØ%}%>нд%{ая%} examples:*

* ил0н00да examples:*

* илан00да examples:*

**н loss after glottal before д: **
**r To l after nasal glottal**

* сыр%>рхавы examples:*

* сыл00хавы examples:*

**r To 0 before glottal and р or л**

* тар%^PalVariation%{дˮØ%}%>%{рл%}° examples:*

* та0000л0 examples:*

* сыр%>рхавы examples:*

* сыл00хавы examples:*

**n to t after non-nasal glottal**

* мя%{дˮØ%}%^SCSG2%>нʼ examples:*

* мя000тʼ examples:*

* ман°С1%^SCSG2%>нʼ examples:*

* мана000тʼ examples:*

* сыр%{йнңъʼØ%}%>нарахав examples:*

* сыр00тарахав examples:*

* мя%{дˮØ%}%^SCSG2%>нась examples:*

* мя000тась examples:*

* тар%^PalVariation%{дˮØ%}%^SCSG2%>нась examples:*

* тар0000тась examples:*

* ман°С1%^SCSG2%>н°ʼ examples:*

* мана000т0ʼ examples:*

**d to t after non-nasal glottal**

* мя%{дˮØ%}%>мд examples:*

* мя000т examples:*

* ман°С1%>мд examples:*

* мана000т examples:*

* мя%{дˮØ%}%>д%{ая%} examples:*

* мя00та examples:*

* мя%{дˮØ%}%>дмʼ examples:*

* мя00тмʼ examples:*

* тар%^PalVariation%{дˮØ%}%>д%{ая%} examples:*

* тар000та examples:*

* тар000тя examples:*

**b to p after non-nasal glottal**

* сырˮ%>бˮ examples:*

* сыр00пˮ examples:*

**ң:0 Before в:м +Sg+Acc+PxPl1:%>ваˮ**

* илң%>ваˮ examples:*

* ил00маˮ examples:*

The rule **ъ:0 with Conj after vowels**:

In the first context ...

In the second context ...

**ˮ:0**

* сырˮ%>бˮ examples:*

* сыр00пˮ examples:*

* сыр%^SCSG2%>накы examples:*

* сыр00такы examples:*
### Realization of glottal stops

#### SURFACE CONSONANT

**х:с in яха**

* яха%^A2I examples:*

* еси0 examples:*

**С1:с GlottalNonNasalToSurface**

* ман°С1%>°ць° examples:*

* ман0с0аць0 examples:*

**%{дˮØ%}:д GlottalNonNasalToSurface**

* мя%{дˮØ%}%>°ць° examples:*

* мя00аць0 examples:*

**%{дˮØ%}:д GlottalNonNasalToSurface**

**ь:0 with  GlottalNonNasalToZERO**

* * *

<small>This (part of) documentation was generated from [src/fst/morphology/phonology.twolc](https://github.com/giellalt/lang-yrk/blob/main/src/fst/morphology/phonology.twolc)</small>

---

## src-fst-morphology-root.lexc.md 


## Morphology
INTRODUCTION TO THE MORPHOLOGICAL ANALYSER OF NENETS

## Definitions for Multichar_Symbols

### Analysis symbols
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

### Symbols that need to be escaped on the lower side (towards twolc):
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
* **+RIGHT +MIDDLE**

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

### Morphophonology

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

### Triggers

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

## The Root lexicon

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

---

## src-fst-morphology-stems-verbs_newwords.lexc.md 

This is where new words are added as lexc entries before they are
added to the xml source files.
V_ "FinnishTRANSLATION" ;

CONTINUE BELOW

* * *

<small>This (part of) documentation was generated from [src/fst/morphology/stems/verbs_newwords.lexc](https://github.com/giellalt/lang-yrk/blob/main/src/fst/morphology/stems/verbs_newwords.lexc)</small>

---

## src-fst-phonetics-txt2ipa.xfscript.md 



retroflex plosive, voiceless			t`  ʈ	    0288, 648 (` = ASCII 096)
retroflex plosive, voiced			d`	ɖ		0256, 598
labiodental nasal					F 	ɱ		0271, 625
retroflex nasal						n` 	ɳ		0273, 627
palatal nasal						J 	ɲ		0272, 626
velar nasal							N 	ŋ		014B, 331
uvular nasal							N\	ɴ		0274, 628
	
bilabial trill						B\ 	ʙ		0299, 665
uvular trill							R\ 	ʀ		0280, 640
alveolar tap							4	ɾ		027E, 638
retroflex flap						r` 	ɽ		027D, 637
bilabial fricative, voiceless		p\ 	ɸ		0278, 632
bilabial fricative, voiced			B 	β		03B2, 946
dental fricative, voiceless			T 	θ		03B8, 952
dental fricative, voiced				D 	ð		00F0, 240
postalveolar fricative, voiceless	S	ʃ		0283, 643
postalveolar fricative, voiced		Z 	ʒ		0292, 658
retroflex fricative, voiceless		s` 	ʂ		0282, 642
retroflex fricative, voiced			z` 	ʐ		0290, 656
palatal fricative, voiceless			C 	ç		00E7, 231
palatal fricative, voiced			j\ 	ʝ		029D, 669
velar fricative, voiced	        	G 	ɣ		0263, 611
uvular fricative, voiceless			X	χ		03C7, 967
uvular fricative, voiced				R 	ʁ		0281, 641
pharyngeal fricative, voiceless		X\ 	ħ		0127, 295
pharyngeal fricative, voiced			?\ 	ʕ		0295, 661
glottal fricative, voiced			h\	ɦ		0266, 614

alveolar lateral fricative, vl.		K 
alveolar lateral fricative, vd.		K\

labiodental approximant				P (or v\) 
alveolar approximant					r\ 
retroflex approximant				r\` 
velar approximant					M\

retroflex lateral approximant		l` 
palatal lateral approximant			L 
velar lateral approximant			L\
Clicks

bilabial								O\	(O = capital letter) 
dental								|\
(post)alveolar						!\ 
palatoalveolar						=\ 
alveolar lateral						|\|\
Ejectives, implosives

ejective								_>	e.g. ejective p		p_>
implosive							_<	e.g. implosive b	b_<
Vowels

close back unrounded					M
close central unrounded 				1 
close central rounded				} 
lax i								I 
lax y								Y 
lax u								U

close-mid front rounded				2 
close-mid central unrounded			@\ 
close-mid central rounded			8 
close-mid back unrounded				7

schwa	ə							@

open-mid front unrounded				E 
open-mid front rounded				9
open-mid central unrounded			3 
open-mid central rounded				3\ 
open-mid back unrounded				V 
open-mid back rounded				O

ash (ae digraph)						{ 
open schwa (turned a)				6

open front rounded					& 
open back unrounded	        		A 
open back rounded					Q
Other symbols

voiceless labial-velar fricative		W 
voiced labial-palatal approx.		H 
voiceless epiglottal fricative		H\ 
voiced epiglottal fricative			<\ 
epiglottal plosive					>\

alveolo-palatal fricative, vl. 		s\ 
alveolo-palatal fricative, voiced	z\ 
alveolar lateral flap				l\ 
simultaneous S and x					x\ 
tie bar								_
Suprasegmentals

primary stress						" 
secondary stress						% 
long									: 
half-long							:\ 
extra-short							_X 
linking mark							-\
Tones and word accents

level extra high						_T 
level high							_H
level mid							_M 
level low							_L 
level extra low						_B
downstep								! 
upstep								^	(caret, circumflex)

contour, rising						 
contour, falling						_F 
contour, high rising					_H_T 
contour, low rising					_B_L 

contour, rising-falling				_R_F 
(NB Instead of being written as diacritics with _, all prosodic 
marks can alternatively be placed in a separate tier, set off 
by < >, as recommended for the next two symbols.)
global rise						<R> 
global fall						<F>
Diacritics						
									
voiceless						_0	(0 = figure), e.g. n_0
voiced							_v 
aspirated						_h 
more rounded						_O	(O = letter) 
less rounded						_c 
advanced							_+
retracted						_-
centralized						_" 
syllabic							=	(or _=) e.g. n= (or n_=) 
non-syllabic						_^ 
rhoticity						`
									
breathy voiced					_t 
creaky voiced					_k
linguolabial						_N 
labialized						_w 
palatalized						'	(or _j) e.g. t' (or t_j) 
velarized						_G 
pharyngealized					_?\
									
dental							_d 
apical							_a 
laminal							_m
nasalized						~	(or _~) e.g. A~ (or A_~) 
nasal release					_n
lateral release					_l 
no audible release				_}

velarized or pharyngealized		_e 
velarized l, alternatively		5 
raised							_r 
lowered							_o 
advanced tongue root				_A 
retracted tongue root			_q

* * *

<small>This (part of) documentation was generated from [src/fst/phonetics/txt2ipa.xfscript](https://github.com/giellalt/lang-yrk/blob/main/src/fst/phonetics/txt2ipa.xfscript)</small>

---

## src-fst-transcriptions-transcriptor-abbrevs2text.lexc.md 



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

<small>This (part of) documentation was generated from [src/fst/transcriptions/transcriptor-abbrevs2text.lexc](https://github.com/giellalt/lang-yrk/blob/main/src/fst/transcriptions/transcriptor-abbrevs2text.lexc)</small>

---

## src-fst-transcriptions-transcriptor-numbers-digit2text.lexc.md 


## File containing Nenets numerals to cyphers 

- HUNDREDSM ; = 200M
- 1:юрˮ HUNDREDM ; = 100M
- TENSM ; = 20-99M
- TEENSM ; = 10-19M
- 1MILJON ; = 1M
- ONESM ; = 1-9M
- 1GIGA ; = 1G
- ONESG ; = 1-9G
- HUNDREDST ; = 200000-999999
- 1:юрˮ HUNDREDT ; = 100000-100999
- TENST ; = 20000-99999,10000-10999
- TEENST ; = 11000-19999
- ONEST ; = 2000-9999
- 1:ёнарˮ% THOUSAND ; = 1000-1999
- ORD_THOUSAND ; = 
- ORD_HUNDREDS ; = 
- UNDERTHOUSAND ; =  100-999
- TENS ; =  20-99
- TEENS ; =  10-19
- ONES ; =  1-9

* * *

<small>This (part of) documentation was generated from [src/fst/transcriptions/transcriptor-numbers-digit2text.lexc](https://github.com/giellalt/lang-yrk/blob/main/src/fst/transcriptions/transcriptor-numbers-digit2text.lexc)</small>

---

## src-fst-transcriptions-transcriptor-symbols2text.lexc.md 



This file contains mappings from abbreviations and some acronyms to full
forms for text-to-speech purposes. This is a supplement to the analyser;
the analyser must tag the strings as +ABBR or similar for the transcriptions
to work. The resulting full form must be lemmas known to the analyser,
for further processing.

We describe here how abbreviations in Nenets are read out,
for text-to-speech systems.

The file contains:

- miscellaneous symbols

- smileys

- Clause boundary symbols

- Single punctuation marks

- Paired punctuation marks

* * *

<small>This (part of) documentation was generated from [src/fst/transcriptions/transcriptor-symbols2text.lexc](https://github.com/giellalt/lang-yrk/blob/main/src/fst/transcriptions/transcriptor-symbols2text.lexc)</small>

---

## tools-grammarcheckers-grammarchecker.cg3.md 


T U N D R A  N E N E T S  G R A M M A R   C H E C K E R

## DELIMITERS

## TAGS AND SETS

### Tags

This section lists all the tags inherited from the fst, and used as tags
in the syntactic analysis. The next section, **Sets**, contains sets defined
on the basis of the tags listed here, those set names are not visible in the output.

#### Beginning and end of sentence
BOS
EOS

#### Parts of speech tags

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
PPUNCT
PUNCT

COMMA
¶

#### Tags for POS sub-categories

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

#### Tags for morphosyntactic properties

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

#### Semantic tags

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

PROP-ATTR
PROP-SUR

TIME-N-SET

####  Syntactic tags

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

### Sets containing sets of lists and tags

This part of the file lists a large number of sets based partly upon the tags defined above, and
partly upon lexemes drawn from the lexicon.
See the sourcefile itself to inspect the sets, what follows here is an overview of the set types.

#### Sets for Single-word sets

INITIAL

#### Sets for word or not

WORD
NOT-COMMA

#### Case sets

ADLVCASE

CASE-AGREEMENT
CASE

NOT-NOM
NOT-GEN
NOT-ACC

#### Verb sets

NOT-V

#### Sets for finiteness and mood

REAL-NEG

MOOD-V

NOT-PRFPRC

#### Sets for person

SG1-V
SG2-V
SG3-V
DU1-V
DU2-V
DU3-V
PL1-V
PL2-V
PL3-V

#### Pronoun sets

#### Adjectival sets and their complements

#### Adverbial sets and their complements

#### Sets of elements with common syntactic behaviour

#### NP sets defined according to their morphosyntactic features

#### The PRE-NP-HEAD family of sets

These sets model noun phrases (NPs). The idea is to first define whatever can
occur in front of the head of the NP, and thereafter negate that with the
expression **WORD - premodifiers**.

#### Border sets and their complements

#### Grammarchecker sets

* * *

<small>This (part of) documentation was generated from [tools/grammarcheckers/grammarchecker.cg3](https://github.com/giellalt/lang-yrk/blob/main/tools/grammarcheckers/grammarchecker.cg3)</small>

---

## tools-tokenisers-tokeniser-disamb-gt-desc.pmscript.md 

## Tokeniser for yrk

Usage:
```
$ make
$ echo "ja, ja" | hfst-tokenise --giella-cg tokeniser-disamb-gt-desc.pmhfst
$ echo "Juos gorreválggain lea (dárbbašlaš) deavdit gáibádusa boasttu olmmoš, man mielde lahtuid." | hfst-tokenise --giella-cg tokeniser-disamb-gt-desc.pmhfst
$ echo "(gáfe) 'ja' ja 3. ja? ц jaja ukjend \"ukjend\"" | hfst-tokenise --giella-cg tokeniser-disamb-gt-desc.pmhfst
$ echo "márffibiillagáffe" | hfst-tokenise --giella-cg tokeniser-disamb-gt-desc.pmhfst
```

Pmatch documentation:
<https://github.com/hfst/hfst/wiki/HfstPmatch>

Characters which have analyses in the lexicon, but can appear without spaces
before/after, that is, with no context conditions, and adjacent to words:
* Punct contains ASCII punctuation marks
* The symbol after m-dash is soft-hyphen `U+00AD`
* The symbol following {•} is byte-order-mark / zero-width no-break space
`U+FEFF`.

Whitespace contains ASCII white space and
the List contains some unicode white space characters
* En Quad U+2000 to Zero-Width Joiner U+200d'
* Narrow No-Break Space U+202F
* Medium Mathematical Space U+205F
* Word joiner U+2060

Apart from what's in our morphology, there are
1. unknown word-like forms, and
2. unmatched strings
We want to give 1) a match, but let 2) be treated specially by
`hfst-tokenise -a`
Unknowns are made of:
* lower-case ASCII
* upper-case ASCII
* select extended latin symbols
* yrk cyrillics
ASCII digits
* select symbols
* Combining diacritics as individual symbols,
* various symbols from Private area (probably Microsoft),
so far:
* U+F0B7 for "x in box"

### Unknown handling
Unknowns are tagged ?? and treated specially with `hfst-tokenise`
hfst-tokenise --giella-cg will treat such empty analyses as unknowns, and
remove empty analyses from other readings. Empty readings are also
legal in CG, they get a default baseform equal to the wordform, but
no tag to check, so it's safer to let hfst-tokenise handle them.

Finally we mark as a token any sequence making up a:
* known word in context
* unknown (OOV) token in context
* sequence of word and punctuation
* URL in context

* * *

<small>This (part of) documentation was generated from [tools/tokenisers/tokeniser-disamb-gt-desc.pmscript](https://github.com/giellalt/lang-yrk/blob/main/tools/tokenisers/tokeniser-disamb-gt-desc.pmscript)</small>

---

## tools-tokenisers-tokeniser-gramcheck-gt-desc.pmscript.md 

## Grammar checker tokenisation for yrk

Requires a recent version of HFST (3.10.0 / git revision>=3aecdbc)
Then just:
```
$ make
$ echo "ja, ja" | hfst-tokenise --giella-cg tokeniser-disamb-gt-desc.pmhfst
```

More usage examples:
```
$ echo "Juos gorreválggain lea (dárbbašlaš) deavdit gáibádusa boasttu olmmoš, man mielde lahtuid." | hfst-tokenise --giella-cg tokeniser-disamb-gt-desc.pmhfst
$ echo "(gáfe) 'ja' ja 3. ja? ц jaja ukjend \"ukjend\"" | hfst-tokenise --giella-cg tokeniser-disamb-gt-desc.pmhfst
$ echo "márffibiillagáffe" | hfst-tokenise --giella-cg tokeniser-disamb-gt-desc.pmhfst
```

Pmatch documentation:
<https://github.com/hfst/hfst/wiki/HfstPmatch>

Characters which have analyses in the lexicon, but can appear without spaces
before/after, that is, with no context conditions, and adjacent to words:
* Punct contains ASCII punctuation marks
* The symbol after m-dash is soft-hyphen `U+00AD`
* The symbol following {•} is byte-order-mark / zero-width no-break space
`U+FEFF`.

Whitespace contains ASCII white space and
the List contains some unicode white space characters
* En Quad U+2000 to Zero-Width Joiner U+200d'
* Narrow No-Break Space U+202F
* Medium Mathematical Space U+205F
* Word joiner U+2060

Apart from what's in our morphology, there are
1) unknown word-like forms, and
2) unmatched strings
We want to give 1) a match, but let 2) be treated specially by hfst-tokenise -a
* select extended latin symbols
* select symbols
* various symbols from Private area (probably Microsoft),
so far:
* U+F0B7 for "x in box"

TODO: Could use something like this, but built-in's don't include šžđčŋ:

Simply give an empty reading when something is unknown:
hfst-tokenise --giella-cg will treat such empty analyses as unknowns, and
remove empty analyses from other readings. Empty readings are also
legal in CG, they get a default baseform equal to the wordform, but
no tag to check, so it's safer to let hfst-tokenise handle them.

Finally we mark as a token any sequence making up a:
* known word in context
* unknown (OOV) token in context
* sequence of word and punctuation
* URL in context

* * *

<small>This (part of) documentation was generated from [tools/tokenisers/tokeniser-gramcheck-gt-desc.pmscript](https://github.com/giellalt/lang-yrk/blob/main/tools/tokenisers/tokeniser-gramcheck-gt-desc.pmscript)</small>

---

## tools-tokenisers-tokeniser-tts-cggt-desc.pmscript.md 

## TTS tokenisation for smj

Requires a recent version of HFST (3.10.0 / git revision>=3aecdbc)
Then just:
```sh
make
echo "ja, ja" \
| hfst-tokenise --giella-cg tokeniser-disamb-gt-desc.pmhfst
```

More usage examples:
```sh
echo "Juos gorreválggain lea (dárbbašlaš) deavdit gáibádusa \
boasttu olmmoš, man mielde lahtuid." \
| hfst-tokenise --giella-cg tokeniser-disamb-gt-desc.pmhfst
echo "(gáfe) 'ja' ja 3. ja? ц jaja ukjend \"ukjend\"" \
| hfst-tokenise --giella-cg tokeniser-disamb-gt-desc.pmhfst
echo "márffibiillagáffe" \
| hfst-tokenise --giella-cg tokeniser-disamb-gt-desc.pmhfst
```

Pmatch documentation:
<https://kitwiki.csc.fi/twiki/bin/view/KitWiki/HfstPmatch>

Characters which have analyses in the lexicon, but can appear without spaces
before/after, that is, with no context conditions, and adjacent to words:
* Punct contains ASCII punctuation marks
* The symbol after m-dash is soft-hyphen `U+00AD`
* The symbol following {•} is byte-order-mark / zero-width no-break space
`U+FEFF`.

Whitespace contains ASCII white space and
the List contains some unicode white space characters
* En Quad U+2000 to Zero-Width Joiner U+200d'
* Narrow No-Break Space U+202F
* Medium Mathematical Space U+205F
* Word joiner U+2060

Apart from what's in our morphology, there are
1) unknown word-like forms, and
2) unmatched strings
We want to give 1) a match, but let 2) be treated specially by hfst-tokenise -a
* select extended latin symbols
* select symbols
* various symbols from Private area (probably Microsoft),
so far:
* U+F0B7 for "x in box"

TODO: Could use something like this, but built-in's don't include šžđčŋ:

Simply give an empty reading when something is unknown:
hfst-tokenise --giella-cg will treat such empty analyses as unknowns, and
remove empty analyses from other readings. Empty readings are also
legal in CG, they get a default baseform equal to the wordform, but
no tag to check, so it's safer to let hfst-tokenise handle them.

Needs hfst-tokenise to output things differently depending on the tag they get

* * *

<small>This (part of) documentation was generated from [tools/tokenisers/tokeniser-tts-cggt-desc.pmscript](https://github.com/giellalt/lang-yrk/blob/main/tools/tokenisers/tokeniser-tts-cggt-desc.pmscript)</small>
