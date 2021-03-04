# Совлат англотранс с диграфами, двойными CG и без Kk

Новая версия на основе [**предыдущей**](https://github.com/kiwi0fruit/ru-translit/blob/main/su_en.md). Базируется на идеях совлата, англотранслитов с диграфами, двойного использования CG, минимизации Kk, умеренного использования Jj.

В качестве основных идей латиницы можно выделить:

* Сознательное исключение буквы Kk,
* Сознательное использование явной йотации буквы Ее для соответствия другим йотированным гласным.
* За основу был взят совлат,
* Который был переделан в ASCII-only версию без небуквенных символов,
* Xx для "ха" был сразу исключён,
* Особое внимание было уделено оптимизации частотных букв и сочетаний.
* Для этого пришлось использовать двойные C и G, а так же диграфы:
* Английские sh, ch, h/kh. Древнеримско-итальянский cz и, наконец, gz, очевидный в контексте cz и двойной G.
* Некоторое ограничение использования буквы Jj, особенно, в конце слов: ь/ie.

а - a,  
о - o,  
у - u,  
э - e / ae - после согласных,  
ы - y,  
я - ja / ia - после согласных / jia - вместо ъя,  
ё - jo / eo - после согласных / jio - вместо ъё,  
ю - ju / iu - после согласных / jiu - вместо ъю,  
е - je / e - после согласных / ie - после согласных перед "о" / jie - вместо ъе,  
и - i / iy - после согласных перед ауэ (но не "о") / y - после к,г и иногда после ц (cy,gy,czy),  

й - j / ji - между согласными или когда нужен **йот, не смягчающий предыдущую согласную**,  
ъ - съ[еёюя] -- sji[eoua] / qq - иначе,  
ь - j (в т.ч. сь[еёюяи] - sj[eouay]),  
ji - йот, не смягчающий предыдущую согласную (диграф, две буквы, но один звук), j - смягчающий предыдущую согласную йот,  

б - b,  
в - v,  
г - g / gh - перед еёюяьзж и иногда перед "и",  
д - d,  
ж - gz / g - перед еёиь,  
з - z,  
к - c / ck - перед еёюяьзчц и иногда перед "и",  
л - l,  
м - m,  
н - n,  
п - p,  
р - r,  
с - s,  
т - t,  
ф - f,  
х - h / kh - после согласных,  
ц - cz,  
ч - ch / c - перед еёиь,  
ш - sh,  
щ - sch / sc - перед еёиь,  

кео - caeo, кэо - ckaeo,  
гео - gaeo, гэо - ghaeo,  
сч - sch / sc - перед еёиь,  
кс - cs / x - иногда, но только когда слово не начинается на кс/кз, и не на стыке морфем,  
кз - ckz / xz - иногда, но только когда слово не начинается на кс/кз, и не на стыке морфем,  
кц - cts,  
ктс - ckts,  
цц - ccz,  
кк - cc / cck,  
йи - jy, сйи - sjiy,  
ьи - jy,  
кх - ckh.

Суть должно быть видно по этим примерам:

* ке/cke, че/ce, це/cze, ге/ghe, же/ge
* ки/cy, чи/ci, ци/czi, ги/gy, жи/gi
* кё/ckeo, чё/ceo, чо/cho, цо/czo, цё/czeo, гё/gheo, жё/geo, жо/gzo
* кя/ckia, ча/cha, ца/cza (гя/ghia, жа/gza) 
* мя/mia, меч/mech, лечь/lecj, ниц/nicz, рож/rogz, трожь/trogj, чиа/ciya, чем/cem, географ/gaeograf, паникёр/panickeor, солнцеобразный/solnczieobraznyj, лучеобразно/lucieobrazno, цирк/czirc, цитолог/czytolog (исключение), отцы/otczy

Allilujja, Jemen (исключение), съезд/sjiezd, месье/mesje, colyhanje, colyhanije, Cserocs, Csenija, taxi, exzema, exzecuczija, sex, saxofon, raep (исключение).  
сьи/sjy сйи/sjiy, сьйя/sjja, сйя/sjiia, сьйс/sjjis, сйс/sjis, сьа/sia (force: sjwa).

Обратите внимание, что йот+твердая гласная (аоуэ) даёт мягкое звучание гласной (a => æ, o => ɵ, u => ʉ, ɛ => e, так пусть и ɨ => i будет). То есть, фонетика строится в предположении, что йы и йи звучат одинаково и в латинице обозначаются jy, чтобы быть согласованными с йотацией других гласных.


|       | и   | ы   | е   | ё    | [оау.]   | [еэ]о | ио   | и[ауэ]    | [яю]     | э    | ь   | аббр. |
| ----- | --- | --- | --- | ---- | -------- | ----- | ---- | --------- | -------- | ---- | --- | ----- |
| **ц** | czi | czy | cze | czeo | cz[oau.] | czieo | czio | cziy[aue] | czi[au]  | czae | czj | Cz    |
| **ч** | ci  | chy | ce  | ceo  | ch[oau.] | cieo  | cio  | ciy[aue]  | ci[au]   | chae | cj  | Ch    |
| **ж** | gi  | gzy | ge  | geo  | gz[oau.] | gieo  | gio  | giy[aue]  | gi[au]   | gzae | gj  | Gz    |
| **ш** | shi | shy | she | sheo | sh[oau.] | shieo | shio | shiy[aue] | shi[au]  | shae | shj | Sh    |
| **щ** | сч  |     |     |      |          |       |      |           |          |      |     | Sch   |

|       | и      | ы   | е   | э   | ё    | [оау.]  | [яю]    | ео   | эо    | и[ауэ]   | ио  | ь   | аббр. |
| ----- | ------ | --- | --- | --- | ---- | ------- | ------- | ---- | ----- | -------- | --- | --- | ----- |
| **к** | cy/cki | cky | cke | cae | ckeo | c[oau.] | cki[au] | caeo | ckaeo | cy[aue]  | cyo | ckj | C/Ck  |
| **г** | gy/ghi | ghy | ghe | gae | gheo | g[oau.] | ghi[au] | gaeo | ghaeo | gy[aue]  | gyo | ghj | G/Gh  |
| **с** | si     | sy  | se  | sae | seo  | s[oau.] | si[au]  | sieo | saeo  | siy[aue] | sio | sj  | S     |

`che` значит тоже самое, что и `ce`, но никогда не используется. Аналогично с `chieo` и `cieo`.

**Про диграфы cz и gz**. Стоит отметить, что рукописная буква z выглядит либо как рукописная цифра 2 с угловатым верхом, либо как кириллическая рукописная "з" с хвостиком внизу, но более угловатая сверху. Когда z отдельно это смотрится нормально, а вот в диграфах cz и gz оба варианта написания z смотрятся плохо. В этом случае стоит использовать специальные рукописные лигатуры. Для cz - рукописная "ц" с петелькой, "c" идет в первую палку "ц", а "z" (вариант с петелькой) идет во вторую палку "ц" и петельку (заглавный вариант тоже должен выглядеть как рукописная "Ц"). Для gz - рукописная "g", к которой справа вплотную добавлена кириллическая буква "з" без петельки внизу (будто стяжка на правой дуге рукописной буквы "ф"). Заглавный вариант выглядит как рукописная "G", у которой внутренняя палочка является началом рукописной "z" (вариант с петелькой). Обе лигатуры легко писать и они имеют в себе логическую связь с составляющими их буквами.

**В аббревиатурах** следующие изменения по сравнению с предыдущим вариантом:

* всегда пишутся Ч/Ch, Ц/Cz, Ж/Gz, Ш/Sh, Я/JA, Е/JE, Ё/JO, Ю/JU, Й/J/JI, Э/E,
* перед "ЭИЫЙ,ЕЁЮЯ,З" в аббревиатурах используются К/Ck,Г/Gh (в общем, везде, где можно прочитать неправильно),
* после C,G,S или перед I (И) всегда писать Х/kH,
* передыдущая буква перед И/I пишется капсом,
* опционально можно сокращать Gh, Ck и kH до G', C', 'H.

ГЕ/GhJE/G'JE, ГЭ/GhE/G'E, ГИ/GHI/G'I, ГЫ/GhY/G'Y, ГЗ/GhZ/G'Z,  
ЖЕ/GzJE, ЖЭ/GzE, ЖИ/GZI, ЖЫ/GzY,  
КЕ/CkJE/C'JE, КЭ/CkE/C'E, КИ/CKI/C'I, КЫ/CkY/C'Y, КЗ/CkZ/C'Z,  
ГХ/GkH/G'H, ГЗ/GhZ/G'Z, КЗ/CkZ/C'Z, КХИ/CkHI/C'HI, НХ/NH, НХИ/NkHI/N'HI,  
СЧИ/SCHI, ЩИ/ScHI, СЧ/SCh, ЩУ/SchU,  
ЦИ/CZI, ЧИ/CHI, ШИ/SHI, СХИ/SkHI/S'HI, ЩИ/ScHI,  
ЙЭ/JIE, ЙИ/JII.

ЕГЭ/JEGhE/JEG'E, ОБЖ/OBGz, ЦПУ/CzPU, ЧС/ChS, США/SShA, ЭЭГ/EEG, ЖЭК/GzEC, ЖКХ/GzCkH/GzC'H, НХЛ/NHL, КХЛ/CkHL/C'HL, ЕКА/JECA, ФИЯ/FIJA, ЦЕРН/CZERN (исключение), ОБСЕ/OBSJE, ГИБДД/GHIBDD/G'IBDD, ЧИМ/CHIM.

Тут вводится специальное правило, что в аббревиатурах после строчных z,h,k нельзя писать заглавную i (I) - чтобы не путать со строчной L (l). Нельзя: ChI, ChII, ChIM. Нужно в качестве исключения писать CHI, CHII, CHIM.


## Пример текста

Piony i vasiljcy vseo jesceo rastut na poliane vozle derevni Peony, scitajuscejsia bogatoj. V nej rodilsia izvestnyj piyanist, perejehavshij v Siyetl na rabotu v companii "Moi i tvoi".

Pjanyj master po projectu sdelal mehanicescyj objiect s izjianom. Jesli brac ne obnarugitsia, to belyje bolidy boljshe ne smogut vyigryvatj goncy.

V pjese pro devushcu v zeleonom platjycze vse sadilisj na ladjy i plyli po recke. No tut iz lesa vyshel Dgeordgz Maximus, conj v paljto i rvanyh dginsah, cotoryj chto-to vyiscyval, i pricazal vsem mytjsia i gotovitj buljon. Znacit snova pjom do lysyh acvalangystov.

Prepodobnyj Bajjes podcynul igraljnyje costi. Vypalo shestj, znacit jemu prideotsia mazatj jod na ranu.

Maer neboljshogo gorodishcy otcryl tabliczu exelia i vozmutilsia czenoj novogo excavatora. Agz exzema snova stala jego bespocoitj. Oh ugz eta pocupca vechnogo dvigatelia v proshlom godu! A tac ge pocupca aeroplana-ecranoleota. Jesli tac pojdeot i daljshe, to biudgetu prideotsia hudo.

V etom vide fraza ot A do Ja nacinajet vygliadetj sovsem po-drugomu. Sejchas sceotca novaja, no pozge ona stanet staraja. Cernysh liubit cogda jego ceshut jeju. Jogz coliucij i pohogz na nejo.

Skhod mestnyh gitelej indijscoj derevni sickhov reshal chto ge delatj s otkhodami companii "Caligula Gaj Julij Czezarj" (lat. ..Caligula Gaius Iulius Caesar). Odin iz prisutstvujuscih nosil hoholoc na golove. On i nasheol vyhod iz situaczii.

"Cto s mechom c nam prideot, tot ot mecha i..." - ne smog dogovoritj starshij mehanic Vasilij.

----

Liubimczem Biljbo byl junyj Frodo Baeggyns. Cogda Biljbo stucnulo devianosto deviatj, on vdrug usynovil sirotu Frodo, sdelal svoim naslednicom i predlogil pereselitjsia v Zasumcy. Tut ugz vse nadegzdy Dericulj-Baeggynsov, davno s vogzdelenijem posmatrivavshih na usadjbu, ruhnuli oconchateljno.

Sluchaju bylo ugodno, chtoby Biljbo s Frodo jesceo i rodilisj v odin denj, 22 sentiabria.

– Frodo, maljcic moj, – scazal cac-to raz Biljbo, – perebiralsia by ty co mne. Gliadishj, i denj rogzdenija vmeste otmechali by.

Frodo v tu poru hodil v dorostcah. Tac hobbity zovut molodeogj v bezotvetstvennom vozraste megzdu dvadczatju i tridczatju tremia, posle cego hobbit naconecz moget scitatj sebia vzroslym.

Proshlo jesceo dvenadczatj let. V Zasumcah cagzdyj god veselo otmechali dvojnoj denj rogzdenija, c etomu privycli, no liubomu bylo jasno, chto nyneshnej osenju gotovitsia nechto nieobychnoje. Biljbo ispolnialosj 111 let – vozrast dlia hobbita vesjma pochtennyj, da i cislo liubopytnoje, nu a Frodo gotovilsia otmetitj tridczatitreohletije – toge znamenateljnaja data – sovershennoletije po-hobbitscy.

----

Imejetsia nescoljco gypotez proiskhogzdenija sobacy, naiboleje verojatnymi jejo predcami scitajutsia volc i necotoryje vidy shacalov.

V sugzdenijah uceonyh o predcah domashnej sobacy prisutstvujut dve tochcy zrenija. Odni scitajut, chto sobacy - polifileticescaja gruppa (proiskhodiaschaja ot nescoljcyh predcov), drugyje pridergivajutsia mnenija, chto vse sobacy proizoshli ot odnogo predca (monofileticescaja tieorija).

----

Alexandr Pushcyn — Zimneje utro

Moroz i solncze; denj chudesnyj!  
Jesceo ty dremleshj, drug prelestnyj —  
Pora, crasavicza, prosnisj:  
Otcroj somcnuty negoj vzory  
Navstrechu severnoj Avrory,  
Zvezdoju severa javisj!

Vechor, ty pomnishj, vjuga zlilasj,  
Na mutnom nebe mgla nosilasj;  
Luna, cac blednoje piatno,  
Scvozj tuci mrachnyje geltela,  
I ty pechaljnaja sidela —  
A nynce… pogliadi v ocno:

Pod golubymi nebesami  
Velicolepnymi covrami,  
Blestia na solncze, sneg legit;  
Prozrachnyj les odin cernejet,  
I jelj scvozj inej zelenejet,  
I rechca podo ljdom blestit.

Vsia comnata jantarnym blescom  
Ozarena. Veseolym trescom  
Trescit zatoplennaja pecj.  
Prijatno dumatj u legzancy.  
No znajeshj: ne veletj li v sancy  
Cobylcu buruju zaprecj?

Scoljzia po utrennemu snegu,  
Drug milyj, predadimsia begu  
Netoroplivogo conia  
I navestim polia pustyje,  
Lesa, nedavno stolj gustyje,  
I bereg, milyj dlia menia.

----

Lermontov M.Ju. — Rodina

Liubliu otciznu ja, no strannoju liubovju!  
Ne pobedit jejo rassudoc moj.  
Ni slava, cuplennaja crovju,  
Ni polnyj gordogo doverija pocoj,  
Ni teomnoj stariny zavetnyje predanja  
Ne sheveliat vo mne otradnogo mechtanja.  
No ja liubliu — za chto, ne znaju sam —  
Jejo stepej holodnoje molchanje,  
Jejo lesov bezbregznyh colyhanje,  
Razlivy rec jejo, podobnyje moriam;  
Proseolochnym puteom liubliu scacatj v teleghe  
I, vzorom medlennym pronzaja noci tenj,  
Vstrechatj po storonam, vzdyhaja o nochleghe,  
Drogzascije ogni pechaljnyh derevenj;  
Liubliu dymoc spaleonnoj gznivy,  
V stepi nochujuscij oboz  
I na holme sredj geoltoj nivy  
Cetu belejuscih bereoz.  
S otradoj, mnogym neznacomoj,  
Ja vigzu polnoje gumno,  
Izbu, pocrytuju solomoj,  
S reznymi stavniami ocno;  
I v prazdnic, vecerom rosistym,  
Smotretj do polnoci gotov  
Na pliascu s topanjem i svistom  
Pod govor pjanyh mugichcov.

// God napisanija: 1841


## Уменьшение вхождений j

V mojom testovom fragmente texta: 34 vkhogzdenij `\ce\W` (`e` posle soglasnyh na concze slov), 45 vkhogzdenij `\cj\W` (`j` posle soglasnyh na concze slov), 28 vkhogzdenij `\ci\W` (`i` posle soglasnyh na concze slov), 37 vkhogzdenij `[eyuoa]j\W`, 0 vkhogzdenij `[eyuoa]i\W`. Gde `\c` - eto soglasnaja `[rtpsdfghklzxcvbnm]`. V russcoj versii testovogo fragmenta 231 bucva `[Аа]` i 213 bucv `[Тт]`. Otnoshenije `Тт` c `Аа` iz https://ru.wikipedia.org/wiki/Частотность ravniajetsia 0.782. A eto ge otnoshenije v testovom fragmente - 0.922. To jestj, text ne samyj srednestatistichnyj... No vseo ravno budem ispoljzovatj jego.

`\ce\W`  
34 / 231 = e1[%] / 8.01[%] => e1 = 1.179%  
34 / 213 = e2[%] / 6.26[%] => e2 = 0.999%  
=> ~1.09%

`\cj\W`  
45 / 231 = j1[%] / 8.01[%] => j1 = 1.560%  
45 / 213 = j2[%] / 6.26[%] => j2 = 1.323%  
=> ~1.44%

`\ci\W`  
28 / 231 = i1[%] / 8.01[%] => i1 = 0.971%  
28 / 213 = i2[%] / 6.26[%] => i2 = 0.823%  
=> ~0.90%

Zamenitj na concze slov `\cj` na `\ce` (a `\ce` na `\cie`) budet stoitj ~1.09% digrafnyh poterj.  
Jesli ge zameniatj prosto `\cj` na `\cie`, to digrafnyje poteri budut ~1.44% (da i eto budet meneje logychno).  
A zamenitj na concze slov `\cj` na `\ci` (a `\ci` na `\ciy`) budet stoitj ~0.90% digrafnyh poterj.


## Пример текста с уменьшенным вхождением j

Piony i vasiljcy vseo jesceo rastut na poliane vozle derevniy Peony, scitajuscejsia bogatoi. V nei rodilsia izvestnyi piyanist.

Pjanyi master po projectu sdelal mehanicescyi objiect s izjianom. Jesliy brac ne obnarugitsia, to belyje bolidy boljshe ne smogut vyigryvati goncy.

V pjese pro devushcu v zeleonom platjycze vse sadilisi na ladjy i plyliy po recke. No tut iz lesa vyshel Dgeordgz Maximus, coni v paljto i rvanyh dginsah, cotoryi chto-to vyiscyval, i pricazal vsem mytjsia i gotoviti buljon. Znacit snova pjom do lysyh acvalangystov.

Prepodobnyi Bajjes podcynul igraljnyje costiy. Vypalo shesti, znacit jemu prideotsia mazati jod na ranu.

Maer neboljshogo gorodishcy otcryl tabliczu exelia i vozmutilsia czenoi novogo excavatora. Agz exzema snova stala jego bespocoiti. Oh ugz eta pocupca vechnogo dvigatelia v proshlom godu! A tac ge pocupca aeroplana-ecranoleota. Jesliy tac pojdeot i daljshe, to biudgetu prideotsia hudo.

V etom vide fraza ot A do Ja nacinajet vygliadeti sovsem po-drugomu. Sejchas sceotca novaja, no pozge ona stanet staraja. Cernysh liubit cogda jego ceshut jeju. Jogz coliucij i pohogz na nejo.

Skhod mestnyh gitelei indijscoi derevniy sickhov reshal chto ge delati s otkhodamiy companii "Caligula Gai Julij Czezari" (lat. ..Caligula Gaius Iulius Caesar). Odin iz prisutstvujuscih nosil hoholoc na golove. On i nasheol vyhod iz situaczii.

"Cto s mechom c nam prideot, tot ot mecha i..." - ne smog dogovoriti starshij mehanic Vasilij.

----

Liubimczem Biljbo byl junyi Frodo Baeggyns. Cogda Biljbo stucnulo devianosto deviati, on vdrug usynovil sirotu Frodo, sdelal svoim naslednicom i predlogil pereselitjsia v Zasumcy. Tut ugz vse nadegzdy Dericuli-Baeggynsov, davno s vogzdelenijem posmatrivavshih na usadjbu, ruhnuliy oconchateljno.

Sluchaju bylo ugodno, chtoby Biljbo s Frodo jesceo i rodilisi v odin deni, 22 sentiabria.

– Frodo, maljcic moi, – scazal cac-to raz Biljbo, – perebiralsia by ty co mne. Gliadishi, i deni rogzdenija vmeste otmechaliy by.

Frodo v tu poru hodil v dorostcah. Tac hobbity zovut molodeogi v bezotvetstvennom vozraste megzdu dvadczatju i tridczatju tremia, posle cego hobbit naconecz moget scitati sebia vzroslym.

Proshlo jesceo dvenadczati let. V Zasumcah cagzdyi god veselo otmechaliy dvojnoi deni rogzdenija, c etomu privycliy, no liubomu bylo jasno, chto nyneshnei osenju gotovitsia nechto nieobychnoje. Biljbo ispolnialosi 111 let – vozrast dlia hobbita vesjma pochtennyi, da i cislo liubopytnoje, nu a Frodo gotovilsia otmetiti tridczatitreohletije – toge znamenateljnaja data – sovershennoletije po-hobbitscy.

----

Imejetsia nescoljco gypotez proiskhogzdenija sobacy, naiboleje verojatnymiy jejo predcamiy scitajutsia volc i necotoryje vidy shacalov.

V sugzdenijah uceonyh o predcah domashnei sobacy prisutstvujut dve tochcy zrenija. Odniy scitajut, chto sobacy - polifileticescaja gruppa (proiskhodiaschaja ot nescoljcyh predcov), drugyje pridergivajutsia mnenija, chto vse sobacy proizoshliy ot odnogo predca (monofileticescaja tieorija).

----

Alexandr Pushcyn — Zimneje utro

Moroz i solncze; deni chudesnyi!  
Jesceo ty dremleshi, drug prelestnyi —  
Pora, crasavicza, prosnisi:  
Otcroi somcnuty negoi vzory  
Navstrechu severnoi Avrory,  
Zvezdoju severa javisi!  

Vechor, ty pomnishi, vjuga zlilasi,  
Na mutnom nebe mgla nosilasi;  
Luna, cac blednoje piatno,  
Scvozi tuciy mrachnyje geltela,  
I ty pechaljnaja sidela —  
A nynce… pogliadiy v ocno:  

Pod golubymiy nebesamiy  
Velicolepnymiy covramiy,  
Blestia na solncze, sneg legit;  
Prozrachnyi les odin cernejet,  
I jeli scvozi inei zelenejet,  
I rechca podo ljdom blestit.  

Vsia comnata jantarnym blescom  
Ozarena. Veseolym trescom  
Trescit zatoplennaja peci.  
Prijatno dumati u legzancy.  
No znajeshi: ne veleti liy v sancy  
Cobylcu buruju zapreci?  

Scoljzia po utrennemu snegu,  
Drug milyi, predadimsia begu  
Netoroplivogo conia  
I navestim polia pustyje,  
Lesa, nedavno stoli gustyje,  
I bereg, milyi dlia menia.  

----

Lermontov M.Ju. — Rodina

Liubliu otciznu ja, no strannoju liubovju!  
Ne pobedit jejo rassudoc moi.  
Ni slava, cuplennaja crovju,  
Ni polnyi gordogo doverija pocoi,  
Ni teomnoi stariny zavetnyje predanja  
Ne sheveliat vo mne otradnogo mechtanja.  
No ja liubliu — za chto, ne znaju sam —  
Jejo stepei holodnoje molchanje,  
Jejo lesov bezbregznyh colyhanje,  
Razlivy rec jejo, podobnyje moriam;  
Proseolochnym puteom liubliu scacati v teleghe  
I, vzorom medlennym pronzaja nociy teni,  
Vstrechati po storonam, vzdyhaja o nochleghe,  
Drogzascije ogniy pechaljnyh dereveni;  
Liubliu dymoc spaleonnoi gznivy,  
V stepiy nochujuscij oboz  
I na holme sredi geoltoi nivy  
Cetu belejuscih bereoz.  
S otradoi, mnogym neznacomoi,  
Ja vigzu polnoje gumno,  
Izbu, pocrytuju solomoi,  
S reznymiy stavniamiy ocno;  
I v prazdnic, vecerom rosistym,  
Smotreti do polnociy gotov  
Na pliascu s topanjem i svistom  
Pod govor pjanyh mugichcov.  

// God napisanija: 1841
