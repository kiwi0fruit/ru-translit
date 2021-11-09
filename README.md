# ru-translit

# Русская латиница от kiwi0fruit (Russcaia Latinicia)

Радикально этимологическая латиница с кучей омофонов для заимствований. Целью было приблизить правила написания к латинским и английским. Но при этом, правила чтения слов едины и не меняются от слова к слову. Ориентированы на не знающих никаких специальных правил людей. Для совместимости с кириллицей аббревиатуры строятся фонетически (как в OK - all correct).

Смысл любой русской латиницы я вижу только в использовании на указателях, латинизации имён, на выпендрёжных вывесках. Редкое использование в URL, никах, именах файлов или коментах. Ну вместо ужасного англотранслита или ужасных славянских латиниц. А вот латинизацию России я считаю плохой идеей и не приветствую.

Являет собой дуальную ASCII-only и диакритическую версии, совместимые между собой. То есть, например, слово из ASCII версии будет значить тоже самое в диакритической версии. Слова, не представимые в кириллице, не являются частью латиницы.

## TOC

* [Краткое описание](#%D0%BA%D1%80%D0%B0%D1%82%D0%BA%D0%BE%D0%B5-%D0%BE%D0%BF%D0%B8%D1%81%D0%B0%D0%BD%D0%B8%D0%B5)
* [Подробное описание](#%D0%BF%D0%BE%D0%B4%D1%80%D0%BE%D0%B1%D0%BD%D0%BE%D0%B5-%D0%BE%D0%BF%D0%B8%D1%81%D0%B0%D0%BD%D0%B8%D0%B5)
* [TODO](#todo)
* [Дополнительные примеры](#%D0%B4%D0%BE%D0%BF%D0%BE%D0%BB%D0%BD%D0%B8%D1%82%D0%B5%D0%BB%D1%8C%D0%BD%D1%8B%D0%B5-%D0%BF%D1%80%D0%B8%D0%BC%D0%B5%D1%80%D1%8B)
* [Аббревиатуры](#%D0%B0%D0%B1%D0%B1%D1%80%D0%B5%D0%B2%D0%B8%D0%B0%D1%82%D1%83%D1%80%D1%8B)
* [Набор на смартфоне](#%D0%BD%D0%B0%D0%B1%D0%BE%D1%80-%D0%BD%D0%B0-%D1%81%D0%BC%D0%B0%D1%80%D1%82%D1%84%D0%BE%D0%BD%D0%B5)
* [Включения иностранных слов без изменений](#%D0%B2%D0%BA%D0%BB%D1%8E%D1%87%D0%B5%D0%BD%D0%B8%D1%8F-%D0%B8%D0%BD%D0%BE%D1%81%D1%82%D1%80%D0%B0%D0%BD%D0%BD%D1%8B%D1%85-%D1%81%D0%BB%D0%BE%D0%B2-%D0%B1%D0%B5%D0%B7-%D0%B8%D0%B7%D0%BC%D0%B5%D0%BD%D0%B5%D0%BD%D0%B8%D0%B9)
* [Требование обратимости латиниц друг в друга - излишне](#%D1%82%D1%80%D0%B5%D0%B1%D0%BE%D0%B2%D0%B0%D0%BD%D0%B8%D0%B5-%D0%BE%D0%B1%D1%80%D0%B0%D1%82%D0%B8%D0%BC%D0%BE%D1%81%D1%82%D0%B8-%D0%BB%D0%B0%D1%82%D0%B8%D0%BD%D0%B8%D1%86-%D0%B4%D1%80%D1%83%D0%B3-%D0%B2-%D0%B4%D1%80%D1%83%D0%B3%D0%B0---%D0%B8%D0%B7%D0%BB%D0%B8%D1%88%D0%BD%D0%B5)
* [Версия для СМС](#%D0%B2%D0%B5%D1%80%D1%81%D0%B8%D1%8F-%D0%B4%D0%BB%D1%8F-%D1%81%D0%BC%D1%81)
* [Пример текста](#%D0%BF%D1%80%D0%B8%D0%BC%D0%B5%D1%80-%D1%82%D0%B5%D0%BA%D1%81%D1%82%D0%B0)
* [Пример текста ASCII-only](#%D0%BF%D1%80%D0%B8%D0%BC%D0%B5%D1%80-%D1%82%D0%B5%D0%BA%D1%81%D1%82%D0%B0-ascii-only)
* [Пример текста СМС](#%D0%BF%D1%80%D0%B8%D0%BC%D0%B5%D1%80-%D1%82%D0%B5%D0%BA%D1%81%D1%82%D0%B0-%D1%81%D0%BC%D1%81)
* [Поддержка шрифтами](#%D0%BF%D0%BE%D0%B4%D0%B4%D0%B5%D1%80%D0%B6%D0%BA%D0%B0-%D1%88%D1%80%D0%B8%D1%84%D1%82%D0%B0%D0%BC%D0%B8)


## Краткое описание

Основные написания:

| а | б | в | г | д | е      | ё      | ж | з | и | й | к    | л | м | н | о | п |
| - | - | - | - | - | ------ | ------ | - | - | - | - | ---- | - | - | - | - | - |
| a | b | v | g | d | ie/e/ė | ieo/eo | j | z | i | i | c/ck | l | m | n | o | p |

| р | с | т | у | ф | х | ц       | ч  | ш  | щ   | ъ   | ы      | ь     | э     | ю  | я  |
| - | - | - | - | - | - | ------- | -- | -- | --- | --- | ------ | ----- | ----- | -- | -- |
| r | s | t | u | f | h | c/cè/ci | ch | sh | sch | ò/î | hy/y/î | è/ì/e | e/ê/æ | iu | ia |

Все написания:

| Таблица 1    | ъе   | ъё    | ъя   | ъю   | ъи | ье   | ьё    | ья   | ью   | ьи   | ьо   |
| ------------ | ---- | ----- | ---- | ---- | -- | ---- | ----- | ---- | ---- | ---- | ---- |
|              | îe   | îeo   | îa   | îu   | î  | ìe   | ìeo   | ìa   | ìu   | ìyi  | ìo   |
| ASCII версия | yiie | yiieo | yiia | yiiu | y  | iiye | iiyeo | iiya | iiyu | iiyi | iiyo |

Каждый второй столбец - ASCII версия:

| Таблица 2                             | е     |       | ё     |     | йо    |      | я     |    | ю     |    |
| ------------------------------------- | ----- | ----- | ----- | --- | ----- | ---- | ----- | -- | ----- | -- |
| **основное написание**                | ie    |       | ieo   |     | io    |      | ia    |    | iu    |    |
| с большой буквы                       | İe    | Ye *  | İeo   | Yeo | İo    | Yo   | İa    | Ya | İu    | Yu |
| после согласной                       | e     |       | eo    |     | îo    | yiio |       |    |       |    |
| после согласной точно "мягкая" и не Ь | ė     | ie    |       |     |       |      |       |    |       |    |
| после Й или И                         | è     | ye    | èo    | yeo | ò     | yo   | à     | ya | ù     | yu |
| исключения в начале слова             | È/è   | Ye/ie |       |     |       |      |       |    |       |    |
| как в Табл. 1                         | *T.1* |       | *T.1* |     | *T.1* |      | *T.1* |    | *T.1* |    |

\* Кроме исключений типа İuliy - Iuliy.

| Таблица 3                  | э  |    | о  |    | а  |    | у  |    | ы  |    |
| -------------------------- | -- | -- | -- | -- | -- | -- | -- | -- | -- | -- |
| **основное написание**     | e  |    | o  |    | a  |    | u  |    | hy |    |
| после согласной            | ê  | ae |    |    |    |    |    |    | y  |    |
| после согласной + А        | è  | ae |    |    |    |    |    |    |    |    |
| после И                    | ê  | e  | o  |    | ä  | a  | ü  | u  |    |    |
| после Ы                    | ê  | ae | ò  | oo | à  | aa | ù  | uu |    |    |
| после согласной + Е        |    |    | ò  | oo |    |    |    |    |    |    |
| после ОАЭЁЯЕ               |    |    |    |    |    |    | ù  | uu |    |    |
| исключения после согласной | æ  | ae |    |    |    |    | ou |    | î  | y  |
| исключения в начале слова  | æ  | e  |    |    |    |    |    |    |    |    |

|                        | и  |    |                                   | й       |    |
| ---------------------- | -- | -- | --------------------------------- | ------- | -- |
| **основное написание** | i  |    | **основное написание**            | i       |    |
| после И                | ÿ  | ii | после И                           | y       |    |
| после других гласных   | ì  | ii | звучащие как в Табл. 1,2          | *T.1,2* |    |
| перед АОУЭИ            | i  | ii | перед согласной в начале слова    | y       |    |
| исключения             | ỳ  | i  | между согласными (в т.ч. в конце) | òi      | -y |
| другие исключения      | ee | ee | йи после гласной                  | iyi     |    |
|                        |    |    | исключения после ЭЕАЯ             | y       |    |

|                                | ъ         |      | ь         |      |
| ------------------------------ | --------- | ---- | --------- | ---- |
| как в Табл. 1,2,4              | *T.1,2,4* |      | *T.1,2,4* |      |
| после ШЩЧЖ                     |           |      | è         | None |
| между согласными               | ò         | -    | è         | ii   |
| после согласной в конце слова  | ò         | None | è/e \*    | ii/e |
| исключения между согласными    |           |      | ì         | ii   |
| иначе                          | -         |      | -         |      |    

\* в случае аналога открытого слога (гласная + однобуквенная-согласная + e) e на конце считается мягким знаком è. Для того, чтобы написать аналогичное Е (йэ) нужно использовать ė или ê: cone, o conė. Не распространяется на kè, gè, jè и все модиф. диакритикой согласные (см. след раздел).

|                        | к        |        |
| ---------------------- |:--------:| ------ |
| **основное написание** | c        |        |
| перед ЕЁИ              | ck       |        |
| исключения перед ЕЁИ   | k        |        |
|                        | **ц**    |        |
| **основное написание** | cè/ce \* | cii/ce |
| перед ЕЁЭИЫ            | c        |        |
| перед ОАУ              | ci       |        |
|                        | **в**    |        |
| **основное написание** | v        |        |
| исключения после ЭЕАЯ  | u        |        |

\* в случае аналога открытого слога (гласная + c + e) e на конце считается мягким знаком è. Для того, чтобы написать аналогичное ЦЕ нужно использовать ê: zaiace, o palicê. 

| Таблица 4    | ЪЭ  | ЪЫ   | ЪО  | ЪА  | ЪУ  | ЬЭ          | ЬЫ          | ЬА          | ЬУ          |
| ------------ | --  | ---- | --- | --- | --- | ----------- | ----------- | ----------- | ----------- |
|              | òhê | òhy  | òhô | òhâ | òhû | ìe/ê/èhê \* | ìyi/ỳ/èhy   | ìa/ia/èhâ   | ìu/iu/èhû   | 
| ASCII версия | -e  | -hy  | -o  | -a  | -u  | iiye/ie/e-e | iiyi/i/e-hy | iiya/ia/e-a | iiyu/iu/e-u |

\* три варианта, ибо вариантов чтения сьэ тоже три: как сье/се/сь-э.


### Значение диакритики

|   |   |
| - | - |
| İ | йотация в начале слова с заглавной буквы |
| Èè&nbsp;Ì&nbsp;ì&nbsp;Òò&nbsp;Àà&nbsp;Ùù&nbsp;Ỳỳ | альтернативное чтение, в т.ч. разбивающее диграф с предыдущей гласной |
| Êê&nbsp;Î&nbsp;î&nbsp;Ôô&nbsp;Ŷŷ&nbsp;Ââ&nbsp;Ûû&nbsp;Ŵŵ | гласные, делающие предыдущую согласную твёрдой или разбивающие диграф с предыдущей гласной (во втором случае звучание гласных Ii,Yy не становится твёрдым) |
| Ėė&nbsp;Ï&nbsp;ï&nbsp;Öö&nbsp;Ää&nbsp;Üü&nbsp;Ÿÿ | гласные, смягчающие предыдущую согласную или разбивающие диграф с предыдущей гласной (во втором случае звучание не становится йотированным) |
| Ẹẹ&nbsp;Ị&nbsp;ị&nbsp;Ọọ&nbsp;Ẏẏ&nbsp;Ạạ&nbsp;Ụụ&nbsp;Ẉẉ | альтернативное чтение предыдущей согласной (ЕеИиОоИиАаУу) |
| Éé&nbsp;Í&nbsp;í&nbsp;Óó&nbsp;Ýý&nbsp;Áá&nbsp;Úú&nbsp;Ẃẃ | ударения |
| Ēē&nbsp;Ī&nbsp;ī&nbsp;Ōō&nbsp;Ȳȳ&nbsp;Āā&nbsp;Ūū | "твёрдые" ударения |
| Ěě&nbsp;Ǐ&nbsp;ǐ&nbsp;Ǒǒ&nbsp;Ǎǎ&nbsp;Ǔǔ | "мягкие" ударения |


### Экспериментальное

1) iescheo всегда пишется как iesche. Бывшее iesche - как ieschė.
2) на конце слов заменять -ciṣm (цизм) на -cism, старый -cism заменять на -cissm
заменять -iṣm$, -iṣma$, -iṣmy$,... (все падежи всех чисел) на -ism$,...
старые -ism$ заменять -issm$
3) cтоит делать различение мужского и женского рода на конце слов в случае аналога открытого слога: tenè, cone.

|                     |      |
| ------------------- | ---- |
| сч (только [ɕː])    | sch  |
| сч ([ɕt͡ɕ] или [ɕː]) | shch |
| шч                  | shch |

Одно и то же слово с "шч" (shch) часто альтернативно читается как [ɕt͡ɕ] или [ɕː], поэтому писать так же читающиеся "сч" довольно уместно - когда раздельное чтение: rashchuvstvovalsia [rɐɕˈt͡ɕustvəvət͡sə], rashchleneniè [rəɕt͡ɕlʲɪˈnʲenʲɪje]. А вот vesnushchatyi читается либо как [vʲɪsˈnuɕːɪtɨj], либо как [vʲɪsˈnuɕt͡ɕɪtɨj]. И тут читатель сам определяет, что это [ɕt͡ɕ]-[ɕˈt͡ɕ], а не [ɕː] или [ʂt͡ɕ] (Ашчян). А вот "sch" это всегда [ɕ], [ʂ] или [ɕː].


### Новые буквы

İ Ææ  
Èè Ì ì Òò Ỳỳ Àà Ùù Ẁẁ  
Êê Î î Ôô Ŷŷ Ââ Ûû Ŵŵ  
Ėė Ï ï Öö Ÿÿ Ää Üü  
Éé Í í Óó Ýý Áá Úú Ẃẃ Ǽǽ

Ḅḅ Çç Ḍḍ Ĝĝ Ġġ Ḥḥ Ḫḫ  
Ĵ ĵ Ɉ ɉ Ḳḳ Ḷḷ Ṇṇ Ṭṭ Ṣṣ Ẓẓ Ẑẑ  
Ẹẹ Ị ị Ọọ Ẏẏ Ạạ Ụụ  
Ēē Ī ī Ōō Ȳȳ Āā Ūū  
Ěě Ǐ ǐ Ǒǒ Ǎǎ Ǔǔ

<img src="./diac.png" alt="dicritics" width="200px">

İėæḅġĝĵḥṭṣẓḳẹịọẏạụ ĖÆḄĠĜĴḤṬṢẒḲẸỊỌẎẠỤ


## TODO

1. [Recycle old descriptions](https://github.com/kiwi0fruit/ru-translit/issues/1)
2. Придумать пометку слов капсом, которые не аббревиатуры. Проработать слова в смешанном регистре.

Немного замечаний о "сч", которые могут быть полезны для обращения латиницы:  

* счлен - в остальных случаях перед согласной это всегда щ,
* щьте, щьтесь, щься - других щь{cons} не бывает,
* не бывает слов, у которых на конце щте, щтесь, щся,
* счь вообще не бывает,
* во всем корпусе текста 500 мб всего одно вхождение (сч|СЧ)\W
* во всем массиве текста 500 мб не было ни случая сч\W


## Подробное описание

Из-за этимологической и орфографической сложности освоение латиницы возможно только с помощью умного ввода, при котором происходит замена неправильно написанных слов. Например, благодаря принципу единственности прочтения, правильно и неправильно написанные слова имеют один и тот же прообраз в кириллице.

**Адаптация заимствований производится с помощью следующих обозначений:**

ḅḥ вх  
ḅh б  
bh бх  
ḍh д  
dh дх  
gh г  
gḥ гх  
kh х  
kḥ кх  
ḷh л  
lh лх  
ph ф  
pḥ пх  
rh р  
rḥ рх  
ṭh ф  
th-theo(theö)-thèo т-тео-тё  
tḥ тх  
sh ш  
sḥ сх  
ṣh с(ь)  
jh жх  
jḥ джх  
wh в  
wḥ вх  
zh ж  
ẓh чж  
zḥ зх

ng нг  
ṇg н  
ck к  
cḳ кк

cḥ-cḥè-cḥy х-хь-хи  
çh к  
çḥ чх  
ch ч (уд. ché, chá)  
çhè-chê-châ ш-ше-ша (уд. chē, chā)  
chẹ-None те-т(ь) (уд. chě)

sch щ  
sch-shch сч(только [ɕː])-сч([ɕˈt͡ɕ] или [ɕː])  
sçhè-schê-schâ сш-сше-сша (уд. schē)  
ṣch ш (уд. ṣchá)  
scḥ сх  
ṣ з  
ḅ в 

çò-cẹ-ça-cị(cẏ)-çy-çæ(çae,çê) с(съ)-се-са-си-сы-сэ (уд. çé, çá, çí, çý, çȳ)  
cè-ce(cæ-cae-cê)-cia-ceo-ci(cy)-cìa ц-це-ца-цо(цё)-ци(цы)-цья (уд. cé, ца-ciá, cí, cý, циа-ciā)  
ch-cė-cïa-cï ч-че-ча-чи (уд. çǐ, cě)  
kè(ckè)-c(k,ck)-ke(cäe,cke)-ki(ky,cki)-cky-cü(ckiu,kiu)-câe кь-к-ке-ки-кы-кю-кэ

g-ge(gäe)-geo(geö)-gèo-gæ(gae-gâe)-gi(gy)-ghy-gè(ghè)-ghìe г-ге-гео-гё-гэ-ги-гы-гь-гье (уд. gé, gá)  
ġè-gê-gêa(gîa)-gŷ ж-же-жа-жи (уд. gē, gā)  
ĝè-gẹ-gị(gẏ)-gẹa(gịa) дж-дже-джи-джа (уд. ĝé)  
dġè-dgê дж-дже

hy ы (уд. hȳ)  
hê-hâ-hï(hÿ) э-а-и (уд. hē,hā,hǐ-hý)  
NO-hẹ-hạ-hịu-hẏ(hị) г-ге-га-гю-ги (уд. ḫé, ḫí, ḫý)  
hè-ḥy-h-he-hi(ḥÿ)-ha-hiu хь-хы-х-хе-хи-ха-хю (уд. hé,há,hí,ḥȳ,ḥý)  
hìa-hìe я-е

dje дже  
j-jè-jj-je-ja(jèa)-ji-jiä-jèi ж-жь-жж-же-жа-жи-жиа-жй (уд. jí-já)
 
ġh-ġhè-ġe х-хь-хе (уд. ġé, ġē)  
ĵi-ĵa-ĵe-ĵê-ĵh ха-хи-хе-хэ-х (уд. ĵí-ĵá-ĵé-ĵē)  
i-jï-jä-jė-jö й-йи-я-е-йо (уд. jǐ-jǎ-jě)

ĵ-ĵj-jê-jâ-jî(jêe) дж-джж-дже-джа-джи (уд. jī-jā)  
jị-jạ-jẹ дзи-дзя-дзе (уд. ɉí-ɉá-ɉé)  
jì-jia цзи-цзя (уд. ɉǐ-jiá)  
ĵĵ чч  
ĵị-ĵạ-ĵẹ чи-чя-че (уд. ĵǐ-ĵǎ-ĵě)

ẓ-ẓe-ẓi(ẓy) ц-це-ци (уд. ẓá)  
ẓạ-ẓị(ẓẏ)-ẓz цза-цзы-цз (уд. ẓā)  
zạ-zị(zẏ) дза-дзы (уд. ẑá)

tṣ ц  
tẓ ц  
rz рз  
rzh рж  
rẓ ж  
sz сз  
sẓ ш  
cz кз  
cẓ ч

x-xiä кс-ксиа  
xia ся

Lỳò Лио (уд. Lỳō)  
Lyo Лё (уд. Lyó)  
Lỳo Льё (уд. Lỳǒ)  
Lyò Лыо (уд. Lyō)

qùa ка  
qùi-qùe-qüa ки-ке-кя  
qui-que-qua кви-кве-ква  
quì-què-quà куи-куэ-куа  
На конце основы склоняемых слов лучше qv. В остальных случаях лучше qu. Ну это все перед гласными.  
Aqva, Aqvy, Aqvu, aquariüm

gva-gvi гва-гви

neyrotism нейротизм, leytenant лейтенант  
Èụstaçò Юстас, Èuropa Европа, neurolog невролог, Eureka Эврека  
Austrià Австрия


## Дополнительные примеры

Уточнение мягкости: parter, partėr partier, partêr partaer.

Франсэ Françae, Франсуа Françoua  
можно было бы: pìeça, pìeçò, pìeçy, но лучше обрусеть: pìesa, pìes, pìesy  
hïstoria, hïèrarcḥ, raiyispolcom

zaiace, унц uncè uncii  
İacov Yacov, İuliy Yuliy, iod iod, iön iion, İèsus IYesus, İüda IUda, İäcov IAcov  
plohiè plohiye, Hèiuston Hiiyuston

crasnyi, miaso, liustra, pìan piiyan, podîezd podyiiezd, iesli, İesli Yesli, İuliy Yuliy, paial, sineie, poimal, proìzoshli proiizoshli, latîne latyne, oni moì / moii, on moi, vyìsckivate vyiisckivate, aero, maèstro maaestro, Ændỳ Endi, piänino piianino, vyûchite vyuuchite, drojè / droj, broshè brosh, Naste, usadèba usadiiba, culìtura culiitura, rugatèsa rugatesia, polianė polianie.

polỳèṭhir полиэфир poliaefir poliæfir, Siætl Сиэтл, dièta диета, diêlectric diaelectric diælectric  
cïao, capriccïö

ня nia nia — miaso miaso  
ния nià niya — Marià Mariya, siniè siniye  
ниа niä niia — piänino piianino, Siêtl Siietl  
нья nìa niiya — dìavol diiyavol, pìesa piiyesa  
нъя nîa nyiia — obîect obyiiect, podîezd podyiiezd  
есть iestè iestii  
на небе na nebė na nebie  
нии niÿ niii — liniÿ liniii  
ний niy niy  
ный nyi nyi, ной noi noi, най nai nai  
наи naì naii  
выи vyì vyii — vyìgryvate vyiigryvate  
выу vyù vyuu — vyüchite vyuuchite  
нио nio nio(niio)  
ньо nìo niiyo  
нё neo  
нео neò — neòn nieon, neòbychno neoobychno

сьйя sìà siiya, сйя sîà syiia, сьйс sèys sii-ys, сйс sòys s-ys


## Аббревиатуры

В латинице используются фонетическо-кириллические аббревиатуры, которые вопреки записи сокращают по звучанию. Таким образом, названия букв в аббревиатурах (а так же диграфы) будут читаться как в кириллице.

Изменения в названиях букв и диграфов (сокращения по звучанию опираются на названия букв):

* **Aa** - а
  * **IA** - я (IA., FIIA ФИЯ, RIÄ РИА RIiA, RIiÄ РИиА RIiiA)
* **Bb** - бэ
* **Cc** - це (C., CPU ЦПУ, CìA ЦА CiA, CiÄ ЦиА CiiA, CI ЦИ)
  * **Ch** - че (Ch., ChS ЧС)
* **Dd** - дэ
* **Ee** - э (была "е" в математике)
  * **IE** / **Ė** - е (IE., IEGÊ ЕГЭ IEGaE/IEG'E, OBSĖ ОБСЕ OBSIE)
  * **IEO** - ё (IEO.)
  * **Ê** - э (Ê. E., IEGÊ ЕГЭ IEGaE/IEG'E, ÊÊG ЭЭГ EEG)
* **Ff** - эф
* **Gg** - гэ (была "же" в математике)
* **Hh** - ха (H., KHL КХЛ, была "аш" в математике)
  * **Hy** - ы
* **Ii** - и
  * **Ì** - и-краткая, йот, ASCII: Y (Ì. Y.)
* **Jj** - же (была "жи" в математике)
* **Kk** - ка
* **Ll** - эль, в аббр. - "эл"
* **Mm** - эм, **Nn** - эн, **Oo** - о, **Pp** - пэ, **Qq** - ку, **Rr** - эр
* **Ss** - эс
  * **Sh** - ша (Sh., SShA США), **Sch** - ща (Sch., MSch МЩ)
* **Tt** - тэ
* **Uu** - у
  * **IU** - ю (IU. IUAR ЮАР)
* **Vv** - вэ
* **Ww** - дубль-вэ, в аббр. - "ву"
* **Xx** - икс
* **Yy** - игрек, в аббр. - "игр"
  * **Hy** - ы (Hy.)
* **Zz** - зэ (была "зет" (зэт) в математике)

Символы (комбинации) внутреннего уровня не являются самостоятельными буквами, но при этом имеют отдельные названия и входят в состав (фонетически образованных) аббревиатур - это нужно для совместимости с кириллицей.

В скобках указаны ASCII-only обозначения.

| **А**  |     **О**      |  **У**      | **Э**       |  **Ы**  |
|:------:|:--------------:|:-----------:|:-----------:|:-------:|
| A / Ä  |     O / Ö      |  U / Ü      | Ê (E/aE/'E) |   Hy    |
| **Я**  |     **Ё**      |  **Ю**      | **Е**       |  **И**  |
|   IA   |      IEO       |   IU        | IE / Ė      |  I (Ii) |
| **Б**  |     **В**      |  **Г**      | **Д**       |  **Ж**  |
|   B    |       V        |    G        |   D         |    J    |
| **З**  |     **Й**      |  **К**      | **Л**       |  **М**  |
|   Z    |       Y        |    K        |   L         |    M    |
| **Н**  |     **П**      |  **Р**      | **С**       |  **Т**  |
|   N    |       P        |    R        |   S         |    T    |
| **Ф**  |     **Х**      |  **Ц**      | **Ч**       |  **Ш**  |
|   F    |       H        | C / Cì (Ci) |   Ch        |   Sh    |
| **Щ**  |                |             |             |         |
|  Sch   |                |             |             |         |

*Буква Cc называется Це и в аббревиатуры идёт как C. И обозначает она там начальный __звук__ Ц. А все начальные звуки Ка в аббревиатурах обозначаются K. Carina Petrova => K.Petrova. Ciceron Romanov => C.Romanov.*  

SHI ШИ, SḤI СХИ (SkHI), SKHI СКХИ,  
CI ЦИ, CìA ЦА (CiA),  
KĖ КЕ (KIE), KÊ КЭ (KaE/K'E), KI КИ,  
SCHI СЧИ, ṢCHI ЩИ (ScHI), SCh СЧ, SchU ЩУ,  
CI ЦИ, CHI ЧИ, CḤI ЦХИ (CiHI),  
YÊ ЙЭ (YE), YIE ЙЕ, YI ЙИ, YA ЙА.

IEGÊ ЕГЭ (IEGaE/IEG'E), OBJ ОБЖ, CPU ЦПУ, ChS ЧС, SShA США, ÊÊG ЭЭГ (EEG), JÊK ЖЭК (JaEK/J'EK), JKH ЖКХ, NHL НХЛ, KHL КХЛ, IEKA ЕКА, FIIA ФИЯ, CERN ЦЕРН, OBSĖ ОБСЕ (OBSIE), GIBDD ГИБДД, ChIM ЧИМ, Nìu York => NY.


## Набор на смартфоне

Оптимально удобный ввод на смартфоне - с помощью проприетарных клавиатур со свайпом. Расширений для самых популярных GBoard и Swift я не обнаружил. Добавить прямо в код клавиатуры Гугла русскую латиницу можно было только если бы был единый стандарт русской латиницы. Это не реально.

Так что остаётся только использовать одну из уже существующих раскладок и импортировать собственный словарь - GBoard позволяет экспортировать и импортировать свои слова (свайп с ними работает, нужно надеяться, что нет ограничения по количеству слов...).

На данный момент я не использую свайп. Так что могу совет дать только по Windows и OpenBoard на Андроиде.

Многие использованные гласные доступны в Windows в раскладке Британская Расширенная. На Андроиде в OpenBoard большинство доступно на раскладке латиница (без языка). Недоступные на Андроиде можно добавить в пользовательский словарь на какую-нибудь комбинацию. Вьетнамская и турецкая раскладки могут быть полезны на Андроиде (на Windows вьетнамская бесполезна).


## Включения иностранных слов без изменений

У каждого слова в русской латинице для меня есть настощая форма в кириллице. Слова в латинице — лишь альтернативное отображение настоящих слов в кирилице. А настоящие слова в латинице всегда помечены специальными знаками:

Y-'cḥromosoma => Y-хромосома  
Y'-cḥromosoma => Y-хромосома  
creep'ota => creep'ота  
'that's => that's  
'citizens' => citizens'  
''tis => 'tis  
'Coca-Cola => Coca-Cola  
'Coca Cola => Coca Кола  
Coca-Col'ca => Coca-Col'ка  
Coca Col'ca => Кока Col'ка  
d'Artanìan' => д'Артаньян  
не поддерживается => полу-jeep (ибо нефиг)  

sobaca .cat dog. => собака cat dog.  

. This.  
Is . horosho. =>  
This.  
Is хорошо.

.This.  
Is . horosho. =>  
This.  
Ис horosho.

* Апостроф в начале слова делает настоящей латиницей вправо до первого пробельного символа. Имеет приоритет над апострофом в середине или конце.
* Апостроф в конце слова делает кириллицу латиницей влево до первого пробельного символа. Имеет приоритет над апострофом в середине слова.
* Апостроф в середине слова (или беспробельной последовательности) делит слово: слева настоящая латиница, справа кириллица латиницей.
* Точка в начале слова делает настоящей латиницей вправо до конца предложения.
* Точка, окруженная пробельными символами, делает настоящей латиницей до следующей такой же точки - можно несколько строк так пометить.


## Требование обратимости латиниц друг в друга - излишне

Требование обратимости латиниц друг в друга - слишком жесткое (диакритической и ASCII версий). ASCII версия не обязана дублировать диакритическую. Она лишь должна дублировать кириллицу. Так что у некоторых слов в ASCII есть несколько возможных написаний с диакритикой, но лишь одно каноническое. Например, ASCII daliishe становится dalèshe, но ASCII culiitura становится culìtura.


## Версия для СМС

Помимо полной версии и ASCII версии можно использовать и СМС версию, которая использует символы, [не уменьшающие длину сообщения](https://en.wikipedia.org/wiki/GSM_03.38#GSM_7-bit_default_alphabet_and_extension_table_of_3GPP_TS_23.038_/_GSM_03.38):

* èùìòà,ÆæÜüÖöÄä - используются в главной латинице (обратите внимание, что у большинства только нижний регистр можно использовать).

Main ASCII SMS:

Siætl Siietl Siætl, diêlectric diielectric diælectric, maèstro maaestro maèstro, piänino piianino piänino, Marià Mariya Marià, pìanyi piiyanyi pìanyi, obîect obyiiect obòiect, na nebė nebie nebie.  
iego iego iego, İego Yego Yego, İuliy Iuliy Iuliy.  
Èuropa IEuropa IEuropa, IEGÊ IEGaE IEG'E, ÊÊG EEG EEG, JÊK JaEK J'EK.  
siniÿ siniii sinìì.


## Пример текста

Alexandr Pushckin — Zimneie utro

Moroz i solnce; dene chudesnyi!  
İesche ty dremleshè, drug prelestnyi —  
Pora, crasavicia, prosnise:  
Otcroi somcnuty negoi vzory  
Navstrechu severnoi Aurory,  
Zvezdoiu severa iavise!

Vecheor, ty pomnishè, vìuga zlilase,  
Na mutnom nebė mgla nosilase;  
Luna, cac blednoie piatno,  
Scvoze tuchi mrachnyie jeltela,  
I ty pechalènaia sidela —  
A nynche… pogliadi v ocno:

Pod golubymi nebesami  
Velicolepnymi covrami,  
Blestia na solnce, sneg lejit;  
Prozrachnyi les odin cherneiet,  
I ielè scvoze inei zeleneiet,  
I rechca podo lèdom blestit.

Vsia comnata iantarnym blescom  
Ozarena. Veseolym trescom  
Treschit zatoplennaia pechè.  
Priàtno dumate u lejancki.  
No znaieshè: ne velete li v sancki  
Cobylcu buruiu zaprechè?

Scolèzia po utrennemu snegu,  
Drug milyi, predadimsia begu  
Netoroplivogo conia  
I navestim polia pustyie,  
Lesa, nedavno stole gustyie,  
I bereg, milyi dlia menia

Lermontov M.IU. — Rodina

Liubliu otchiznu ia, no strannoiu liubovìu!  
Ne pobedit ieio rassudoc moi.  
Ni slava, cuplennaia crovìu,  
Ni polnyi gordogo doverià pocoi,  
Ni teomnoi stariny zavetnyie predanìa  
Ne sheveliat vo mne otradnogo mechtanìa.  
No ia liubliu — za chto, ne znaiu sam —  
İeio stepei holodnoie molchanìe,  
İeio lesov bezbrejnyh colyhanìe,  
Razlivy rec ieio, podobnyie moriam;  
Proseolochnym puteom liubliu scacate v telege  
I, vzorom medlennym pronzaia nochi tenè,  
Vstrechate po storonam, vzdyhaia o nochlege,  
Drojaschiè ogni pechalènyh derevene;  
Liubliu dymoc spaleonnoi jnivy,  
V stepi nochuiuschiy oboz  
I na holme srede jeoltoi nivy  
Chetu beleiuschih bereoz.  
S otradoi, mnogim neznacomoi,  
İa viju polnoie gumno,  
Izbu, pocrytuiu solomoi,  
S reznymi stavniami ocno;  
I v prazdnic, vecherom rosistym,  
Smotrete do polnochi gotov  
Na pliascu s topanìem i svistom  
Pod govor pìanyh mujichcov.

// God napisanià: 1841

Piony i vasilècki vseo iesche rastut na polianė vozle derevni Peony, schitaiuscheisia bogatoi. V nei rodilsia izvestnyi piänist, pereiehavshiy v Siêtl na rabotu v companiÿ "Moì i tvoì sièsty".

Pìanyi master po proiectu sdelal mecḥanichesckiy obîect s izîanom. İesli brac ne obnarujitsia, to belyie bolidy bolèshe ne smogut vyìgryvate goncki i vyüchite svoì oshibcki.

V pìesė pro devushcu v zeleonom platìyicê vse sadilise na ladìyi i plyli po recke. No tut iz lesa vyshel Gẹorĝè Maximus, cone v palèto i rvanyh jêensah, cotoryi cogo-to obîsckival, i pricazal vsem mytèsia, gotovite bulìon i tancevate jîgu. Znachit snova pìeom do lysyh aqualangistov.

Prepodobnyi Bayes podkinul igralènyie costi. Vypalo shestè, znachit iemu prideotsia mazate iod na ranu.

Mær nebolèshogo gorodishcki otcryl tabliciu exelia i vozmutilsia cenoi novogo excavatora. Aj eczêma snova stala iego bespocoìte. Oh uj eta pocupca vechnogo dvigatelia v proshlom godu! A tac je pocupca aeroplana-ecranoleota dlia Ændỳ. İesli tac poideot i dalèshe, to biudgêtu prideotsia hudo.

V etom vidė phraṣa ot A do İa nachinaiet vygliadete sovsem po-drugomu. Seichas scheotca novaia, no pozje ona stanet staraia. Chernysh liubit cogda iego cheshut ieiu. İeoj coliuchiy i pohoj na neio.

Sḥod mestnyh jitelei indiyscoi derevni sikḥov reshal chto je delate s otḥodami companiÿ "Caligula Gai İuliy Cæṣare" (lat. Caligula Gaius Iulius Caesar). Odin iz prisutstvuiuschih nosil hoholoc na golovė. On i nasheol vyhod iz situatciÿ.

"Cto s mechom c nam prideot, tot ot mecha i..." - ne smog dogovorite starshiy mecḥanic Vasiliy.

Liubimcem Bilìbo byl iunyi Frodo Bæggins. Cogda Bilìbo stucnulo devianosto deviate, on vdrug usynovil sirotu Frodo, sdelal svoìm naslednicom i predlojil pereselitèsia v Zasumcki. Tut uj vse nadejdy Dericule-Bægginsov, davno s vojdelenièm posmatrivavshih na usadèbu, ruhnuli oconchatelèno.

Sluchaiu bylo ugodno, chtoby Bilìbo s Frodo iesche i rodilise v odin dene, 22 sentiabria.

– Frodo, malèchic moi, – scazal cac-to raz Bilìbo, – perebiralsia by ty co mne. Gliadishè, i dene rojdenià vmeste otmechali by.

Frodo v tu poru hodil v dorostcah. Tac hobbity zovut molodeojè v bezotvetstvennom vozraste mejdu dvadciatìu i tridciatìu tremia, posle chego hobbit naconece mojet schitate sebia vzroslym.

Proshlo iesche dvenadciate let. V Zasumcah cajdyi god veselo otmechali dvoinoi dene rojdenià, c etomu privycli, no liubomu bylo iasno, chto nyneshnei osenìu gotovitsia nechto neòbychnoie. Bilìbo ispolnialose 111 let – vozrast dlia hobbita vesèma pochtennyi, da i chislo liubopytnoie, nu a Frodo gotovilsia otmetite tridciatitreohletiè – toje znamenatelènaia data – sovershennoletiè po-hobbitscki.

Imeietsia nescolèco hẏpotheṣ proìsḥojdenià sobacki, naìboleie veroiatnymi ieio predcami schitaìutsia volc i necotoryie vidy shacalov.

V sujdeniàh ucheonyh o predcah domashnei sobacki prisutstvuiut dve tochcki zrenià. Odni schitaiut, chto sobacki - polỳphỳletichescaia gruppa (proìsḥodiaschaia ot nescolèckih predcov), drugiè priderjivaiutsia mnenià, chto vse sobacki proìzoshli ot odnogo predca (monophỳletichescaia theorià).


## Пример текста ASCII-only

Alexandr Pushckin — Zimneie utro

Moroz i solnce; dene chudesnyi!  
Yesche ty dremlesh, drug prelestnyi —  
Pora, crasavicia, prosnise:  
Otcroi somcnuty negoi vzory  
Navstrechu severnoi Aurory,  
Zvezdoiu severa iavise!

Vecheor, ty pomnish, viiyuga zlilase,  
Na mutnom nebie mgla nosilase;  
Luna, cac blednoie piatno,  
Scvoze tuchi mrachnyie jeltela,  
I ty pechaliinaia sidela —  
A nynche… pogliadi v ocno:

Pod golubymi nebesami  
Velicolepnymi covrami,  
Blestia na solnce, sneg lejit;  
Prozrachnyi les odin cherneiet,  
I iele scvoze inei zeleneiet,  
I rechca podo liidom blestit.  

Vsia comnata yantarnym blescom  
Ozarena. Veseolym trescom  
Treschit zatoplennaia pech.  
Priyatno dumate u lejancki.  
No znaiesh: ne velete li v sancki  
Cobylcu buruiu zaprech?

Scolezia po utrennemu snegu,  
Drug milyi, predadimsia begu  
Netoroplivogo conia  
I navestim polia pustyie,  
Lesa, nedavno stole gustyie,  
I bereg, milyi dlia menia.

Lermontov M.IU. — Rodina

Liubliu otchiznu ia, no strannoiu liuboviiyu!  
Ne pobedit ieio rassudoc moi.  
Ni slava, cuplennaia croviiyu,  
Ni polnyi gordogo doveriya pocoi,  
Ni teomnoi stariny zavetnyie predaniiya  
Ne sheveliat vo mne otradnogo mechtaniiya.  
No ia liubliu — za chto, ne znaiu sam —  
Yeio stepei holodnoie molchaniiye,  
Yeio lesov bezbrejnyh colyhaniiye,  
Razlivy rec ieio, podobnyie moriam;  
Proseolochnym puteom liubliu scacate v telege  
I, vzorom medlennym pronzaia nochi tene,  
Vstrechate po storonam, vzdyhaia o nochlege,  
Drojaschiye ogni pechaliinyh derevene;  
Liubliu dymoc spaleonnoi jnivy,  
V stepi nochuiuschiy oboz  
I na holme srede jeoltoi nivy  
Chetu beleiuschih bereoz.  
S otradoi, mnogim neznacomoi,  
Ya viju polnoie gumno,  
Izbu, pocrytuiu solomoi,  
S reznymi stavniami ocno;  
I v prazdnic, vecherom rosistym,  
Smotrete do polnochi gotov  
Na pliascu s topaniiyem i svistom  
Pod govor piiyanyh mujichcov.

// God napisaniya: 1841

Piony i vasiliicki vseo iesche rastut na polianie vozle derevni Peony, schitaiuscheisia bogatoi. V nei rodilsia izvestnyi piianist, pereiehavshiy v Siietl na rabotu v companiii "Moii i tvoii siyesty".

Piiyanyi master po proiectu sdelal mekhanichesckiy obyiiect s izyiianom. Yesli brac ne obnarujitsia, to belyie bolidy boliishe ne smogut vyiigryvate goncki i vyuuchite svoii oshibcki.

V piiyesie pro devushcu v zeleonom platiiyicie vse sadilise na ladiiyi i plyli po recke. No tut iz lesa vyshel Djeordj Maximus, cone v paliito i rvanyh djinsah, cotoryi cogo-to obysckival, i pricazal vsem mytesia i gotovite buliiyon. Znachit snova piiyeom do lysyh aqualangistov.

Prepodobnyi Bayes podkinul igraliinyie costi. Vypalo shestii, znachit iemu prideotsia mazate iod na ranu.

Maer neboliishogo gorodishcki otcryl tabliciu exelia i vozmutilsia cenoi novogo excavatora. Aj eczaema snova stala iego bespocoiite. Oh uj eta pocupca vechnogo dvigatelia v proshlom godu! A tac je pocupca aeroplana-ecranoleota dlia Endi. Yesli tac poideot i daliishe, to biudjetu prideotsia hudo.

V etom vidie phraza ot A do IA nachinaiet vygliadete sovsem po-drugomu. Seichas scheotca novaia, no pozje ona stanet staraia. Chernysh liubit cogda iego cheshut ieiu. Yeoj coliuchiy i pohoj na neio.

Skhod mestnyh jitelei indiyscoi derevni sikkhov reshal chto je delate s otkhodami companiii "Caligula Gai Iuliy Caezare" (lat. Caligula Gaius Iulius Caesar). Odin iz prisutstvuiuschih nosil hoholoc na golovie. On i nasheol vyhod iz situatciii.

"Cto s mechom c nam prideot, tot ot mecha i..." - ne smog dogovorite starshiy mekhanic Vasiliy.

Liubimcem Biliibo byl iunyi Frodo Baeggins. Cogda Biliibo stucnulo devianosto deviate, on vdrug usynovil sirotu Frodo, sdelal svoiim naslednicom i predlojil pereselitesia v Zasumcki. Tut uj vse nadejdy Dericule-Baegginsov, davno s vojdeleniyem posmatrivavshih na usadiibu, ruhnuli oconchateliino.

Sluchaiu bylo ugodno, chtoby Biliibo s Frodo iesche i rodilise v odin dene, 22 sentiabria.

– Frodo, malechic moi, – scazal cac-to raz Biliibo, – perebiralsia by ty co mne. Gliadish, i dene rojdeniya vmeste otmechali by.

Frodo v tu poru hodil v dorostcah. Tac hobbity zovut molodeoj v bezotvetstvennom vozraste mejdu dvadciatiiyu i tridciatiiyu tremia, posle chego hobbit naconece mojet schitate sebia vzroslym.

Proshlo iesche dvenadciate let. V Zasumcah cajdyi god veselo otmechali dvoinoi dene rojdeniya, c etomu privycli, no liubomu bylo iasno, chto nyneshnei oseniiyu gotovitsia nechto neoobychnoie. Biliibo ispolnialose 111 let – vozrast dlia hobbita vesiima pochtennyi, da i chislo liubopytnoie, nu a Frodo gotovilsia otmetite tridciatitreohletiye – toje znamenatelenaia data – sovershennoletiye po-hobbitscki.

Imeietsia nescoleco gypothez proiiskhojdeniya sobacki, naiiboleie veroiatnymi ieio predcami schitaiutsia volc i necotoryie vidy shacalov.

V sujdeniyah ucheonyh o predcah domashnei sobacki prisutstvuiut dve tochcki zreniya. Odni schitaiut, chto sobacki - poliphiletichescaia gruppa (proiiskhodiaschaia ot nescoleckih predcov), drugiye priderjivaiutsia mneniya, chto vse sobacki proiizoshli ot odnogo predca (monophiletichescaia thieoriya).


## Пример текста СМС

Alexandr Pushckin — Zimneie utro

Moroz i solnce; dene chudesnyi!  
Yesche ty dremleshè, drug prelestnyi —  
Pora, crasavicia, prosnise:  
Otcroi somcnuty negoi vzory  
Navstrechu severnoi Aurory,  
Zvezdoiu severa iavise!

Vecheor, ty pomnishè, vìuga zlilase,  
Na mutnom nebie mgla nosilase;  
Luna, cac blednoie piatno,  
Scvoze tuchi mrachnyie jeltela,  
I ty pechalènaia sidela —  
A nynche… pogliadi v ocno:

Pod golubymi nebesami  
Velicolepnymi covrami,  
Blestia na solnce, sneg lejit;  
Prozrachnyi les odin cherneiet,  
I ielè scvoze inei zeleneiet,  
I rechca podo lèdom blestit.

Vsia comnata iantarnym blescom  
Ozarena. Veseolym trescom  
Treschit zatoplennaia pechè.  
Priàtno dumate u lejancki.  
No znaieshè: ne velete li v sancki  
Cobylcu buruiu zaprechè?

Scolèzia po utrennemu snegu,  
Drug milyi, predadimsia begu  
Netoroplivogo conia  
I navestim polia pustyie,  
Lesa, nedavno stole gustyie,  
I bereg, milyi dlia menia

Lermontov M.IU. — Rodina

Liubliu otchiznu ia, no strannoiu liubovìu!  
Ne pobedit ieio rassudoc moi.  
Ni slava, cuplennaia crovìu,  
Ni polnyi gordogo doverià pocoi,  
Ni teomnoi stariny zavetnyie predanìa  
Ne sheveliat vo mne otradnogo mechtanìa.  
No ia liubliu — za chto, ne znaiu sam —  
Yeio stepei holodnoie molchanìe,  
Yeio lesov bezbrejnyh colyhanìe,  
Razlivy rec ieio, podobnyie moriam;  
Proseolochnym puteom liubliu scacate v telege  
I, vzorom medlennym pronzaia nochi tenè,  
Vstrechate po storonam, vzdyhaia o nochlege,  
Drojaschiè ogni pechalènyh derevene;  
Liubliu dymoc spaleonnoi jnivy,  
V stepi nochuiuschiy oboz  
I na holme srede jeoltoi nivy  
Chetu beleiuschih bereoz.  
S otradoi, mnogim neznacomoi,  
Ya viju polnoie gumno,  
Izbu, pocrytuiu solomoi,  
S reznymi stavniami ocno;  
I v prazdnic, vecherom rosistym,  
Smotrete do polnochi gotov  
Na pliascu s topanìem i svistom  
Pod govor pìanyh mujichcov.

// God napisanià: 1841

Piony i vasilècki vseo iesche rastut na polianie vozle derevni Peony, schitaiuscheisia bogatoi. V nei rodilsia izvestnyi piänist, pereiehavshiy v Siætl na rabotu v companìì "Moì i tvoì sièsty".

Pìanyi master po proiectu sdelal mekhanichesckiy obòiect s izòianom. Yesli brac ne obnarujitsia, to belyie bolidy bolèshe ne smogut vyìgryvate goncki i vyüchite svoì oshibcki.

V pìesie pro devushcu v zeleonom platìyicie vse sadilise na ladìyi i plyli po recke. No tut iz lesa vyshel 'George Maximus, cone v palèto i rvanyh djeensah, cotoryi cogo-to obysckival, i pricazal vsem mytèsia, gotovite bulìon i tancevate djigu. Znachit snova pìeom do lysyh aqualangistov.

Prepodobnyi Bayes podkinul igralènyie costi. Vypalo shestè, znachit iemu prideotsia mazate iod na ranu.

Mær nebolèshogo gorodishcki otcryl tabliciu exelia i vozmutilsia cenoi novogo excavatora. Aj eczema snova stala iego bespocoìte. Oh uj eta pocupca vechnogo dvigatelia v proshlom godu! A tac je pocupca aeroplana-ecranoleota dlia Ændi. Yesli tac poideot i dalèshe, to biudjetu prideotsia hudo.

V etom vidie phraza ot A do Ya nachinaiet vygliadete sovsem po-drugomu. Seichas scheotca novaia, no pozje ona stanet staraia. Chernysh liubit cogda iego cheshut ieiu. Yeoj coliuchiy i pohoj na neio.

Skhod mestnyh jitelei indiyscoi derevni sikkhov reshal chto je delate s otkhodami companìì "Caligula Gai Iuliy Cæzare" (lat. Caligula Gaius Iulius Caesar). Odin iz prisutstvuiuschih nosil hoholoc na golovie. On i nasheol vyhod iz situatcìì.

"Cto s mechom c nam prideot, tot ot mecha i..." - ne smog dogovorite starshiy mekhanic Vasiliy.

Liubimcem Bilìbo byl iunyi Frodo Bæggins. Cogda Bilìbo stucnulo devianosto deviate, on vdrug usynovil sirotu Frodo, sdelal svoìm naslednicom i predlojil pereselitèsia v Zasumcki. Tut uj vse nadejdy Dericule-Bægginsov, davno s vojdelenièm posmatrivavshih na usadèbu, ruhnuli oconchatelèno.

Sluchaiu bylo ugodno, chtoby Bilìbo s Frodo iesche i rodilise v odin dene, 22 sentiabria.

– Frodo, malèchic moi, – scazal cac-to raz Bilìbo, – perebiralsia by ty co mne. Gliadishè, i dene rojdenià vmeste otmechali by.

Frodo v tu poru hodil v dorostcah. Tac hobbity zovut molodeojè v bezotvetstvennom vozraste mejdu dvadciatìu i tridciatìu tremia, posle chego hobbit naconece mojet schitate sebia vzroslym.

Proshlo iesche dvenadciate let. V Zasumcah cajdyi god veselo otmechali dvoinoi dene rojdenià, c etomu privycli, no liubomu bylo iasno, chto nyneshnei osenìu gotovitsia nechto neòbychnoie. Bilìbo ispolnialose 111 let – vozrast dlia hobbita vesèma pochtennyi, da i chislo liubopytnoie, nu a Frodo gotovilsia otmetite tridciatitreohletiè – toje znamenatelènaia data – sovershennoletiè po-hobbitscki.

Imeietsia nescolèco gypothez proìskhojdenià sobacki, naìboleie veroiatnymi ieio predcami schitaìutsia volc i necotoryie vidy shacalov.

V sujdeniàh ucheonyh o predcah domashnei sobacki prisutstvuiut dve tochcki zrenià. Odni schitaiut, chto sobacki - poliphiletichescaia gruppa (proìsḥodiaschaia ot nescolèckih predcov), drugiè priderjivaiutsia mnenià, chto vse sobacki proìzoshli ot odnogo predca (monophiletichescaia theorià).


## Поддержка шрифтами

Понять какие шрифты поддерживают письмо на этой латинице можно с помощью такого тестового фрагмента, который содержит всю диакритику, кроме используемой только в ударениях:

> İ Ėė Ææ  
> Èè Ì ì Òò Ỳỳ Àà Ùù  
> Êê Î î Ôô Ŷŷ Ââ Ûû Ŵŵ  
> Ï ï Öö Ää Üü  
> Ḅḅ Çç Ḍḍ Ĝĝ Ġġ Ḥḥ  
> Ĵ ĵ Ḳḳ Ḷḷ Ṇṇ Ṭṭ Ṣṣ Ẓẓ  
> Ẹẹ Ị ị Ọọ Ẏẏ Ạạ Ụụ
> 
> Vecheor, ty pomnishè, vìuga zlilase, Na mutnom nebė mgla nosilase; Luna, cac blednoie piatno, Scvoze tuchi mrachnyie jeltela, I ty pechalènaia sidela — A nynche… pogliadi v ocno: Ḅaḅylon

Следует обратить внимание, что все точки стоят на правильных местах. А так же оценить общую эстетику шрифта по фрагменту стиха. Прошли отбор:

* _Serif_: STIX Two Text, Source Serif Pro, Merriweather, Crimson Text, Crimson Pro, EB Garamond, Cormorant Garamond, Cormorant SC, Gentium Basic, Gentium Book Basic, Yrsa, Alegreya, IBM Plex Serif, Noto Serif, Roboto Slab, Cardo, Tinos, Taviraj, Gelasio, Judson, Podkova, Castoro, Hepta Slab, Bodoni Moda, Gowun Batang, Rasa, Andada Pro, Bona Nova, Manuale, Besley, Brygada 1918, Piazzolla
* _Sans-Serif_: Roboto, Open Sans, Noto Sans, Source Sans Pro, Fira Sans, Merriweather Sans, Montserrat, Inter, Nunito, Nunito Sans, IBM Plex Sans, Arimo, Mulish, Varela Round, Kanit, Signika, Encode Sans, Encode Sans SC, Archivo, Recursive, Gothic A1, Faustina, Saira, Lexend, Lexend Deca, Bai Jamjuree, Andika, Andika New Basic, Niramit, Amiko, K2D,  Livvic, KoHo, Varta, Trispace
* _Monospace_: Roboto Mono, Cousine, Inconsolata, Source Code Pro, IBM Plex Mono
* _Handwriting_: Great Vibes, Mali, Itim, Charm, Yomogi, Sedgwick Ave, Sedgwick Ave Display, Dekko
* _Display_: Arima Madurai, Gluten, Yeseva One, Chonburi, Calistoga, Bellota, Bellota Text, Goldman, Srisakdi, Viaoda Libre

