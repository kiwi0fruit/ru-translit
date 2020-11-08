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

V pjyese pro devushku v zelyonom platjyice vse sadilisj na ladjyi i plyli po reke. No tut iz lesa vyshel konj v paljto, kotoryj chto-to vyiskival, i prikazal vsem mytjsya i gotovitj buljyion. Znachit snova pjyom.

Prepodobnyj Bajyes podkinul igraljnyje kosti. Vypalo shestj, znachit yemu pridyotsya mazatj jod na ranu.

Męr neboljshogo gorodishki otkryl tablicu exelya i vozmutilsya cenoj novogo exkavatora. Azh ekzema snova stala yego bespokoitj. Oh uzh eta pokupka vechnogo dvigatelya v proshlom godu! A tak zhe pokupka aeroplana-ekranolyota. Yesli tak pojdyot i daljshe, to byudzhetu pridyotsya hudo.

V etom vide fraza ot A to Ya nachinayet vyglyadetj sovsem po-drugomu. Sejchas şhyotka novaya, no pozzhe ona stanet staraya. Chernysh lyubit kogda yego cheshut yeyu. Yozh kolyuchij i pohozh na neyo.

Skhod mestnyh zhitelej indijskoj derevni sikkhov reshal chto zhe delatj s otkhodami kompanii "Gaj Yulij Cezarj". Odin iz prisutstvuyuşhih nosil hoholok na golove. On i nashyol vyhod iz situacii.

"Kto s mechom k nam pridyot, tot ot mecha i..." - ne smog dogovoritj starshij mehanik Vasilij.

Imeyetsya neskoljko gipotez proiskhozhdeniya sobaki, naiboleye veroyatnymi yeyo predkami schitayutsya volk i nekotoryje vidy shakalov.

V suzhdeniyah uchyonyh o predkah domashnej sobaki prisutstvuyut dve tochki zreniya. Odni schitayut, chto sobaki - polifileticheskaya gruppa (proiskhodyaşhaya ot neskoljkih predkov), drugie priderzhivayutsya mneniya, chto vse sobaki proizoshli ot odnogo predka (monofileticheskaya teoriya).


### Альтернативный вариант

Частые новые буквы: Çç(Ц), Ęę(Э), Şş(Щ), Įį(Йот,Ь). Неиспользуемые старые: Ww, Qq. Буквы для аббревиатур: Ââ(Я),Êê(Е),Ôô(Ё),Ûû(Ю),Ĉĉ(Ч),Ĥĥ(Х),Ŝŝ(Ш),Ẑẑ(Ж),Ĵĵ(Й),Ŷŷ(Ы),ɨɨ(Ь),ɟɟ(Ъ).

Pįjanyj master po proectu sdelal mehanichescij object s izjanom. Įesli brac ne obnaruzhitsįa, to belyj bolid bolįshe ne smozhet vyigryvatį gonci.

V pįjese pro devushcu v zelįonom platįjiçe vse sadilisį na ladįji i plyli po rece. No tut iz lesa vyshel conį v palįto, cotoryj chto-to vyiscival, i pricazal vsem mytįsįa i gotovitį bulįyon. Znachit snova pįjom.

Prepodobnyj Bajįes podcinul igralįnyįe costi. Vypalo shestį, znachit įemu pridįotsįa mazatį jod na ranu.

Męr nebolįshogo gorodishci otcryl tabliçu exelįa i vozmutilsįa çenoj novogo excavatora. Azh eczema snova stala įego bespocoitį. Oh uzh eta pocupca vechnogo dvigatelįa v proshlom godu! A tac zhe pocupca aeroplana-ecranolįota. Įesli tac pojdįot i dalįshe, to bįudzhetu pridįotsįa hudo.

V etom vide fraza ot A to Įa nachinaįet vyglįadetį sovsem po-drugomu. Sejchas şhįotca novaįa, no pozzhe ona stanet staraįa. Chernysh lįubit cogda įego cheshut įeįu. Įozh colįuchij i pohozh na neįo.

Skhod mestnyh zhitelej indijscoj derevni sickhov reshal chto zhe delatį s otkhodami companii "Gaj Įulij Çezarį". Odin iz prisutstvuįuşhih nosil hoholoc na golove. On i nashįol vyhod iz situaçii.

"Cto s mechom c nam pridįot, tot ot mecha i..." - ne smog dogovoritį starshij mehanic Vasilij.

Imeįetsįa nescolįco gipotez proiskhozhdeniįa sobaci, naiboleįe veroįatnymi įeįo predcami schitaįutsįa volc i necotoryįe vidy shacalov.

V suzhdeniįah uchįonyh o predcah domashnej sobaci prisutstvuįut dve tochci zreniįa. Odni schitaįut, chto sobaci - polifiletichescaįa gruppa (proiskhodįaşhaįa ot nescolįcih predcov), drugiįe priderzhivaįutsįa mneniįa, chto vse sobaci proizoshli ot odnogo predca (monofiletichescaįa teoriįa).


## Кириллица => латиница

Пока что это только зачатки двух алгоритмов прямого и обратного пребразования.

### Таблица No.1 (сложные составные: й,ъ,ы,ь=>j,y)

`\c` - согласная (consonant), но не йот. Специальный символ регулярных выражений для `[qwrtpsdfghklzxcvbnmцкнгшщзхфвпрлджчсмтб]` (но без й, j).

|                      |              Cyrillic RegEx | Translit RE   | Примеры                                                                                                                   |
| -------------------- | ---------------------------:|:------------- | ------------------------------------------------------------------------------------------------------------------------- |
| ъ[еёюя] / j[eoua]    |            `(?<=\c)ъ[еёюя]` | `j[eoua]`     | *(после согласных перед йотированными гласными)* объект/objekt, изъян/izjan                                               |
| ъ/wj                 |               `ъ(?=[\w\c])` | `wj`          | *(перед согласными или в конце слова)* онъ/onwj, Муъминат/Muwjminat                                                       |
| ъи/ji                |                    `объима` | `objima`      | *(исключения отображения; йотированные)* объимать/objimatj                                                                |
| ъ/wjh                |                         `ъ` | `wjh`         | *(не йотированные)* объизвестить/obwjhizvestitj, Йонъин/Jonwjhin, Чанъань/Chanwjhanj, Муръйин/Murwjhjin, Чанъын/Сhanwjhyn |
|                      |                             |               |                                                                                                                           |
| ь[еёюяи] / jy[eouai] |           `(?<=\c)ь[еёюяи]` | `jy[eouai]`   | *(после согласных перед и или йотированными гласными)* пьеса/pjyesa, пьян/pjyan, ладьи/ladjyi, платьице/platjyice         |
| ьо / jyio            |                 `(?<=\c)ьо` | `jyio`        | *(после согласных перед о)* батальон/bataljyion/batalįjon, лосьон/losjyion, сеньор/senjyior                               |
| ь / jyie             |                  `бельэтаж` | `beljyietazh` | *(исключения отображения; йотированные)* бельэтаж/beljyietazh                                                             |
| ь/j                  |        `(?<=\c)ь(?=[\w\c])` | `j`           | *(после согласных перед согласными или в конце слова)* прячься/pryachjsya, мыться/mytjsya, конь/konj                      |
| ь/jh                 |                         `ь` | `jh`          | *(не йотированные, просто смягченные)* костьутиль/kostjhutilj, грабьармия/grabjharmiya, Мурьйин/Murjhjin, Чаньын/Сhanjhyn |
|                      |                             |               |                                                                                                                           |
| ы[еёюя] / yj[eoua]   |                   `ы[еёюя]` | `yj[eoua]`    | *(перед йотированными гласными)* белые/belyje, бедныя/bednyja                                                             |
| ы/yw                 |               `ы(?=[эоуа])` | `yw`          | Нарва-Йыэсуу/Narva-Jywesuu, Баймаклыаул/Bajmaklywaul                                                                      |
| ыи/ywi               |              `(?<![й\c])ыи` | `ywi`         | аыи/aywi, сьыио/sjywio                                                                                                    |
| ыи/yi                |              `(?<=[й\c])ыи` | `yi`          | выигрывать/vyigryvatj, выискивать/vyiskivatj                                                                              |
| ы/y                  |                         `ы` | `y`           | крыска/kryska, ыпся/ypsja, пыхтел/pyhtel, белый/belyj, выйигрывать/vyjigryvatj, байыс/bajys                               |
|                      |                             |               |                                                                                                                           |
| й/jj                 | `(?<=[й\c])й`&#124;`й(?=й)` | `jj`          | подйезд/podjjyezd, подйод/podjjod, Мурйин/Murjjin, подййод/podjjjjod                                                      |
| й/jj                 |         `(?<=ы)й(?=[эоуа])` | `jj`          | белыйа/belyjja, белыйэ/belyjje, белыйе/belyjye                                                                            |
| й/j                  |                         `й` | `j`           | байес/bajyes, белый/belyj, йод/jod, йиппи/jippi, байяс/bajyas, байас/bajas, йэс/jes, баян/bayan                           |

----

|                      |        Cyrillic RegEx | Latiniça RE  | Примеры                                                                                                                                     |
| -------------------- | ---------------------:|:------------ | ------------------------------------------------------------------------------------------------------------------------------------------- |
| ъ[еёюя] / j[eoua]    |      `(?<=\c)ъ[еёюя]` | `j[eoua]`    | *(после согласных перед йотированными гласными)* объект/object, изъян/izjan                                                                 |
| ъи/ji                |              `объима` | `objima`     | *(исключения отображения; йотированные)* объимать/objimatį                                                                                  |
| ъ/ɟ                  |                   `ъ` | `ɟ`          | *(не йотированные)* объизвестить/obɟizvestitį, Йонъин/Yonɟin, Чанъань/Chanɟanį, онъ/onɟ, Муъминат/Muɟminat, Муръйин/Murɟjin, Чанъын/Сhanɟyn |
|                      |                       |              |                                                                                                                                             |
| ь[еёюяи] / įy[eouai] |     `(?<=\c)ь[еёюяи]` | `įy[eouai]`  | *(после согласных перед и или йотированными гласными)* пьеса/pįjesa, пьян/pįjan, ладьи/ladįji, платьице/platįjiçe                           |
| ьо / įjo             |           `(?<=\c)ьо` | `įjo`        | *(после согласных перед о)* батальон/batalįyon, лосьон/losįyon, сеньор/senįyor                                                              |
| ь / įje              |            `бельэтаж` | `belįjetazh` | *(исключения отображения; йотированные)* бельэтаж/belįyetazh                                                                                |
| ь/į                  |  `(?<=\c)ь(?=[\w\c])` | `į`          | *(после согласных перед согласными или в конце слова)* прячься/prįachįsįa, мыться/mytįsįa, конь/conį                                        |
| ь/ɨ                  |                   `ь` | `ɨ`          | *(не йотированные, просто смягченные)* костьутиль/costɨutilį, грабьармия/grabɨarmiįa, Мурьйин/Murɨjin, Чаньын/Сhanɨyn                       |
|                      |                       |              |                                                                                                                                             |
| ый/yj                | `(?<=\c)ый(?![\w\c])` | `yj`         | *(после согласной, но НЕ перед согласной или конца слова)* белыйа/belyja, белыйя/belyjįa                                                                                                               |
| ы/y                  |            `(?<=\c)ы` | `y`          | *(после согласных)* белые/belyįe, белый/belyj                                                                                |
| ы/ȳ                  |            `(?<!\c)ы` | `ȳ`          | *(не после согласных)* ынлу/ynlu, ыы/yy, Нарва-Йыэсуу/Narva-Jyesuu, **забанить įy[aeou] с ы**                                                                                                                                       |
|                      |                       |              |                                                                                                                                             |
| ый/yį                | `(?<=\c)ый(?=[\w\c])` | `yį`         | *(перед согласными и в конце слова)* белый/belyj, белыйс/belyjs                                                                             |
| ы/ŷ                  |         `ы(?=[эоуа])` | `yw`         | Нарва-Йыэсуу/Narva-Jyesuu, Баймаклыаул/Baymaklyaul, белыйа/belyja, белыйя/belyjįa                                                           |
| ыи/ŷi                |        `(?<![й\c])ыи` | `ywi`        | аыи/ayi, сьыо/sįŷo                                                                                                                  |
| ыи/yi                |        `(?<=[й\c])ыи` | `yi`         | выигрывать/vyigryvatį, выискивать/vyiskivatį                                                                                                |
| ы/y                  |                   `ы` | `y`          | крыска/kryska, ыпся/ypsįa, пыхтел/pyhtel, выйигрывать/vyjigryvatį, байыс/bajys                                                 |
|                      |                       |              |                                                                                                                                             |
| й/ŷ                  |            `(?<=\c)й` | `ŷ`          | Сёркйосен/Sįorkĵosen                                                                                                                        |
| йы/įȳ                |            `(?<!ы)йы` | `įȳ`         | Нарва-Йыэсуу/Narva-Jyesuu                                                                                                                   |
| й/jj                 |   `(?<=ы)й(?=[эоуа])` | `jj`         | аллилуйя/allilujįa, белыйа/belyja, белыйэ/belyje, белыйе/belyjįe                                                                                              |
| й/j                  |                   `й` | `j`          | байес/bajįes, йод/jod, йиппи/jippi, байяс/bajįas, байас/bajas, йэс/jes, баян/baįan                                             |


### Таблица No.2 (простые составные)

|              |                         Cyrillic RegEx | Translit RE / Latiniça RE | Примеры                                                                                                                                                                                                                             |
| ------------ | --------------------------------------:|:------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| проект/.../e |                    `проект`&#124;`...` | `e`                       | *(исключения отображения)* проект/proekt/proect, проэкт/proękt/proęct (слова, которые должны были быть с йотированной е, но произносятся с **ударным** э)                                                                           |
| е/ye         |                   `^е`&#124;`(?<!\c)е` | `ye`                      | если/yesli/įesli, байес/bajyes/bajįes, Раевская/Rayevskaya/Raįevscaįa, зяе/zyaye/zįaįe, заем/zayem/zaįem, заём/zayom/zaįom, ехо/yeho/įeho, йeс/jyes/jįes, таец/tayec/taįeç, заезд/zayezd/zaįezd, траектория/trayektoriya/traįectoriįa |
| е/e          |                                    `е` | `e`                       | мех/meh                                                                                                                                                                                                                     |
| экс/ex       |                                  `экс` | `ex`                      | экскаватор/exkavator/excavator, эксель/exelj/exelį, мэкс/mex, экзамен/ekzamen/eczamen, экзема/ekzema/eczema, Мексика/Meksika/Mecsica, мех/meh                                                                                                      |
| э/e          |                   `^э`&#124;`(?<!\c)э` | `e`                       | эхо/eho, аэроплан/aeroplan, этот/etot, эон/eon, экран/ekran/ecran, эротика/erotika/erotica, йэс/jes, Ноэль/Noelj/Noelį, алоэ/aloe, радиоэхо/radioeho                    |
| э/ae(ę)      |                           `(?<=\cа*)э` | `ae`                      | мэр/maer/męr, мер/mer, маэр/maaer/maęr, мааэр/maaaer/maaęr, маер/mayer/maįer, моаэр/moaer                                                                                                        |
|              |                                        |                           |                                                                                                                                                                                                                                     |
| сьч/sjwch    |                                  `сьч` | `sjwch`                   | сьч/sjwch (в случае с диакритикой эта замена не нужна)                                                                                                                                                                      |
| щ/sjch(şch)  |                                    `щ` | `sjch`                    | щётка/sjchyotka/şhįotca, счёт/cshyot/schįot                                                                                                                                                                                   |
| ж/zh         |                                    `ж` | `zh`                      | ёж/yozh/įozh, возжи/vozzhi, позже/pozzhe                                                                                                                                                                         |
| ч/ch         |                                    `ч` | `ch`                      | Черныш/Chernysh, счётная/schyotnaya/schįotnaįa                                                                                                                                                                                 |
| ш/sh         |                                    `ш` | `sh`                      | шлем/shlem                                                                                                                                                                                                                  |
| х/kh         | `(?=[хтсшзжцчщъьйк])х`&#124;`(?=экс)x` | `kh`                      | сход/skhod, кхе/kkhe/ckhe, сикх/sikkh/sickh, мех/meh, Муръхин/Murwjhkhin/Murɟhin, Мурьхин/Murjkhin/Murįhin, отход/otkhod                                                                               |
| х/h          |                                    `х` | `h`                       | хохолок/hoholok/hoholoc, выход/vyhod, меха/meha, эхо/eho, вече/veche, меча/mecha, эч/ech, мэч/maech/męch, хья/hjya/hįja, хьан/hjhan/hɨan                                                            |
|              |                                        |                           |                                                                                                                                                                                                                                     |
| ё/yo         |                                    `ё` | `yo`                      | мёд/myod/mįod, ёмко/yomko/įomco                                                                                                                                                                                                |
| ю/yu         |                                    `ю` | `yu`                      | мюсли/myusli/mįusli, Юля/Yulya/Įulįa                                                                                                                                                                                             |
| я/ya         |                                    `я` | `ya`                      | Изя/Izya/Izįa, Якорь/Yakorj/Įakorį, баян/bayan/baįan                                                                                                                                                                          |
| ERR          |                                        | `[qwx]`                   |                                                                                                                                                                                                                                     |


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
