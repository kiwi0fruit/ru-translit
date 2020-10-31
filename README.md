# ru-translit (kiwi0fruit's)

### Uniquely reversible and lossless: Russian to English transliteration (no extra letters, diacritics and non-letters) together with dual romanization of Russian (russkaya latinica) with extended alphabet (Êê,Žž,...)

### Однозначно обратимые и без потерь: транслитерация из русского в английский алфавит (без дополнительных букв, диакритических и небуквенных знаков) и дуальная русская латиница на основе этого транслита с расширенным алфавитом (Êê, Žž,...)

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
| е/ê     | ô     | ž     | i/î     | j/ĵ   | h     | č       | š       | šč      |
| **ъ**   | **ы** | **ь** | **э**   | **ю** | **я** | **экс** | **шч**  | **ьь**  |
| j/jhjh  | y/yy  | j/jh  | ae/e    | yu/ju | ya/ja | ex      | shwch   | jhwjh   |
| j/ɉɉ    | y     | j/ɉ   | ę       | û     | â     | ęx      | šwč     | ɉwɉ     |

Подробнее:

| **е/сье/ые/съе/^e/[аяй]e** | **ё/сьё/ыё/съё** | **и/сьи/сыи/аыи/съи** |
|:---------------------:|:----------------:|:-------------------:|
| e/sjye/yje/sje/^ye/ye | yo/sjyo/yjo/sjo  | i/sjyi/syi/ayyi/sji |
| e/sjê/yê/sje/^ê/ê     | ô/sjô/yô/sjo     | i/sjî/syi/aŷi/sji   |
| **ю/сью/ыю/съю**      | **я/сья/ыя/съя** | **э/^э/экс**        |
| yu/sjyu/yju/sju       | ya/sjya/yja/sja  | ae/^e/ex            |
| û/sjû/yû/sju          | â/sjâ/yâ/sja     | ę/^e/ex             |

| **й/сй/ыйа** | **съе/ъ/съи** | **ы/ые/ы/ыи** | **ь/сье/ь/сьи** |
|:------------:|:-------------:|:-------------:|:---------------:|
| j/sjj/yjja   | sje/jhjh/sji  | y/yje/yy/yi   | j/sjye/jh/sjyi  |
| j/sĵ/sĵa     | sje/ɉɉ/sji    | y/yê/y/yi     | j/sjê/ɉ/sjî     |

Многие буквы совпадают с [ГОСТ 16876-71 табл. 2](https://ru.wikipedia.org/wiki/%D0%A2%D1%80%D0%B0%D0%BD%D1%81%D0%BB%D0%B8%D1%82%D0%B5%D1%80%D0%B0%D1%86%D0%B8%D1%8F_%D1%80%D1%83%D1%81%D1%81%D0%BA%D0%BE%D0%B3%D0%BE_%D0%B0%D0%BB%D1%84%D0%B0%D0%B2%D0%B8%D1%82%D0%B0_%D0%BB%D0%B0%D1%82%D0%B8%D0%BD%D0%B8%D1%86%D0%B5%D0%B9#%D0%A1%D1%80%D0%B0%D0%B2%D0%BD%D0%B8%D1%82%D0%B5%D0%BB%D1%8C%D0%BD%D0%B0%D1%8F_%D1%82%D0%B0%D0%B1%D0%BB%D0%B8%D1%86%D0%B0_%D1%81%D0%B8%D1%81%D1%82%D0%B5%D0%BC_%D1%82%D1%80%D0%B0%D0%BD%D1%81%D0%BB%D0%B8%D1%82%D0%B5%D1%80%D0%B0%D1%86%D0%B8%D0%B8) или [ГОСТ 7.79-2000 сист. Б](https://ru.wikipedia.org/wiki/%D0%A2%D1%80%D0%B0%D0%BD%D1%81%D0%BB%D0%B8%D1%82%D0%B5%D1%80%D0%B0%D1%86%D0%B8%D1%8F_%D1%80%D1%83%D1%81%D1%81%D0%BA%D0%BE%D0%B3%D0%BE_%D0%B0%D0%BB%D1%84%D0%B0%D0%B2%D0%B8%D1%82%D0%B0_%D0%BB%D0%B0%D1%82%D0%B8%D0%BD%D0%B8%D1%86%D0%B5%D0%B9#%D0%A1%D1%80%D0%B0%D0%B2%D0%BD%D0%B8%D1%82%D0%B5%D0%BB%D1%8C%D0%BD%D0%B0%D1%8F_%D1%82%D0%B0%D0%B1%D0%BB%D0%B8%D1%86%D0%B0_%D1%81%D0%B8%D1%81%D1%82%D0%B5%D0%BC_%D1%82%D1%80%D0%B0%D0%BD%D1%81%D0%BB%D0%B8%D1%82%D0%B5%D1%80%D0%B0%D1%86%D0%B8%D0%B8).

Алфавит транслитерации состоит из **25** букв (английский алфавит без Qq. А Ww нужна для неестественных сочетаний). Основной расширенный алфавит для латиницы без диграфов состоит из **36** букв (английский алфавит без Qq, плюс Ââ,Čč,Ęę,Êê,Îî,Ĵĵ,Ôô,Šš,Ûû,Žž,Ɉɉ. А Ww нужна для неестественных сочетаний). Из диакритических знаков для естественных русских языковых конструкций используются только [циркумфлекс](https://ru.wikipedia.org/wiki/%D0%A6%D0%B8%D1%80%D0%BA%D1%83%D0%BC%D1%84%D0%BB%D0%B5%D0%BA%D1%81), [гачек](https://ru.wikipedia.org/wiki/%D0%93%D0%B0%D1%87%D0%B5%D0%BA) и [ę – типичное сокращение для ae](https://ru.wikipedia.org/wiki/%C3%86_%28%D0%BB%D0%B0%D1%82%D0%B8%D0%BD%D0%B8%D1%86%D0%B0%29). Все буквы поддерживаются клавиатурой Google, кроме зачеркнутой j (Ɉɉ), используемой для обозначения ъ в неестественных позициях.

***Слово на латинице является грамматически верным если:***

1. его образ от прообраза совпадает с самим словом (`lat_word == RUtoEN(ENtoRU(lat_word))`),
2. его прообраз грамматически верен (`ENtoRU(lat_word)`).

Так же нужно специальное правило для аббревиатур: АЭС/AES, АЕС/AES/AÊS, ФМШ/FMS/FMŠ, ЭЮЯ/EUA/EÛÂ.
То есть, использовать не модификатор а модифицируемую букву (отбросить диакритический знак в латинице).

*Латиница без диграфов станет удобной только при наличии удобных програмных средств ввода. Для мобильных устройств: словаря для swipe-клавиатуры, в которой все 34 буквы основного расширенного алфавита расположены отдельно. Для десктопа скорее всего придется переиспользовать именно русскую раскладку - нужно, чтобы одновременно были доступны все буквы.* Например, вот такая:

| .   | .   | .   | .   | .   | .   | .   | .   | .   | .       | .   | .   | .   | .   |
| ---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:-------:|:---:|:---:|:---:|:---:|
| ё ô | й j | ц c | у u | к k | е e | н n | г g | ш š | щ **ê** | з z | х h | ъ x | \ î |
|     | ф f | ы y | в v | а a | п p | р r | о o | л l | д d     | ж ž | э ę |     | = ĵ |
|     |     | я â | ч č | с s | м m | и i | т t | ь ɉ | б b     | ю û | . , |     |     |



## Примеры текстов в транслитерации

*По-моему, это вариант гораздо лучше подходит для русско-английских билингвов, чем вариант с диакритическими знаками.*

Pjyanyj master po proektu sdelal mehanicheskij objekt s izjanom. Yesli brak ne obnaruzhitsya, to belyj bolid boljshe ne smozhet vyigryvatj gonki.

V pjyese pro devushku v zelyonom platjyice vse sadilisj na ladjyi i plyli po reke. No tut iz lesa vyshel konj v paljto i prikazal vsem mytjsya.

Prepodobnyj Bajyes podkinul igraljnyje kosti. Vypalo shestj, znachit yemu pridyotsya mazatj jod na ranu.

Maer neboljshogo gorodishki otkryl tablicu exelya i vozmutilsya cenoj novogo exkavatora. Azh ekzema snova stala yego bespokoitj. Oh uzh eta pokupka vechnogo dvigatelya v proshlom godu! A tak zhe pokupka aaeroplana-ekranolyota. Yesli tak pojdyot i daljshe, to byudzhetu pridyotsya hudo.

V etom vide fraza ot A to Ya nachinayet vyglyadetj sovsem po-drugomu. Sejchas shchyotka novaya, no pozzhe ona stanet staraya. Chernysh lyubit kogda yego cheshut yeyu. Yozh kolyuchij i pohozh na neyo.

Skhod mestnyh zhytelej indijskoj derevni sikkhov reshal chto zhe delatj s otkhodami kompanii "The LLC". Odin iz prisutstvuyushchih nosil hoholok na golove. On i nashyol vyhod iz situacii.

"Kto s mechom k nam pridyot, tot ot mecha i..." - ne smog dogovoritj starshij mehanik Vasilij.

Imeetsya neskoljko gipotez proiskhozhdeniya sobaki, naibolee veroyatnymi yeyo predkami schitayutsya volk i nekotoryje vidy shakalov.

V suzhdeniyah uchyonyh o predkah domashnej sobaki prisutstvuyut dve tochki zreniya. Odni schitayut, chto sobaki - polifileticheskaya gruppa (proiskhodyashchaya ot neskoljkih predkov), drugie priderzhivayutsya mneniya, chto vse sobaki proizoshli ot odnogo predka (monofileticheskaya teoriya).


## Примеры текстов на латинице

Pjânyj master po proektu sdelal mehaničeskij objekt s izjanom. Êsli brak ne obnaružitsâ, to belyj bolid boljše ne smožet vyigryvatj gonki.

V pjêse pro devušku v zelônom platjîce vse sadilisj na ladjî i plyli po reke. No tut iz lesa vyšel konj v paljto i prikazal vsem mytjsâ.

Prepodobnyj Bajês podkinul igraljnyê kosti. Vypalo šestj, značit êmu pridôtsâ mazatj jod na ranu.

Męr neboljšogo gorodiški otkryl tablicu ęxelâ i vozmutilsâ cenoj novogo ęxkavatora. Až ękzema snova stala êgo bespokoitj. Oh už ęta pokupka večnogo dvigatelâ v prošlom godu! A tak že pokupka aęroplana-ękranolôta. Êsli tak pojdôt i daljše, to bûdžetu pridôtsâ hudo.

V ętom vide fraza ot A to Â načinaêt vyglâdetj sovsem po-drugomu. Sejčas ščôtka novaâ, no pozže ona stanet staraâ. Černyš lûbit kogda êgo češut êû. Ôž kolûčij i pohož na neô.

Shod mestnyh žytelej indijskoj derevni sikhov rešal čto že delatj s othodami kompanii "The LLC". Odin iz prisutstvuûščih nosil hoholok na golove. On i našôl vyhod iz situacii.

"Kto s mečom k nam pridôt, tot ot meča i..." - ne smog dogovoritj staršij mehanik Vasilij.

Imeetsâ neskoljko gipotez proishoždeniâ sobaki, naibolee veroâtnymi êô predkami sčitaûtsâ volk i nekotoryê vidy šakalov.

V suždeniâh učônyh o predkah domašnej sobaki prisutstvuût dve točki zreniâ. Odni sčitaût, čto sobaki - polifiletičeskaâ gruppa (proishodâščaâ ot neskoljkih predkov), drugie priderživaûtsâ mneniâ, čto vse sobaki proizošli ot odnogo predka (monofiletičeskaâ teoriâ).


## Кириллица => латиница

Пока что это только зачатки двух алгоритмов прямого и обратного пребразования.

### Таблица No.1 (сложные составные: й,ъ,ы,ь=>j,y)

`\c` - согласная (consonant), но не йот. Специальный символ регулярных выражений для `[qwrtpsdfghklzxcvbnmцкнгшщзхфвпрлджчсмтб]` (но без й, j).

|     | Cyrillic RegEx | Latin RegEx | Примеры                                      |
| --------- | --------------:|:----- | -------------------------------------------- |
| ъе/je, ъё/jo, ъи/ji, ъю/ju, ъя/ja | `(?<=\c)ъ[еёюяи]` | `(?<=\c)j[eouai]` | об**ъе**кт/ob**je**kt, из**ъя**н/iz**ja**n, м**е**ра/m**e**ra, **е**сли/**ye**sli/**ê**sli, з**я**ка/z**ya**ka/z**â**ka, Мур**ъи**н/Mur**ji**n |
| ъ/jhjh/ɉɉ | `ъ`           | `jhjh` | он**ъ**/on**jhjh**/on**ɉɉ**, Му**ъ**минат/Mu**jhjh**minat/Mu**ɉɉ**minat, Чан**ъ**ань/Chan**jhjh**anj/Čan**ɉɉ**anj, Мур**ъйи**н/Mur**jhjhji**n/Mur**ɉɉji**n |
| | | | |
| ье/jye/jê, ьё/jyo/jô, ьи/jyi/jî, ью/jyu/jû, ья/jya/jâ | `(?<=\c)ь[еёюяи]` | `(?<=\c)jy[eouai]` | п**ье**са/p**jye**sa/p**jê**sa, п**ья**н/p**jya**n/p**jâ**n, лад**ьи**/lad**jyi**/lad**jî**, плат**ьи**це/plat**jyi**ce/plat**jî**ce, Мур**ьи**н/Mur**jyi**n/Mur**jî**n |
| ь/j               | `(?<=\c)ь(?![эоуaйы])` | `(?<=\c)j` | пряч**ь**ся/pryach**j**sya/prâč**j**sâ, мыт**ь**ся/myt**j**sya/myt**j**sâ, кон**ь**/kon**j** |
| ь/jh/ɉ    | `ь`            | `jh`  | Чан**ь**ол/Сhan**jh**ol/Čan**ɉ**ol, Мур**ьй**ин/Mur**jhj**in/Mur**ɉj**in, Чан**ь**ын/Сhan**jh**yn/Čan**ɉ**yn |
| | | | |
| ые/yje/yê, ыё/yjo/yô, ыю/yju/yû, ыя/yja/yâ | `(?<!ы)ы[еёюя]` | `yj[eoua]` | бел**ые**/bel**yje**/bel**yê**, бедн**ыя**/bedn**yja**/bedn**yâ** |
| ые/yyje/ŷê, ыё/yyjo/ŷô, ыю/yyju/ŷû, ыя/yyja/ŷâ | `(?<=ы)ы[еёюя]` | `yyj[eoua]` | ы**ые**/yy**yyje**/y**yê** |
| ы/yy/ŷ    | `ы(?=[эоуаы])` | `yy`  | **ы**а/**yy**a/**y**a, **ы**я/**y**ja/**y**â |
| ы/yy/ŷ    | `(?<=ы)ы`      | `yy`  | **ыы**/**yyyy**/**yy**                       |
| ыи/yyi/ŷi | `(?<![й\c])ыи` | `yyi` | а**ыи**/a**yyi**/a**yi**                     |
| ыи/yi/yi  | `(?<=[й\c])ыи` | `yi`  | в**ыи**грывать/v**yi**gryvatj, в**ыи**скивать/v**yi**skivatj |
| ы/y       | `ы`            | `y`   | кр**ы**ска/kr**y**ska, **ы**пся/**y**psya/**y**psâ, п**ы**хтел/p**y**htel, бел**ы**й/bel**y**j, в**ы**йигрывать/v**y**jigryvatj/v**y**jigryvatj, ба**й**ыс/ba**j**ys |
| | | | |
| й/jj/ĵ    | `(?<=[й\c])й`  | `jj`  | **йй**/**jjjj**/**ĵĵ**, под**й**езд/pod**jj**yezd/pod**ĵ**êzd, под**й**од/pod**jj**od/pod**ĵ**od, Мур**й**ин/Mur**jj**in/Mur**ĵ**in |
| й/jj/ĵ    | `й(?=й)`       | `jj`  | **йй**/**jjjj**/**ĵĵ** |
| й/jj/ĵ | `(?<=ы)й(?=[эоуа])` | `jj` | белы**й**а/bely**jj**a/bely**ĵ**a, белы**й**е/bely**jj**ye/bely**ĵ**ê, **й**эс/**jj**aes/**ĵ**ęs |
| й/j       | `й`            | `j`   | ба**й**ес/ba**j**yes/ba**j**ês, белы**й**/bely**j**, **й**од/**j**od, **й**иппи/**j**ippi, ба**й**ас/ba**j**as, ба**й**яс/ba**j**yas/ba**j**âs, баян/bayan/baân |


### Таблица No.2 (простые составные)

|        | Cyrillic RegEx | Latin RegEx   | Примеры                                                                            |
| ------ | --------------:|:------------- | ---------------------------------------------------------------------------------- |
| е/ye/ê | `(?<=аяй)е`    | `ye`          | бай**е**с/baj**ye**s/baj**ê**s, Ра**е**вская/Ra**ye**vskaya/Ra**ê**vskaâ, зя**е**/zya**ye**/zâ**ê**, за**е**м/za**ye**m/za**ê**m, заём/zayom/zaôm |
| е/ye/ê | `^е`           | `ye`          | **е**сли/**ye**sli/**ê**sli, **е**хо/**ye**ho/êho                                  |
| е/e    | `е`            | `e`           | м**е**х/m**e**h, про**е**кт/pro**e**kt, за**е**зд/za**e**zd                        |
| экс/ex | `экс      `    | `ex`          | **экс**каватор/**ex**kavator/**ęx**kavator, **экс**ель/**ex**elj/**ęx**elj, м**экс**/m**ex**/m**ęx**, экзамен/ekzamen/ękzamen, экзема/ekzema/ękzema, Мексика/Meksika, мех/meh |
| э/e    | `^э`           | `e`           | **эх**о/**eh**o/**ęh**o, **э**тот/**e**tot/**ę**tot, **э**он/**e**on/**ę**on, **э**кран/**e**kran/**ę**kran, **э**ротика/**e**rotika/**ę**rotika |
| э/ae/ę | `э`            | `ae`          | м**э**р/m**ae**r/m**ę**r, мер/mer, Но**э**ль/No**ae**lj/No**ę**lj, а**э**роплан/a**ae**roplan/a**ę**roplan, радио**э**хо/radio**ae**ho/radio**ę**ho, ма**э**р/ma**ae**r/ma**ę**r, в**эч**ный/v**aech**nyj/v**ęč**nyj, й**э**с/jj**ae**s/ĵ**ę**s |
| | | | |
| шч/shwch/šwč | `шч`     | `shwch`       | **шч**ётка/**shwch**yotka/**šwč**ôtka                                              |
| щ/shch/šč    | `щ`      | `shch`        | **щ**ётка/**shch**yotka/**šč**ôtka, **cч**ёт/**sch**yot/**sč**ôt                   |
| ж/zh/ž | `ж`            | `zh`          | ё**ж**/yo**zh**/ô**ž**, во**зж**и/vo**zzh**i/vo**zž**i, по**зж**е/po**zž**e        |
| ч/ch/č | `ч`            | `ch`          | **ч**ерныш/**ch**ernysh/**č**ernyš, с**ч**ётная/s**ch**yotnaya/s**č**ôtnaâ         |
| ш/sh/š | `ш`            | `sh`          | **ш**лем/**sh**lem/**š**lem                                                        |
| х/kh/ĥ | `(?=[хтсшзжцчщъьйк])х` | `kh` | с**х**од/s**kh**od/s**h**od, **кх**е/**kkh**e/**kh**e, си**кх**/si**kkh**/si**kh**, ме**х**/me**h**/me**h**, Муръ**х**ин/Murjhjh**kh**in/Murɉɉ**h**in, Мурь**х**ин/Murj**kh**in/Murj**h**in, от**х**од/ot**kh**od/ot**h**od |
| х/h    | `х`            | `h`           | **х**о**х**олок/**h**o**h**olok, в**ы**ход/v**y**hod, ме**х**а/me**h**a, э**х**о/e**h**o, вече/veche/veče, меча/mecha/meča, эч/ech/ęč, мэч/maech/męč, **х**ья/**h**jya/**h**jâ, **х**ьан/**h**jhan/**h**ɉan |
| | | | |
| ё/yo/ô | `ё`            | `yo`          | **ё**мко/**yo**mko/**ô**mko, м**ё**д/m**yo**d/m**ô**d                              |
| ю/yu/û | `ю`            | `yu`          | **Ю**ля/**Yu**lya/**Û**lâ                                                          |
| я/ya/â | `я`            | `ya`          | Из**я**/Iz**ya**/Iz**â**                                                           |
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


[latin capital letter j with stroke, latin small letter dotless j, latin small letter dotless j with stroke U+025F](https://en.m.wikipedia.org/wiki/List_of_Unicode_characters).
