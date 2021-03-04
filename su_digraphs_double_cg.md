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
я - ja / ea - после согласных / jia - вместо ъя,  
ё - jo / eo - после согласных / jio - вместо ъё,  
ю - ju / eu - после согласных / jiu - вместо ъю,  
е - je / e - после согласных / ie - после согласных перед "оау" / jie - вместо ъе,  
и - i / iy - после согласных перед "э", после гласных в конце слова / y - после к,г и иногда после ц (cy,gy,czy),  

й - i - после гласных в конце слова (кроме ij) / ji - между согласными или когда нужен **йот, не смягчающий предыдущую согласную** / j - иначе,  
ъ - съ[еёюя] — sji[eoua] / qq - иначе,  
ь - сь[еэёоюяи] — sj[eeoouay] / сь[ау] — se[au] / ie - иначе,  
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
* кя/ckea, ча/cha, ца/cza (гя/ghea, жа/gza)
* мя/mea, меч/mech, лечь/lecie, ниц/nicz, рож/rogz, трожь/trogie, чиа/cia, чем/cem, географ/gaeograf, паникёр/panickeor, солнцеобразный/solnczieobraznyi, лучеобразно/lucieobrazno, цирк/czirc, цитолог/czytolog (исключение), отцы/otczy, полиэтилен/poliyetilen.

Allilujja, Jemen (исключение), съезд/sjiezd, месье/mesje, colyhanje, colyhanije, Cserocs, Csenija, taxi, exzema, exzecuczija, sex, saxofon, raep (исключение).
сьи/sjy сйи/sjiy, сйс/sjis, сьа/sea (force: siewa), сьйя/sjja, сйя/sjiia, сьйс/siejs, сейс/sejs.

Обратите внимание, что йот+твердая гласная (аоуэ) даёт мягкое звучание гласной (a => æ, o => ɵ, u => ʉ, ɛ => e, так пусть и ɨ => i будет). То есть, фонетика строится в предположении, что йы и йи звучат одинаково и в латинице обозначаются jy, чтобы быть согласованными с йотацией других гласных.


|       | и   | ы   | е   | [ёяю]    | [оау.]   | [еэ][оау] | иэ    | и[оау]   | э    | ь    | аббр. |
| ----- | --- | --- | --- | -------- | -------- | --------- | ----- | -------- | ---- | ---- | ----- |
| **ц** | czi | czy | cze | cze[oau] | cz[oau.] | czie[oau] | cziye | czi[oau] | czae | czie | Cz    |
| **ч** | ci  | chy | ce  | ce[oau]  | ch[oau.] | cie[oau]  | ciye  | ci[oau]  | chae | cie  | Ch    |
| **ж** | gi  | gzy | ge  | ge[oau]  | gz[oau.] | gie[oau]  | giye  | gi[oau]  | gzae | gie  | Gz    |
| **ш** | shi | shy | she | she[oau] | sh[oau.] | shie[oau] | shiye | shi[oau] | shae | shie | Sh    |
| **щ** | сч  |     |     |          |          |           |       |          |      |      | Sch   |

|       | и      | ы   | е   | э   | [ёяю]    | [оау.]  | ео   | эо    | иэ   | и[оау]  | ь    | аббр. |
| ----- | ------ | --- | --- | --- | -------- | ------- | ---- | ----- | ---- | ------- | ---- | ----- |
| **к** | cy/cki | cky | cke | cae | cke[oau] | c[oau.] | caeo | ckaeo | cye  | cy[oau] | ckie | C/Ck  |
| **г** | gy/ghi | ghy | ghe | gae | ghe[oau] | g[oau.] | gaeo | ghaeo | gye  | gy[oau] | ghie | G/Gh  |
| **с** | si     | sy  | se  | sae | se[oau]  | s[oau.] | sieo | saeo  | siye | si[oau] | sie  | S     |

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

Piony i vasiliecy vseo jesceo rastut na poleane vozle derevni Peony, scitajuscejsea bogatoi. V nei rodilsea izvestnyi pianist, perejehavshij v Siyetl na rabotu v companii "Moiy i tvoiy".

Pjanyi master po projectu sdelal mehanicescyi objiect s izjianom. Jesli brac ne obnarugitsea, to belyje bolidy bolieshe ne smogut vyigryvatie goncy.

V pjese pro devushcu v zeleonom platjycze vse sadilisie na ladjy i plyli po recke. No tut iz lesa vyshel Dgeordgz Maximus, conie v palieto i rvanyh dginsah, cotoryi chto-to vyiscyval, i pricazal vsem mytiesea i gotovitie buljon. Znacit snova pjom do lysyh acvalangystov.

Prepodobnyi Bajjes podcynul igralienyje costi. Vypalo shestie, znacit jemu prideotsea mazatie jod na ranu.

Maer nebolieshogo gorodishcy otcryl tabliczu exelea i vozmutilsea czenoi novogo excavatora. Agz exzema snova stala jego bespocoitie. Oh ugz eta pocupca vechnogo dvigatelea v proshlom godu! A tac ge pocupca aeroplana-ecranoleota. Jesli tac pojdeot i dalieshe, to beudgetu prideotsea hudo.

V etom vide fraza ot A do Ja nacinajet vygleadetie sovsem po-drugomu. Sejchas sceotca novaja, no pozge ona stanet staraja. Cernysh leubit cogda jego ceshut jeju. Jogz coleucij i pohogz na nejo.

Skhod mestnyh gitelei indijscoi derevni sickhov reshal chto ge delatie s otkhodami companii "Caligula Gai Julij Czezarie" (lat. ..Caligula Gaius Iulius Caesar). Odin iz prisutstvujuscih nosil hoholoc na golove. On i nasheol vyhod iz situaczii.

"Cto s mechom c nam prideot, tot ot mecha i..." - ne smog dogovoritie starshij mehanic Vasilij.

----

Leubimczem Biliebo byl junyi Frodo Baeggyns. Cogda Biliebo stucnulo deveanosto deveatie, on vdrug usynovil sirotu Frodo, sdelal svoim naslednicom i predlogil pereselitiesea v Zasumcy. Tut ugz vse nadegzdy Dericulie-Baeggynsov, davno s vogzdelenijem posmatrivavshih na usadiebu, ruhnuli oconchatelieno.

Sluchaju bylo ugodno, chtoby Biliebo s Frodo jesceo i rodilisie v odin denie, 22 senteabrea.

– Frodo, maliecic moi, – scazal cac-to raz Biliebo, – perebiralsea by ty co mne. Gleadishie, i denie rogzdenija vmeste otmechali by.

Frodo v tu poru hodil v dorostcah. Tac hobbity zovut molodeogie v bezotvetstvennom vozraste megzdu dvadczatju i tridczatju tremea, posle cego hobbit naconecz moget scitatie sebea vzroslym.

Proshlo jesceo dvenadczatie let. V Zasumcah cagzdyi god veselo otmechali dvojnoi denie rogzdenija, c etomu privycli, no leubomu bylo jasno, chto nyneshnei osenju gotovitsea nechto nieobychnoje. Biliebo ispolnealosie 111 let – vozrast dlea hobbita vesiema pochtennyi, da i cislo leubopytnoje, nu a Frodo gotovilsea otmetitie tridczatitreohletije – toge znamenatelienaja data – sovershennoletije po-hobbitscy.

----

Imejetsea nescolieco gypotez proiskhogzdenija sobacy, naiboleje verojatnymi jejo predcami scitajutsea volc i necotoryje vidy shacalov.

V sugzdenijah uceonyh o predcah domashnei sobacy prisutstvujut dve tochcy zrenija. Odni scitajut, chto sobacy - polifileticescaja gruppa (proiskhodeaschaja ot nescoliecyh predcov), drugyje pridergivajutsea mnenija, chto vse sobacy proizoshli ot odnogo predca (monofileticescaja tieorija).

----

Alexandr Pushcyn — Zimneje utro

Moroz i solncze; denie chudesnyi!  
Jesceo ty dremleshie, drug prelestnyi —  
Pora, crasavicza, prosnisie:  
Otcroi somcnuty negoi vzory  
Navstrechu severnoi Avrory,  
Zvezdoju severa javisie!  

Vechor, ty pomnishie, vjuga zlilasie,  
Na mutnom nebe mgla nosilasie;  
Luna, cac blednoje peatno,  
Scvozie tuci mrachnyje geltela,  
I ty pechalienaja sidela —  
A nynce… pogleadi v ocno:  

Pod golubymi nebesami  
Velicolepnymi covrami,  
Blestea na solncze, sneg legit;  
Prozrachnyi les odin cernejet,  
I jelie scvozie inei zelenejet,  
I rechca podo liedom blestit.  

Vsea comnata jantarnym blescom  
Ozarena. Veseolym trescom  
Trescit zatoplennaja pecie.  
Prijatno dumatie u legzancy.  
No znajeshie: ne veletie li v sancy  
Cobylcu buruju zaprecie?  

Scoliezea po utrennemu snegu,  
Drug milyi, predadimsea begu  
Netoroplivogo conea  
I navestim polea pustyje,  
Lesa, nedavno stolie gustyje,  
I bereg, milyi dlea menea.  

----

Lermontov M.Ju. — Rodina

Leubleu otciznu ja, no strannoju leubovju!  
Ne pobedit jejo rassudoc moi.  
Ni slava, cuplennaja crovju,  
Ni polnyi gordogo doverija pocoi,  
Ni teomnoi stariny zavetnyje predanja  
Ne sheveleat vo mne otradnogo mechtanja.  
No ja leubleu — za chto, ne znaju sam —  
Jejo stepei holodnoje molchanje,  
Jejo lesov bezbregznyh colyhanje,  
Razlivy rec jejo, podobnyje moream;  
Proseolochnym puteom leubleu scacatie v teleghe  
I, vzorom medlennym pronzaja noci tenie,  
Vstrechatie po storonam, vzdyhaja o nochleghe,  
Drogzascije ogni pechalienyh derevenie;  
Leubleu dymoc spaleonnoi gznivy,  
V stepi nochujuscij oboz  
I na holme sredie geoltoi nivy  
Cetu belejuscih bereoz.  
S otradoi, mnogym neznacomoi,  
Ja vigzu polnoje gumno,  
Izbu, pocrytuju solomoi,  
S reznymi stavneami ocno;  
I v prazdnic, vecerom rosistym,  
Smotretie do polnoci gotov  
Na pleascu s topanjem i svistom  
Pod govor pjanyh mugichcov.  

// God napisanija: 1841
