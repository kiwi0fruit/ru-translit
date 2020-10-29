# ru-translit (kiwi0fruit's)

### Uniquely reversible and lossless: Russian to English transliteration (no extra letters, diacritics and non-letters) together with dual romanization of Russian (russkaâ latinica) with extended alphabet (Êê,Žž,...)

### Однозначно обратимые и без потерь: транслитерация из русского в английский алфавит (без дополнительных букв, диакритических и небуквенных знаков) и дуальная русская латиница на основе этого транслита с расширенным алфавитом (Êê, Žž,...)

Придумал в качестве развлечения ещё один транслит. Развлечением было удовлетворить ограничениям:

* Транслит - полностью обратимый (является кодировкой без потерь и позволяет точно восстановить произвольный русский текст из латиницы). То есть, это [**инъективное отображение**](https://ru.wikipedia.org/wiki/%D0%98%D0%BD%D1%8A%D0%B5%D0%BA%D1%86%D0%B8%D1%8F_(%D0%BC%D0%B0%D1%82%D0%B5%D0%BC%D0%B0%D1%82%D0%B8%D0%BA%D0%B0)),
* Транслит содержит только буквы (в частности, не использует апостроф): отображение из русских букв `[А-Яа-я]` в английские `[A-Za-z]` без добавлений,
* Не содержит далёких фонетических замен типа щ → w. Желательно, чтобы "звучало" похоже на английский или латинский.

Когда составлял правила хотелось:

* чтобы х в контекстах, где её нельзя перепутать с составными буквами, кодировалась h, а иначе – kh,
* чтобы j после согласных означала ь, а в остальных случаях – й или йот,
* чтобы ы кодировалась как y.
* чтобы ъe/ъя в разрешённых русским языком местах кодировались je/ja,
* чтобы ьe/ья в типичных местах кодировались jye/jya,
* чтобы ыe/ыя в типичных местах кодировались yje/yja,
* в остальных случаях е/я кодировались e/ya,
* для случаев нетипичного использования русских букв можно ввести контекстно-независимые обозначения типа й/jj, ы/yy, ъ/wjh, ь/jh.


## Кириллица <=> латиница

Главной целью проекта была обратимая транслитерация в английский алфавит, близкая к английскому чтению. Латиница с диакритическими знаками является простой, но стилистически однородной, производной от транслитерации.

| **a** | **б** | **в** | **г** | **д** | **з** | **к** | **л** | **м** |
|:-----:|:-----:|:-----:|:-----:|:-----:|:-----:|:-----:|:-----:|:-----:|
| a     | b     | v     | g     | d     | z     | k     | l     | m     |
| **н** | **о** | **п** | **р** | **с** | **т** | **у** | **ф** | **ц** |
| n     | o     | p     | r     | s     | t     | u     | f     | c     |

Краткая версия:

| **е** | **ё** | **ж** | **и** | **й** | **х** | **ч**   | **ш**   | **щ**   | 
|:-----:|:-----:|:-----:|:-----:|:-----:|:-----:|:-------:|:-------:|:-------:|
| e/ê   | ô     | ž     | i/î   | j/ĵ   | h/ĥ   | č       | š       | šč      |
| e/ye/je | yo/jo | zh  | i/yi/ji | j/jj | h/kh | ch      | sh      | shch    |
| **ъ** | **ы** | **ь** | **э** | **ю** | **я** | **экс** |         |         |
| j/wɉ  | y/ŷ   | j/ɉ   | e/ę   | û     | â     | ex      |         |         |
| j/wjh | y/yy  | j/jh  | e/ae  | yu/ju | ya/ja | ex      |         |         |

Подробная версия:

| **е/се/сье/ые/съе** | **ё/сьё/ыё/съё** | **и/сьи/сыи/аыи/съи**   |
|:-------------------:|:----------------:|:-----------------------:|
| ye/se/sjye/yje/sje  | yo/sjyo/yjo/sjo  | i/sjyi/syi/ayyi/sji     |
| ê/se/sjê/yê/sje     | ô/sjô/yô/sjo     | i/sjî/syi/aŷi/sji       |
| **ю/сью/ыю/съю**    | **я/сья/ыя/съя** | **э/сэ/саэ/аэ/экс/экз** |
| yu/sjyu/yju/sju     | ya/sjya/yja/sja  | e/sae/saae/ae/ex/ekz    |
| û/sjû/yû/sju        | â/sjâ/yâ/sja     | e/sę/saę/ae/ex/ekz      |

| **ж** | **ч** | **х**         | **ш/шч**      | **щ**           |
|:-----:|:-----:|:-------------:|:-------------:|:---------------:|
| zh    | ch    | h/kh          | sh/shwch      | shch            |
| ž     | č     | h/ĥ           | š/šwč         | šč              |
|       | **й** | **съе/ъ/съи** | **ы/ые/ы/ыи** | **ь/сье/ь/сьи** |
|       | j/jj  | sje/wjh/sji   | y/yje/yy/yi   | j/sjye/jh/sjyi  |
|       | j/ĵ   | sje/wɉ/sji    | y/yê/ŷ/yi     | j/sjê/ɉ/sjî     |

Многие буквы совпадают с [ГОСТ 16876-71 табл. 2](https://ru.wikipedia.org/wiki/%D0%A2%D1%80%D0%B0%D0%BD%D1%81%D0%BB%D0%B8%D1%82%D0%B5%D1%80%D0%B0%D1%86%D0%B8%D1%8F_%D1%80%D1%83%D1%81%D1%81%D0%BA%D0%BE%D0%B3%D0%BE_%D0%B0%D0%BB%D1%84%D0%B0%D0%B2%D0%B8%D1%82%D0%B0_%D0%BB%D0%B0%D1%82%D0%B8%D0%BD%D0%B8%D1%86%D0%B5%D0%B9#%D0%A1%D1%80%D0%B0%D0%B2%D0%BD%D0%B8%D1%82%D0%B5%D0%BB%D1%8C%D0%BD%D0%B0%D1%8F_%D1%82%D0%B0%D0%B1%D0%BB%D0%B8%D1%86%D0%B0_%D1%81%D0%B8%D1%81%D1%82%D0%B5%D0%BC_%D1%82%D1%80%D0%B0%D0%BD%D1%81%D0%BB%D0%B8%D1%82%D0%B5%D1%80%D0%B0%D1%86%D0%B8%D0%B8) или [ГОСТ 7.79-2000 сист. Б](https://ru.wikipedia.org/wiki/%D0%A2%D1%80%D0%B0%D0%BD%D1%81%D0%BB%D0%B8%D1%82%D0%B5%D1%80%D0%B0%D1%86%D0%B8%D1%8F_%D1%80%D1%83%D1%81%D1%81%D0%BA%D0%BE%D0%B3%D0%BE_%D0%B0%D0%BB%D1%84%D0%B0%D0%B2%D0%B8%D1%82%D0%B0_%D0%BB%D0%B0%D1%82%D0%B8%D0%BD%D0%B8%D1%86%D0%B5%D0%B9#%D0%A1%D1%80%D0%B0%D0%B2%D0%BD%D0%B8%D1%82%D0%B5%D0%BB%D1%8C%D0%BD%D0%B0%D1%8F_%D1%82%D0%B0%D0%B1%D0%BB%D0%B8%D1%86%D0%B0_%D1%81%D0%B8%D1%81%D1%82%D0%B5%D0%BC_%D1%82%D1%80%D0%B0%D0%BD%D1%81%D0%BB%D0%B8%D1%82%D0%B5%D1%80%D0%B0%D1%86%D0%B8%D0%B8).

Базовый алфавит остоит из **24** букв (английский алфавит без Qq и Ww). Плюс **10** букв для латиницы без двухбуквенных сочетаний (Ââ,Čč,Ęę,Êê,Ĥĥ,Îî,Ôô,Šš,Ûû,Žž) и **4** буквы для кодирования неестественных для русского языка сочетаний букв (Ŷŷ,Ɉɉ,Ĵĵ,Ww). Основной расширенный алфавит состоит из **34** букв. Полный расширенный алфавит состоит из **38** букв. Из диакритических знаков для естественных русских языковых конструкций используются только [циркумфлекс](https://ru.wikipedia.org/wiki/%D0%A6%D0%B8%D1%80%D0%BA%D1%83%D0%BC%D1%84%D0%BB%D0%B5%D0%BA%D1%81), [гачек](https://ru.wikipedia.org/wiki/%D0%93%D0%B0%D1%87%D0%B5%D0%BA) и ę – типичное сокращение для ae. Редкая модифицированная зачеркнутая j (Ɉɉ) для обозначения ъ в неестественных позициях не поддерживается клавиатурой Google.

***Слово на латинице является грамматически верным если:***

1. его образ от прообраза совпадает с самим словом (`lat_word == RUtoEN(ENtoRU(lat_word))`),
2. его прообраз грамматически верен (`ENtoRU(lat_word)`).

Так же нужно специальное правило для аббревиатур: АЭС/AES, АЕС/AES/AÊS, ФМШ/FMS/FMŠ, ЭЮЯ/EUA/EÛÂ.
То есть, использовать не модификатор а модифицируемую букву (отбросить диакритический знак в латинице).

## Кириллица => латиница

Пока что это только зачатки двух алгоритмов прямого и обратного пребразования.

### Таблица No.1 (сложные составные: й,ъ,ы,ь=>j,y)

`\c` - согласная (consonant), но не йот. Специальный символ регулярных выражений для `[qwrtpsdfghklzxcvbnmцкнгшщзхфвпрлджчсмтб]` (но без й, j).

|     | Cyrillic RegEx | Latin RegEx | Примеры                                      |
| --------- | --------------:|:----- | -------------------------------------------- |
| ъе/je, ъё/jo, ъи/ji, ъю/ju, ъя/ja | `(?<=\c)ъ[еёюяи]` | `(?<=\c)j[eouai]` | об**ъе**кт/ob**je**kt, из**ъя**н/iz**ja**n, м**е**ра/m**e**ra, **е**сли/**ye**sli/**ê**sli, з**я**ка/z**ya**ka/z**â**ka, Мур**ъи**н/Mur**ji**n |
| ъ/wjh/wɉ  | `ъ`            | `wjh` | он**ъ**/on**wjh**/on**wɉ**, Му**ъ**минат/Mu**wjh**minat/Mu**wɉ**minat, Чан**ъ**ань/Chan**wjh**anj/Chan**wɉ**anj, Мур**ъйи**н/Mur**wjhji**n/Mur**wɉji**n |
| | | | |
| ье/jye/jê, ьё/jyo/jô, ьи/jyi/jî, ью/jyu/jû, ья/jya/jâ | `(?<=\c)ь[еёюяи]` | `(?<=\c)jy[eouai]` | п**ье**са/p**jye**sa/p**jê**sa, п**ья**н/p**jya**n/p**jâ**n, лад**ьи**/lad**jyi**/lad**jî**, плат**ьи**це/plat**jyi**ce/plat**jî**ce, Мур**ьи**н/Mur**jyi**n/Mur**jî**n |
| ь/j               | `(?<=\c)ь(?![эоуaйы])` | `(?<=\c)j` | пряч**ь**ся/pryach**j**sya/prâč**j**sâ, мыт**ь**ся/myt**j**sya/myt**j**sâ, кон**ь**/kon**j** |
| ь/jh/ɉ    | `ь`            | `jh`  | Чан**ь**ол/Сhan**jh**ol/Čan**ɉ**ol, Мур**ьй**ин/Mur**jhj**in/Mur**ɉj**in, Чан**ь**ын/Сhan**jh**yn/Čan**ɉ**yn |
| | | | |
| ые/yje/yê, ыё/yjo/yô, ыю/yju/yû, ыя/yja/yâ | `(?<!ы)ы[еёюя]` | `yj[eoua]` | бел**ые**/bel**yje**/bel**yê**, бедн**ыя**/bedn**yja**/bedn**yâ** |
| ые/yyje/ŷê, ыё/yyjo/ŷô, ыю/yyju/ŷû, ыя/yyja/ŷâ | `(?<=ы)ы[еёюя]` | `yyj[eoua]` | ы**ые**/yy**yyje**/ŷ**ŷê** |
| ы/yy/ŷ    | `ы(?=[эоуаы])` | `yy`  | **ы**а/**yy**a/**ŷ**a, **ы**я/**y**ja/**y**â |
| ы/yy/ŷ    | `(?<=ы)ы`      | `yy`  | **ыы**/**yyyy**/**ŷŷ**                       |
| ыи/yyi/ŷi | `(?<![й\c])ыи` | `yyi` | а**ыи**/a**yyi**/a**ŷi**                     |
| ыи/yi/yi  | `(?<=[й\c])ыи` | `yi`  | в**ыи**грывать/v**yi**gryvatj, в**ыи**скивать/v**yi**skivatj |
| ы/y       | `ы`            | `y`   | кр**ы**ска/kr**y**ska, **ы**пся/**y**psya/**y**psâ, п**ы**хтел/p**y**htel, бел**ы**й/bel**y**j, в**ы**йигрывать/v**y**jjigryvatj/v**y**ĵigryvatj, ба**й**ыс/ba**j**ys |
| | | | |
| й/jj/ĵ    | `(?<=[й\c])й`  | `jj`  | **йй**/**jjjj**/**ĵĵ**, под**й**езд/pod**jj**yezd/pod**ĵ**êzd, под**й**од/pod**jj**od/pod**ĵ**od, Мур**й**ин/Mur**jj**in/Mur**ĵ**in |
| й/jj/ĵ    | `й(?=й)`       | `jj`  | **йй**/**jjjj**/**ĵĵ** |
| й/jj/ĵ | `(?<=ы)й(?=[эоуа])` | `jj` | белы**й**а/bely**jj**a/bely**ĵ**a, белы**й**е/bely**jj**ye/bely**ĵ**ê, **й**эс/**jj**es/**ĵ**es |
| й/j       | `й`            | `j`   | ба**й**ес/ba**j**yes/ba**j**ês, белы**й**/bely**j**, **й**од/**j**od, **й**иппи/**j**ippi, ба**й**ас/ba**j**as, ба**й**яс/ba**j**yas/ba**j**âs, баян/bayan/baân |


### Таблица No.2 (простые составные)

|        | Cyrillic RegEx | Latin RegEx   | Примеры                                                                            |
| ------ | --------------:|:------------- | ---------------------------------------------------------------------------------- |
| е/ye/ê |     `(?<!\c)е` | `ye`          | за**е**зд/za**ye**zd/za**ê**zd, бай**е**с/baj**ye**s/baj**ê**s, **е**сли/**ye**sli/**ê**sli, **е**хо/**ye**ho/êho |
| е/e    |     `(?<=\c)е` | `e`           | м**е**х/m**e**h                                                                    |
| экс/ex  | `экс     `    | `ex`          | **экс**каватор/**ex**kavator, **экс**ель/**ex**elj, м**экс**/m**ex**, экзамен/ekzamen, экзема/ekzema, Мексика/Meksika, мех/meh |
| э/ae/ę  | `(?<=\ca?)э`  | `ae`          | м**э**р/m**ae**r/m**ę**r, мер/mer, д**э**хо/d**ae**ho/d**ę**ho, ма**э**р/ma**ae**r/ma**ę**r, ааэро/aaero, еаэро/yeaero/êaero, в**эч**ный/v**aech**nyj/v**ęč**nyj |
| э/e     | `(?<!\c)э`    | `e`           | **эх**о/**eh**o, **э**тот/**e**tot, **э**он/**e**on, **э**кран/**e**kran, радио**э**хо/radio**e**ho, а**э**роплан/a**e**roplan, **э**ротика/**e**rotika, Но**э**ль/No**e**lj |
| | | | |
| шч/shwch/šwč | `шч`     | `shwch`       | **шч**ётка/**shwch**yotka/**šwč**ôtka                                              |
| щ/shch/šč    | `щ`      | `shch`        | **щ**ётка/**shch**yotka/**šč**ôtka, **cч**ёт/**sch**yot/**sč**ôt                   |
| ж/zh/ž | `ж`            | `zh`          | ё**ж**/yo**zh**/ô**ž**, во**зж**и/vo**zzh**i/vo**zž**i, по**зж**е/po**zž**e        |
| ч/ch/č | `ч`            | `ch`          | **ч**ерныш/**ch**ernysh/**č**ernyš, с**ч**ётная/s**ch**yotnaya/s**č**ôtnaâ         |
| ш/sh/š | `ш`            | `sh`          | **ш**лем/**sh**lem/**š**lem                                                        |
| х/kh/ĥ | `(?=[хтсшзжцчщъьйк])х` | `kh` | с**х**од/s**kh**od/s**ĥ**od, **кх**е/**kkh**e/**kĥ**e, си**кх**/si**kkh**/si**kĥ**, ме**х**/me**h**/me**h**, Муръ**х**ин/Murwjh**kh**in/Murwɉ**ĥ**in, Мурь**х**ин/Murj**kh**in/Murj**ĥ**in, от**х**од/ot**kh**od/ot**ĥ**od |
| х/h    | `х`            | `h`           | **х**о**х**олок/**h**o**h**olok, в**ы**ход/v**y**hod, ме**х**а/me**h**a, э**х**о/e**h**o, вече/veche/veče, меча/mecha/meča, эч/ech/eč, мэч/maech/męch, **х**ья/**h**jya/**h**jâ, **х**ьан/**h**jhan/**h**ɉan |
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
