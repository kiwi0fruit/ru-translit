# ru-translit (kiwi0fruit's)

### Uniquely reversible lossless Russian to English transliteration (without use of extra letters, diacritics and non-letter spelling marks). Uniquely reversible lossless Romanization of Russian with extended alphabet (Ââ,Ĉĉ,Ėė,Êê,Ĥĥ,ȷ,Ĵĵ,Ôô,Ṡṡ,Ŝŝ,Ûû,Ŵŵ,Ŷŷ,Ẑẑ)

### Однозначно обратимая транслитерация без потерь из русского в английский алфавит (без использования дополнительных букв, диакритических и небуквенных знаков). Однозначно обратимая русская латиница без потерь на основе этого транслита с расширенным алфавитом (Ââ,Ĉĉ,Ėė,Êê,Ĥĥ,ȷ,Ĵĵ,Ôô,Ṡṡ,Ŝŝ,Ûû,Ŵŵ,Ŷŷ,Ẑẑ)

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
| e/sjê/yê/sje   | ô/sjô/yô/sjo    | û/sjû/yû/sju    | â/sjâ/yâ/sja    |

| ж  | й    | х/х/эх   | ч  | ш  | щ    | ъ/съя  | ы    | ь    | э  |
| -- | ---- | -------- | -- | -- | ---- | ------ | ---- | ---- | -- |
| zh | jj/j | kh/h/ehh | ch | sh | schh | wh/sja | yy/y | jh/j | eh |
| ẑ  | ĵ/j  | ĥ/h/ėĥ   | ĉ  | ŝ  | ṡĉ   | ŵ/sja  | ŷ/y  | ȷ/j  | ė  |

| a | б | в | г | д | з | и | к | л | м | н | о | п | р | с | т | у | ф | ц |
| - | - | - | - | - | - | - | - | - | - | - | - | - | - | - | - | - | - | - |
| a | b | v | g | d | z | i | k | l | m | n | o | p | r | s | t | u | f | c |

Базовый алфавит остоит из 24 букв (английский алфавит без Xx и Qq). Плюс 14 букв (Ââ,Ĉĉ,Ėė,Êê,Ĥĥ,ȷ,Ĵĵ,Ôô,Ṡṡ,Ŝŝ,Ûû,Ŵŵ,Ŷŷ,Ẑẑ).  
Расширенный алфавит состоит из 38 букв. Таким образом, из диакритических знаков используются только [циркумфлекс](https://ru.wikipedia.org/wiki/%D0%A6%D0%B8%D1%80%D0%BA%D1%83%D0%BC%D1%84%D0%BB%D0%B5%D0%BA%D1%81) и добавление [надстрочной точки](https://ru.wikipedia.org/wiki/%D0%A2%D0%BE%D1%87%D0%BA%D0%B0_(%D0%B4%D0%B8%D0%B0%D0%BA%D1%80%D0%B8%D1%82%D0%B8%D1%87%D0%B5%D1%81%D0%BA%D0%B8%D0%B9_%D0%B7%D0%BD%D0%B0%D0%BA)) (убирание в случае с j).

Многие буквы совпадают с [ГОСТ 16876-71 табл. 2](https://ru.wikipedia.org/wiki/%D0%A2%D1%80%D0%B0%D0%BD%D1%81%D0%BB%D0%B8%D1%82%D0%B5%D1%80%D0%B0%D1%86%D0%B8%D1%8F_%D1%80%D1%83%D1%81%D1%81%D0%BA%D0%BE%D0%B3%D0%BE_%D0%B0%D0%BB%D1%84%D0%B0%D0%B2%D0%B8%D1%82%D0%B0_%D0%BB%D0%B0%D1%82%D0%B8%D0%BD%D0%B8%D1%86%D0%B5%D0%B9#%D0%A1%D1%80%D0%B0%D0%B2%D0%BD%D0%B8%D1%82%D0%B5%D0%BB%D1%8C%D0%BD%D0%B0%D1%8F_%D1%82%D0%B0%D0%B1%D0%BB%D0%B8%D1%86%D0%B0_%D1%81%D0%B8%D1%81%D1%82%D0%B5%D0%BC_%D1%82%D1%80%D0%B0%D0%BD%D1%81%D0%BB%D0%B8%D1%82%D0%B5%D1%80%D0%B0%D1%86%D0%B8%D0%B8) или [ГОСТ 7.79-2000 сист. Б](https://ru.wikipedia.org/wiki/%D0%A2%D1%80%D0%B0%D0%BD%D1%81%D0%BB%D0%B8%D1%82%D0%B5%D1%80%D0%B0%D1%86%D0%B8%D1%8F_%D1%80%D1%83%D1%81%D1%81%D0%BA%D0%BE%D0%B3%D0%BE_%D0%B0%D0%BB%D1%84%D0%B0%D0%B2%D0%B8%D1%82%D0%B0_%D0%BB%D0%B0%D1%82%D0%B8%D0%BD%D0%B8%D1%86%D0%B5%D0%B9#%D0%A1%D1%80%D0%B0%D0%B2%D0%BD%D0%B8%D1%82%D0%B5%D0%BB%D1%8C%D0%BD%D0%B0%D1%8F_%D1%82%D0%B0%D0%B1%D0%BB%D0%B8%D1%86%D0%B0_%D1%81%D0%B8%D1%81%D1%82%D0%B5%D0%BC_%D1%82%D1%80%D0%B0%D0%BD%D1%81%D0%BB%D0%B8%D1%82%D0%B5%D1%80%D0%B0%D1%86%D0%B8%D0%B8).


### Шаг алгоритма No.1

`\c` - согласная (consonant), но не йот. Специальный символ регулярных выражений для `[qwrtpsdfghklzxcvbnmцкнгшщзхфвпрлджчсмтб]` (но без й, j).

|        | Cyrillic\_Regular\_Expression | Latin\_Regular\_Expression | Examples                                               |
| ------ | ---------------------:|:------------------- | --------------------------------------------------------------------- |
| ъе/je, ъё/jo, ъю/ju, ъя/ja | `(?<=\c)ъ[еёюя]` | `(?<=\c)j[eoua]` | об**ъе**кт/ob**je**kt, из**ъя**н/iz**ja**n, м**е**ра/m**e**ra, з**я**ка/z**ya**ka/z**â**ka |
| ъ/wh/ŵ | `ъ`                   | `wh`                | он**ъ**/on**wh**/on**ŵ**, Му**ъ**минат/Mu**wh**minat/Mu**ŵ**minat, Чан**ъ**ань/Chan**wh**anj/Chan**ŵ**anj, Мур**ъйи**н/Mur**whji**n/Mur**ŵji**n, Мур**ъи**н/Mur**whi**n/Mur**ŵi**n |
| ые/yje/yê, ыё/yjo/yô, ыю/yju/yû, ыя/yja/yâ | `ы[еёюя]` | `yj[eoua]` | бел**ые**/bel**yje**/bel**yê**, бедн**ыя**/bedn**yja**/bedn**yâ** |
| ый/yj  | `ый(?=[_\c\W])`       | `yj`                | бел**ый**/bel**yj**, бел**ый**с/bel**yj**s                            |
| ый/yjj/yĵ | `ый(?![_\c\W])`    | `yjj`               | л**ый**ес/l**yjj**es/l**yĵ**es, бел**ый**а/bel**yjj**a/bel**yĵ**a, бел**ый**е/bel**yjj**e/bel**yĵ**e  |
| ы/yy/ŷ | `ы(?=[эоуаи])`        | `yy`                | в**ы**играть/v**yy**igratj/v**ŷ**igratj, в**ы**искивать/v**yy**iskivatj/v**ŷ**iskivatj, **ы**а/**yy**a/**ŷ**a, **ы**я/**y**ja/**y**â, **ы**йи/**y**jji/**y**ĵi |
| ы/y    | `ы`                   | `y`                 | кр**ы**ска/kr**y**ska, **ы**пся/**y**psya/**y**psâ, п**ы**хтел/p**y**htel      |
| ье/jye/jê, ьё/jyo/jô, ью/jyu/jû, ья/jya/jâ | `(?<=\c)ь[еёюя]` | `(?<=\c)jy[eoua]` | п**ье**са/p**jye**sa/p**jê**sa, п**ья**н/p**jya**n/p**jâ**n |
| ь/j    | `(?<=\c)ь(?![эоуaы])` | `(?<=\c)j`          | пряч**ь**ся/pryach**j**sya/prâĉ**j**sâ, мыт**ь**ся/myt**j**sya/myt**j**sâ, кон**ь**/kon**j**, лад**ьи**/lad**ji**, плат**ьи**це/plat**ji**ce, Мур**ьи**н/Mur**ji**n |
| ь/jh/ȷ (Ь/JH/JH) | `ь`         | `jh`                | Чан**ь**ол/Сhan**jh**ol/Ĉan**ȷ**ol, Мур**ьй**ин/Mur**jhj**in/Mur**ȷj**in |
| й/j    | `(?<![ый\c])й(?!й)`   | `j`                 | **й**од/**j**od, ба**й**ес/ba**j**es, **й**иппи/**j**ippi, ба**й**ыс/ba**j**ys, ба**й**яс/ba**j**yas/ba**j**âs |
| й/jj/ĵ | `й`                   | `jj`                | **йй**/**jjjj**/**ĵĵ**, под**й**ес/pod**jj**es/pod**ĵ**es, под**й**од/pod**jj**od/pod**ĵ**od, Мур**й**ин/Mur**jj**in/Mur**ĵ**in |
| эх/ehh/ėĥ | `эх`               | `ehh`               | **эх**о/**ehh**o/**ėĥ**o, эон/ehon/ėon                                |
| х/kh/ĥ | `(?=[хтсшзжцчщъьейк])х` | `kh`              | с**х**од/s**kh**od/s**ĥ**od, **кх**е/**kkh**e/**kĥ**e, си**кх**/si**kkh**/si**kĥ**, ме**х**/me**kh**/me**ĥ**, мэр/mehr/mėr, Муръ**х**ин/Murwh**kh**in/Murŵ**ĥ**in, Мурь**х**ин/Murj**kh**in/Murj**ĥ**in, от**х**од/ot**kh**od/ot**ĥ**od |
| х/h    | `х`                   | `h`                 | **х**о**х**олок/**h**o**h**olok, в**ы**ход/v**y**hod, **х**ья/**h**jya/**h**jâ, **х**ьан/**h**jhan/**h**ȷan |
| е/e    | `е`                   | `e`                 | в**е**к/v**e**k                                                       |
| ё/yo/ô | `ё`                   | `yo`                | **ё**мко/**yo**mko/**ô**mko, м**ё**д/m**yo**d/m**ô**d                 |
| ж/zh/ẑ | `ж`                   | `zh`                | ё**ж**/yo**zh**/ô**ẑ**                                                |
| щ/schh/ṡĉ | `щ`                | `schh`              | **щ**ётка/**schh**yotka/**ṡĉ**ôtka, **cч**ёт/**sch**yot/**sĉ**ôt, **шч**ётка/**shch**yotka/**ŝĉ**ôtka |
| ч/ch/ĉ | `ч`                   | `ch`                | **ч**ерныш/**ch**ernysh/**ĉ**ernyŝ, с**ч**ётная/s**ch**yotnaya/s**ĉ**ôtnaâ |
| ш/sh/ŝ | `ш`                   | `sh`                | **ш**лем/**sh**lem/**ŝ**lem                                           |
| э/eh/ė | `э`                   | `eh`                | **эх**о/**ehh**o/**ėĥ**o, **э**он/**eh**on/**ė**on, **э**кран/**eh**kran/**ė**kran, м**э**р/m**eh**r/m**ė**r |
| ю/yu/û | `ю`                   | `yu`                | **Ю**ля/**Yu**lya/**Û**lâ                                             |
| я/ya/â | `я`                   | `ya`                | Из**я**/Iz**ya**/Iz**â**                                              |
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
* [ ] Проверить как с вводом на смартфоне. Можно ли получить все нужные мне буквы?

[latin small letter z with circumflex](https://en.m.wikipedia.org/wiki/List_of_Unicode_characters).
