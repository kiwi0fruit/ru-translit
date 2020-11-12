# ru-translit (kiwi0fruit's)

### Uniquely reversible Russian to English transliteration (no extra letters, diacritics and non-letters) and dual romanization with diacritics (russkaya latinica)

### Однозначно обратимая транслитерация из русского в английский алфавит (без дополнительных букв, диакритических и небуквенных знаков) и парная к ней романизация с диакритикой (русская латиница)

Придумал в качестве развлечения ещё один транслит.

Развлечением было удовлетворить ограничениям:

* Транслит - полностью обратимый (является кодировкой без потерь и позволяет точно восстановить произвольный русский текст из латиницы). То есть, это [**инъективное отображение**](https://ru.wikipedia.org/wiki/%D0%98%D0%BD%D1%8A%D0%B5%D0%BA%D1%86%D0%B8%D1%8F_(%D0%BC%D0%B0%D1%82%D0%B5%D0%BC%D0%B0%D1%82%D0%B8%D0%BA%D0%B0)),
* Транслит содержит только буквы (в частности, не использует апостроф): отображение из русских букв `[А-Яа-я]` в английские `[A-Za-z]` без добавлений,
* Не содержит далёких фонетических замен типа щ → w. Желательно, чтобы "звучало" похоже на английский или математический латинский.


## Кириллица <=> латиница

Главной целью проекта была обратимая транслитерация в английский алфавит, близкая к английскому чтению.

Основаные идеи внутренней грамматики:

* y значит йот,
* y йотирует следующую гласную, но не смягчает предыдущую согласную (яма/yama, съезд/syezd),
* y после согласных звучит ы, но йотирование гласных имеет приоритет (мы/my),
* ный будет nyy, уйя будет uyya, ные будет nyye; логично, однозначно, слегка разочаровывает, но неизбежно (красный/krasnyy, аллилуйя/alliluyya),
* i после согласных смягчает их, но не йотирует следующую гласную (мёд/miod), это поведение отключается добавлением h после двух гласных (пион/piohn),
* j перед гласной (aoue, но не y) или h становится дж, в остальных случаях он смягчает предыдущую согласную (Джордж/Jorjh, пьеса/pjyesa, конь/konj).
* e после согласных всегда смягчает, можно опустить i (пень/penj). В остальных случаях e обозначает звук э (это/eto, поэт/poet). Йотировать надо для уезд/uyezd. Убрать смягчение после согласной можно с помощью ae: мэр/maer. Это можно отключить с помощью h: маэстро/maehstro.
* qq обозначает паузу, гортанную смычку или просто игнорируемый диграф (зависит от слова).

|              | Правило                                                                                                                                                            | Примеры                                                                                        |
|:------------:|:------------------------------------------------------------------------------------------------------------------------------------------------------------------ |:---------------------------------------------------------------------------------------------- |
|    **ъ**     | None (после согласных перед **яёюе** или **и** когда она йотируется), **qq** (иначе)                                                                               | изъян/izyan, объимать/obyimatj, объизвестить/obqqizvestitj, Йонъин/Jonqqin                     |
| **ь[аоуэ]**  | **jy[aoue]h** (гласные **аоуэ** после **ь** когда они **йотируются**: о йотируется почти всегда, ауэ почти не йотируются за редкими исключениями)                  | бульон/buljyohn, бельэтаж/beljyehtazh                                                          |
|    **ь**     | **jqq** (перед гласными **аоуэ** или **ои** когда они **не** йотируются), **j** (иначе)                                                                            | грабьармия/grabjqqarmiya, пьеса/pjyesa, ладьи/ladjyi, грабьобоз/grabjqqoboz (выдуманное слово) |
| **й[аоуэ]**  | **y[aoue]h** (гласные **аоуэ** после й)                                                                                                                            | йод/yohd                                                                                       |
|    **й**     | **y** (остальные случаи)                                                                                                                                           | красный/krasnyy, аллилуйя/alliluyya                                                            |
|    **ы**     | **y** (после согласных), hy (иначе)                                                                                                                                | выход/vykhod, Нарва-Йыэсуу/Narva-Yhyhesuu                                                      |
| **ы[аоуэи]** | **yh[aouei]** (гласные **аоуэи** после ы)                                                                                                                          | выигрывать/vyhigrayvatj, выучить/vyhuchitj                                                     |
|    **е**     | **е** (после согласных или в ситуациях когда е читается как э), **ye** (иначе)                                                                                     | мера/mera, еда/yeda, проект/proekt                                                             |
|    **э**     | **ae** (после согласных), **е** (иначе)                                                                                                                            | мэр/maer, этот/etot                                                                            |
|  **аэ/аэх**  | **aeh/aehh** (после согласных)                                                                                                                                     | маэстро/maehstro, Алаэхос/Alaehhos                                                             |
|  **[яёю]**   | **i[aou]** (после согласных), **y[aou]** (иначе)                                                                                                                   | мёд/miod, ёлка/yolka, пюре/piure, якорь/yakorj                                                 |
|  **и[аоу]**  | **i[aou]h** (после согласных), **i[aou]** (иначе)                                                                                                                  | пианино/piahnino, ион/ion                                                                      |
| **и[аоу]х**  | **i[aou]hh** (х становится просто h, а не kh)                                                                                                                      | диахрония/diahhroniya                                                                          |
|    **х**     | **kh** (когда есть неоднозначность из-за других диграфов и триграфов с h), **h** (иначе)                                                                           | сход/skhod, лях/liakh                                                                          |
|    **дж**    | в словах, где **д** и **ж** не попадают в разные морфемы и нет чередования корней, где они порознь: **j** (перед гласными **аоуэи**), **jh** (в остальных случаях) | Джордж/Jorjh, поджечь/podzhechj                                                                |
|    **кс**    | в словах, где **к** и **с** не попадают в разные морфемы и нет чередования корней, где они порознь: **x**                                                          | Максим/Maxim, спёкся/spioksia                                                                  |

|  **a**  | **б** |  **в**  | **г**  |  **д**   |
|:-------:|:-----:|:-------:|:------:|:--------:|
|  a/ha   |   b   |    v    |   g    |    d     |
|  **е**  | **ё** |  **ж**  | **з**  |  **и**   |
|  e/ye   | io/yo |   zh    |   z    |   i/hi   |
|  **й**  | **к** |  **л**  | **м**  |  **н**   |
|    y    |   k   |    l    |   m    |    n     |
|  **о**  | **п** |  **р**  | **с**  |  **т**   |
|  o/ho   |   p   |    r    |   s    |    t     |
|  **у**  | **ф** |  **х**  | **ц**  |  **ч**   |
|  u/hu   |   f   |  h/kh   |   c    |    ch    |
|  **ш**  | **щ** |  **ъ**  | **ы**  |  **ь**   |
|   sh    | shch  | None/qq |  y/hy  |  j/jqq   |
|  **э**  | **ю** |  **я**  | **кс** |  **дж**  |
| ae/e/he | iu/yu |  ia/ya  |  x/ks  | j/jh/dzh |
| **шч**  |       |         |        |          |
|  shwch  |       |         |        |          |

Многие буквы совпадают с [ГОСТ 16876-71 табл. 2](https://ru.wikipedia.org/wiki/%D0%A2%D1%80%D0%B0%D0%BD%D1%81%D0%BB%D0%B8%D1%82%D0%B5%D1%80%D0%B0%D1%86%D0%B8%D1%8F_%D1%80%D1%83%D1%81%D1%81%D0%BA%D0%BE%D0%B3%D0%BE_%D0%B0%D0%BB%D1%84%D0%B0%D0%B2%D0%B8%D1%82%D0%B0_%D0%BB%D0%B0%D1%82%D0%B8%D0%BD%D0%B8%D1%86%D0%B5%D0%B9#%D0%A1%D1%80%D0%B0%D0%B2%D0%BD%D0%B8%D1%82%D0%B5%D0%BB%D1%8C%D0%BD%D0%B0%D1%8F_%D1%82%D0%B0%D0%B1%D0%BB%D0%B8%D1%86%D0%B0_%D1%81%D0%B8%D1%81%D1%82%D0%B5%D0%BC_%D1%82%D1%80%D0%B0%D0%BD%D1%81%D0%BB%D0%B8%D1%82%D0%B5%D1%80%D0%B0%D1%86%D0%B8%D0%B8) или [ГОСТ 7.79-2000 сист. Б](https://ru.wikipedia.org/wiki/%D0%A2%D1%80%D0%B0%D0%BD%D1%81%D0%BB%D0%B8%D1%82%D0%B5%D1%80%D0%B0%D1%86%D0%B8%D1%8F_%D1%80%D1%83%D1%81%D1%81%D0%BA%D0%BE%D0%B3%D0%BE_%D0%B0%D0%BB%D1%84%D0%B0%D0%B2%D0%B8%D1%82%D0%B0_%D0%BB%D0%B0%D1%82%D0%B8%D0%BD%D0%B8%D1%86%D0%B5%D0%B9#%D0%A1%D1%80%D0%B0%D0%B2%D0%BD%D0%B8%D1%82%D0%B5%D0%BB%D1%8C%D0%BD%D0%B0%D1%8F_%D1%82%D0%B0%D0%B1%D0%BB%D0%B8%D1%86%D0%B0_%D1%81%D0%B8%D1%81%D1%82%D0%B5%D0%BC_%D1%82%D1%80%D0%B0%D0%BD%D1%81%D0%BB%D0%B8%D1%82%D0%B5%D1%80%D0%B0%D1%86%D0%B8%D0%B8).

Алфавит транслитерации использует все буквы английского алфавита.

***Слово на латинице является грамматически верным если:***

1. его образ от прообраза совпадает с самим словом (`lat_word == RUtoEN(ENtoRU(lat_word))`),
2. его прообраз грамматически верен (`ENtoRU(lat_word)`).

Для обратимых аббревиатур, выглядящих прилично и совместимых с чтением по-русски придётся расширять алфавит:

| **я** | **е** | **ё** | **ю** | **и** | **ы** | **э** |
|:-----:|:-----:|:-----:|:-----:|:-----:|:-----:|:-----:|
|  Ää   |  Ëë   |  Öö   |  Üü   |  Ïï   |  Ÿÿ   |  Ęę   |
| **ч** | **щ** | **ж** | **ш** | **х** | **й** |       |
|  Ĉĉ   |  Ŝŝ   |  Žž   |  Šš   |  Ĥĥ   |  Ŷŷ   |       |

**ъ**: QQqq, **ь**: JQQjqq.


## Пример текста транслитом

*По-моему, это вариант гораздо лучше подходит для русско-английских билингвов, чем варианты с большим количеством диакритических знаков. В английском нет диакритики, в русском - почти нет (ё ставят только при опасности неправильного прочтения, й трудно считать диакритикой). Так что не удивительно, что диакритика будет вызывать отторжение. В варианте минималистичной диакритики она ставится тоже в очень малом числе случаев.*

Pjyanyy master po proektu sdelal mehanicheskiy obyekt s izyanom. Yesli brak ne obnaruzhitsia, to belyye bolidy boljshe ne smogut vyhigryvatj gonki.

V pjyese pro devushku v zelionom platjyice vse sadilisj na ladjyi i plyli po reke. No tut iz lesa vyshel Jorjh Maximus, konj v paljto i rvanyh jinsah, kotoryy chto-to vyhiskival, i prikazal vsem mytjsia i gotovitj buljyohn. Znachit snova pjyom do lysyh akvalangistov.

Prepodobnyy Bayyes podkinul igraljnyye kosti. Vypalo shestj, znachit yemu pridiotsia mazatj yohd na ranu.

Maer neboljshogo gorodishki otkryl tablicu exelia i vozmutilsia cenoy novogo exkavatora. Azh ekzema snova stala yego bespokoitj. Oh uzh eta pokupka vechnogo dvigatelia v proshlom godu! A tak zhe pokupka aeroplana-ekranoliota. Yesli tak poydiot i daljshe, to biujetu pridiotsia hudo.

V etom vide fraza ot A to Ya nachinayet vygliadetj sovsem po-drugomu. Seychas shchiotka novaya, no pozzhe ona stanet staraya. Chernysh liubit kogda yego cheshut yeyu. Yozh koliuchiy i pohozh na neyo.

Skhod mestnyh zhiteley indiyskoy derevni sikkhov reshal chto zhe delatj s otkhodami kompanii "Kaligula Gay Yuliy Cezarj" (lat. Caligula Gaius Iulius Caesar). Odin iz prisutstvuyushchih nosil hoholok na golove. On i nashiol vykhod iz situacii.

"Kto s mechom k nam pridiot, tot ot mecha i..." - ne smog dogovoritj starshiy mehanik Vasiliy.

Imeyetsia neskoljko gipotez proiskhozhdeniya sobaki, naiboleye veroyatnymi yeyo predkami schitayutsia volk i nekotoryye vidy shakalov.

V suzhdeniyakh uchionyh o predkah domashney sobaki prisutstvuyut dve tochki zreniya. Odni schitayut, chto sobaki - polifileticheskaya gruppa (proiskhodiashchaya ot neskoljkih predkov), drugiye priderzhivayutsia mneniya, chto vse sobaki proizoshli ot odnogo predka (monofileticheskaya teoriya).


### Пример текста латиницей

*Отличается от предыдущего варианта тем, что:*

* Jj и Ii заменены на Įį в значении смягчения предыдущей согласной.
* Это совместимо меняет переключатель h из Лион/Liohn/Lïon, лён/lion/lįon.
* Так же AEae после согласных заменена на Ęę. Это совместимо меняет переключатель h из маэстро/maehstro/maęstro, мэр/maer/męr.
* Тоже самое с йод/yohd/ŷod и выучить/vyhuchitj/vÿuchitį.
* С ŝh вместо shch всё очевидно.

*Всё остальное тоже самое, что и в предыдущем варианте.*

Новые буквы, встречающиеся не в аббревиатурах: Įį(Ь), Ŝŝ(Щ), Ęę(Э), Ïï(И), Ÿÿ(Ы), Ŷŷ(Й). Совсем редкие буквы теперь: **ь**: Îî, **ъ**: QQqq.

Pįyanyy master po proektu sdelal mehanicheskiy obyekt s izyanom. Yesli brak ne obnaruzhitsįa, to belyye bolidy bolįshe ne smogut vÿigryvatį gonki.

V pįyese pro devushku v zelįonom platįyice vse sadilisį na ladįyi i plyli po reke. No tut iz lesa vyshel Jorjh Maximus, konį v palįto i rvanyh jinsah, kotoryy chto-to vÿiskival, i prikazal vsem mytįsįa i gotovitį bulįyohn. Znachit snova pįyom do lysyh akvalangistov.

Prepodobnyy Bayyes podkinul igralįnyye kosti. Vypalo shestį, znachit yemu pridįotsįa mazatį ŷod na ranu.

Męr nebolįshogo gorodishki otkryl tablicu exelįa i vozmutilsįa cenoy novogo exkavatora. Azh ekzema snova stala yego bespokoitį. Oh uzh eta pokupka vechnogo dvigatelįa v proshlom godu! A tak zhe pokupka aeroplana-ekranolįota. Yesli tak poydįot i dalįshe, to bįujetu pridįotsįa hudo.

V etom vide fraza ot A to Ya nachinayet vyglįadetį sovsem po-drugomu. Seychas ŝhįotka novaya, no pozzhe ona stanet staraya. Chernysh lįubit cogda yego cheshut yeyu. Yozh kolįuchiy i pohozh na neyo.

Skhod mestnyh zhiteley indiyskoy derevni sikkhov reshal chto zhe delatį s otkhodami companii "Kaligula Gay Yuliy Cezarį" (lat. Caligula Gaius Iulius Caesar). Odin iz prisutstvuyuŝhih nosil hoholok na golove. On i nashįol vÿhod iz situacii.

"Kto s mechom k nam pridįot, tot ot mecha i..." - ne smog dogovoritį starshiy mehanik Vasiliy.

Imeyetsįa neskolįko gipotez proiskhozhdeniya sobaki, naiboleye veroyatnymi yeyo predkami schitayutsįa volk i nekotoryye vidy shakalov.

V suzhdeniyakh uchįonyh o predkah domashney sobaki prisutstvuyut dve tochki zreniya. Odni schitayut, chto sobaki - polifileticheskaya gruppa (proiskhodįaŝhaya ot neskolįkih predkov), drugiye priderzhivayutsįa mneniya, chto vse sobaki proizoshli ot odnogo predka (monofileticheskaya teoriya).


## Кириллица => латиница

Пока что это только зачатки двух алгоритмов прямого и обратного пребразования.

`\c` - согласная (consonant), но не йот. Специальный символ регулярных выражений для `[qwrtpsdfghklzxcvbnmцкнгшщзхфвпрлджчсмтб]` (но без й, j).


### Таблица Translit No.1

|                      |              Cyrillic RegEx | Translit RegEx | Примеры                                                                                                                                                 |     |
| -------------------- | ---------------------------:|:-------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------- | --- |
| ъ[еёюя] / j[eoua]    |            `(?<=\c)ъ[еёюя]` | `j[eoua]`      | *(после согласных перед йотированными гласными)* объект/obhyekt, изъян/izyan                                                                             |     |
| ъ/wj                 |               `ъ(?=[\w\c])` | `wj`           | *(перед согласными или в конце слова)* онъ/onw, Муъминат/Muwminat                                                                                     |     |
| ъи/ji                |                    `объима` | `objima`       | *(исключения отображения; йотированные)* объимать/obwjyimatj                                                                                              |     |
| ъ/wjh                |                         `ъ` | `wjh`          | *(не йотированные)* объизвестить/obwizvestitj, Йонъин/Jonwin, Чанъань/Chanwanj, Муръйин/Murwjhjin, Чанъын/Сhanwjhyn                               |     |
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
| х/h       |                                    `х` | `h`            | хохолок/hoholok, выход/vykhod, меха/meha, эхо/eho, вече/veche, меча/mecha, эч/ech, мэч/maech, хья/hjya, хьан/hjhan |
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
| ъ[еёюя] / jy[eoua]    | после согласных перед йотированными гласными         | объект/objyect, изъян/izjyan                                                                                                                |      `(?<=\c)ъ[еёюя]` | `jy[eoua]`      |
| ъ/jy                  | йотированные исключения отображения                  | объимать/objyimatį                                                                                                                          |              `объима` | `objyima`       |
| ъ/ĵ                  |                                                      | объизвестить/obĵizvestitį, Йонъин/Ĭonĵin, Чанъань/Chanĵanį, онъ/onĵ, Муъминат/Muĵminat, нъйи/nĵįi, нъын/nĵyn                                |                   `ъ` | `ĵ`            |
|                      |                                                      |                                                                                                                                             |                       |                |
| ь[еёюяи] / įy[eouai] | после согласных перед йотированными гласными или и   | пьеса/pįyesa, пьян/pįyan, ладьи/ladįyi, платьице/platįyiçe                                                                                  |     `(?<=\c)ь[еёюяи]` | `įy[eouai]`    |
| ьо / įjyo            | после согласных перед о                              | батальон/batalįjyon, лосьон/losįjyon, сеньор/senįjyor                                                                                       |           `(?<=\c)ьо` | `įjyo`         |
| ь / įjy              | йотированные исключения отображения                  | бельэтаж/belįjyetazh                                                                                                                        |            `бельэтаж` | `belįjyetazh`  |
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
| щ/ŝh   |                `щ` | `ŝh`           | щётка/ŝhįotca, счёт/schįot                                                                                                                                                                   |
| ж/zh   |                `ж` | `zh`           | ёж/įozh, возжи/vozzhi, позже/pozzhe                                                                                                                                                          |
| ч/ch   |                `ч` | `ch`           | Черныш/Chernysh, счётная/schįotnaįa                                                                                                                                                          |
| ш/sh   |                `ш` | `sh`           | шлем/shlem                                                                                                                                                                                   |
| х/kh   | `(?=[тсшзжцчщк])х` | `kh`           | *(после некоторых согласных)* сход/skhod, кхе/ckhe, сикх/sickh, шхуна/shkhuna, чхать/chkhatį, мех/meh, нъхи/nĵhi, ньхи/nįhi, отход/otkhod, хахх/hahh                                         |
| х/h    |                `х` | `h`            | хохолок/hoholoc, выход/vykhod, меха/meha, эхо/eho, вече/veche, меча/mecha, эч/ech, мэч/męch, хья/hįya, хьан/hîan                                                                              |
|        |                    |                |                                                                                                                                                                                              |
| ё/yo   |                `ё` | `yo`           | мёд/mįod, ёмко/įomco                                                                                                                                                                         |
| ю/yu   |                `ю` | `yu`           | мюсли/mįusli, Юля/Įulįa                                                                                                                                                                      |
| я/ya   |                `я` | `ya`           | Изя/Izįa, Якорь/Įacorį, баян/baįan                                                                                                                                                           |
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

Основная раскладка. Добавляет более менее частые новые буквы: Çç(Ц), Ęę(Э), Ŝŝ(Щ), Įį(Йот,Ь,Й), Ĭĭ(Й).

| Ĭĭ(\`~ё) | 1!  | 2"(@") | 3#(#№) | 4;($;) | 5:(%) | 6^(^:) | 7&(&?) | 8\* | 9(  | 0)          | -\_         | =+             |
|:--------:|:---:|:------:|:------:|:------:|:-----:|:------:|:------:|:---:|:---:|:-----------:|:-----------:|:--------------:|
|          | Qq  |   Ww   |   Ee   |   Rr   | Tt    | Yy     | Uu     | Ii  | Oo  | Pp          | **Çç**([{х) | **Ŝŝ**(]}ъ)    |
|          | Aa  |   Ss   |   Dd   |   Ff   | Gg    | Hh     | Jj     | Kk  | Ll  | **Įį**(;:ж) | **Ęę**('"э) | **\\'**(\\\|/) |
|          |     |   Zz   |   Xx   |   Cc   | Vv    | Bb     | Nn     | Mm  | ,<  | .>          | /?          |                |

Дополнительная раскладка. Буквы для аббревиатур: Ââ(Я),Êê(Е),Ôô(Ё),Ûû(Ю),Čč(Ч),Šš(Ш),Žž(Ж),Ĥĥ(Х). Для очень редких слов: Ŷŷ(Ы),Îî(Ь),Ĵĵ(Ъ).

| Ĭĭ | 1!     | 2"     | 3#     | 4;     | 5:     | 6^     | 7&     | 8\*    | 9(     | 0) | -\_ | =+  |
|:--:|:------:|:------:|:------:|:------:|:------:|:------:|:------:|:------:|:------:|:--:|:---:|:---:|
|    |   Qq   |   Ww   | **Êê** |   Rr   | Tt     | **Ŷŷ** | **Ûû** | **Îî** | **Ôô** | Pp | Çç  | Ŝŝ  |
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
