# ru-translit (kiwi0fruit's)

### Uniquely reversible and lossless: Russian to English transliteration (no extra letters, diacritics and non-letters) together with dual romanization of Russian (russkaya latinica) with extended alphabet (Ęę,...)

### Однозначно обратимые и без потерь: транслитерация из русского в английский алфавит (без дополнительных букв, диакритических и небуквенных знаков) и дуальная русская латиница на основе этого транслита с расширенным алфавитом (Ęę,...)

Придумал в качестве развлечения ещё один транслит. Моими новшествами являются: обратимое без потерь кодирование й,ъ,ы,ь через j,y. А так же кодирование э через ae. В остальном взял лучшее из уже существующего.

Развлечением было удовлетворить ограничениям:

* Транслит - полностью обратимый (является кодировкой без потерь и позволяет точно восстановить произвольный русский текст из латиницы). То есть, это [**инъективное отображение**](https://ru.wikipedia.org/wiki/%D0%98%D0%BD%D1%8A%D0%B5%D0%BA%D1%86%D0%B8%D1%8F_(%D0%BC%D0%B0%D1%82%D0%B5%D0%BC%D0%B0%D1%82%D0%B8%D0%BA%D0%B0)),
* Транслит содержит только буквы (в частности, не использует апостроф): отображение из русских букв `[А-Яа-я]` в английские `[A-Za-z]` без добавлений,
* Не содержит далёких фонетических замен типа щ → w. Желательно, чтобы "звучало" похоже на английский или математический латинский.

Когда составлял правила хотелось, чтобы:

* х в контекстах, где её нельзя перепутать с составными буквами, кодировалась h, а иначе – kh,
* j после согласных означала ь, а в остальных случаях – й или йот,
* ы кодировалась как y.
* ъe/ъя в разрешённых русским языком местах кодировались je/ja,
* ьe/ья в типичных местах кодировались jye/jya,
* ыe/ыя в типичных местах кодировались yje/yja,
* э кодировалась как ae.
* в остальных случаях е/я кодировались e/ya,
* нетипичное использование русских букв можно было закодировать контекстно-независимыми обозначения типа й/jj, ы/yy, ъ/jhjh, ь/jh,
* НО, в итоге из-за логики кодирования й,ъ,ы,ъ пришлось е кодировать как ye кроме случаев после согласных - там "e". А э кодировать как "e", кроме случаев после согласной - там ae.


## Кириллица <=> латиница

Главной целью проекта была обратимая транслитерация в английский алфавит, близкая к английскому чтению. Латиница с диакритическими знаками является простой, но стилистически однородной, производной от транслитерации.

| **a** | **б** | **в** | **г** | **д** | **з** | **к** | **л** | **м** |
|:-----:|:-----:|:-----:|:-----:|:-----:|:-----:|:-----:|:-----:|:-----:|
| a     | b     | v     | g     | d     | z     | k     | l     | m     |
| **н** | **о** | **п** | **р** | **с** | **т** | **у** | **ф** | **ц** |
| n     | o     | p     | r     | s     | t     | u     | f     | c     |

Краткая версия (шч и ьь - технические замены для обратимости):

| **е**   | **ё** | **ж** | **и**   | **й** | **х** | **ч**   | **ш**   | **щ**   | 
|:-------:|:-----:|:-----:|:-------:|:-----:|:-----:|:-------:|:-------:|:-------:|
| е/ye/je | yo/jo | zh    | i/yi/ji | j/jj  | h/kh  | ch      | sh      | shch    |
| е/ję    | ë     | ž     | i/į     | j/ĵ   | h     | č       | š       | šč      |
| **ъ**   | **ы** | **ь** | **э**   | **ю** | **я** | **экс** | **шч**  | **ьь**  |
| j/jhjh  | y/yy  | j/jh  | ae/e    | yu/ju | ya/ja | ex      | shwch   | jhwjh   |
| j/ɉ     | y     | j/ʝ   | ę       | ų     | ą     | ęx      | šwč     | ʝʝ      |

Подробнее:

| **е/сье/ые/съе/^e/[аяй]e** | **ё/сьё/ыё/съё** | **и/сьи/сыи/аыи/съи** |
|:---------------------:|:----------------:|:-------------------:|
| e/sjye/yje/sje/^ye/ye | yo/sjyo/yjo/sjo  | i/sjyi/syi/ayyi/sji |
| e/sje/ye/sję/^e/e     | ë/sjë/yë/sjo     | i/sjį/syi/ayi/sji   |
| **ю/сью/ыю/съю**      | **я/сья/ыя/съя** | **э/^э/экс**        |
| yu/sjyu/yju/sju       | ya/sjya/yja/sja  | ae/^e/ex            |
| ų/sjų/yų/sju          | ą/sją/yą/sja     | ę/^ę/ęx             |

| **й/сй/ыйа** | **съе/ъ/съи** | **ы/ые/ы/ыи** | **ь/сье/ь/сьи** |
|:------------:|:-------------:|:-------------:|:---------------:|
| j/sjj/yjja   | sje/jhjh/sji  | y/yje/yy/yi   | j/sjye/jh/sjyi  |
| j/sĵ/yĵa     | sje/ɉ/sji     | y/ye/y/yi     | j/sje/ʝ/sjį     |

Многие буквы совпадают с [ГОСТ 16876-71 табл. 2](https://ru.wikipedia.org/wiki/%D0%A2%D1%80%D0%B0%D0%BD%D1%81%D0%BB%D0%B8%D1%82%D0%B5%D1%80%D0%B0%D1%86%D0%B8%D1%8F_%D1%80%D1%83%D1%81%D1%81%D0%BA%D0%BE%D0%B3%D0%BE_%D0%B0%D0%BB%D1%84%D0%B0%D0%B2%D0%B8%D1%82%D0%B0_%D0%BB%D0%B0%D1%82%D0%B8%D0%BD%D0%B8%D1%86%D0%B5%D0%B9#%D0%A1%D1%80%D0%B0%D0%B2%D0%BD%D0%B8%D1%82%D0%B5%D0%BB%D1%8C%D0%BD%D0%B0%D1%8F_%D1%82%D0%B0%D0%B1%D0%BB%D0%B8%D1%86%D0%B0_%D1%81%D0%B8%D1%81%D1%82%D0%B5%D0%BC_%D1%82%D1%80%D0%B0%D0%BD%D1%81%D0%BB%D0%B8%D1%82%D0%B5%D1%80%D0%B0%D1%86%D0%B8%D0%B8) или [ГОСТ 7.79-2000 сист. Б](https://ru.wikipedia.org/wiki/%D0%A2%D1%80%D0%B0%D0%BD%D1%81%D0%BB%D0%B8%D1%82%D0%B5%D1%80%D0%B0%D1%86%D0%B8%D1%8F_%D1%80%D1%83%D1%81%D1%81%D0%BA%D0%BE%D0%B3%D0%BE_%D0%B0%D0%BB%D1%84%D0%B0%D0%B2%D0%B8%D1%82%D0%B0_%D0%BB%D0%B0%D1%82%D0%B8%D0%BD%D0%B8%D1%86%D0%B5%D0%B9#%D0%A1%D1%80%D0%B0%D0%B2%D0%BD%D0%B8%D1%82%D0%B5%D0%BB%D1%8C%D0%BD%D0%B0%D1%8F_%D1%82%D0%B0%D0%B1%D0%BB%D0%B8%D1%86%D0%B0_%D1%81%D0%B8%D1%81%D1%82%D0%B5%D0%BC_%D1%82%D1%80%D0%B0%D0%BD%D1%81%D0%BB%D0%B8%D1%82%D0%B5%D1%80%D0%B0%D1%86%D0%B8%D0%B8).

Алфавит транслитерации состоит из **24+1** букв (английский алфавит без Qq. А Ww нужна для неестественных сочетаний). Основной расширенный алфавит для латиницы с диакритикой состоит из **32+4** букв (английский алфавит без Qq, плюс Ąą,Čč,Ëë,Ęę,Įį,Šš,Ųų,Žž,Ĵĵ, Ɉɉ, Ʝʝ. А Ĵĵ, Ɉɉ, Ʝʝ, Ww нужны для неестественных сочетаний). Все буквы поддерживаются клавиатурой Google, кроме зачеркнутой и вьющейся j (Ɉɉ, Ʝʝ), используемых для обозначения ъ и ь в неестественных позициях.

***Слово на латинице является грамматически верным если:***

1. его образ от прообраза совпадает с самим словом (`lat_word == RUtoEN(ENtoRU(lat_word))`),
2. его прообраз грамматически верен (`ENtoRU(lat_word)`).

Так же нужно специальное правило для аббревиатур: АЭС/AES/AĘS, АЕС/AES, ФМШ/FMS, ЭЮЯ/EUA/ĘUA, ЁМ/EM/ËM.
То есть, использовать не модификатор а модифицируемую букву (отбросить диакритический знак в латинице). Так же не стоит забывать, что все слова с буквой ё могут быть корректно написаны с буквой е, так что ë/yo становятся Ë/E в качестве общего знаменателя.

*Латиница с диакритикой станет удобной только при наличии удобных програмных средств ввода. Для мобильных устройств: словаря для swipe-клавиатуры, в которой все главные буквы основного расширенного алфавита расположены отдельно (в том же порядке, что и для декстопа). Ww доступна только в английской клавиатуре. А редкие варианты спрятаны в более частые варианты, x спрятана в ę). Для десктопа скорее всего придется переиспользовать именно русскую раскладку - нужно, чтобы одновременно были доступны все буквы. Например, вот такую*:

| ё ĵ |     |     |     | ; ʝ | % Ʝ |     |     |     |         |     |     |         | = ɉ     |
| ---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:-------:|:---:|:---:|:-------:|:-------:|
|     | й j | ц c | у u | к k | е e | н n | г g | ш š | **щ ë** | з z | х h | **ъ x** | **\ į** |
|     | ф f | ы y | в v | а a | п p | р r | о o | л l | д d     | ж ž | э ę |         |         |
|     |     | я ą | ч č | с s | м m | и i | т t | ь j | б b     | ю ų | . , |         |         |



## Примеры текстов в транслитерации

*По-моему, это вариант гораздо лучше подходит для русско-английских билингвов, чем вариант с диакритическими знаками.*

Pjyanyj master po proektu sdelal mehanicheskij objekt s izjanom. Yesli brak ne obnaruzhitsya, to belyj bolid boljshe ne smozhet vyigryvatj gonki.

V pjyese pro devushku v zelyonom platjyice vse sadilisj na ladjyi i plyli po reke. No tut iz lesa vyshel konj v paljto i prikazal vsem mytjsya.

Prepodobnyj Bajyes podkinul igraljnyje kosti. Vypalo shestj, znachit yemu pridyotsya mazatj jod na ranu.

Maer neboljshogo gorodishki otkryl tablicu exelya i vozmutilsya cenoj novogo exkavatora. Azh ekzema snova stala yego bespokoitj. Oh uzh eta pokupka vechnogo dvigatelya v proshlom godu! A tak zhe pokupka aeroplana-ekranolyota. Yesli tak pojdyot i daljshe, to byudzhetu pridyotsya hudo.

V etom vide fraza ot A to Ya nachinayet vyglyadetj sovsem po-drugomu. Sejchas shchyotka novaya, no pozzhe ona stanet staraya. Chernysh lyubit kogda yego cheshut yeyu. Yozh kolyuchij i pohozh na neyo.

Skhod mestnyh zhytelej indijskoj derevni sikkhov reshal chto zhe delatj s otkhodami kompanii "The LLC". Odin iz prisutstvuyushchih nosil hoholok na golove. On i nashyol vyhod iz situacii.

"Kto s mechom k nam pridyot, tot ot mecha i..." - ne smog dogovoritj starshij mehanik Vasilij.

Imeetsya neskoljko gipotez proiskhozhdeniya sobaki, naibolee veroyatnymi yeyo predkami schitayutsya volk i nekotoryje vidy shakalov.

V suzhdeniyah uchyonyh o predkah domashnej sobaki prisutstvuyut dve tochki zreniya. Odni schitayut, chto sobaki - polifileticheskaya gruppa (proiskhodyashchaya ot neskoljkih predkov), drugie priderzhivayutsya mneniya, chto vse sobaki proizoshli ot odnogo predka (monofileticheskaya teoriya).


## Примеры текстов на латинице

Pjyanyj master po proektu sdelal mehanicheskij obɉekt s izɉyanom. Esli brak ne obnaruzhitsja, to belyj bolid boljshe ne smozhet vyigryvatj gonki.

V pjese pro devushku v zelënom platjyice vse sadilisj na ladjyi i plyli po reke. No tut iz lesa vyshel konj v paljto i prikazal vsem mytjsja.

Prepodobnyj Bajes podkinul igraljnye kosti. Vypalo shestj, znachit emu pridëtsja mazatj jod na ranu.

Męr neboljshogo gorodishki otkryl tablicu ęxelja i vozmutilsja cenoj novogo ęxkavatora. Azh ękzema snova stala ego bespokoitj. Oh uzh ęta pokupka vechnogo dvigatelja v proshlom godu! A tak zhe pokupka aęroplana-ękranolëta. Esli tak pojdët i daljshe, to bjudzhetu pridëtsja hudo.

V ętom vide fraza ot A do Ya nachinaet vygljadetj sovsem po-drugomu. Sejchas sçhëtka novaya, no pozzhe ona stanet staraya Chernysh ljubit kogda ego cheshut eyu. Ëzh koljuchij i pohozh na neë.

Skhod mestnyh zhytelej indijskoj derevni sikkhov reshal chto zhe delatj s othodami kompanii "The LLC". Odin iz prisutstvuyusçhih nosil hoholok na golove. On i nashël vyhod iz situacii.

"Kto s mechom k nam pridët, tot ot mecha i..." - ne smog dogovoritj starshij mehanik Vasilij.

Imeetsja neskoljko gipotez proishozhdeniya sobaki, naibolee veroyatnymi eë predkami schitayutsja volk i nekotorye vidy shakalov.

V suzhdeniyah uchënyh o predkah domashnej sobaki prisutstvuyut dve tochki zreniya. Odni schitayut, chto sobaki - polifileticheskaya gruppa (proishodjasçhaya ot neskoljkih predkov), drugie priderzhivayutsja mneniya, chto vse sobaki proizoshli ot odnogo predka (monofileticheskaya teoriya).


## Кириллица => латиница

Пока что это только зачатки двух алгоритмов прямого и обратного пребразования.

### Таблица No.1 (сложные составные: й,ъ,ы,ь=>j,y)

`\c` - согласная (consonant), но не йот. Специальный символ регулярных выражений для `[qwrtpsdfghklzxcvbnmцкнгшщзхфвпрлджчсмтб]` (но без й, j).

|     | Cyrillic RegEx | Latin RegEx | Примеры                                      |
| --------- | --------------:|:----- | -------------------------------------------- |
| ъе/je, ъё/jo, ъи/ji, ъю/ju, ъя/ja | `(?<=\c)ъ[еёюяи]` | `(?<=\c)j[eouai]` | об**ъе**кт/ob**je**kt/ob**ję**kt, из**ъя**н/iz**ja**n, м**е**ра/m**e**ra, **е**сли/**ye**sli/**e**sli, з**я**ка/z**ya**ka/z**ą**ka, Мур**ъи**н/Mur**ji**n |
| ъ/jhjh/ɉ  | `ъ`           | `jhjh` | он**ъ**/on**jhjh**/on**ɉ**, Му**ъ**минат/Mu**jhjh**minat/Mu**ɉ**minat, Чан**ъ**ань/Chan**jhjh**anj/Čan**ɉ**anj, Мур**ъйи**н/Mur**jhjhji**n/Mur**ɉji**n |
| | | | |
| ье/jye/je, ьё/jyo/jë, ьи/jyi/jį, ью/jyu/jų, ья/jya/ją | `(?<=\c)ь[еёюяи]` | `(?<=\c)jy[eouai]` | п**ье**са/p**jye**sa/p**je**sa, п**ья**н/p**jya**n/p**ją**n, лад**ьи**/lad**jyi**/lad**jį**, плат**ьи**це/plat**jyi**ce/plat**jį**ce, Мур**ьи**н/Mur**jyi**n/Mur**jį**n |
| ь/j               | `(?<=\c)ь(?![эоуaйы])` | `(?<=\c)j` | пряч**ь**ся/pryach**j**sya/prąč**j**są, мыт**ь**ся/myt**j**sya/myt**j**są, кон**ь**/kon**j** |
| ь/jh/ʝ    | `ь`            | `jh`  | Чан**ь**ол/Сhan**jh**ol/Čan**ʝ**ol, Мур**ьй**ин/Mur**jhj**in/Mur**ʝj**in, Чан**ь**ын/Сhan**jh**yn/Čan**ʝ**yn |
| | | | |
| ые/yje/ye, ыё/yjo/yë, ыю/yju/yų, ыя/yja/yą | `(?<!ы)ы[еёюя]` | `yj[eoua]` | бел**ые**/bel**yje**/bel**ye**, бедн**ыя**/bedn**yja**/bedn**yą** |
| ые/yyje/ye, ыё/yyjo/yë, ыю/yyju/yų, ыя/yyja/yą | `(?<=ы)ы[еёюя]` | `yyj[eoua]` | ы**ые**/yy**yyje**/y**ye** |
| ы/yy/y    | `ы(?=[эоуаы])` | `yy`  | **ы**а/**yy**a/**y**a, **ы**я/**y**ja/**y**ą |
| ы/yy/y    | `(?<=ы)ы`      | `yy`  | **ыы**/**yyyy**/**yy**                       |
| ыи/yyi/yi | `(?<![й\c])ыи` | `yyi` | а**ыи**/a**yyi**/a**yi**                     |
| ыи/yi/yi  | `(?<=[й\c])ыи` | `yi`  | в**ыи**грывать/v**yi**gryvatj, в**ыи**скивать/v**yi**skivatj |
| ы/y       | `ы`            | `y`   | кр**ы**ска/kr**y**ska, **ы**пся/**y**psya/**y**psą, п**ы**хтел/p**y**htel, бел**ы**й/bel**y**j, в**ы**йигрывать/v**y**jigryvatj/v**y**jigryvatj, ба**й**ыс/ba**j**ys |
| | | | |
| й/jj/ĵ    | `(?<=[й\c])й`  | `jj`  | **йй**/**jjjj**/**ĵĵ**, под**й**езд/pod**jj**yezd/pod**ĵ**ezd, под**й**од/pod**jj**od/pod**ĵ**od, Мур**й**ин/Mur**jj**in/Mur**ĵ**in |
| й/jj/ĵ    | `й(?=й)`       | `jj`  | **йй**/**jjjj**/**ĵĵ** |
| й/jj/ĵ | `(?<=ы)й(?=[эоуа])` | `jj` | белы**й**а/bely**jj**a/bely**ĵ**a, белы**й**е/bely**jj**ye/bely**ĵ**e, **й**эс/**jj**es/**ĵ**ęs |
| й/j       | `й`            | `j`   | ба**й**ес/ba**j**yes/ba**j**es, белы**й**/bely**j**, **й**од/**j**od, **й**иппи/**j**ippi, ба**й**ас/ba**j**as, ба**й**яс/ba**j**yas/ba**j**ąs, баян/bayan/baąn |


### Таблица No.2 (простые составные)

|        | Cyrillic RegEx | Latin RegEx   | Примеры                                                                            |
| ------ | --------------:|:------------- | ---------------------------------------------------------------------------------- |
| е/ye/e | `(?<=[аяй])е`  | `ye`          | бай**е**с/baj**ye**s/baj**e**s, Ра**е**вская/Ra**ye**vskaya/Ra**e**vskaą, зя**е**/zya**ye**/zą**e**, за**е**м/za**ye**m/za**e**m, заём/zayom/zaëm |
| е/ye/e | `^е`           | `ye`          | **е**сли/**ye**sli/**e**sli, **е**хо/**ye**ho/eho                                  |
| е/e    | `е`            | `e`           | м**е**х/m**e**h, про**е**кт/pro**e**kt, за**е**зд/za**e**zd                        |
| экс/ex/ęx | `экс`       | `ex`          | **экс**каватор/**ex**kavator/**ęx**kavator, **экс**ель/**ex**elj/**ęx**elj, м**экс**/m**ex**/m**ęx**, экзамен/ekzamen/ękzamen, экзема/ekzema/ękzema, Мексика/Meksika, мех/meh |
| э/e/ę | `^э`&#124;`(?<=[аяй])э` | `e`   | **эх**о/**eh**o/**ęh**o, а**э**роплан/a**e**roplan/a**ę**roplan, **э**тот/**e**tot/**ę**tot, **э**он/**e**on/**ę**on, **э**кран/**e**kran/**ę**kran, **э**ротика/**e**rotika/**ę**rotika |
| э/ae/ę | `э`            | `ae`          | м**э**р/m**ae**r/m**ę**r, мер/mer, Но**э**ль/No**ae**lj/No**ę**lj, радио**э**хо/radio**ae**ho/radio**ę**ho, ма**э**р/ma**ae**r/ma**ę**r, в**эч**ный/v**aech**nyj/v**ęč**nyj, й**э**с/jj**ae**s/ĵ**ę**s |
| | | | |
| шч/shwch/šwč | `шч`     | `shwch`       | **шч**ётка/**shwch**yotka/**šwč**ëtka                                              |
| щ/shch/šč    | `щ`      | `shch`        | **щ**ётка/**shch**yotka/**šč**ëtka, **cч**ёт/**sch**yot/**sč**ët                   |
| ж/zh/ž | `ж`            | `zh`          | ё**ж**/yo**zh**/ë**ž**, во**зж**и/vo**zzh**i/vo**zž**i, по**зж**е/po**zž**e        |
| ч/ch/č | `ч`            | `ch`          | **ч**ерныш/**ch**ernysh/**č**ernyš, с**ч**ётная/s**ch**yotnaya/s**č**ëtnaą         |
| ш/sh/š | `ш`            | `sh`          | **ш**лем/**sh**lem/**š**lem                                                        |
| х/kh/ĥ | `(?=[хтсшзжцчщъьйк])х` | `kh` | с**х**од/s**kh**od/s**h**od, **кх**е/**kkh**e/**kh**e, си**кх**/si**kkh**/si**kh**, ме**х**/me**h**/me**h**, Муръ**х**ин/Murjhjh**kh**in/Murɉ**h**in, Мурь**х**ин/Murj**kh**in/Murj**h**in, от**х**од/ot**kh**od/ot**h**od |
| х/h    | `х`            | `h`           | **х**о**х**олок/**h**o**h**olok, в**ы**ход/v**y**hod, ме**х**а/me**h**a, э**х**о/e**h**o, вече/veche/veče, меча/mecha/meča, эч/ech/ęč, мэч/maech/męč, **х**ья/**h**jya/**h**ją, **х**ьан/**h**jhan/**h**ʝan |
| | | | |
| ё/yo/ë | `ё`            | `yo`          | **ё**мко/**yo**mko/**ë**mko, м**ё**д/m**yo**d/m**ë**d                              |
| ю/yu/ų | `ю`            | `yu`          | **Ю**ля/**Yu**lya/**Ų**lą                                                          |
| я/ya/ą | `я`            | `ya`          | Из**я**/Iz**ya**/Iz**ą**                                                           |
| ERROR  |                | `[qwx]`       |                                                                                    |


### Таблица No.3

| Cyr | Lat | Cyr | Lat |
| ---:|:--- | ---:|:--- |
| `а` | `a` | `м` | `m` |
| `б` | `b` | `н` | `n` |
| `в` | `v` | `о` | `o` |
| `г` | `g` | `п` | `p` |
| `д` | `d` | `р` | `r` |
|     |     | `с` | `s` |
| `з` | `z` | `т` | `t` |
|     |     | `у` | `u` |
| `и` | `i` | `ф` | `f` |
| `й` | `j` | `х` | `h` |
| `к` | `k` | `ц` | `c` |
| `л` | `l` | `ы` | `y` |


## TO DO

* [ ] Написать кодировщик и декодировщик на питоне, а потом проверить на каком-нибудь словаре, а так же на случайно-сгенерированных словах. Я не проверял алгоритм декодирования даже мысленно. Но интуитивно чувствую, что он хорошо определён и реализуем. Собственно, алгоритм кодировки строился такой, чтобы не было такого, чтобы разные русские слова (любые) отображались в одну и ту же транслитерацию.
* [ ] Попробовать сделать фильтр pandoc. Но там надо посмотреть какой элемент гарантированно содержит только голый текст.
* [ ] Сделать режим, в котором просто все русские обособленные слова преобразуются в массиве текста.
* [ ] Оформить в виде модуля питона с CLI.
* [ ] Написать инструкцию как сконвертировать произвольную страницу в интернете с помощью сохранения как html и конвертации фильтром/пандоком.
* [ ] Попробовать сделать однострочный джавастрипт, которым можно перевести любую уже открытую страницу в интернете.


[latin capital letter j with stroke, latin small letter dotless j, latin small letter dotless j with stroke U+025F](https://en.wikipedia.org/wiki/List_of_Unicode_characters), [List of Latin-script letters](https://en.wikipedia.org/wiki/List_of_Latin-script_letters).
