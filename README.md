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
* ный будет nyy, уйя будет uyya, ные будет nyye; логично, однозначно, слегка разочаровывает, но неизбежно (красный/krasnyy, аллилуйя/alliluyya),
* i после согласных смягчает их, но не йотирует следующую гласную (мёд/miod), это поведение отключается добавлением h после двух гласных (пион/piohn),
* j после согласной обозначает смягчение. Других использований быть не должно. В частности, не должно быть комбинаций ja, je и т.д. (пьеса/pjyesa, конь/konj).
* e после согласных всегда смягчает, можно опустить i (пень/penj). В остальных случаях e обозначает звук э (это/eto, поэт/poet). Йотировать надо для уезд/uyezd. Убрать смягчение после согласной можно с помощью ae: мэр/maer. Это можно отключить с помощью h: маэстро/maehstro.
* qq обозначает паузу, гортанную смычку или просто игнорируемый диграф (зависит от слова).
* слова на латинице из других языков можно писать, экранируя с помощью " /" и "/ ".

Парная **латиница с диакритикой** отличается от предыдущего варианта тем, что:

* Jj заменена на Įį в значении смягчения предыдущей согласной.
* Это совместимо меняет переключатель h из Лион/Liohn/Lïon, лён/lion.
* Так же AEae после согласных заменена на Ęę. Это совместимо меняет переключатель h из маэстро/maehstro/maęstro, мэр/maer/męr.
* Тоже самое с йод/yohd/ŷod и выучить/vyhuchitj/vÿuchitj.
* ŝh вместо sjh (Щ), dž вместо dzh (ДЖ).
* Диакритика над гласными это точки, а над согласными - крышки и гачеки.
* Большая часть диакритики используется исключительно для аббревиатур: ГЭС/GĘS, АЭС/AES, ЖКХ/ŽKĤ, ЖЭК/ŽĘK, ЕС/ĖS, США/SŠA, МЧС/MČS, ЮАР/ÜAR, ЭЭГ/EEG, ЕГЭ/ĖGĘ, ЧС/ČS, микрорайон Щ/mikrorayohn Ŝ/mikroraŷon Ŝ.

*Всё остальное тоже самое, что и в предыдущем варианте.* Новые буквы, встречающиеся не в аббревиатурах: Ŝŝ(Щ), Žž(Ж), Ęę(Э), Ïï(И), Ÿÿ(Ы), Ŷŷ(Й), Įį(Ъ).

|          |  **a**  | **б** |  **в**  | **г**  |  **д**   |
| -------- |:-------:|:-----:|:-------:|:------:|:--------:|
| translit |  a/ha   |   b   |    v    |   g    |    d     |
| latinica |    a    |       |         |        |          |
|          |  **е**  | **ё** |  **ж**  | **з**  |  **и**   |
| translit |  e/ye   | io/yo |   zh    |   z    |   i/hi   |
| latinica |         |       |         |        |   i/ï    |
|          |  **й**  | **к** |  **л**  | **м**  |  **н**   |
| translit |    y    |   k   |    l    |   m    |    n     |
| latinica |   y/ŷ   |       |         |        |          |
|          |  **о**  | **п** |  **р**  | **с**  |  **т**   |
| translit |  o/ho   |   p   |    r    |   s    |    t     |
| latinica |    o    |       |         |        |          |
|          |  **у**  | **ф** |  **х**  | **ц**  |  **ч**   |
| translit |  u/hu   |   f   |  h/kh   |   c    |    ch    |
| latinica |    u    |       |         |        |          |
|          |  **ш**  | **щ** |  **ъ**  | **ы**  |  **ь**   |
| translit |   sh    |  sjh  | None/qq |  y/hy  |  j/jqq   |
| latinica |         |  ŝh   | None/į  |  y/ÿ   |   j/jį   |
|          |  **э**  | **ю** |  **я**  | **дж** |          |
| translit | ae/e/he | iu/yu |  ia/ya  |  dzh   |          |
| latinica |   ę/e   |       |         |   dž   |          |


|              | Правило транслита / правило латиницы                                                                                                                               | Кириллица/Транслит/Латиница                                                                                                                                                                                                              |
|:------------:|:------------------------------------------------------------------------------------------------------------------------------------------------------------------ |:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
|    **ъи**    | **yi** (**ъи** после согласных в словарных словах-исключениях, когда и йотируется)                                                                                 | объимать/obyimatj/obyimatį, обйимать/obyihmatj/obŷimatį, обйимоть/obyimotj/obyimotį, объимоть/obqqimotj/obqqimotį, объйимать/obqqyimatj/obqqyimatį (здесь логика модификации с помощью h изменена только для словарных слов-исключений) |
|    **ъ**     | None (после согласных перед **яёюе**), **qq** (иначе)                                                                                                              | изъян/izyan, объект/obyekt, объизвестить/obqqizvestitj/obqqizvestitį, Йонъин/Yonhqqin, Сёркйосен/Siorkyohsen/Siorkŷosen, онъ/onqq, Муъминат/Muqqminat, Чанъань/Chanqqanj/Chanqqanį, нъын/nqqhyn/nqqÿn                                               |
|    **ьо**    | **jyoh** / **įyoh** (**ьо** когда они **йотируются**, а это почти всегда)                                                                                          | бульон/buljyohn/bulįŷon, сеньор/senjyohr/senįŷor, лосьон/losjyohn/losįŷon, лосьйон/losjyohhn/losįŷohn (здесь **специально для ьо** изменена логика модификации с помощью h)                                                              |
|    **ьи**    | **jyi** / **įyi** (**ьи** когда они **йотируются**, а это почти всегда)                                                                                            | ладьи/ladjyi/ladįyi, платьице/platjyice/platįyice, ладьйи/ladjyih/ladįŷi (здесь **специально для ьи** изменена логика модификации с помощью h)                                                                                          |
|  **ь[ауэ]**  | **jy[aue]h** / **įy[aue]h** (гласные **ауэ** после **ь** в словарных словах-исключениях, когда они **йотируются**)                                                 | бельэтаж/beljyehtazh/belįŷetazh, бельйэтаж/beljyehhtazh/belįŷehtazh, бельэт/beljqqet/belįet (здесь логика модификации с помощью h изменена только для словарных слов-исключений)                                                         |
|    **ь**     | **jqq** / **į** (перед гласными **аоуэиы** когда они **не** йотируются), **j** / **į**(иначе)                                                                      | грабьармия/grabjqqarmiya/grabįarmiya, костьутиль/kostjqqutilj/kostįutilį, пьеса/pjyesa/pįyesa, пьян/pjyan/pįyan, прячься/priachjsia/priachįsia, мыться/mytjsia/mytįsia, конь/konj/konį, ньын/njqqhyn/nįÿn                                |
| **й[аоуэ]**  | **y[aoue]h** / **ŷ[aoue]** (гласные **аоуэ** после й)                                                                                                              | йод/yohd/ŷod, йэс/yehs/ŷes                                                                                                                                                                                                               |
|    **й**     | **y** (остальные случаи)                                                                                                                                           | красный/krasnyy, аллилуйя/alliluyya, Байес/Bayyes, ныйя/nyyya, йиппи/yippi                                                                                                                                                               |
|    **ы**     | **y** (после согласных), **hy** / **ÿ** (иначе)                                                                                                                    | пыл/pyl, пыхтел/pyhtel, Нарва-Йыэсуу/Narva-Yhyhesuu/Narva-Yÿesuu, Шайыр/Shayhyr/Shayÿr                                                                                                                                                   |
| **ы[аоуэи]** | **yh[aouei]** / **ÿ[aouei]** (гласные **аоуэи** после ы)                                                                                                           | выход/vykhod/vÿhod, выигрывать/vyhigryvatj/vÿigryvatį, выучить/vyhuchitj/vÿuchitį, выострить/vyhostritj/vÿostritį                                                                                              |
|    **е**     | **е** (после согласных или в словарных словах-исключениях когда е читается как э), **ye** (иначе)                                                                  | мера/mera, еда/yeda, если/yesli, заезд/zayezd, Байес/Bayyes, заем/zayem, заём/zayom, траектория/trayektoriya, проект/proekt, проэкт/proehkt/proękt, проэхкт/proekhkt/proęhkt, проэк/proek/proek (проект - словарное исключение с особым правилом отображения)      |
|    **э**     | **ae** / **ę** (после согласных), **е** (иначе)                                                                                                                    | мэр/maer/męr, этот/etot, аэроплан/aeroplan, поэт/poet, эротика/erotika, йэс/yehs/ŷes                                                                                                                                                     |
| **аэ\|аэх**  | **aeh\|aehh** / **aę\|aęh** (после согласных)                                                                                                                      | маэстро/maehstro/maęstro, Алаэхос/Alaehhos/Alaęhos                                                                                                                                                                                       |
|  **[яёю]**   | **i[aou]** / **į[aou]** (после согласных), **y[aou]** (иначе)                                                                                                      | мёд/miod, ёлка/yolka, пюре/piure, якорь/yakorj/yakorį                                                                                                                                                                         |
|  **и[аоу]**  | **i[aou]h** / **ï[aou]** (после согласных), **i[aou]** (иначе)                                                                                                     | пианино/piahnino/pïanino, ион/ion                                                                                                                                                                                                        |
| **и[аоу]х**  | **i[aou]hh** / **ï[aou]h** (х становится просто h, а не kh)                                                                                                        | диахрония/diahhroniya/dïahroniya                                                                                                                                                                                                         |
|    **х**     | **kh** (когда есть неоднозначность из-за других диграфов и триграфов с h), **h** (иначе)                                                                           | сход/skhod, лях/liakh, кхе/kkhe, сикх/sikkh, шхуна/shkhuna, чхать/chkhatj/chkhatį, отход/otkhod, хахх/hahh, хохолок/hoholok, выход/vykhod/vÿhod, меха/meha, эхо/eho, вече/veche, меча/mecha, сьха/sjkha/sįha, ньхи/njhi/nįhi                                         |
|    **дж**    | **dzh** / **dž** | Джордж/Dzhordzh/Džordž                                                            |


Из таблицы выше видно, что для ь и ъ (особенно ъи и ьэ) придется определять отображение по умолчанию и запомненные в словарь исключения из него. Так, стоит ожидать, что ъи и ьэ по умолчанию должны быть не йотированными, но известны и йотированные исключения.

|          | Ещё примеры                               |
| -------- | ----------------------------------------- |
| щ/sjh/ŝh | щётка/sjhiotka/ŝhiotka, счёт/schiot       |
| ж/zh     | ёж/yozh, возжи/vozzhi, позже/pozzhe       |
| ч/ch     | Черныш/Chernysh, счётная/schiotnaya       |
| ш/sh     | шлем/shlem                                |
| ё/io/yo  | мёд/miod, ёмко/yomko                      |
| ю/iu/yu  | мюсли/miusli, Юля/Yulia                   |
| я/ia/ya  | Изя/Izia, Якорь/Yakorj/Yakorį, баян/bayan |

Многие буквы совпадают с [ГОСТ 16876-71 табл. 2](https://ru.wikipedia.org/wiki/%D0%A2%D1%80%D0%B0%D0%BD%D1%81%D0%BB%D0%B8%D1%82%D0%B5%D1%80%D0%B0%D1%86%D0%B8%D1%8F_%D1%80%D1%83%D1%81%D1%81%D0%BA%D0%BE%D0%B3%D0%BE_%D0%B0%D0%BB%D1%84%D0%B0%D0%B2%D0%B8%D1%82%D0%B0_%D0%BB%D0%B0%D1%82%D0%B8%D0%BD%D0%B8%D1%86%D0%B5%D0%B9#%D0%A1%D1%80%D0%B0%D0%B2%D0%BD%D0%B8%D1%82%D0%B5%D0%BB%D1%8C%D0%BD%D0%B0%D1%8F_%D1%82%D0%B0%D0%B1%D0%BB%D0%B8%D1%86%D0%B0_%D1%81%D0%B8%D1%81%D1%82%D0%B5%D0%BC_%D1%82%D1%80%D0%B0%D0%BD%D1%81%D0%BB%D0%B8%D1%82%D0%B5%D1%80%D0%B0%D1%86%D0%B8%D0%B8) или [ГОСТ 7.79-2000 сист. Б](https://ru.wikipedia.org/wiki/%D0%A2%D1%80%D0%B0%D0%BD%D1%81%D0%BB%D0%B8%D1%82%D0%B5%D1%80%D0%B0%D1%86%D0%B8%D1%8F_%D1%80%D1%83%D1%81%D1%81%D0%BA%D0%BE%D0%B3%D0%BE_%D0%B0%D0%BB%D1%84%D0%B0%D0%B2%D0%B8%D1%82%D0%B0_%D0%BB%D0%B0%D1%82%D0%B8%D0%BD%D0%B8%D1%86%D0%B5%D0%B9#%D0%A1%D1%80%D0%B0%D0%B2%D0%BD%D0%B8%D1%82%D0%B5%D0%BB%D1%8C%D0%BD%D0%B0%D1%8F_%D1%82%D0%B0%D0%B1%D0%BB%D0%B8%D1%86%D0%B0_%D1%81%D0%B8%D1%81%D1%82%D0%B5%D0%BC_%D1%82%D1%80%D0%B0%D0%BD%D1%81%D0%BB%D0%B8%D1%82%D0%B5%D1%80%D0%B0%D1%86%D0%B8%D0%B8).

Алфавит транслитерации использует все буквы английского алфавита кроме Ww, Xx. Алфавит латиницы не использует Ww, Xx, Jj. Но зато дополнительно использует 14 новых букв (см. ниже).

***Слово на латинице является грамматически верным если:***

1. его образ от прообраза совпадает с самим словом (`lat_word == RUtoEN(ENtoRU(lat_word))`),
2. его прообраз грамматически верен (`ENtoRU(lat_word)`).

Для обратимых аббревиатур, выглядящих прилично и совместимых с чтением по-русски придётся расширять алфавит. Буквы, уже используемые в латинице, помечены скобками. Остальные - используются только в аббревиатурах:

| **я** | **е** | **ё** | **ю** | **и** | **ы** | **э** |
|:-----:|:-----:|:-----:|:-----:|:-----:|:-----:|:-----:|
|  Ää   |  Ėė   |  Öö   |  Üü   | [Ïï]  | [Ÿÿ]  | [Ęę]  |
| **ч** | **щ** | **ж** | **ш** | **х** | **й** | **ь** |
|  Čč   | [Ŝŝ]  |  [Žž] |  Šš   |  Ĥĥ   | [Ŷŷ]  | [Įį]  |

**ъ**: QQqq.


Примеры аббревиатур: ГЭС/GĘS, АЭС/AES, ЖКХ/ŽKĤ, ЖЭК/ŽĘK, ЕС/ĖS, США/SŠA, МЧС/MČS, ЮАР/ÜAR, ЭЭГ/EEG, ЕГЭ/ĖGĘ, ЧС/ČS, микрорайон Щ/mikrorayohn Ŝ.


## Raskladka klaviahtury dlia latinicy

Основная раскладка. Добавляет новые буквы, встречающиеся не в аббревиатурах: Įį(Ь), Ŝŝ(Щ), Žž(Ж), Ęę(Э), Ïï(И), Ÿÿ(Ы), Ŷŷ(Й).

| Ÿÿ(\`~) | 1!        | 2@        | 3#        | 4$ | 5%  | 6^ | 7&        | 8\* | 9(  | 0) |     -\_    |   =+       |
|:-------:|:---------:|:---------:|:---------:|:--:|:---:|:--:|:---------:|:---:|:---:|:--:|:----------:|:----------:|
|         | **Ŷŷ**(q) | **Ïï**(w) |   Ee      | Rr | Tt  | Yy |   Uu      | Ii  | Oo  | Pp | **Ŝŝ**([{) | **Žž**(]}) |
|         | Aa        |   Ss      |   Dd      | Ff | Gg  | Hh | **Įį**(j) | Kk  | Ll  | ;: | '"         | \\\|       |
|         |           |   Zz      | **Ęę**(x) | Cc | Vv  | Bb |   Nn      | Mm  | ,<  | .> | /?         |            |

Дополнительная раскладка. Буквы для аббревиатур: Ää(Я),Ėė(Е),Öö(Ё),Üü(Ю),Čč(Ч),Šš(Ш),Žž(Ж),Ĥĥ(Х).

| Ÿÿ  |   1!   |   2@   |   3#   |   4$   | 5%  |   6^   |   7&   |  8\*   |   9(   | 0)  | -\_ | =+   |
|:---:|:------:|:------:|:------:|:------:|:---:|:------:|:------:|:------:|:------:|:---:|:---:|:----:|
|     | **Qq** |   Ïï   | **Ėė** |   Rr   | Tt  | **Ŷŷ** | **Üü** | **Ïï** | **Öö** | Pp  | Ŝŝ  | Žž   |
|     | **Ää** | **Šš** |   Dd   |   Ff   | Gg  | **Ĥĥ** |   Įį   |   Kk   |   Ll   | ;:  | '"  | \\\| |
|     |        | **Žž** |   Ęę   | **Čč** | Vv  |   Bb   |   Nn   |   Mm   |   ,<   | .>  | /?  |      |


## Primer texta translitom

*По-моему, это вариант гораздо лучше подходит для русско-английских билингвов, чем варианты с большим количеством диакритических знаков. В английском нет диакритики, в русском - почти нет (ё ставят только при опасности неправильного прочтения, й трудно считать диакритикой). Так что не удивительно, что диакритика будет вызывать отторжение. В варианте минималистичной диакритики она ставится тоже в очень малом числе случаев.*

Pjyanyy master po proektu sdelal mehanicheskiy obyekt s izyanom. Yesli brak ne obnaruzhitsia, to belyye bolidy boljshe ne smogut vyhigryvatj gonki.

V pjyese pro devushku v zelionom platjyice vse sadilisj na ladjyi i plyli po reke. No tut iz lesa vyshel Dzhordzh Maksimus, konj v paljto i rvanyh dzhinsah, kotoryy chto-to vyhiskival, i prikazal vsem mytjsia i gotovitj buljyohn. Znachit snova pjyom do lysyh akvalangistov.

Prepodobnyy Bayyes podkinul igraljnyye kosti. Vypalo shestj, znachit yemu pridiotsia mazatj yohd na ranu.

Maer neboljshogo gorodishki otkryl tablicu ekselia i vozmutilsia cenoy novogo ekskavatora. Azh ekzema snova stala yego bespokoitj. Oh uzh eta pokupka vechnogo dvigatelia v proshlom godu! A tak zhe pokupka aeroplana-ekranoliota. Yesli tak poydiot i daljshe, to biudzhetu pridiotsia hudo.

V etom vide fraza ot A to Ya nachinayet vygliadetj sovsem po-drugomu. Seychas sjhiotka novaya, no pozzhe ona stanet staraya. Chernysh liubit kogda yego cheshut yeyu. Yozh koliuchiy i pohozh na neyo.

Skhod mestnyh zhiteley indiyskoy derevni sikkhov reshal chto zhe delatj s otkhodami kompanii "Kaligula Gay Yuliy Cezarj" (lat. /Caligula Gaius Iulius Caesar/ ). Odin iz prisutstvuyusjhih nosil hoholok na golove. On i nashiol vykhod iz situacii.

"Kto s mechom k nam pridiot, tot ot mecha i..." - ne smog dogovoritj starshiy mehanik Vasiliy.

Imeyetsia neskoljko gipotez proiskhozhdeniya sobaki, naiboleye veroyatnymi yeyo predkami schitayutsia volk i nekotoryye vidy shakalov.

V suzhdeniyakh uchionyh o predkah domashney sobaki prisutstvuyut dve tochki zreniya. Odni schitayut, chto sobaki - polifileticheskaya gruppa (proiskhodiasjhaya ot neskoljkih predkov), drugiye priderzhivayutsia mneniya, chto vse sobaki proizoshli ot odnogo predka (monofileticheskaya teoriya).


## Primer teksta latinicey

Pįyanyy master po proektu sdelal mehanicheskiy obyekt s izyanom. Yesli brak ne obnaruzhitsia, to belyye bolidy bolįshe ne smogut vÿigryvatį gonki.

V pįyese pro devushku v zelionom platįyice vse sadilisį na ladįyi i plyli po reke. No tut iz lesa vyshel Džordž Maksimus, konį v palįto i rvanyh džinsah, kotoryy chto-to vÿiskival, i prikazal vsem mytįsia i gotovitį bulįyohn. Znachit snova pįyom do lysyh akvalangistov.

Prepodobnyy Bayyes podkinul igralįnyye kosti. Vypalo shestį, znachit yemu pridiotsia mazatį ŷod na ranu.

Męr nebolįshogo gorodishki otkryl tablicu ekselia i vozmutilsia cenoy novogo ekskavatora. Azh ekzema snova stala yego bespokoitį. Oh uzh eta pokupka vechnogo dvigatelia v proshlom godu! A tak zhe pokupka aeroplana-ekranoliota. Yesli tak poydiot i dalįshe, to biudžetu pridiotsia hudo.

V etom vide fraza ot A to Ya nachinayet vygliadetį sovsem po-drugomu. Seychas ŝhiotka novaya, no pozzhe ona stanet staraya. Chernysh liubit cogda yego cheshut yeyu. Yozh koliuchiy i pohozh na neyo.

Skhod mestnyh zhiteley indiyskoy derevni sikkhov reshal chto zhe delatį s otkhodami companii "Kaligula Gay Yuliy Cezarį" (lat. /Caligula Gaius Iulius Caesar/ ). Odin iz prisutstvuyuŝhih nosil hoholok na golove. On i nashiol vÿhod iz situacii.

"Kto s mechom k nam pridiot, tot ot mecha i..." - ne smog dogovoritį starshiy mehanik Vasiliy.

Imeyetsia neskolįko gipotez proiskhozhdeniya sobaki, naiboleye veroyatnymi yeyo predkami schitayutsia volk i nekotoryye vidy shakalov.

V suzhdeniyakh uchionyh o predkah domashney sobaki prisutstvuyut dve tochki zreniya. Odni schitayut, chto sobaki - polifileticheskaya gruppa (proiskhodiaŝhaya ot neskolįkih predkov), drugiye priderzhivayutsia mneniya, chto vse sobaki proizoshli ot odnogo predka (monofileticheskaya teoriya).


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
