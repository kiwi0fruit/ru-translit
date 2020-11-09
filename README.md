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

Новые более-менее частые буквы: Çç(Ц), Ęę(Э), Şş(Щ), Įį(Йот,Ь,Й), Ĭĭ(Й). Неиспользуемые старые: Ww, Qq. Буквы для аббревиатур: Ââ(Я),Êê(Е),Ôô(Ё),Ûû(Ю),Čč(Ч),Šš(Ш),Žž(Ж),Ĥĥ(Х). Для очень редких слов: Ŷŷ(Ы),Îî(Ь),Ĵĵ(Ъ). Примечательные старые: Jj(ДЖдж,Ъъ),Xx(КСкс).

Pįyanyį master po proectu sdelal mehanichesciį objyect s izjyanom. Įesli brac ne obnaruzhitsįa, to belyį bolid bolįshe ne smozhet vyigryvatį gonci.

V pįyese pro devushcu v zelįonom platįyiçe vse sadilisį na ladįyi i plyli po rece. No tut iz lesa vyshel conį v palįto, cotoryį chto-to vyiscival, i pricazal vsem mytįsįa i gotovitį bulįjon. Znachit snova pįyom.

Prepodobnyį Baįyes podcinul igralįnyįe costi. Vypalo shestį, znachit įemu pridįotsįa mazatį ĭod na ranu.

Męr nebolįshogo gorodishci otcryl tabliçu exelįa i vozmutilsįa çenoį novogo excavatora. Azh eczema snova stala įego bespocoitį. Oh uzh eta pocupca vechnogo dvigatelįa v proshlom godu! A tac zhe pocupca aeroplana-ecranolįota. Įesli tac poįdįot i dalįshe, to bįudzhetu pridįotsįa hudo.

V etom vide fraza ot A to Įa nachinaįet vyglįadetį sovsem po-drugomu. Seįchas şhįotca novaįa, no pozzhe ona stanet staraįa. Chernysh lįubit cogda įego cheshut įeįu. Įozh colįuchiį i pohozh na neįo.

Skhod mestnyh zhiteleį indiįscoį derevni sickhov reshal chto zhe delatį s otkhodami companii "Caligula Gaį Įuliį Çezarį". Odin iz prisutstvuįuşhih nosil hoholoc na golove. On i nashįol vyhod iz situaçii.

"Cto s mechom c nam pridįot, tot ot mecha i..." - ne smog dogovoritį starshiį mehanic Vasiliį.

Imeįetsįa nescolįco gipotez proiskhozhdeniįa sobaci, naiboleįe veroįatnymi įeįo predcami schitaįutsįa volc i necotoryįe vidy shacalov.

V suzhdeniyah uchįonyh o predcah domashneį sobaci prisutstvuįut dve tochci zreniįa. Odni schitaįut, chto sobaci - polifiletichescaįa gruppa (proiskhodįaşhaįa ot nescolįcih predcov), drugiįe priderzhivaįutsįa mneniįa, chto vse sobaci proizoshli ot odnogo predca (monofiletichescaįa teoriįa).


## Кириллица => латиница

Пока что это только зачатки двух алгоритмов прямого и обратного пребразования.

`\c` - согласная (consonant), но не йот. Специальный символ регулярных выражений для `[qwrtpsdfghklzxcvbnmцкнгшщзхфвпрлджчсмтб]` (но без й, j).


### Таблица Translit No.1

|                      |              Cyrillic RegEx | Translit RegEx | Примеры                                                                                                                                                 |     |
| -------------------- | ---------------------------:|:-------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------- | --- |
| ъ[еёюя] / j[eoua]    |            `(?<=\c)ъ[еёюя]` | `j[eoua]`      | *(после согласных перед йотированными гласными)* объект/objekt, изъян/izjan                                                                             |     |
| ъ/wj                 |               `ъ(?=[\w\c])` | `wj`           | *(перед согласными или в конце слова)* онъ/onwj, Муъминат/Muwjminat                                                                                     |     |
| ъи/ji                |                    `объима` | `objima`       | *(исключения отображения; йотированные)* объимать/objimatj                                                                                              |     |
| ъ/wjh                |                         `ъ` | `wjh`          | *(не йотированные)* объизвестить/obwjhizvestitj, Йонъин/Jonwjhin, Чанъань/Chanwjhanj, Муръйин/Murwjhjin, Чанъын/Сhanwjhyn                               |     |
|                      |                             |                |                                                                                                                                                         |     |
| ь[еёюяи] / jy[eouai] |           `(?<=\c)ь[еёюяи]` | `jy[eouai]`    | *(после согласных перед и или йотированными гласными)* пьеса/pjyesa, пьян/pjyan, ладьи/ladjyi, платьице/platjyice                                       |     |
| ьо / jyio            |                 `(?<=\c)ьо` | `jyio`         | *(после согласных перед о)* батальон/bataljyion, лосьон/losjyion, сеньор/senjyior                                                                       |     |
| ь / jyie             |                  `бельэтаж` | `beljyietazh`  | *(исключения отображения; йотированные)* бельэтаж/beljyietazh                                                                                           |     |
| ь/j                  |        `(?<=\c)ь(?=[\w\c])` | `j`            | *(после согласных перед согласными или в конце слова)* прячься/pryachjsya, мыться/mytjsya, конь/konj                                                    |     |
| ь/jh                 |                         `ь` | `jh`           | *(не йотированные, просто смягченные)* костьутиль/kostjhutilj, грабьармия/grabjharmiya, Мурьйин/Murjhjin, Чаньын/Сhanjhyn                               |     |
|                      |                             |                |                                                                                                                                                         |     |
| ы[еёюя] / yj[eoua]   |                   `ы[еёюя]` | `yj[eoua]`     | *(перед йотированными гласными)* белые/belyje, бедныя/bednyja                                                                                           |     |
| ы/yw                 |               `ы(?=[эоуа])` | `yw`           | Нарва-Йыэсуу/Narva-Jywesuu, Баймаклыаул/Bajmaklywaul                                                                                                    |     |
| ыи/ywi               |              `(?<![й\c])ыи` | `ywi`          | аыи/aywi, сьыио/sjywio                                                                                                                                  |     |
| ыи/yi                |              `(?<=[й\c])ыи` | `yi`           | выигрывать/vyigryvatj, выискивать/vyiskivatj                                                                                                            |     |
| ы/y                  |                         `ы` | `y`            | крыска/kryska, ыпся/ypsja, пыхтел/pyhtel, белый/belyj, выйигрывать/vyjigryvatj, байыс/bajys                                                             |     |
|                      |                             |                |                                                                                                                                                         |     |
| й/jj                 | `(?<=[й\c])й`&#124;`й(?=й)` | `jj`           | подйезд/podjjyezd, подйод/podjjod, Мурйин/Murjjin, подййод/podjjjjod                                                                                    |     |
| й/jj                 |         `(?<=ы)й(?=[эоуа])` | `jj`           | белыйа/belyjja, белыйэ/belyjje, белыйе/belyjye                                                                                                          |     |
| й/j                  |                         `й` | `j`            | байес/bajyes, белый/belyj, йод/jod, йиппи/jippi, байяс/bajyas, байас/bajas, йэс/jes, баян/bayan                                                         |     |
|                      |                             |                |                                                                                                                                                         |     |
| проект/.../e         |         `проект`&#124;`...` | `e`            | *(исключения отображения)* проект/proekt, проэкт/proękt (слова, которые произносятся с ударным звуком э)                                                |     |
| е/ye                 |        `^е`&#124;`(?<!\c)е` | `ye`           | если/yesli, байес/bajyes, Раевская/Rayevskaya, зяе/zyaye, заем/zayem, заём/zayom, ехо/yeho, йeс/jyes, таец/tayec, заезд/zayezd, траектория/trayektoriya |     |
| е/e                  |                         `е` | `e`            | мех/meh                                                                                                                                                 |     |
| экс/ex               |                       `экс` | `ex`           | экскаватор/exkavator, эксель/exelj, мэкс/mex, экзамен/ekzamen, экзема/ekzema, Мексика/Meksika, мех/meh                                                  |     |
| э/e                  |        `^э`&#124;`(?<!\c)э` | `e`            | эхо/eho, аэроплан/aeroplan, этот/etot, эон/eon, экран/ekran, эротика/erotika, йэс/jes, Ноэль/Noelj, алоэ/aloe, радиоэхо/radioeho                        |     |
| э/ae                 |                `(?<=\cа*)э` | `ae`           | мэр/maer, мер/mer, маэр/maaer, мааэр/maaaer, маер/mayer, моаэр/moaer                                                                                    |     |


### Таблица Translit No.2

|           |                         Cyrillic RegEx | Translit RegEx | Примеры                                                                                                           |
| --------- | --------------------------------------:|:-------------- | ----------------------------------------------------------------------------------------------------------------- |
| сьч/sjwch |                                  `сьч` | `sjwch`        | сьч/sjwch                                                                                                         |
| щ/sjch    |                                    `щ` | `sjch`         | щётка/sjchyotka, счёт/cshyot                                                                                      |
| ж/zh      |                                    `ж` | `zh`           | ёж/yozh, возжи/vozzhi, позже/pozzhe                                                                               |
| ч/ch      |                                    `ч` | `ch`           | Черныш/Chernysh, счётная/schyotnaya                                                                               |
| ш/sh      |                                    `ш` | `sh`           | шлем/shlem                                                                                                        |
| х/kh      | `(?=[хтсшзжцчщъьйк])х`&#124;`(?=экс)x` | `kh`           | сход/skhod, кхе/kkhe, сикх/sikkh, мех/meh, Муръхин/Murwjhkhin, Мурьхин/Murjkhin, отход/otkhod                     |
| х/h       |                                    `х` | `h`            | хохолок/hoholok, выход/vyhod, меха/meha, эхо/eho, вече/veche, меча/mecha, эч/ech, мэч/maech, хья/hjya, хьан/hjhan |
|           |                                        |                |                                                                                                                   |
| ё/yo      |                                    `ё` | `yo`           | мёд/myod, ёмко/yomko                                                                                              |
| ю/yu      |                                    `ю` | `yu`           | мюсли/myusli, Юля/Yulya                                                                                           |
| я/ya      |                                    `я` | `ya`           | Изя/Izya, Якорь/Yakorj, баян/bayan                                                                                |
| ERROR     |                                        | `[qwx]`        |                                                                                                                   |


### Таблица Translit No.3

| Cyr | Lat | Cyr | Lat |
| ---:|:--- | ---:|:--- |
| `а` | `a` | `н` | `n` |
| `б` | `b` | `о` | `o` |
| `в` | `v` | `п` | `p` |
| `г` | `g` | `р` | `r` |
| `д` | `d` | `с` | `s` |
| `з` | `z` | `т` | `t` |
| `и` | `i` | `у` | `u` |
| `к` | `k` | `ф` | `f` |
| `л` | `l` | `х` | `h` |
| `м` | `m` | `ц` | `c` |


### Таблица Latiniça No.1

|                      | Контекст                                             | Примеры                                                                                                                                     |        Cyrillic RegEx | Latiniça RegEx |
| -------------------- | ---------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------:|:-------------- |
| ъ[еёюя] / j[eoua]    | после согласных перед йотированными гласными         | объект/objyect, изъян/izjyan                                                                                                                |      `(?<=\c)ъ[еёюя]` | `j[eoua]`      |
| ъ/j                  | йотированные исключения отображения                  | объимать/objyimatį                                                                                                                          |              `объима` | `objima`       |
| ъ/ĵ                  |                                                      | объизвестить/obĵizvestitį, Йонъин/Ĭonĵin, Чанъань/Chanĵanį, онъ/onĵ, Муъминат/Muĵminat, нъйи/nĵįi, нъын/nĵyn                                |                   `ъ` | `ĵ`            |
|                      |                                                      |                                                                                                                                             |                       |                |
| ь[еёюяи] / įy[eouai] | после согласных перед йотированными гласными или и   | пьеса/pįyesa, пьян/pįyan, ладьи/ladįyi, платьице/platįyiçe                                                                                  |     `(?<=\c)ь[еёюяи]` | `įy[eouai]`    |
| ьо / įjo             | после согласных перед о                              | батальон/batalįjon, лосьон/losįjon, сеньор/senįjor                                                                                          |           `(?<=\c)ьо` | `įjo`          |
| ь / įj               | йотированные исключения отображения                  | бельэтаж/belįjetazh                                                                                                                         |            `бельэтаж` | `belįjetazh`   |
| ь/į                  | после согласных перед согласными или в конце слова   | прячься/prįachįsįa, мыться/mytįsįa, конь/conį                                                                                               |  `(?<=\c)ь(?=[\w\c])` | `į`            |
| ь/î                  |                                                      | костьутиль/costîutilį, грабьармия/grabîarmiya, ньйи/nîįi, ньын/nîyn                                                                         |                   `ь` | `î`            |
|                      |                                                      |                                                                                                                                             |                       |                |
| й/ĭ                  | после согласных                                      | Сёркйосен/Sįorcĭosen                                                                                                                        |            `(?<=\c)й` | `ĭ`            |
| й/ĭ                  | перед не йотированными гласными (кроме и, ы)         | йод/ĭod, йэс/ĭes                                                                                                                            |         `й(?=[эоуа])` | `ĭ`            |
| й[еёюя] / įy[eoua]   | перед йотированными гласными                         | Байес/Baįyes, аллилуйя/alliluįya, ыйя/yįya                                                                                                  |         `й(?=[еёюя])` | `įy[eoua]`     |
| й/į                  |                                                      | белый/belyį, йиппи/įippi, Шайыр/Shaįyr, Нарва-Йыэсуу/Narva-Įŷesuu                                                                           |                   `й` | `į`            |
|                      |                                                      |                                                                                                                                             |                       |                |
| ы/ŷ                  | после дж и перед не йотированными гласными (кроме ы) | изджыан/izjŷan                                                                                                                              | `(?<=дж)ы(?=[эоуаи])` | `ŷ`            |
| ы/y                  | после согласных                                      | белый/belyį, крыска/kryska, пыхтел/pyhtel, выострить/vyostritį, выигрывать/vyigryvatį                                                       |            `(?<=\c)ы` | `y`            |
| ы/ŷ                  | перед не йотированными гласными (кроме ы)            | Нарва-Йыэсуу/Narva-Įŷesuu, аыи/aŷi                                                                                                          |        `ы(?=[эоуаи])` | `ŷ`            |
| ы/y                  |                                                      | ынлу/ynlu, ыы/yy, Шайыр/Shaįyr                                                                                                              |                   `ы` | `y`            |
|                      |                                                      |                                                                                                                                             |                       |                |
| е/e                  | после согласных                                      | мех/meh                                                                                                                                     |            `(?<=\c)е` | `e`            |
| e/e                  | не йотированные исключения отображения               | проект/proect, проэкт/proęct (слова, которые произносятся с ударным звуком э)                                                               |              `проект` | `proect`       |
| е/įe                 |                                                      | если/įesli, байес/baįyes, Раевская/Raįevscaįa, заем/zaįem, заём/zaįom, заезд/zaįezd, траектория/traįectoriįa                                |                   `е` | `įe`           |
| э/ę                  | после согласных                                      | мэр/męr                                                                                                                                     |            `(?<=\c)э` | `ę`            |
| э/e                  |                                                      | эхо/eho, аэроплан/aeroplan, этот/etot, эон/eon, экран/ecran, эротика/erotica, йэс/ĭes, маэр/maer, Ноэль/Noelį, алоэ/aloe, радиоэхо/radioeho |                   `э` | `e`            |


### Таблица Latiniça No.2

В аббревиатуры J идёт как D для совместимости с кириллицей.

|        |     Cyrillic RegEx | Latiniça RegEx | Примеры                                                                                                                                                                                      |
| ------ | ------------------:|:-------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| джх/jh |              `джх` | `jh`           | *(в словах, где д и ж не попадают в разные морфемы)* джхо/jho                                                                                                                                |
| дж/j   |               `дж` | `j`            | *(в словах, где д и ж не попадают в разные морфемы)* Джимми/Jimmi, доджо/dojo, додзё/dodzįo, аджика/ajika, поджигать/podzhigatį, обджект/object, обджэкт/objęct, изджан/izjan, изджян/izjįan |
| ксх/xh |              `ксх` | `xh`           | *(в словах, где к и с не попадают в разные морфемы)* эксхорт/exhort                                                                                                                          |
| кс/x   |               `кс` | `x`            | *(в словах, где к и с не попадают в разные морфемы)* максима/maxima, экскаватор/excavator, эксель/exelį, Мексика/Mexica, плакса/placsa, экзамен/eczamen, экзема/eczema                       |
| щ/şh   |                `щ` | `şh`           | щётка/şhįotca, счёт/schįot                                                                                                                                                                   |
| ж/zh   |                `ж` | `zh`           | ёж/įozh, возжи/vozzhi, позже/pozzhe                                                                                                                                                          |
| ч/ch   |                `ч` | `ch`           | Черныш/Chernysh, счётная/schįotnaįa                                                                                                                                                          |
| ш/sh   |                `ш` | `sh`           | шлем/shlem                                                                                                                                                                                   |
| х/kh   | `(?=[тсшзжцчщк])х` | `kh`           | *(после некоторых согласных)* сход/skhod, кхе/ckhe, сикх/sickh, шхуна/shkhuna, чхать/chkhatį, мех/meh, нъхи/nĵhi, ньхи/nįhi, отход/otkhod, хахх/hahh                                         |
| х/h    |                `х` | `h`            | хохолок/hoholoc, выход/vyhod, меха/meha, эхо/eho, вече/veche, меча/mecha, эч/ech, мэч/męch, хья/hįya, хьан/hîan                                                                              |
|        |                    |                |                                                                                                                                                                                              |
| ё/yo   |                `ё` | `yo`           | мёд/mįod, ёмко/įomco                                                                                                                                                                         |
| ю/yu   |                `ю` | `yu`           | мюсли/mįusli, Юля/Įulįa                                                                                                                                                                      |
| я/ya   |                `я` | `ya`           | Изя/Izįa, Якорь/Įakorį, баян/baįan                                                                                                                                                           |
| ERROR  |                    | `[qwx]`        |                                                                                                                                                                                              |


### Таблица Latiniça No.3

| Cyr | Lat | Cyr | Lat |
| ---:|:--- | ---:|:--- |
| `а` | `a` | `н` | `n` |
| `б` | `b` | `о` | `o` |
| `в` | `v` | `п` | `p` |
| `г` | `g` | `р` | `r` |
| `д` | `d` | `с` | `s` |
| `з` | `z` | `т` | `t` |
| `и` | `i` | `у` | `u` |
| `к` | `c` | `ф` | `f` |
| `л` | `l` | `х` | `h` |
| `м` | `m` | `ц` | `ç` |


### Раскладка клавиатуры для латиницы

Основная раскладка. Добавляет более менее частые новые буквы: Çç(Ц), Ęę(Э), Şş(Щ), Įį(Йот,Ь,Й), Ĭĭ(Й).

| Ĭĭ(\`~ё) | 1!  | 2"(@") | 3#(#№) | 4;($;) | 5:(%) | 6^(^:) | 7&(&?) | 8\* | 9(  | 0)          | -\_         | =+             |
|:--------:|:---:|:------:|:------:|:------:|:-----:|:------:|:------:|:---:|:---:|:-----------:|:-----------:|:--------------:|
|          | Qq  |   Ww   |   Ee   |   Rr   | Tt    | Yy     | Uu     | Ii  | Oo  | Pp          | **Çç**([{х) | **Şş**(]}ъ)    |
|          | Aa  |   Ss   |   Dd   |   Ff   | Gg    | Hh     | Jj     | Kk  | Ll  | **Įį**(;:ж) | **Ęę**('"э) | **\\'**(\\\|/) |
|          |     |   Zz   |   Xx   |   Cc   | Vv    | Bb     | Nn     | Mm  | ,<  | .>          | /?          |                |

Дополнительная раскладка. Буквы для аббревиатур: Ââ(Я),Êê(Е),Ôô(Ё),Ûû(Ю),Čč(Ч),Šš(Ш),Žž(Ж),Ĥĥ(Х). Для очень редких слов: Ŷŷ(Ы),Îî(Ь),Ĵĵ(Ъ).

| Ĭĭ | 1!     | 2"     | 3#     | 4;     | 5:     | 6^     | 7&     | 8\*    | 9(     | 0) | -\_ | =+  |
|:--:|:------:|:------:|:------:|:------:|:------:|:------:|:------:|:------:|:------:|:--:|:---:|:---:|
|    |   Qq   |   Ww   | **Êê** |   Rr   | Tt     | **Ŷŷ** | **Ûû** | **Îî** | **Ôô** | Pp | Çç  | Şş  |
|    | **Ââ** | **Šš** |   Dd   |   Ff   | Gg     | **Ĥĥ** | **Ĵĵ** | Kk     | Ll     | Įį | Ęę  | \\' |
|    |        | **Žž** |   Xx   | **Čč** | Vv     | Bb     | Nn     | Mm     | ,<     | .> | /?  |     |


## TO DO

* [ ] Написать кодировщик и декодировщик на питоне, а потом проверить на каком-нибудь словаре, а так же на случайно-сгенерированных словах. Я не проверял алгоритм декодирования даже мысленно. Но интуитивно чувствую, что он хорошо определён и реализуем. Собственно, алгоритм кодировки строился такой, чтобы не было такого, чтобы разные русские слова (любые) отображались в одну и ту же транслитерацию.
* [ ] Попробовать сделать фильтр pandoc. Но там надо посмотреть какой элемент гарантированно содержит только голый текст.
* [ ] Сделать режим, в котором просто все русские обособленные слова преобразуются в массиве текста.
* [ ] Оформить в виде модуля питона с CLI.
* [ ] Написать инструкцию как сконвертировать произвольную страницу в интернете с помощью сохранения как html и конвертации фильтром/пандоком.
* [ ] Попробовать сделать однострочный джавастрипт, которым можно перевести любую уже открытую страницу в интернете.

Mics:

* [latin capital letter j with stroke, latin small letter dotless j, latin small letter dotless j with stroke U+025F](https://en.wikipedia.org/wiki/List_of_Unicode_characters), [List of Latin-script letters](https://en.wikipedia.org/wiki/List_of_Latin-script_letters).
* [Частотность](https://ru.wikipedia.org/wiki/%D0%A7%D0%B0%D1%81%D1%82%D0%BE%D1%82%D0%BD%D0%BE%D1%81%D1%82%D1%8C)
