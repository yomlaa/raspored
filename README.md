# Пројекат "Распоред"
је напредна веб-апликација намењена приказу распореда часова за одељења Митровачке Гимназије.

## Иницијатива 

Још од основне школе на полеђину свеска смо лепили распоред часова како би редовно прегледали за који часове треба да се припремимо, неки су одлазили корак даље и записали су и када се који час завршава и када почиње следећи. 

Мало је оних који своје распореде уче напамет, тако да проблем тражења те једне свеске где се налази распоред пренео и у средњу школу. Срећом, у Митровачкој Гимназији постоји дигитални запис распореда часова на веб-сајту школе. 

Ученици би преузели свој распоред и сачували га у галерију или ставили као позадину на закључаном екрану свога телефона. Како ове методе нису ефикасне (довољно) и имајући у обзир да је било неопходно да корисник сам преузме нови распоред уколико се изврши нека промена или уколико жели видети неки други распоред, дошао сам на идеју да направим апликацију која би радила управо то, а лака инсталација и приступ је баш оно што је неопходно овако једноставној услузи како би се избегло фрустрирање корисника. 

## Реализација 

### Набављање свих распореда 

Како бих уштедео на величини сајта, уместо PNG датотека са сајта, преузео сам две PDF датотеке са распоредима за ученике и професоре са сајта гимназије. Слике морају бити векторског формата како би сајт био испод 5MB (Што сам себи поставио као циљ овог пројекта). 

Приказ PDF страница је много компликованији него приказ рецимо SVG слике, тако да сам конвертовао око 97 станица PDF-а у посебне SVG датотеке. У поређењу са PNG датотекама, SVG је заузимао oko 80% мање места. 

### “Vue.js” – Јаваскрипт оквир 

Да би поједноставио процес развијања и како би умањио непотребан рад на стандардне веб-принципе, одлучио сам да апликација развијам у модуларном оквиру званом „Vue.js”. 

### Бутстреп – Стил и контроле 

За дизајнирањем посебних контроли и стилова у оваквом пројекту није било потребе, све је лако регулисано коришћењем Бутстреп библиотеке контроли и стилова. 

  Поред стандардних стилова, коришћене су и следеће контроле: 
  Дугме 
  Модал (искочна порука) 
  Формулар опције (Групе, Радио дугме, Селектор елемент, Инпут елемент, Дугме на           штиклирање) 

Поменути елементи су додати у „main.js” датотеци пројекта. 

## Фајербејс – Хостинг и сервисирање 

Ради брзине дистрибуције и лаког одржавања сервера, за хостинг је изабран сервис Гугл Фајербејс који нуди бесплатни веб-хостинг и подржава све потребне стандарде за „PWA“ технологију.
## Употреба и перформансе 

#### Гугл Лајтхаус

Коришћењем Гугле алатке за тестирање перформанси и компатибилности веб-апликација пројекат распоред постиже следеће резултате: 

#### Перформансе – 100% оптимизовано 

#### Приступачност – 91% оптимизовано (ово поглавље је једино које не достиже 100% - главни разлог томе је што Бутстреп дугмад испод приказа распореда имају исту позадину као и веб-страница, али то не би требало да представља проблем јер имају јасну боју ивица – прилог 4 и прилог 6)  

#### Најбоља пракса – 100% оптимизовано 

#### Оптимизација за претраживаче – 100% оптимизовано 

 

Током писања овог рада, апликација „Raspored“ се налази на домену rs.draganovik.com, а изворни код ће за време одбране рада бити постављен и на Гитхаб на домену github.com/draganovik/Raspored. 
