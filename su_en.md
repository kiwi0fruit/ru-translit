# Совлат англотранс с двойными CG

### Краткий конспект

(подробности ниже)

|   **a**   |   **о**   |  **у**   |  **э**   |  **ы**   |
|:---------:|:---------:|:--------:|:--------:|:--------:|
|     a     |     o     |    u     |   e/ae   |    y/i   |
|   **я**   |   **ё**   |  **ю**   |  **е**   |  **и**   |
|   ja/ia   |   jo/io   |  ju/iu   |  je/e/ie |  i/iy/y  |
|   **б**   |   **в**   |  **г**   |  **д**   |  **ж**   |
|     b     |     v     |   g/gh   |    d     |  g[eij]  |
|   **з**   |   **й**   |  **к**   |  **л**   |  **м**   |
|     z     |   j/ji    |   c/ck   |    l     |    m     |
|   **н**   |   **п**   |  **р**   |  **с**   |  **т**   |
|     n     |     p     |    r     |    s     |    t     |
|   **ф**   |   **х**   |  **ц**   |  **ч**   |  **ш**   |
|     f     |   h/kh    |  c[eij]  |    ch    |    sh    |
|   **щ**   |   **ъ**   |  **ь**   |  **сч, чж, кж**          | **кс, кц, ктс, йи, кх**  |
|    sch    |  None/qq  |    j     |   sch, cg[eij], ckg[eij] | cs, cts, ckts, jy/iy, ckh |

После ц и ж могут быть только мягкие гласные (e/i) или ь (j). ки это cy, ги это gy, перед остальными мягкими гласными Кк это ck, Гг это gh. После ч, ш, щ, кц могут быть только e,i,a,o,u (ie, ia, io, iu, j(ь), ae(э), y(ы) не бывает). Ха это h в начале слов и после гласных, иначе - kh. Мягкий знак это j, а перед a,o,u,e(э),y(ы) его не бывает, но можно задать нужный прообраз с помощью jw. Твердый знак перед йотированными гласными не ставится - достаточно отсутствия смягчения согласной, а в остальных нетипичных случаях - qq. И Ее, и Ээ после согласных это просто Ee (кроме случаев твердых Кк и Гг: cae, gae), но для разводки противоречий можно явно поставить мягкую Ее - ie или твёрдую Ээ - ae.

**i йотирует только после j**.

*Ещё правила (которые имеют приоритет перед другими описанными - я еще не исправил описание)*: **чж - cg[eij]**, в аббревиатуры и инициалы идёт как **Ch** (Cgiunkhua), **кж - ckg[eij]**. Для **ё после согласных** (но не после йота или Цц) использовать **eo** вместо **io** (а **eo** после согласных кроме **h** и **k** становится **ieo**: lieo/лео, gheo/гео, ghiol/гёл, geoltoc/жёлток, licio/лицо). Так будет менее логично, но зато чуть более этимологично и будет лучшее переиспользование уже обученных нейросетей в голове. Так же стоит считать, что:

1) ц[еэиы]/c[ei] - ц\_/ць/сj - ц[оёаяую]/ci[oau] - ци[аоуэ]/ciy[aoue] - це[аоуэ]/ce[aoue]
2) ж[еэиы]/g[ei] - ж\_/жь/gj - жё/geo - ж[оаяую]/gi[oau] - жи[аоуэ]/giy[aoue] - жео/gieo - же[ауэ]/ge[aue]
3) к[еы]/ck[ey] - к[ауои]/с[auoy] - к[яюё]/cki[auo] - кэ/cae - ки[аоуэ]/cy[aoue] - ке[аоуэ]/cke[aoue]
4) г[еы]/gh[ey] - г[ауои]/g[auoy] - г[яюё]/ghi[auo] - гэ/gae - ги[аоуэ]/gy[aoue] - ге[аоуэ]/ghe[aoue]
5) ч[еэиыаяуюёо]/ch[eiauo] - ч\_/чь/ch - чи[аоуэ]/chi[aoue] - че[аоуэ]/che[aoue]
6) ш[еэиыаяуюёо]/sh[eiauo] - ш\_/шь/sh - ши[аоуэ]/shi[aoue] - ше[аоуэ]/she[aoue]
7) с[еауоиы]/s[eauoiy] - сё/seo - с[яю]/si[au] - сэ/se/sae - си[аоуэ]/siy[aoue] - сео/sieo - се[ауэ]/se[aue]

**Если "ке" читается как "кэ", то писать стоит "cae" вместо "cke".**

нянька/nianjca, конь/conj, пьеса/pjiesa, объект/object, ночь/noch, меч/mech, жду/gjdu, рожь/rogj, нож/nogj 

*Дополнительные опциональные правила*: Может, стоит ввести и **кс - x, cs (на стыке морфем)**. Xenija вопреки всему даёт инициал **C.** Так же можно писать **кз** как **xz** для словарных исключений (exzamen). Ещё можно писать **кв** как **cqu** (cquity), а **ф** как **ph** в некоторых словарных словах латинского происхождения.  


### Подробности в виде таблицы

**_force_** обозначает принудительное задание прообраза в кириллице не дефолтным вариантом. При достаточно жирном словаре отображения из/в кириллицу принудительное задание не должно по идее использоваться совсем.

|                  **a, [жц]а, [чщш]а**                  |  **о, [жц]о, [чщш]о, сьо, [чщш]ьо**  |            **у, [жц]у, [чщш]у**             |        **э, сэ, [жшчщц]э, саэ**         |               **ы, [жшчщц]ы**               |
|:------------------------------------------------------:|:---------------------------:|:-------------------------------------------:|:---------------------------------------:|:-------------------------------------------:|
|                   a, [...]ia, [...]a                   |  o, [...]io, [...]o, sjio, [...]jo   |             u, [...]iu, [...]u              |          e, sae, [...]e, saae           |                  y, [...]i                  |
|                **я, ся, [йь]я, [чщш]ья**               |  **ё, сё, [йь]ё, [чщш]ьё**   |          **ю, сю, [йь]ю, [чщш]ью**           |        **е, се, [йь]е, [чщш]ье**         |    **и, си[аоуэ], [кгй]и, сьи, [чщш]ьи**     |
|                 ja, sia, jia, [...]ja                  |    jo, sio, jio, [...]jo    |            ju, siu, jiu, [...]ju            |          je, se, jie, [...]je           |     i, siy[aoue], [cgj]y, sjiy, [...]jy     |
|                         **б**                          |            **в**            |           **г, г[ьъйеяёюыж], ги**           |                  **д**                  | **ж, жь, ж[иыеэяаёоюу], _force: жь, ж[яёю], ж[ыэ]_** |
|                           b                            |              v              |               g, gh[...], gy                |                    d                    |          gj, gj, g[...], _gjj, gii[...], wg[...]_           |
|                         **з**                          | **й, йи, сйс, _force: й[оауэы]_** |           **к, к[ьъйеяёюч], ки, кц, ктс**           |                  **л**                  |                    **м**                    |
|                           z                            |       j, jy, sjis, _wj[...]_        |               c, ck[...], cy, cts, ckts                 |                    l                    |                      m                      |
|                         **н**                          |            **п**            |                    **р**                    |                  **с**                  |                    **т**                    |
|                           n                            |              p              |                      r                      |                    s                    |                      t                      |
|                         **ф**                          |  **х, ^х, [иыеэяаёоюу]х**   | **ц, ць, ц[иыеэяаёоюу], _force: ць, ц[яю], ц[ыэё]_** | **ч, ч[иыеэяаёоюу]** |   **ш, ш[иыеэяаёоюу]**   |
|                           f                            |       kh, ^h, [...]h        |          cj, cj, c[...], _cjj, cii[...], wc[...]_           |         ch, ch[ieaou],         |           sh, sh[ieaou],           |
|                         **щ**                          |       **ъ, съ[еяёю]**       |        **ь, сь[еяёоюи], _force сь[эаоуы]_**         |               **кс**               |          **сч , _force сч[...]_**           |
| так же как "сч" ("щ" имеет приоритет обратного образа) |        qq, sj[eaou]         |          j, sji[eaoouy], _sjw[...]_          |                 cs                 |          sch, _wsch[...]_           |

Дополнительно: **чж - cg[eij]** (в аббревиатуры и инициалы идёт как **Ch**), **кж - ckg[eij]**. И: **кх - ckh**.


### Аббревиатуры

**После Щ,Ч,Ш,Г,К,Й "И" пишется как Y: SchY, ChY, ShY, GY, CY, JY.**  
**А "Ы" пишется: SchhY, ChhY, ShhY, GhY, CkY, JIY.**

| **А** |     **О**      |  **У**  | **Э**  |  **Ы**  |
|:-----:|:--------------:|:-------:|:------:|:-------:|
|   A   |       O        |    U    |   E    |    Y    |
| **Я** |     **Ё**      |  **Ю**  | **Е**  |  **И**  |
|  JA   |      JO        |   JU    |  JE    |   I/Y   |
| **Б** |     **В**      |  **Г**  | **Д**  |  **Ж**  |
|   B   |       V        |  G/Gh   |   D    |   GI    |
| **З** |     **Й**      |  **К**  | **Л**  |  **М**  |
|   Z   |      J/JI      |  C/Ck   |   L    |    M    |
| **Н** |     **П**      |  **Р**  | **С**  |  **Т**  |
|   N   |       P        |    R    |   S    |    T    |
| **Ф** |     **Х**      |  **Ц**  | **Ч**  |  **Ш**  |
|   F   |       H        |   CI    |  Ch    |   Sh    |
| **Щ** |     **СЧ**     |         |        |         |
|  Sch  |      SCh       |         |        |         |

КЦ/CCI, КИ/CY, КИИ/CYI, ЧИ/ChY, ШИ/ShY, КЫ/CkY, ГЫ/GhY, ЧЫ/ChhY, ШЫ/ShhY, ЦИ/CII, ЙА/JIA, ЯР/JAR, ФИО/FIO, ЙИ/JY, ЙЫ/JIY, КТС/CTS, НХЛ/NHL, САЭ/SAE, СЭ/SE, СЕ/SJE

Сокращения не по правилам для краткости (когда они отдельно):

щ/sch, щ./sch., Щ/Sch, **Щ./Sc.**  
сч/sch, сч./sch., Сч/Sch, СЧ/SCh  
ск/sc, **ск./sck.**, Ск/Sc, СК/SC, **Ск./Sck.**  
чж/cgj, чж./cgj., Чж/Cgj, ЧЖ/ChGI, ЧЖ./ChGI., **Чж./Сg.**  
кг/cg, **кг./ckg.**, Кг/Cg, КГ/CG, КГ./CG., **Кг./Сkg.**  
ж/gj, Ж/Gj, Ж./Gi.  
жи/giy, Жи/Giy, ЖИ/GII  
ц/cj, Ц/Cj, Ц./Ci.  
ци/ciy, Ци/Ciy, ЦИ/CII


### Подробности

**Слова на латинице из других языков** можно писать, экранируя с помощью ``" ::[\w]"`` и ``"[\w]:: "``.

Когда требуется пометить всего одно слово - до следующего знака препинания, то это можно сделать с помощью одной запятой в начале слова (``" ,[\w]"``). А если нужно пометить кусок текста до следующего пробельного символа, то это можно сделать с помошью всего одной точки (``" .[\w]"``). А с помощью двух точек можно пометить кусок текста до конца предложения (``" ..[\w]"``) - так же можно принудительно закрыть с помощью ``"[\w].. "``.

,R-aghent vypil butylcu .Coca-Cola i zagovoril ..Hello, do you speak English?

=>

R-агент выпил бутылку Coca-Cola и заговорил Hello, do you speak English?

oj ..Hello... no. => ой Hello... no. => oj ..Hello... no.

oj ::Hello?:: => ой Hello? => oj .Hello?

oj ..Hello... да no. => ой ..Hello... да no. => oj ..Hello... да no. (экранирующие точки нельзя убирать, т.к. текст не полностью на латинице)

**Слова в верхнем регистре считаются аббревиатурами и пишутся по своим лаконичным правилам.** Это может ухудшать чтение текста, набранного капсом (после конверсии в латиницу). Но его и так трудно читать, так что не жалко. Не бывает словарных аббревиатур - все аббревиатуры (слова капсом) используют одни и те же стандарты.

Cлова на латинице в верхнем регистре, чтобы они не считались аббревиатурами можно писать, экранируя с помощью ``" -"`` и ``"- "``:

Vsem -GIVO- sobratjsia!

Но другие способы выделения все равно предпочтительнее:

Vsem *givo* sobratjsia!

**Использование k и z минимизировано.**

В латинице используется 25 букв - все, кроме Xx.

Латиница использует подход к й, ь, ъ и гласным как во ВТОРОЙ версии совлата (дополнительно отличается ъ от ь). А вот согласные используются как в латинице Ярослава Тимина с моими модификациями.

Примечательно чередование Кк/Цц, которые обе через Cc. Только Цц когда смягченная. Редкие смягченные Кк даются через ck. Тоже самое с Гг/Жж через Gg. Жж - когда смягченная. Редкие смягченные Гг даются через gh. Исключением являются ки/cy и ги/gy, т.к. кы и гы не бывает, то можно переназначить.

### Гласные, ь, ъ, й

Финальная юникод-латиница использует подход к й, ь, ъ и гласным как в ПЕРВОЙ версии совлата (дополнительно отличается ъ от ь), а версия в базовой латинице-26 скорее как во второй версии совлата.

**ы - y, и - i/iy/y.**

* Ее - JEje + Ee (еда/jeda, сек/sec) / IEie (сье/sjie, йе/jie)
* Ёё - JOjo + Oo (ёж/jogj, её/jejo, съё/sjo) / IOio (жё/gio, цё/cio, сьё/sjio)
* Юю - JUju + Uu / IUiu (аналогично ё)
* Яя - JAja + Aa / IAia (аналогично ё, йя/jia)
* Оо - Oo (очевидно) / IOio (сьо/sjio, жо/gio, цо/cio)
* Ии - Ii (очевидно) / IYiy (сьи/sjiy; сиа/siya)
* Ьь - Jj (сь./sj., ськ/sjc) / None (сьо/sjio, сьё/sjio, сье/sjie, сьи/sjiy)
* Ъъ - QQqq (съо/sqqo) / None (съе/sje, съё/sjo)
* Йй - Jj (йод/jod)
* Ээ - Ee (этот/etot, мэр/mer) / AEae (мэр/maer)

Новая буква "Ё" - IOio, больше не является всегда ударной.


### к/c/ck + ц/c/cj

**не дефолтный прообраз** - технические исключения, когда слова нет в словаре. Показано как должны записываться нестандартные прообразы.

| к          | ц      | кь, къя          | ць, цья        | не дефолтный прообраз |
| ---------- | ------ | ---------------- | -------------- | --------------------- |
| к/c        | ц/cj   | кь/ckj, къя/ckja | ць/cj, цья/cja | ць/cjj                |
| ка/ca      | ца/cia | кя/ckia          | ця/cia         | ця/ciia, цъя/cjqqja   |
| ку/cu      | цу/ciu | кю/ckiu          | цю/ciu         | цю/ciiu               |
| ко/co      | цо/cio | кё/ckio          | цё/cio         | цё/ciio               |
| кэ/cae     | цэ/ce  | ке/cke           | це/ce          | цэ/wce, цьэ/cjjwe     |
| **кы/cky** | цы/ci  | **ки/cy**        | ци/ci          | цы/wci                |


### г/g/gh + ж/g/gj

| г          | ж      | гь, гъя          | жь, жья        | не дефолтный прообраз |
| ---------- | ------ | ---------------- | -------------- | --------------------- |
| г/g        | ж/gj   | гь/ghj, гъя/ghja | жь/gj, жья/gja | жь/gjj                |
| га/ga      | жа/gia | гя/ghia          | жя/gia         | жя/giia, жъя/gjqqja   |
| гу/gu      | жу/giu | гю/ghiu          | жю/giu         | жю/giiu               |
| го/go      | жо/gio | гё/ghio          | жё/gio         | жо/wgio               |
| гэ/gae     | жэ/ge  | ге/ghe           | же/ge          | жэ/wge, жьэ/gjjwe     |
| **гы/ghy** | жы/gi  | **ги/gy**        | жи/gi          | жы/wgi                |


### ч/ch + ш/sh

| ч      | ш      | чь              | шь              | не дефолтный прообраз                  |
| ------ | ------ | --------------- | --------------- | -------------------------------------- |
| ч/ch   | ш/sh   | чь/ch, чья/chja | шь/sh, шья/shja | шь/shj, чь/chj, чъя/chqqja, шъя/shqqja |
| ча/cha | ша/sha | чя/cha          | шя/sha          | шя/shia, чя/chia                       |
| чу/chu | шу/shu | чю/chu          | шю/shu          | шю/shiu, чю/chiu                       |
| чо/cho | шо/sho | чё/cho          | шё/sho          | шо/wsho, чо/wcho                       |
| чэ/che | шэ/she | че/che          | ше/she          | шэ/shae, чэ/chae, чьэ/chjwe            |
| чы/chi | шы/shi | чи/chi          | ши/shi          | шы/shy, чы/chy                       |


### Ещё подробности

Спаривание к + ц позволило использовать c/ck + c/cj (вместо k + c).

Спаривание г + ж позволило использовать g/gh + g/gj (вместо g + zh).

ТО ЕСТЬ: меньше угловатых букв k и zh - ура!

Дефолтные прообразы: ча, че, чё, чу, чи, ч (а не чь), ша, ше, шё, шу, ши, ш (а не шь), жа, же, жё, жу, жи, ж (а не жь), ща, ще, щё, щу, щи, щ (а не щь), ца, це, цо, цу, ци, ц (а не ць) (ну кроме словарных исключений).  
Можно использовать переключатель w/', который в конце сбрасыват до дефолтных. А прямо перед местом неоднозначности прообраза можно переключить на альтернативный вариант с помощью w/'/ii/jj: жури/giuriw/giuri', жюри/giiuri, жерло/gerlow/gerlo', жэрло/wgerlo/'gerlo, кож/cogjw/cogj', кожь/cogjj (тоже самое с ц).  
Но в стандартном сценарии использования это не должно применяться - умное отображение в кириллицу само должно догадываться исходя из контекста.
Аббревиатуры - особый случай: ЖУ/GIU, ЖЮ/GIJU, ГЮ/GJU, ГУ/GU, КИ/CY, ЦЮ/CIJU.

По дефолту прообраз sch это щ, а не сч (ну кроме словарных исключений). Можно использовать переключатель сброса на дефолт w/': щёт/schotw/schot'. Или указать явно: счит/wschit.

* Заметьте, что дефолтные прообразы задаются спецификацией и зафиксированы. А вот прообразы умного алгоритма могут менять от версии к версии.
* Иногда **w** еще используется как патч для проблем, возникающих из-за словарных исключений - с помощью сброса до дефолтных значений (проект/proect, проэкт/proectw).
* **w** может быть заменет на одинарный апостроф (`'`). Если нужно использовать смысловой апостроф в конце слова или перед sch/j[aoue] или после шипящих, то его нужно будет заменить на два одинарных апострофа (`''`).


## Занимательные примеры

скалка/scalca  
щавель/schavelj  
гео/gheo  
Гёте/Ghiote  
пьеса/pjiesa  
мэр/mer/maer  
подъезд/podjezd  
...(подйыэзд/podwjyezd  
....подйиэзд/podjyezd  
....подйэзд/podwjezd  
....подйезд/podwjiezd  
....подъэзд/podqqezd  
....подьэзд/podjwezd  
....грабьармия/grabiarmija - словарное исключение, ибо нефиг так писать)  
пьём/pjiom  
...(пьеом/pjieom)  
пион/piyon  
пианино/piyanino  
платьице/platjiyce  
...(платйице/platjyce  
....йипи/jypi  
....йыпи/wjypi  
....платйыце/platwjyce)  
бульон/buljion  
объём/objom  
ёмкость/jomcostj  
йогурт/jogurt  
чёрный/chornyj  
неон/neon  
мёд/miod  
яма/jama  
Аеонтина/Ajeontina  
...(Аёнтина/Ajontina  
....Айеонтина/Ajieontina)  
обжёг/obgiog  
покъезд/pockjezd  
Д.Алигьери/D.Alighjieri  
кьем/ckjiem  
цьем/cjem  
чьем/chjem  
нанцьян/nancjan  
...(нанцъян/nancjqqjan  
....нанцъан/nancjqqan  
....нанцьан/nancjjwan)  
Йемен/Jemen (пофиксен как словарное исключение)  
Йеме/Jieme (не пофиксен)  
Байес/Bajies  
...(Баиес/Baijes)  
Аллилуйя/Allilujia  
айё/ajio  
аьк/aqjc  
ладьеобразные/ladjieobraznyje  
царь/ciarj  
Цезарь/Cezarj  
нэцкэ/necjcae/naecjcae  
Ксения/Csenija  
Кения/Ckenija  
вовлёкся/vovliocsia  
эксперт/ecspert  
Ж.Депардье/Gi.Depardjie  
Ж.Верн/Gi.Vern  
цундере/ciundere  
акация/acacija  
нация/nacija  
акция/actsija  
заяц/zajacj  
грецкий/grecjcyj  
греческий/grechescyj  
гречка/grechca  
чизкейк/chizckejc  
ноктюрн/noctiurn  
актёр/actior  
октябрь/octiabrj  
генетика/ghenetica  
герой/gheroj  
гиря/gyria  
гироскоп/gyroscop  
гимназия/gymnazija  
женщина/genschina  
Джексон/Dgecson  
Германия/Ghermanija  
хоккей/hocckej  
пицца/piccia  
дочка/dochca  
Чжунхуа/Cgiunkhua  
тревожься/trevogjsia  
...(тревожься/trevogjjsiaw  
....тревожйся/trevogjisia  
....тревожьися/trevogjysia  
....тревожьйся/trevogjjisia  
....тревожйа/trevogjwja  
....тревожъя/trevogjqqja) 

ГЭС/GES, АЭС/AES, ЖКХ/GICH, ЦХ/CIH, ЖЭК/GIEC, ЕС/JES, США/SShA, МЧС/MChS, ЮАР/JUAR, ЭЭГ/EEG, ЕГЭ/JEGE, микрорайон Щ/microrajon Sch, СЧК/SChC, ЩК/SchC, ЛЁН/LJON, ЛИОН/LION.

ИОН/ION, ЛИЁН/LIJON, ЙОД/JIOD, ЙЁД/JJOD, ЁД/JOD, НЫЭ/NYE, НЫЕ/NYJE, НЙ/NJ, ЦЗ/CIZ, ЧЗ/ChZ, ЦРУ/CIRU, ОБЖ/OBGI, АиФ/AiF.


## Пример текста

Piyony i vasiljcy vseo jescho rastut na poliane vozle derevni Peony, schitajuschejsia bogatoj.

Pjianyj master po proectu sdelal mehanichescyj object s izjanom. Jesli brac ne obnarugitsia, to belyje bolidy boljshe ne smogut vyigryvatj goncy.

V pjiese pro devushcu v zeleonom platjiyce vse sadilisj na ladjiy i plyli po recke v strane Cgiunkhua. No tut iz lesa vyshel Dgeordgj Macsimus, conj v paljto i rvanyh dginsah, cotoryj chto-to vyiscyval, i pricazal vsem mytjsia i gotovitj buljion. Znachit snova pjiom do lysyh acvalangystov.

Prepodobnyj Bajies podcynul igraljnyje costi. Vypalo shestj, znachit jemu prideotsia mazatj jod na ranu.

Maer neboljshogo gorodishcy otcryl tabliciu ecselia i vozmutilsia cenoj novogo ecscavatora. Agj eczema snova stala jego bespocoitj. Oh ugj eta pocupca vechnogo dvigatelia v proshlom godu! A tac ge pocupca aeroplana-ecranoleota. Jesli tac pojdeot i daljshe, to biudgetu prideotsia hudo.

V etom vide fraza ot A do Ja nachinajet vygliadetj sovsem po-drugomu. Sejchas schotca novaja, no pozge ona stanet staraja. Chernysh liubit cogda jego cheshut jeju. Jogj coliuchij i pohogj na nejo.

Skhod mestnyh gitelej indijscoj derevni sickhov reshal chto ge delatj s otkhodami companii "Caligula Gaj Julij Cezarj" (lat. ..Caligula Gaius Iulius Caesar). Odin iz prisutstvujuschih nosil hoholoc na golove. On i nashol vyhod iz situacii.

"Cto s mechom c nam prideot, tot ot mecha i..." - ne smog dogovoritj starshij mehanic Vasilij.

----

Liubimcem Biljbo byl junyj Frodo Baeggins. Cogda Biljbo stucnulo devianosto deviatj, on vdrug usynovil sirotu Frodo, sdelal svoim naslednicom i predlogil pereselitjsia v Zasumcy. Tut ugj vse nadegjdy Dericulj-Baegginsov, davno s vogjdelenijem posmatrivavshih na usadjbu, ruhnuli oconchateljno.

Sluchaju bylo ugodno, chtoby Biljbo s Frodo jescho i rodilisj v odin denj, 22 sentiabria.

– Frodo, maljchic moj, – scazal cac-to raz Biljbo, – perebiralsia by ty co mne. Gliadish, i denj rogjdenija vmeste otmechali by.

Frodo v tu poru hodil v dorostcah. Tac hobbity zovut molodeogj v bezotvetstvennom vozraste megjdu dvadciatjiu i tridciatjiu tremia, posle chego hobbit naconecj moget schitatj sebia vzroslym.

Proshlo jescho dvenadciatj let. V Zasumcah cagjdyj god veselo otmechali dvojnoj denj rogjdenija, c etomu privycli, no liubomu bylo jasno, chto nyneshnej osenjiu gotovitsia nechto nieobychnoje. Biljbo ispolnialosj 111 let – vozrast dlia hobbita vesjma pochtennyj, da i chislo liubopytnoje, nu a Frodo gotovilsia otmetitj tridciatitreohletije – toge znamenateljnaja data – sovershennoletije po-hobbitscy.

----

Imejetsia nescoljco gypotez proiskhogjdenija sobacy, naiboleje verojatnymi jejo predcami schitajutsia volc i necotoryje vidy shacalov.

V sugjdenijah uchonyh o predcah domashnej sobacy prisutstvujut dve tochcy zrenija. Odni schitajut, chto sobacy - polifiletichescaja gruppa (proiskhodiaschaja ot nescoljcyh predcov), drugyje pridergivajutsia mnenija, chto vse sobacy proizoshli ot odnogo predca (monofiletichescaja tieorija).

----

Alecsandr Pushcyn — Zimneje utro

Moroz i solnce; denj chudesnyj!  
Jescho ty dremlesh, drug prelestnyj —  
Pora, crasavicia, prosnisj:  
Otcroj somcnuty negoj vzory  
Navstrechu severnoj Avrory,  
Zvezdoju severa javisj!

Vechor, ty pomnish, vjiuga zlilasj,  
Na mutnom nebe mgla nosilasj;  
Luna, cac blednoje piatno,  
Scvozj tuchi mrachnyje geltela,  
I ty pechaljnaja sidela —  
A nynche… pogliadi v ocno:

Pod golubymi nebesami  
Velicolepnymi covrami,  
Blestia na solnce, sneg legit;  
Prozrachnyj les odin chernejet,  
I jelj scvozj inej zelenejet,  
I rechca podo ljdom blestit.

Vsia comnata jantarnym blescom  
Ozarena. Veselym trescom  
Treschit zatoplennaja pech.  
Prijatno dumatj u legiancy.  
No znajesh: ne veletj li v sancy  
Cobylcu buruju zaprech?

Scoljzia po utrennemu snegu,  
Drug milyj, predadimsia begu  
Netoroplivogo conia  
I navestim polia pustyje,  
Lesa, nedavno stolj gustyje,  
I bereg, milyj dlia menia.

----

Lermontov M.Ju. — Rodina

Liubliu otchiznu ja, no strannoju liubovjiu!  
Ne pobedit jejo rassudoc moj.  
Ni slava, cuplennaja сrovjiu,  
Ni polnyj gordogo doverija pocoj,  
Ni teomnoj stariny zavetnyje predanjia  
Ne sheveliat vo mne otradnogo mechtanjia.  
No ja liubliu — za chto, ne znaju sam —  
Jejo stepej holodnoje molchanjie,  
Jejo lesov bezbregjnyh colyhanjie,  
Razlivy rec jejo, podobnyje moriam;  
Proseolochnym puteom liubliu scacatj v teleghe  
I, vzorom medlennym pronzaja nochi tenj,  
Vstrechatj po storonam, vzdyhaja o nochleghe,  
Drogiaschije ogni pechaljnyh derevenj;  
Liubliu dymoc spaleonnoj gjnivy,  
V stepi nochujuschij oboz  
I na holme sredj geoltoj nivy  
Chetu belejuschih bereoz.  
S otradoj, mnogym neznacomoj,  
Ja vigiu polnoje gumno,  
Izbu, pocrytuju solomoj,  
S reznymi stavniami ocno;  
I v prazdnic, vecherom rosistym,  
Smotretj do polnochi gotov  
Na pliascu s topanjiem i svistom  
Pod govor pjianyh mugichcov.

// God napisanija: 1841
