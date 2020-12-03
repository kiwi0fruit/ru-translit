# ru-translit (kiwi0fruit's)

### Uniquely reversible Russian to English transliteration/romanization: no extra letters, two versions - with and without non-letters (russkaja latinica)

### Однозначно обратимая транслитерация/романизация из русского в английский алфавит: без дополнительных букв, две версии - с небуквенными знаками и без (русская латиница)

Содержание:

* [Четыре разные "И" русской латиницы от которых всё зависит](#%D1%87%D0%B5%D1%82%D1%8B%D1%80%D0%B5-%D1%80%D0%B0%D0%B7%D0%BD%D1%8B%D0%B5-%D0%B8-%D1%80%D1%83%D1%81%D1%81%D0%BA%D0%BE%D0%B9-%D0%BB%D0%B0%D1%82%D0%B8%D0%BD%D0%B8%D1%86%D1%8B-%D0%BE%D1%82-%D0%BA%D0%BE%D1%82%D0%BE%D1%80%D1%8B%D1%85-%D0%B2%D1%81%D1%91-%D0%B7%D0%B0%D0%B2%D0%B8%D1%81%D0%B8%D1%82)
* [Английская латиница](#%D0%B0%D0%BD%D0%B3%D0%BB%D0%B8%D0%B9%D1%81%D0%BA%D0%B0%D1%8F-%D0%BB%D0%B0%D1%82%D0%B8%D0%BD%D0%B8%D1%86%D0%B0)
* [Аббревиатуры английской латиницы](#%D0%B0%D0%B1%D0%B1%D1%80%D0%B5%D0%B2%D0%B8%D0%B0%D1%82%D1%83%D1%80%D1%8B-%D0%B0%D0%BD%D0%B3%D0%BB%D0%B8%D0%B9%D1%81%D0%BA%D0%BE%D0%B9-%D0%BB%D0%B0%D1%82%D0%B8%D0%BD%D0%B8%D1%86%D1%8B)
* [Совлат-англотранс латиница с диакритикой](#%D1%81%D0%BE%D0%B2%D0%BB%D0%B0%D1%82-%D0%B0%D0%BD%D0%B3%D0%BB%D0%BE%D1%82%D1%80%D0%B0%D0%BD%D1%81-%D0%BB%D0%B0%D1%82%D0%B8%D0%BD%D0%B8%D1%86%D0%B0-%D1%81-%D0%B4%D0%B8%D0%B0%D0%BA%D1%80%D0%B8%D1%82%D0%B8%D0%BA%D0%BE%D0%B9)
* [Аббревиатуры совлат-англотранс латиницы](#%D0%B0%D0%B1%D0%B1%D1%80%D0%B5%D0%B2%D0%B8%D0%B0%D1%82%D1%83%D1%80%D1%8B-%D1%81%D0%BE%D0%B2%D0%BB%D0%B0%D1%82-%D0%B0%D0%BD%D0%B3%D0%BB%D0%BE%D1%82%D1%80%D0%B0%D0%BD%D1%81-%D0%BB%D0%B0%D1%82%D0%B8%D0%BD%D0%B8%D1%86%D1%8B)
* [Примеры интересных случаев](#%D0%BF%D1%80%D0%B8%D0%BC%D0%B5%D1%80%D1%8B-%D0%B8%D0%BD%D1%82%D0%B5%D1%80%D0%B5%D1%81%D0%BD%D1%8B%D1%85-%D1%81%D0%BB%D1%83%D1%87%D0%B0%D0%B5%D0%B2)
* [Пример текста английской латиницы](#%D0%BF%D1%80%D0%B8%D0%BC%D0%B5%D1%80-%D1%82%D0%B5%D0%BA%D1%81%D1%82%D0%B0-%D0%B0%D0%BD%D0%B3%D0%BB%D0%B8%D0%B9%D1%81%D0%BA%D0%BE%D0%B9-%D0%BB%D0%B0%D1%82%D0%B8%D0%BD%D0%B8%D1%86%D1%8B)
* [Пример текста совлат-англотранс латиницы](#%D0%BF%D1%80%D0%B8%D0%BC%D0%B5%D1%80-%D1%82%D0%B5%D0%BA%D1%81%D1%82%D0%B0-%D1%81%D0%BE%D0%B2%D0%BB%D0%B0%D1%82-%D0%B0%D0%BD%D0%B3%D0%BB%D0%BE%D1%82%D1%80%D0%B0%D0%BD%D1%81-%D0%BB%D0%B0%D1%82%D0%B8%D0%BD%D0%B8%D1%86%D1%8B)

Придумал в качестве развлечения ещё один транслит.

Развлечением было удовлетворить ограничениям:

* Транслит - полностью обратимый (является кодировкой без потерь и позволяет точно восстановить произвольный русский текст из латиницы). То есть, это [**инъективное отображение**](https://ru.wikipedia.org/wiki/%D0%98%D0%BD%D1%8A%D0%B5%D0%BA%D1%86%D0%B8%D1%8F_(%D0%BC%D0%B0%D1%82%D0%B5%D0%BC%D0%B0%D1%82%D0%B8%D0%BA%D0%B0)),
* Транслит содержит только буквы (в частности, не использует апостроф): отображение из русских букв `[А-Яа-я]` в английские `[A-Za-z]` без добавлений,
* Не содержит далёких фонетических замен типа щ → w. Желательно, чтобы "звучало" похоже на английский или математический латинский.


## Четыре разные "И" русской латиницы от которых всё зависит

Придумывая латиницы с не более, чем четырьмя новыми буквами, обнаружил, что все отлично срастается после задания трёх разных "И":

* йотирующая и — **й** (включая спрятанную в еёюя и редко даже в ьи и ьо),
* смягчающая и — **ь** (включая спрятанную в еёюя и даже в и),
* ы — **ы**,
* собственно, и — **и**.

Но в базовой латинице букв со смыслом "и" всего три: i, j (диакритический вариант i), y ("и" греческая). А нужно 4. Поэтому, получаются компромиссы.


## Английская латиница

Основные идеи внутренней грамматики **транслита без диакритики**:

* йотирующая, но не смягчающая, "и" (йот; еёюя НЕ после согласных) — **j** (яма/jama, съезд/sjezd, пьеса/pjjesa, ладьи/ladjji), 
* смягчающая, но не йотирующая, "и" (ь; ёюя после согласных) — **i** после согласных перед aouy, иначе - **j**, но йотирование имеет приоритет (мёд/miod, пьеса/pjjesa, конь/konj, пион/piyon),
* "ы" — **y** (мы/my),
* собственно, "и" — **iy** после согласных перед aou, иначе - **i** (мир/mir, лён/lion, пион/piyon, Сиэтл/Sietl).
* **e** после согласных всегда смягчает, можно опустить i (пень/penj). В остальных случаях **e** обозначает звук э (это/eto, поэт/poet). Йотировать надо для "е" не после согласных (уезд/ujezd).
* Убрать смягчение **для э** после согласной можно с помощью **ye** (мэр/myer, сэр/syer). Убрать такое поведение можно с помощью **yy** (сыэ/syye).
* Таким образом, смягчение с момощью "i" и твёрдость с помощью "y" комплементарны. Для каждой буквы из "aoue" после согласных работает либо смягчение, либо твердость - но никогда и то, и другое.

Дополнительно:

* **qq** обозначает паузу, гортанную смычку или просто игнорируемый диграф, в редких случаях даже может значить йотацию вопреки всей логике - зависит от слова (объизвестить/obqqizvestitj, грабьармия/grabjqqarmija).
* х обозначется **h/kh** (ход/hod, сход/skhod).
* слова на латинице из других языков можно писать, экранируя с помощью " /" и "/ " (или `\w[(]?/` и `/[,.?;!)']?\w`).
* разные способы написания звука /щ/ (щ и сч) передаются с помощью **sc**. Разные виды йотирования (е,ё,ю,я vs. йэ,йо,йу,йа, ьё vs. ьо, и т.п.) так же передаются только с помощью **jo,je,ju,ja**. Обратное отображение в кириллицу осуществляется с помощью "умного" алгоритма, который, в том числе, использует словарь. Для новых слов, альтернативных написаний и слов, отсутствующих в словаре, используется переключатель **w**. Если прообраз слова должен содержать только е,ё,ю,я,щ, то в конце слова ставится w. Если же слово в каком-то месте должно содержать йэ,йо,йу,йа,сч, то w ставится явно префиксом **wjo,wje,wju,wja,wsc** (счёт/sciot, счет/scet, щётка/sciotka, считаются/scitajutsia, считающейся/scitajucsejsia, йод/jod, ёж/jozh, ёдъёд/jodjodw, ёдйод/jodwjod, йоща/wjosca).
* иногда **w** еще используется как патч для проблем, возникающих из-за словарных исключений (проект/proekt, проэкт/prowekt).

|   **a**   |   **о**   |  **у**   |  **э**   |  **ы**   |
|:---------:|:---------:|:--------:|:--------:|:--------:|
|     a     |     o     |    u     |   e/ye   |    y     |
|   **я**   |   **ё**   |  **ю**   |  **е**   |  **и**   |
|   ja/ia   |   jo/io   |  ju/iu   |   je/e   |   i/iy   |
|   **б**   |   **в**   |  **г**   |  **д**   |  **ж**   |
|     b     |     v     |    g     |    d     |    zh    |
|   **з**   |   **й**   |  **к**   |  **л**   |  **м**   |
|     z     |   j/wj    |    k     |    l     |    m     |
|   **н**   |   **п**   |  **р**   |  **с**   |  **т**   |
|     n     |     p     |    r     |    s     |    t     |
|   **ф**   |   **х**   |  **ц**   |  **ч**   |  **ш**   |
|     f     |   h/kh    |   cz     |    c     |    sh    |
|   **щ**   |   **ъ**   |  **ь**   |  **сч**  | **чз, чж** |
|  sc/wsc   |  None/qq  |   j/jqq  |  sc/wsc  | chz, chzh  |

Алфавит транслитерации использует все буквы английского алфавита кроме Xx.

***Слово на латинице является грамматически верным если:***

1. его образ от прообраза совпадает с самим словом (`lat_word == CyrToLat(LatToCyr(lat_word))`),
2. его прообраз грамматически верен (`LatToCyr(lat_word)`).


## Аббревиатуры английской латиницы

Все слова в верхнем регистре считаются аббревиатурами и записываются по специальным правилам. Vодифицирующая буква диграфа пишется в нижнем регистре, а модифицируемая буква - в верхнем.

ГЭС/GyES, АЭС/AES, ЖКХ/ZhkKH, ЖЭК/ZhyEK, ЕС/jES, США/SShA, МЧС/MCS, ЮАР/jUAR, ЭЭГ/EEG, ЕГЭ/jEGyE, микрорайон Щ/mikrorajon SC, СЧК/wSCK, ЩК/SCK, ЛЁН/LiON, ЛИОН/LIyON.

ИОН/ION, ЛИЁН/LIjON, ЙОД/wJOD, йод/jod, ЙЁД/JjOD, ЁД/jOD, ёд/jodw, НЫЭ/NYyE, НЫЕ/NYjE, НЙ/NwJ, ЧЗ/ChZ, ЦЗ/CzZ, ЦРУ/CzRU.

Аббревиатур с Ь и Ъ не должно быть, поэтому в них даже W не заменяется: ЛЪЁН/LJON, ЛЬОН/LJWJON, ЛЬЁН/LJJON, ЛЬЙОН/LJQQWJON

**Слова в верхнем регистре считаются аббревиатурами и пишутся по своим лаконичным правилам.** Это может ухудшать чтение текста, набранного капсом (после конверсии в латиницу). Но его и так трудно читать, так что не жалко. Не бывает словарных аббревиатур - все аббревиатуры (слова капсом) используют одни и те же стандарты (обратите внимание на йод и ёд выше).

Cлова на латинице в верхнем регистре, чтобы они не считались аббревиатурами можно писать, экранируя с помощью " \\" и "\ " (или `\w[(]?\\` и `\\[,.?;!)']?\w`).

Vsem \ZHIVO\ sobratjsia!

Но другие способы выделения все равно предпочтительнее:

Vsem *zhivo* sobratjsia!


## Совлат-англотранс латиница с диакритикой

Отличия от Английской латиницы 25:

* после согласных sia => sà, sio => sò, siu => sù (я,ё,ю), мягкий знак sj => sì, qj => ì (смягчающие, но не йотирующие буквы),
* siy => sį (и),
* sye => sę (э),
* wj => ĵ (й),
* wsc => sĉ (сч),
* w в конце слова => ꞌ,
* qq не в конце слова => ꞌ, qq в конце слова => qq (ъ,ь),
* dzh => dž (дж), zhzh => žž (жж), chzh => cž (чж),
* cz => ç (ц),
* добавлены новые буквы Àà, Òò, Ùù, Ìì, Įį, Ęę, Çç, Ĉĉ, Ĵĵ, Žž, Ꞌꞌ и убраны Xx, Ww, Qq,
* отличия аббревиатур описаны отдельно (ещё новые буквы: Èè, Šš, Ĥĥ),
* ударения: sà => sǎ, sò => sǒ, sù => sǔ, se => sě (je => jé), sę => sé, i => í, a => á, o => ó, u => ú, y => ý (iy => iý, į => í) (ещё новые буквы: Ǎǎ, Ǒǒ, Ǔǔ, Ěě, Íí, Éé, Áá, Óó, Úú, Ýý).

|   **a**   |   **о**   |  **у**   |  **э**   |  **ы**   |
|:---------:|:---------:|:--------:|:--------:|:--------:|
|     a     |     o     |    u     |   e/ę    |    y     |
|   **я**   |   **ё**   |  **ю**   |  **е**   |  **и**   |
|   ja/à    |   jo/ò    |  ju/ù    |   je/e   |   i/į    |
|   **б**   |   **в**   |  **г**   |  **д**   |  **ж**   |
|     b     |     v     |    g     |    d     |    zh    |
|   **з**   |   **й**   |  **к**   |  **л**   |  **м**   |
|     z     |    j/ĵ    |    k     |    l     |    m     |
|   **н**   |   **п**   |  **р**   |  **с**   |  **т**   |
|     n     |     p     |    r     |    s     |    t     |
|   **ф**   |   **х**   |  **ц**   |  **ч**   |  **ш**   |
|     f     |   h/kh    |    ç     |    c     |    sh    |
| **щ** |   **ъ**   | **ь** | **сч** | **чз, чж, дж, жж** |
|   sc  | None/ꞌ/qq |  ì/ìꞌ | sc/sĉ  |  chz, cž, dž, žž   |


## Аббревиатуры совлат-англотранс латиницы

ГЭС/GĘS, АЭС/AES, ЖКХ/ŽKĤ, ЖЭК/ŽĘK, ЕС/ÈS, США/SŠA, МЧС/MCS, ЮАР/ÙAR, ЭЭГ/EEG, ЕГЭ/ÈGĘ, микрорайон Щ/mikrorajon SC, СЧК/SĈK, ЩК/SCK, ЛЁН/LÒN, ЛИОН/LĮON.

ИОН/ION, ЛИЁН/LIÒN, ЙОД/ĴOD, йод/jod, ЙЁД/JÒD, ЁД/ÒD, ёд/jodꞌ, НЫЭ/NYĘ, НЫЕ/NYÈ, НЙ/NĴ, ЧЗ/ĈZ, ЦЗ/ÇZ, ЦРУ/ÇRU.

Аббревиатур с Ь и Ъ не должно быть: ЛЪЁН/LJON, ЛЬОН/LÌĴON, ЛЬЁН/LÌJON, ЛЬЙОН/LÌꞋĴON


## Примеры интересных случаев

лён/lion/lòn  
Лион/Liyon/Lįon  
пион/piyon/pįon  
пиы/piyy/pįy  
мэр/myer/męr  
ыэр/yer  
мыэр/myyer/myęr  
этот/etot  
если/jesli  
конь/konj/konì  
кони/koni  
Юля/Julia/Julà  
Юлия/Julija  
Юлиан/Juliyan/Julįan  
пьяный/pjjanyj/pìjanyj  
подъезд/podjezd  
пьеса/pjjesa/pìjesa  
пйеса/pwjjesa/pĵjesa  
паьеса/paqjjesa/paìjesa  
паьаса/paqjqqasa/paìꞌasa  
пайъеса/pajqqjesa/pajꞌjesa  
ёж/jozh  
йож/wjozh/ĵozh  
йод/jod  
ёд/jodw/jodꞌ   
ёдйод/jodwjoh/jodĵod  
аллилуйя/allilujja  
ладьи/ladjji/ladìji  
Таунйин/Taunjin  
Пиньиу/Pinjjiu/Pinìjiu  
Таунйиан/Taunjian  
Тарвасйыги/Tarvasjygi  
баньтьынг/banjtjqqyng/banìtìꞌyng  
сьйы/sjjy/sìjy  
пьём/pjjom/pìjom  
бульон/buljjon/bulìjon  
выучить/vyucitj/vyucitì  
выострить/vyostritj/vyostritì  
выигрывать/vyigryvatj/vyigryvatì  
объимать/obqqimatj/obꞌimatì  
объизвестить/obqqizvestitj/obꞌizvestitì  
бельэтаж/beljqqetazh/belìjetazh  
грабьармия/grabjqqarmija/grabìꞌarmija  

|              | Правило транслита / правило латиницы                                                                                                                     | Кириллица/Транслит/Латиница                                                                                                                                                                                                          |
|:------------:|:-------------------------------------------------------------------------------------------------------------------------------------------------------- |:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
|    **ъ**     | None (после согласных перед **яёюе**), **qq/ꞌ** (иначе, не в конце слова), **qq** (в конце слова)                                                                                                    | изъян/izjan, объект/objekt, объимать/obqqimatj/obꞌimatì, объизвестить/obqqizvestitj/obꞌizvestitì, Йонъин/Jonqqin/Jonꞌin, Сёркйосен/Siorkjosen, ёркйосен/jorkwjosen/jorkĵosen, онъ/onqq/onqq, Муъминат/Muqqminat/Muꞌminat, Чанъань/Canqqanj/Canꞌanì, нъын/nqqyn/nꞌyn                                             |
|    **ьо**    | **jjo/ìjo**                                                  | бульон/buljjon/bulìjon, бульонъён/buljwjonjon/bulìĵonjon, сеньор/senjjor/senìjor, лосьон/losjjon/losìjon, лосьён/losjqqjon/losìꞌjon, лосьйон/losjwjon/losìĵon, осьён/osjjon/osìjon, осьон/osjwjon/osìĵon, осьйон/osjqqwjon/osìꞌĵon (здесь **специально для словарных слов с ьо** изменена логика модификации с помощью w - важно какой вариант, ьё или ьо, является ходовым для данного слова)                  |
|    **ьи**    | **jji/ìji**                                                                                            | ладьи/ladjji/ladìji, платьице/platjjicze/platìjiçe, Вильйинг/Viljqqjing/Vilìꞌjing                                                                                                      |
|    **ь**     | **jqq/ìꞌ** (перед гласными **ауэы** и буквами **йьъ**), **j/ì** (иначе)                                                                           | бельэтаж/beljjetazh/belìjetazh, бельетаж/beljqqjetazh/belìꞌjetazh, бельйэтаж/beljwjetazh/belìĵetazh, ельэтаж/eljqqetazh/elìꞌetazh, ельетаж/eljjetazh/elìjetazh, ельйэтаж/eljwjetazh/elìĵetazh, грабьармия/grabjqqarmija/grabìꞌarmija, костьутиль/kostjqqutilj/kostìꞌutilì, пьеса/pjjesa/pìjesa пьян/pjjan/pìjan, прячься/priacjsia/pràcìsà, мыться/mytjsia/mytìsà, конь/konj/konì, ньын/njqqyn/nìꞌyn (здесь **специально для словарного исключения бельэтаж** изменена логика модификации с помощью w)                                                                                     |
| **й[аоуэ]**  | **j[aoue]** (гласные **аоуэ** после й), **wj[aoue]/ĵ[aoue]** (альтернативная йотация)                                                             | йод/jod, ёж/jozh, йэс/wjes/ĵes, ёдйод/jodwjoh/jodĵoh                              |
|    **й**     | **j** (остальные простые случаи), **wj/ĵ** (сложные случаи)                                                                                       | красный/krasnyj, аллилуйя/allilujja, Байес/Bajjes, йиппи/jippi, сйс/swjs/sĵs                                                    |
|    **ы**     | **y**                                                                                                        | пыл/pyl, пыхтел/pyhtel, мы/my, красный/krasnyj, Нарва-Йыэсуу/Narva-Jyesuu, Шайыр/Shajyr, выход/vyhod, выигрывать/vyigryvatj/vyigryvatì, выучить/vyucitj/vyucitì, выострить/vyostritj/vyostritì                                                                                                                        |
|    **е**     | **е** (после согласных или в словарных словах-исключениях когда е читается как э), **je** (иначе)                                                        | мера/mera, еда/jeda, если/jesli, заезд/zajezd, Байес/Bajjes, заем/zajem, заём/zajom, траектория/trajektorija, проект/proekt, проэкт/prowekt/proękt, проэк/proek/proek (**проект - словарное исключение** с особым правилом отображения) |
|    **э**     | **ye/ę** (после согласных или после ы в закрытом слоге), **е** (иначе)                                                                                                         | мэр/myer/męr, этот/etot, аэроплан/aeroplan, поэт/poet, эротика/erotika, йэс/wjes/ĵes, ыэр/yer, мыэр/myyer/myęr                                                                                                                                               |
|  **[яёю]**   | **i[aou]/[àòù]** (после согласных), **j[aou]** (иначе)                                                                                                         | синяя/siniaja/sinàja, мёд/miod/mòd, ёлка/jolka, пюре/piure/pùre, якорь/jakorj/jakorì                                                                                                                                                                        |
|    **х**     | **kh** (когда есть неоднозначность из-за других диграфов и триграфов с h), **h** (иначе)                                                                 | сход/skhod, кхе/kkhe, сикх/sikkh, шхуна/shkhuna, чхать/ckhatj/ckhatì, отход/otkhod, хахх/hahh, хохолок/hoholok, выход/vyhod, меха/meha, эхо/eho, вече/vece, меча/meca                                         |

|                | Ещё примеры                                                                            |
| -------------- | -------------------------------------------------------------------------------------- |
| дж, dzh/dž     | Джордж/Dzhordzh/Džordž                                                                 |
| щ, sc          | щётка/sciotka/scòtka, ещё/jescio/jescò                                                 |
| сч, sc, wsc/sĉ | счёт/sciot/scòt, трусчёт/truwsciot/trusĉòt                                             |
| ж, zh          | ёж/jozh, возжи/vozzhi, позже/pozzhe                                                    |
| жж, zhzh/žž    | жужжать/zhuzhzhatj/zhužžatì                                                            |
| чж, сhzh/сž    | Чжань/Chzhanj/Cžanì                                                                    |
| ч, c, ch       | чесать/cesatj/cesatì, Черныш/Cernysh, счётная/sciotnaja/scòtnaja, Кирпичзев/Kirpichzev |
| ц, cz/ç        | центурион/czenturiyon/çenturįon, процессор/proczessor/proçessor, Цезарь/Czezarj/Çezarì |
| ш, sh          | шлем/shlem                                                                             |
| ё, jo, io/ò    | мёд/miod/mòd, ёмко/jomko                                                               |
| ю, ju, iu/ù    | мюсли/miusli/mùsli, Юля/Julia/Julà                                                     |
| я, ja, ia/à    | Изя/Izia/Izà, Якорь/Jakorj/Jakorì, баян/bajan                                          |


## Пример текста английской латиницы

Piyony i vasiljki vsio jescio rastut na poliane vozle derevni Piony, scitajuscejsia bogatoj.

Pjjanyj master po proektu sdelal mehaniceskij objekt s izjanom. Jesli brak ne obnaruzhitsia, to belyje bolidy boljshe ne smogut vyigryvatj gonki.

V pjjese pro devushku v zelionom platjjicze vse sadilisj na ladjji i plyli po reke. No tut iz lesa vyshel Dzhordzh Maksimus, konj v paljto i rvanyh dzhinsah, kotoryj cto-to vyiskival, i prikazal vsem mytjsia i gotovitj buljjon. Znacit snova pjjom do lysyh akvalangistov.

Prepodobnyj Bajjes podkinul igraljnyje kosti. Vypalo shestj, znacit jemu pridiotsia mazatj jod na ranu.

Myer neboljshogo gorodishki otkryl tabliczu ekselia i vozmutilsia czenoj novogo ekskavatora. Azh ekzema snova stala jego bespokoitj. Oh uzh eta pokupka vecnogo dvigatelia v proshlom godu! A tak zhe pokupka aeroplana-ekranoliota. Jesli tak pojdiot i daljshe, to biudzhetu pridiotsia hudo.

V etom vide fraza ot A to Ja nacinajet vygliadetj sovsem po-drugomu. Sejcas sciotka novaja, no pozzhe ona stanet staraja. Cernysh liubit kogda jego ceshut jeju. Jozh koliucij i pohozh na nejo.

Skhod mestnyh zhitelej indijskoj derevni sikkhov reshal cto zhe delatj s otkhodami kompanii "Kaligula Gaj Julij Czezarj" (lat. /Caligula Gaius Iulius Caesar/ ). Odin iz prisutstvujuscih nosil hoholok na golove. On i nashiol vyhod iz situaczii.

"Kto s mecom k nam pridiot, tot ot meca i..." - ne smog dogovoritj starshij mehanik Vasilij.

----

Liubimczem Biljbo byl junyj Frodo Sumniks. Kogda Biljbo stuknulo devianosto deviatj, on vdrug usynovil sirotu Frodo, sdelal svoim naslednikom i predlozhil pereselitjsia v Zasumki. Tut uzh vse nadezhdy Derikulj-Sumniksov, davno s vozhdelenijem posmatrivavshih na usadjbu, ruhnuli okoncateljno.

Slucaju bylo ugodno, ctoby Biljbo s Frodo jescio i rodilisj v odin denj, 22 sentiabria.

– Frodo, maljcik moj, – skazal kak-to raz Biljbo, – perebiralsia by ty ko mne. Gliadishj, i denj rozhdenija vmeste otmecali by.

Frodo v tu poru hodil v dorostkah. Tak hobbity zovut molodiozhj v bezotvetstvennom vozraste mezhdu dvadczatjju i tridczatjju tremia, posle cego hobbit nakonecz mozhet scitatj sebia vzroslym.

Proshlo jescio dvenadczatj let. V Zasumkah kazhdyj god veselo otmecali dvojnoj denj rozhdenija, k etomu privykli, no liubomu bylo jasno, cto nyneshnej osenjju gotovitsia necto neobycnoje. Biljbo ispolnialosj 111 let – vozrast dlia hobbita vesjma poctennyj, da i cislo liubopytnoje, nu a Frodo gotovilsia otmetitj tridczatitriohletije – tozhe znamemateljnaja data – sovershennoletije po-hobbitski.

----

Imejetsia neskoljko gipotez proiskhozhdenija sobaki, naiboleje verojatnymi jejo predkami scitajutsia volk i nekotoryje vidy shakalov.

V suzhdenijah ucionyh o predkah domashnej sobaki prisutstvujut dve tocki zrenija. Odni scitajut, cto sobaki - polifileticeskaja gruppa (proiskhodiascaja ot neskoljkih predkov), drugije priderzhivajutsia mnenija, cto vse sobaki proizoshli ot odnogo predka (monofileticeskaja teorija).


## Пример текста совлат-англотранс латиницы

Pįony i vasilìki vsò jescò rastut na polàne vozle derevni Pòny, scitajuscejsà bogatoj.

Pìjanyj master po proektu sdelal mehaniceskij objekt s izjanom. Jesli brak ne obnaruzhitsà, to belyje bolidy bolìshe ne smogut vyigryvatì gonki.

V pìjese pro devushku v zelònom platìjiçe vse sadilisì na ladìji i plyli po reke. No tut iz lesa vyshel Džordž Maksimus, konì v palìto i rvanyh džinsah, kotoryj cto-to vyiskival, i prikazal vsem mytìsà i gotovitì bulìjon. Znacit snova pìjom do lysyh akvalangistov.

Prepodobnyj Bajjes podkinul igralìnyje kosti. Vypalo shestì, znacit jemu pridòtsà mazatì jod na ranu.

Męr nebolìshogo gorodishki otkryl tabliçu ekselà i vozmutilsà çenoj novogo ekskavatora. Azh ekzema snova stala jego bespokoitì. Oh uzh eta pokupka vecnogo dvigatelà v proshlom godu! A tak zhe pokupka aeroplana-ekranolòta. Jesli tak pojdòt i dalìshe, to bùdžetu pridòtsà hudo.

V etom vide fraza ot A to Ja nacinajet vyglàdetì sovsem po-drugomu. Sejcas scòtka novaja, no pozzhe ona stanet staraja. Cernysh lùbit kogda jego ceshut jeju. Jozh kolùcij i pohozh na nejo.

Skhod mestnyh zhitelej indijskoj derevni sikkhov reshal cto zhe delatì s otkhodami kompanii "Kaligula Gaj Julij Çezarì" (lat. /Caligula Gaius Iulius Caesar/ ). Odin iz prisutstvujuscih nosil hoholok na golove. On i nashòl vyhod iz situaçii.

"Kto s mecom k nam pridòt, tot ot meca i..." - ne smog dogovoritì starshij mehanik Vasilij.

----

Lùbimçem Bilìbo byl junyj Frodo Sumniks. Kogda Bilìbo stuknulo devànosto devàtì, on vdrug usynovil sirotu Frodo, sdelal svoim naslednikom i predlozhil pereselitìsà v Zasumki. Tut uzh vse nadezhdy Derikulì-Sumniksov, davno s vozhdelenijem posmatrivavshih na usadìbu, ruhnuli okoncatelìno.

Slucaju bylo ugodno, ctoby Bilìbo s Frodo jescò i rodilisì v odin denì, 22 sentàbrà.

– Frodo, malìcik moj, – skazal kak-to raz Bilìbo, – perebiralsà by ty ko mne. Glàdishì, i denì rozhdenija vmeste otmecali by.

Frodo v tu poru hodil v dorostkah. Tak hobbity zovut molodòzhì v bezotvetstvennom vozraste mezhdu dvadçatìju i tridçatìju tremà, posle cego hobbit nakoneç mozhet scitatì sebà vzroslym.

Proshlo jescò dvenadçatì let. V Zasumkah kazhdyj god veselo otmecali dvojnoj denì rozhdenija, k etomu privykli, no lùbomu bylo jasno, cto nyneshnej osenìju gotovitsà necto neobycnoje. Bilìbo ispolnàlosì 111 let – vozrast dlà hobbita vesìma poctennyj, da i cislo lùbopytnoje, nu a Frodo gotovilsà otmetitì tridçatitròhletije – tozhe znamematelìnaja data – sovershennoletije po-hobbitski.

----

Imejetsà neskolìko gipotez proiskhozhdenija sobaki, naiboleje verojatnymi jejo predkami scitajutsà volk i nekotoryje vidy shakalov.

V suzhdenijah ucònyh o predkah domashnej sobaki prisutstvujut dve tocki zrenija. Odni scitajut, cto sobaki - polifileticeskaja gruppa (proiskhodàscaja ot neskolìkih predkov), drugije priderzhivajutsà mnenija, cto vse sobaki proizoshli ot odnogo predka (monofileticeskaja teorija).


## TO DO

* [ ] Написать кодировщик и декодировщик на питоне, а потом проверить на каком-нибудь словаре, а так же на случайно-сгенерированных словах. Я не проверял алгоритм декодирования даже мысленно. Но интуитивно чувствую, что он хорошо определён и реализуем. Собственно, алгоритм кодировки строился такой, чтобы не было такого, чтобы разные русские слова (любые) отображались в одну и ту же транслитерацию.
* [ ] Попробовать сделать фильтр pandoc. Но там надо посмотреть какой элемент гарантированно содержит только голый текст.
* [ ] Сделать режим, в котором просто все русские обособленные слова преобразуются в массиве текста.
* [ ] Оформить в виде модуля питона с CLI.
* [ ] Написать инструкцию как сконвертировать произвольную страницу в интернете с помощью сохранения как html и конвертации фильтром/пандоком.
* [ ] Попробовать сделать однострочный джавастрипт, которым можно перевести любую уже открытую страницу в интернете.

Mics:

* [List of Unicode characters](https://en.wikipedia.org/wiki/List_of_Unicode_characters), [List of Latin-script letters](https://en.wikipedia.org/wiki/List_of_Latin-script_letters).
* [Частотность](https://ru.wikipedia.org/wiki/%D0%A7%D0%B0%D1%81%D1%82%D0%BE%D1%82%D0%BD%D0%BE%D1%81%D1%82%D1%8C)
