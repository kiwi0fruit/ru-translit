# Латиница Dual-ASCKIIWI-diacritic

Новая версия на основе [**предыдущей**](https://github.com/kiwi0fruit/ru-translit/blob/main/su_en.md). Являет собой дуальную ASCII-only и диакритическую версии, совместимые между собой. То есть, например, слово из ASCII версии будет значить тоже самое в диакритической версии. 

* Латиница обратимая,
* Сознательное исключение буквы Kk где возможно,
* Диакритическая версия подразумевает эргономичный ввод букв с помощью раскладки клавиатуры [US-International](https://en.wikipedia.org/wiki/US_international_keyboard#US-International),
* Запрет использования буквы Jj в конце слов.

*После слэша дано написание в ASCII-only версии. Требования этимологии распространяются только на основу слова.*

новые буквы: áäóöýÿúüéëíïôç

а - a,  
о - o,  
у - u,  
б - b,  
в - v,  
г - gh - в исключениях где этимология требует h (ghippopotam),  
г - g - обычно,  
д - d,  
ж - gz,  
л - l,  
м - m,  
н - n,  
п - p,  
р - r,  
с - s,  
т - t,  
ф - f,  
х - çh / kh - после согласных или где этимология требует ch или kh (sçhod, çhimera),  
х - h - обычно,  
ш - sh,  
ч - ch,  

я - á / ya - после согласных (sinája),  
я - á / ja - после и,й (Mariá, allilujá),  
я - ja - иначе,  
ё - eó / yo - после согласных (meód),  
ё - eó / jo - после и,й (mumieó),  
ё - jeó / jo - иначе (jeógz),  
ю - ú / yu - после согласных (lúbimyi),  
ю - ú / ju - после и,й (Juliú),  
ю - ju - иначе,  
е - e - после согласных (leto),  
е - é / je - после и,й (sinié, Bajés),  
е - je - иначе (Jevropa),  
и - í / yi - в конце слова после гласных кроме "и" (moí мои),  
ии - ii - в конце слова (bacterii),  
и - ý / yi - в исключениях где этимология требует "y" (sýstema),  
и - i - обычно,  
э - ae - после согласных (maer),  
э - e - обычно (etot),  
ае - äe /aae - после согласных (mäestro),  
ае - ae - обычно (aero),  

**Тут проблема со словообразованием, которое портит суффиксы. Возможно, оно же есть с КИ**  
ъ - съ[ёеюя] — sji[oeua],  
ъ - qh - иначе (obqhizvestié объизвестить),  
йи - sjií — сйи - после согласных (**jiippi, superjiippi**),  
йи - jí / jyi - иначе (rajíspolcom rajyispolcom),  
ь - сь[еюя] — sj[eua] (pjesa),  
ьи - сьи — sjí / sjyi (platjíce / platjyice, creslice),  
ьё - сьё — sjeó / sjo (pjeóm),  
ьо - сьо — jö /siio (buljön),  
ь - сь[ыэуа] — sí[yeua] / sii[yeua] (belíetagz),  
ь - é / j - после согласных (paléma),  
ь - qh - иначе (aqh аь),  
й - i - после гласных в конце слова (кроме ий - ij) (moi мой),  
ий - ij - в конце слова (sinij),  
й - **TODO: wj - перед гласными после согласных**,  
й - й[оыауэ] — j[öÿäüë] / ji[oyaue] - не после согласных (jöd, Majämi, ejën эйэн),  
й - j - иначе (allilujá, pojmal),  
*ji - йот, не смягчающий предыдущую согласную (диграф, две буквы, но один звук),*  
*j - смягчающий предыдущую согласную йот,*  
ы - y - после согласного звука (в т.ч. йота) и одновременно: перед согласным звуком (в т.ч. йотации) или в конце слова (ty, crasnyi, crasnyje),  
ы - y / yy - после согласного звука (в т.ч. йота) и одновременно: перед нейотированными гласными аоуиы (vyüchil / vyyuchil, vyïscyvaté, tyÿ тыы),  
ы - ÿ / yy - после согласного звука (в т.ч. йота) и одновременно: перед "э" (tÿe тыэ),  
ы - ÿ / yy - в остальных случаях (ÿdgzyd / yydgzyd ыджыд),    

з - z,  
з - sz - в исключениях где этимология требует "s",  
сз - ssz,  

к - c - обычно,  
к - c - обычно перед ц,  
кц - ctz - в словах, где этимология требует t,  
к - ck - перед еёюяьзч и иногда перед "и" (см. ниже),  
ктз - ckttz,  
кс - x - где этимология требует x, но только когда слово не начинается на кс/кз, и не на стыке морфем, 
кс - cs - иначе,  
кз - xz - где этимология требует x, но только когда слово не начинается на кс/кз, и не на стыке морфем,  
кз - ckz - иначе,
кк - ckk,  
кх - ckh,  
чч - cch,  
ки - cy - перед согласным звуком (в т.ч. йотации) или в конце слова,  
ки - cki - в остальных случаях,  

ц - cz - обычно,  
ц - tz - где этимология требует t (но не в начале слова),  
ц - ц[иеь] — с[ieé] / с[iej] - перед иеь,  
тз - tsz,  
цз - czsz,  
цц - czz,  

щ - sç / shch,  
шч - shéch / shjch,  
шьч - *не поддерживается*,  

Суть должно быть видно по этим примерам:

* ке/cke, че/ce, це/cze, ге/ghe, же/ge
* ки/cy, чи/ci, ци/czi, ги/gy, жи/gi
* кё/ckeo, чё/ceo, чо/cho, цо/czo, цё/czeo, гё/gheo, жё/geo, жо/gzo
* кя/ckia, ча/cha, ца/cza (гя/ghia, жа/gza) 
* мя/mia, меч/mech, лечь/leci, ниц/nicz, рож/rogz, трожь/trogi, чиа/ciya, чем/cem, географ/gaeograf, паникёр/panickeor, солнцеобразный/solnczieobraznyi, лучеобразно/lucieobrazno, цирк/czirc, цитолог/czytolog (исключение), отцы/otczy

Allilujja, Jemen (исключение), съезд/sjiezd, месье/mesje, colyhanje, colyhanije, Cserocs, Csenija, taxi, exzema, exzecuczija, sex, saxofon, raep (исключение), sszadi (сзади), otszyv (отзыв), militziá/militzija.  
сьи/sjy сйи/sjiy, сьйя/sjja, сйя/sjiia, сьйс/sjjis, сйс/sjis.

Обратите внимание, что йот+твердая гласная (аоуэ) даёт мягкое звучание гласной (a => æ, o => ɵ, u => ʉ, ɛ => e, так пусть и ɨ => i будет). То есть, фонетика строится в предположении, что йы и йи звучат одинаково и в латинице обозначаются jy, чтобы быть согласованными с йотацией других гласных.

|        |  и   |  ы    |  е   |  ё    |  [оау.]   |  ео    |  и[оауэ]    |  [яю]     |  э     |  ьс    |  ь.    |  с   | аббр. |
| ------ | ---- | ----- | ---- | ----- | --------- | ------ | ----------- | --------- | ------ | ------ | ------ | ---- | ----- |
| **ц**  | czi  | czy   | cze  | czeo  | cz[oau.]  | czieo  | cziy[oaue]  | czi[au]   | czae   | czjs   | czi.   | czs  | Cz    |
| **ж**  | gi   | gzy   | ge   | geo   | gz[oau.]  | gieo   | giy[oaue]   | gi[au]    | gzae   | gjs    | gi.    | gzs  | Gz    |
| **ш**  | shi  | shy   | she  | sheo  | sh[oau.]  | shieo  | shiy[oaue]  | shi[au]   | shae   | shjs   | shi.   | shs  | Sh    |
| **ч**  | ci   | chy   | ce   | ceo   | ch[oau.]  | cieo   | ciy[oaue]   | ci[au]    | chae   | cjs    | ci.    | chs  | Ch    |
| **щ**  | **sci** | **schy** | **sce** | **sceo** | sci[oau.] | **scieo** | **sciy[oaue]** | **schi[au]** | **schae** | **schjs** | **schi.** | scjs | Sch   |
| **сч** | schi | wschy | sche | scheo | **sch[oau.]** | schieo | schiy[oaue] | wschi[au] | wschae | wschjs | wschi. | **schs** | SCh   |

Жирным показан вариант, который будет стандартным после реформы орфограции.

|       | и      | ы   | е   | э   | ё    | [оау.c]  | [яю]    | ео   | эо    | и[оауэ]   | ьс   | ь.   | аббр. |
| ----- | ------ | --- | --- | --- | ---- | -------- | ------- | ---- | ----- | --------- | ---- | ---- | ----- |
| **к** | cy/cki | cky | cke | cae | ckeo | c[oau.s] | cki[au] | caeo | ckaeo | cy[oaue]  | ckjs | cki. | C/Ck  |
| **г** | gy/ghi | ghy | ghe | gae | gheo | g[oau.s] | ghi[au] | gaeo | ghaeo | gy[oaue]  | ghjs | ghi. | G/Gh  |
| **с** | si     | sy  | se  | sae | seo  | s[oau.s] | si[au]  | sieo | saeo  | siy[oaue] | sjs  | si.  | S     |

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

Piyony i vasiljcy vseo jesceo rastut na poliane vozle derevniy Peony, schitajuscejsia bogatoi. V nei rodilsia izvestnyi piyanist.

Pjanyi master po projectu sdelal mehanicescyi objiect s izjianom. Jesliy brac ne obnarugitsia, to belyje bolidy boljshe ne smogut vyigryvati goncy.

V pjese pro devushcu v zeleonom platjycze vse sadilisi na ladjy i plyliy po recke. No tut iz lesa vyshel Dgeordgz Maximus, coni v paljto i rvanyh dginsah, cotoryi chto-to vyiscyval, i pricazal vsem mytjsia i gotoviti bulion. Znacit snova pjom do lysyh acvalangystov.

Prepodobnyi Bajjes podcynul igraljnyje costiy. Vypalo shesti, znacit jemu prideotsia mazati jiod na ranu.

Maer neboljshogo gorodishcy otcryl tabliczu exelia i vozmutilsia czenoi novogo excavatora. Agz exzema snova stala jego bespocoiti. Oh ugz eta pocupca vechnogo dvigatelia v proshlom godu! A tac ge pocupca aeroplana-ecranoleota. Jesliy tac pojdeot i daljshe, to biudgetu prideotsia hudo.

V etom vide fraza ot A do Ja nacinajet vygliadeti sovsem po-drugomu. Sejchas sceotca novaja, no pozge ona stanet staraja. Cernysh liubit cogda jego ceshut jeju. Jogz coliucij i pohogz na nejo.

Skhod mestnyh gitelei indijscoi derevniy sickhov reshal chto ge delati s otkhodamiy companii "Caligula Gai Julij Czezari" (lat. ..Caligula Gaius Iulius Caesar). Odin iz prisutstvujuscih nosil hoholoc na golove. On i nasheol vyhod iz situaczii.

"Cto s mechom c nam prideot, tot ot mecha i..." - ne smog dogovoriti starshij mehanic Vasilij.

----

Liubimczem Biljbo byl junyi Frodo Baeggyns. Cogda Biljbo stucnulo devianosto deviati, on vdrug usynovil sirotu Frodo, sdelal svoim naslednicom i predlogil pereselitjsia v Zasumcy. Tut ugz vse nadegzdy Dericuli-Baeggynsov, davno s vogzdelenijem posmatrivavshih na usadjbu, ruhnuliy oconchateljno.

Sluchaju bylo ugodno, chtoby Biljbo s Frodo jesceo i rodilisi v odin deni, 22 sentiabria.

– Frodo, maljcic moi, – scazal cac-to raz Biljbo, – perebiralsia by ty co mne. Gliadishi, i deni rogzdenija vmeste otmechaliy by.

Frodo v tu poru hodil v dorostcah. Tac hobbity zovut molodeogi v bezotvetstvennom vozraste megzdu dvadczatju i tridczatju tremia, posle cego hobbit naconecz moget schitati sebia vzroslym.

Proshlo jesceo dvenadczati let. V Zasumcah cagzdyi god veselo otmechaliy dvojnoi deni rogzdenija, c etomu privycliy, no liubomu bylo jasno, chto nyneshnei osenju gotovitsia nechto nieobychnoje. Biljbo ispolnialosi 111 let – vozrast dlia hobbita vesjma pochtennyi, da i cislo liubopytnoje, nu a Frodo gotovilsia otmetiti tridczatitreohletije – toge znamenateljnaja data – sovershennoletije po-hobbitscy.

----

Imejetsia nescoljco gypotez proiskhogzdenija sobacy, naiboleje verojatnymiy jejo predcamiy schitajutsia volc i necotoryje vidy shacalov.

V sugzdenijah uceonyh o predcah domashnei sobacy prisutstvujut dve tochcy zrenija. Odniy schitajut, chto sobacy - polifileticescaja gruppa (proiskhodiasciaja ot nescoljcyh predcov), drugyje pridergivajutsia mnenija, chto vse sobacy proizoshliy ot odnogo predca (monofileticescaja tieorija).

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
Niy slava, cuplennaja crovju,  
Niy polnyi gordogo doverija pocoi,  
Niy teomnoi stariny zavetnyje predanja  
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


## Объединение ASCII-only и диакритической латиницы в одно целое с помощью локали и лигатур шрифтов

В современных шрифтах есть две функции:

1) языковая локаль, которая меняет отображение шрифта в зависимости от установленного на странице или фрагменте текста языка. Например, если здесь https://localfonts.eu/freefonts/bulgarian-cyrillic/source-serif-pro/ переключить на болгарскую локаль, то кириллический шрифт изменит начертание.  
2) лигатуры, которые способны менять начертания букв, когда те стоят рядом. Там же среди фрагментов текста можно выбрать "ff fi fl fj ffi ffl ffj", чтобы посмотреть на лигатуры в действии.

Представим, что у нас есть текст на русской латинице, содержащий вставки на английском, которые отмечены, что у них английский язык (уже в тэгах html).

И эта русская латиница является ASCII-only. Но с помощью современного шрифта со специальной русской локалью и лигатурами некоторые сочетания букв в ASCII-only тексте слепляются в диакритические.

В качестве примера для латиницы ASCKIIWI:

sae => sæ  
seo => sø  
jo => jø  
sjio => sj́ø  
ji => j́  
wj => j̋  
sia => sá, siu => sú, sie => sé  
siy. => sý. (кроме ciy,giy)  
iy => í  
sio => sįo, siia => sįa, siiu => sįu, siie => sįe, siiy => sįy (кроме scio, там sciio => scįo)  
skh => sκh  
caeo => ckéo, gaeo => ghéo  
cz => ç  
wsch => ṡch  

Диграфы согласных, скорее всего, трогать не стоит. Ибо иначе написание будет слишком разниться в ASCII и лигатурной версиях, а это не очень хорошо.


## Пример текста

Píony i vasiljcy vsø jescø rastut na poláne vozle derevný Pøny, schitajuscejsá bogatoi. V nei rodilsá izvestnyi píanist.

Pjanyi master po projectu sdelal mehanicescyi obj́ect s izj́anom. Jeslý brac ne obnarugitsá, to belyje bolidy boljshe ne smogut vyigryvati goncy.

V pjese pro devushcu v zelønom platjyçe vse sadilisi na ladjy i plylý po recke. No tut iz lesa vyshel Dgørdgz Maximus, coni v paljto i rvanyh dginsah, cotoryi chto-to vyiscyval, i pricazal vsem mytjsá i gotoviti bulįon. Znacit snova pjøm do lysyh acvalangystov.

Prepodobnyi Bajjes podcynul igraljnyje costý. Vypalo shesti, znacit jemu pridøtsá mazati j́od na ranu.

Mær neboljshogo gorodishcy otcryl tabliçu exelá i vozmutilsá çenoi novogo excavatora. Agz exzema snova stala jego bespocoiti. Oh ugz eta pocupca vechnogo dvigatelá v proshlom godu! A tac ge pocupca aeroplana-ecranoløta. Jeslý tac pojdøt i daljshe, to búdgetu pridøtsá hudo.

V etom vide fraza ot A do Ja nacinajet vygládeti sovsem po-drugomu. Sejchas scøtca novaja, no pozge ona stanet staraja. Cernysh lúbit cogda jego ceshut jeju. Jogz colúcij i pohogz na nejø.

Sκhod mestnyh gitelei indijscoi derevný sicκhov reshal chto ge delati s otκhodamý companii "Caligula Gai Julij Czezari" (lat. ..Caligula Gaius Iulius Caesar). Odin iz prisutstvujuscih nosil hoholoc na golove. On i nashøl vyhod iz situaçii.

"Cto s mechom c nam pridøt, tot ot mecha i..." - ne smog dogovoriti starshij mehanic Vasilij.

----

Lúbimçem Biljbo byl junyi Frodo Bæggyns. Cogda Biljbo stucnulo devánosto deváti, on vdrug usynovil sirotu Frodo, sdelal svoim naslednicom i predlogil pereselitjsá v Zasumcy. Tut ugz vse nadegzdy Dericuli-Bæggynsov, davno s vogzdelenijem posmatrivavshih na usadjbu, ruhnulý oconchateljno.

Sluchaju bylo ugodno, chtoby Biljbo s Frodo jescø i rodilisi v odin deni, 22 sentábrá.

– Frodo, maljcic moi, – scazal cac-to raz Biljbo, – perebiralsá by ty co mne. Gládishi, i deni rogzdenija vmeste otmechalý by.

Frodo v tu poru hodil v dorostcah. Tac hobbity zovut molodøgi v bezotvetstvennom vozraste megzdu dvadçatju i tridçatju tremá, posle cego hobbit naconeç moget schitati sebá vzroslym.

Proshlo jescø dvenadçati let. V Zasumcah cagzdyi god veselo otmechalý dvojnoi deni rogzdenija, c etomu privyclý, no lúbomu bylo jasno, chto nyneshnei osenju gotovitsá nechto néobychnoje. Biljbo ispolnálosi 111 let – vozrast dlá hobbita vesjma pochtennyi, da i cislo lúbopytnoje, nu a Frodo gotovilsá otmetiti tridçatitrøhletije – toge znamenateljnaja data – sovershennoletije po-hobbitscy.

----

Imejetsá nescoljco gypotez proisκhogzdenija sobacy, naiboleje verojatnymý jejø predcamý schitajutsá volc i necotoryje vidy shacalov.

V sugzdenijah ucønyh o predcah domashnei sobacy prisutstvujut dve tochcy zrenija. Odný schitajut, chto sobacy - polifileticescaja gruppa (proisκhodásciaja ot nescoljcyh predcov), drugyje pridergivajutsá mnenija, chto vse sobacy proizoshlý ot odnogo predca (monofileticescaja téorija).

----

Alexandr Pushcyn — Zimneje utro

Moroz i solnçe; deni chudesnyi!  
Jescø ty dremleshi, drug prelestnyi —  
Pora, crasaviça, prosnisi:  
Otcroi somcnuty negoi vzory  
Navstrechu severnoi Avrory,  
Zvezdoju severa javisi!  

Vechor, ty pomnishi, vjuga zlilasi,  
Na mutnom nebe mgla nosilasi;  
Luna, cac blednoje pátno,  
Scvozi tuciy mrachnyje geltela,  
I ty pechaljnaja sidela —  
A nynce… pogládý v ocno:  

Pod golubymý nebesamý  
Velicolepnymý covramý,  
Blestá na solnçe, sneg legit;  
Prozrachnyi les odin cernejet,  
I jeli scvozi inei zelenejet,  
I rechca podo ljdom blestit.  

Vsá comnata jantarnym blescom  
Ozarena. Vesølym trescom  
Trescit zatoplennaja peci.  
Prijatno dumati u legzancy.  
No znajeshi: ne veleti lý v sancy  
Cobylcu buruju zapreci?  

Scoljzá po utrennemu snegu,  
Drug milyi, predadimsá begu  
Netoroplivogo coná  
I navestim polá pustyje,  
Lesa, nedavno stoli gustyje,  
I bereg, milyi dlá mená.  

----

Lermontov M.Ju. — Rodina

Lúblú otciznu ja, no strannoju lúbovju!  
Ne pobedit jejø rassudoc moi.  
Ný slava, cuplennaja crovju,  
Ný polnyi gordogo doverija pocoi,  
Ný tømnoi stariny zavetnyje predanja  
Ne shevelát vo mne otradnogo mechtanja.  
No ja lúblú — za chto, ne znaju sam —  
Jejø stepei holodnoje molchanje,  
Jejø lesov bezbregznyh colyhanje,  
Razlivy rec jejø, podobnyje morám;  
Prosølochnym putøm lúblú scacati v teleghe  
I, vzorom medlennym pronzaja nociy teni,  
Vstrechati po storonam, vzdyhaja o nochleghe,  
Drogzascije ogný pechaljnyh dereveni;  
Lúblú dymoc spalønnoi gznivy,  
V stepý nochujuscij oboz  
I na holme sredi gøltoi nivy  
Cetu belejuscih berøz.  
S otradoi, mnogym neznacomoi,  
Ja vigzu polnoje gumno,  
Izbu, pocrytuju solomoi,  
S reznymý stavnámý ocno;  
I v prazdnic, vecerom rosistym,  
Smotreti do polnociy gotov  
Na pláscu s topanjem i svistom  
Pod govor pjanyh mugichcov.  

// God napisanija: 1841
