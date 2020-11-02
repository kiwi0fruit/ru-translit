# ru-translit (kiwi0fruit's)

### Uniquely reversible Russian to English transliteration (no extra letters, diacritics and non-letters)

### Однозначно обратимая транслитерация из русского в английский алфавит (без дополнительных букв, диакритических и небуквенных знаков)

Придумал в качестве развлечения ещё один транслит.

Развлечением было удовлетворить ограничениям:

* Транслит - полностью обратимый (является кодировкой без потерь и позволяет точно восстановить произвольный русский текст из латиницы). То есть, это [**инъективное отображение**](https://ru.wikipedia.org/wiki/%D0%98%D0%BD%D1%8A%D0%B5%D0%BA%D1%86%D0%B8%D1%8F_(%D0%BC%D0%B0%D1%82%D0%B5%D0%BC%D0%B0%D1%82%D0%B8%D0%BA%D0%B0)),
* Транслит содержит только буквы (в частности, не использует апостроф): отображение из русских букв `[А-Яа-я]` в английские `[A-Za-z]` без добавлений,
* Не содержит далёких фонетических замен типа щ → w. Желательно, чтобы "звучало" похоже на английский или математический латинский.

Когда составлял правила хотелось, чтобы:

* х в контекстах, где её нельзя перепутать с составными буквами, кодировалась h, а иначе – kh,
* j после согласных означала ь, а в остальных случаях – й или йот,
* ы кодировалась как y.
* ъe/ъя в разрешённых русским языком местах кодировались wje/wja(ĵe/ĵa),
* ьe/ья в типичных местах кодировались jye/jya,
* ыe/ыя в типичных местах кодировались yje/yja,
* э кодировалась как ae(ę).
* нетипичное использование русских букв можно было закодировать контекстно-независимыми обозначения типа й/jj, ы/yw(ŷ), ъ/wjh(ĵh), ь/jh,
* НО, в итоге из-за логики кодирования й,ъ,ы,ъ и э пришлось е кодировать как "e" только после согласных. И э кодировать как "ae" тоже только после согласных.


## Кириллица <=> латиница

Главной целью проекта была обратимая транслитерация в английский алфавит, близкая к английскому чтению (в скобках указана минималистичные диактритические знаки, улучшающие чтение и доступные в клавиатуре Google).

| **a** | **б** | **в** | **г** | **д** | **з** | **к** | **л** | **м** |
|:-----:|:-----:|:-----:|:-----:|:-----:|:-----:|:-----:|:-----:|:-----:|
| a     | b     | v     | g     | d     | z     | k     | l     | m     |
| **н** | **о** | **п** | **р** | **с** | **т** | **у** | **ф** | **ц** |
| n     | o     | p     | r     | s     | t     | u     | f     | c     |

Краткая версия (шч и ьь - технические замены для обратимости):

| **е**   | **ё** | **ж** | **и**   | **й** | **х** | **ч**   | **ш**   | **щ**   | 
|:-------:|:-----:|:-----:|:-------:|:-----:|:-----:|:-------:|:-------:|:-------:|
| е/ye/je | yo/jo | zh    | i/yi/ji | j/jj  | h/kh  | ch      | sh      | shch(şch)    |
| **ъ**   | **ы** | **ь** | **э**   | **ю** | **я** | **экс** | **шч**  |   |
| j/wj(ĵ)/wjh(ĵh) | y/yw(ŷ) | j/jh  | ae(ę)/e    | yu/ju | ya/ja | ex      | shwch(shch)   |    |

Подробнее:

| **е/сье/ые/съе/сe**  | **ё/сьё/ыё/съё/сё**  | **и/сьи/сыи/аыи/съи** |
|:--------------------:|:--------------------:|:---------------------:|
| ye/sjye/yje/swje(sĵe)/se  | yo/sjyo/yjo/swjo(sĵo)/sjo | i/sjyi/syi/aywi(aŷi)/swji(sĵi)  |
| **ю/сью/ыю/съю/сю**  | **я/сья/ыя/съя/ся**  | **э/сэ/экс**       |
| yu/sjyu/yju/swju(sĵu)/sju | ya/sjya/yja/swja(sĵu)/sja | e/sae(sę)/ex           |

| **й/сй/ыйа** | **съе/със/съа/съи**  | **ы/ые/ыа/ыи** | **ь/сье/ь/сьи** |
|:------------:|:--------------------:|:--------------:|:---------------:|
| j/sjj/yjja   | swje(sĵe)/swjs(sĵs)/swjha(sĵha)/swji(sĵi) | y/yje/ywa(ŷa)/yi   | j/sjye/jh/sjyi  |

Многие буквы совпадают с [ГОСТ 16876-71 табл. 2](https://ru.wikipedia.org/wiki/%D0%A2%D1%80%D0%B0%D0%BD%D1%81%D0%BB%D0%B8%D1%82%D0%B5%D1%80%D0%B0%D1%86%D0%B8%D1%8F_%D1%80%D1%83%D1%81%D1%81%D0%BA%D0%BE%D0%B3%D0%BE_%D0%B0%D0%BB%D1%84%D0%B0%D0%B2%D0%B8%D1%82%D0%B0_%D0%BB%D0%B0%D1%82%D0%B8%D0%BD%D0%B8%D1%86%D0%B5%D0%B9#%D0%A1%D1%80%D0%B0%D0%B2%D0%BD%D0%B8%D1%82%D0%B5%D0%BB%D1%8C%D0%BD%D0%B0%D1%8F_%D1%82%D0%B0%D0%B1%D0%BB%D0%B8%D1%86%D0%B0_%D1%81%D0%B8%D1%81%D1%82%D0%B5%D0%BC_%D1%82%D1%80%D0%B0%D0%BD%D1%81%D0%BB%D0%B8%D1%82%D0%B5%D1%80%D0%B0%D1%86%D0%B8%D0%B8) или [ГОСТ 7.79-2000 сист. Б](https://ru.wikipedia.org/wiki/%D0%A2%D1%80%D0%B0%D0%BD%D1%81%D0%BB%D0%B8%D1%82%D0%B5%D1%80%D0%B0%D1%86%D0%B8%D1%8F_%D1%80%D1%83%D1%81%D1%81%D0%BA%D0%BE%D0%B3%D0%BE_%D0%B0%D0%BB%D1%84%D0%B0%D0%B2%D0%B8%D1%82%D0%B0_%D0%BB%D0%B0%D1%82%D0%B8%D0%BD%D0%B8%D1%86%D0%B5%D0%B9#%D0%A1%D1%80%D0%B0%D0%B2%D0%BD%D0%B8%D1%82%D0%B5%D0%BB%D1%8C%D0%BD%D0%B0%D1%8F_%D1%82%D0%B0%D0%B1%D0%BB%D0%B8%D1%86%D0%B0_%D1%81%D0%B8%D1%81%D1%82%D0%B5%D0%BC_%D1%82%D1%80%D0%B0%D0%BD%D1%81%D0%BB%D0%B8%D1%82%D0%B5%D1%80%D0%B0%D1%86%D0%B8%D0%B8).

Алфавит транслитерации состоит из **25** букв (английский алфавит без Qq). Минималистичная диакритика требует еще 4 символа (Ęę,Ĵĵ,Şş,Ŷŷ), но уже не нуждается в Ww. Итого **28** букв. Если делать специальную раскладку клавиатуры, то клавишу `]/Ъ` заменить на Ĵĵ, `W/Ц` заменить на Şş, `[/Х` заменить на Ŷŷ, `Q/Й` заменить на Ęę,

***Слово на латинице является грамматически верным если:***

1. его образ от прообраза совпадает с самим словом (`lat_word == RUtoEN(ENtoRU(lat_word))`),
2. его прообраз грамматически верен (`ENtoRU(lat_word)`).

Так же нужно специальное правило для аббревиатур: АЭС/AES, АЕС/AES, ФМШ/FMS, ЭЮЯ/EUA, ЁМ/EM (не OM).
То есть, использовать не модификатор а модифицируемую букву (отбросить диакритический знак в латинице). Так же не стоит забывать, что все слова с буквой ё могут быть корректно написаны с буквой е, так что yo становится E в качестве общего знаменателя.


## Примеры текстов в транслитерации

*По-моему, это вариант гораздо лучше подходит для русско-английских билингвов, чем варианты с диакритическими знаками. В английском нет диакритики, в русском - почти нет (ё никто не ставит, оставшуюся й трудно считать диакритикой). Так что не удивительно, что диакритика будет вызывать отторжение.*

Pjyanyj master po prowektu sdelal mehanicheskij obwjekt s izwjanom. Yesli brak ne obnaruzhitsja, to belyj bolid boljshe ne smozhet vyigryvatj gonki.

DIAC: Pjyanyj master po proektu sdelal mehanicheskij obĵekt s izĵanom.

V pjyese pro devushku v zeljonom platjyice vse sadilisj na ladjyi i plyli po reke. No tut iz lesa vyshel konj v paljto i prikazal vsem mytjsja.

Prepodobnyj Bajyes podkinul igraljnyje kosti. Vypalo shestj, znachit yemu pridjotsja mazatj jod na ranu.

Maer neboljshogo gorodishki otkryl tablicu exelja i vozmutilsja cenoj novogo exkavatora. Azh ekzema snova stala yego bespokoitj. Oh uzh eta pokupka vechnogo dvigatelja v proshlom godu! A tak zhe pokupka aeroplana-ekranoljota. Yesli tak pojdjot i daljshe, to bjudzhetu pridjotsja hudo.

DIAC: Męr neboljshogo gorodishki otkryl tablicu exelja. A tak zhe pokupka aęroplana-ekranoljota.

V etom vide fraza ot A to Ya nachinayet vygljadetj sovsem po-drugomu. Sejchas shchjotka novaya, no pozzhe ona stanet staraya. Chernysh ljubit kogda yego cheshut yeyu. Yozh koljuchij i pohozh na neyo.

DIAC: V etom vide fraza ot A to Ya nachinaet vygljadetj sovsem po-drugomu. Sejchas şchjotka novaya, no pozzhe ona stanet staraya.

Skhod mestnyh zhytelej indijskoj derevni sikkhov reshal chto zhe delatj s otkhodami kompanii "The LLC". Odin iz prisutstvuyushchih nosil hoholok na golove. On i nashjol vyhod iz situacii.

DIAC: Odin iz prisutstvuyuşchih nosil hoholok na golove.

"Kto s mechom k nam pridjot, tot ot mecha i..." - ne smog dogovoritj starshij mehanik Vasilij.

Imeyetsja neskoljko gipotez proiskhozhdeniya sobaki, naiboleye veroyatnymi yeyo predkami schitayutsja volk i nekotoryje vidy shakalov.

DIAC: Imeetsja neskoljko gipotez proiskhozhdeniya sobaki, naibolee veroyatnymi yeyo predkami schitayutsja volk i nekotoryje vidy shakalov.

V suzhdeniyah uchjonyh o predkah domashnej sobaki prisutstvuyut dve tochki zreniya. Odni schitayut, chto sobaki - polifileticheskaya gruppa (proiskhodjashchaya ot neskoljkih predkov), drugie priderzhivayutsja mneniya, chto vse sobaki proizoshli ot odnogo predka (monofileticheskaya teoriya).

DIAC: proiskhodjaşchaya ot neskoljkih predkov


## Кириллица => латиница

Пока что это только зачатки двух алгоритмов прямого и обратного пребразования.

### Таблица No.1 (сложные составные: й,ъ,ы,ь=>j,y)

`\c` - согласная (consonant), но не йот. Специальный символ регулярных выражений для `[qwrtpsdfghklzxcvbnmцкнгшщзхфвпрлджчсмтб]` (но без й, j).

|        | Cyrillic RegEx | Latin RegEx | Примеры                                      |
| ------ | --------------:|:----- | -------------------------------------------- |
| ъе/wje(ĵe), ъё/wjo(ĵo), ъи/wji(ĵi), ъю/wju(ĵu), ъя/wja(ĵa) | `(?<=\c)ъ[еёюяи]` | `(?<=\c)wj[eouai]` | об**ъе**кт/ob**wje**kt/ob**ĵe**kt, из**ъя**н/iz**wja**n/iz**ĵa**n, мера/mera, если/yesli, зяка/zjaka, Мур**ъи**н/Mur**wji**n/Mur**ĵi**n |
| ъ/wj(ĵ)  | `ъ(?![эоуайы])` | `wj ` | он**ъ**/on**wj**/on**ĵ**, Му**ъ**минат/Mu**wj**minat/Mu**ĵ**minat |
| ъ/wjh(ĵh)  | `ъ`            | `wjh` | Чан**ъ**ань/Chan**wjh**anj/Chan**ĵh**anj, Мур**ъ**йин/Mur**wjh**jin/Mur**ĵh**jin |
| | | | |
| ье/jye, ьё/jyo, ьи/jyi, ью/jyu, ья/jya | `(?<=\c)ь[еёюяи]` | `(?<=\c)jy[eouai]` | п**ье**са/p**jye**sa, п**ья**н/p**jya**n, лад**ьи**/lad**jyi**, плат**ьи**це/plat**jyi**ce, Мур**ьи**н/Mur**jyi**n |
| ь/j    | `(?<=\c)ь(?![эоуaйы])` | `(?<=\c)j` | пряч**ь**ся/prjach**j**sja, мыт**ь**ся/myt**j**sja, кон**ь**/kon**j** |
| ь/jh   | `ь`            | `jh`  | батал**ь**он/batal**jh**on, сен**ь**ор/sen**jh**or, Чан**ь**ол/Сhan**jh**ol, Мур**ьй**ин/Mur**jhj**in, Чан**ь**ын/Сhan**jh**yn |
| | | | |
| ые/yje, ыё/yjo, ыю/yju, ыя/yja | `(?<!ы)ы[еёюя]` | `yj[eoua]` | бел**ые**/bel**yje**, бедн**ыя**/bedn**yja** |
| ы/yw(ŷ)   | `ы(?=[эоуа])`  | `yw`  | Нарва-Й**ыэ**суу/Narva-J**ywe**suu/Narva-J**ŷe**suu, Баймакл**ыа**ул/Bajmakl**ywa**ul/Bajmakl**ŷa**ul |
| ыи/ywi(ŷi) | `(?<![й\c])ыи` | `ywi` | а**ыи**/a**ywi**/a**ŷi** |
| ыи/yi  | `(?<=[й\c])ыи` | `yi`  | в**ыи**грывать/v**yi**gryvatj, в**ыи**скивать/v**yi**skivatj |
| ы/y    | `ы`            | `y`   | кр**ы**ска/kr**y**ska, **ы**пся/**y**psja, п**ы**хтел/p**y**htel, бел**ы**й/bel**y**j, в**ы**йигрывать/v**y**jigryvatj, ба**й**ыс/ba**j**ys |
| | | | |
| й/jj   | `(?<=\c)й`     | `jj`  | под**й**езд/pod**jj**yezd, под**й**од/pod**jj**od, Мур**й**ин/Mur**jj**in, под**йй**од/pod**jjj**od |
| й/jj   | `(?<=ы)й(?=[эоуа])` | `jj` | белы**й**а/bely**jj**a, белы**й**э/bely**jj**e, белыйе/belyjye  |
| й/j    | `й`            | `j`   | ба**й**ес/ba**j**yes, белы**й**/bely**j**, **й**од/**j**od, **й**иппи/**j**ippi, ба**й**яс/ba**j**yas, ба**й**ас/ba**j**as, **й**эс/**j**es, баян/bayan |


### Таблица No.2 (простые составные)

|        | Cyrillic RegEx | Latin RegEx   | Примеры                                                                            |
| ------ | ------------:|:------------- | ---------------------------------------------------------------------------------- |
| проект/.../we(e) | `проект`&#124;`...` | `we` | про**е**кт/pro**we**kt/pro**e**kt (слова, которые должны были быть с `ye`, но произносятся с **ударным** "э") (в случае с диакритикой эта замена не нужна) |
| е/ye(ye/e) | `^е`&#124;`(?<!\c)е` | `ye`  | **е**сли/**ye**sli, бай**е**с/baj**ye**s, Ра**е**вская/Ra**ye**vskaya/Ra**e**vskaya, зя**е**/zja**ye**/zja**e**, за**е**м/za**ye**m/za**e**m, заём/zayom, **е**хо/**ye**ho, йeс/j**ye**s, та**е**ц/ta**ye**c/ta**e**c, за**е**зд/za**ye**zd/za**e**zd, тра**е**ктория/tra**ye**ktoriya/tra**e**ktoriya (в случае с диакритикой е после гласных можно брать просто "e") |
| е/e    | `е`          | `e`           | м**е**х/m**e**h |
| экс/ex | `экс`        | `ex`          | **экс**каватор/**ex**kavator, **экс**ель/**ex**elj, м**экс**/m**ex**, экзамен/ekzamen, экзема/ekzema, Мексика/Meksika, мех/meh |
| э/e    | `^э`&#124;`(?<!\c)э` | `e`   | **эх**о/**eh**o, а**э**роплан/a**e**roplan/a**ę**roplan, **э**тот/**e**tot, **э**он/**e**on, **э**кран/**e**kran, **э**ротика/**e**rotika, й**э**с/j**e**s, Но**э**ль/No**e**lj/No**ę**lj, ало**э**/alo**e**/alo**ę**, радио**э**хо/radio**e**ho/radio**ę**ho (с диакритикой э после гласных всегда должна всегда быть в варианте ę - чтобы убрать необходимость в we) |
| э/ae(ę)   | `(?<=\cа*)э` | `ae`          | м**э**р/m**ae**r/m**ę**r, мер/mer, ма**э**р/ma**ae**r/ma**ę**r, маа**э**р/maa**ae**r/maa**ę**r, маер/mayer/maer, моаэр/moaer/moaęr |
| | | | |
| шч/shwch | `шч`       | `shwch`       | **шч**ётка/**shwch**jotka (в случае с диакритикой эта замена не нужна) |
| щ/shch(şch)   | `щ`        | `shch`        | **щ**ётка/**shch**jotka/**şch**jotka, счёт/schjot |
| ж/zh | `ж`            | `zh`          | ё**ж**/yo**zh**, во**зж**и/vo**zzh**i, по**зж**е/po**zzh**e |
| ч/ch | `ч`            | `ch`          | **ч**ерныш/**ch**ernysh, с**ч**ётная/s**ch**jotnaya |
| ш/sh | `ш`            | `sh`          | **ш**лем/**sh**lem |
| х/kh | `(?=[хтсшзжцчщъьйк])х` | `kh`  | с**х**од/s**kh**od, **кх**е/**kkh**e, си**кх**/si**kkh**, ме**х**/me**h**, Муръ**х**ин/Murwjh**kh**in, Мурь**х**ин/Murj**kh**in, от**х**од/ot**kh**od |
| х/h  | `х`            | `h`           | **х**о**х**олок/**h**o**h**olok, в**ы**ход/v**y**hod, ме**х**а/me**h**a, э**х**о/e**h**o, вече/veche, меча/mecha, эч/ech, мэч/maech, **х**ья/**h**jya, **х**ьан/**h**jhan |
| | | | |
| ё/jo | `(?<=\c)ё`     | `je`          | м**ё**д/m**jo**d |
| ё/yo | `ё`            | `yo`          | **ё**мко/**yo**mko |
| ю/ju | `(?<=\c)ю`     | `ju`          | м**ю**сли/m**ju**sli |
| ю/yu | `ю`            | `yu`          | **Ю**ля/**Yu**lja |
| я/ja | `(?<=\c)я`     | `ja`          | Из**я**/Iz**ja** |
| я/ya | `я`            | `ya`          | **Я**корь/**Ya**korj, ба**я**н/ba**ya**n |
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
