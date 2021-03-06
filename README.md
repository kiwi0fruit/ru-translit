# ru-translit (kiwi0fruit's)

# Русская латиница "Латинский симулякр"

Радикально этимологическая латиница с кучей омофонов. Целью было приблизить правила написания к латинским и английским. Но при этом, правила чтения слов едины и не меняются от слова к слову. Для совместимости с кириллицей аббревиатуры строятся фонетически (как в OK - all correct).

Из-за этимологической и орфографической сложности освоение латиницы возможно только с помощью умного воода, при котором происходит замена неправильно написанных слов. Например, благодаря принципу единственности прочтения, правильно и неправильно написанные слова имеют один и тот же прообраз в кириллице.

Являет собой дуальную ASCII-only и диакритическую версии, совместимые между собой. То есть, например, слово из ASCII версии будет значить тоже самое в диакритической версии. Слова, не представимые в кириллице, не являются частью латиницы.

* Латиница обратимая,
* Сознательное исключение буквы Kk где возможно,
* Диакритическая версия подразумевает эргономичный ввод букв с помощью раскладки клавиатуры [US-International](https://en.wikipedia.org/wiki/US_international_keyboard#US-International), а знаки ударения вводятся с помощью [EurKEY](https://en.wikipedia.org/wiki/EurKEY). То есть, это две раскладки для английского языка. Более того, раскладку для ударений можно и не ставить,
* Минимизация использования буквы Jj в конце слов.

Новые буквы: áàóòýỳúùéèìíç (13 - ÁÀÓÒÝỲÚÙÉÈÌÍÇ). Ударения: âǎôǒêěûǔîŵǐŷy̌ãõẽũỹĩ ÂǍÔǑÊĚÛǓÎŴǏŶY̌ÃÕẼŨỸĨ. То есть, алфавит состоит из 26 букв базовой латиницы, Çç и 5 диакритических знаков (акут, гравис, и три ударения: крышка, гачек, тильда). 5 диакритических знаков могут быть только над гласными. *Важно наличие трёх типов ударений. А что это именно крышка, гачек и тильда не обязательно*.

[Предыдущая версия](su_en.md) для справки о преемственности.


* [Краткое описание](#%D0%BA%D1%80%D0%B0%D1%82%D0%BA%D0%BE%D0%B5-%D0%BE%D0%BF%D0%B8%D1%81%D0%B0%D0%BD%D0%B8%D0%B5)
* [Подробное описание](#%D0%BF%D0%BE%D0%B4%D1%80%D0%BE%D0%B1%D0%BD%D0%BE%D0%B5-%D0%BE%D0%BF%D0%B8%D1%81%D0%B0%D0%BD%D0%B8%D0%B5)
* [Дополнительные примеры](#%D0%B4%D0%BE%D0%BF%D0%BE%D0%BB%D0%BD%D0%B8%D1%82%D0%B5%D0%BB%D1%8C%D0%BD%D1%8B%D0%B5-%D0%BF%D1%80%D0%B8%D0%BC%D0%B5%D1%80%D1%8B)
* [Ударения](#%D1%83%D0%B4%D0%B0%D1%80%D0%B5%D0%BD%D0%B8%D1%8F)
* [Про диграфы cz и gz](#%D0%BF%D1%80%D0%BE-%D0%B4%D0%B8%D0%B3%D1%80%D0%B0%D1%84%D1%8B-cz-%D0%B8-gz)
* [Аббревиатуры](#%D0%B0%D0%B1%D0%B1%D1%80%D0%B5%D0%B2%D0%B8%D0%B0%D1%82%D1%83%D1%80%D1%8B)
* [Набор на смартфоне](#%D0%BD%D0%B0%D0%B1%D0%BE%D1%80-%D0%BD%D0%B0-%D1%81%D0%BC%D0%B0%D1%80%D1%82%D1%84%D0%BE%D0%BD%D0%B5)
* [Включения иностранных слов без изменений](#%D0%B2%D0%BA%D0%BB%D1%8E%D1%87%D0%B5%D0%BD%D0%B8%D1%8F-%D0%B8%D0%BD%D0%BE%D1%81%D1%82%D1%80%D0%B0%D0%BD%D0%BD%D1%8B%D1%85-%D1%81%D0%BB%D0%BE%D0%B2-%D0%B1%D0%B5%D0%B7-%D0%B8%D0%B7%D0%BC%D0%B5%D0%BD%D0%B5%D0%BD%D0%B8%D0%B9)
* [Требование обратимости латиниц друг в друга - излишне](#%D1%82%D1%80%D0%B5%D0%B1%D0%BE%D0%B2%D0%B0%D0%BD%D0%B8%D0%B5-%D0%BE%D0%B1%D1%80%D0%B0%D1%82%D0%B8%D0%BC%D0%BE%D1%81%D1%82%D0%B8-%D0%BB%D0%B0%D1%82%D0%B8%D0%BD%D0%B8%D1%86-%D0%B4%D1%80%D1%83%D0%B3-%D0%B2-%D0%B4%D1%80%D1%83%D0%B3%D0%B0---%D0%B8%D0%B7%D0%BB%D0%B8%D1%88%D0%BD%D0%B5)
* [Пример текста](#%D0%BF%D1%80%D0%B8%D0%BC%D0%B5%D1%80-%D1%82%D0%B5%D0%BA%D1%81%D1%82%D0%B0)


### Краткое описание

**UPD** еще не записаные [исправления латиницы](https://github.com/kiwi0fruit/ru-translit/issues/1).

Смягчение гласных делается акутом (áú), сделать, наоборот твёрдыми - грависом (èì). Буквы Кк и Цц даются с помощью Cc: твердые - Кк, мягкие - Цц. У сочетаний th,ch,j,g,dj,dg можно изменить звучание с помощью букв ò,èìóàùỳ, а у букв b,w - с помощью èìóàùỳ. В альтернативных этимологических вариантах приоритет у латинской этимологии, следом - английской. Если ни та, ни эта этимология, то используется изначальный язык, ближайший к латыни. Например: кинематограф - kinematograph (нем.) - cinématographe (фр.) => cìnematograph.

ъ - ò, qh (не после согл.)  
ь - é, qh  

а - a, à (после букв с изм. звуч.), à (иногда после гласн.)  
о - o, ó (после букв с изм. звуч.), ò (иногда после гласн.)  
у - u, ù, ù, w (этимлг. изм. звуч.)  

е - je, e (после согл.), é (после "й" / после i в оконч.), è (после букв с изм. звуч.)  
ё - jeo, éo, éo, èo, jo (после "е")  

ю - ju, ú (после согл., "й" / после i в оконч.)  
я - ja, á  

и - i, í (после гласн. кроме иы / после йь / загл. в нач. слова), ì (этимлг. после Кк / после букв с изм. звуч.), y (после Кк / этимлг.), ý (этимлг.), ỳ (этимлг. после букв с изм. звуч.)  
ы - ỳ, y (когда рядом только согл. звуки), ì (этимлг.), òi (этимлг. после Бб)  
э - e, è (после согл. / иногда после гласн.), ae (этимлг. / после Бб)  
й - j, i (после гласных кроме ыи не перед гласн. или "й"), ji (перед ауэ), y (этимлг.)  

б - b,  
в - v, этимлг.: b (изм. звуч.), bh, w, wh  
г - g, gh (перед ъьз / этимлг.)  
д - d,  
ж - gz, gj (этимлг.), zh (этимлг. изм. звуч.),  
з - z,  
к - c, этимлг.: k, ck, qù, qú  
л - l,  
м - m,  
н - n,  
п - p,  
р - r, rh (этимлг.)  
с - s,  
т - t, th (этимлг.)  
ф - f, ph (этимлг.), th (изм. звуч. этимлг.)  
х - h, ch (изм. звуч. этимлг.)  
ц - c, cz (не перед гласн.), этимлг.: cz, tz, czz  
ч - ch,  
ш - sh,  
щ - sch  
кв - cv, qv (этимлг.)  
кс - cs, x (этимлг.)  
кз - ckz, xz (этимлг.)  
дж: этимл. изм. звуч.: j, g, dj, dg  
чж: zh (этимлг.)


## Подробное описание

Полезно помнить, что после согласных: ò/ъ и é/ь.

*После слэша дано написание в ASCII-only версии. Требования этимологии распространяются только на основу слова.*

Я поленился дописать в таблицу чж/zh, ж/zhò по тому же принципу альтернативного прочтения: zha/чжа, zhà/жа.

|     |     |     |     |
| --- | --- | --- | --- |
| г | gh | перед зьъ или где этимология требует h | ghippopotam, zighzag, Buchghàlter / Bukhghalter, Alighjeri Алигьери, adgheziá |
| гэ | gae | всегда |     |
| гы | gy | всегда |     |
| ж | gz | всегда перед ьъ | dgzé / dgzj джь |
| жз | gjz |     |     |
| ж | gj | где этимология требует g/ж или j/ж - но не после d или перед h | gjurnal, degjavú дежавю, Gjeorgj Жорж |
| дж | dg[èìỳò] / dgj | где этимология требует dg | búdgèt / byudgjet, poridgò поридж, podgzidal, ogzidal, podgibaté, zagibaté, podgon, Sandgerdi / Сандгерди |
| дж | g[èìỳò] / gjh | где этимология требует g - но не после d | Gèorgò / Gjhyorgjh Джордж, Gìuljetta / Gjhuljetta, Gìovanni / Gjhovanni, gìn / gjhin / джин, Gèòrgò / Gjheorgjh / Джеордж, Energỳ / Energjhy Энерджи |
| дж | jae, j[èìòóàùỳh] / jh | где этимология требует - но не после d,g | Jaeims, Jàems / Jhaaems Джаэмс, Jàrmush, jìnsy, Jaeck, Jèrsý, hajjò / hajjh, jóker, ỳjỳd / yyjhyd ыджыд - альтернативный вариант |
| дж | djae, dj[èìòóàùỳh] / djh | где этимология требует dj |     |
| ж | z | после ж/gz |     | gzugzzit |
| ж | j | после ж/gj |     |
| джж | jjò / jjh |   | hajjò / hajjh |
| бэ | bae | всегда | Baecon |
| бы | bòi / by | где этимология требует i | obòisc |
| в | bh | перед согласными или в конце слова, где этимология требует b | febhralé |
| в | b[èìóàùỳ] / bh | перед гласными где этимология требует b | sýmból / syimbhol, Bỳzantiá / Bhyzantija, Bàbỳlon, djaból |
| р | rh | где этимология требует rh | rhythm |
| т | tò / th | перед з | otòzyv / othzyv |
| т | th | где этимология требует th, "тъ" с использованием th не бывает | mathematica, theoriá, theologiá, Theodor, orthogonalényj |
| ф | th[èìòóàùỳ] / fh | где этимология требует th | Thèodor / Fhyodor Фёдор, orthógraphiá орфография, scythò скиф, scyth - скит |
| ф | ph | где этимология требует ph | telephon |
| х | ch[èìòóàùỳ] / kh | где этимология требует ch или kh | chìmera / khimera, chór, Czúrichò / Czyurikh Цюрих |
| х | ch[\c][èìóàùỳ] / kh[\c][eioauy] | перед согласной+гласной где этимология требует ch или kh | Chrìstos, Lochnèss / Lokhness, Lochònèss / Lokhnaess, Lachònaes / Lokhnaess, Lochénèss / Lochnaess Лочнэс, buchghàlter, chtónichescyj хтонический, chtèonichescyj хтёнический |
| х | òh / kh | после согласных | sòhod / skhod |
| х | òch / kh | после "с/s" когда этимология требует ch | rasòchìmera / raskhimera расхимера |
| ч | c | перед ч | capricchio |
| щ | sch (shch) |     |     |
| сч | sch (sçh / ssch) |     | вторые варианты нужны только при выходе за словарь известных слов    |
| ссч | ssçh / sssch |     |     |
| шч | shéch / shjch |      | vesnushéchat |
| шьч | запрещен |     |     |
| в | wh | когда этимология требует wh | Whaitran Вайтран |
| у | w[èìóàỳ] / wu,ww | перед гласными когда этимология требует w - кроме уу | Wótson / Wuotson Уотсон, Wèst / Wuest Уэст, brawùzer / brawwzer браузер, ударение: brawũzer |
| в | w | когда этимология требует w | Watson Ватсон, Watt Ватт, Wurst, Wuàt / Wuuatt Вуатт |
|     |     | *Специальные комбинации, чьё звучание изменяется буквами èìòóàùỳ: b,w,th,ch,j,g,dj,dg, звучание **b,w НЕ** меняется буквой Òò.*    | *После b,w,th,ch,j,g,dj,dg - Óó не смягчает, а полностью меняет звучание предыдущей буквы. Как и после Cc.* |
|     |     |     |     |
|     |     |     |     |
| к | ck | когда этимология требует ck или ch | hockei - исключение, Mackiavelli, Maickl, за компанию: Mishelé, Michàelé |
| к | k | когда этимология требует k | Keniá, kefir, koboljd, koala, karate |
| кс | x | где этимология требует x, но только не на стыке морфем | taxi, Xeniá |
| кз | xz | где этимология требует x, но только не на стыке морфем | exzamen |
| кз | ckz | иначе | eckzema |
| кх | ckh |    | sickh |
| кв | qv | когда этимология требует q | aqvarium |
| ки | cì / cki | где этимология требует ci | cìno / ckino кино, cìnematograph |
| ки | cy |     | recy, reca |
| ке | cè / cke |     | ocèan / ockean, cèntavr / ckentavr, v recè / v recke |
| кы | cky |     | alenéckyj |
| кэ | cae | всегда |       |
| к | c | иначе |     |
| к[иеяё] | qú[ieao] / qk[ie],qky[ao] | когда этимология требует qu | marqúiz, teqúila, banqúir, qúilé, maqúet, piqúet, liqúor, anqúeta |
| к[оа] | qù[oa] / qk[oa] | когда этимология требует qu | qùarantin |
|     |     | *Примеры:* | ocèan, cèntavr, cìno кино, cìnematograph, cyber, cysta киста, cìrasa кираса, ascèt аскет, ancker анкер, scèptic скептик, Cyrill, Cypr, scythò, cyt кит, cynolog |
|     |     |     |     |
|     |     |     |     |
| -ция | -tziá / -tzija | где русское словообразование эквивалентно латинскому "-ia", превращающемуся в "tia". Все русские -ция с этим же смыслом так же надо причесать под эту форму | fractziá, militziá, militzai, politziá, instructziá |
| ц | tz | где этимология требует t, но не требует "c". Тут много какие латинские суффиксы могут быть: -tiō, -tion | ratzion, tzundere, tzigan |
| цц | tzz | когда этимология требует t, но не требует Cc |     |
| ц | cz / cz | где этимология требует z, но не требует t | Ponczi, Czúrichò / Czyurikh Цюрих |
| цц | czz | когда этимология требует Cc или z, но не требует t | piczza |
| ци | cý / cyi | где этимология требует Yy, но не на конце слова | cýan / cyian циан, cýcl |
| цы | ci | в словах-исключениях | cipléonoc |
| цы | cý / cyi | иначе | otcý / otcyi |
| ц[иеё] | c[ie], céo / czyo | иначе | cedité, otcedité, accent, Ciceron, Cezaré, Céos / Czyos Цёс |
| ц[аоу] | c[áóú] / cy[aou] | иначе | latinicá, jaicó / jaicyo |
| ц | ç / cz | в транскрипционная система Палладия - где противопоставление твердых-мягких гласных | çá ця, cá ца, Çúané / Czyuanj Цюань |
| ц | cz | иначе | zajacz |
|     |     |     |     |
|     |     |     |     |
| е | e | после согласных | leto |
| е | é / je | после й, после "и" в окончаниях | sinié / sinije, Bajés / Bajjes |
| е | je | иначе | Jevropa, podòjezd / podjiezd, pjesa |
| ё | yo / yo | где этимология требует именно yo | Yoda    |
| ё | éo / yo | после согласных | méod / myod, geograph географ |
| ё | éo / jeo | после й, после "и" в окончаниях | mumiéo / mumijeo, mumiéò / mumijeeo, jéogz / jjeogz йёж, jéògz / jjeeogz йеож |
| ё | jo | после "е" | jejo, nejo, nejio / нейо |
| ё | jeo | иначе | jeogz, podòjeom / podjieom, pjeom, pjeòm / pjeeom пьеом |
| ещё | ещё$ / (j)esche$ | исключение для ещё на конце слова | jesche ещё, jeshchíe / jeshchiie ещьэ - звучит как "ще" |
| ю | yu / yu | где этимология требует именно yu | Mayuri    |
| ю | ú / yu | после согласных | lúbimyj / lyubimyj |
| ю | ú / ju | после й, после "и" в окончаниях | Juliú / Juliju |
| ю | ju | иначе | jula, pju |
| я | ya / ya | где этимология требует именно ya | nya |
| я | á / ya | после согласных | sinája / sinyaja |
| я | á / ja | после й, после "и" в окончаниях | Mariá / Marija, allilujá / allilujja, sijaté - не окончание, pajaté - морфемы не мутируют |
| я | ja | иначе | ja я, pjan |
|     |     |     | *já,jú,jé,jéo,jý создают дополнительную йотацию, а jí не создаёт дополнительную йотацию, а jó вообще джо.* |
|     |     |     |     |
|     |     |     |     |
| и | í / i | в начале слова перед гласной или йотом с заглавной буквы | Íacov / Iacov, Íesus / Iesus - исключение, ion / ion |
| ии | íy / iy | в начале слова с заглавной буквы перед согласной | Íyda / Iyda |
| и | í / ii | после гласных (кроме и,ы), или просто после й | moí / moii мои, rajíspolcom / rajiispolcom, superòjíp / superjiip суперйип, Luí / Luii, zaíca / zaiica |
| и | jí / jy | после ь | platjíce / platjyce |
| и | y | в исключениях где этимология требует "y" и где нельзя спутать с "ы" | Yggdrasilé Иггдрасиль |
| и | ý / yi | в исключениях где этимология требует "y" | sýstema / syistema, gýmanziá, gýroscop |
| и | i | обычно - в т.ч. "ии" в конце слова | bacterii, mir |
|     |     |     |     |
|     |     |     |     |
| ы | ì / y | когда этимология требует i | muzìca / muzyca, latìnè / latynj |
| ы | y | после согласного звука (в т.ч. йота) и одновременно перед: согласным звуком (в т.ч. йотации), или нейотированными гласными аоуиыэ, или в конце слова | ty, crasnyj, crasnyje, vyùchil / vyyuchil, vyíscyvaté / vyyiscyvatj, tyè / tyye тыэ, jyò / jyyo йыо, sòjyí / sjiyyi сйыи, jys йыс, sòjys / sjiys сйыс, tyy тыы - можно удваивать, но platjíce / platjyce |
| ы | ỳ / yy | в остальных случаях | ỳdgzyd / yydgzyd ыджыд, aỳ / ayy аы |
|     |     |     | *Тут можно заметить, что Ee после согласных это Ее, а не после согласных - Ээ. А Yy после согласных, хоть и с оговорками, - это Ыы, а иначе - Ии.* |
|     |     |     |     |
|     |     |     |     |
|     |     | ghy,phy,thy,rhy,chỳ(khy),cy | всегда ги,фи,ти,ри,хи,ки |
|     |     | gy,fy,ty,ry,hy/òhy(xhy),ky/cky | гы,фы,ты,ры,хы,кы |
|     |     | *Примеры:* | ghypotheza, phyzica, tachỳony |
|     |     |     |     |
|     |     |     |     |
| э | è / ae | после Аа | aèro / aaero, maèstro / maaestro |
| э | ae / ae | когда этимология требует Aa | maer, Thaetcher, Aeppl, Aendý / Aendyi |
| э | è / ae | обычно после согласных | partèr / partaer |
| э | e | иначе | etot, erotica |
|     |     |     |     |
|     |     |     |     |
| ъ | j | перед йотированными гласными - съ[ёеюя] — sòj[oeua] / sji[oeua] | sòjezd / sjiezd, zajezd |
| ъ | ò / qh | в остальных случаях после согласных, кроме j,w | obòizvestité / obqhizvestitj объизвестить |
| ъ | qh | иначе | aqh аъ |
|     |     |     |     |
|     |     |     |     |
| ь | j | перед йотированными гласными кроме "ё" - сь[еюя] — sj[eua] | pjesa |
| ьё | jeo | сьё — sjeo | pjeom |
| ь | í / ii | перед нейотированными гласными кроме "и,о" - сь[ыэуа] — sí[yeua] / sii[yeua] | belíetagj бельэтаж - звучит как "лье",  partíer / partiier партьэр - звучит как "те". Нужно все исключения прочтения писать йотированно - beljetagj |
| ьи | jí | сьи — sjí / sjy | platjíce / platjyce, creslice |
| ьо | jo | сьо — sjo | buljon |
| ь | j / j | после согласных в заимствованиях где по этимологии не было дополнительного смягчения | culjtura, paljma |
| ь | é / j | после согласных | conécy / conjcy коньки, léda / ljda льда, scolézcyj |
| ь | qh | иначе запрещено | aqh аь становится аъ |
|     |     |     |     |
|     |     |     |     |
| й | y | где этимология требует | yippi, York, superòyippi / superqhyippi, superéyippi / superiiyippi - альтернативная этимологичная форма, tonjyork тоньйорк |
| й | ji | после согласной перед согласной или в конце слова; перед нейотированными гласными ауэ - кроме иыо | sjis сйс, sés / sjs сьс, sòjie / sqhjie сйэ, sòie съиэ, ajia айа, ejien эйэн |
| й | j | перед "о" **не** после согласной | jod, major |
| йо | (ò)jo / jio |     | Séorkòjosen / Syorkjiosen Сёркйосен |
| йи | jí / jii |     | rajíspolcom / rajiispolcom, jíp / jiip, superòjíp / superjiip |
| йы | jy |     | jyí / jyyi йыи |
| й | i | после гласных не перед гласными - кроме ий,ый | moi мой, poimal поймал, dui дуй, dúim дюйм, Einshtein, zaíca / zaiica заика |
| й | j | иначе - в т.ч. ий,ый | allilujá / allilujja, sinij, crasnyj |



### Дополнительные примеры

сьйя/sjjja/séjá, сйя/sjija/sjiá, сьйс/sjjis/séjis, сйс/sjis.

Уточнение мягкости: parter, partíer/partiier, partèr/partuer.

Обратите внимание, что йот+твердая гласная (аоуэ) даёт мягкое звучание гласной (a => æ, o => ɵ, u => ʉ, ɛ => e, так пусть и ɨ => i будет). То есть, фонетика строится в предположении, что йы и йи звучат одинаково.


### Ударения

Либо твердые ударения, либо специальные должны иметь диакритику для Ww. Мягкие - только для всех гласных. Итого, нужно выбрать три из доступных вариантов:

ǎǒěǔǐ ǍǑĚǓǏ, но комб. Y̌y̌  
âôêûŵŷî ÂÔÊÛŴŶÎ  
ãõẽũỹĩ ÃÕẼŨỸĨ  
äöëüÿẅï ÄÖËÜŸẄÏ  
āōēūȳī ĀŌĒŪȲĪ  
ảỏẻủỷỉ ẢỎẺỦỶỈ  
ạọẹụỵẉị ẠỌẸỤỴẈỊ  

Основная идея:

* a => â (как ударение в валийском),
* á => ǎ (второй тип ударения есть в португальском, но первый там классическое á, второй тип - â),
* i => ǐ,
* ì => î,
* грависы - твёрдые, акуты - мягкие,
* крышки - твердые, гачеки - мягкие.
* тильды - после специальных букв, всегда звучит аоуеи, никогда - яёюэы.



Подробная версия:

без ударения => c ударением

* Aa, Àà (Аа) => Ââ (Àà - отдельная от диграфов Аа после гласных)
* Àà (Аа) => Ãã (Àà - модифицирующая J,B,...)
* Áá (Яя) => Ǎǎ
* Uu, Ùù (Уу) => Ûû (Ùù - отдельная от диграфов Уу после гласных)
* Ùù (Уу) => Ũũ (Ùù - модифицирующая J,B,...)
* Úú (Юю) => Ǔǔ
* Oo, Òò (Оо) => Ôô (Òò - отдельная от диграфов Оо после гласных)
* Óó (Оо) => Õõ (Óó - модифицирующая J,B,...)
* ÉOéo (Ёё) => ÉǑéǒ
* Òò (Ъъ) — doesn't need (Òò - значит Ъъ после согласных кроме Jj)
* Ee, Èè (Ээ) => Êê (Èè - отдельная от диграфов Ээ после гласных)
* Ee, Éé (Ее) => Ěě (Éé - после j,i)
* Èè (Ее) => Ẽẽ (Èè - модифицирующая J,B,...)
* Éé (Ьь) — doesn't need (Éé - значит Ьь после согласных кроме Jj)
* Yy (Ыы) => Ŷŷ
* Ýý (Ии) => Y̌y̌ / yî (Ýý - Ии греческой этимологии)
* Ỳỳ (Ии) => Ỹỹ (Ỳỳ - модифицирующая J,B,...)
* I i, Í í (Ии) => Ǐ ǐ
* Ì ì (Ии) => Ĩ ĩ ( Ì ì - модифицирующая J,B,...)
* Ì ì (Ыы) => Î î ( Ì ì - этимологическое Ыы)
* Í í (Ьь) — doesn't need (Í í - Ьь после согласных, но не Jj)
* Ww => Ŵŵ

Y̌y̌ использует комбинированные символы. Тильда является грубым и доступным для набора визуальным приближением комбинации грависа и крышки / гачека - как в ẰẦỒỀ ằầồề.

Под ударением: sýstem => sy̌stem / syîstem, vyíscyvaté => vyǐscyvaté, latìné => latîné,  
Wèst / Уэст => Wẽst / Уэ́ст, Ŵèst / У́эст,  
jè (дже) => jẽ / jhě, je (е) => jê, Jà (Джа) => Jã / Jhâ, Bà (Ва) => Bã / Bhâ, Chà (Ха) => Chã / Khâ.

С помощью US-International можно ввести все буквы и твёрдые ударения. Кроме Ỳỳ - для этого нужно установить [United Kingdom (Extended) Layout](https://en.wikipedia.org/wiki/US_international_keyboard#United_Kingdom_(Extended)_Layout) и Y̌y̌,ÃãÕõẼẽŨũỸỹ Ĩ ĩ - их можно скопировать или использовать запасной диграф. С помощью EurKEY можно ввести оставшиеся мягкие ударения. Сносным вариантом является установить языком системы русский, в русский язык ввода дополнительно добавить раскладку United Kingdom Extended Layout. Вторым языком сделать английский США. В него добавить раскладки US-International и EurKEY. Главные раскладки - русская и US-International, а до оставшихся двух можно добраться при желании.


### Про диграфы cz и gz

Стоит отметить, что рукописная буква z выглядит либо как рукописная цифра 2 с угловатым верхом, либо как кириллическая рукописная "з" с хвостиком внизу, но более угловатая сверху. Когда z отдельно это смотрится нормально, а вот в диграфах cz и gz оба варианта написания z смотрятся плохо. В этом случае стоит использовать специальные рукописные лигатуры. Для cz - рукописная "ц" с петелькой, "c" идет в первую палку "ц", а "z" (вариант с петелькой) идет во вторую палку "ц" и петельку (заглавный вариант тоже должен выглядеть как рукописная "Ц"). Для gz - рукописная "g", к которой справа вплотную добавлена кириллическая буква "з" без петельки внизу (будто стяжка на правой дуге рукописной буквы "ф"). Заглавный вариант выглядит как рукописная "G", у которой внутренняя палочка является началом рукописной "z" (вариант с петелькой). Обе лигатуры легко писать и они имеют в себе логическую связь с составляющими их буквами.


### Аббревиатуры

В латинице используются фонетическо-кириллические аббревиатуры, которые вопреки записи сокращают по звучанию. Таким образом, названия букв в аббревиатурах (а так же диграфы) будут читаться как в кириллице.

Изменения в названиях букв и диграфов (сокращения по звучанию опираются на названия букв):

* **Aa**
  * **Áá** - я (Á., FIÁ)
* **Bb**
* **Cc, Çç** - це (C., ÇPU, перед EI в аббревиатурах - просто C)
  * **Ch** - че (Ch., ChS)
* **Dd**
* **Ee, Éé** - е (E., ÉGÈ, после согласных (кроме ЙЖ) в аббр. - просто E)
  * **ÉÓéó** - ё (Éo.) / **Èè** - э (È., ÉGÈ)
* **Ff**
* **Gg** - гэ (была "же" в математике)
  * **GJ** - же (Gj., OBGJ) 
* **Hh** - ха (H., KHL, была "аш" в математике)
* **Ii** / **Jj** - йот (была "жи" в математике и "и-краткая" в алфавите)
* **Kk** - ка / **Ll** - эль, в аббр. - "эл"
* **Mm, Nn, Oo, Pp** / **Qq** - ку / **Rr**
* **Ss**
  * **Sh** - ша (Sh., VSh) / **Sch** - ща (Sch., MSch)
* **Tt**
* **Uu**
  * **Úú** - ю (Ú. ÚAR)
* **Vv** / **Ww** - дубль-вэ, в аббр. - "ву" / **Xx** - икс
* **Yy** - игрек, в аббр. - "игр"
  * **Ỳỳ** - ы (Ỳ.)
* **Zz** - зэт, в аббр. - "зэ" (была "зэ" в алфавите)

Символы (комбинации) внутреннего уровня не являются самостоятельными буквами, но при этом имеют отдельные названия и входят в состав (фонетически образованных) аббревиатур - это нужно для совместимости с кириллицей.

В скобках указаны ASCII-only обозначения.

| **А**  |     **О**      |  **У**  | **Э**  |  **Ы**  |
|:------:|:--------------:|:-------:|:------:|:-------:|
| A / À  |       O        |  U / Ù  | È (Eh) |  Ỳ (Yh) |
| **Я**  |     **Ё**      |  **Ю**  | **Е**  |  **И**  |
| Á (JA) | EÓ (Eo) / ÉÓ (JEo) | Ú (JU) | E / É (JE) | I / Í / Ý |
| **Б**  |     **В**      |  **Г**  | **Д**  |  **Ж**  |
|   B    |       V        |  G / Gh |   D    |   GJ    |
| **З**  |     **Й**      |  **К**  | **Л**  |  **М**  |
|   Z    |   J / J (JI)   |    K    |   L    |    M    |
| **Н**  |     **П**      |  **Р**  | **С**  |  **Т**  |
|   N    |       P        |    R    |   S    |    T    |
| **Ф**  |     **Х**      |  **Ц**  | **Ч**  |  **Ш**  |
|   F    |       H        | C / Ç (Cj) | Ch  |   Sh    |
| **Щ**  |  **ШЧ, СЧ**    |  **ГЙ** |        |         |
|  Sch   |   ShCh, SCh    |   GhJ   |       |         |

* в аббр. Ц перед EI - просто C, иначе - Ç,
* в аббр. Е после согласных (кроме ЙЖ) - просто E (EÓ), иначе - É (ÉÓ),
* в аббр. в АСКИ версии Й перед АУИ - JI, иначе - J,
* в аббр. в диакритической версии АУИ после ЙЖ пишутся ÀÙÍ,
* после строчных букв буква И в аббревиатуры идёт как Ý.
* сочетание ГЙ пишется GhJ

*Буква Cc называется Це и в аббревиатуры идёт как Ç/C. И обозначает она там начальнй __звук__ Ц. А все начальные звуки Ка в аббревиатурах обозначаются K. Carina Petrova => K.Petrova. Ciceron Romanov => C.Romanov. ÇPU.*  

GJÍ ЖИ (GJI), GJZL ЖЗЛ, GZI ГЗИ, TZ ТЗ,  
SZI СЗИ, ShÝ ШИ (ShI), SHI СХИ,  
ÉGÈ ЕГЭ (JEGEh),  
GE ГЕ, GÈ ГЭ (GEh), GI ГИ, GỲ ГЫ (GYh),  
GJÉ ЖЕ (GJJE), GJÈ ЖЭ (GJEh), GJÍ ЖИ (GJI), GJỲ ЖЫ (GJYh), GzA ГзА,  
CI ЦИ, ÇZI ЦЗИ (CZI), ÇA ЦА (CA), ÇZA ЦЗА (CZA), ÇzA ЦзА (CzA),  

KE КЕ, KÈ КЭ (KEh), KI КИ,  
GH ГХ, GZ ГЗ, KZ КЗ, KHI КХИ, NH НХ, NHI НХИ,  
SChÝ СЧИ (SChI), SchÝ ЩИ (SchI), SCh СЧ, SchU ЩУ,  
CI ЦИ, ChÝ ЧИ (ChI), ShÝ ШИ (ShI), SHI СХИ,  
JÈ ЙЭ (JEh), JÉ ЙЕ (JJE), JÍ ЙИ (JII), JÀ ЙА (JIA).

ÉGÈ ЕГЭ (JEGEh), OBGJ ОБЖ, ÇPU ЦПУ (CPU), ChS ЧС, SShA США, ÈÈG ЭЭГ (EhEhG), GJÈK ЖЭК (GJEhK), GJKH ЖКХ, NHL НХЛ, KHL КХЛ, ÉKA ЕКА (JEKA), FIÁ ФИЯ (FIJA), CERN ЦЕРН, OBSE ОБСЕ, GIBDD ГИБДД, ChIM ЧИМ.

Возможно использование исключений типа Nju York => NY вместо NJ, т.к. Y свободна для смысла йота в аббревиатурах.


### Набор на смартфоне

Оптимально удобный ввод на смартфоне - с помощью проприетарных клавиатур со свайпом. Расширений для самых популярных GBoard и Swift я не обнаружил. Добавить прямо в код клавиатуры Гугла русскую латиницу можно было только если бы был единый стандарт русской латиницы. Это не реально.

Так что остаётся только использовать одну из уже существующих раскладок и импортировать собственный словарь - GBoard позволяет экспортировать и импортировать свои слова (свайп с ними работает, нужно надеяться, что нет ограничения по количеству слов...).

Описание выше, является довольно существенным ограничением на проектирование латиницы.

А как можно использовать уже существующую клавиатуру в GBoard? Адаптировать её под письмо в стиле US-international. То есть, клавиатура должна иметь выделенные кнопки под апостроф и, возможно, грэйв. А так же она должна мочь при долгом нажатии печатать буквы с диакритикой, используемые в латинице (US-international тоже должна их печатать). Тогда если в словарь пользователя добавить импортом словарь слов в русской латинице с сокращениями ввода типа m'aso => máso, то сценарии печати на swype будут совпадать со сценариями печати в US-international.

В моей текущей латинице я рассматриваю вариант использования акутов для мягкости, а грэйвов - для твёрдости (i,í - и, y,ì - ы, á - я, è - э). Но, стоит отметить, что при долгом нажатии нужны только частые буквы. А вот буквы для ударений и аббревиатур вполне можно печатать через подсказки специальных автозамен из личного словаря 'a' => ǎ (á под ударением), a' => â (a под ударением) - как предложено [тут](https://android.stackexchange.com/questions/224043/gboard-set-custom-unicode-characters-on-longpress-or-add-custom-keyboard-keys-o).

Точно так же как в US-international тоже обязательны только частые буквы, а буквы для ударений и аббревиатур можно использовать из EurKey (для удобного переключения между US-international и EurKey нужно дефолтным языком сделать русский - это позволит удалить дефолтную раскладку US). Приоритет должен быть у EurKey, т.к. он содержит неизменённую оригинальную раскладку, просто добавляет новые возможности через AltGr.

![EurKey](./EurKey.png).

Интересными раскладками в GBoard, имеющими ровно одну дополнительную клавишу для ' и \`, являются следующие: Валлийский, Хауса (могут интегрироваться с английским - на них будут подсказки и свайп англиских слов) и Бенч (может печатать ěǎǔǒǐ). При этом, валлийский может печатать ỳ. Остальные найденные не столь хороши: Южно-боливийский кечуа (без поддержки swype), Пурепеча, Кечуа (могут набирать Çç), Покот, Хилигайнон (ничем не примечательны).

Так что Валлийский и Хауса из GBoard - идеальные кандидаты для переделки в аналог US-international. Бенч можно добавить для ударений. А эсперанто - для диакритики над согласными. Кстати, диакритические буквы из валийского и эсперанто будут доступны из из обычной английской клавиатуры, если подключить их интеграцию. Бенч, к сожалению, не интегрируется.

Если Вы хотите использовать и английский, и русскую латиницу на одной клавиатуре, то хватит установки только Валлийского и английского, если же Вы бы хотели писать на разных клавиатурах, то нужно установить и валлийский, и хауса - у них одинаковые клавиатуры при переключении между которыми кнопки будут оставаться на своих местах. Английский писать в Хауса (нужно интегрировать английский в него), русскую латиницу - в валлийском.

Но, похоже, больше трёх раскладок - это неудобно. Поэтому, есть смысл все писать в валлийской.

Если же Вы предпочитаете клавиатуры с открытым исходным кодом, то придется пропатчить и скомпилировать OpenBoard.


### Включения иностранных слов без изменений

*Выбранный выше способ ввода на смартфоне может сделать ввод инородных включений слегка неудобнее, но не думаю, что значительно.*

От небуквенного символа до кавычки сразу после буквы - иностранное включение.

.US-international — от нетипичной точки перед буквой (сразу после пробела - \w или ^) - экранирует вплоть до пробела (\w или $). Заметьте, что ".3" не катит.  
..this is OK. I eto horosho. — от нетипичных двух точек сразу перед буквой до конца предложения.  
.. — можно от .. до .. помечать целые абзацы. Но, в отличие от предыдущего варианта, нужны пробельные символы вокруг ".." (\w,^,$). Но можно и просто вот так:  
.. this is .. horosho.  

Andrew' (одно слово - только буквы)  
gh'/г', gz'/ж' (так же)  
'Watson'ovscyj (русское окончание Watson'овский)  
this' is' horosho. (каждое нужное помечено)  

z-распад / z'-raspad  
час-x / chas-x'  
girls' / girls''  
'ghealach / ''ghealach'  
он нам 'сильно помог':) / on nam 'siléno pomog':)  
(как обычные кавычки их все ещё можно использовать)  
час-x z-распад / chas-x' z'-raspad  
час-кс ' з'-распад / chas-x ' z'-raspad  
(перед открывающей кавычкой должен быть небуквенный символ, чтобы она считалась именно открывающей кавычкой)  
d'Arc / d'Arc'  
Д'Арк / D'Arc  
'Watson'овский / ''Watson'ovscyj  
Watson'овский / 'Watson'ovscyj  
vs. / vs'.  


### Требование обратимости латиниц друг в друга - излишне

Требование обратимости латиниц друг в друга - слишком жесткое (диакритической и АСКИ версий). АСКИ версия не обязана дублировать диакритическую. Она лишь должна дублировать кириллицу. Так что у некоторых слов в АСКИ есть несколько возможных написаний с диакритикой, но лишь одно каноническое. Например, АСКИ daljshe становится daléshe, но АСКИ culjtura остаётся culjtura.

На данный момент единственные расхождения:

* ь/j/é после согласных,
* заимствования с ya,yo,yu после согласных,
* этимологическая ы/ì/y,
* этимологические ки/cì/cki,ке/cè/cke vs. этимологические ки/cki/cki,ке/cke/cke,
* òh/kh vs. этимологические ch/kh,
* cz/cz vs. ç/cz,
* sae/sae vs. sè/sae.


## Пример текста

Piony I vasiléci vséo jesche rastut na poláne vozle derevni Péony, schitajuscheisá bogatoi. V nei rodilsá izvestnyj pianist, perejehavshij v Sietl na rabotu v companii "Moí I tvoí".

Pjanyj master po projectu sdelal mechànichescij object s izjanom. Jesli brac ne obnarugzitsá, to belyje bolidy boléshe ne smogut vyígryvaté gonci I vyúchité svoí oshibci.

V pjése pro devushcu v zeléonom platjícze vse sadilisé na ladjí I plyli po rece. No tut iz lesa vyshel Gèorgò Maximus, coné v paléto I rvanyh jìnsah, cotoryj cogo-to oboìscival, I pricazal vsem mytésá I gotovité buljón. Znachit snova pjéom do lysyh aqvalangistov.

Prepodobnyj Bajés podcinul igralényje costi. Vypalo shesté, znachit jemu pridéotsá mazaté jod na ranu.

Maer neboléshogo gorodishci otcryl tabliczu exelá I vozmutilsá czenoi novogo excavatora. Agz exzema snova stala jego bespocoíté. Oh ugz eta pocupca vechnogo dvigatelá v proshlom godu! A tac gze pocupca aeroplana-ecranoléota. Jesli tac poidéot I daléshe, to búdgètu pridéotsá hudo.

V etom vide phraza ot A do Ja nachinajet vygládeté sovsem po-drugomu. Seichas schéotca novaja, no pozgze ona stanet staraja. Chernysh lúbit cogda jego cheshut jeju. Jeogz colúchij I pohogz na nejo.

Sòhod mestnyh gzitelei indijscoi derevni sickhov reshal chto gze delaté s otòhodami companii "Caligula Gai Julij Càezaré" (lat. .Caligula Gaius Iulius Caesar). Odin iz prisutstvujuschih nosil hoholoc na golove. On I nashéol vyhod iz situatsii.

"Cto s mechom c nam pridéot, tot ot mecha I..." - ne smog dogovorité starshij mechànic Vasilij.

Lúbimczem Biljbo byl junyj Frodo Baeggins. Cogda Biljbo stucnulo devánosto deváté, on vdrug usynovil sirotu Frodo, sdelal svoím naslednicom I predlogzil pereselitésá v Zasumci. Tut ugz vse nadegzdy Dericulé-Baegginsov, davno s vogzdeleniém posmatrivavshih na usadébu, ruhnuli oconchateléno.

Sluchaju bylo ugodno, chtoby Biljbo s Frodo jesche I rodilisé v odin dené, 22 sentábrá.

– Frodo, maléchic moi, – scazal cac-to raz Biljbo, – perebiralsá by ty co mne. Gládishé, I dené rogzdeniá vmeste otmechali by.

Frodo v tu poru hodil v dorostcah. Tac hobbity zovut molodéogzé v bezotvetstvennom vozraste megzdu dvadczatjú I tridczatjú tremá, posle chego hobbit naconecz mogzet schitaté sebá vzroslym.

Proshlo jesche dvenadczaté let. V Zasumcah cagzdyj god veselo otmechali dvoinoi dené rogzdeniá, c etomu privycli, no lúbomu bylo jasno, chto nyneshnei osenjú gotovitsá nechto neobychnoe. Biljbo ispolnálosé 111 let – vozrast dlá hobbita veséma pochtennyj, da I chislo lúbopytnoje, nu a Frodo gotovilsá otmetité tridczatitréohletié – togze znamenatelénaja data – sovershennoletié po-hobbitsci.

Imejetsá nescoléco hÿpothez proísòhogzdeniá sobaci, naíboleje verojatnymi jejo predcami schitajutsá volc I necotoryje vidy shacalov.

V sugzdeniáh uchéonyh o predcah domashnei sobaci prisutstvujut dve tochci zreniá. Odni schitajut, chto sobaci - polýphyletichescaja gruppa (proísòhodáschaja ot nescolécih predcov), drugié pridergzivajutsá mneniá, chto vse sobaci proízoshli ot odnogo predca (monophyletichescaja theoriá).

Alexandr Pushcin — Zimneje utro

Moroz I solncze; dené chudesnyj!  
Jesche ty dremleshé, drug prelestnyj —  
Pora, crasavicza, prosnisé:  
Otcroi somcnuty negoi vzory  
Navstrechu severnoi Avrory,  
Zvezdoju severa javisé!  

Vechor, ty pomnishé, vjúga zlilasé,  
Na mutnom nebe mgla nosilasé;  
Luna, cac blednoje pátno,  
Scvozé tuchi mrachnyje gzeltela,  
I ty pechalénaja sidela —  
A nynche… pogládi v ocno:  

Pod golubymi nebesami  
Velicolepnymi covrami,  
Blestá na solnce, sneg legzit;  
Prozrachnyj les odin chernejet,  
I jelé scvozé inei zelenejet,  
I rechca podo lédom blestit.  

Vsá comnata jantarnym blescom  
Ozarena. Veséolym trescom  
Treschit zatoplennaja peché.  
Prijatno dumaté u legzanci.  
No znajeshé: ne veleté li v sanci  
Cobylcu buruju zapreché?  

Scolézá po utrennemu snegu,  
Drug milyj, predadimsá begu  
Netoroplivogo coná  
I navestim polá pustyje,  
Lesa, nedavno stolé gustyje,  
I bereg, milyj dlá mená.  

Lermontov M.Ju. — Rodina

Lúblú otchiznu ja, no strannoju lúbovjú!  
Ne pobedit jejo rassudoc moi.  
Ni slava, cuplennaja crovjú,  
Ni polnyj gordogo doveriá pocoi,  
Ni téomnoi stariny zavetnyje predanjá  
Ne shevelát vo mne otradnogo mechtanjá.  
No ja lúblú — za chto, ne znaju sam —  
Jejo stepei holodnoje molchanjé,  
Jejo lesov bezbregznyh colyhanjé,  
Razlivy rec jejo, podobnyje morám;  
Proséolochnym putéom lúblú scacaté v telege  
I, vzorom medlennym pronzaja nochi tené,  
Vstrechaté po storonam, vzdyhaja o nochlege,  
Drogzaschié ogni pechalényh derevené;  
Lúblú dymoc spaléonnoi gznivy,  
V stepi nochujuschij oboz  
I na holme sredé gzéoltoi nivy  
Chetu belejuschih beréoz.  
S otradoi, mnogim neznacomoi,  
Ja vigzu polnoje gumno,  
Izbu, pocrytuju solomoi,  
S reznymi stavnámi ocno;  
I v prazdnic, vecherom rosistym,  
Smotreté do polnochi gotov  
Na pláscu s topanjém I svistom  
Pod govor pjányh mugzichcov.  

// God napisaniá: 1841
