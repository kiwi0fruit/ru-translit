# ru-translit (kiwi0fruit's)

### Uniquely reversible lossless Russian to English transliteration (without use of extra letters, diacritics and non-letter spelling marks). Uniquely reversible lossless Romanization of Russian with extended alphabet (two types of diacritics only: Êê, Ěě)

### Однозначно обратимая транслитерация без потерь из русского в английский алфавит (без использования дополнительных букв, диакритических и небуквенных знаков). Однозначно обратимая русская латиница без потерь на основе этого транслита с расширенным алфавитом (только два вида диакритических знаков: Êê, Ěě)

Придумал в качестве развлечения ещё один транслит. Развлечением было удовлетворить ограничениям:

* Транслит - полностью обратимый (является кодировкой без потерь и позволяет точно восстановить произвольный русский текст из латиницы). То есть, это [**инъективное отображение**](https://ru.wikipedia.org/wiki/%D0%98%D0%BD%D1%8A%D0%B5%D0%BA%D1%86%D0%B8%D1%8F_(%D0%BC%D0%B0%D1%82%D0%B5%D0%BC%D0%B0%D1%82%D0%B8%D0%BA%D0%B0)),
* Транслит содержит только буквы (в частности, не использует апостроф): отображение из русских букв `[А-Яа-я]` в английские `[A-Za-z]` без добавлений,
* Не содержит далёких фонетических замен типа щ → w. Желательно, чтобы "звучало" похоже на английский или латинский.

Когда составлял правила хотелось:

* чтобы h означала х в контекстах, где её нельзя перепутать с составными буквами, иначе – kh,
* чтобы j после согласных означала ь, а в остальных случаях – й или йот,
* чтобы ъe/ъя в разрешённых русским языком местах кодировались je/ja,
* чтобы ьe/ья в типичных местах кодировались jye/jya,
* чтобы ыe/ыя в типичных местах кодировались yje/yja,
* в остальных случаях е/я кодировались e/ya,
* для остальных случаев можно ввести контекстно-независимые обозначения типа й/jj, ы/yy, ъ/jhh, ь/jh.


## Кириллица <=> латиница

| **е/сье/ые/съе** | **ё/сьё/ыё/съё** | **и/сьи/ыи/съи**     |
|:----------------:|:----------------:|:--------------------:|
| e/sjye/yje/sje   | yo/sjyo/yjo/sjo  | i/sjyi/yji/sji       |
| e/sjê/yê/sje     | ô/sjô/yô/sjo     | i/sjî/yî/sji         |
| **ю/сью/ыю/съю** | **я/сья/ыя/съя** | **э/экз/экс/эх/эч**  |
| yu/sjyu/yju/sju  | ya/sjya/yja/sja  | eh/exz/ex/ehch/ehchh |
| û/sjû/yû/sju     | â/sjâ/yâ/sja     | ě/ěxz/ěx/ěch/ěĉ      |

| **ж** | **й** | **ч** | **х**     | **ш/шч** | **щ**       |
|:-----:|:-----:|:-----:|:---------:|:--------:|:-----------:|
| zh    | j/jj  | ch    | h/kh      | sh/shchh | shch        |
| ž     | j/ĵ   | č     | h/ĥ       | š/šĉ     | šč          |
|       |       |       | **съя/ъ** | **ы/ыя** | **ь/сья/ь** |
|       |       |       | sja/jhh   | y/yja/yy | j/sjya/jh   |
|       |       |       | sja/ɟ     | y/yâ/ŷ   | j/sjâ/ȷ     |

| **a** | **б** | **в** | **г** | **д** | **з** | **к** | **л** | **м** |
|:-----:|:-----:|:-----:|:-----:|:-----:|:-----:|:-----:|:-----:|:-----:|
| a     | b     | v     | g     | d     | z     | k     | l     | m     |
| **н** | **о** | **п** | **р** | **с** | **т** | **у** | **ф** | **ц** |
| n     | o     | p     | r     | s     | t     | u     | f     | c     |

Базовый алфавит остоит из 24 букв (английский алфавит без Qq и Ww). Плюс 13 букв (Ââ,Ĉĉ,Čč,Êê,Ěě,Ĥĥ,Îî,Ĵĵ,Ôô,Šš,Ûû,Ŷŷ,Žž).  
Расширенный алфавит состоит из 37 букв. Из диакритических знаков для естественных русских языковых конструкций используются только [циркумфлекс](https://ru.wikipedia.org/wiki/%D0%A6%D0%B8%D1%80%D0%BA%D1%83%D0%BC%D1%84%D0%BB%D0%B5%D0%BA%D1%81) и [гачек](https://ru.wikipedia.org/wiki/%D0%93%D0%B0%D1%87%D0%B5%D0%BA). Дополнительно могут быть использованы 3 редкие модификации j для обозначения ъ и ь в невозмножных позициях (Ɉ,ɟ,ȷ). Клавиатура Google их не поддерживает.

***Слово на латинице является грамматически верным если:***

1. его образ от прообраза совпадает с самим словом (`lat_word == RUtoEN(ENtoRU(lat_word))`),
2. его прообраз грамматически верен (`ENtoRU(lat_word)`).

Многие буквы совпадают с [ГОСТ 16876-71 табл. 2](https://ru.wikipedia.org/wiki/%D0%A2%D1%80%D0%B0%D0%BD%D1%81%D0%BB%D0%B8%D1%82%D0%B5%D1%80%D0%B0%D1%86%D0%B8%D1%8F_%D1%80%D1%83%D1%81%D1%81%D0%BA%D0%BE%D0%B3%D0%BE_%D0%B0%D0%BB%D1%84%D0%B0%D0%B2%D0%B8%D1%82%D0%B0_%D0%BB%D0%B0%D1%82%D0%B8%D0%BD%D0%B8%D1%86%D0%B5%D0%B9#%D0%A1%D1%80%D0%B0%D0%B2%D0%BD%D0%B8%D1%82%D0%B5%D0%BB%D1%8C%D0%BD%D0%B0%D1%8F_%D1%82%D0%B0%D0%B1%D0%BB%D0%B8%D1%86%D0%B0_%D1%81%D0%B8%D1%81%D1%82%D0%B5%D0%BC_%D1%82%D1%80%D0%B0%D0%BD%D1%81%D0%BB%D0%B8%D1%82%D0%B5%D1%80%D0%B0%D1%86%D0%B8%D0%B8) или [ГОСТ 7.79-2000 сист. Б](https://ru.wikipedia.org/wiki/%D0%A2%D1%80%D0%B0%D0%BD%D1%81%D0%BB%D0%B8%D1%82%D0%B5%D1%80%D0%B0%D1%86%D0%B8%D1%8F_%D1%80%D1%83%D1%81%D1%81%D0%BA%D0%BE%D0%B3%D0%BE_%D0%B0%D0%BB%D1%84%D0%B0%D0%B2%D0%B8%D1%82%D0%B0_%D0%BB%D0%B0%D1%82%D0%B8%D0%BD%D0%B8%D1%86%D0%B5%D0%B9#%D0%A1%D1%80%D0%B0%D0%B2%D0%BD%D0%B8%D1%82%D0%B5%D0%BB%D1%8C%D0%BD%D0%B0%D1%8F_%D1%82%D0%B0%D0%B1%D0%BB%D0%B8%D1%86%D0%B0_%D1%81%D0%B8%D1%81%D1%82%D0%B5%D0%BC_%D1%82%D1%80%D0%B0%D0%BD%D1%81%D0%BB%D0%B8%D1%82%D0%B5%D1%80%D0%B0%D1%86%D0%B8%D0%B8).


## Кириллица => латиница

Пока что это только зачатки двух алгоритмов прямого и обратного пребразования.

### Таблица No.1

`\c` - согласная (consonant), но не йот. Специальный символ регулярных выражений для `[qwrtpsdfghklzxcvbnmцкнгшщзхфвпрлджчсмтб]` (но без й, j).

|        | Cyrillic RegEx        | Latin RegEx         | Примеры                                                |
| ------ | ---------------------:|:------------------- | --------------------------------------------------------------------- |
| ъе/je, ъё/jo, ъи/ji, ъю/ju, ъя/ja | `(?<=\c)ъ[еёюяи]` | `(?<=\c)j[eouai]` | об**ъе**кт/ob**je**kt, из**ъя**н/iz**ja**n, м**е**ра/m**e**ra, з**я**ка/z**ya**ka/z**â**ka, Мур**ъи**н/Mur**ji**n |
| ъ/jhh/ɟ (Ъ/JHH/Ɉ) | `ъ`        | `jhh`                | он**ъ**/on**jhh**/on**ɟ**, Му**ъ**минат/Mu**jhh**minat/Mu**ɟ**minat, Чан**ъ**ань/Chan**jhh**anj/Chan**ɟ**anj, Мур**ъйи**н/Mur**jhhji**n/Mur**ɟji**n |
| ье/jye/jê, ьё/jyo/jô, ьи/jyi/jî, ью/jyu/jû, ья/jya/jâ | `(?<=\c)ь[еёюяи]` | `(?<=\c)jy[eouai]` | п**ье**са/p**jye**sa/p**jê**sa, п**ья**н/p**jya**n/p**jâ**n, лад**ьи**/lad**jyi**/lad**jî**, плат**ьи**це/plat**jyi**ce/plat**jî**ce, Мур**ьи**н/Mur**jyi**n/Mur**jî**n |
| ь/j    | `(?<=\c)ь(?![эоуaйы])` | `(?<=\c)j`         | пряч**ь**ся/pryach**j**sya/prâč**j**sâ, мыт**ь**ся/myt**j**sya/myt**j**sâ, кон**ь**/kon**j** |
| ь/jh/ȷ (Ь/JH/JH) | `ь`         | `jh`                | Чан**ь**ол/Сhan**jh**ol/Čan**ȷ**ol, Мур**ьй**ин/Mur**jhj**in/Mur**ȷj**in, Чан**ь**ын/Сhan**jh**yn/Čan**ȷ**yn |
| ые/yje/yê, ыё/yjo/yô, ыи/yji/yî, ыю/yju/yû, ыя/yja/yâ | `ы[еёюяи]` | `yj[eouai]` | бел**ые**/bel**yje**/bel**yê**, бедн**ыя**/bedn**yja**/bedn**yâ** |
| ый/yjj/yĵ | `ый(?![_\c\W])`    | `yjj`               | л**ый**ес/l**yjj**es/l**yĵ**es, бел**ый**а/bel**yjj**a/bel**yĵ**a, бел**ый**е/bel**yjj**e/bel**yĵ**e  |
| ый/yj  | `ый(?=[_\c\W])`       | `yj(?=[_\c\W])`     | бел**ый**/bel**yj**, бел**ый**с/bel**yj**s                            |
| ы/y    | `ы`                   | `y`                 | кр**ы**ска/kr**y**ska, **ы**пся/**y**psya/**y**psâ, п**ы**хтел/p**y**htel |
| ы/yy/ŷ | `ы(?=[эоуаиы])`       | `yy`                | в**ы**игрывать/v**yy**igryvatj/v**ŷ**igryvatj, в**ы**искивать/v**yy**iskivatj/v**ŷ**iskivatj, **ы**а/**yy**a/**ŷ**a, **ы**я/**y**ja/**y**â, **ы**йи/**y**jji/**y**ĵi |
| ы/yy/ŷ | `(?<=ы)ы`             | `yy`                | **ыы**/**yyyy** |
| й/j    | `(?<![ый\c])й(?!й)`   | `j`                 | **й**од/**j**od, ба**й**ес/ba**j**es, **й**иппи/**j**ippi, ба**й**ыс/ba**j**ys, ба**й**яс/ba**j**yas/ba**j**âs |
| й/jj/ĵ | `й`                   | `jj`                | **йй**/**jjjj**/**ĵĵ**, под**й**ес/pod**jj**es/pod**ĵ**es, под**й**од/pod**jj**od/pod**ĵ**od, Мур**й**ин/Mur**jj**in/Mur**ĵ**in |


### Таблица No.2

|        | Cyrillic RegEx | Latin RegEx   | Примеры                                                                            |
| ------ | --------------:|:------------- | ---------------------------------------------------------------------------------- |
| экз/exz/ěxz | `экз`     | `exz`         | **экз**амен/**exz**amen/**ěxz**amen, **экз**ема/**exz**ema/**ěxz**ema              |
| экс/ex/ěx | `экс(?!з)`  | `ex`          | **экс**каватор/**ex**kavator/**ěx**kavator, **экс**ель/**ex**elj/**ěx**elj         |
| эч/ehchh/ěĉ | `эч`      | `ehchh`       | в**эч**ный/v**ehchh**nyj/v**ěĉ**nyj                                                |
| эх/ehch/ěch | `эх`      | `ehch`        | **эх**о/**ehch**o/**ěch**o, вече/veche/veče, меча/mecha/meča, меха/mekha/meĥa      |
| э/eh/ě | `э`            | `eh`          | **э**он/**eh**on/**ě**on, **э**кран/**eh**kran/**ě**kran, м**э**р/m**eh**r/m**ě**r |
| шч/shchh/šĉ | `шч`      | `shchh`       | **шч**ётка/**shchh**yotka/**šĉ**ôtka                                               |
| щ/shch/šč | `щ`         | `shch`        | **щ**ётка/**shch**yotka/**šč**ôtka, **cч**ёт/**sch**yot/**sč**ôt                   |
| ж/zh/ž | `ж`            | `zh`          | ё**ж**/yo**zh**/ô**ž**                                                             |
| ч/ch/č | `ч`            | `ch`          | **ч**ерныш/**ch**ernysh/**č**ernyš, с**ч**ётная/s**ch**yotnaya/s**č**ôtnaâ         |
| ш/sh/š | `ш`            | `sh`          | **ш**лем/**sh**lem/**š**lem                                                        |
| х/kh/ĥ | `(?=[хтсшзжцчщъьейк])х` | `kh` | с**х**од/s**kh**od/s**ĥ**od, **кх**е/**kkh**e/**kĥ**e, си**кх**/si**kkh**/si**kĥ**, ме**х**/me**kh**/me**ĥ**, мэр/mehr/měr, Муръ**х**ин/Murjhh**kh**in/Murɟ**ĥ**in, Мурь**х**ин/Murj**kh**in/Murj**ĥ**in, от**х**од/ot**kh**od/ot**ĥ**od |
| х/h    | `х`            | `h`           | **х**о**х**олок/**h**o**h**olok, в**ы**ход/v**y**hod, **х**ья/**h**jya/**h**jâ, **х**ьан/**h**jhan |
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
| `е` | `e` | `с` | `s` |
| `з` | `z` | `т` | `t` |
| `ы` | `y` | `у` | `u` |
| `и` | `i` | `ф` | `f` |
| `й` | `j` | `х` | `h` |
| `к` | `k` | `ц` | `c` |
| `л` | `l` |     |     |


## TO DO

* [ ] Написать кодировщик и декодировщик на питоне, а потом проверить на каком-нибудь словаре, а так же на случайно-сгенерированных словах. Я не проверял алгоритм декодирования даже мысленно. Но интуитивно чувствую, что он хорошо определён и реализуем. Собственно, алгоритм кодировки строился такой, чтобы не было такого, чтобы разные русские слова (любые) отображались в одну и ту же транслитерацию.
* [ ] Попробовать сделать фильтр pandoc. Но там надо посмотреть какой элемент гарантированно содержит только голый текст.
* [ ] Сделать режим, в котором просто все русские обособленные слова преобразуются в массиве текста.
* [ ] Оформить в виде модуля питона с CLI.
* [ ] Написать инструкцию как сконвертировать произвольную страницу в интернете с помощью сохранения как html и конвертации фильтром/пандоком.
* [ ] Попробовать сделать однострочный джавастрипт, которым можно перевести любую уже открытую страницу в интернете.


[latin capital letter j with stroke, latin small letter dotless j, latin small letter dotless j with stroke U+025F](https://en.m.wikipedia.org/wiki/List_of_Unicode_characters).
