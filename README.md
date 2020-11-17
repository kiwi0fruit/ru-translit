# ru-translit (kiwi0fruit's)

### Uniquely reversible Russian to English transliteration (no extra letters, diacritics and non-letters) and dual romanization with diacritics (russkaya latinica)

### Однозначно обратимая транслитерация из русского в английский алфавит (без дополнительных букв, диакритических и небуквенных знаков) и парная к ней романизация с диакритикой (русская латиница)

Содержание:

* [Кириллица <=> латиница](#kirillica--latinica)
* [Раскладка клавиатуры для латиницы](#raskladka-klaviahtury-dlia-latinicy)
* [Пример текста транслитом](#primer-texta-translitom)
* [Пример текста латиницей](#primer-teksta-latinicey)

Придумал в качестве развлечения ещё один транслит.

Развлечением было удовлетворить ограничениям:

* Транслит - полностью обратимый (является кодировкой без потерь и позволяет точно восстановить произвольный русский текст из латиницы). То есть, это [**инъективное отображение**](https://ru.wikipedia.org/wiki/%D0%98%D0%BD%D1%8A%D0%B5%D0%BA%D1%86%D0%B8%D1%8F_(%D0%BC%D0%B0%D1%82%D0%B5%D0%BC%D0%B0%D1%82%D0%B8%D0%BA%D0%B0)),
* Транслит содержит только буквы (в частности, не использует апостроф): отображение из русских букв `[А-Яа-я]` в английские `[A-Za-z]` без добавлений,
* Не содержит далёких фонетических замен типа щ → w. Желательно, чтобы "звучало" похоже на английский или математический латинский.


## Kirillica <=> latinica

Главной целью проекта была обратимая транслитерация в английский алфавит, близкая к английскому чтению.

Основаные идеи внутренней грамматики **транслита без диакритики**:

* y значит йот,
* y йотирует следующую гласную, но не смягчает предыдущую согласную (яма/yama, съезд/syezd),
* y после согласных звучит ы, но йотирование гласных имеет приоритет (мы/my),
* разные виды йотирования переключаются после yo,ye,yu,ya. Причем, когда место возможного переключения йотирования всего одно, то переключение происходит в конце слова, а когда их несколько, то сразу после (ёд/yod, йод/yodw, ёдйод/yodyohd). Если переключатель h всего один и он и так в конце слова, то его не стоит трогать (ручьйи/ruchjyih).
* j после согласных смягчает их, но не йотирует следующую гласную (мёд/mjod, пьеса/pjyesa, конь/konj),
* после ы буквы й,е,ё,ю,я,а,о,у,э становятся y,ye,yo,yu,ya,wa,wo,wu,we (красный/krasnyy, красные/krasnyye, аллилуйя/alliluyya, выучить/vywuchitj, выискивать/vywiskivatj).
* e после согласных всегда смягчает, можно опустить i (пень/penj). В остальных случаях e обозначает звук э (это/eto, поэт/poet). Йотировать надо для уезд/uyezd. Убрать смягчение после согласной можно с помощью we: мэр/mwer, сэр/swer.
* qq обозначает паузу, гортанную смычку или просто игнорируемый диграф - зависит от слова (объизвестить/obqqizvestitj, грабьармия/grabjqqarmiya).
* х обозначется h/kh (ход/hod, сход/skhod).
* слова на латинице из других языков можно писать, экранируя с помощью " /" и "/ ".

Парная **латиница с диакритикой** отличается от предыдущего варианта тем, что:

* Jj заменено на Įį.
* QQqq заменено на Ɂɂ (объизвестить/obɂizvestitį, грабьармия/grabįɂarmiya).
* Ww перед гласными и в конце слова, а так же k перед h заменены на Ꞌꞌ ([Saltillo](https://en.wikipedia.org/wiki/Saltillo_(linguistics))), которое есть полноценная некомбинируемая буква, имеющая верхний и нижний регистры. Это меняет переключатель w из йод/yodꞌ, сход/sꞌhod, сэр/sꞌer, выучить/vyꞌuchitį, выискивать/vyꞌiskivatį.
* śh вместо sjh (Щ), dž вместо dzh (ДЖ).
* Большая часть диакритики используется исключительно для аббревиатур: ГЭС/GÈS, АЭС/AES, ЖКХ/ŽKĤ, ЖЭК/ŽÈK, ЕС/ÊS, США/SŠA, МЧС/MČS, ЮАР/ÛAR, ЭЭГ/EEG, ЕГЭ/ÊGÈ, ЧС/ČS, микрорайон Щ/mikrorayonw Ś/mikrorayonꞌ Ś.

*Всё остальное тоже самое, что и в предыдущем варианте.* Новые буквы, встречающиеся не в аббревиатурах: Śś(Щ), Įį(Ь, смягчение), DŽdž(ДЖ), Ꞌꞌ(буква для частых диграфов), Ɂɂ(очень редкие Ъ,Ь), Ŷŷ(очень редкое Й).

\c - consonant, согласная.

|          |  **a**  | **б** |  **в**  | **г**  | **д** |
| -------- |:-------:|:-----:|:-------:|:------:|:-----:|
| translit |  a/wa   |   b   |    v    |   g    |   d   |
| latinica |  a/ꞌa   |       |         |        |       |
|          |  **е**  | **ё** |  **ж**  | **з**  | **и** |
| translit |  ye/e   | yo/jo |   zh    |   z    |   i   |
| latinica |         | yo/įo |         |        |       |
|          |  **й**  | **к** |  **л**  | **м**  | **н** |
| translit |  y/yihh |   k   |    l    |   m    |   n   |
| latinica |   y/ŷ   |       |         |        |       |
|          |  **о**  | **п** |  **р**  | **с**  | **т** |
|          |  o/wo   |   p   |    r    |   s    |   t   |
|          |  o/ꞌo   |       |         |        |       |
|          |  **у**  | **ф** |  **х**  | **ц**  | **ч** |
|          |    u    |   f   |  h/kh   |   c    |  ch   |
|          |         |       |  h/ꞌh   |        |       |
|          |  **ш**  | **щ** |  **ъ**  | **ы**  | **ь** |
| translit |   sh    |  sjh  | None/qq |  y/wy  | j/jqq |
| latinica |         |  śh   | None/ɂ  |  y/ꞌy  | į/įɂ  |
|          |  **э**  | **ю** |  **я**  | **дж** |       |
| translit |  e/we   | yu/ju |  ya/ja  |  dzh   |       |
| latinica |  e/ꞌe   | yu/įu |  ya/įa  |   dž   |       |


|              | Правило транслита / правило латиницы                                                                              | Кириллица/Транслит/Латиница                                                                                                                                                                                                                                   |
|:------------:|:----------------------------------------------------------------------------------------------------------------- |:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
|    **ъи**    | **yi** (**ъи** после согласных в словарных словах-исключениях, когда и йотируется)                                | объимать/obyimatj, обйимать/obyimatjw/obyimatjꞌ, обйимоть/obyimotj, объимоть/obqqimotj/obɂimotj, объйимать/obqqyimatj/obɂyimatj (здесь логика модификации с помощью w(h) изменена только для словарных слов-исключений)                                           |
|    **ъ**     | None (после согласных перед **яёюе**), **qq** / **ɂ** (иначе)                                                     | изъян/izyan, объект/obyekt, объизвестить/obqqizvestitj/obɂizvestitj, Йонъин/Yonqqinw/Yonɂinꞌ, Сёркйосен/Siorkyosenw/Siorkyosenꞌ, онъ/onqq/onɂ, Муъминат/Muqqminat/Muɂminat, Чанъань/Chanqqanj/Chanɂanj, нъын/nqqwyn/nɂꞌyn                                        |
|    **ьо**    | **jyo...w** / **jyo...ꞌ** (**jyoh**) (**ьо** когда они **йотируются**, а это почти всегда)                                          | бульон/buljyonw/buljyonꞌ, бульонъён/buljyohnyon, сеньор/senjyorw/senjyorꞌ, лосьон/losjyonw/losjyonꞌ, лосьйон/losjyonww/losjyonꞌꞌ (здесь **специально для ьо** изменена логика модификации с помощью w(h))                                                                                   |
|    **ьи**    | **jyi** (**ьи** когда они **йотируются**, а это почти всегда)                                                     | ладьи/ladjyi, платьице/platjyice, ладьйи/ladjyih/ladjyiꞌ (здесь **специально для ьи** изменена логика модификации с помощью w(h))                                                                                                                                 |
|  **ь[ауэ]**  | **jy[aue]h** / **jŷ[aue]** (гласные **ауэ** после **ь** в словарных словах-исключениях, когда они **йотируются**) | бельэтаж/beljyehtazh/beljŷetazh, бельйэтаж/beljyehhtazh/beljŷehtazh, бельэт/beljqqet/beljįet (здесь логика модификации с помощью w(h) изменена только для словарных слов-исключений)                                                                             |
|    **ь**     | **jqq** / **jį** (перед гласными **аоуэиы** когда они **не** йотируются), **j** (иначе)                           | грабьармия/grabjqqarmiya/grabjįarmiya, костьутиль/kostjqqutilj/kostjįutilį, пьеса/pjyesa, пьян/pjyan, прячься/priachjsia, мыться/mytjsia, конь/konj, ньын/njqqhyn/njįÿn                                                                                       |
| **й[аоуэ]**  | **y[aoue]h** / **ŷ[aoue]** (гласные **аоуэ** после й)                                                             | йод/yohd/ŷod, йэс/yehs/ŷes                                                                                                                                                                                                                                    |
|    **й**     | **y** (остальные простые случаи), **yiw** / **ŷ** (сложные случаи)                                                | красный/krasnyy, аллилуйя/alliluyya, Байес/Bayyes, ныйя/nyyya, йиппи/yippi, нйя/nyihhya/nŷya                                                                                                                                                                                    |
|    **ы**     | **y** (после согласных), **hy** / **ÿ** (иначе) | пыл/pyl, пыхтел/pyhtel, мы/my, красный/krasnyy, Нарва-Йыэсуу/Narva-Ywywesuu/Narva-Yꞌyꞌesuu, Шайыр/Shaywyr/Shayꞌyr                                                                                                                                                                        |
| **ы[аоуэи]** | **yh[aouei]** / **ÿ[aouei]** (гласные **аоуэи** после ы)                                                          | выход/vykhod, выигрывать/vyhigryvatj/vÿigryvatj, выучить/vyhuchitj/vÿuchitj, выострить/vyhostritj/vÿostritj                                                                                                                                                   |
|    **е**     | **е** (после согласных или в словарных словах-исключениях когда е читается как э), **ye** (иначе)                 | мера/mera, еда/yeda, если/yesli, заезд/zayezd, Байес/Bayyes, заем/zayem, заём/zayom, траектория/trayektoriya, проект/proekt, проэкт/proehkt/proèkt, проэхкт/proekhkt/proèhkt, проэк/proek/proek (проект - словарное исключение с особым правилом отображения) |
|    **э**     | **ae** / **è** (после согласных), **е** (иначе)                                                                   | мэр/maer/mèr, этот/etot, аэроплан/aeroplan, поэт/poet, эротика/erotika, йэс/yehs/ŷes                                                                                                                                                                          |
|  **[яёю]**   | **i[aou]** (после согласных), **y[aou]** (иначе)                                                                  | мёд/miod, ёлка/yolka, пюре/piure, якорь/yakorj                                                                                                                                                                                                                |
|  **и[аоу]**  | **i[aou]h** / **ï[aou]** (после согласных), **i[aou]** (иначе)                                                    | пианино/piahnino/pïanino, ион/ion                                                                                                                                                                                                                             |
| **и[аоу]х**  | **i[aou]hh** / **ï[aou]h** (х становится просто h, а не kh)                                                       | диахрония/diahhroniya/dïahroniya                                                                                                                                                                                                                              |
|    **х**     | **kh** (когда есть неоднозначность из-за других диграфов и триграфов с h), **h** (иначе)                          | сход/skhod, лях/liakh, кхе/kkhe, сикх/sikkh, шхуна/shkhuna, чхать/chkhatj, отход/otkhod, хахх/hahh, хохолок/hoholok, выход/vykhod (vÿhod не каноничен, сворачивать kh не стандарт), меха/meha, эхо/eho, вече/veche, меча/mecha, сьха/sjkha, ньхи/njhi         |
|    **дж**    | **dzh** / **dž**                                                                                                  | Джордж/Dzhordzh/Džordž                                                                                                                                                                                                                                        |

Из таблицы выше видно, что для ь и ъ (особенно ъи и ьэ) придется определять отображение по умолчанию и запомненные в словарь исключения из него. Так, стоит ожидать, что ъи и ьэ по умолчанию должны быть не йотированными, но известны и йотированные исключения.

|          | Ещё примеры                         |
| -------- | ----------------------------------- |
| щ/sjh(śh) | щётка/sjhiotka/śhįotka, счёт/schjot/schįot |
| ж/zh     | ёж/yozh, возжи/vozzhi, позже/pozzhe |
| ч/ch     | Черныш/Chernysh, счётная/schjotnaya/schįotnaya |
| ш/sh     | шлем/shlem                          |
| ё/jo(įo)/yo | мёд/mjod/mįod, ёмко/yomko            |
| ю/ju(įu)/yu | мюсли/mjusli/mįusli, Юля/Yulja/Yulįa |
| я/ja(įa)/ya | Изя/Izja/Izįa, Якорь/Yakorj/Yakorį, баян/bayan |

Многие буквы совпадают с [ГОСТ 16876-71 табл. 2](https://ru.wikipedia.org/wiki/%D0%A2%D1%80%D0%B0%D0%BD%D1%81%D0%BB%D0%B8%D1%82%D0%B5%D1%80%D0%B0%D1%86%D0%B8%D1%8F_%D1%80%D1%83%D1%81%D1%81%D0%BA%D0%BE%D0%B3%D0%BE_%D0%B0%D0%BB%D1%84%D0%B0%D0%B2%D0%B8%D1%82%D0%B0_%D0%BB%D0%B0%D1%82%D0%B8%D0%BD%D0%B8%D1%86%D0%B5%D0%B9#%D0%A1%D1%80%D0%B0%D0%B2%D0%BD%D0%B8%D1%82%D0%B5%D0%BB%D1%8C%D0%BD%D0%B0%D1%8F_%D1%82%D0%B0%D0%B1%D0%BB%D0%B8%D1%86%D0%B0_%D1%81%D0%B8%D1%81%D1%82%D0%B5%D0%BC_%D1%82%D1%80%D0%B0%D0%BD%D1%81%D0%BB%D0%B8%D1%82%D0%B5%D1%80%D0%B0%D1%86%D0%B8%D0%B8) или [ГОСТ 7.79-2000 сист. Б](https://ru.wikipedia.org/wiki/%D0%A2%D1%80%D0%B0%D0%BD%D1%81%D0%BB%D0%B8%D1%82%D0%B5%D1%80%D0%B0%D1%86%D0%B8%D1%8F_%D1%80%D1%83%D1%81%D1%81%D0%BA%D0%BE%D0%B3%D0%BE_%D0%B0%D0%BB%D1%84%D0%B0%D0%B2%D0%B8%D1%82%D0%B0_%D0%BB%D0%B0%D1%82%D0%B8%D0%BD%D0%B8%D1%86%D0%B5%D0%B9#%D0%A1%D1%80%D0%B0%D0%B2%D0%BD%D0%B8%D1%82%D0%B5%D0%BB%D1%8C%D0%BD%D0%B0%D1%8F_%D1%82%D0%B0%D0%B1%D0%BB%D0%B8%D1%86%D0%B0_%D1%81%D0%B8%D1%81%D1%82%D0%B5%D0%BC_%D1%82%D1%80%D0%B0%D0%BD%D1%81%D0%BB%D0%B8%D1%82%D0%B5%D1%80%D0%B0%D1%86%D0%B8%D0%B8).

Алфавит транслитерации использует все буквы английского алфавита кроме Xx. Алфавит латиницы не использует Ww, Xx, Qq, Jj и дополнительно использует 14 новых букв (см. ниже).

***Слово на латинице является грамматически верным если:***

1. его образ от прообраза совпадает с самим словом (`lat_word == RUtoEN(ENtoRU(lat_word))`),
2. его прообраз грамматически верен (`ENtoRU(lat_word)`).

Для обратимых аббревиатур, выглядящих прилично и совместимых с чтением по-русски придётся расширять алфавит. Буквы, уже используемые в латинице, помечены скобками. Остальные - используются только в аббревиатурах:

| **я** | **е** | **ё** | **ю** | **э** | **ь** | для диграфов |
|:-----:|:-----:|:-----:|:-----:|:-----:|:-----:|:------------:|
|  Ââ   |  Êê   |  Ôô   |  Ûû   |  Èè   |  Įį   |     [Ꞌꞌ]     |
| **ч** | **щ** | **ж** | **ш** | **х** | **й** | **для ъ,ь**  |
|  Čč   | [Śś]  | [Žž]  |  Šš   |  Ĥĥ   | [Ŷŷ]  |     [Ɂɂ]     |

Ъ, Ы, Ь: Ɂ, ꞋY, JɁ

Примеры аббревиатур: ГЭС/GÈS, АЭС/AES, ЖКХ/ŽKĤ, ЖЭК/ŽÈK, ЕС/ÊS, США/SŠA, МЧС/MČS, ЮАР/ÛAR, ЭЭГ/EEG, ЕГЭ/ÊGÈ, ЧС/ČS, микрорайон Щ/mikrorayonw Ś/mikrorayonꞌ Ś.


## Raskladka klaviahtury dlia latinicy

Основная раскладка. Добавляет новые буквы, встречающиеся более менее часто: Śś(Щ), Žž(Ж), Ꞌꞌ(буква для диграфов).

| :;(\`~) | 1!  | 2"(@") | 3'(#№) | 4$  | 5%  | 6^  | 7&  | 8\* | 9(  | 0)  |    -\_     |   =#(=+)   |
|:-------:|:---:|:------:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:----------:|:----------:|
|         | Qq  |   Ww   | Ee  | Rr  | Tt  | Yy  | Uu  | Ii  | Oo  | Pp  | **Śś**([{) | **Žž**(]}) |
|         | Aa  |   Ss   | Dd  | Ff  | Gg  | Hh  | Jj  | Kk  | Ll  | **Įį**(;:) | **Ꞌꞌ**('") |    \\\|    |
|         |     |   Zz   | Xx  | Cc  | Vv  | Bb  | Nn  | Mm  | ,<  | .>  |     /?     |            |

Дополнительная раскладка. Буквы для аббревиатур и очень редких слов: Ââ(Я),Êê(Е),Ôô(Ё),Ûû(Ю),Čč(Ч),Šš(Ш),Žž(Ж),Ĥĥ(Х),Ŷŷ(Йй),Ɂɂ(редкие Ъ,Ь).

| :;  |   1!   |   2"   |   3#   |   4$   | 5%  |   6^   |   7&   | 8\* |   9(   | 0)  | -\_ |  =+  |
|:---:|:------:|:------:|:------:|:------:|:---:|:------:|:------:|:---:|:------:|:---:|:---:|:----:|
|     | **Ɂɂ** | **Ꞌꞌ** | **Êê** |   Rr   | Tt  | **Ŷŷ** | **Ûû** | Ii  | **Ôô** | Pp  | Śś  |  Žž  |
|     | **Ââ** | **Šš** |   Dd   |   Ff   | Gg  | **Ĥĥ** |   Įį   | Kk  |   Ll   | Įį  | Ꞌꞌ  | \\\| |
|     |        | **Žž** | **Èè** | **Čč** | Vv  |   Bb   |   Nn   | Mm  |   ,<   | .>  | /?  |      |


## Primer texta translitom

*По-моему, это вариант гораздо лучше подходит для русско-английских билингвов, чем варианты с большим количеством диакритических знаков. В английском нет диакритики, в русском - почти нет (ё ставят только при опасности неправильного прочтения, й трудно считать диакритикой). Так что не удивительно, что диакритика будет вызывать отторжение. В варианте минималистичной диакритики она ставится тоже в очень малом числе случаев.*

Pjyanyy master po proektu sdelal mehanicheskiy obyekt s izyanom. Yesli brak ne obnaruzhitsja, to belyye bolidy boljshe ne smogut vywigryvatj gonki.

V pjyese pro devushku v zeljonom platjyice vse sadilisj na ladjyi i plyli po reke. No tut iz lesa vyshel Dzhordzh Maksimus, konj v paljto i rvanyh dzhinsah, kotoryy chto-to vywiskival, i prikazal vsem mytjsja i gotovitj buljyonw. Znachit snova pjyom do lysyh akvalangistov.

Prepodobnyy Bayyes podkinul igraljnyye kosti. Vypalo shestj, znachit yemu pridjotsja mazatj yodw na ranu.

Mwer neboljshogo gorodishki otkryl tablicu ekselja i vozmutilsja cenoy novogo ekskavatora. Azh ekzema snova stala yego bespokoitj. Oh uzh eta pokupka vechnogo dvigatelja v proshlom godu! A tak zhe pokupka aeroplana-ekranoljota. Yesli tak poydjot i daljshe, to bjudzhetu pridjotsja hudo.

V etom vide fraza ot A to Ya nachinayet vygliadetj sovsem po-drugomu. Seychas sjhjotka novaya, no pozzhe ona stanet staraya. Chernysh ljubit kogda yego cheshut yeyu. Yozh koljuchiy i pohozh na neyo.

Skhod mestnyh zhiteley indiyskoy derevni sikkhov reshal chto zhe delatj s otkhodami kompanii "Kaligula Gay Yuliy Cezarj" (lat. /Caligula Gaius Iulius Caesar/ ). Odin iz prisutstvuyusjhih nosil hoholok na golove. On i nashjol vykhod iz situacii.

"Kto s mechom k nam pridjot, tot ot mecha i..." - ne smog dogovoritj starshiy mehanik Vasiliy.

Imeyetsja neskoljko gipotez proiskhozhdeniya sobaki, naiboleye veroyatnymi yeyo predkami schitayutsja volk i nekotoryye vidy shakalov.

V suzhdeniyah uchjonyh o predkah domashney sobaki prisutstvuyut dve tochki zreniya. Odni schitayut, chto sobaki - polifileticheskaya gruppa (proiskhodjasjhaya ot neskoljkih predkov), drugiye priderzhivayutsja mneniya, chto vse sobaki proizoshli ot odnogo predka (monofileticheskaya teoriya).


## Primer teksta latinicey

Pjyanyy master po proektu sdelal mehanicheskiy obyekt s izyanom. Yesli brak ne obnaruzhitsja, to belyye bolidy boljshe ne smogut vyꞌigryvatj gonki.

V pjyese pro devushku v zeljonom platjyice vse sadilisj na ladjyi i plyli po reke. No tut iz lesa vyshel Džordž Maksimus, konj v paljto i rvanyh džinsah, kotoryy chto-to vyꞌiskival, i prikazal vsem mytjsja i gotovitj buljyonꞌ. Znachit snova pjyom do lysyh akvalangistov.

Prepodobnyy Bayyes podkinul igraljnyye kosti. Vypalo shestj, znachit yemu pridjotsja mazatj yodꞌ na ranu.

Mꞌer neboljshogo gorodishki otkryl tablicu ekselja i vozmutilsja cenoy novogo ekskavatora. Azh ekzema snova stala yego bespokoitj. Oh uzh eta pokupka vechnogo dvigatelja v proshlom godu! A tak zhe pokupka aeroplana-ekranoljota. Yesli tak poydjot i daljshe, to bjudzhetu pridjotsja hudo.

V etom vide fraza ot A to Ya nachinayet vygliadetj sovsem po-drugomu. Seychas śhjotka novaya, no pozzhe ona stanet staraya. Chernysh ljubit kogda yego cheshut yeyu. Yozh koljuchiy i pohozh na neyo.

Sꞌhod mestnyh zhiteley indiyskoy derevni sikꞌhov reshal chto zhe delatj s otꞌhodami kompanii "Kaligula Gay Yuliy Cezarj" (lat. /Caligula Gaius Iulius Caesar/ ). Odin iz prisutstvuyuśhih nosil hoholok na golove. On i nashjol vyꞌhod iz situacii.

"Kto s mechom k nam pridjot, tot ot mecha i..." - ne smog dogovoritj starshiy mehanik Vasiliy.

Imeyetsja neskoljko gipotez proisꞌhozhdeniya sobaki, naiboleye veroyatnymi yeyo predkami schitayutsja volk i nekotoryye vidy shakalov.

V suzhdeniyah uchjonyh o predkah domashney sobaki prisutstvuyut dve tochki zreniya. Odni schitayut, chto sobaki - polifileticheskaya gruppa (proisꞌhodjaśhaya ot neskoljkih predkov), drugiye priderzhivayutsja mneniya, chto vse sobaki proizoshli ot odnogo predka (monofileticheskaya teoriya).


## TO DO

* [ ] Написать кодировщик и декодировщик на питоне, а потом проверить на каком-нибудь словаре, а так же на случайно-сгенерированных словах. Я не проверял алгоритм декодирования даже мысленно. Но интуитивно чувствую, что он хорошо определён и реализуем. Собственно, алгоритм кодировки строился такой, чтобы не было такого, чтобы разные русские слова (любые) отображались в одну и ту же транслитерацию.
* [ ] Попробовать сделать фильтр pandoc. Но там надо посмотреть какой элемент гарантированно содержит только голый текст.
* [ ] Сделать режим, в котором просто все русские обособленные слова преобразуются в массиве текста.
* [ ] Оформить в виде модуля питона с CLI.
* [ ] Написать инструкцию как сконвертировать произвольную страницу в интернете с помощью сохранения как html и конвертации фильтром/пандоком.
* [ ] Попробовать сделать однострочный джавастрипт, которым можно перевести любую уже открытую страницу в интернете.

Mics:

* [latin capital letter z with stroke](https://en.wikipedia.org/wiki/List_of_Unicode_characters), [List of Latin-script letters](https://en.wikipedia.org/wiki/List_of_Latin-script_letters).
* [Частотность](https://ru.wikipedia.org/wiki/%D0%A7%D0%B0%D1%81%D1%82%D0%BE%D1%82%D0%BD%D0%BE%D1%81%D1%82%D1%8C)
