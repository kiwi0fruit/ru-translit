# ru-translit (kiwi0fruit's)

### Uniquely reversible lossless Russian to English transliteration (without use of extra letters, diacritics and non-letter spelling marks). Uniquely reversible lossless Romanization of Russian with extended alphabet (Ǎǎ,Ĉĉ,Čč,Êê,Ěě,Ĥĥ,Ĵĵ,Ǒǒ,Šš,Ǔǔ,Ŵŵ,Ŷŷ,Žž)

### Однозначно обратимая транслитерация без потерь из русского в английский алфавит (без использования дополнительных букв, диакритических и небуквенных знаков). Однозначно обратимая русская латиница без потерь на основе этого транслита с расширенным алфавитом (Ǎǎ,Ĉĉ,Čč,Êê,Ěě,Ĥĥ,Ĵĵ,Ǒǒ,Šš,Ǔǔ,Ŵŵ,Ŷŷ,Žž)

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
* для остальных случаев можно ввести контекстно-независимые обозначения типа й/jj, ы/yy, ъ/wh, ь/jh.


## Кириллица <=> латиница

| е/сье/ые/съе   | ё/сьё/ыё/съё    | ю/сью/ыю/съю    | я/сья/ыя/съя    |
| -------------- | --------------- | --------------- | --------------- |
| e/sjye/yje/sje | yo/sjyo/yjo/sjo | yu/sjyu/yju/sju | ya/sjya/yja/sja |
| e/sjě/yě/sje   | ǒ/sjǒ/yǒ/sjo    | ǔ/sjǔ/yǔ/sju    | ǎ/sjǎ/yǎ/sja    |

| ж  | й    | х    | ч  | ш/шч     | щ    | ъ/съя  | ы    | ь    | э/экз/экс/эх/эч      |
| -- | ---- | ---- | -- | -------- | ---- | ------ | ---- | ---- | -------------------- |
| zh | jj/j | kh/h | ch | sh/shchh | shch | wh/sja | yy/y | jh/j | eh/exz/ex/ehch/ehchh |
| ž  | ĵ/j  | ĥ/h  | č  | š/šĉ     | šč   | ŵ/sja  | ŷ/y  | jh/j | ê/êxz/êx/êĥ/êĉ       |

| a | б | в | г | д | з | и | к | л | м | н | о | п | р | с | т | у | ф | ц |
| - | - | - | - | - | - | - | - | - | - | - | - | - | - | - | - | - | - | - |
| a | b | v | g | d | z | i | k | l | m | n | o | p | r | s | t | u | f | c |

Базовый алфавит остоит из 25 букв (английский алфавит без Qq). Плюс 13 букв (Ǎǎ,Ĉĉ,Čč,Êê,Ěě,Ĥĥ,Ĵĵ,Ǒǒ,Šš,Ǔǔ,Ŵŵ,Ŷŷ,Žž).  
Расширенный алфавит состоит из 38 букв. Таким образом, из диакритических знаков используются только [циркумфлекс](https://ru.wikipedia.org/wiki/%D0%A6%D0%B8%D1%80%D0%BA%D1%83%D0%BC%D1%84%D0%BB%D0%B5%D0%BA%D1%81) и [гачек](https://ru.wikipedia.org/wiki/%D0%93%D0%B0%D1%87%D0%B5%D0%BA).

Многие буквы совпадают с [ГОСТ 16876-71 табл. 2](https://ru.wikipedia.org/wiki/%D0%A2%D1%80%D0%B0%D0%BD%D1%81%D0%BB%D0%B8%D1%82%D0%B5%D1%80%D0%B0%D1%86%D0%B8%D1%8F_%D1%80%D1%83%D1%81%D1%81%D0%BA%D0%BE%D0%B3%D0%BE_%D0%B0%D0%BB%D1%84%D0%B0%D0%B2%D0%B8%D1%82%D0%B0_%D0%BB%D0%B0%D1%82%D0%B8%D0%BD%D0%B8%D1%86%D0%B5%D0%B9#%D0%A1%D1%80%D0%B0%D0%B2%D0%BD%D0%B8%D1%82%D0%B5%D0%BB%D1%8C%D0%BD%D0%B0%D1%8F_%D1%82%D0%B0%D0%B1%D0%BB%D0%B8%D1%86%D0%B0_%D1%81%D0%B8%D1%81%D1%82%D0%B5%D0%BC_%D1%82%D1%80%D0%B0%D0%BD%D1%81%D0%BB%D0%B8%D1%82%D0%B5%D1%80%D0%B0%D1%86%D0%B8%D0%B8) или [ГОСТ 7.79-2000 сист. Б](https://ru.wikipedia.org/wiki/%D0%A2%D1%80%D0%B0%D0%BD%D1%81%D0%BB%D0%B8%D1%82%D0%B5%D1%80%D0%B0%D1%86%D0%B8%D1%8F_%D1%80%D1%83%D1%81%D1%81%D0%BA%D0%BE%D0%B3%D0%BE_%D0%B0%D0%BB%D1%84%D0%B0%D0%B2%D0%B8%D1%82%D0%B0_%D0%BB%D0%B0%D1%82%D0%B8%D0%BD%D0%B8%D1%86%D0%B5%D0%B9#%D0%A1%D1%80%D0%B0%D0%B2%D0%BD%D0%B8%D1%82%D0%B5%D0%BB%D1%8C%D0%BD%D0%B0%D1%8F_%D1%82%D0%B0%D0%B1%D0%BB%D0%B8%D1%86%D0%B0_%D1%81%D0%B8%D1%81%D1%82%D0%B5%D0%BC_%D1%82%D1%80%D0%B0%D0%BD%D1%81%D0%BB%D0%B8%D1%82%D0%B5%D1%80%D0%B0%D1%86%D0%B8%D0%B8).


### Шаг алгоритма No.1

`\c` - согласная (consonant), но не йот. Специальный символ регулярных выражений для `[qwrtpsdfghklzxcvbnmцкнгшщзхфвпрлджчсмтб]` (но без й, j).

|        | Cyrillic\_Regular\_Expression | Latin\_Regular\_Expression | Examples                                               |
| ------ | ---------------------:|:------------------- | --------------------------------------------------------------------- |
| ъе/je, ъё/jo, ъю/ju, ъя/ja | `(?<=\c)ъ[еёюя]` | `(?<=\c)j[eoua]` | об**ъе**кт/ob**je**kt, из**ъя**н/iz**ja**n, м**е**ра/m**e**ra, з**я**ка/z**ya**ka/z**ǎ**ka |
| ъ/wh/ŵ | `ъ`                   | `wh`                | он**ъ**/on**wh**/on**ŵ**, Му**ъ**минат/Mu**wh**minat/Mu**ŵ**minat, Чан**ъ**ань/Chan**wh**anj/Chan**ŵ**anj, Мур**ъйи**н/Mur**whji**n/Mur**ŵji**n, Мур**ъи**н/Mur**whi**n/Mur**ŵi**n |
| ые/yje/yě, ыё/yjo/yǒ, ыю/yju/yǔ, ыя/yja/yǎ | `ы[еёюя]` | `yj[eoua]` | бел**ые**/bel**yje**/bel**yě**, бедн**ыя**/bedn**yja**/bedn**yǎ** |
| ый/yj  | `ый(?=[_\c\W])`       | `yj`                | бел**ый**/bel**yj**, бел**ый**с/bel**yj**s                            |
| ый/yjj/yĵ | `ый(?![_\c\W])`    | `yjj`               | л**ый**ес/l**yjj**es/l**yĵ**es, бел**ый**а/bel**yjj**a/bel**yĵ**a, бел**ый**е/bel**yjj**e/bel**yĵ**e  |
| ы/yy/ŷ | `ы(?=[эоуаи])`        | `yy`                | в**ы**играть/v**yy**igratj/v**ŷ**igratj, в**ы**искивать/v**yy**iskivatj/v**ŷ**iskivatj, **ы**а/**yy**a/**ŷ**a, **ы**я/**y**ja/**y**ǎ, **ы**йи/**y**jji/**y**ĵi |
| ы/y    | `ы`                   | `y`                 | кр**ы**ска/kr**y**ska, **ы**пся/**y**psya/**y**psǎ, п**ы**хтел/p**y**htel      |
| ье/jye/jě, ьё/jyo/jǒ, ью/jyu/jǔ, ья/jya/jǎ | `(?<=\c)ь[еёюя]` | `(?<=\c)jy[eoua]` | п**ье**са/p**jye**sa/p**jě**sa, п**ья**н/p**jya**n/p**jǎ**n |
| ь/j    | `(?<=\c)ь(?![эоуaй])` | `(?<=\c)j`          | пряч**ь**ся/pryach**j**sya/prǎč**j**sǎ, мыт**ь**ся/myt**j**sya/myt**j**sǎ, кон**ь**/kon**j**, лад**ьи**/lad**ji**, плат**ьи**це/plat**ji**ce, Мур**ьи**н/Mur**ji**n, Чан**ь**ын/Сhan**j**yn/Čan**j**yn |
| ь/jh   | `ь`                   | `jh`                | Чан**ь**ол/Сhan**jh**ol/Čan**jh**ol, Мур**ьй**ин/Mur**jhj**in         |
| й/j    | `(?<![ый\c])й(?!й)`   | `j`                 | **й**од/**j**od, ба**й**ес/ba**j**es, **й**иппи/**j**ippi, ба**й**ыс/ba**j**ys, ба**й**яс/ba**j**yas/ba**j**ǎs |
| й/jj/ĵ | `й`                   | `jj`                | **йй**/**jjjj**/**ĵĵ**, под**й**ес/pod**jj**es/pod**ĵ**es, под**й**од/pod**jj**od/pod**ĵ**od, Мур**й**ин/Mur**jj**in/Mur**ĵ**in |
| х/kh/ĥ | `(?=[хтсшзжцчщъьейк])х` | `kh`              | с**х**од/s**kh**od/s**ĥ**od, **кх**е/**kkh**e/**kĥ**e, си**кх**/si**kkh**/si**kĥ**, ме**х**/me**kh**/me**ĥ**, мэр/mehr/mêr, Муръ**х**ин/Murwh**kh**in/Murŵ**ĥ**in, Мурь**х**ин/Murj**kh**in/Murj**ĥ**in, от**х**од/ot**kh**od/ot**ĥ**od |
| х/h    | `х`                   | `h`                 | **х**о**х**олок/**h**o**h**olok, в**ы**ход/v**y**hod, **х**ья/**h**jya/**h**jǎ, **х**ьан/**h**jhan/**h**jan |
| е/e    | `е`                   | `e`                 | в**е**к/v**e**k                                                       |
| ё/yo/ǒ | `ё`                   | `yo`                | **ё**мко/**yo**mko/**ǒ**mko, м**ё**д/m**yo**d/m**ǒ**d                 |
| ж/zh/ž | `ж`                   | `zh`                | ё**ж**/yo**zh**/ǒ**ž**                                                |
| шч/shchh/šĉ | `шч`             | `shchh`             | **шч**ётка/**shchh**yotka/**šĉ**ǒtka                                  |
| щ/shch/šč | `щ`                | `shch`              | **щ**ётка/**shch**yotka/**šč**ǒtka, **cч**ёт/**sch**yot/**sč**ǒt      |
| ч/ch/č | `ч`                   | `ch`                | **ч**ерныш/**ch**ernysh/**č**ernyš, с**ч**ётная/s**ch**yotnaya/s**č**ǒtnaǎ |
| ш/sh/š | `ш`                   | `sh`                | **ш**лем/**sh**lem/**š**lem                                           |
| экз/exz/êxz | `экз`            | `exz`               | **экз**амен/**exz**amen, **экз**ема/**exz**ema                        |
| экс/ex/êx | `экс(?!з)`         | `ex`                | **экс**каватор/**ex**kavator, **экс**ель/**ex**elj                    |
| эч/ehchh/êĉ | `эч`             | `ehchh`             | в**эч**ный/v**ehchh**nyj/v**êĉ**nyj                                   |
| эх/ehch/êĥ | `эх`              | `ehch`              | **эх**о/**ehch**o/**êĥ**o, вече/veche/veče, меча/mecha/meča, меха/mekha/meĥa |
| э/eh/ê | `э`                   | `eh`                | **э**он/**eh**on/**ê**on, **э**кран/**eh**kran/**ê**kran, м**э**р/m**eh**r/m**ê**r |
| ю/yu/ǔ | `ю`                   | `yu`                | **Ю**ля/**Yu**lya/**Ǔ**lǎ                                             |
| я/ya/ǎ | `я`                   | `ya`                | Из**я**/Iz**ya**/Iz**ǎ**                                              |
| ERROR  |                       | `[qwx]`             |                                                                       |


### Шаг алгоритма No.2

| Cyr | Lat | Cyr | Lat |
| ---:|:--- | ---:|:--- |
| `а` | `a` | `м` | `m` |
| `б` | `b` | `н` | `n` |
| `в` | `v` | `о` | `o` |
| `г` | `g` | `п` | `p` |
| `д` | `d` | `р` | `r` |
|     |     | `с` | `s` |
| `з` | `z` | `т` | `t` |
| `и` | `i` | `у` | `u` |
| `к` | `k` | `ф` | `f` |
| `л` | `l` | `ц` | `c` |


## TO DO

* [ ] Написать кодировщик и декодировщик на питоне, а потом проверить на каком-нибудь словаре, а так же на случайно-сгенерированных словах. Я не проверял алгоритм декодирования даже мысленно. Но интуитивно чувствую, что он хорошо определён и реализуем. Собственно, алгоритм кодировки строился такой, чтобы не было такого, чтобы разные русские слова (любые) отображались в одну и ту же транслитерацию.
* [ ] Попробовать сделать фильтр pandoc. Но там надо посмотреть какой элемент гарантированно содержит только голый текст.
* [ ] Сделать режим, в котором просто все русские обособленные слова преобразуются в массиве текста. Дополнительно `«»`=>`“”`, `№`=>`No.`.
* [ ] Оформить в виде модуля питона с CLI.
* [ ] Написать инструкцию как сконвертировать произвольную страницу в интернете с помощью сохранения как html и конвертации фильтром/пандоком.
* [ ] Попробовать сделать однострочный джавастрипт, которым можно перевести любую уже открытую страницу в интернете.
* [ ] Проверить как с вводом на смартфоне. Можно ли получить все нужные мне буквы?

[latin small letter z with circumflex](https://en.m.wikipedia.org/wiki/List_of_Unicode_characters).
