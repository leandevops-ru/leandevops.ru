---
title: 'Введение'
title: 'The Problem with IT service Delivery'
date: '2023-03-04'
draft: false
---

In the fast-moving hypercompetitive world of today, innovation is as crucial
as it is hard. People want ever better solutions faster. This requires pushing
the envelope, taking chances into the new and unknown. While such bets do
not always succeed, playing it safe risks a slide into irrelevance.

**September 23, 2010**: Blockbuster Entertainment filed for Chapter 11
bankruptcy protection after suffering from challenging losses due to
strong competition from Netflix and other video on-demand services.
Despite having a commanding lead in home video rentals and an offer
to enter the video on demand business as early as 1999, Blockbuster
failed to foresee the growing popularity of mail-order and streaming
movie services.

Few industries face expectations for innovation as high as those the IT
industry faces. From smartphones and the applications and services that
bring new capabilities instantly to our fingertips, to the advanced analytics
engines that help us understand ourselves and the universe around us ever
faster and more accurately, we have grown to expect a continuous stream of
revolutionary breakthroughs that both titillate and improve the quality of
our lives.
But this increasingly rapid flow has hardly been cost free.

**January 3, 2018**: Security vulnerabilities Meltdown and Spectre were
revealed to the world. Each exploits weaknesses in the speculative
execution features found on most modern microprocessors, allowing an
attacker to reveal and extract targeted private data. Being at the
hardware level, these vectors thwarted both system and virtualization
security protections. This created particularly damaging risks to cloud
service providers and their customers. IT providers dependent upon
legacy software were left with the choice of painful upgrades and
patches or remaining vulnerable. To make matters worse, many of the
initial firmware, operating system, and virtualization patches were
haphazardly created and rolled out. These created instability, unwanted
reboots, and occasional bricking of systems. Patches also degraded
system performance between 2 and 19 percent.[^1]

[^1]: “Speculative Execution Exploit Performance Impacts - Describing the performance impacts to
security patches for CVE-2017-5754 CVE-2017-5753 and CVE-2017-5715,” Red Hat:
https://access.redhat.com/articles/3307751

Each innovation brings with it additional layers of technology, increasing
the level of complexity in the operating stack. With so many moving parts
produced by an ever growing list of providers, it is difficult for any one
person to definitively know everything there is to know about an IT stack
they rely upon or are responsible for. Like a building with an unknown
foundation, this complexity creates a level of uncertainty that makes
innovation more difficult. It also threatens to add fragility that drives up the
likelihood of failure.

At the same time that technical stacks have increased in complexity,
customer patience for failure has eroded. As demands for using IT solutions
to solve problems have grown, IT has become deeply embedded into nearly
every aspect of our lives, large and small. Now everything from our
household appliances and cars to banks and emergency services relies upon
an increasingly intricate web of software and IT hosted services to function.
Any one failure can cascade into something both crippling and costly for
both the user community and the provider. What constitutes a failure has
also expanded to include not just faults and broken functionality but also
poor usability and missed expectations.

**August 1, 2012**: The major market maker Knight Capital Group
suffered from an error in its SMARS algorithmic router software that
led to a $460 million trading loss over the course of 45 minutes. This
exceeded the total assets of the firm, eventually pushing the company to
be acquired.

Solving for innovation speed, reliability, and expectations matching has
kicked off a competition between two approaches: reducing delivery
friction and managing service delivery risk. This competition is important
as it affects how organizations approach DevOps, and ultimately its chances
for success. However, while each approach does address some important
factors, each also contains a number of serious flaws. These not only cause
frustrating delivery problems themselves, but can actually hinder the
organization from achieving the single most important aspect of service
delivery: effectively helping customers reach their target outcomes.

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

## Beginning the DevOps Journey

**March 2015**: Woolworths Australia completed a 6-year project to
replace a 30-year-old in-house ERP system with SAP. The project’s lack
of understanding of day-to-day business procedures quickly led to the
breakdown in the company’s supply chain. Shelves quickly became bare
while suppliers and stores struggled to get orders through the new
system. Store managers lost the ability to get profit and loss reports for
18 months, limiting their ability to manage profitability at the store
level. These failures contributed to a $766 million loss and the layoff of
hundreds of employees.[^3]

[^3]:  “Three ERP failure case studies and what you can learn from them,” ERP Focus,
https://www.erpfocus.com/erp-failure-case-studies.html

Unfortunately, in emphasizing outputs and uptime we assume but do not
check that we are actually delivering solutions that help customers get to
their target outcomes. The reason for this comes back to how we have
become accustomed to working. It would seem odd to most people working
in delivery to be expected to figure out themselves what the customer is
trying to achieve and how to deliver it to them. We instead expect to be told
what features or requirements need to be delivered. This removes a lot of
ambiguity, and eliminates the need for any direct customer contact.

Having trackable lists of requirements also makes it far clearer how we will
be evaluated. Managers can simply measure delivery outputs like how
much work was done and how well it aligns to what was asked for.

While unambiguous and easy to manage, measuring the delivery of outputs
provides little incentive for workers to check that customers are able to use
what was delivered to reach their target outcomes. The fact that managers
tend to be measured on their ability to deliver requirements on time and on
budget only compounds this problem. It is as if any gap between what was
asked for and what the customer needs is the customer’s problem. This is
far from a sustainable strategy for any business.

Being disconnected from target outcomes also changes what factors are
considered when making delivery decisions. With evaluation metrics taking
center stage, focus turns to any actions that can turn them favorable. Teams
soon learn how to quickly game measures such as velocity (by breaking up
jobs into many small tasks), bug counts (closing, deprioritizing, or
reclassifying them as “features”), and code coverage (creating poorly
constructed unit tests that do little to test the underlying code), undercutting
their intended value.

So what does all this have to do with DevOps?

To be truly successful, a DevOps implementation has to remove all the
barriers and disincentives that prevent the delivery organization from
helping customers reach their target outcomes. This takes systematically
moving away from traditional beliefs, habits, and approaches about IT
service delivery and establishing a more situationally aware, outcomebased, and continually learning and improving approach.

As you will see, this transition is incredibly difficult to do. Habits and
beliefs are hard to break with. This takes a lot of convincing, especially
when it challenges traditional systems used to assess people and work
product performance.

The best way to take people on this journey is to begin with making the
dysfunction visible. The best approach is to strip the delivery process back
to its core, the decision.

One person, a US Air Force pilot and military strategist named John Boyd,
pursued such a search in order to understand what is necessary to optimize
the decision-making process. As you will see, his journey provides a useful
lens to better understand the decision-making process itself and how
improving your decision making can help you deliver the target outcomes
that matter.

## Summary

IT service delivery organizations commonly feel that they must choose
between optimizing for output and speed by targeting delivery friction, and
managing risk by minimizing unknown variation through defined practices
and review processes. Not only are such approaches flawed, they cause
teams to lose sight of the fact that service delivery is about delivering
solutions that help customers achieve their target outcomes.
To deliver more effectively, teams should instead think of service delivery
as a decision-making process. By understanding how decisions are made,
decision-making can be improved to deliver the target outcomes that matter.
