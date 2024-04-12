# Nenets twol file

This file documents the [phonology.twolc file](http://github.com/giellalt/lang-yrk/blob/main/src/fst/phonology.twolc) 

## Letters of the alphabet
* **а б в г д е ё ж з и й к л м н ң о п р с т у ф х ц ч ш щ ъ ы ь э ю я** 
* **А Б В Г Д Е Ё Ж З И Й К Л М Н Ң О П Р С Т У Ф Х Ц Ч Ш Щ Ъ Ы Ь Э Ю Я** 

* **°:0** Directly from Tapani Salminen extra short vowel

* **ә:а** Directly from Tapani Salminen schwa

## Archiphonemes for vowels

* %{ауоэØ%}:а  А1:а А1:у А1:о А1:э SCHWA
* %{ауоэиыØ%}:0 before pros

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

* **%{аяуюØ%}:0** хан+N+Sg+Acc+PxSg1: ханув, ханав

* **%{увм%}:0** +N+Sg+Pros

* **%{вм%}:0** +N+Sg+Nom+PxSg1

## triggers

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

## Boundary symbols

*  %>      
hash

# Rules

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

## VOWEL LOWERING

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
## VOWEL LOSS

**а:ю яˮавла:яˮавлу**

**а:ю яˮавла:яˮавлу**

**я:0 Stem vowel loss in plural accusative**

* тёня%^PalLoss%^VowLoss examples:*

* тён000 examples:*

## CONSONANT CHANGES

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
## Realization of glottal stops

### SURFACE CONSONANT

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
