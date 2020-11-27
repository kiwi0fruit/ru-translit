# ru-translit (kiwi0fruit's)

### Uniquely reversible Russian to English transliteration/romanization: no extra letters, two versions - with and without non-letters (russkaja latinica)

### Однозначно обратимая транслитерация/романизация из русского в английский алфавит: без дополнительных букв, две версии - с небуквенными знаками и без (русская латиница)

Содержание:

* [Четыре разные "И" русской латиницы от которых всё зависит](#%D1%87%D0%B5%D1%82%D1%8B%D1%80%D0%B5-%D1%80%D0%B0%D0%B7%D0%BD%D1%8B%D0%B5-%D0%B8-%D1%80%D1%83%D1%81%D1%81%D0%BA%D0%BE%D0%B9-%D0%BB%D0%B0%D1%82%D0%B8%D0%BD%D0%B8%D1%86%D1%8B-%D0%BE%D1%82-%D0%BA%D0%BE%D1%82%D0%BE%D1%80%D1%8B%D1%85-%D0%B2%D1%81%D1%91-%D0%B7%D0%B0%D0%B2%D0%B8%D1%81%D0%B8%D1%82)
* [Базовая латиница 25](#%D0%B1%D0%B0%D0%B7%D0%BE%D0%B2%D0%B0%D1%8F-%D0%BB%D0%B0%D1%82%D0%B8%D0%BD%D0%B8%D1%86%D0%B0-25)
* [Примеры интересных случаев](#%D0%BF%D1%80%D0%B8%D0%BC%D0%B5%D1%80%D1%8B-%D0%B8%D0%BD%D1%82%D0%B5%D1%80%D0%B5%D1%81%D0%BD%D1%8B%D1%85-%D1%81%D0%BB%D1%83%D1%87%D0%B0%D0%B5%D0%B2)
* [Аббревиатуры](#%D0%B0%D0%B1%D0%B1%D1%80%D0%B5%D0%B2%D0%B8%D0%B0%D1%82%D1%83%D1%80%D1%8B)
* [Пример текста](#%D0%BF%D1%80%D0%B8%D0%BC%D0%B5%D1%80-%D1%82%D0%B5%D0%BA%D1%81%D1%82%D0%B0)

Придумал в качестве развлечения ещё один транслит.

Развлечением было удовлетворить ограничениям:

* Транслит - полностью обратимый (является кодировкой без потерь и позволяет точно восстановить произвольный русский текст из латиницы). То есть, это [**инъективное отображение**](https://ru.wikipedia.org/wiki/%D0%98%D0%BD%D1%8A%D0%B5%D0%BA%D1%86%D0%B8%D1%8F_(%D0%BC%D0%B0%D1%82%D0%B5%D0%BC%D0%B0%D1%82%D0%B8%D0%BA%D0%B0)),
* Транслит содержит только буквы (в частности, не использует апостроф): отображение из русских букв `[А-Яа-я]` в английские `[A-Za-z]` без добавлений,
* Не содержит далёких фонетических замен типа щ → w. Желательно, чтобы "звучало" похоже на английский или математический латинский.


## Четыре разные "И" русской латиницы от которых всё зависит

*Четыре разные "И" русской латиницы от которых всё зависит*.

Придумывая латиницы с не более, чем четырьмя новыми буквами, обнаружил, что все отлично срастается после задания трёх разных "И":

* йотирующая и — **й** (включая спрятанную в еёюя и редко даже в ьи и ьо),
* смягчающая и — **ь** (включая спрятанную в еёюя и даже в и),
* ы — **ы**,
* собственно, и — **и**.

Но в базовой латинице букв со смыслом "и" всего три: i, j (диакритический вариант i), y ("и" греческая). А нужно 4. Поэтому, получаются компромиссы.


## Базовая латиница 25

Основные идеи внутренней грамматики **транслита без диакритики**:

* йотирующая, но не смягчающая, "и" (йот; еёюя НЕ после согласных) — **j** (яма/jama, съезд/sjezd, пьеса/pjjesa, ладьи/ladjji), 
* смягчающая, но не йотирующая, "и" (ь; ёюя после согласных) — **i** после согласных перед aouy, иначе - **j**, но йотирование имеет приоритет (мёд/miod, пьеса/pjjesa, конь/konj, пион/piyon),
* "ы" — **y** (мы/my),
* собственно, "и" — **iy** после согласных перед aou, иначе - **i** (мир/mir, лён/lion, пион/piyon).

Дополнительно:

* **e** после согласных всегда смягчает, можно опустить i (пень/penj). В остальных случаях **e** обозначает звук э (это/eto, поэт/poet). Йотировать надо для уезд/ujezd. Убрать смягчение после согласной можно с помощью **we/'e**: мэр/mwer/m'er, сэр/swer/s'er.
* **qq** обозначает паузу, гортанную смычку или просто игнорируемый диграф - зависит от слова (объизвестить/obqqizvestitj, грабьармия/grabjqqarmija).
* х обозначется **h/kh** (ход/hod, сход/skhod).
* слова на латинице из других языков можно писать, экранируя с помощью " /" и "/ ".
* разные виды йотирования переключаются для jo,je,ju,ja. Причем, когда место возможного переключения йотирования всего одно, то переключение происходит в конце слова - простой вариант. А когда их несколько, то сразу перед диграфом jo,ja,ju,je  (ёд/jod, йод/jodw/jod', ёдйод/jodwjod/jod'jod).
* разные способы написания звука /щ/ переключаются так же в конце слова, только с помощью **w**/**'** когда йотации гласных нет в слове и с помощью **ww**/**"** когда она есть (счёт/schiotw/schiot', щётка/schiotka, считаются/schitajutsiaww/schitajutsia"). Если есть неоднозначность, то отличие ставится явно префиксом **wsch**/**'sch** (считающейся/wschitajucshejsia/'schitajucshejsia).

|   **a**   |   **о**   |  **у**   |  **э**   |  **ы**   |
|:---------:|:---------:|:--------:|:--------:|:--------:|
|     a     |     o     |    u     | e/we('e) |    y     |
|   **я**   |   **ё**   |  **ю**   |  **е**   |  **и**   |
|   ia/ja   |   io/jo   |  iu/ju   |   e/je   |   i/iy   |
|   **б**   |   **в**   |  **г**   |  **д**   |  **ж**   |
|     b     |     v     |    g     |    d     |    zh    |
|   **з**   |   **й**   |  **к**   |  **л**   |  **м**   |
|     z     |  j/wj('j) |    k     |    l     |    m     |
|   **н**   |   **п**   |  **р**   |  **с**   |  **т**   |
|     n     |     p     |    r     |    s     |    t     |
|   **ф**   |   **х**   |  **ц**   |  **ч**   |  **ш**   |
|     f     |   h/kh    |    c     |    ch    |    sh    |
|   **щ**   |   **ъ**   |  **ь**   |  **сч**  |          |
|    sch    |  None/qq  |  j/jqq   | sch/wsch('sch) |    |

**По сути апостроф и w всегда стоят в одних и тех же местах, и могут дать варианты как для обычных текстов (с апострофом), так и для URL (с w).**

Алфавит транслитерации использует все буквы английского алфавита кроме Xx.

***Слово на латинице является грамматически верным если:***

1. его образ от прообраза совпадает с самим словом (`lat_word == RUtoEN(ENtoRU(lat_word))`),
2. его прообраз грамматически верен (`ENtoRU(lat_word)`).


## Примеры интересных случаев

лён/lion  
Лион/Liyon  
пион/piyon  
пиы/piyy  
мэр/mwer/m'er  
м'эр/m''er (удваивается только если прообраз от наивного образа без апострофа)  
этот/etot  
если/jesli  
конь/konj  
кони/koni  
Юля/Julia  
Юлия/Julija  
Юлиан/Juliyan  
пьяный/pjjanyj  
подъезд/podjezd  
пьеса/pjjesa  
пйеса/pwjjesa/p'jjesa  
паьеса/paqjjesa  
паьаса/paqjqqasa  
пайъеса/pajqqjesa  
ёж/jozh  
йож/jozhw/jozh'  
йод/jodw/jod'  
ёдйод/jodwjoh/jod'jod  
аллилуйя/allilujja  
ладьи/ladjji  
Таунйин/Taunjin  
Пиньиу/Pinjjiu  
Таунйиан/Taunjian  
Тарвасйыги/Tarvasjygi  
баньтьынг/banjtjqqyng  
сьйы/sjjy  
пьём/pjjom  
бульон/buljjonw/buljjon'  
выучить/vyuchitj  
выигрывать/vyigryvatj  
объимать/obqqimatj  
объизвестить/obqqizvestitj  
бельэтаж/beljqqetazh  
грабьармия/grabjqqarmija  

|         | Ещё примеры                           |
| ------- | ------------------------------------- |
| дж/dzh  | Джордж/Dzhordzh                       |
| щ/sch   | щётка/schiotka, счёт/schiotw/schiot'  |
| ж/zh    | ёж/jozh, возжи/vozzhi, позже/pozzhe   |
| ч/ch    | Черныш/Chernysh, счётная/schiotnayaww/schiotnaya" |
| ш/sh    | шлем/shlem                            |
| ё/jo/io | мёд/miod, ёмко/jomko                  |
| ю/ju/iu | мюсли/miusli, Юля/Julia               |
| я/ja/ia | Изя/Izia, Якорь/Jakorj, баян/bajan    |


## Аббревиатуры

Все слова в верхнем регистре считаются аббревиатурами и записываются по специальным правилам. Есть два варианта аббревиатур: для случаев, когда нужны только буквы базовой латиницы, и когда можно использовать не буквенные символы. В первом случае модифицирующая буква диграфа пишется в нижнем регистре, а модифицируемая буква - в верхнем. Во втором случае префиксные модифицирующие буквы **w**, **i**, **j**, **k** заменяются на **'** (апостроф), а постфиксные **h** и **y** - на **|**. Щ - особый случай: Щ/Sch/S||.

ГЭС/GwES/G'ES, АЭС/AES, ЖКХ/ZhkKH/Z|'KH, ЖЭК/ZhwEK/Z|'EK, ЕС/jES/'ES, США/SShA/SS|A, МЧС/MChS/MC|S, ЮАР/jUAR/'UAR, ЭЭГ/EEG, ЕГЭ/jEGwE/'EG'E, микрорайон Щ/mikrorajonw Sch/mikrorajon' S||, СЧК/SChKw/SC|K', ЩК/SchK/S||K, ЛЁН/LiON/L'ON, ЛИОН/LIyON/LI|ON.

ИОН/ION, ЛИЁН/LIjON/LI'ON, ЙОД/JODw/JOD', ЙЁД/JjOD/J'OD, ЁД/jOD/'OD, НЫЭ/NYE, НЫЕ/NYjE/NY'E, НЙ/NwJ/N'J.

Аббревиатур с Ь и Ъ не должно быть, поэтому в них даже W не заменяется: ЛЪЁН/LJON, ЛЬОН/LJJONW, ЛЬЁН/LJJON, ЛЬЙОН/LJJONWW

**Слова в верхнем регистре считаются аббревиатурами и пишутся по своим лаконичным правилам.** Это может ухудшать чтение текста, набранного капсом (после конверсии в латиницу). Но его и так трудно читать, так что не жалко.


## Пример текста

Piyony i vasiljki vsio jeschio rastut na poliane vozle derevni Piony, 'schitajucshejsia bogatoj.

Pjjanyj master po proektu sdelal mehanicheskij objekt s izjanom. Jesli brak ne obnaruzhitsia, to belyje bolidy boljshe ne smogut vyigryvatj gonki.

V pjjese pro devushku v zelionom platjjice vse sadilisj na ladjji i plyli po reke. No tut iz lesa vyshel Dzhordzh Maksimus, konj v paljto i rvanyh dzhinsah, kotoryj chto-to vyiskival, i prikazal vsem mytjsia i gotovitj buljjon'. Znachit snova pjjom do lysyh akvalangistov.

Prepodobnyj Bajjes podkinul igraljnyje kosti. Vypalo shestj, znachit jemu pridiotsia mazatj jod' na ranu.

M'er neboljshogo gorodishki otkryl tablicu ekselia i vozmutilsia cenoj novogo ekskavatora. Azh ekzema snova stala jego bespokoitj. Oh uzh eta pokupka vechnogo dvigatelia v proshlom godu! A tak zhe pokupka aeroplana-ekranoliota. Jesli tak pojdiot i daljshe, to biudzhetu pridiotsia hudo.

V etom vide fraza ot A to Ja nachinajet vygliadetj sovsem po-drugomu. Sejchas schiotka novaja, no pozzhe ona stanet staraja. Chernysh liubit kogda jego cheshut jeju. Jozh koliuchij i pohozh na nejo.

Skhod mestnyh zhitelej indijskoj derevni sikkhov reshal chto zhe delatj s otkhodami kompanii "Kaligula Gaj Julij Cezarj" (lat. /Caligula Gaius Iulius Caesar/ ). Odin iz prisutstvujuschih nosil hoholok na golove. On i nashiol vyhod iz situacii.

"Kto s mechom k nam pridiot, tot ot mecha i..." - ne smog dogovoritj starshij mehanik Vasilij.

----

Liubimcem Biljbo byl junyj Frodo Sumniks. Kogda Biljbo stuknulo devianosto deviatj, on vdrug usynovil sirotu Frodo, sdelal svoim naslednikom i predlozhil pereselitjsia v Zasumki. Tut uzh vse nadezhdy Derikulj-Sumniksov, davno s vozhdelenijem posmatrivavshih na usadjbu, ruhnuli okonchateljno.

Sluchaju bylo ugodno, chtoby Biljbo s Frodo jeschio i rodilisj v odin denj, 22 sentiabria.

– Frodo, maljchik moj, – skazal kak-to raz Biljbo, – perebiralsia by ty ko mne. Gliadishj, i denj rozhdenija vmeste otmechali by.

Frodo v tu poru hodil v dorostkah. Tak hobbity zovut molodiozhj v bezotvetstvennom vozraste mezhdu dvadcatjju i tridcatjju tremia, posle chego hobbit nakonec mozhet schitatj' sebia vzroslym.

Proshlo jeschio dvenadcatj let. V Zasumkah kazhdyj god veselo otmechali dvojnoj denj rozhdenija, k etomu privykli, no liubomu bylo jasno, chto nyneshnej osenjju gotovitsia nechto neobychnoje. Biljbo ispolnialosj 111 let – vozrast dlia hobbita vesjma pochtennyj, da i chislo liubopytnoje, nu a Frodo gotovilsia otmetitj tridcatitriohletije – tozhe znamemateljnaja data – sovershennoletije po-hobbitski.

----

Imejetsia neskoljko gipotez proiskhozhdenija sobaki, naiboleje verojatnymi jejo predkami schitajutsia" volk i nekotoryje vidy shakalov.

V suzhdenijah uchionyh o predkah domashnej sobaki prisutstvujut dve tochki zrenija. Odni schitajut", chto sobaki - polifileticheskaja gruppa (proiskhodiaschaja ot neskoljkih predkov), drugije priderzhivajutsia mnenija, chto vse sobaki proizoshli ot odnogo predka (monofileticheskaja teorija).


# Перенести из старой версии

|              | Правило транслита / правило латиницы                                                                                                                     | Кириллица/Транслит/Латиница                                                                                                                                                                                                          |
|:------------:|:-------------------------------------------------------------------------------------------------------------------------------------------------------- |:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
|    **ъи**    | **yi** (**ъи** после согласных в словарных словах-исключениях, когда и йотируется)                                                                       | объимать/obyimatj, обйимать/obyimatjw/obyimatj', обйимоть/obyimotj, объимоть/obqqimotj/obqqimotj, объйимать/obqqyimatj (здесь логика модификации с помощью w/h изменена только для словарных слов-исключений)                        |
|    **ъ**     | None (после согласных перед **яёюе**), **qq** (иначе)                                                                                                    | изъян/izyan, объект/obyekt, объизвестить/obqqizvestitj, Йонъин/Yonqqinw/Yonqqin', Сёркйосен/Sjorkyosenw/Sjorkyosen', онъ/onqq, Муъминат/Muqqminat, Чанъань/Chanqqanj, нъын/nqqwyn/nqq'yn                                             |
|    **ьо**    | **jyo...w** / **jyo...'** (**jyo...h** / **jŷo**) (**ьо** когда они **йотируются**, а это почти всегда)                                                  | бульон/buljyonw/buljyon', бульонъён/buljyohnyon/buljŷonyon, сеньор/senjyorw/senjyor', лосьон/losjyonw/losjyon', лосьйон/losjyonww/losjyon'' (здесь **специально для ьо** изменена логика модификации с помощью w/h)                  |
|    **ьи**    | **jyi** (**ьи** когда они **йотируются**, а это почти всегда)                                                                                            | ладьи/ladjyi, платьице/platjyice ладьйи/ladjyiw/ladjyi' (здесь **специально для ьи** изменена логика модификации с помощью w/h)                                                                                                      |
|  **ь[ауэ]**  | **jy[aue]...w** / **jy[aue]...'** (**jy[aue]...h** / **jŷ[aue]**) (гласные **ауэ** после **ь** в словарных словах-исключениях, когда они **йотируются**) | бельэтаж/beljyetazhw/beljyetazh', бельйэтаж/beljyetazhww/beljyetazh'', бельэт/beljqqet (здесь логика модификации с помощью w/h изменена только для словарных слов-исключений)                                                        |
|    **ь**     | **jqq** (перед гласными **аоуэиы** когда они **не** йотируются), **j** (иначе)                                                                           | грабьармия/grabjqqarmiya, костьутиль/kostjqqutilj, пьеса/pjyesa пьян/pjyan, прячься/prjachjsja, мыться/mytjsja, конь/konj, ньын/njqqwyn/njqq'yn                                                                                      |
| **й[аоуэ]**  | **y[aoue]...w** / **y[aoue]...'** (**y[aoue]...h** / **ŷ[aoue]**) (гласные **аоуэ** после й)                                                             | йод/yodw/yod', йэс/yesw/yes', ёдйод/yodyohd/yodŷod, ёдйойс/yodyoyhs/yodŷoys, ёдйойэ/yodyohyeh/yodŷoŷe, ёдйойе/yodyoyhye/yodŷoyye, ёдйоы/yodyohwy/yodŷo'y, ёдйоэ/yodyohwe/yodŷoe, ёдйоя/yodyohya/yodŷoya                              |
|    **й**     | **y** (остальные простые случаи), **yii** / **ŷ** (сложные случаи)                                                                                       | красный/krasnyy, аллилуйя/alliluyya, Байес/Bayyes, ныйя/nyyya, йиппи/yippi, сйс/syiis/sŷs, сйиис/syiwis/syi'is, сьйс/sjyiis/sjŷs, сьйиис/sjyiwisw/sjyi'is', сьиис/sjyiwis/sjyi'is                                                    |
|    **ы**     | **y** (после согласных), **wy** / **'y** (иначе)                                                                                                         | пыл/pyl, пыхтел/pyhtel, мы/my, красный/krasnyy, Нарва-Йыэсуу/Narva-Ywywesuu/Narva-Y'y'esuu, Шайыр/Shaywyr/Shay'yr                                                                                                                    |
| **ы[аоуэи]** | **yw[aouei]** / **y'[aouei]** (гласные **аоуэи** после ы)                                                                                                | выход/vyhod, выигрывать/vywigryvatj/vy'igryvatj, выучить/vywuchitj/vy'uchitj, выострить/vywostritj/vy'ostritj                                                                                                                        |
|    **е**     | **е** (после согласных или в словарных словах-исключениях когда е читается как э), **ye** (иначе)                                                        | мера/mera, еда/yeda, если/yesli, заезд/zayezd, Байес/Bayyes, заем/zayem, заём/zayom, траектория/trayektoriya, проект/proekt, проэкт/prowekt/pro'ekt, проэк/proek/proek (проект - словарное исключение с особым правилом отображения) |
|    **э**     | **we** / **'e** (после согласных), **е** (иначе)                                                                                                         | мэр/mwer/m'er, этот/etot, аэроплан/aeroplan, поэт/poet, эротика/erotika, йэс/yesw/yes'                                                                                                                                               |
|  **[яёю]**   | **j[aou]** (после согласных), **y[aou]** (иначе)                                                                                                         | синяя/sinjaya, мёд/mjod, ёлка/yolka, пюре/pjure, якорь/yakorj                                                                                                                                                                        |
|    **х**     | **kh** (когда есть неоднозначность из-за других диграфов и триграфов с h), **h** (иначе)                                                                 | сход/skhod, кхе/kkhe, сикх/sikkh, шхуна/shkhuna, чхать/chkhatj, отход/otkhod, хахх/hahh, хохолок/hoholok, выход/vyhod, меха/meha, эхо/eho, вече/veche, меча/mecha, сцьха/scjkha, нцьхи/ncjhi                                         |

Из таблицы выше видно, что для ь и ъ (особенно ъи и ьэ) придется определять отображение по умолчанию и запомненные в словарь исключения из него. Так, стоит ожидать, что ъи и ьэ по умолчанию должны быть не йотированными, но известны и йотированные исключения.


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
