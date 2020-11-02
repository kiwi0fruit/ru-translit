# ru-translit (kiwi0fruit's)

### Uniquely reversible and lossless: Russian to English transliteration (no extra letters, diacritics and non-letters)

### Однозначно обратимые и без потерь: транслитерация из русского в английский алфавит (без дополнительных букв, диакритических и небуквенных знаков)

Придумал в качестве развлечения ещё один транслит.

Развлечением было удовлетворить ограничениям:

* Транслит - полностью обратимый (является кодировкой без потерь и позволяет точно восстановить произвольный русский текст из латиницы). То есть, это [**инъективное отображение**](https://ru.wikipedia.org/wiki/%D0%98%D0%BD%D1%8A%D0%B5%D0%BA%D1%86%D0%B8%D1%8F_(%D0%BC%D0%B0%D1%82%D0%B5%D0%BC%D0%B0%D1%82%D0%B8%D0%BA%D0%B0)),
* Транслит содержит только буквы (в частности, не использует апостроф): отображение из русских букв `[А-Яа-я]` в английские `[A-Za-z]` без добавлений,
* Не содержит далёких фонетических замен типа щ → w. Желательно, чтобы "звучало" похоже на английский или математический латинский.

Когда составлял правила хотелось, чтобы:

* х в контекстах, где её нельзя перепутать с составными буквами, кодировалась h, а иначе – kh,
* j после согласных означала ь, а в остальных случаях – й или йот,
* ы кодировалась как y.
* ъe/ъя в разрешённых русским языком местах кодировались wje/wja,
* ьe/ья в типичных местах кодировались jye/jya,
* ыe/ыя в типичных местах кодировались yje/yja,
* э кодировалась как ae.
* нетипичное использование русских букв можно было закодировать контекстно-независимыми обозначения типа й/jj, ы/yw, ъ/wjh, ь/jh,
* НО, в итоге из-за логики кодирования й,ъ,ы,ъ и э пришлось е кодировать как ye в начале или после `[аяй]`. А э, наоборот, кодировать как "e" в начале или после `[аяй]`.


## Кириллица <=> латиница

Главной целью проекта была обратимая транслитерация в английский алфавит, близкая к английскому чтению.

| **a** | **б** | **в** | **г** | **д** | **з** | **к** | **л** | **м** |
|:-----:|:-----:|:-----:|:-----:|:-----:|:-----:|:-----:|:-----:|:-----:|
| a     | b     | v     | g     | d     | z     | k     | l     | m     |
| **н** | **о** | **п** | **р** | **с** | **т** | **у** | **ф** | **ц** |
| n     | o     | p     | r     | s     | t     | u     | f     | c     |

Краткая версия (шч и ьь - технические замены для обратимости):

| **е**   | **ё** | **ж** | **и**   | **й** | **х** | **ч**   | **ш**   | **щ**   | 
|:-------:|:-----:|:-----:|:-------:|:-----:|:-----:|:-------:|:-------:|:-------:|
| е/ye/je | yo/jo | zh    | i/yi/ji | j/jj  | h/kh  | ch      | sh      | shch    |
| **ъ**   | **ы** | **ь** | **э**   | **ю** | **я** | **экс** | **шч**  | **ьь**  |
| j/jhjh  | y/yy  | j/jh  | ae/e    | yu/ju | ya/ja | ex      | shwch   | jhwjh   |

Подробнее:

| **е/сье/ые/съе/^e/[аяй]e** | **ё/сьё/ыё/съё** | **и/сьи/сыи/аыи/съи** |
|:---------------------:|:----------------:|:-------------------:|
| e/sjye/yje/sje/^ye/ye | yo/sjyo/yjo/sjo  | i/sjyi/syi/ayyi/sji |
| **ю/сью/ыю/съю**      | **я/сья/ыя/съя** | **э/^э/экс**        |
| yu/sjyu/yju/sju       | ya/sjya/yja/sja  | ae/^e/ex            |

| **й/сй/ыйа** | **съе/ъ/съи** | **ы/ые/ы/ыи** | **ь/сье/ь/сьи** |
|:------------:|:-------------:|:-------------:|:---------------:|
| j/sjj/yjja   | sje/jhjh/sji  | y/yje/yy/yi   | j/sjye/jh/sjyi  |

Многие буквы совпадают с [ГОСТ 16876-71 табл. 2](https://ru.wikipedia.org/wiki/%D0%A2%D1%80%D0%B0%D0%BD%D1%81%D0%BB%D0%B8%D1%82%D0%B5%D1%80%D0%B0%D1%86%D0%B8%D1%8F_%D1%80%D1%83%D1%81%D1%81%D0%BA%D0%BE%D0%B3%D0%BE_%D0%B0%D0%BB%D1%84%D0%B0%D0%B2%D0%B8%D1%82%D0%B0_%D0%BB%D0%B0%D1%82%D0%B8%D0%BD%D0%B8%D1%86%D0%B5%D0%B9#%D0%A1%D1%80%D0%B0%D0%B2%D0%BD%D0%B8%D1%82%D0%B5%D0%BB%D1%8C%D0%BD%D0%B0%D1%8F_%D1%82%D0%B0%D0%B1%D0%BB%D0%B8%D1%86%D0%B0_%D1%81%D0%B8%D1%81%D1%82%D0%B5%D0%BC_%D1%82%D1%80%D0%B0%D0%BD%D1%81%D0%BB%D0%B8%D1%82%D0%B5%D1%80%D0%B0%D1%86%D0%B8%D0%B8) или [ГОСТ 7.79-2000 сист. Б](https://ru.wikipedia.org/wiki/%D0%A2%D1%80%D0%B0%D0%BD%D1%81%D0%BB%D0%B8%D1%82%D0%B5%D1%80%D0%B0%D1%86%D0%B8%D1%8F_%D1%80%D1%83%D1%81%D1%81%D0%BA%D0%BE%D0%B3%D0%BE_%D0%B0%D0%BB%D1%84%D0%B0%D0%B2%D0%B8%D1%82%D0%B0_%D0%BB%D0%B0%D1%82%D0%B8%D0%BD%D0%B8%D1%86%D0%B5%D0%B9#%D0%A1%D1%80%D0%B0%D0%B2%D0%BD%D0%B8%D1%82%D0%B5%D0%BB%D1%8C%D0%BD%D0%B0%D1%8F_%D1%82%D0%B0%D0%B1%D0%BB%D0%B8%D1%86%D0%B0_%D1%81%D0%B8%D1%81%D1%82%D0%B5%D0%BC_%D1%82%D1%80%D0%B0%D0%BD%D1%81%D0%BB%D0%B8%D1%82%D0%B5%D1%80%D0%B0%D1%86%D0%B8%D0%B8).

Алфавит транслитерации состоит из **25** букв (английский алфавит без Qq).

***Слово на латинице является грамматически верным если:***

1. его образ от прообраза совпадает с самим словом (`lat_word == RUtoEN(ENtoRU(lat_word))`),
2. его прообраз грамматически верен (`ENtoRU(lat_word)`).

Так же нужно специальное правило для аббревиатур: АЭС/AES, АЕС/AES, ФМШ/FMS, ЭЮЯ/EUA, ЁМ/EM (не OM).
То есть, использовать не модификатор а модифицируемую букву (отбросить диакритический знак в латинице). Так же не стоит забывать, что все слова с буквой ё могут быть корректно написаны с буквой е, так что yo становится E в качестве общего знаменателя.


## Примеры текстов в транслитерации

*По-моему, это вариант гораздо лучше подходит для русско-английских билингвов, чем варианты с диакритическими знаками. Я пробовал придумать вариант с диакритическими знаками такой, чтобы его было удобнее читать, чем этот - не смог.*

Pjyanyj master po proektu sdelal mehanicheskij obwjekt s izwjanom. Yesli brak ne obnaruzhitsja, to belyj bolid boljshe ne smozhet vyigryvatj gonki.

V pjyese pro devushku v zeljonom platjyice vse sadilisj na ladjyi i plyli po reke. No tut iz lesa vyshel konj v paljto i prikazal vsem mytjsja.

Prepodobnyj Bajyes podkinul igraljnyje kosti. Vypalo shestj, znachit yemu pridjotsja mazatj jod na ranu.

Maer neboljshogo gorodishki otkryl tablicu exelja i vozmutilsja cenoj novogo exkavatora. Azh ekzema snova stala yego bespokoitj. Oh uzh eta pokupka vechnogo dvigatelja v proshlom godu! A tak zhe pokupka aeroplana-ekranoljota. Yesli tak pojdjot i daljshe, to bjudzhetu pridjotsja hudo.

V etom vide fraza ot A to Ya nachinayet vygljadetj sovsem po-drugomu. Sejchas shchjotka novaya, no pozzhe ona stanet staraya. Chernysh ljubit kogda yego cheshut yeyu. Yozh koljuchij i pohozh na neyo.

Skhod mestnyh zhytelej indijskoj derevni sikkhov reshal chto zhe delatj s otkhodami kompanii "The LLC". Odin iz prisutstvuyushchih nosil hoholok na golove. On i nashjol vyhod iz situacii.

"Kto s mechom k nam pridjot, tot ot mecha i..." - ne smog dogovoritj starshij mehanik Vasilij.

Imeetsja neskoljko gipotez proiskhozhdeniya sobaki, naibolee veroyatnymi yeyo predkami schitayutsja volk i nekotoryje vidy shakalov.

V suzhdeniyah uchjonyh o predkah domashnej sobaki prisutstvuyut dve tochki zreniya. Odni schitayut, chto sobaki - polifileticheskaya gruppa (proiskhodjashchaya ot neskoljkih predkov), drugie priderzhivayutsja mneniya, chto vse sobaki proizoshli ot odnogo predka (monofileticheskaya teoriya).


## Кириллица => латиница

Пока что это только зачатки двух алгоритмов прямого и обратного пребразования.

### Таблица No.1 (сложные составные: й,ъ,ы,ь=>j,y)

`\c` - согласная (consonant), но не йот. Специальный символ регулярных выражений для `[qwrtpsdfghklzxcvbnmцкнгшщзхфвпрлджчсмтб]` (но без й, j).

|        | Cyrillic RegEx | Latin RegEx | Примеры                                      |
| ------ | --------------:|:----- | -------------------------------------------- |
| ъе/wje, ъё/wjo, ъи/wji, ъю/wju, ъя/wja | `(?<=\c)ъ[еёюяи]` | `(?<=\c)wj[eouai]` | об**ъе**кт/ob**wje**kt, из**ъя**н/iz**wja**n, мера/mera, если/yesli, зяка/zjaka, Мур**ъи**н/Mur**wji**n |
| ъ/wjh  | `ъ`            | `wjh` | он**ъ**/on**wjh**, Му**ъ**минат/Mu**wjh**minat, Чан**ъ**ань/Chan**wjh**anj, Мур**ъ**йин/Mur**wjh**jin |
| | | | |
| ье/jye, ьё/jyo, ьи/jyi, ью/jyu, ья/jya | `(?<=\c)ь[еёюяи]` | `(?<=\c)jy[eouai]` | п**ье**са/p**jye**sa, п**ья**н/p**jya**n, лад**ьи**/lad**jyi**, плат**ьи**це/plat**jyi**ce, Мур**ьи**н/Mur**jyi**n |
| ь/j    | `(?<=\c)ь(?![эоуaйы])` | `(?<=\c)j` | пряч**ь**ся/prjach**j**sja, мыт**ь**ся/myt**j**sja, кон**ь**/kon**j** |
| ь/jh   | `ь`            | `jh`  | Чан**ь**ол/Сhan**jh**ol, Мур**ьй**ин/Mur**jhj**in, Чан**ь**ын/Сhan**jh**yn |
| | | | |
| ые/yje, ыё/yjo, ыю/yju, ыя/yja | `(?<!ы)ы[еёюя]` | `yj[eoua]` | бел**ые**/bel**yje**, бедн**ыя**/bedn**yja** |
| ы/yw   | `ы(?=[эоуа])`  | `yw`  | Нарва-Й**ыэ**суу/Narva-J**ywe**suu, Баймакл**ыа**ул/Bajmakl**ywa**ul |
| ыи/ywi | `(?<![й\c])ыи` | `ywi` | а**ыи**/a**ywi** |
| ыи/yi  | `(?<=[й\c])ыи` | `yi`  | в**ыи**грывать/v**yi**gryvatj, в**ыи**скивать/v**yi**skivatj |
| ы/y    | `ы`            | `y`   | кр**ы**ска/kr**y**ska, **ы**пся/**y**psja, п**ы**хтел/p**y**htel, бел**ы**й/bel**y**j, в**ы**йигрывать/v**y**jigryvatj, ба**й**ыс/ba**j**ys |
| | | | |
| й/jj   | `(?<=\c)й`     | `jj`  | под**й**езд/pod**jj**yezd, под**й**од/pod**jj**od, Мур**й**ин/Mur**jj**in, под**йй**од/pod**jjj**od |
| й/jj/ĵ | `(?<=ы)й(?=[эоуа])` | `jj` | белы**й**а/bely**jj**a/bely**ĵ**a, белы**й**е/bely**jj**ye/bely**ĵ**e, **й**эс/**jj**es/**ĵ**ęs |
| й/j       | `й`            | `j`   | ба**й**ес/ba**j**yes/ba**j**es, белы**й**/bely**j**, **й**од/**j**od, **й**иппи/**j**ippi, ба**й**ас/ba**j**as, ба**й**яс/ba**j**yas/ba**j**ąs, баян/bayan/baąn |


### Таблица No.2 (простые составные)

|        | Cyrillic RegEx | Latin RegEx   | Примеры                                                                            |
| ------ | --------------:|:------------- | ---------------------------------------------------------------------------------- |
| е/ye   | `^е`&#124;`(?<=[аяй])е` | `ye` | **е**сли/**ye**sli/**e**sli, бай**е**с/baj**ye**s/baj**e**s, Ра**е**вская/Ra**ye**vskaya/Ra**e**vskaą, зя**е**/zya**ye**/zą**e**, за**е**м/za**ye**m/za**e**m, заём/zayom/zaëm, **е**хо/**ye**ho/eho |
| е/e    | `е`            | `e`           | м**е**х/m**e**h, про**е**кт/pro**e**kt, за**е**зд/za**e**zd                        |
| экс/ex/ęx | `экс`       | `ex`          | **экс**каватор/**ex**kavator/**ęx**kavator, **экс**ель/**ex**elj/**ęx**elj, м**экс**/m**ex**/m**ęx**, экзамен/ekzamen/ękzamen, экзема/ekzema/ękzema, Мексика/Meksika, мех/meh |
| э/e/ę | `^э`&#124;`(?<=[аяйы])э` | `e`  | **эх**о/**eh**o/**ęh**o, а**э**роплан/a**e**roplan/a**ę**roplan, **э**тот/**e**tot/**ę**tot, **э**он/**e**on/**ę**on, **э**кран/**e**kran/**ę**kran, **э**ротика/**e**rotika/**ę**rotika, , й**э**с/jj**e**s/ĵ**ę**s |
| э/ae/ę | `э`            | `ae`          | м**э**р/m**ae**r/m**ę**r, мер/mer, Но**э**ль/No**ae**lj/No**ę**lj, радио**э**хо/radio**ae**ho/radio**ę**ho, ма**э**р/ma**ae**r/ma**ę**r, в**эч**ный/v**aech**nyj/v**ęč**nyj |
| | | | |
| шч/shwch/šwč | `шч`     | `shwch`       | **шч**ётка/**shwch**yotka/**šwč**ëtka                                              |
| щ/shch/šč    | `щ`      | `shch`        | **щ**ётка/**shch**yotka/**šč**ëtka, **cч**ёт/**sch**yot/**sč**ët                   |
| ж/zh | `ж`            | `zh`          | ё**ж**/yo**zh**/ë**ž**, во**зж**и/vo**zzh**i/vo**zž**i, по**зж**е/po**zž**e        |
| ч/ch | `ч`            | `ch`          | **ч**ерныш/**ch**ernysh/**č**ernyš, с**ч**ётная/s**ch**yotnaya/s**č**ëtnaą         |
| ш/sh | `ш`            | `sh`          | **ш**лем/**sh**lem/**š**lem                                                        |
| х/kh | `(?=[хтсшзжцчщъьйк])х` | `kh` | с**х**од/s**kh**od/s**h**od, **кх**е/**kkh**e/**kh**e, си**кх**/si**kkh**/si**kh**, ме**х**/me**h**/me**h**, Муръ**х**ин/Murjhjh**kh**in/Murɉ**h**in, Мурь**х**ин/Murj**kh**in/Murj**h**in, от**х**од/ot**kh**od/ot**h**od |
| х/h  | `х`            | `h`           | **х**о**х**олок/**h**o**h**olok, в**ы**ход/v**y**hod, ме**х**а/me**h**a, э**х**о/e**h**o, вече/veche/veče, меча/mecha/meča, эч/ech/ęč, мэч/maech/męč, **х**ья/**h**jya/**h**ją, **х**ьан/**h**jhan/**h**ʝan |
| | | | |
| ё/jo | `(?<=\c)ё`     | `je`          | м**ё**д/m**jo**d |
| ё/yo | `ё`            | `yo`          | **ё**мко/**yo**mko |
| ю/ju | `(?<=\c)ю`     | `ju`          | м**ю**сли/m**ju**sli |
| ю/yu | `ю`            | `yu`          | **Ю**ля/**Yu**lja |
| я/ja | `(?<=\c)я`     | `ja`          | Из**я**/Iz**ja** |
| я/ya | `я`            | `ya`          | **Я**корь/**Ya**korj |
| ERR  |                | `[qwx]`       |                  |


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
