---
title: 'Instrumentation and Observability'
date: '2023-05-13'
draft: true
---

## Инструментирование упаковки и зависимостей

Следующая часть процесса --- это сами артефакты сборки. Как и инструментирование
разработки, полученная информация в основном полезна для технических команд.
Интересно, что относительно мало людей уделяют время изучению структуры этих
артефактов, способов их использования и подробностей их зависимостей.
Большинство просто помещают их на сервер или в хранилище без возможности
отслеживания.

Лично я предпочитаю размещать артефакты в репозитории, где они могут быть более
чисто версионированы, и где можно оставлять идентификаторы задач, информацию о
сборке и другие заметки. Это также место, где я предпочитаю уведомлять различные
инструменты автоматизации о любых обновлениях, которые могут быть использованы
для запуска следующих шагов процесса доставки. Многие инструменты для сборки и
оркестрации позволяют настраивать поиск такой информации. Это обеспечивает
дополнительную прослеживаемость артефакта как вверху, по цепочке сборки к коду и
идентификаторам задач, так и внизу, по цепочке развертывания. Также полезным
сигналом является использование меток для автоматических систем развертывания,
чтобы инициировать обновление целевой среды развертывания. При полном управлении
программным обеспечением и конфигурациями сред разработки в полностью
отслеживаемом и автоматизированном режиме также можно отслеживать пакеты с
такими условиями.

При правильной реализации все данные должны быть доступны для запросов и
отображения на панели управления в дальнейшем.

Помимо информации, связанной с конкретной версией артефакта, есть несколько
важных факторов, которые стоит учитывать и отражать в отчётах:
* **Насколько атомарны мои пакеты?** Атомарные пакеты означают, что вы можете
применять и удалять их в любой среде с небольшим риском того, что они оставят
следы или иным образом изменят среду таким образом, что это не сможет быть
автоматически отменено.
* **Насколько мои пакеты независимы от среды?** Многие организации привыкли
создавать разные пакеты для разработки, тестирования и продакшена. Это нехорошая
привычка, так как она создает потенциальные <<неизвестности>>, которые могут
вызвать проблемы. Эти различия следует преобразовать в параметры конфигурации
или флаги, которые можно будет установить при установке или запуске. Если есть
причина, по которой это невозможно сделать, и такие различия действительно
неизбежны, убедитесь, что пакеты, зависящие от среды, отражены в отчете вместе
со своими причинами, потенциальными рисками и способами их тестирования и
смягчения.
* **Какие зависимости имеют мои пакеты?** Зависимочти --- это неприятные вещи,
которые часто не получают должного внимания. Это особенно верно, когда они
внешние, или, что еще хуже, получены через что-то вроде NPM или Maven. Эти
зависимости должны быть учтены и отражены в отчете, с применением смягчающих
мер, где это возможно, например, иметь локальные копии, чтобы избежать их
исчезновения или скрытых проблем.

Каждый из этих факторов направлен на выявление и отслеживание уровня вашей
подверженности потенциальным <<неизвестностям>>. Обычно я размещаю эти вопросы
на панели управления или вики, чтобы каждый мог быть в курсе их состояния и
того, насколько хорошо они в настоящее время управляются. Целью должно быть
минимизировать эти риски, либо устранить их, либо выделить их опасность.

## Instrumenting Tooling

Increasing reliance on tooling and automation is generally a good thing. When
done well, it reduces variability and makes us think about ways of making our
ecosystem more repeatable. But how many of us instrument our tooling to capture
and track what has been done with it, how it performed, and what the end results
were? How many of us create traceable links between tooling actions, the
artifacts they used or interacted with, and any tasks behind their initiation?

Capturing this information is very useful, particularly to those who are heavily
reliant on the expected tooling performance. This information provides
visibility of the overall health of the tooling and how well it is performing
its job. If you have been unfortunate enough to have had tooling die or
misbehave and leave your ecosystem a mess, you probably know how useful any
records of what happened and why are for cleaning up from the wreckage and
preventing it from happening in the future. I have seen many cases where
monitoring systems get overloaded and do not report in a timely way. I have also
discovered build tools, backup jobs, and other maintenance activities that broke
in silent ways that were not discovered until disaster struck.

Instrumentation can help you spot inconsistencies before they become problems.
Instrumentation can also help you spot potential improvements and even size up
their likely value. A good habit to get teams into is scheduling a regular
instrumentation and reporting review to get teams in the habit of reviewing how
well they understand what is going on with tooling, as well as to find any areas
where instrumentation missed or was not sufficiently effective to proactively
spot deteriorating conditions. Often this can help the team discover
inconsistencies within or between various tools, or places where it was
misinterpreted, that can be improved. 

## Instrumenting Environment Change and Configuration Management

An extremely common and generally good practice in IT is to create change
tickets whenever you make an environment change in production. It forms a good
record to know when changes were made, who made them, what changed, and why. 

But how many of us actually capture in any great detail what was actually done,
how exactly it was done, and the differences between the original and new
states? How many of us go back to change records with any regularity to compare
current or past ecosystem dynamics with changes that have been made? 

As the deliverer of services, the changes that you make are arguably the most
notable and important activity you do that affects the dynamics of the
ecosystem. This is why it is important to capture the changes you make, as well
as the differences between the existing and new configuration state. Doing this
is very important for building shared awareness, as well as aiding in
troubleshooting any subsequent incidents a change causes in a way that the root
cause can be understood. Documenting changes in this way is so important that I
always encourage teams to put up links to the details of the last five to ten
changes on the front page of any incident reporting tool. I have found time and
again that this not only helps whomever is fiddling an incident to reduce the
time to recover, but also helps those involved in the change to address any of
the root causes in a much more succinct way.

Unfortunately, most delivery teams do a terrible job of capturing the full
details of any change in a way that can both maintain shared awareness of
ecosystem state and be used as a complete audit trail. It is often done so
poorly that many operational teams are resistant to frequent production changes.

The most common way that change information is missed occurs when changes are
performed manually. Such untracked manual changes sometimes happen when people
have to jump in to troubleshoot a problem to get things to work. Other times
there is some commercial software being used that forces changes to be made by
hand through admin consoles or other difficult-to-script mechanisms. Both of
these result in details often being missed and should be minimized or tracked
wherever possible. I have seen teams save shell histories or use scripted test
tools that can manipulate GUIs to have a more repeatable and trackable record.

Another surprisingly common challenge occurs when work is automated but the
tools performing the change do not capture the prior configuration state, what
transpired when the change was performed. Some fail to check the end result of
the change to see that it matches what was expected. I have personally seen
deployment tools that shuffled around files or symbolic links, appended things
to configuration files and the like, or shuffled around some containers, and
then declared victory without actually seeing that the actions resulted in what
was expected. In some cases, the tools ignored errors, from permissions
conflicts to files either not being where they were supposed to be or not being
complete, and moved on to the next step. Other times service APIs failed to come
up properly or responded in unexpected ways. Even when the errors are captured,
few bother to look at them until something blows up, if at all.

Perhaps the biggest and most common issue is that while we might track changes
made to production services, very few of us do the same for test and development
environments, or for changes made to supporting services such as monitoring or
backup services. In fact, it is extremely common for changes to be made by an
untracked hand in all of them.

The other challenge is that few of us actually capture and compare the
configurations that exist in development, test, and production to analyze their
differences and understand how these differences might create different dynamics
in each. Did the package going to production pass through the development and
test environments? If not, was it installed in them afterward? This does not
mean that development and test environments need to have exactly the same
configurations as production, or even that they need to have the same
configuration as each other. Most of the time it is nearly impossible for that
to be the case. However, accepting that there are differences doesn’t mean that
you shouldn’t bother to know what those differences are, or check and take into
account how they might alter behavior. Overlooking or ignoring these differences
creates yet more unnecessary and often problematic unknowns.

Capturing, reporting, and analyzing such information allows you to have a much
better grasp on what you have within your environment. Creating links between
all the artifacts and activities, from task tickets to the change tickets at the
end of the cycle, allows you to walk your ecosystem, beginning at any point, to
understand and build context into what is happening in it.

## Instrumenting Testing

When done well, testing will contain a treasure trove of useful information. It
can provide all sorts of insights, many that go beyond exposing potential risks
caused by defects in the code. One of the most important ways that testing
instrumentation can help improve shared ecosystem awareness is to use it to
capture how service changes will likely behave in the target operational
ecosystem.

Using automated testing tools and testing instrumentation in this way might
sound unremarkable at first, or even a restatement of what most believe testing
teams do. The difference is that it is not aimed at “quality assurance.” For
one, the premise of quality assurance is broken. QA does not really assure much
of anything. It mostly tells you what bugs were encountered during testing.
Others likely exist that were simply not encountered.

This doesn’t mean that such testing shouldn’t be done. Instead, testing should
be oriented in a way that tries to improve your understanding of how services
will behave under different scenarios and conditions in order to improve your
ability to respond effectively to various service behaviors. Testing should also
help you more easily figure out what conditions are likely occurring when
certain service behaviors are seen.

I also like to use testing to better expose the service hazards created by
brittle code found through development instrumentation. This helps expose more
details of the “size of the prize” by investing in refactoring or a more
thorough overhaul of a problematic area.

To make testing instrumentation maximally useful, I try to augment it with
production instrumentation tooling whenever possible (and vice versa).
Monitoring and service instrumentation, log analysis tools, nondestructive test
tools, synthetic transaction tools, and so forth can provide a quick way of
being able to compare like-for-like results. Exposing test cases and test case
results in a way that can be compared with what is experienced in the production
environment also allows for both test and operational instrumentation to be
retuned in order to make sure that the right dynamics are looked at and compared
in the future.

Another useful item to capture are the deployment configuration differences
between test environments and production environments. Doing this in a way that
can also capture and denote the various behavior and performance differences
that the configuration differences between the environments create allows you to
verify your understandings of potential points of friction and bottlenecks
caused by deployment configuration differences. This allows you to have more
confidence in what levers can be changed when such conditions are triggered in
production.

## Instrumenting Production

Few IT professionals would argue that instrumenting production is not sensible.
Learning the best way to do so is probably the main reason you decided to read
this chapter in the first place. The production environment is an extremely
target-rich environment for making your ecosystem observable. It is where your
users meet your services, and thus is the place where you should look to
understand how those services are helping customers meet their target outcomes.
Many organizations have realized this, which has given birth to a great deal of
interest and investment in Big Data analytics solutions.

What is often missed is that building an accurate level of understanding of this
dynamic in the most holistic and efficient manner requires more than what can be
done using more traditional monitoring and logging approaches. This is true even
when supported by fancy Big Data analytical tools.

If your goal is to improve your understanding of your production ecosystem in
order to make more effective decisions, there are a number of instrumentation
areas that are worth considering that are often overlooked, as described in the
following sections.

## Queryable/Reportable Live Code and Services

One of the biggest problems with serverless services and the like is that
instrumenting and tracking them in traditional ways isn’t all that
straightforward. One of the best ways to overcome this is by placing queryable
hooks in your services directly that can give you an idea of what is going on.

You do not need to have particularly advanced hooks to start. Even something as
simple as a hook that responds to a flag asking “Are you alive?” is a useful
start. This can easily be expanded to “What are your health vitals?” all the way
to more debugging-like information such as “What is happening with these
users/sessions/data as it traverses the service?” Other ways to instrument and
track what is happening is to use capabilities like Java Management Extensions
(JMX), or having services register themselves and push out regular metrics in a
pub/sub sort of way to a central bus or point where they can be collected and
analyzed.

None of these approaches are particularly difficult to implement. What makes
such capabilities worthwhile is that implementing and using them can reduce a
lot of the complexity and time lag that occurs with trying to do the same thing
through a more traditional logging mechanism. The values they return can be made
to conform to a usable standard, which allows the values to be quickly put up on
a dashboard for analysis to find any disparities across service instances.

When done well, instrumenting services and user interfaces can enable you to
observe users and user sessions in near real time as they move across the
service ecosystem. This is a particularly handy capability to have when
analyzing problems being experienced by one or a small subset of users.

## Presenting Task, Change, Incident, and Problem Records Together 

A lot of service management tool vendors talk about the power of using their
tooling ecosystems being in how everything connects together. They will include
ticketing systems with workflows, configuration management databases (CMDBs),
and even monitoring. The problem is that the vast majority of the data is either
buried in its own silo or isn’t particularly easy to put together in views that
are useful to you and others who need it.

I have found that it is often extremely useful to present all of this
information together. This is especially true with change information, which
should be immediately viewable to anyone who is fielding an incident. To do
this, I generally favor using a simple web page or some other equally
uncomplicated mechanism that is easily viewable whether you are on the go or
sitting at your desk.

While keeping change and incident records together is extremely important, I
also like to look for ways of easily tracing the chain of relationships from any
point in my ecosystem. Having the ability to start, for example, with a package
or configuration and walk both back to the series of tasks that created it and
forward to where it was deployed and how is extremely powerful. This approach
allows you to pull together information you might need in the right context at
the right time. The cross-seeding, as mentioned earlier, is critical to this;
however, making it easy to use also means that it will be used much more
heavily. Creating a simple system that allows you to easily walk the ecosystem
is key to this.

Another useful thing to do is to present the data and trends that might be
interesting to technical and nontechnical audiences regularly. This can be
everything from failed changes and aspects of changes that created unexpected
service behavior to incidents that took far longer than normal to handle. This
presentation needs to be done in a way that can spur improvement, not in a way
that get turned into a blame game. Blaming, as we know, encourages people to
hide data and disconnect relationships. I tend to focus most reporting to those
closer to the action but allow it to be packaged up in a blameless way for
delivery to upper management when help and support are needed.

## Environment Configuration 

We talked about configuration management and deployments earlier. But are you
aware of everything that is in your delivery ecosystem? Do you know how quickly
and consistently you can rebuild and redeploy each part of your delivery
ecosystem from scratch?

Knowing what you have in your delivery ecosystem is more than knowing the
versions of the software installed or very basic elements like network addresses
and the like. It is about knowing and regularly reviewing exactly what the
ecosystem is composed of. I have found the best way to discern this information
is by rebuilding as much of your ecosystem as you can regularly.

By “rebuilding” I mean more than moving a bunch of containers or Virtual Machine
Disk (VMDKs) files around. I mean being able to reinstall the full stack,
configure it, and put it into production. Knowing how quickly and consistently
you can do this enables you to know how long it might take to rebuild any
component in an emergency.

Rebuilding also acts as a catalyst for flagging situations where there are
single points of failure in the rebuild process. Being able to rebuild this way
also means that you do not have to count on some discovery tool to try to learn
and monitor what you might have, if it can figure it out at all. It also means
that if you fall foul of a security breach such as a ransomware attack, you can
have some confidence regarding how much of the stack you can burn to the ground
and rebuild rather than lose.

Another important part of tracking the environment configuration is that you can
build a way to capture and understand what is changing in your environment and
how it is changing. It also allows you to spot suspicious or unauthorized
changes quickly.

I try to look for opportunities to regularly do rebuilds, as well as build
dashboards that record friction points and other danger hot spots that the team
can try to remove. These should be reviewed at very regular intervals, at least
as often as strategic reviews, where goals can be set and actions can be taken
to improve the situation.

## Logging

Logging is a traditional and important part of every ecosystem; however, how
often do we actually examine those logs? How trustworthy are they in telling us
what we want to know? How structured and readable are they?

I approach logging in two streams: 
*   **Operational usefulness:** Logs that are not trustworthy, that are
difficult to parse, or that simply do not provide any value should be
highlighted. What about them is not useful, trustworthy, or easy to parse? What
is the effect on operational support? Capturing and reviewing this information
allows you to address the situation. You sometimes might find that there are
better ways of obtaining the same information, or that there is so much spurious
noise that much of what is currently logged should be shut off or tuned way
down. Logging is definitely one of those places where you can have too much, too
little, and too irrelevant.
*   **Longer-term utility:** What do the logs convey, and who can use that
information? Are there any legal or regulatory rules that might affect their
handling or storage? Are they easy to obtain and process? How long do they take
to process into a useable form, and why? What is their accuracy? Highlighting
and tracking such logs and log data entries, especially those that are important
or may diverge from the needs of those looking to consume the information, helps
identify potential awareness lags that might reduce the efficacy of decision
making. 

## Monitoring

Monitoring is one of those things that we all do. It makes sense. But much like
the concerns about service instrumentation that my DevOps friends expressed, how
useful is all of the monitoring to you? Does it always tell you what you need to
know in a timely way with enough context to act?

Even though much of the monitoring data organizations collect is subpar at best,
many of us tend to feel that more is better. We will often collect alerts and
statistics that we almost never look at, let alone use, leaving monitoring
systems looking like the digital equivalent of a hoarder’s garage full of old
newspapers.

The best way to approach monitoring is by going through it to determine not only
its accuracy but also who will consume the data, for what reason, and what
decisions they are likely to make based on it. If there are better, more
accurate, or more timely ways that information can easily be obtained, then the
old method should be replaced with the newer, better one. If monitoring triggers
alerts that do not get looked at until several pile up or something else occurs,
that issue should be addressed. Getting too much useless information is
sometimes worse than not receiving anything, as it desensitizes you to the
information.

Monitoring tuning should be part of regular tactical review. This should be done
especially after incidents where it was not sufficiently effective in helping
proactively catch problems before they caused problems. There is also value to
look at how to improve the overall efficacy of monitoring at strategic reviews.
Monitoring needs to be continuously tuned and improved as dynamics change.

Staff should also be encouraged to not grow to accept the buildup of noisy or
useless monitoring. 

## Security Tracking and Analysis 

Security tends to be the source of policies that create inconveniences that
often seem far larger than the security value they provide. However, in the
services world security is necessary to protect both your organization and,
ultimately, your customer; however, security also has a side benefit that is
often overlooked. Security can provide an even stronger impetus to capture and
track what is in your ecosystem. This can be used to better understand ecosystem
behavior caused by various states and user activities that can improve your
overall awareness.

Many security techniques and instrumentation tend to either sit on top of other
tracking mechanisms, like logs, environment configuration tracking, and the
like, or have their own specialized tools to monitor such things as peculiar
traffic and threats. These mechanisms are looking for things that look odd or
abnormal, which can be done in two ways.

You can use these mechanisms to look for a list of activities and states that
reflect known security threats and violations. This is the way that most
organizations go about it, as it is fairly straightforward to do, but it is not
the best approach to count on entirely as it assumes by default that there has
been no unauthorized access. This is not the best stance for most organizations,
especially those that are a big or interesting enough target. This approach also
does not account for the fact that a lot of the more nefarious security
violations begin from the inside, either from an internal bad actor or someone
who has had their credentials compromised in some way.

The other way to approach security is to try to capture and track the state and
activities of as much of your operating ecosystem as possible. This includes
tracking configuration and data changes, network traffic, and the like, leaving
tempting honeypots around to try to lure bad actors to learn more about them so
that you can better protect the more sensitive parts of your ecosystem.

To be able to track this information, capture and track the configuration and
changes that you make so you can easily query and check for any unknown
differences. This should capture both potential security threats and behaviors
(whether from errant tools or unfollowed processes) that aren’t being tracked.

Highlights of such data should be made visible to help teams and the
organization improve. 

## Service Data

The last area that you should consider consists of the structure, storage, and
accessibility of service data. This includes both customer data and other forms
of data used to drive your services.

Even though most Big Data programs look to heavily mine service data, relatively
few organizations spend much time thinking about the overall architecture and
structure of the data they have beyond what is absolutely necessary to drive
services. Such data inevitably grows organically into various piles scattered
about the ecosystem. This results in duplication and mismatches that make the
data far more difficult to piece together and understand than what it
represents. It also makes it more difficult to obtain the information to
analyze.

To reduce these sorts of problems, it is best to put two mechanisms in place as
part of your delivery process: 
*   Have a rotating role that builds and owns the architectural map of what data
is stored where, in what way, and by which applications and services it used.
Duplicates and mismatches should be found and eliminated wherever possible.
*   Have data architecture and design be considered as part of the delivery
process to begin with. Where should data live? What should access it? Have
duplicates been accounted for and minimized wherever possible? How might data be
extracted, to where, and for what purpose? This process does not have to be
particularly heavyweight. In fact, it is far easier to manage smaller changes
than bigger ones. 

## Pulling It All Together

Putting in place the right instrumentation to deliver the right information to
the right audience to meet their objectives can sound really difficult. Where do
you start? How do you keep it going? How do you improve?

Sometimes it is difficult to see the best path forward, especially when you are
very close to the problem and used to the ways you have always done things.

Fortunately, IT is far from the only industry that faces this sort of
instrumentation problem. Many other industries require instrumentation because
they also have high availability requirements, highly unpredictable demand, and
unforgiving high sensitivity to failure. Looking at how someone in a very
different context copes can often help you step back and more objectively look
at your own world.

The industry that I personally like to walk through is one that most of us
interact with almost every day but think little about: _the wastewater
management industry_. 

## Instrumenting a Wastewater Ecosystem

<!-- image here, p.366 -->

Few would argue that a service that both takes care of your waste and keeps your
neighbor’s out of your home is not important. Yet how many people think about
the complexities of building and managing such a system?

I had the opportunity to see one such system run by the City of Los Angeles up
close. The smells were predictably nasty, as were the daily safety hazards
employees were exposed to working around a live network of sewers, wet wells,
digesters, and holding ponds. But what most would assume would be a very
pedestrian and often forgotten-about service soon proved to be anything but.

Like most cities, LA provides water and sewerage services to residents and
businesses through a network of pipes and tunnels running throughout the city.
People not only expect their water to be safe and whatever goes down the drain
to not come back up, but also expect the streets to be free of waste. Sewers are
also places where, without active monitoring and dispersion, harmful gases can
build up, creating hazardous clouds and at times explosive conditions.

Los Angeles, however, faces far more challenges than the average municipality.
The greater metropolitan area covers over 4800 square miles of arid and semiarid
terrain crossing a complex topology of mountains and valleys. The area is prone
to both drought and flash flooding. Both are bad for sewage systems. The former
can leave waste building up in the pipes. The latter can overwhelm the waste and
runoff systems, leaving hazards filling the streets, and sometimes even people’s
homes. To add to the complexity, LA also has to contend with additional natural
hazards like earthquakes, landslides, and wildfires. If that isn’t difficult
enough, the water, sewage, and storm systems crisscross a maze of local
authorities that often do not see eye to eye, let alone have both the desire and
means to cooperate.

Despite these challenges, I witnessed a dynamic system in action that has become
one of the most advanced in the world. Not only is sewage in the streets
exceedingly rare, but runoff and waste discharges have over the years been
reduced by over 95%. What is more, the system has improved water quality and
delivery capabilities, dropped total water consumption in real terms, and
reduced the amount of coastline fouling and other environmental problems. This
has been accomplished despite continued population growth and change across the
region.

How does the LA Sanitation department do it?

For one, they realized there was no way the ecosystem would survive if the city
took the approach of building a static design of a network of pipes in the
ground. A single storm or a rogue factory illegally dumping hazardous materials
into the system could destroy large sections of the region. They needed to
actively learn about the ecosystem and the changes going on within it, all while
constantly trying to find new ways to improve.

The department stayed focused on the target outcomes: keep wastewater out of
people’s homes and the streets, and minimize health hazards and pollution, all
while looking for opportunities to recycle and reuse water along the way. They
began by trying to understand more about the environment they were operating in.
They scattered sensors and ran tests throughout the network and across the
region. These help them understand how water flows on the surface, underground,
as well as through the drainage and sewerage networks. These check not only
capacity and flow rates, but also monitor for hazardous concentrations of
everything from explosive and poisonous gases to problematic materials flowing
through the system. They also look at how the entire system is performing, from
the sewers, pump stations, and treatment plants to the behaviors of the people
who use and operate them.

This monitoring and tracking is fundamentally different than traditional IT
monitoring and service workflow management. Unlike IT, they were not focused
primarily on spotting anomalies to react to. It can take months or even years to
change a storm channel or add sewer capacity, making even the most backward IT
procurement process seem lightning fast. Instead, they go beyond IT by seeking
to actively understand and shape the ecosystem itself. Information is constantly
analyzed and used to continually improve the efficacy of everyone’s
understanding of the network.

This approach and mindset does more than improve responsiveness to potential
failure scenarios. It allows for friction points and risk areas to stand out and
be better understood. Anything from a new factory to a reformulation of a
commonly used bath gel can easily change the dynamics of the entire network.
They also look at local and regional hydrology and surface drainage patterns to
understand and predict potential runoff hazards. Active harvesting of
information helps build an ever more accurate understanding of the operating
environment and any relevant patterns it might contain. This improves the
targeting of everything from high-value infrastructure improvement to local
policy and ordinance changes. They even go so far as to engage in planning and
permitting to understand how proposed changes might affect the system, proposing
solutions that help keep the ecosystem healthy.

As sophistication has increased, so have the public demands that have been
placed on the service. If water is so scarce, can runoff and wastewater be
harvested and made reusable, or even potable? Can waste be somehow recycled and
put toward a useful cause that reduces its negative environmental impact?

The district tries to stay attuned to these demands. They constantly look at
revamping storm drainage, sewage, and water delivery methods to maximize water
reuse. Not only has wastewater treatment improved, but the district has learned
that they can take advantage of some unique features of the LA basin to improve
water reuse. Much of Los Angeles sits on top of alternating aquifers and oil.
They realized that they can confidently inject recycled gray water into the
ground at strategic locations where the soil composition will further treat the
water while simultaneously recharging underground aquifers that are already used
as potable water sources. This maintains local water sources while stabilizing
the ground to reduce the risks of subsistence and saltwater intrusion, as well
as minimizing underground movements that may potentially activate an earthquake
fault. These efforts have been so successful that not only have waste levels
been lowered, but actual water usage has been reduced in real terms even as the
population has grown.

Recovery does not end with water. Methane from the network is captured and used
to generate power, all while efforts are put in place to recycle as much of the
rest of the waste as possible. This is an immensely challenging task,
particularly as there is no real way to force users across the ecosystem to
report on what they flush down the drains, let alone how and when they use the
network.

The result of all of these efforts is that those running the ecosystem feel as
if they understand the heartbeat of the city. They can see the patterns of usage
every day, from a steady increase in flow from residential districts as people
get up in the morning, to a shift to office and retail parks and industrial
districts as people to go to work, and back to residential districts in the
evening. Similarly, market trends and seasonal patterns of factories and offices
become apparent as flows and the makeup of their contents change. Even the
impacts of public events and weather patterns can be identified and understood
within the signal noise of other events occurring throughout the network.

All of these observations allow for better targeting and more proactive response
to change, helping surprises become increasingly rare. This knowledge can then
be fed back into city planning, zoning, and permitting, uncovering potential
problems before they have a chance to damage this otherwise hiddenaway
ecosystem. 

## Instrumenting an IT Ecosystem

You can use the same sort of thinking described in the previous section to build
in a similarly powerful understanding of your IT ecosystem.

Later in my career, I worked for a company that provided a wide variety of web
and Internet-based services. Performance and usability expectations differed
considerably. For instance, users were far more sensitive to response and
quality issues with streaming media than, say, an RSS feed. However, there were
also important differences between markets. Not meeting these expectations had a
significant detrimental effect to both market reputation and the bottom line.

Being heavily consumer-facing, many of our services were also vulnerable to
extreme “Slashdot-effect” style traffic spikes. There were times when traffic
would suddenly grow by 1000–100000 times the normal flow. Without sufficient
available infrastructure and a quick response, everything could quickly
collapse. However, the business case for acquiring all the extra capacity was
not always clear-cut. It was prohibitively expensive to have so much excess
remain idle most of the time, and as service performance characteristics change
over time, it was not even clear that capacity acquired now would work
effectively in the future.

With so many shifting variables, we needed to find ways to instrument to better
understand the dynamics of our ecosystem.

On the service side, we started to build in hooks that allowed us to peer into
the health and performance characteristics of the services themselves. We
matched these with other operational instrumentation such as logs and monitoring
information to provide additional clues of how various events would affect the
dynamics of the operating ecosystem.

We also put the same sorts of instrumentation in place in the development and
test environments, where we looked for the sorts of events and load profiles
that might create performance problems. This allowed us to then work out various
options we might have for handling such challenges, from more traditional
capacity scaling to disabling various features and making certain elements
static or cached.

We then began to instrument up the amount of time and variability involved in
responding to changing events. This included turnaround time and accuracy for
responding to an event, the time and potential risks involved in changing the
capacity of various service elements, time and complexity involved in disabling
or changing features, time and potential problems with moving and restoring
data, and the like. This gave us some indication of our costs of delay that
could be used to guide investments.

Another element that was important to all of this instrumentation was
understanding customer expectations and usage patterns. While it was never easy
to spot coming load spikes or gauge customer satisfaction with a service, we did
find a number of useful clues that helped. For instance, we noticed clear time
windows during the day when some services were used more heavily than others. We
could also see a number of clues of customers becoming frustrated with service
performance.

With all of this information, we started finding places to optimize. We began to
heavily automate our ability to deploy and reconfigure service instances to
improve our response speed and flexibility. We used customer usage patterns to
dynamically rebalance the capacity of various services throughout the day. For
elements that had higher friction profiles like data, we looked to
opportunistically replicate and reposition data to improve our responsiveness to
potential events.

We also regularly reviewed the quality and timeliness of our instrumentation
data. This allowed us to continually tune what we had, find new places to
instrument, and build reasonably accurate indications of the likely return on
investment (RoI) for such work. 

In the end, we became far more responsive to ecosystem changes. We also managed
to improve our overall utilization rates to maximize the value of our
infrastructure and development investments. Being more proactive also greatly
improved team morale and creativity. 

## Summary

Instrumenting your delivery ecosystem to make its dynamics observable is
critical to establish the situational awareness necessary for decision making.
But to do it effectively you need to understand what the right data is for the
audience consuming it, and what they are consuming it for. We in IT do a lot of
things that make this difficult, from hoarding the wrong data to picking up data
that is distorted by insufficient accuracy, timeliness, and biases. By building
the right instrumentation and review mechanisms in your ecosystem, you can find
and minimize these distortions to get you on the right track.