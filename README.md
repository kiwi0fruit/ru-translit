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
* ъe/ъя в разрешённых русским языком местах кодировались wje/wja,
* ьe/ья в типичных местах кодировались jye/jya,
* ыe/ыя в типичных местах кодировались yje/yja,
* э кодировалась как ae.
* нетипичное использование русских букв можно было закодировать контекстно-независимыми обозначения типа й/jj, ы/yw, ъ/wjh, ь/jh,
* НО, в итоге из-за логики кодирования й,ъ,ы,ъ и э пришлось е кодировать как "e" только после согласных. И э кодировать как "ae" тоже только после согласных.


## Кириллица <=> латиница

Главной целью проекта была обратимая транслитерация в английский алфавит, близкая к английскому чтению (в скобках указана минималистичные диактритические знаки, улучшающие чтение и доступные в клавиатуре Google).

| **a** | **б** | **в** | **г** | **д** | **з** | **к** | **л** | **м** |
|:-----:|:-----:|:-----:|:-----:|:-----:|:-----:|:-----:|:-----:|:-----:|
|   a   |   b   |   v   |   g   |   d   |   z   |   k   |   l   |   m   |
| **н** | **о** | **п** | **р** | **с** | **т** | **у** | **ф** | **ц** |
|   n   |   o   |   p   |   r   |   s   |   t   |   u   |   f   |   c   |

Краткая версия (сьч - техническая замена для обратимости):

|   **е**    | **ё** | **ж** |  **и**  | **й** | **х** |  **ч**  |  **ш**  | **щ** |
|:----------:|:-----:|:-----:|:-------:|:-----:|:-----:|:-------:|:-------:|:-----:|
| е/ye/je/we | yo/jo |  zh   | i/yi/ji | j/jj  | h/kh  |   ch    |   sh    | sjch  |
|   **ъ**    | **ы** | **ь** |  **э**  | **ю** | **я** | **экс** | **сьч** |       |
|  j/wj/wjh  | y/yw  | j/jh  |  ae/e   | yu/ju | ya/ja |   ex    |  sjwch  |       |

Подробнее:

| **е/сье/ые/съе/се/е=[ɛ]=[э]** | **ё/сьё/ыё/съё** | **и/сьи/сыи/аыи/съи** |
|:-----------------------------:|:----------------:|:---------------------:|
|    ye/sjye/yje/swje/se/we     | yo/sjyo/yjo/swjo |  i/sji/syi/aywi/swji  |
|       **ю/сью/ыю/съю**        | **я/сья/ыя/съя** |     **э/сэ/экс**      |
|       yu/sjyu/yju/swju        | ya/sjya/yja/swja |       e/sae/ex        |

| **й/сй/ыйа** | **съе/със/съа/съи**  | **ы/ые/ыа/ыи** | **ь/сье/ь/сьи** |
|:------------:|:--------------------:|:--------------:|:---------------:|
|  j/sjj/yjja  | swje/swjs/swjha/swji |  y/yje/ywa/yi  |  j/sjye/jh/sji  |

Многие буквы совпадают с [ГОСТ 16876-71 табл. 2](https://ru.wikipedia.org/wiki/%D0%A2%D1%80%D0%B0%D0%BD%D1%81%D0%BB%D0%B8%D1%82%D0%B5%D1%80%D0%B0%D1%86%D0%B8%D1%8F_%D1%80%D1%83%D1%81%D1%81%D0%BA%D0%BE%D0%B3%D0%BE_%D0%B0%D0%BB%D1%84%D0%B0%D0%B2%D0%B8%D1%82%D0%B0_%D0%BB%D0%B0%D1%82%D0%B8%D0%BD%D0%B8%D1%86%D0%B5%D0%B9#%D0%A1%D1%80%D0%B0%D0%B2%D0%BD%D0%B8%D1%82%D0%B5%D0%BB%D1%8C%D0%BD%D0%B0%D1%8F_%D1%82%D0%B0%D0%B1%D0%BB%D0%B8%D1%86%D0%B0_%D1%81%D0%B8%D1%81%D1%82%D0%B5%D0%BC_%D1%82%D1%80%D0%B0%D0%BD%D1%81%D0%BB%D0%B8%D1%82%D0%B5%D1%80%D0%B0%D1%86%D0%B8%D0%B8) или [ГОСТ 7.79-2000 сист. Б](https://ru.wikipedia.org/wiki/%D0%A2%D1%80%D0%B0%D0%BD%D1%81%D0%BB%D0%B8%D1%82%D0%B5%D1%80%D0%B0%D1%86%D0%B8%D1%8F_%D1%80%D1%83%D1%81%D1%81%D0%BA%D0%BE%D0%B3%D0%BE_%D0%B0%D0%BB%D1%84%D0%B0%D0%B2%D0%B8%D1%82%D0%B0_%D0%BB%D0%B0%D1%82%D0%B8%D0%BD%D0%B8%D1%86%D0%B5%D0%B9#%D0%A1%D1%80%D0%B0%D0%B2%D0%BD%D0%B8%D1%82%D0%B5%D0%BB%D1%8C%D0%BD%D0%B0%D1%8F_%D1%82%D0%B0%D0%B1%D0%BB%D0%B8%D1%86%D0%B0_%D1%81%D0%B8%D1%81%D1%82%D0%B5%D0%BC_%D1%82%D1%80%D0%B0%D0%BD%D1%81%D0%BB%D0%B8%D1%82%D0%B5%D1%80%D0%B0%D1%86%D0%B8%D0%B8).

Алфавит транслитерации состоит из **25** букв (английский алфавит без Qq).

***Слово на латинице является грамматически верным если:***

1. его образ от прообраза совпадает с самим словом (`lat_word == RUtoEN(ENtoRU(lat_word))`),
2. его прообраз грамматически верен (`ENtoRU(lat_word)`).

Так же нужно специальное правило для аббревиатур: АЭС/AES, АЕС/AES, ФМШ/FMS, ЭЮЯ/EUA, ЁМ/EM (не OM).
То есть, использовать не модификатор а модифицируемую букву (отбросить диакритический знак в латинице). Так же не стоит забывать, что все слова с буквой ё могут быть корректно написаны с буквой е, так что yo становится E в качестве общего знаменателя.


## Примеры текстов в транслитерации

*По-моему, это вариант гораздо лучше подходит для русско-английских билингвов, чем варианты с большим количеством диакритических знаков. В английском нет диакритики, в русском - почти нет (ё ставят только при опасности неправильного прочтения, й трудно считать диакритикой). Так что не удивительно, что диакритика будет вызывать отторжение. В варианте минималистичной диакритики она ставится тоже в очень малом числе случаев.*

Pjyanyj master po proektu sdelal mehanicheskij objekt s izjanom. Yesli brak ne obnaruzhitsya, to belyj bolid boljshe ne smozhet vyigryvatj gonki.

V pjyese pro devushku v zelyonom platjyice vse sadilisj na ladjyi i plyli po reke. No tut iz lesa vyshel konj v paljto, kotoryj cho-to vyiskival, i prikazal vsem mytjsya i gotovitj buljyion. Znachit snova pjyom.

Prepodobnyj Bajyes podkinul igraljnyje kosti. Vypalo shestj, znachit yemu pridyotsya mazatj jod na ranu.

Męr neboljshogo gorodishki otkryl tablicu exelya i vozmutilsya cenoj novogo exkavatora. Azh ekzema snova stala yego bespokoitj. Oh uzh eta pokupka vechnogo dvigatelya v proshlom godu! A tak zhe pokupka aeroplana-ekranolyota. Yesli tak pojdyot i daljshe, to byudzhetu pridyotsya hudo.

V etom vide fraza ot A to Ya nachinayet vyglyadetj sovsem po-drugomu. Sejchas şhyotka novaya, no pozzhe ona stanet staraya. Chernysh lyubit kogda yego cheshut yeyu. Yozh kolyuchij i pohozh na neyo.

Skhod mestnyh zhitelej indijskoj derevni sikkhov reshal chto zhe delatj s otkhodami kompanii "Gaj Yulij Cezarj". Odin iz prisutstvuyuşhih nosil hoholok na golove. On i nashyol vyhod iz situacii.

"Kto s mechom k nam pridyot, tot ot mecha i..." - ne smog dogovoritj starshij mehanik Vasilij.

Imeyetsya neskoljko gipotez proiskhozhdeniya sobaki, naiboleye veroyatnymi yeyo predkami schitayutsya volk i nekotoryje vidy shakalov.

V suzhdeniyah uchyonyh o predkah domashnej sobaki prisutstvuyut dve tochki zreniya. Odni schitayut, chto sobaki - polifileticheskaya gruppa (proiskhodyaşhaya ot neskoljkih predkov), drugie priderzhivayutsya mneniya, chto vse sobaki proizoshli ot odnogo predka (monofileticheskaya teoriya).


### Альтернативный вариант

Частые новые буквы: Çç(Ц), Ęę(Э), Şş(Щ), Įį(Йот,Ь). Неиспользуемые старые: Ww, Qq. Буквы для аббревиатур: Â(Я),Ê(Е),Ô(Ё),Û(Ю),Ĉ(Ч),Ĥ(Х),Ŝ(Ш),Ẑ(Ж),Ŷ(Й) (для Yy(Ы), Įį(Ь) диакритики для аббревиатур нет). Примечательные старые: Jj(Ъ).

Pįyanyį master po proectu sdelal mehanichesciy object s izjanom. Įesli brac ne obnaruzhitsįa, to belyį bolid bolįshe ne smozhet vyigryvatį gonci.

V pįyese pro devushcu v zelįonom platįyiçe vse sadilisį na ladįyi i plyli po rece. No tut iz lesa vyshel conį v palįto, cotoryį cho-to vyiscival, i pricazal vsem mytįsįa i gotovitį bulįjon. Znachit snova pįyom.

Prepodobnyį Bayįes podcinul igralįnyįe costi. Vypalo shestį, znachit įemu pridįotsįa mazatį yod na ranu.

Męr nebolįshogo gorodishci otcryl tabliçu exelįa i vozmutilsįa çenoy novogo excavatora. Azh eczema snova stala įego bespocoitį. Oh uzh eta pocupca vechnogo dvigatelįa v proshlom godu! A tac zhe pocupca aeroplana-ecranolįota. Įesli tac poydįot i dalįshe, to bįudzhetu pridįotsįa hudo.

V etom vide fraza ot A to Įa nachinaįet vyglįadetį sovsem po-drugomu. Seychas şhįotca novaįa, no pozzhe ona stanet staraįa. Chernysh lįubit cogda įego cheshut įeįu. Įozh colįuchiy i pohozh na neįo.

Skhod mestnyh zhiteley indiyscoy derevni sickhov reshal chto zhe delatį s otkhodami companii "Gay Įuliy Çezarį". Odin iz prisutstvuįuşhih nosil hoholoc na golove. On i nashįol vyhod iz situaçii.

"Cto s mechom c nam pridįot, tot ot mecha i..." - ne smog dogovoritį starshiy mehanic Vasiliy.

Imeįetsįa nescolįco gipotez proiskhozhdeniįa sobaci, naiboleįe veroįatnymi įeįo predcami schitaįutsįa volc i necotoryįe vidy shacalov.

V suzhdeniįah uchįonyh o predcah domashney sobaci prisutstvuįut dve tochci zreniįa. Odni schitaįut, chto sobaci - polifiletichescaįa gruppa (proiskhodįaşhaįa ot nescolįcih predcov), drugiįe priderzhivaįutsįa mneniįa, chto vse sobaci proizoshli ot odnogo predca (monofiletichescaįa teoriįa).


## Кириллица => латиница

Пока что это только зачатки двух алгоритмов прямого и обратного пребразования.

### Таблица No.1 (сложные составные: й,ъ,ы,ь=>j,y)

`\c` - согласная (consonant), но не йот. Специальный символ регулярных выражений для `[qwrtpsdfghklzxcvbnmцкнгшщзхфвпрлджчсмтб]` (но без й, j).

|                                  |              Cyrillic RegEx | Translit RE / Latiniça RE | Примеры                                                                                                                                                 |
| -------------------------------- | ---------------------------:|:------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------- |
| ъ[еёюя] / j[eoua]                |            `(?<=\c)ъ[еёюя]` | `j[eoua]`                 | (после согласных перед йотированными гласными) объект/objekt/object, изъян/izjan                                                                        |
| ъ/wj/j                           |               `ъ(?=[\w\c])` | `wj` / `j`                | (перед согласными или в конце слова) онъ/onwj/onj, Муъминат/Muwjminat/Mujminat                                                                          |
| ъи/ji                            |                   `объимат` | `objimat`                 | (исключения отображения; йотированные) объимать/objimatj/objimatį                                                                                       |
| ъ/wjh/ĵ                          |                         `ъ` | `wjh` / `ĵ`               | (не йотированные) объизвестить/obwjhizvestitj/obĵizvestitį, Йонъин/Jonwjhin/Yonĵin, Чанъань/Chanwjhanj/Chanĵanį                                         |
|                                  |                             |                           |                                                                                                                                                         |
| ь[еёюяи] / jy[eouai] / įy[eouai] |           `(?<=\c)ь[еёюяи]` | `jy[eouai]` / `įy[eouai]` | (после согласных перед и или йотированными гласными) пьеса/pjyesa/pįyesa, пьян/pjyan/pįyan, ладьи/ladjyi/ladįyi, платьице/platjyice/platįyiçe           |
| ьо/jyio                          |                 `(?<=\c)ьо` | `jyio` / `įjo`            | (после согласных перед о) батальон/bataljyion/batalįjon, лосьон/losjyion/losįjon, сеньор/senjyior/senįjor                                               |
| ь/j                              |        `(?<=\c)ь(?=[\w\c])` | `j` / `į`                 | (после согласных перед согласными или в конце слова) прячься/pryachjsya/prįachįsįa, мыться/mytjsya/mytįsįa, конь/konj/konį                              |
| ь/jh                             |                         `ь` | `jh`                      | Мурьйин/Murjhjin/Murįhyin, Чаньын/Сhanjhyn/Сhanįhyn (придуманные слова)                                                                                 |
|                                  |                             |                           |                                                                                                                                                         |
| ые/yje, ыё/yjo, ыю/yju, ыя/yja   |             `(?<!ы)ы[еёюя]` | `yj[eoua]`                | бел**ые**/bel**yje**, бедн**ыя**/bedn**yja**                                                                                                            |
| ы/yw(ŷ)                          |               `ы(?=[эоуа])` | `yw`                      | Нарва-Й**ыэ**суу/Narva-J**ywe**suu/Narva-J**ŷe**suu, Баймакл**ыа**ул/Bajmakl**ywa**ul/Bajmakl**ŷa**ul                                                   |
| ыи/ywi(ŷi)                       |              `(?<![й\c])ыи` | `ywi`                     | а**ыи**/a**ywi**/a**ŷi**, сь**ыи**о/sj**ywi**o                                                                                                          |
| ыи/yi                            |              `(?<=[й\c])ыи` | `yi`                      | в**ыи**грывать/v**yi**gryvatj, в**ыи**скивать/v**yi**skivatj                                                                                            |
| ы/y                              |                         `ы` | `y`                       | кр**ы**ска/kr**y**ska, **ы**пся/**y**psja, п**ы**хтел/p**y**htel, бел**ы**й/bel**y**j, в**ы**йигрывать/v**y**jigryvatj, ба**й**ыс/ba**j**ys             |
|                                  |                             |                           |                                                                                                                                                         |
| й/jj                             | `(?<=[й\c])й`&#124;`й(?=й)` | `jj`                      | под**й**езд/pod**jj**yezd, под**й**од/pod**jj**od, Мур**й**ин/Mur**jj**in, под**йй**од/pod**jjjj**od                                                    |
| й/jj                             |         `(?<=ы)й(?=[эоуа])` | `jj`                      | белы**й**а/bely**jj**a, белы**й**э/bely**jj**e, белыйе/belyjye                                                                                          |
| й/j                              |                         `й` | `j`                       | ба**й**ес/ba**j**yes, белы**й**/bely**j**, **й**од/**j**od, **й**иппи/**j**ippi, ба**й**яс/ba**j**yas, ба**й**ас/ba**j**as, **й**эс/**j**es, баян/bayan |


### Таблица No.2 (простые составные)

|                  |                         Cyrillic RegEx | Translit RE / Latiniça RE | Примеры                                                                                                                                                                                                                             |
| ---------------- | --------------------------------------:|:------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| проект/.../we(ê) |                    `проект`&#124;`...` | `we`                      | про**е**кт/pro**we**kt/pro**ê**kt (слова, которые должны были быть с `ye`, но произносятся с **ударным** "э")                                                                                                                       |
| е/ye             |                   `^е`&#124;`(?<!\c)е` | `ye`                      | **е**сли/**ye**sli, бай**е**с/baj**ye**s, Ра**е**вская/Ra**ye**vskaya, зя**е**/zja**ye**, за**е**м/za**ye**m, заём/zayom, **е**хо/**ye**ho, йeс/j**ye**s, та**е**ц/ta**ye**c, за**е**зд/za**ye**zd, тра**е**ктория/tra**ye**ktoriya |
| е/e              |                                    `е` | `e`                       | м**е**х/m**e**h                                                                                                                                                                                                                     |
| экс/ex           |                                  `экс` | `ex`                      | **экс**каватор/**ex**kavator, **экс**ель/**ex**elj, м**экс**/m**ex**, экзамен/ekzamen, экзема/ekzema, Мексика/Meksika, мех/meh                                                                                                      |
| э/e              |                   `^э`&#124;`(?<!\c)э` | `e`                       | **эх**о/**eh**o, а**э**роплан/a**e**roplan, **э**тот/**e**tot, **э**он/**e**on, **э**кран/**e**kran, **э**ротика/**e**rotika, й**э**с/j**e**s, Но**э**ль/No**e**lj, ало**э**/alo**e**, радио**э**хо/radio**e**ho                    |
| э/ae(ę)          |                           `(?<=\cа*)э` | `ae`                      | м**э**р/m**ae**r/m**ę**r, мер/mer, ма**э**р/ma**ae**r/ma**ę**r, маа**э**р/maa**ae**r/maa**ę**r, маер/mayer/maer, моаэр/moaer                                                                                                        |
|                  |                                        |                           |                                                                                                                                                                                                                                     |
| сьч/sjwch        |                                  `сьч` | `sjwch`                   | **сьч**/**sjwch** (в случае с диакритикой эта замена не нужна)                                                                                                                                                                      |
| щ/sjch(şch)      |                                    `щ` | `sjch`                    | **щ**ётка/**sjch**jotka/**şch**jotka, счёт/schjot                                                                                                                                                                                   |
| ж/zh             |                                    `ж` | `zh`                      | ё**ж**/yo**zh**, во**зж**и/vo**zzh**i, по**зж**е/po**zzh**e                                                                                                                                                                         |
| ч/ch             |                                    `ч` | `ch`                      | **ч**ерныш/**ch**ernysh, с**ч**ётная/s**ch**jotnaya                                                                                                                                                                                 |
| ш/sh             |                                    `ш` | `sh`                      | **ш**лем/**sh**lem                                                                                                                                                                                                                  |
| х/kh             | `(?=[хтсшзжцчщъьйк])х`&#124;`(?=экс)x` | `kh`                      | с**х**од/s**kh**od, **кх**е/**kkh**e, си**кх**/si**kkh**, ме**х**/me**h**, Муръ**х**ин/Murwjh**kh**in, Мурь**х**ин/Murj**kh**in, от**х**од/ot**kh**od                                                                               |
| х/h              |                                    `х` | `h`                       | **х**о**х**олок/**h**o**h**olok, в**ы**ход/v**y**hod, ме**х**а/me**h**a, э**х**о/e**h**o, вече/veche, меча/mecha, эч/ech, мэч/maech, **х**ья/**h**jya, **х**ьан/**h**jan                                                            |
|                  |                                        |                           |                                                                                                                                                                                                                                     |
| ё/yo             |                                    `ё` | `yo`                      | м**ё**д/m**jo**d, **ё**мко/**yo**mko                                                                                                                                                                                                |
| ю/yu             |                                    `ю` | `yu`                      | м**ю**сли/m**yu**sli, **Ю**ля/**Yu**lja                                                                                                                                                                                             |
| я/ya             |                                    `я` | `ya`                      | Из**я**/Iz**ya**, **Я**корь/**Ya**korj, ба**я**н/ba**ya**n                                                                                                                                                                          |
| ERR              |                                        | `[qwx]`                   |                                                                                                                                                                                                                                     |


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
