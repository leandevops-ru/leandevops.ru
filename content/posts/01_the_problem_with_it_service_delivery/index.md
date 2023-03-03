---
title: 'Введение'
title: 'The Problem with IT service Delivery'
date: '2023-03-04'
draft: false
---

> _Расскажи мне, и я забуду. Научи меня, и запомню. Вовлеки меня, и действительно
> научусь._
>
> Бенджамин Франклин

Современный мир развивается безумно быстро. Сегодня инновации важны как никогда.
Люди хотят наилучшие решения и побыстрее. Чтобы добиться этого приходится
сталкиваться с новым и неизвестным, а это всегда рискованно. Но другого пути и
нет, без риска можно создавать только посредственные продукты, которые не
произведут никакого впечатления на пользователей.

> **23 сентября 2010**: Blockbuster Entertainment подала заявку на защиту от
> банкротства после того, как понесла значительные убытки из-за сильной
> конкуренции со стороны Netflix и других видео сервисов. Несмотря на
> лидирующие позиции в прокате домашнего видео и предложение войти в бизнес
> стримминга видео ещё в 1999 году, Blockbuster не смогла предвидеть растущую
> популярность стримминговых сервисов.

Немногие индустрии развиваются также быстро, как информационные технологии. От
самих телефонов до программного обеспечения, которое на них работает. Но
такой стремительный рост приносит и огромное количество проблем.

> **3 января 2018**: Миру были раскрыты уязвимости в системах безопасности
> Meltdown и Spectre. Каждая из них использует слабые места в функциях
> спекулятивного выполнения, имеющихся в большинстве современных
> микропроцессоров, позволяя злоумышленнику извлекать личные данные. Находясь
> на аппаратном уровне, эти уязвимости препятствовали защите как системы, так и
> виртуализации. Это создало особенно серьезные риски для поставщиков облачных
> услуг и их клиентов. ИТ-провайдеры, зависящие от устаревшего программного
> обеспечения, были поставлены перед выбором болезненных обновлений и
> исправления или остаться уязвимыми. Что еще хуже, многие из первоначальных
> исправлений для микропрограммного обеспечения, операционной системы и
> виртуализации были созданы и внедрены насильно. Это создавало нестабильность,
> нежелательные перезагрузки и случайные сбои в работе систем. Исправления
> также снизили производительность некоторых систем вплоть до 19%.[^1]

[^1]: “Speculative Execution Exploit Performance Impacts --- Describing the
  performance impacts to security patches for CVE-2017-5754 CVE-2017-5753 and
  CVE-2017-5715,” Red Hat: https://access.redhat.com/articles/3307751

Каждая инновация приносит с собой новые уровни технологии, повышая сложность
системы. С таким количеством движущихся частей, производимых постоянно растущим
списком поставщиков, любому человеку трудно знать об используемом стеке все,
что нужно. Подобно зданию с неизвестным фундаментом, эта сложность создает
неопределенность, которая затрудняет внедрение инноваций. Это также добавляет
хрупкости, увеличивает вероятность неудачи.

В то же время, когда технологии усложнились, терпение клиентов к неудачам
иссякло. По мере того как рос спрос на ИТ-решения, они глубоко укоренились
практически во всех аспектах нашей жизни. Теперь все, от нашей бытовой техники,
автомобилей и банков до служб экстренной помощи, зависит от функционирования
все более сложной сети программного обеспечения. Любой единичный сбой может
каскадом перерасти во что-то разрушительное и дорогостоящее как для сообщества
пользователей, так и для поставщика. Теперь к сбою может привести не только
ошибка в реализации функционала, но и неправильное использование, а также
ошибочные ожидания.

> **1 августа 2012 года**: Крупный маркет-мейкер Knight Capital Group пострадал
> от ошибки в своем программном обеспечении алгоритмического маршрутизатора
> SMARS, которая привела к убыткам в размере 460 миллионов долларов в течение 45
> минут. Это превысило совокупные активы фирмы, что в конечном итоге привело к
> поглощению другой компанией.

Решение задач, связанных с инновациями, скоростью, надежностью и соответствием
ожиданиям, положило начало конкуренции между двумя подходами: снижением трений
при доставке и управлением рисками при предоставлении услуг. Это соревнование
важно, поскольку оно влияет на то, как организации относятся к DevOps, и, в
конечном счете, на их шансы на успех. Однако, хотя каждый подход учитывает
некоторые важные факторы, каждый из них также содержит ряд серьёзных
недостатков. Это не только само по себе вызывает неприятные проблемы с
доставкой, но и может фактически помешать организации достичь единственного
наиболее важного аспекта доставки: эффективного оказания помощи клиентам в
достижении их целевых результатов.

## Метод #1: Сокращение трудностей при доставке

**Сентябрь 7, 2017**: Агенство кредитной истории Equifax объвило, что хакеры
взломали и украли персональную информацию до 143 миллионов американских
потребителей. Взлом, как сообщается, произошел приблизительно в мае через 
эксплойт ранее сообщенной уязвимости Apache Struts. Несмотря на то, что патч, 
устранявший проблемму, был доступен с марта, Equifax, по-видимому, не 
предприняла необходимых мер предосторожности для устранения уязвимости до тех
пор, пока не произошел взлом. Неназванные источники утверждают, что решение об
отсрочке могло быть принято из-за нехватки ресурсов для других мероприятий по
разработке программного обеспечения.

Восприятие того, что вы слишком медленно реагируете на события, независимо от
того, исправляется ли это новая ошибка или уязвимость, или удовлетворяется
какой-то новый потребительский спрос или нормативное требование, может быть не
только неприятным, но и фатальным для бизнеса. Это подрывает доверие и 
уверенность в компетенцию организации.

Хуже того, скорость зависит не только от количества минут или часов, необходимых
для реагирования, но и от того, реагирует ли организация быстрее, чем ее
конкуренты. Поскольку найти и перейти к новому поставщику становится все проще
такое восприятие может привести к быстрой потере доли рынка.

Это стремление к увеличению скорости и оперативности дало старт в гонке
оптимизации доставки ответов, что в прочем не удивительно. Наиболее очевидным 
для команд доставки было начать искать любые источники разногласий при доставке
в окружающей среде, которые можно устранить.

Разногласия при доставке - это все, что снижает скорость доставки, пропускную
способность или оперативность реагирования. Поскольку существуют реальные 
выгоды, которых можно достичь, устранив разногласия при доставке, отрасль
наводнена решениями.

Для примера, Agile методологии Scrum и Kanban ориентиррованны на традиционно
длиные циклы доставки что делает изменение приоритетов доставки и вывод решений
на рынок медленным и громоздким. Разделение работы на небольшие части, как
предписывают эти методологии, также имеет дополнительное преимущество в более
быстром получении обратной связи, что может помочь сократить потери, вызванные
неправильным пониманием или несогласованностью требований.

Аналогичным образом, методы кодирования и усовершенствования инструментария
разработки релизов, которые сопровождают инициативы DevOps по непрерывной
интеграции/доставке, подталкивают разработчиков к более частым проверкам
кода в менее сложных структурах репозитория кода. Это, вместе с более быстрыми
циклами сборки, интеграции и тестирования, увеличивает количество
отзывов, которые разработчики получают во время доставки. Это позволяет
гораздо быстрее выявлять проблемы и решать их, пока контекст еще свеж в
сознании людей. Парное программирование, unit тесты и код ревью также помогают
разработчикам писать более элегантный код, одновременно улучшая знания кодовой
базы всей команды.

Переход от монолитных архитектур к более автономным модульным сервисам,
работающим на облачных экземплярах, которые можно запускать практически
мгновенно, потенциально значительно ускоряет процесс масштабирования и замены
устаревших и непригодных компонентов. Платформа-как-услуга (PaaS) и программные
решения с открытым исходным кодом позволяют разработчикам делиться решениями
общих проблем и заимствовать их, что еще ускоряет время, необходимое для вывода
решений на рынок.

Все эти улучшения по уменьшению разногласий звучат великолепно. Однако они имеют
ряд темных сторон, что немногие признают открыто, не говоря уже о том, чтобы
полностью их понимать. Это не только создает головную боль для сотрудников
организации доставки, но и мешает доставлять результаты, что беспокоит клиентов.

## The Downsides of Targeting Delivery Friction

The first challenge with fixating on eliminating delivery friction is that it is
easy for delivery teams to focus on building as much as they can as quickly
as they can rather than on trying to understand what the customer is trying
to accomplish and how their solution might help them achieve it. Some
believe that by simply delivering more you will eventually deliver
something customers find useful. Others who have been influenced by
traditional financial accounting often translate building more assets while
expending the same number of man hours as a financial win regardless of
their utility. Both are incredibly wasteful and count on success being little
more than a matter of chance.

This cycle of producing as much as you can as fast as possible is often
reinforced by delivery teams being evaluated on how much they can deliver
in a period of time. At first glance this might not seem like much of a
problem, but if you feel that your throughput is falling below expectations,
it can be extremely tempting to push friction elimination to the extreme by
cutting corners and take on unnecessary risks for the benefit of speed.

**March 22, 2016**: Open source developer Azer Koçulu unpublished
more than 250 of his own modules from the NPM package manager due
to a trademark disagreement. One of those, left-pad, was a mindlessly
simple module used to pad out the lefthand side of strings with zeroes or
spaces. Despite being only five lines long, left-pad became a critical
dependency for tens of thousands of projects, including widely used
Node and Babel. Its disappearance caused development and deployment
activities worldwide to fall over, exposing the brittleness of the NPM
system.

This push to release faster has also been far from inclusive. The
development-centric nature means that most improvements have focused on
making the lives of developers easier, often to the exclusion of others. QA,
and especially operational teams, often find themselves being pushed or
worked around for the sake of increasing delivery speed. As these groups
are usually measured by metrics such as service uptime and the frequency
and severity of production problems, they feel that this rushing is against
their best interests, jeopardizing their ability to perform their jobs
effectively. It also doesn’t help that many developers only have limited
awareness of, and often little interest in, the technology stack they are
deploying into. This increases the odds of something going wrong.

**January 31, 2017**: Source code hosting service Gitlab.com experienced
a major service outage due to the accidental removal of data from their
primary database server. While troubleshooting a production problem
on a secondary server, an engineer accidentally wiped the data in the
primary server’s database. None of the backups were in a state to be
sufficiently useful to restore all lost data. In the end it is estimated that 6
hours of data, including 4979 comments and 707 user accounts, were
lost in 5037 projects.

Operationally focused teams have pushed back. While they are not opposed
to reducing friction, they favor actions that minimize problems arising in
the first place. This has given birth to our second approach, managing
service delivery risk.

## Метод #2: Управление риском предоставления услуг

**Февраль 29, 2012**: В Microsoft Azure произошел массовый 36-часовой сбой из-за
ошибки високосного года в коде обработки сертификатов передачи SSL, который
управляет обменом данными между агентами хоста и их виртуальными гостевыми
агентами. Сертификатам были присвоены недопустимые даты, что привело к ошибкам,
которые в конечном итоге привели к сбою целых кластеров и переходу в автономный
режим. Эта проблема усугубилась попыткой отката кода, которая завершилась
неудачей из-за проблем несовместимости между кодом отката и более новыми
сетевыми плагинами. Это создало дополнительные осложнения, которые увеличили
продолжительность отключения.

Способность быстро реагировать на неудачу - это здорово. Но служба поддержки и
ИТ-операционные группы знают, что сбой может быть дорогостоящим, часто таким
образом, что другие не могут понять, пока не становится слишком поздно. Это не
только отнимает огромное количество ресурсов службы поддержки для реагирования
на производственные проблемы и решения их, но и подрывает доверие к заказчику
Лучше постараться избежать неудачи в первую очередь.

Команды, которые придерживаются такого мнения, вместо этого предпочитают пытаться
напрямую управлять рисками при предоставлении услуг. Все, что неизвестно, плохо
документировано или недостаточно понято, представляет собой неуправляемую
опасность, которая подвергает организацию риску неудачи.

Чтобы смягчить такие опасности, команды, которые уделяют приоритезируют
управление рисками, пытаются заранее определить все риски. Поскольку
недокументированные отклонения считаются крупнейшим источником неуправляемой
опасности, такие организации обычно начинают с того, что предписывают, чтобы все
действия по доставке осуществлялись в соответствии со стандартными <<лучшими
практиками>>. Эти практики тщательно документированы и включают в себя большинство
повседневных действий, охватывающих от технического обслуживания и устранения
неполадок до внесения изменений в инфраструктуру и сервис. Идея заключается в
том, что опасность недокументированных изменений можно свести к минимуму,
заставив все следовать строго документированному стандарту.

Зная, что не все необходимые изменения могут быть полностью стандартизированы,
нестандартные изменения проходят через процесс, который пытается сделать их
достаточно известными, чтобы можно было уловить и оценить риски, которые они
могут создать. Это делается путем документирования подробностей об изменениях, о
том, как они будут выполняться, и об их потенциальном воздействии, а затем
представления их в рамках процесса управленческого анализа и контроля, где они
могут быть рассмотрены ответственными сторонами, чтобы определить, приемлемы ли
какие-либо потенциальные риски, связанные с предлагаемыми изменениями. Если это
не так, то стороне, желающая чтобы внести изменение, необходимо отказаться от
него или внести в него изменения, чтобы сделать его приемлемым.

Документирование всех возможных стандартных практик является одновременно
утомительным и отнимающим много времени. Вместо того, чтобы разрабатывать все
эти процессы самостоятельно, большинство организаций перенимают их у одной из
многих популярных платформ управления ИТ-сервисами, таких как ITIL [^2].
Преимущество этих фреймворков в том, что они известны как лучшие отраслевые
практики, содержащие множество простых в использовании шаблонов и процедур, с
которыми знакомы многие ИТ-организации.

Они также широко признаны аудиторами за соответствие законодательству и 
нормативным актам.

[^2]: “What is ITIL,” https://www.itgovernance.co.uk/itil

## The Downsides of Targeting Service Delivery Risk

Implementing an industry best practice to minimize unknown variation and
enable responsible parties to review nonstandard changes before they are
pushed live sounds like a good idea. While all the extra processing might
introduce additional delivery friction, it seems like the sort that might help
the organization deliver more effectively. Isn’t having a service that
performs as expected a critical part of what a customer needs?

The problem with this approach begins with the fact that it makes four
flawed assumptions:
+ Work will be predictable.
+ People will correctly follow a documented process.
+ People in authority are capable of making effective decisions.
+ Industry-certified frameworks are less risky than noncertified or lesserknown approaches.

The first assumption is that the vast majority of work needing to be
performed in production will necessarily be predictable enough that all
necessary steps to get to a satisfactory result can be documented beforehand
without any need for variation.

This leads us to the second assumption, which is the belief that everyone
will follow all documented processes exactly without any variation. Even
though service management frameworks demand an audit trail, the vast
majority accept the change script and checklist that engineers follow as
sufficient evidence without any real programmatic means to ensure that
someone hasn’t miskeyed an action, done something out of order, or taken
shortcuts along the way.

There is also the reliance on “responsible parties” chosen to sit on a Change
Advisory Board (CAB) to review changes to determine whether the risks
they pose are acceptable. The members of these CABs are usually selected
from managers, heads of functions, and key stakeholders of areas affected
by the change. While CABs usually can catch such problems as scheduling
conflicts and communication gaps, they are usually far enough away from
the day-to-day details that it is difficult for them to have enough awareness
and understanding of the potential risks the changes pose to the ecosystem
and the dangers they might have for the customer.

The final problem with this approach is that it silently makes the
assumption that the current state is by default somehow less risky than any
nonstandard one. Not only is that not necessarily true, inaction can actually
increase the risk to the organization. I have personally seen organizations
get caught in this trap a number of times. Sometimes it is a critical customer
threatening to leave, or demands from some regulatory body under the
threat of major fines and legal action, if a particular change they absolutely
had to have was not made by a certain date. Other times a dangerous defect
has been found in a critical service, usually one involving some commercial
third party, that requires an extended downtime window to fix. In such
cases it can be extremely difficult to push through a change quickly, even
when not doing so can jeopardize the future existence of the organization.

## The Essence of Delivery

The customer inevitably finds themselves stuck in the middle of this
conflict between those who try to optimize for delivery speed and attempt
to manage risk. Naturally, customers want both quick delivery and no
faults. They simply do not understand why they cannot have both.
Meanwhile, each team thinks their approach is right and their goals should
be prioritized. Do the IT Operations staff not understand the time and
innovation pressures in the market? Is the work of the delivery team as
risky as is being implied? They both seem to care deeply about the success
of the company. How can these two technical teams have such opposing
views?

Can DevOps be a solution?

Before answering those questions, it is worthwhile to first consider the
purpose for why we are doing IT delivery in the first place.

At the most basic level, delivery is nothing more than a chain of interrelated
decisions. Like any decision, they are made to reach some sort of preferred,
or at least less bad, state than the current trajectory. In the context of service
delivery, they are made for the purpose of helping customers achieve their
target outcome.

A target outcome is a set of desirable or otherwise important conditions that
the customer wants to reach. Delivering to achieve a target outcome is more
than simply delivering an output or meeting a promise of a service
reliability level. Reaching a target outcome means functionally satisfying a
need, whether it is to solve an existing problem, minimize or prevent one
from occurring, exploit an opportunity, or to otherwise improve the current
condition.

The connection between an outcome and the tool or service attempting to
deliver it can be straightforward (“I want to stay informed about today’s
weather so that I know if I need to alter what I wear”), complex with many
solutions (“I want better global weather and market information so that I
can choose the best crop to farm”), nested (“I want better climate
information to design buildings that have a lower carbon footprint but stay
comfortable for its inhabitants”), or even part of an aspirational journey (“I
want to reduce man’s impact on the environment worldwide”). The target
outcome provides us with a direction or purpose to deliver toward.

In order to reach an outcome, you need to have some idea of current
conditions. What is the size of the gap between the current state and the
desired state? What are the means available that can be used to attempt to
close that gap, what obstacles might get in the way that need to be avoided
or overcome along the way, and how can we tell if we are making material
progress toward the target outcome? The answers together are what we call
our situational awareness, the idea that we know what is going on around
us to make better decisions more rapidly.

Any good decision maker reflects on the impact of the decisions they make.
Did they result in the changes we were expecting, and did those changes
result in progress toward the target outcome? Understanding what did and
did not go well and why helps us learn and improve our decision making,
and thereby our ability to deliver more effectively, in the future.

## Начало пути DevOps

**Март 2015**: Компания Woolworths Australia завершила шестилетний проект по
замене тридцатилетней собственной ERP-системы на SAP. У проекта отсутствовало 
понимание ежедневных бизнес-процессов, что быстро привело к сбою в цепочке 
поставок компании. Полки быстро опустели, пока поставщики и магазины пытались 
провести заказы через новую систему. Менеджеры магазинов потеряли возможность 
получать отчеты о прибылях и убытках за 18 месяцев, что ограничило их в 
управлении доходностью на уровне магазина. Эти неудачи привели к убыткам в 
размере 766 миллионов долларов и увольнению сотен сотрудников [^3].

[^3]:  “Three ERP failure case studies and what you can learn from them,” ERP Focus,
https://www.erpfocus.com/erp-failure-case-studies.html

К сожалению, делая акцент на результатах и времени работы, мы предполагаем, но 
не проверяем, действительно ли мы предоставляем решения, которые помогают 
клиентам достичь целевых показателей. Причина этого кроется в том, как мы 
привыкли работать. Большинству людей, работающих в команде разработчиков, 
кажется странным, что от них ожидают, что они сами будут выяснять, чего хочет
добиться заказчик и как ему это предоставить. Вместо этого мы ожидаем, что нам 
скажут, какие функции или требования должны быть предоставлены. Это устраняет 
множество двусмысленностей и избавляет от необходимости прямого контакта с 
клиентом.

Наличие отслеживаемых списков требований также делает гораздо более понятным 
процесс того, как нас будут оценивать. Менеджеры могут просто отследить 
результаты работы, например, сколько работы было сделано и насколько она 
соответствует тому, что было запрошено.

Несмотря на однозначность и простоту управления, отслеживание результатов дает 
мало стимулов работникам для проверки того, что клиенты могут использовать то, 
что было предоставлено для достижения целевых показателей. Тот факт, что 
менеджеров обычно оценивают по их способности выполнить требования в срок и в 
рамках бюджета, только усугубляет эту проблему. Создается впечатление, что любой
разрыв между тем, что было запрошено, и тем, что нужно клиенту, является 
проблемой клиента. Это далеко не устойчивая стратегия для любого бизнеса.

Отсутствие связи с целевыми показателями также меняет факторы, которые 
учитываются при принятии решений. Когда на первый план выходят оценочные
показатели, внимание переключается на любые действия, которые могут 
изменить их в лучшую сторону. Команды вскоре учатся быстро варьировать такими 
показателями, как скорость (разбивая работу на множество мелких заданий), 
количество ошибок (закрывая, деприоритизируя или переклассифицируя их в 
"особенности") и покрытие кода (создавая плохо построенные unit тесты, 
которые мало что делают для проверки основного кода), что снижает их целевую 
ценность. 

Так какое отношение все это имеет к DevOps?

Чтобы быть действительно успешным, внедрение DevOps должно устранить все 
барьеры и стимулы, которые мешают организации, предоставляющей услуги, помогать 
клиентам достигать целевых показателей. Для этого необходимо систематически 
отказываться от традиционных убеждений, привычек и подходов к предоставлению 
ИТ-услуг и применять более ситуационный, ориентированный на результат, постоянно 
обучающийся и совершенствующийся подход.

Как вы увидите, этот переход невероятно трудно осуществить. С привычками и 
убеждениями трудно расстаться. Для этого нужно много убеждать, особенно когда 
это бросает вызов традиционным системам, используемым для оценки работы людей и 
продуктов труда.

Лучший способ увлечь людей в это путешествие --- начать с того, чтобы сделать 
проблему видимой. Наилучший подход заключается в сведении командного процесса к 
его сути, к решению.

Один человек, пилот ВВС США и военный стратег по имени Джон Бойд, провел 
исследование, чтобы понять, что необходимо для оптимизации процесса принятия 
решений. Как вы увидите, его исследование дает практическое определение
для лучшего понимания самого процесса принятия решений и того, как улучшение 
этого процесса может помочь вам достичь целевых показателей, которые имеют 
значение.

## Резюме

Организации, предоставляющие ИТ-услуги, обычно считают, что они должны 
осуществлять выбор между оптимизацией производства и скоростью устранения трений
в команде разработчиков и управлением рисками путем минимизации неизвестных 
вариаций с помощью определенных практик и процессов проверки. Такие подходы не
только ошибочны, но и заставляют команды упускать из виду тот факт, что 
сфера предоставления услуг --- это предоставление решений, которые помогают
клиентам достичь целевых показателей. Для более эффективной работы команды  
должны рассматривать предоставление услуг как процесс принятия решений. Понимая, 
как принимаются решения, можно улучшить этот процесс для достижения 
целевых показателей, которые имеют значение.
