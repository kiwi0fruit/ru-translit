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
|     f     |   h/ch    |   cz     |    c     |    sh    |
|   **щ**   |   **ъ**   |  **ь**   |  **сч**  | **чз, чьз** |
|    sc     |  None/qq  |   j/jqq  |  sc/wsc  |  cjz, cjqqz |

Алфавит транслитерации использует все буквы английского алфавита кроме Xx.

***Слово на латинице является грамматически верным если:***

1. его образ от прообраза совпадает с самим словом (`lat_word == CyrToLat(LatToCyr(lat_word))`),
2. его прообраз грамматически верен (`LatToCyr(lat_word)`).


## Аббревиатуры английской латиницы

Все слова в верхнем регистре считаются аббревиатурами и записываются по специальным правилам. Vодифицирующая буква диграфа пишется в нижнем регистре, а модифицируемая буква - в верхнем.

ГЭС/GyES, АЭС/AES, ЖКХ/ZhKH, ЧХ/CcH, ЖЭК/ZhyEK, ЕС/jES, США/SShA, МЧС/MCS, ЮАР/jUAR, ЭЭГ/EEG, ЕГЭ/jEGyE, микрорайон Щ/mikrorajon SC, СЧК/wSCK, ЩК/SCK, ЛЁН/LiON, ЛИОН/LIyON.

ИОН/ION, ЛИЁН/LIjON, ЙОД/wJOD, йод/jod, ЙЁД/JjOD, ЁД/jOD, ёд/jodw, НЫЭ/NYyE, НЫЕ/NYjE, НЙ/NwJ, ЧЗ/CjZ, ЦЗ/CzZ, ЦРУ/CzRU.

Аббревиатур с Ь и Ъ не должно быть, поэтому в них даже W не заменяется: ЛЪЁН/LJON, ЛЬЁН/LJJON, ЛЬОН/LJWJON, ЛЬЙОН/LJQQWJON

**Слова в верхнем регистре считаются аббревиатурами и пишутся по своим лаконичным правилам.** Это может ухудшать чтение текста, набранного капсом (после конверсии в латиницу). Но его и так трудно читать, так что не жалко. Не бывает словарных аббревиатур - все аббревиатуры (слова капсом) используют одни и те же стандарты (обратите внимание на йод и ёд выше).

Cлова на латинице в верхнем регистре, чтобы они не считались аббревиатурами можно писать, экранируя с помощью " \\" и "\ " (или `\w[(]?\\` и `\\[,.?;!)']?\w`).

Vsem \ZHIVO\ sobratjsia!

Но другие способы выделения все равно предпочтительнее:

Vsem *zhivo* sobratjsia!


## Совлат-англотранс латиница с диакритикой

Отличия от Английской латиницы 25:

* после согласных sia => sà, sio => sò, siu => sù, siy => sì (буквы Я,Ё,Ю,Йи), мягкий знак sjja => sjà, sjjo => sjò, sjju => sjù, sjje => sjè, sjji => sjì (и смягчающие, и йотирующие буквы ограниченного применения),
* после й: jja => jà, jjo => jò, jju => jù, jje => jè,
* sye => sė (э),
* wj => ĵ (й), wsc => sĉ (сч),
* w в конце слова => ' (апостроф),
* dzh => dž (дж), zhzh => žž (жж), czh => cž (чж),
* cz => ç (ц),
* убраны буквы Xx, Ww,
* добавлены буквы Àà, Òò, Ùù, Èè, Ìì, Ėė, Çç, Žž,
* ещё буквы для аббревиатур: Ĉĉ, Ĵĵ, Šš, Ĥĥ,
* буквы для ручной настройки обратимости Ĉĉ, Ĵĵ, ' (апостроф),
* таким образом, grave (àòùèì) даёт смягчение/йотирование, крышка и точка (ĥĉĵė) экранирует от диграфов, корона и cедиль (žšç) меняют звучание.
* ударения: sà => sǎ, sò => sǒ, sù => sǔ, se => sě (je => jé, jè => jě), sė => sé, i => í, a => á, o => ó, u => ú, y => ý (iy => iý, ì => í) (ещё новые буквы: Ǎǎ, Ǒǒ, Ǔǔ, Ěě, Íí, Éé, Áá, Óó, Úú, Ýý).

**Таким образом, буквы àòùèì после согласных смягчают, а не после согласных - йотируют.**

|   **a**   |   **о**   |  **у**   |  **э**   |  **ы**   |
|:---------:|:---------:|:--------:|:--------:|:--------:|
|     a     |     o     |    u     |   e/ė    |    y     |
|   **я**   |   **ё**   |  **ю**   |  **е**   |  **и**   |
|   ja/à    |   jo/ò    |  ju/ù    |  je/e/è  |   i/ì    |
|   **б**   |   **в**   |  **г**   |  **д**   |  **ж**   |
|     b     |     v     |    g     |    d     |    zh    |
|   **з**   |   **й**   |  **к**   |  **л**   |  **м**   |
|     z     |    j/ĵ    |    k     |    l     |    m     |
|   **н**   |   **п**   |  **р**   |  **с**   |  **т**   |
|     n     |     p     |    r     |    s     |    t     |
|   **ф**   |   **х**   |  **ц**   |  **ч**   |  **ш**   |
|     f     |   h/ch    |    ç     |    c     |    sh    |
|  **щ** |  **ъ**  | **ь** | **сч** | **чз, чьз, чж, дж, жж** |
|    sc  | None/qq | j/jqq | sc/sĉ  | ĉz, cjqqz, cž, dž, žž  |


## Аббревиатуры совлат-англотранс латиницы

ГЭС/GyES/GĖS, АЭС/AES, ЖКХ/ZhKH/ŽKH, ЧХ/CcH/CĤ, ЖЭК/ZhyEK/ŽĖK, ЕС/jES/ÈS, США/SShA/SŠA, МЧС/MCS, ЮАР/jUAR/ÙAR, ЭЭГ/EEG, ЕГЭ/jEGyE/ÈGĖ, микрорайон Щ/mikrorajon SC, СЧК/wSCK/SĈK, ЩК/SCK, ЛЁН/LiON/LÒN, ЛИОН/LIyON/LÌON.

ИОН/ION, ЛИЁН/LIjON/LIÒN, ЙОД/wJOD/ĴOD, йод/jod, ЙЁД/JjOD/JÒD, ЁД/jOD/ÒD, ёд/jodw/jod', НЫЭ/NYyE/NYĖ, НЫЕ/NYjE/NYÈ, НЙ/NwJ/NĴ, ЧЗ/CjZ/ĈZ, ЦЗ/CzZ/ÇZ, ЦРУ/CzRU/ÇRU.

Аббревиатур с Ь и Ъ не должно быть: ЛЪЁН/LJON, ЛЬЁН/LJJON/LJÒN, ЛЬОН/LJWJON/LJĴON, ЛЬЙОН/LJQQWJON/LJQQĴON


## Примеры интересных случаев

лён/lion/lòn  
Лион/Liyon/Lìon  
пион/piyon/pìon  
пиы/piyy/pìy  
мэр/myer/mėr  
ыэр/yer  
мыэр/myyer/myėr  
этот/etot  
если/jesli  
конь/konj  
кони/koni  
Юля/Julia/Julà  
Юлия/Julija  
Юлиан/Juliyan/Julìan  
пьяный/pjjanyj/pjànyj  
подъезд/podjezd  
пьеса/pjjesa/pjèsa  
пйеса/pwjjesa/pĵèsa  
паьеса/paqjjesa/paqjèsa  
паьаса/paqjqqasa  
пайъеса/pajqqjesa  
ёж/jozh  
йож/wjozh/ĵozh  
йод/jod  
ёд/jodw/jod'   
ёдйод/jodwjoh/jodĵod  
аллилуйя/allilujja/allilujà  
ладьи/ladjji/ladjì  
Таунйин/Taunjin  
Пиньиу/Pinjjiu/Pinjìu  
Таунйиан/Taunjian  
Тарвасйыги/Tarvasjygi  
баньтьынг/banjtjqqyng  
сьйы/sjjy  
пьём/pjjom/pjòm  
бульон/buljjon/buljòn  
выучить/vyucitj  
выострить/vyostritj  
выигрывать/vyigryvatj  
объимать/obqqimatj  
объизвестить/obqqizvestitj  
бельэтаж/beljjetazh/beljètazh  
грабьармия/grabjqqarmija  

|              | Правило транслита / правило латиницы                                                                                                                     | Кириллица/Транслит/Латиница                                                                                                                                                                                                          |
|:------------:|:-------------------------------------------------------------------------------------------------------------------------------------------------------- |:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
|    **ъ**     | None (после согласных перед **яёюе**), **qq** (иначе)                                                                                                    | изъян/izjan, объект/objekt, объимать/obqqimatj, объизвестить/obqqizvestitj, Йонъин/Jonqqin, Сёркйосен/Siorkjosen, ёркйосен/jorkwjosen/jorkĵosen, онъ/onqq, Муъминат/Muqqminat, Чанъань/Canqqanj, нъын/nqqyn                                             |
|    **ьо**    | **jjo/jò**                                                  | бульон/buljjon/buljòn, бульонъён/buljwjonjon/buljĵonjon, сеньор/senjjor/senjòr, лосьон/losjjon/losjòn, лосьён/losjqqjon, лосьйон/losjwjon/losjĵon, осьён/osjjon/osjòn, осьон/osjwjon/osjĵon, осьйон/osjqqwjon/osjqqĵon (здесь **специально для словарных слов с ьо** изменена логика модификации с помощью w - важно какой вариант, ьё или ьо, является ходовым для данного слова)                  |
|    **ьи**    | **jji/jì**                                                                                            | ладьи/ladjji/ladjì, платьице/platjjicze/platjìçe, Вильйинг/Viljqqjing                                                                                                      |
|    **ь**     | **jqq** (перед гласными **ауэы** и буквами **йьъ**), **j** (иначе)                                                                           | бельэтаж/beljjetazh/beljètazh, бельетаж/beljqqjetazh, бельйэтаж/beljwjetazh/beljĵetazh, ельэтаж/eljqqetazh, ельетаж/eljjetazh/eljètazh, ельйэтаж/eljwjetazh/eljĵetazh, грабьармия/grabjqqarmija, костьутиль/kostjqqutilj, пьеса/pjjesa/pjèsa пьян/pjjan/pjàn, прячься/priacjsia/pràcjsà, мыться/mytjsia/mytjsà, конь/konj, ньын/njqqyn (здесь **специально для словарного исключения бельэтаж** изменена логика модификации с помощью w)                                                                                     |
| **й[аоуэ]**  | **j[aoue]** (гласные **аоуэ** после й), **wj[aoue]/ĵ[aoue]** (альтернативная йотация)                                                             | йод/jod, ёж/jozh, йэс/wjes/ĵes, ёдйод/jodwjoh/jodĵoh                              |
|    **й**     | **j** (остальные простые случаи), **wj/ĵ** (сложные случаи)                                                                                       | красный/krasnyj, аллилуйя/allilujja/allilujà, Байес/Bajjes/Bajès, йиппи/jippi, сйс/swjs/sĵs                                                    |
|    **ы**     | **y**                                                                                                        | пыл/pyl, пыхтел/pyhtel, мы/my, красный/krasnyj, Нарва-Йыэсуу/Narva-Jyesuu, Шайыр/Shajyr, выход/vyhod, выигрывать/vyigryvatj, выучить/vyucitj, выострить/vyostritj                                                                                                                        |
|    **е**     | **е** (после согласных или в словарных словах-исключениях когда е читается как э), **jje/jè** (после й), **je** (иначе)                                                        | мера/mera, еда/jeda, если/jesli, заезд/zajezd, Байес/Bajjes/Bajès, заем/zajem, заём/zajom, траектория/trajektorija, проект/proekt, проэкт/prowekt/proękt, проэк/proek/proek (**проект - словарное исключение** с особым правилом отображения) |
|    **э**     | **ye/ė** (после согласных или после ы в закрытом слоге), **е** (иначе)                                                                                                         | мэр/myer/mėr, этот/etot, аэроплан/aeroplan, поэт/poet, эротика/erotika, йэс/wjes/ĵes, ыэр/yer, мыэр/myyer/myėr                                                                                                                                               |
|  **[яёю]**   | **i[aou]/[àòù]** (после согласных), **jj[aou]/j[àòù]** (после й), **j[aou]** (иначе)                                                                                                         | синяя/siniaja/sinàja, мёд/miod/mòd, ёлка/jolka, пюре/piure/pùre, якорь/jakorj                                                                                                                                                                        |
|    **х**     | **ch** (когда есть неоднозначность из-за других диграфов и триграфов с h), **h** (иначе)                                                                 | сход/schod, кхе/khe, сикх/sikh, шхуна/shchuna, чхать/cchatj, отход/otchod, хахх/hahh, хохолок/hoholok, выход/vyhod, меха/meha, эхо/eho, вече/vece, меча/meca (помимо диграфов из этой спецификации стоит так же избегать **th** и **ck**)                                         |

|                | Ещё примеры                                                                            |
| -------------- | -------------------------------------------------------------------------------------- |
| дж, dzh/dž     | Джордж/Dzhordzh/Džordž                                                                 |
| щ, sc          | щётка/sciotka/scòtka, ещё/jescio/jescò                                                 |
| сч, sc, wsc/sĉ | счёт/sciot/scòt, трусчёт/truwsciot/trusĉòt                                             |
| ж, zh          | ёж/jozh, возжи/vozzhi, позже/pozzhe                                                    |
| жж, zhzh/žž    | жужжать/zhuzhzhatj/zhužžatj                                                            |
| чж, сzh/сž     | Чжань/Czhanj/Cžanj, цха/czcha/çcha                                                     |
| ч, c, ch       | чесать/cesatj, Черныш/Cernysh, счётная/sciotnaja/scòtnaja, Кирпичзев/Kirpicjzev, чхать/cchatj, чьз/cjqqz |
| ц, cz/ç        | центурион/czenturiyon/çenturìon, процессор/proczessor/proçessor, Цезарь/Czezarj/Çezarj |
| ш, sh          | шлем/shlem                                                                             |
| ё, jo, io/ò    | мёд/miod/mòd, ёмко/jomko                                                               |
| ю, ju, iu/ù    | мюсли/miusli/mùsli, Юля/Julia/Julà                                                     |
| я, ja, ia/à    | Изя/Izia/Izà, Якорь/Jakorj, баян/bajan                                                 |


## Пример текста английской латиницы

Piyony i vasiljki vsio jescio rastut na poliane vozle derevni Piony, scitajuscejsia bogatoj.

Pjjanyj master po proektu sdelal mehaniceskij objekt s izjanom. Jesli brak ne obnaruzhitsia, to belyje bolidy boljshe ne smogut vyigryvatj gonki.

V pjjese pro devushku v zelionom platjjicze vse sadilisj na ladjji i plyli po reke. No tut iz lesa vyshel Dzhordzh Maksimus, konj v paljto i rvanyh dzhinsah, kotoryj cto-to vyiskival, i prikazal vsem mytjsia i gotovitj buljjon. Znacit snova pjjom do lysyh akvalangistov.

Prepodobnyj Bajjes podkinul igraljnyje kosti. Vypalo shestj, znacit jemu pridiotsia mazatj jod na ranu.

Myer neboljshogo gorodishki otkryl tabliczu ekselia i vozmutilsia czenoj novogo ekskavatora. Azh ekzema snova stala jego bespokoitj. Oh uzh eta pokupka vecnogo dvigatelia v proshlom godu! A tak zhe pokupka aeroplana-ekranoliota. Jesli tak pojdiot i daljshe, to biudzhetu pridiotsia hudo.

V etom vide fraza ot A to Ja nacinajet vygliadetj sovsem po-drugomu. Sejcas sciotka novaja, no pozzhe ona stanet staraja. Cernysh liubit kogda jego ceshut jeju. Jozh koliucij i pohozh na nejo.

Schod mestnyh zhitelej indijskoj derevni sikhov reshal cto zhe delatj s otchodami kompanii "Kaligula Gaj Julij Czezarj" (lat. /Caligula Gaius Iulius Caesar/). Odin iz prisutstvujuscih nosil hoholok na golove. On i nashiol vyhod iz situaczii.

"Kto s mecom k nam pridiot, tot ot meca i..." - ne smog dogovoritj starshij mehanik Vasilij.

----

Liubimczem Biljbo byl junyj Frodo Sumniks. Kogda Biljbo stuknulo devianosto deviatj, on vdrug usynovil sirotu Frodo, sdelal svoim naslednikom i predlozhil pereselitjsia v Zasumki. Tut uzh vse nadezhdy Derikulj-Sumniksov, davno s vozhdelenijem posmatrivavshih na usadjbu, ruhnuli okoncateljno.

Slucaju bylo ugodno, ctoby Biljbo s Frodo jescio i rodilisj v odin denj, 22 sentiabria.

– Frodo, maljcik moj, – skazal kak-to raz Biljbo, – perebiralsia by ty ko mne. Gliadishj, i denj rozhdenija vmeste otmecali by.

Frodo v tu poru hodil v dorostkah. Tak hobbity zovut molodiozhj v bezotvetstvennom vozraste mezhdu dvadczatjju i tridczatjju tremia, posle cego hobbit nakonecz mozhet scitatj sebia vzroslym.

Proshlo jescio dvenadczatj let. V Zasumkah kazhdyj god veselo otmecali dvojnoj denj rozhdenija, k etomu privykli, no liubomu bylo jasno, cto nyneshnej osenjju gotovitsia necto neobycnoje. Biljbo ispolnialosj 111 let – vozrast dlia hobbita vesjma poctennyj, da i cislo liubopytnoje, nu a Frodo gotovilsia otmetitj tridczatitriohletije – tozhe znamemateljnaja data – sovershennoletije po-hobbitski.

----

Imejetsia neskoljko gipotez proischozhdenija sobaki, naiboleje verojatnymi jejo predkami scitajutsia volk i nekotoryje vidy shakalov.

V suzhdenijah ucionyh o predkah domashnej sobaki prisutstvujut dve tocki zrenija. Odni scitajut, cto sobaki - polifileticeskaja gruppa (proiskhodiascaja ot neskoljkih predkov), drugije priderzhivajutsia mnenija, cto vse sobaki proizoshli ot odnogo predka (monofileticeskaja teorija).


## Пример текста совлат-англотранс латиницы

Pìony i vasiljki vsò jescò rastut na polàne vozle derevni Pòny, scitajuscejsà bogatoj.

Pjànyj master po proektu sdelal mehaniceskij objekt s izjanom. Jesli brak ne obnaruzhitsà, to belyje bolidy boljshe ne smogut vyigryvatj gonki.

V pjèse pro devushku v zelònom platjìçe vse sadilisj na ladjì i plyli po reke. No tut iz lesa vyshel Džordž Maksimus, konj v paljto i rvanyh džinsah, kotoryj cto-to vyiskival, i prikazal vsem mytjsà i gotovitj buljòn. Znacit snova pjòm do lysyh akvalangistov.

Prepodobnyj Bajès podkinul igraljnyje kosti. Vypalo shestj, znacit jemu pridòtsà mazatj jod na ranu.

Mėr neboljshogo gorodishki otkryl tabliçu ekselà i vozmutilsà çenoj novogo ekskavatora. Azh ekzema snova stala jego bespokoitj. Oh uzh eta pokupka vecnogo dvigatelà v proshlom godu! A tak zhe pokupka aeroplana-ekranolòta. Jesli tak pojdòt i daljshe, to bùdžetu pridòtsà hudo.

V etom vide fraza ot A to Ja nacinajet vyglàdetj sovsem po-drugomu. Sejcas scòtka novaja, no pozzhe ona stanet staraja. Cernysh lùbit kogda jego ceshut jeju. Jozh kolùcij i pohozh na nejo.

Schod mestnyh zhitelej indijskoj derevni sikhov reshal cto zhe delatj s otchodami kompanii "Kaligula Gaj Julij Çezarj" (lat. /Caligula Gaius Iulius Caesar/). Odin iz prisutstvujuscih nosil hoholok na golove. On i nashòl vyhod iz situaçii.

"Kto s mecom k nam pridòt, tot ot meca i..." - ne smog dogovoritj starshij mehanik Vasilij.

----

Lùbimçem Biljbo byl junyj Frodo Sumniks. Kogda Biljbo stuknulo devànosto devàtj, on vdrug usynovil sirotu Frodo, sdelal svoim naslednikom i predlozhil pereselitjsà v Zasumki. Tut uzh vse nadezhdy Derikulj-Sumniksov, davno s vozhdelenijem posmatrivavshih na usadjbu, ruhnuli okoncateljno.

Slucaju bylo ugodno, ctoby Biljbo s Frodo jescò i rodilisj v odin denj, 22 sentàbrà.

– Frodo, maljcik moj, – skazal kak-to raz Biljbo, – perebiralsà by ty ko mne. Glàdishj, i denj rozhdenija vmeste otmecali by.

Frodo v tu poru hodil v dorostkah. Tak hobbity zovut molodòzhj v bezotvetstvennom vozraste mezhdu dvadçatjù i tridçatjù tremà, posle cego hobbit nakoneç mozhet scitatj sebà vzroslym.

Proshlo jescò dvenadçatj let. V Zasumkah kazhdyj god veselo otmecali dvojnoj denj rozhdenija, k etomu privykli, no lùbomu bylo jasno, cto nyneshnej osenjù gotovitsà necto neobycnoje. Biljbo ispolnàlosj 111 let – vozrast dlà hobbita vesjma poctennyj, da i cislo lùbopytnoje, nu a Frodo gotovilsà otmetitj tridçatitròhletije – tozhe znamemateljnaja data – sovershennoletije po-hobbitski.

----

Imejetsà neskoljko gipotez proischozhdenija sobaki, naiboleje verojatnymi jejo predkami scitajutsà volk i nekotoryje vidy shakalov.

V suzhdenijah ucònyh o predkah domashnej sobaki prisutstvujut dve tocki zrenija. Odni scitajut, cto sobaki - polifileticeskaja gruppa (proiskhodàscaja ot neskoljkih predkov), drugije priderzhivajutsà mnenija, cto vse sobaki proizoshli ot odnogo predka (monofileticeskaja teorija).


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
