# ru-translit (kiwi0fruit's)

### Uniquely reversible Russian to English transliteration (no extra letters, diacritics and non-letters) and dual romanization with diacritics (russkaya latinica)

### Однозначно обратимая транслитерация из русского в английский алфавит (без дополнительных букв, диакритических и небуквенных знаков) и парная к ней романизация с диакритикой (русская латиница)

Содержание:

* [Четыре разные "И" русской латиницы от которых всё зависит](#%D1%87%D0%B5%D1%82%D1%8B%D1%80%D0%B5-%D1%80%D0%B0%D0%B7%D0%BD%D1%8B%D0%B5-%D0%B8-%D1%80%D1%83%D1%81%D1%81%D0%BA%D0%BE%D0%B9-%D0%BB%D0%B0%D1%82%D0%B8%D0%BD%D0%B8%D1%86%D1%8B-%D0%BE%D1%82-%D0%BA%D0%BE%D1%82%D0%BE%D1%80%D1%8B%D1%85-%D0%B2%D1%81%D1%91-%D0%B7%D0%B0%D0%B2%D0%B8%D1%81%D0%B8%D1%82)
* [Новая версия]()
* [Старая версия]()
  * [Кириллица <=> латиница](#%D0%BA%D0%B8%D1%80%D0%B8%D0%BB%D0%BB%D0%B8%D1%86%D0%B0--%D0%BB%D0%B0%D1%82%D0%B8%D0%BD%D0%B8%D1%86%D0%B0)
  * [Раскладка клавиатуры для латиницы](#%D1%80%D0%B0%D1%81%D0%BA%D0%BB%D0%B0%D0%B4%D0%BA%D0%B0-%D0%BA%D0%BB%D0%B0%D0%B2%D0%B8%D0%B0%D1%82%D1%83%D1%80%D1%8B-%D0%B4%D0%BB%D1%8F-%D0%BB%D0%B0%D1%82%D0%B8%D0%BD%D0%B8%D1%86%D1%8B)
  * [Пример текста транслитом](#%D0%BF%D1%80%D0%B8%D0%BC%D0%B5%D1%80-%D1%82%D0%B5%D0%BA%D1%81%D1%82%D0%B0-%D1%82%D1%80%D0%B0%D0%BD%D1%81%D0%BB%D0%B8%D1%82%D0%BE%D0%BC)
  * [Пример текста латиницей](#%D0%BF%D1%80%D0%B8%D0%BC%D0%B5%D1%80-%D1%82%D0%B5%D0%BA%D1%81%D1%82%D0%B0-%D0%BB%D0%B0%D1%82%D0%B8%D0%BD%D0%B8%D1%86%D0%B5%D0%B9)

Придумал в качестве развлечения ещё один транслит.

Развлечением было удовлетворить ограничениям:

* Транслит - полностью обратимый (является кодировкой без потерь и позволяет точно восстановить произвольный русский текст из латиницы). То есть, это [**инъективное отображение**](https://ru.wikipedia.org/wiki/%D0%98%D0%BD%D1%8A%D0%B5%D0%BA%D1%86%D0%B8%D1%8F_(%D0%BC%D0%B0%D1%82%D0%B5%D0%BC%D0%B0%D1%82%D0%B8%D0%BA%D0%B0)),
* Транслит содержит только буквы (в частности, не использует апостроф): отображение из русских букв `[А-Яа-я]` в английские `[A-Za-z]` без добавлений,
* Не содержит далёких фонетических замен типа щ → w. Желательно, чтобы "звучало" похоже на английский или математический латинский.


# Четыре разные "И" русской латиницы от которых всё зависит

*Четыре разные "И" русской латиницы от которых всё зависит*.

Придумывая латиницы с не более, чем четырьмя новыми буквами, обнаружил, что все отлично срастается после задания трёх разных "И":

* йотирующая и — **й** (включая спрятанную в еёюя и редко даже в ьи и ьо),
* смягчающая и — **ь** (включая спрятанную в еёюя и даже в и),
* ы — **ы**,
* собственно, и — **и**.

Но в базовой латинице букв со смыслом "и" всего три: i, j (диакритический вариант i), y ("и" греческая). А нужно 4. Поэтому, получаются компромиссы.

*Данная транслитерация будет*:

* йотирующая и — **y**,
* смягчающая и — **j**,
* ы — *тоже* **y**,
* собственно, и — **i**.


# Новая версия

## Базовая латиница 25

Основные идеи внутренней грамматики **транслита без диакритики**:

* йотирующая, но не смягчающая, "и" (йот; еёюя НЕ после согласных) — **j** (яма/jama, съезд/sjezd, пьеса/pjjesa, ладьи/ladjji), 
* смягчающая, но не йотирующая, "и" (ь; ёюя после согласных) — **i** после согласных перед aouy, иначе - **j**, но йотирование имеет приоритет (мёд/miod, пьеса/pjjesa, конь/konj, пион/piyon),
* "ы" — **y** (мы/my),
* собственно, "и" — **iy** после согласных перед aou, иначе - **i** (мир/mir, лён/lion, пион/piyon).
* префиксный изолятор для гласных — **w**/**'** (мэр/mwer/m'er, сэр/swer/s'er) 

Дополнительно:

* **e** после согласных всегда смягчает, можно опустить i (пень/penj). В остальных случаях **e** обозначает звук э (это/eto, поэт/poet). Йотировать надо для уезд/ujezd. Убрать смягчение после согласной можно с помощью **we/'e**: мэр/mwer/m'er, сэр/swer/s'er.
* **qq** обозначает паузу, гортанную смычку или просто игнорируемый диграф - зависит от слова (объизвестить/obqqizvestitj, грабьармия/grabjqqarmija).
* х обозначется **h/kh** (ход/hod, сход/skhod).
* слова на латинице из других языков можно писать, экранируя с помощью " /" и "/ ".
* разные виды йотирования переключаются для jo,je,ju,ja. Причем, когда место возможного переключения йотирования всего одно, то переключение происходит в конце слова - простой вариант. А когда их несколько, то сразу перед диграфом jo,ja,ju,je  (ёд/jod, йод/jodw/jod', ёдйод/jodwjod/jod'jod).
* разные способы написания звука /щ/ переключаются так же в конце слова (счёт/schiotw/schiot', щётка/schiotka). Если есть неоднозначность, то отличие ставится явно (ёдщa/jodscha, ёдсча/jodwscha/jod'scha).

|   **a**   |   **о**   |  **у**   |  **э**   |  **ы**   |
|:---------:|:---------:|:--------:|:--------:|:--------:|
| a  | o  | u | e/we(ꞌe) | y |
|   **я**   |   **ё**   |  **ю**   |  **е**   |  **и**   |
|   ia/ja   |   io/jo   |  iu/ju   |   e/je   | i/iy |
|   **б**   |   **в**   |  **г**   |  **д**   |  **ж**   |
|     b     |     v     |    g     |    d     |    zh    |
|   **з**   |   **й**   |  **к**   |  **л**   |  **м**   |
|     z     | j/wj('j) |    k     |    l     |    m     |
|   **н**   |   **п**   |  **р**   |  **с**   |  **т**   |
|     n     |     p     |    r     |    s     |    t     |
|   **ф**   |   **х**   |  **ц**   |  **ч**   |  **ш**   |
|     f     |   h/kh    |    c     |    ch    |    sh    |
|   **щ**   |   **ъ**   |  **ь**   | **сч** |          |
| sch |  None/qq  |  j/jqq   | sch/wsch('sch) |          |

**По сути апостроф и w всегда стоят в одних и тех же местах, и могут дать варианты как для обычных текстов (с апострофом), так и для URL (с w).**

### Примеры интересных случаев

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


### Аббревиатуры

Все слова в верхнем регистре считаются аббревиатурами и записываются по специальным правилам. Есть два варианта аббревиатур: для случаев, когда нужны только буквы базовой латиницы, и когда можно использовать не буквенные символы. В первом случае модифицирующая буква диграфа пишется в нижнем регистре, а модифицируемая буква - в верхнем. Во втором случае префиксные модифицирующие буквы **w**, **i**, **j**, **k** заменяются на **'** (апостроф), а постфиксные **h** и **y** - на **|**. Щ - особый случай: Sch/S||.

ГЭС/GwES/G'ES, АЭС/AES, ЖКХ/ZhkKH/Z|'KH, ЖЭК/ZhwEK/Z|'EK, ЕС/jES/'ES, США/SShA/SS|A, МЧС/MChS/MC|S, ЮАР/jUAR/'UAR, ЭЭГ/EEG, ЕГЭ/jEGwE/'EG'E, микрорайон Щ/mikrorajonw Sch/mikrorajon' S||, СЧК/SChKw/SC|K', ЩК/SchK/S||K, ЛЁН/LiON/L'ON, ЛИОН/LIyON/LI|ON.

ИОН/ION
ЛИЁН/LIjON/LI'ON
ЙОД/JODw/JOD'
ЙЁД/JjOD/J'OD
ЁД/jOD/'OD
ЛЪЁН/LJON (аббревиатур с Ь и Ъ не бывает)
ЛЬОН/LJJONW/LJION'
ЛЬЁН/LJION
ЛЬЙОН/LJIONWW/LJJON''


### Пример текста

Piyony i piyoniata vsio jeschio rastut na poliane vozle derevni Piony, 'schitajucshejsia bogatoj.

Pjjanyj master po proektu sdelal mehanicheskij objekt s izjanom. Jesli brak ne obnaruzhitsia, to belyje bolidy boljshe ne smogut vyigryvatj gonki.

V pjjese pro devushku v zelionom platjjice vse sadilisj na ladjji i plyli po reke. No tut iz lesa vyshel Dzhordzh Maksimus, konj v paljto i rvanyh dzhinsah, kotoryj chto-to vyiskival, i prikazal vsem mytjsia i gotovitj buljjon'. Znachit snova pjjom do lysyh akvalangistov.

Prepodobnyj Bajjes podkinul igraljnyje kosti. Vypalo shestj, znachit jemu pridiotsia mazatj jod' na ranu.

M'er neboljshogo gorodishki otkryl tablicu ekselia i vozmutilsia cenoj novogo ekskavatora. Azh ekzema snova stala jego bespokoitj. Oh uzh eta pokupka vechnogo dvigatelia v proshlom godu! A tak zhe pokupka aeroplana-ekranoliota. Jesli tak pojdiot i daljshe, to biudzhetu pridiotsia hudo.

V etom vide fraza ot A to Ja nachinajet vygliadetj sovsem po-drugomu. Sejchas schiotka novaja, no pozzhe ona stanet staraja. Chernysh liubit kogda jego cheshut jeju. Jozh koliuchij i pohozh na nejo.

Skhod mestnyh zhitelej indijskoj derevni sikkhov reshal chto zhe delatj s otkhodami kompanii "Kaligula Gaj Julij Cezarj" (lat. /Caligula Gaius Iulius Caesar/ ). Odin iz prisutstvujuschih nosil hoholok na golove. On i nashiol vyhod iz situacii.

"Kto s mechom k nam pridiot, tot ot mecha i..." - ne smog dogovoritj starshij mehanik Vasilij.

Imejetsia neskoljko gipotez proiskhozhdenija sobaki, naiboleje verojatnymi jejo predkami schitajutsia' volk i nekotoryje vidy shakalov.

V suzhdenijah uchionyh o predkah domashnej sobaki prisutstvujut dve tochki zrenija. Odni schitajut', chto sobaki - polifileticheskaja gruppa (proiskhodiaschaja ot neskoljkih predkov), drugije priderzhivajutsia mnenija, chto vse sobaki proizoshli ot odnogo predka (monofileticheskaja teorija).


# Старая версия

## Кириллица <=> латиница

Главной целью проекта была обратимая транслитерация в английский алфавит, близкая к английскому чтению.

Основные идеи внутренней грамматики **транслита без диакритики**:

* y значит йот,
* y йотирует следующую гласную, но не смягчает предыдущую согласную (яма/yama, съезд/syezd),
* y после согласных звучит ы, но йотирование гласных имеет приоритет (мы/my),
* разные виды йотирования переключаются после yo,ye,yu,ya. Причем, когда место возможного переключения йотирования всего одно, то переключение происходит в конце слова - простой вариант. А когда их несколько, то сразу после диграфа yo,ya,yu,ye (если после него идёт свободная й/y, то и после неё) (ёд/yod, йод/yodw, ёдйод/yodyohd, ёдйойс/yodyoyhs, ёдйойэ/yodyohyeh, ёдйойе/yodyoyhye, ёдйоы/yodyohwy, ёдйоэ/yodyohwe, ёдйоя/yodyohya).
* j после согласных смягчает их, но не йотирует следующую гласную (мёд/mjod, пьеса/pjyesa, конь/konj),
* после ы буквы й,е,ё,ю,я,а,о,у,э,и,ы становятся y,ye,yo,yu,ya,wa,wo,wu,we,wi,wy (красный/krasnyy, красные/krasnyye, аллилуйя/alliluyya, выучить/vywuchitj, выискивать/vywiskivatj).
* e после согласных всегда смягчает, можно опустить j (пень/penj). В остальных случаях e обозначает звук э (это/eto, поэт/poet). Йотировать надо для уезд/uyezd. Убрать смягчение после согласной можно с помощью we: мэр/mwer, сэр/swer.
* qq обозначает паузу, гортанную смычку или просто игнорируемый диграф - зависит от слова (объизвестить/obqqizvestitj, грабьармия/grabjqqarmiya).
* х обозначется h/kh (ход/hod, сход/skhod).
* слова на латинице из других языков можно писать, экранируя с помощью " /" и "/ ".

Парная **латиница с диакритикой** отличается от предыдущего варианта тем, что:

* Ꞌꞌ вместо Ww. Это [Saltillo](https://en.wikipedia.org/wiki/Saltillo_(linguistics)) - полноценная некомбинируемая буква, имеющая верхний и нижний регистры и попадающая под регулярное выражение`\w+`. (йод/yodꞌ, сэр/sꞌer, выучить/vyꞌuchitj, выискивать/vyꞌiskivatj).
* şch вместо scjh (Щ),
* dž вместо dzh (ДЖ),
* ŷ[aoue] вместо y[aoue]...h (ёдйод/yodŷod),
* Большая часть диакритики используется исключительно для аббревиатур: ГЭС/GÈS, АЭС/AES, ЖКХ/ŽKĤ, ЖЭК/ŽÈK, ЕС/ÊS, США/SŠA, МЧС/MČS, ЮАР/ÛAR, ЭЭГ/EEG, ЕГЭ/ÊGÈ, микрорайон Щ/mikrorayonw Ş/mikrorayonꞌ Ş.

*Всё остальное тоже самое, что и в предыдущем варианте.* Новые буквы, встречающиеся не в аббревиатурах: ŞCHşch(Щ), DŽdž(ДЖ), Ꞌꞌ(W), Ŷŷ(очень редкое Й).

**Вариант латиницы дан в скобках.**

|   **a**   |   **о**   |  **у**   |  **э**   |  **ы**   |
|:---------:|:---------:|:--------:|:--------:|:--------:|
| a/wa(ꞌa)  | o/wo(ꞌo)  | u/wu(ꞌu) | e/we(ꞌe) | y/wy(ꞌy) |
|   **я**   |   **ё**   |  **ю**   |  **е**   |  **и**   |
|   ya/ja   |   yo/jo   |  yu/ju   |   ye/e   | i/wi(ꞌi) |
|   **б**   |   **в**   |  **г**   |  **д**   |  **ж**   |
|     b     |     v     |    g     |    d     |    zh    |
|   **з**   |   **й**   |  **к**   |  **л**   |  **м**   |
|     z     | y/y\*h(ŷ) |    k     |    l     |    m     |
|   **н**   |   **п**   |  **р**   |  **с**   |  **т**   |
|     n     |     p     |    r     |    s     |    t     |
|   **ф**   |   **х**   |  **ц**   |  **ч**   |  **ш**   |
|     f     |   h/kh    |    c     |    ch    |    sh    |
|   **щ**   |   **ъ**   |  **ь**   |  **дж**  |          |
| scjh(şch) |  None/qq  |  j/jqq   | dzh(dž)  |          |


|              | Правило транслита / правило латиницы                                                                                                                     | Кириллица/Транслит/Латиница                                                                                                                                                                                                          |
|:------------:|:-------------------------------------------------------------------------------------------------------------------------------------------------------- |:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
|    **ъи**    | **yi** (**ъи** после согласных в словарных словах-исключениях, когда и йотируется)                                                                       | объимать/obyimatj, обйимать/obyimatjw/obyimatjꞌ, обйимоть/obyimotj, объимоть/obqqimotj/obqqimotj, объйимать/obqqyimatj (здесь логика модификации с помощью w/h изменена только для словарных слов-исключений)                        |
|    **ъ**     | None (после согласных перед **яёюе**), **qq** (иначе)                                                                                                    | изъян/izyan, объект/obyekt, объизвестить/obqqizvestitj, Йонъин/Yonqqinw/Yonqqinꞌ, Сёркйосен/Sjorkyosenw/Sjorkyosenꞌ, онъ/onqq, Муъминат/Muqqminat, Чанъань/Chanqqanj, нъын/nqqwyn/nqqꞌyn                                             |
|    **ьо**    | **jyo...w** / **jyo...ꞌ** (**jyo...h** / **jŷo**) (**ьо** когда они **йотируются**, а это почти всегда)                                                  | бульон/buljyonw/buljyonꞌ, бульонъён/buljyohnyon/buljŷonyon, сеньор/senjyorw/senjyorꞌ, лосьон/losjyonw/losjyonꞌ, лосьйон/losjyonww/losjyonꞌꞌ (здесь **специально для ьо** изменена логика модификации с помощью w/h)                  |
|    **ьи**    | **jyi** (**ьи** когда они **йотируются**, а это почти всегда)                                                                                            | ладьи/ladjyi, платьице/platjyice ладьйи/ladjyiw/ladjyiꞌ (здесь **специально для ьи** изменена логика модификации с помощью w/h)                                                                                                      |
|  **ь[ауэ]**  | **jy[aue]...w** / **jy[aue]...ꞌ** (**jy[aue]...h** / **jŷ[aue]**) (гласные **ауэ** после **ь** в словарных словах-исключениях, когда они **йотируются**) | бельэтаж/beljyetazhw/beljyetazhꞌ, бельйэтаж/beljyetazhww/beljyetazhꞌꞌ, бельэт/beljqqet (здесь логика модификации с помощью w/h изменена только для словарных слов-исключений)                                                        |
|    **ь**     | **jqq** (перед гласными **аоуэиы** когда они **не** йотируются), **j** (иначе)                                                                           | грабьармия/grabjqqarmiya, костьутиль/kostjqqutilj, пьеса/pjyesa пьян/pjyan, прячься/prjachjsja, мыться/mytjsja, конь/konj, ньын/njqqwyn/njqqꞌyn                                                                                      |
| **й[аоуэ]**  | **y[aoue]...w** / **y[aoue]...ꞌ** (**y[aoue]...h** / **ŷ[aoue]**) (гласные **аоуэ** после й)                                                             | йод/yodw/yodꞌ, йэс/yesw/yesꞌ, ёдйод/yodyohd/yodŷod, ёдйойс/yodyoyhs/yodŷoys, ёдйойэ/yodyohyeh/yodŷoŷe, ёдйойе/yodyoyhye/yodŷoyye, ёдйоы/yodyohwy/yodŷoꞌy, ёдйоэ/yodyohwe/yodŷoe, ёдйоя/yodyohya/yodŷoya                              |
|    **й**     | **y** (остальные простые случаи), **yii** / **ŷ** (сложные случаи)                                                                                       | красный/krasnyy, аллилуйя/alliluyya, Байес/Bayyes, ныйя/nyyya, йиппи/yippi, сйс/syiis/sŷs, сйиис/syiwis/syiꞌis, сьйс/sjyiis/sjŷs, сьйиис/sjyiwisw/sjyiꞌisꞌ, сьиис/sjyiwis/sjyiꞌis                                                    |
|    **ы**     | **y** (после согласных), **wy** / **ꞌy** (иначе)                                                                                                         | пыл/pyl, пыхтел/pyhtel, мы/my, красный/krasnyy, Нарва-Йыэсуу/Narva-Ywywesuu/Narva-Yꞌyꞌesuu, Шайыр/Shaywyr/Shayꞌyr                                                                                                                    |
| **ы[аоуэи]** | **yw[aouei]** / **yꞌ[aouei]** (гласные **аоуэи** после ы)                                                                                                | выход/vyhod, выигрывать/vywigryvatj/vyꞌigryvatj, выучить/vywuchitj/vyꞌuchitj, выострить/vywostritj/vyꞌostritj                                                                                                                        |
|    **е**     | **е** (после согласных или в словарных словах-исключениях когда е читается как э), **ye** (иначе)                                                        | мера/mera, еда/yeda, если/yesli, заезд/zayezd, Байес/Bayyes, заем/zayem, заём/zayom, траектория/trayektoriya, проект/proekt, проэкт/prowekt/pro'ekt, проэк/proek/proek (проект - словарное исключение с особым правилом отображения) |
|    **э**     | **we** / **ꞌe** (после согласных), **е** (иначе)                                                                                                         | мэр/mwer/mꞌer, этот/etot, аэроплан/aeroplan, поэт/poet, эротика/erotika, йэс/yesw/yesꞌ                                                                                                                                               |
|  **[яёю]**   | **j[aou]** (после согласных), **y[aou]** (иначе)                                                                                                         | синяя/sinjaya, мёд/mjod, ёлка/yolka, пюре/pjure, якорь/yakorj                                                                                                                                                                        |
|    **х**     | **kh** (когда есть неоднозначность из-за других диграфов и триграфов с h), **h** (иначе)                                                                 | сход/skhod, кхе/kkhe, сикх/sikkh, шхуна/shkhuna, чхать/chkhatj, отход/otkhod, хахх/hahh, хохолок/hoholok, выход/vyhod, меха/meha, эхо/eho, вече/veche, меча/mecha, сцьха/scjkha, нцьхи/ncjhi                                         |

Из таблицы выше видно, что для ь и ъ (особенно ъи и ьэ) придется определять отображение по умолчанию и запомненные в словарь исключения из него. Так, стоит ожидать, что ъи и ьэ по умолчанию должны быть не йотированными, но известны и йотированные исключения.

|             | Ещё примеры                           |
| ----------- | ------------------------------------- |
| дж/dzh(dž)  | Джордж/Dzhordzh/Džordž                |
| щ/scjh(şch) | щётка/scjhjotka/şchjotka, счёт/schjot |
| ж/zh        | ёж/yozh, возжи/vozzhi, позже/pozzhe   |
| ч/ch        | Черныш/Chernysh, счётная/schjotnaya   |
| ш/sh        | шлем/shlem                            |
| ё/jo/yo     | мёд/mjod, ёмко/yomko                  |
| ю/ju/yu     | мюсли/mjusli, Юля/Yulja               |
| я/ja/ya     | Изя/Izja, Якорь/Yakorj, баян/bayan    |

Многие буквы совпадают с [ГОСТ 16876-71 табл. 2](https://ru.wikipedia.org/wiki/%D0%A2%D1%80%D0%B0%D0%BD%D1%81%D0%BB%D0%B8%D1%82%D0%B5%D1%80%D0%B0%D1%86%D0%B8%D1%8F_%D1%80%D1%83%D1%81%D1%81%D0%BA%D0%BE%D0%B3%D0%BE_%D0%B0%D0%BB%D1%84%D0%B0%D0%B2%D0%B8%D1%82%D0%B0_%D0%BB%D0%B0%D1%82%D0%B8%D0%BD%D0%B8%D1%86%D0%B5%D0%B9#%D0%A1%D1%80%D0%B0%D0%B2%D0%BD%D0%B8%D1%82%D0%B5%D0%BB%D1%8C%D0%BD%D0%B0%D1%8F_%D1%82%D0%B0%D0%B1%D0%BB%D0%B8%D1%86%D0%B0_%D1%81%D0%B8%D1%81%D1%82%D0%B5%D0%BC_%D1%82%D1%80%D0%B0%D0%BD%D1%81%D0%BB%D0%B8%D1%82%D0%B5%D1%80%D0%B0%D1%86%D0%B8%D0%B8) или [ГОСТ 7.79-2000 сист. Б](https://ru.wikipedia.org/wiki/%D0%A2%D1%80%D0%B0%D0%BD%D1%81%D0%BB%D0%B8%D1%82%D0%B5%D1%80%D0%B0%D1%86%D0%B8%D1%8F_%D1%80%D1%83%D1%81%D1%81%D0%BA%D0%BE%D0%B3%D0%BE_%D0%B0%D0%BB%D1%84%D0%B0%D0%B2%D0%B8%D1%82%D0%B0_%D0%BB%D0%B0%D1%82%D0%B8%D0%BD%D0%B8%D1%86%D0%B5%D0%B9#%D0%A1%D1%80%D0%B0%D0%B2%D0%BD%D0%B8%D1%82%D0%B5%D0%BB%D1%8C%D0%BD%D0%B0%D1%8F_%D1%82%D0%B0%D0%B1%D0%BB%D0%B8%D1%86%D0%B0_%D1%81%D0%B8%D1%81%D1%82%D0%B5%D0%BC_%D1%82%D1%80%D0%B0%D0%BD%D1%81%D0%BB%D0%B8%D1%82%D0%B5%D1%80%D0%B0%D1%86%D0%B8%D0%B8).

Алфавит транслитерации использует все буквы английского алфавита кроме Xx. Алфавит латиницы не использует Ww, Xx и дополнительно использует 14 новых букв (см. ниже).

***Слово на латинице является грамматически верным если:***

1. его образ от прообраза совпадает с самим словом (`lat_word == RUtoEN(ENtoRU(lat_word))`),
2. его прообраз грамматически верен (`ENtoRU(lat_word)`).

Для обратимых аббревиатур, выглядящих прилично и совместимых с чтением по-русски придётся расширять алфавит. Буквы, уже используемые в латинице, помечены скобками. Остальные - используются только в аббревиатурах:

| **я** | **е** | **ё** | **ю** | **э** | **ы** | **w** |
|:-----:|:-----:|:-----:|:-----:|:-----:|:-----:|:-----:|
|  Ââ   |  Êê   |  Ôô   |  Ûû   |  Èè   |  Ỳỳ   | [Ꞌꞌ]  |
| **щ** | **ж** | **ч** | **ш** | **х** | **й** |       |
| [Şş]  | [Žž]  |  Čč   |  Šš   |  Ĥĥ   | [Ŷŷ]  |       |

Ъ, Ь: QQ, J/JQQ. В словах в верхнем регистре Щ пишется просто как Ş, без CH.

Примеры аббревиатур: ГЭС/GÈS, АЭС/AES, ЖКХ/ŽKĤ, ЖЭК/ŽÈK, ЕС/ÊS, США/SŠA, МЧС/MČS, ЮАР/ÛAR, ЭЭГ/EEG, ЕГЭ/ÊGÈ, микрорайон Щ/mikrorayonw Ş/mikrorayonꞌ Ş. То есть специально для аббревиатур, когда после ş идет диграф ch - он считается частью щ. А когда идет č, то считается уже отдельной буквой.

**Слова в верхнем регистре считаются аббревиатурами и пишутся по своим лаконичным правилам.** Это может ухудшать чтение текста, набранного капсом (после конверсии в латиницу). Но его и так трудно читать, так что не жалко.


## Раскладка клавиатуры для латиницы

Основная раскладка. Добавляет новые буквы, встречающиеся более менее часто: Şş(для Щ), Žž(для ДЖ), Ꞌꞌ(W).

| Ꞌꞌ(\`~) | 1!  | 2“(@) | 3”(#) | 4[($) | 5](%) | 6^  | 7&  | 8\* | 9(  | 0)  |   -\_   |    =+     |
|:-------:|:---:|:-----:|:-----:|:-----:|:-----:|:---:|:---:|:---:|:---:|:---:|:-------:|:---------:|
|         | Qq  |  Ww   |  Ee   |  Rr   |  Tt   | Yy  | Uu  | Ii  | Oo  | Pp  | Şş([{)  |  Žž(]})   |
|         | Aa  |  Ss   |  Dd   |  Ff   |  Gg   | Hh  | Jj  | Kk  | Ll  | ;:  | '\`('") | \\#(\\\|) |
|         |     |  Zz   |  Xx   |  Cc   |  Vv   | Bb  | Nn  | Mm  | ,<  | .>  |   /?    |           |

Дополнительная раскладка. Ещё буквы для аббревиатур и очень редких альтернативных йотирований: Ââ(Я), Êê(Е), Ôô(Ё), Ûû(Ю), Èè(Э), Čč(Ч), Šš(Ш), Ĥĥ(Х), Ŷŷ(Йй), Ỳỳ(Ыы).

| Ꞌꞌ  |   1!   |   2“   |   3”   |   4[   | 5]  |   6^   |   7&   | 8\* |   9(   | 0)  | -\_ | =+  |
|:---:|:------:|:------:|:------:|:------:|:---:|:------:|:------:|:---:|:------:|:---:|:---:|:---:|
|     |   Qq   |   Ww   | **Êê** |   Rr   | Tt  | **Ỳỳ** | **Ûû** | Ii  | **Ôô** | Pp  | Şş  | Žž  |
|     | **Ââ** | **Šš** |   Dd   |   Ff   | Gg  | **Ĥĥ** | **Ŷŷ** | Kk  |   Ll   | ;:  | '\` | \\# |
|     |        | **Žž** | **Èè** | **Čč** | Vv  |   Bb   |   Nn   | Mm  |   ,<   | .>  | /?  |     |


## Транслитерация транслита в английский язык

* qq просто убирается,
* w после "y" и перед гласной [aoueyi] => h, в остальных случаях просто убирается,
* j перед гласной [aoue] => i, в остальных случаях просто убирается.


## Пример текста транслитом

*По-моему, это вариант гораздо лучше подходит для русско-английских билингвов, чем варианты с большим количеством диакритических знаков. В английском нет диакритики, в русском - почти нет (ё ставят только при опасности неправильного прочтения, й трудно считать диакритикой). Так что не удивительно, что диакритика будет вызывать отторжение. В варианте минималистичной диакритики она ставится тоже в очень малом числе случаев.*

Piony i pionjata vsjo yescjhjo rastut na poljane vozle derevni Pjony.

Pjyanyy master po proektu sdelal mehanicheskiy obyekt s izyanom. Yesli brak ne obnaruzhitsja, to belyye bolidy boljshe ne smogut vywigryvatj gonki.

V pjyese pro devushku v zeljonom platjyice vse sadilisj na ladjyi i plyli po reke. No tut iz lesa vyshel Dzhordzh Maksimus, konj v paljto i rvanyh dzhinsah, kotoryy chto-to vywiskival, i prikazal vsem mytjsja i gotovitj buljyonw. Znachit snova pjyom do lysyh akvalangistov.

ГЭС/GwES, АЭС/AES, ЖКХ/ZhKkH, ЖЭК/ZhwEK, ЕС/yES, США/SShA, МЧС/MChS, ЮАР/yUAR, ЭЭГ/EEG, ЕГЭ/yEGwE, микрорайон Щ/mikrorayonw SCjh.

Prepodobnyy Bayyes podkinul igraljnyye kosti. Vypalo shestj, znachit yemu pridjotsja mazatj yodw na ranu.

Mwer neboljshogo gorodishki otkryl tablicu ekselja i vozmutilsja cenoy novogo ekskavatora. Azh ekzema snova stala yego bespokoitj. Oh uzh eta pokupka vechnogo dvigatelja v proshlom godu! A tak zhe pokupka aeroplana-ekranoljota. Yesli tak poydjot i daljshe, to bjudzhetu pridjotsja hudo.

V etom vide fraza ot A to Ya nachinayet vygljadetj sovsem po-drugomu. Seychas scjhjotka novaya, no pozzhe ona stanet staraya. Chernysh ljubit kogda yego cheshut yeyu. Yozh koljuchiy i pohozh na neyo.

Skhod mestnyh zhiteley indiyskoy derevni sikkhov reshal chto zhe delatj s otkhodami kompanii "Kaligula Gay Yuliy Cezarj" (lat. /Caligula Gaius Iulius Caesar/ ). Odin iz prisutstvuyuscjhih nosil hoholok na golove. On i nashjol vyhod iz situacii.

"Kto s mechom k nam pridjot, tot ot mecha i..." - ne smog dogovoritj starshiy mehanik Vasiliy.

Imeyetsja neskoljko gipotez proiskhozhdeniya sobaki, naiboleye veroyatnymi yeyo predkami schitayutsja volk i nekotoryye vidy shakalov.

V suzhdeniyah uchjonyh o predkah domashney sobaki prisutstvuyut dve tochki zreniya. Odni schitayut, chto sobaki - polifileticheskaya gruppa (proiskhodjascjhaya ot neskoljkih predkov), drugiye priderzhivayutsja mneniya, chto vse sobaki proizoshli ot odnogo predka (monofileticheskaya teoriya).


## Пример текста латиницей

Piony i pionjata vsjo yeşchjo rastut na poljane vozle derevni Pjony.

Pjyanyy master po proektu sdelal mehanicheskiy obyekt s izyanom. Yesli brak ne obnaruzhitsja, to belyye bolidy boljshe ne smogut vyꞌigryvatj gonki.

V pjyese pro devushku v zeljonom platjyice vse sadilisj na ladjyi i plyli po reke. No tut iz lesa vyshel Džordž Maksimus, konj v paljto i rvanyh džinsah, kotoryy chto-to vyꞌiskival, i prikazal vsem mytjsja i gotovitj buljyonꞌ. Znachit snova pjyom do lysyh akvalangistov.

ГЭС/GÈS, АЭС/AES, ЖКХ/ŽKĤ, ЖЭК/ŽÈK, ЕС/ÊS, США/SŠA, МЧС/MČS, ЮАР/ÛAR, ЭЭГ/EEG, ЕГЭ/ÊGÈ, микрорайон Щ/mikrorayonꞌ Ş.

Prepodobnyy Bayyes podkinul igraljnyye kosti. Vypalo shestj, znachit yemu pridjotsja mazatj yodꞌ na ranu.

Mꞌer neboljshogo gorodishki otkryl tablicu ekselja i vozmutilsja cenoy novogo ekskavatora. Azh ekzema snova stala yego bespokoitj. Oh uzh eta pokupka vechnogo dvigatelja v proshlom godu! A tak zhe pokupka aeroplana-ekranoljota. Yesli tak poydjot i daljshe, to bjudžetu pridjotsja hudo.

V etom vide fraza ot A to Ya nachinayet vygljadetj sovsem po-drugomu. Seychas şchjotka novaya, no pozzhe ona stanet staraya. Chernysh ljubit kogda yego cheshut yeyu. Yozh koljuchiy i pohozh na neyo.

Skhod mestnyh zhiteley indiyskoy derevni sikkhov reshal chto zhe delatj s otkhodami kompanii “Kaligula Gay Yuliy Cezarj” (lat. /Caligula Gaius Iulius Caesar/ ). Odin iz prisutstvuyuşchih nosil hoholok na golove. On i nashjol vyhod iz situacii.

“Kto s mechom k nam pridjot, tot ot mecha i...” - ne smog dogovoritj starshiy mehanik Vasiliy.

Imeyetsja neskoljko gipotez proiskhozhdeniya sobaki, naiboleye veroyatnymi yeyo predkami schitayutsja volk i nekotoryye vidy shakalov.

V suzhdeniyah uchjonyh o predkah domashney sobaki prisutstvuyut dve tochki zreniya. Odni schitayut, chto sobaki - polifileticheskaya gruppa (proiskhodjaşchaya ot neskoljkih predkov), drugiye priderzhivayutsja mneniya, chto vse sobaki proizoshli ot odnogo predka (monofileticheskaya teoriya).


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
