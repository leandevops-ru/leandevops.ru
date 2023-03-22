---
title: 'Friction'
date: '2023-03-25'
draft: true
---
> *Only three things happen naturally in organizations: friction, confusion, and
> underperformance. Everything else requires leadership.*
>
> --- Peter Drucker

 When it comes to service delivery, most of us equate friction with those
 elements that hinder our delivery speed and throughput. It is what drives so
 many of us to automate our builds and deployments, purchase cloud services, and
 adopt various Agile practices. But thinking about friction so narrowly can
 cause us to suboptimize, or worse overlook, everything else that is getting in
 our way of achieving the desired outcomes.

 For John Boyd and Helmuth von Moltke, discussed in the previous two chapters,
 friction is what degrades our situational awareness and impedes learning.
 Boyd's Energy-Maneuverability (EM) theory proved that even if you were faster
 and more capable than your opponent, you could still fail if you did not
 sufficiently adapt to changing conditions or incorporate learning effectively
 along the way.

 Lean takes friction a bit further. In product and service delivery, Lean\
 practitioners note that you can succeed at delivery and yet still fail if you
 are less effective than the competition at helping your customer achieve their
 desired outcome. To avoid this, team members in Lean organizations know to
 explicitly search for and try to eliminate anything that hinders or does not
 directly add value in any way that the customer can perceive, declaring it
 *waste*.

 For Taiichi Ohno, who is credited with creating the Toyota Production System,
 waste takes three forms: pure waste (*muda*), overburden (*muri*), and
 irregularity (*mura*).

 What is powerful about this approach is that it makes us openly question
 everything we do under the lens of how it contributes to the target outcome.
 The

 idea of removing friction and waste quickly reminds us that it is not how fast
 you can go that is important, but rather how far you can progress toward the
 target outcome. This different perspective on delivery forces us to challenge
 the status quo, driving us to continually experiment, learn, and improve to
 better achieve those outcomes.

 ## Understanding Ohno's Forms of Waste

 **Figure 4.1**\
 Ohno's wastes

 Lean and the idea of targeting waste came out of the US government's "Training
 Within Industry" (TWI) program,[^1] which was designed to improve productivity
 of war production efforts and overcome labor scarcity during World War II. One
 of its most valuable components, Job Methods (JM), specifically targeted waste
 reduction through continuous improvement.

 [^1]: https://www.lean.org/search/documents/105.pdf

 Workers using JM were encouraged to constantly look for ways to improve the
 methods used to perform their work by thinking about why they were necessary
 and how they contributed to the intent behind the work. Were there unnecessary
 steps or details that could be eliminated? Could steps be rearranged or
 simplified to reduce mistakes or the time needed to complete a job? Workers who
 came up with improvements were celebrated and encouraged to share them widely.

 There ideas were brought to Japan by US Army General Douglas MacArthur, the
 Supreme Commander for the Allied Powers in Japan after Japan's defeat in World
 War II. He was in charge of reconstruction after the war, and was eager to

 find ways to speed it up to improve the living conditions of the Japanese
 citizenry. One of the approach's early adopters was Taiichi Ohno, a Toyota
 plant manager and later vice president of Toyota, who needed a way to help his
 struggling company compete against more resource-rich competitors like GM.

 Ohno pushed these ideas to everyone across the company, from the worker on the
 assembly line to the executives at the top. To get everyone willing to pitch in
 to find ways to continually improve, he had to encourage them to change the way
 they viewed their jobs. Rather than just following instructions, they needed to
 continuously and critically examine everything that went into delivery.
 Anything that either got in the way of delivery or otherwise did not directly
 contribute to meeting the customer's needs needed to be viewed as a form of
 waste that needed to be eliminated.

 Ohno and the Toyota teams found that waste can take many forms. Being familiar
 with these types and their effects can help with identifying and minimizing
 their presence in your own ecosystems.

> ### Friction vs. Waste
> At this point you might be thinking "Hey, I thought this chapter was about
> friction! Why is he talking about some Japanese guy's definition of waste?" In
> short, waste is a form of friction. The extensive body of knowledge from Lean
> has many lessons that apply to IT. I believe it is worthwhile to introduce
> many of its concepts in the original language to both minimize confusion and
> to allow you, the reader, to be able to investigate other Lean literature
> further. However, like a lot of Lean terms, the term "waste" is easy to
> misunderstand, misapply, or view as irrelevant in the IT context. Most people
> think of waste as a useless but mostly harmless byproduct of some process. It
> might not be desirable to have, but unless you know it is causing real
> problems, it is viewed as being safe to ignore. This is especially true in IT,
> where waste is neither physical nor usually visible. Friction, however, is
> seen as a real thing in IT. Whether it is in the form of poorly written
> requirements, buggy code, poor tools, not enough deployment environments, or
> slow processes, friction hinders our ability to progress and successfully
> deliver. Friction is also viewed less as a personal affront than waste. I know
> that I am far more open to finding an easier, more "frictionless" way of doing
> something than finding a "less wasteful" way.
>
> Finally, labelling something as friction more clearly describes its impact to
> our knowledge-driven decision-making industry. Anything that makes us slower
> to reaching a solution, whether it is working on useless tasks, having to redo
> a task, or waiting for a slow  process to complete, is friction. If it is
> helpful to you as you progress through this chapter, please feel free to
> replace the word "waste" with "friction" in your mind.

 ## Muda (Pure Waste)


 **Figure 4.2**\
Muda is as bad as it looks.

Muda is the Japanese word for waste as well as uselessness, idleness, and
futility. By definition it is an activity that the customer wouldn't willingly
pay for. Contrary to popular belief, the target isn't to figure out how to do
things cheaper. Rather, it is to identify and remove anything that doesn't
tangibly contribute to achieving the desired outcome.

Seeking out Muda is more than just finding useless things to eliminate. Muda can
help us identify places where situational awareness has been lost, where
customer outcomes have been misunderstood, or even where learning has been
hobbled. It also gets us to better understand the underlying intent for all the
things we are told we need to do in order to meet any legal, regulatory, or
internal requirements that do not provide direct tangible value to the customer.
For Ohno, these\
requirements were also a form of Muda. While they may be difficult to eliminate,
it doesn't mean that we cannot somehow minimize or streamline any friction they
may create and still meet their intended purpose.

Shigeo Shingo, one of the creators of the Toyota Production System, helpfully
identified seven types of waste in manufacturing. Over the years, an eighth was
added (non-used employee talent), creating a helpful list for teams to use in
their efforts to root out waste. To guide us on our journey I have created a
useful analog in the DevOps world, which is shown in Table 4.1.

 **Table 4.1**\
Seven Types of Waste in Manufacturing and Their Corresponding Terms in DevOps


This may seem like a somewhat obvious list of things not to do. But it takes
more than just declaring that you are not going to do them. It is important to
understand why they happen, as well as how they degrade our decision making.

Doing so should help you understand the power of many of the mechanisms, from
Workflow and Queue Master to Service Engineering Leads and sync points, that I
heavily rely upon both to make it obvious when they are occurring and to help
teams eliminate them.

To better understand these types of waste, let's step through each of them.

### Waste 1: Defects*

 **Figure 4.3**\
Even subtle defects can be deadly.

Whether they are bugs or shortcomings in a service, no one needs to be told that
defects are obvious waste. They are a failure that gets in the way of a product
or service performing as the customer needs.

Not only does no one intentionally create defects, no one likes to be known for
doing so. The friction they create can slow down delivery in embarrassing and
unexpected ways. As most teams are judged on how quickly they can deliver, this
combination means that defects are often underplayed, hidden, or labelled
as"features."

Allowing a defect to fester only makes the situation worse. Defects found
shortly after they are created are far easier to fix. The person who created a
defect is far more likely to have enough context to know where it is located. As
time goes on, context is lost, memories fade, and other changes may further
obscure the root cause and thereby make it harder to find. Once a defect makes
it into production, costs go up astronomically. Not only does this make it far
more difficult to triage and fix, but now customers have likely been impacted.

Defect-ridden code is also hard to work with. It makes meeting deadlines far
more unpredictable. Not only do defects need to be fixed, but they also make it
easy to unintentionally create additional ones. Few people like working in such
dangerously unpredictable conditions. Even the knowledge that an area has rotten
code can make it incredibly difficult to attract and retain good delivery staff
to work on it, making it that much more difficult to deliver effectively.

The best way to prevent defects from occurring is to understand their causes. As
covered in Chapter 5, "Risk," defects are the result of insufficient situational
awareness of your delivery ecosystem. To demonstrate this, here is a list of the
most common causes of defects:

 - Misunderstood requirements

 - Errors and poorly worded instructions

 - Lost or insufficient context within the problem space

 - Inconsistent or poorly structured and/or managed code, configuration, and/or
   data

 - A lack of, or hard to follow, dependency management

 - Poorly tracked or understood build and/or run environment management

 - Nondeterministic/nonreliable/nonrepeatable installation and rollback
   functions

 - Using an unsuitable or unfamiliar tool or language

 - Typos

 Each one of these is an example of lost awareness. Some, like misunderstood
 requirements or lost context, are obvious. However, even more subtle causes
 like typos or tooling/language mismatches that seem minor on their face can
 cause very real, and often hard to find, problems.

 Lean tackles this problem by trying to "mistake proof" the delivery line. It
 uses techniques designed to do this in two ways.

 One approach is to design the system in such a way that it is impossible to
 make certain mistakes. Manufacturers do this regularly with tools and parts by
 creating a shape that can only be put together in one correct way. An example
 is the asymmetrical shape of an HDMI connector. In IT this can be done by
 creating tools that prevent dangerous commands or invalid configurations from
 being executed by accident. I cover some strategies for this in more length in
 Chapter 10, "Automation."

 The other way is to put in place mechanisms that make it far easier to spot
 mistakes and potentially hazardous conditions in the first place. Lean\
 manufacturers use multiple techniques to bring immediate attention to anything
 abnormal or out of place.

 One example is to use a clear marking such as color coding or symbols. Colors
 and symbols are great ways of providing a lot of information quickly with
 little overhead. Lean manufacturers use different colors for certain parts,
 trays, carts, and even places where tools are placed.

 This simple technique is very helpful, and a familiar one for any heavy IDE
 (integrated development environment) tool user. I also use it heavily with
 color coding management interfaces and terminal windows between environments,
 color coding datacenter cabling and connectors, as well as color coding between
 different types of alarms and graphs. I have even worked with teams to "color
 code" tools, frameworks, and languages to the types of tasks that they are most
 suited for. Sometimes this "color code" is the use of distinct symbols or
 markings like stripe patterns in case someone is color blind. Using such
 coding\
 mechanisms both encourages people to use the most appropriate option for the
 job and gets them to ask, and if needed debate, why a certain tool or
 technology is not favored for a particular job type.

 Another example of a mechanism for spotting mistakes is what in Lean is
 called"stop the line." In a Lean factory there will be *Andon* cords placed
 throughout the assembly line that activate an alarm to alert everyone of a
 defect. If the defect is not fixable immediately, the assembly line is halted.
 This exposes where a fault

 was found, aiding efforts to find the source, and prevents the failed product
 from moving further up the line where the fault can be concealed or create
 additional faults.

 In IT such mechanisms are more difficult to put in place. We can and do stop
 builds and delivery pipelines when a failure condition is encountered. However,
 problems are not always obvious in the heat of the moment, when it is difficult
 to step back and see the whole. This is why I recommend having both a Queue
 Master, as detailed in Chapter 13, "Queue Master," who can help find problems
 directly, as well as a Service Engineering Lead, as detailed in Chapter 9,
 "Service Delivery Maturity and the Service Engineering Lead," who can help the
 larger team build the maturity to see more effectively themselves.

 A shift toward such mistake proofing makes environments safe for teams to work
 in and repositions teams to view defects as a failure of the system that needs
 to be addressed to help all rather than as their own personal failure, which
 they might be tempted to conceal from others.

 ### Waste 2: Overproduction

 **Figure 4.4**\
 "But I only ordered one!"

 You can have too much of a good thing, especially when if it is rarely, if
 ever, used.

Overproduction occurs when something is produced that has no paying customer.

 For manufacturers this excess results in inventory build-up that needs to be
 stored, discounted, or thrown away. This is obviously a Bad Thing To Do. Not
 only do you have to decide whether it is better to pay to store it or throw it
 away, the resources used to create it remain tied up in something that is not
 providing any value.

 While IT overproduction is caused by many of the same forces as in
 manufacturing, namely a focus on outputs over outcomes, it is both far less
 visible and more destructive.

 IT overproduction lurks in the form of unused or unneeded features, excess
 code, and unwanted activities that provide little demonstrable value. People
 may claim that customers want the unused features, but never bother to see if
 this is true or how it contributes to the overall outcome. Internal processes
 and tools may look useful but the output may be ignored or no longer provide
 any value.

 What many IT professionals miss is that all of this overproduction is not just
 wasteful, but also introduces a lot of excess friction into delivery. Excess
 features and code might not be used but they have to be integrated, tested,
 deployed, and managed in production. If they are not, they can end up turning
 into dangerous landmines that can inadvertently destroy a company, as happened
 with Knight Capital (as detailed in Chapter 10, "Automation").

 Excess code and features also obscure our overall understanding of our\
 ecosystem. They make it far more difficult to find problems, understand what
 code is and is not being exercised as customers use it, and figure out the best
 place to make changes and add features and functionality that customers
 actually do need.

 To counter overproduction, I always try to make it obvious what the costs of
 doing it are to the organization. I track the extra support and maintenance
 costs, the added infrastructure costs, and the increase and variability of
 delivery times and defects it causes. I also try to capture actual usage
 patterns to make it easier to spot features that are rarely, if ever, used.
 This allows for the technical teams to hold a fact-based discussion with the
 business to ensure that what is being done is in the best interests of the
 organization and the outcomes of its customers.

> #### Making the Wrong Numbers  
> Anyone who has worked at a telecommunications company knows voice service is
> still considered a keystone in the industry. This is despite the explosive
> growth of packet-switched networking and Internet-based services.
> 
> One such provider was looking to consolidate and upgrade their many legacy
> voice products. They built and acquired many over the years that served a
> myriad of consumer and business needs. But as time went on, these systems were
> growing increasingly unstable and expensive to manage. Many of these systems
> were also not compatible with newer fiber lines. Despite this clearly growing
> problem, few stakeholders could agree on the best way to resolve it. 
>
> Marketing and Sales were fearful that any loss of features would not only look
> bad but risked losing customers. As a result they demanded that any new
> solution include all 200 existing features found across all systems currently
> in place. 
>
> This left the delivery teams in a conundrum. There was simply no system on the
> market that contained every one of these features. The only way any solution
> could accommodate it would require either integrating several commercial
> solutions together with custom code or building everything from scratch
> in-house. Either approach would be both costly and take years to implement. As
>  Marketing, Sales, and Support all strongly pushed back anything that did not
>  have feature parity on Day 1, there was no way to easily phase in a solution.
>  
> The teams struggled with this problem quarter after quarter with little to
> show for it. The company became increasingly concerned as the risk of system
> failures grew with no solution yet in sight. 
>
> This seemingly insurmountable problem actually had a rather simple solution.
> Customers didn't really want every feature. They only wanted the ones that
> were valuable to them. Some features were for long-obsolete needs or ones that
> could be better handled in another way. Also, not every customer or market was
> equally valuable to the company. If a feature had to be built and supported at
> a loss for a customer, it needed to be agreed as to why. 
>
> Keeping all this in mind, one team decided to dig in to see which features
> were actually being used by which customers along with the revenue each
>  generated. They found that there were roughly six features that were heavily
> used, along with another seven that were infrequently used by customers who
> were important enough to the company that it made sense to include them. All
> of these features were so common as to be included in most solutions available
> on the market. The vast majority of the remaining 180 features had either
> never been used or not been used for the past five years.
>
> The data was so obvious that the other three teams backed down. Soon after, a
> solution was delivered with all the necessary features. This was then rolled
> out to friendly parties to try. Not long after, we migrated the rest and then
> proceeded to shut down all of the legacy systems.

 ### Waste 3: Systemic Impediments and Waiting

 **Figure 4.5**\
 "Please wait for the next available representative..."

 Even with all of the focus over the years on new tools and processes designed
 to reduce delivery friction, we still struggle to get things done. Much of this
 is caused by a wide array of systemic impediments that IT teams manage to
 inflict upon themselves, either out of habit or through a lack of communication
 and understanding. Each one inevitably degrades our ability to make effective
 decisions.

 While the most obvious impediments cluster around operational areas, many exist
 throughout the service delivery lifecycle. Common forms include frustrating
 bottlenecks, misalignments, and hard blockers that stop you from being able to
 make any progress at all until they are eventually removed. They result in
 delivery delays, rework, missed customer expectations, and frustration that can
 increase tension across the organization.

 #### Identifying Systemic Impediments

 The first step on the path to eliminating this form of waste is to first
 recognize the causes of systemic impediments. Frequently the cause grows out of
 a previous problem or goal that is no longer valid. Other times, communication
 issues and misalignments in goals or understood target outcomes create
 contention that hinders progress. Uncovering these causes and their costs to
 the organization can help bring attention to, and ultimately remove, an
 impediment.

 To help you on your journey, here is a list of some of the most common systemic
 impediments:

 - **Communication challenges:** Distance, whether physical or organizational,
 limits timely high-bandwidth face-to-face communication. Instead, we are left
 to rely upon more lossy, out-of-sync communication mechanisms such as email and
 documents that lose context and can be misinterpreted in ways that reduce our
 situational awareness and cross-organizational alignment. As you will discover
 in Chapter 6, "Situational Awareness," the increasing globalization of IT also
 can introduce language and cultural background differences that can lead to
 further problems and create distrust.

 - **Poorly configured work environments:** In our increasingly virtual world,
 many organizations miss the value of a well-designed shared work\
 environment. This is a place where team members can meet to work\
 collaboratively with minimal outside interruptions. It also acts as an\
 information store and sync point, creating a useful structure to capture and
 share information, as well as catch and correct misinterpretations. Without a
 shared work environment, whether due to limited space, geographical\
 distribution, or a global event such as a health crisis, sharing becomes more
 informal and uneven. Without concerted effort to implement tools that improve
 information sharing, collaborative working, and conflict resolution,
 information can be lost, and trust can be hindered.

 - **Poor environment management:** Environment hygiene, from all the\
 components that make up the service to the software, operating systems, patch
 levels, configurations, and physical and/or virtual layers of coding, testing,
 and operating environments, is important to keep track of and maintain. Any
 lack of hygiene introduces potential variation where situational awareness can
 be lost, thereby reducing the efficacy of decision making.

 - **Poor code management:** Code that is poorly written, commented, tracked, or
 updated makes working with it slow and error-prone. Supporting development
 tools and their usage, from code repository tools and structures to build and
 test tools and the artifacts they generate, are also important for code health.
 Anyone who has worked in a place with a large number of code branches and\
 infrequently checked-in code knows how painful merging and integration is. This
 pain is caused because there has been so much disjointed change that no one
 person has the full context of the code. The gaps in awareness this creates
 across the team are difficult to close and also distract from the target
 outcomes you are trying to deliver.

 - **Excessive tight coupling:** Components, systems, and services can grow to
 become so interdependent upon each other that any change to one has a
 significant and immediate ripple effect on another. Tight coupling forces
 affected parts to be treated as a single unit. This reduces flexibility by
 forcing any changes in one to be treated as changes in all. It multiplies the
 effort required to deliver, manage, and troubleshoot. It can also increase the
 amount of downtime required to make a change, as affected parts cannot be
 swapped out or changed individually, as well as reduce the number of options
 available to easily scale those areas.

 - **Competing objectives:** Organizations can fall into the trap of having\
 individuals or teams with different or even conflicting objectives. This can
 lead to disagreements, rivalries, and blocks that hinder progress. Not only do
 competing objectives impede business and create an impenetrable fog that
 obfuscates the strategic intent of the organization, they can divide and be
 heavily demoralizing to staff.

> **Friction-Filled Clouds**  I am impatient by nature, and waiting
> unnecessarily for something is a particular pet peeve of mine. However, I am
> not so impatient that I am willing to rush through something if it means more
> work and friction later. Deploying services on the cloud is probably the place
> where this balance comes most to the forefront. 
>
> Many organizations transition to using the cloud to work around internal
> impediments. A common catalyst is all the friction involved in waiting for new
> hardware and software to be installed and made available. This can make going
> out and instantly provisioning an AWS or Azure instance quite alluring,
> especially when the alternative can take weeks or months.
>
> I commonly see IT Operations organizations miss the problem that\ developers
> and others across the organization are trying to solve. Instead, they focus on
> the technology of cloud computing. Many try to build "internal clouds" or put
> in place yet another lengthy  provisioning process for using an external
> provider. One company I was at even went so far as insisting that each service
> provisioned needed to go through a weeklong design process for each new
> virtual machine or container to "make sure that everything was documented and
> approved."
>
> Process is hardly the only source of friction. A second common friction-filled
> mistake occurs when teams fail to manage their cloud service configurations.
> consoles become full of one-offs, while configuration and\
> orchestration tools like Puppet, Docker, Kubernetes, and Terraform are either
> not used at all or are so full of untracked one-offs  that it becomes
> difficult to know what is in production or how to reproduce it. 
>
> A third mistake is to so tightly couple cloud services as to lose much of the
> flexibility that moving to cloud services would otherwise afford. This forces
> teams to take down, update, and bring back up such services together in a
> resource-heavy coordinated fashion.

 ### Упущение 4: Чрезмерная специализация

![](images/4.6.png)

 **Рисунок 4.6**\
 Билл несовсем правильно понял тот момент, когда ему сказали, что его 
 специализация позволит занять ему высокие посты.

 Когда вы сталкиваетесь с достаточно глубокими и сложными проблемами, наличие 
 специализированных знаний и опыта может быть очень полезным. Кроме того, процесс 
 становления <<полезным>> человеком в решении определенных типов проблем может 
 даже повысить самооценку. Приобретение таких навыков требует времени и практики, 
 а более сложные или редкие наборы навыков часто сопровождаются и повышенной 
 оплатой. Это побуждает людей к становлению специалистом более узкого профиля.

 Так что же здесь может быть не так?

 Проблема начинается с того, как используются специалисты. Если их навыки 
 являются редкими или дорогими, многие компании стремятся обеспечить максимальную
 эффективность своих инвестиций. Они уделяют самое пристальное внимание таким 
 специалистам и предоставляют им всю работу, требующую данного опыта. Это создает
 проблемы, которые в конечном итоге ухудшают ситуационную осведомленность и 
 ослабляют организационное доверие и обучение.

 Одной из таких проблем является риск отрыва работы от общего контекста. 
 Специалисты проводят так много времени, работая над задачами, которые 
 соответствуют исключительно их специализации, что часто остаются в стороне от 
 того, что происходит в более крупной экосистеме, а вместе с ней и от общей цели 
 работы. Аналогичным образом, работники, находящиеся за пределами таких 
 специальностей, не имеют достаточного представления того, что сделал специалист 
 и почему. Это уменьшает чувство сопричастности для всех участников жизненного 
 цикла, создавая благодатную почву для перекладывания ответственности и обвинений.

 Другая проблема заключается в том, что личность работника и его ценность часто
 ассоциируются с типом его навыка, а не с его способностью помочь компании 
 достичь целевых результатов. Специализация работника --- это валюта, и чем реже 
 она встречается, тем больше стоит работник. Это лишает специалистов стимула 
 делиться своими знаниями с другими, тем самым опасаясь поставить под угрозу свою 
 ценность.

 Важно отметить, что крупные организации наиболее подвержены проблеме 
 специализации. Причин тому множество:

 - **Наём, ориентированный на навыки:** Специализацию гораздо легче определить как 
 потребность и нанять на должность, поэтому у менеджеров легко возникает соблазн
 организовать команды по определенным признакам специализации. 
 Узкоспециализированная работа должна передаваться из одного подразделения в 
 другое, чтобы быть завершенной. Подходы к найму, при которых кандидаты проходят 
 специальные тесты, соответствующие узкому диапазону допустимых решений, часто 
 смещены в сторону аналогично мыслящих людей. Это делает команды более 
 восприимчивыми к <<туннельному зрению>> и политики <<не здесь придумано>>.

 - **Отсутствие сопричастности и недостаточное понимание работы:** При недостаточном 
 понимании работы и отсутствии сопричастности к более крупной экосистеме 
 осведомленность и отзывчивость часто еще больше фрагментируются. Работа легко 
 теряет значимый приоритет. Команды оптимизируют свою работу на основе того, что 
 им наиболее выгодно, даже если это происходит за счет недооптимизации более 
 крупной организации. По мере блокирования работы и возникновения 
 междисциплинарных проблем неизбежно возникает соблазн перекладывания вины и 
 обвинений.

 - **Борьба с процессом устаревания:** Быстрые изменения в технологиях или стратегиях
 могут привести к устареванию специализированных навыков. Действующие специалисты, 
 которые видят, что работа переходит из их области компетенции в иную область, 
 могут попытаться затормозить или сорвать перемены, препятствуя возможности  
 организации к адаптации.

 - **Отсутствие личной вовлеченности и заинтересованности:** Разделение обязанностей 
 создает жесткую и менее стимулирующую рабочую среду. Отсутствие ощущения 
 совместного участия в решении поставленных задач может ограничить творческий 
 потенциал и внедрение новых технологий и решений. Ограниченное понимание 
 руководством этих основополагающих факторов может еще больше замедлить 
 деятельность организации.

 Лучший решением для организации служит постоянный поиск возможностей для 
 минимизации потребности в специализации. Один из таких способов --- избегать 
 слишком сложных решений, требующих глубокой специализации. Другой способ --- 
 ротация ролей, а также поиск творческих путей для регулярной помощи членам 
 команды в обучении друг друга.

 Там, где специализированная работа неизбежна, есть способы перестроить роли 
 специалистов и команды, чтобы минимизировать влияние возможных недостатков. 
 Лучше всего внедрить специалистов в качестве профильных экспертов в команды, 
 которые владеют всем жизненным циклом. Эта модель схожа с подходом Spotify 
 <<отряды и гильдии>>. Вместо того чтобы выполнять всю работу самостоятельно, 
 специалисты могут консультировать и обучать других, чтобы обеспечить правильное 
 выполнение действий. Это не только повышает гибкость за счет увеличения размера 
 и надлежащей квалификации персонала, но и создает привлекательный стимул для 
 сотрудников постоянно приобретать новые навыки. Специалисты могут продолжать 
 оттачивать свои навыки, погружаясь в более глубокие проблемы и обмениваясь 
 опытом с другими экспертами в более широкой группе по интересам. 
 Более широкий круг общения помогает людям стать экспертами, обладающими 
 глубокими специальными знаниями как минимум в одной области, а также имеющими
 широкую компетенцию во многих других областях.


> **Дисфункция чрезмерной специализации**  
> Я часто сталкиваюсь с компаниями, которые слишком полагаются на специалистов 
> при выполнении определенной деятельности, создавая всевозможные препятствия, 
> которые мешают другим командам выполнять свою работу. Три наиболее 
> распространенные группы - это администраторы баз данных (DBA), сетевые 
> инженеры и специалисты по информационной безопасности.
> 
> Быть таким специалистом или иметь таких специалистов в команде разработчиков 
> не обязательно плохо. Я часто рекомендую их присутствие. Когда они являются 
> частью разнообразной и квалифицированной команды, они могут помочь в принятии 
> более оптимальных техническиx решений. Они могут также обучить других кодировать 
> и выполнять задачи по обслуживанию, используя лучшие подходы, а также могут 
> решать те сложные проблемы, которые в противном случае могут ограничить вашу
> способность в удовлетворение потребностей клиентов.
> 
> Однако сами специалисты нуждаются в регулярных задачах и вызовах, чтобы они 
> могли оставаться заинтересованными и расти вместе с командой. Когда этого 
> не происходит, они часто ставят свою ценность для команды в зависимость от 
> того, какую работу они могут выполнить в одиночку. Это неизбежно заставляет
> их вести себя слишком навязчиво по отношению к своей рабочей области, до 
> такой степени, что это становится единственной точкой отказа.
> 
> У меня была подобная проблема в одной компании с администраторами DBA и 
> сетевыми инженерами. Там существовала политика, согласно которой для всех работ
> с базой данных требовался администратор, а со стороны сети большая часть 
> доступа контролировалась списками контроля доступа (ACL), которые должны были 
> быть подписаны, а затем выполнены сетевым инженером.  Обе политики делали
> изменения и установку очень медленно. Хотя администраторам баз данных и 
> сетевым инженерам нравилось чувство уважения и ощущение важности к себе, 
> давление на них было велико, а работа была утомительной и неинтересной.
> 
> Поэтому я изменил всю структуру, начав с DBA.
> 
> Я сел c некоторыми из лучших DBA в компании. Они были чрезвычайно талантливы, 
> и, возможно, одними из лучших, с кем я когда-либо работал. Я очень хотел 
> устранить все <<узкие места>>. Но я также ценил их знания и хотел, чтобы
> чтобы они понимали, что им бросают вызов и при это они совершенствуются. 
> 
> Я предложил им придумать инструменты и другие методы, которые позволят другим 
> людям выполнять простые задачи с минимальным риском. Наряду с этим мы создали 
> систему баллов, которая позволяла инженерам, показавшим, что они могут 
> ответственно выполнять эти задачи, получать больше привилегий для выполнения 
> других, более рискованных задач. А те, которые не справлялись, теряли баллы,
> а вместе с ними и свои привилегии.
>  
> Затем я создал подразделение Database Engineering (DBE), которое должно было 
> отвечать за будущие архитектурные решения баз данных, исследовать новые 
> перспективные технологии и стратегии оптимизации данных, а также работать с 
> разработчиками над улучшением практики кодирования и структуры данных. Как и 
> в случае с инженерами, для DBA была разработана система баллов. Те, кто создавал 
> и совершенствовал инструменты и методики, позволяющие выполнять работу, 
> получали возможность стать DBE и развивать свою сферу интересов. А те, кому это 
> было неинтересно, продолжали работать над административными задачами баз данных,
> но они могли оказаться на месте тех самых инженеров, которые тормозили рабочий 
> процесс.
> 
> Этот подход оказался чрезвычайно популярным, и за короткое время почти все 
> <<узкие места>> исчезли. Мы также добились выигрыша в том, что наши лучшие DBE 
> теперь решали некоторые новейшие технологические проблемы, что позволило 
> нам обогнать многих наших конкурентов.
> 
> Я использовал аналогичный подход и в сетевой инженерии. Вскоре команда нашла 
> способы отказаться от сетевых ACL и заменить их технологиями, которые в конечном итоге 
> составили основу программно-определяемых сетей (SDN). Это позволило командам 
> разработчиков повысить гибкость, обеспечив при этом безопасность и 
> производительность сетей.

 ### Waste 5: Handoffs

 **Figure 4.7**\
 Handoffs

 Handoffs are a fact of life. Not everyone can always do everything all the
 time. Sometimes it may even be prudent, or a legal requirement, to
 intentionally separate responsibilities across teams.

 Handoffs, however, introduce two challenges. The first is that people and teams
 do not always share the same set of priorities. When priorities differ, work
 can easily become trapped along a handoff chain. Whether a team is waiting for
 another team to complete a piece of work they need or a partially completed
 item is waiting to be picked up and completed, the delay it causes appears the
 same from the customer's perspective.

 The second challenge is that handoff and integration points become
 opportunities for information and context to be lost. The resulting flawed
 assumptions can lead to errors and rework, as well as complicate the
 troubleshooting of any problems that cross the handoff or integration boundary.

 The most common form of handoffs are those between specialist roles and domain
 experts brought in to complete an activity. I have personally seen
 back-and-forth loops between DBAs and engineers or developers and testers that
 drag on for days or weeks.

 Another common challenge is caused by the overly tight coupling between
 components as well as nonsensical splitting of responsibilities across teams.
 Ironically, such splitting is often done under the belief that more teams with
 fewer responsibilities will automatically result in faster delivery regardless
 of how tasks are divided up. This usually leads to dividing tasks at the very
 bottlenecks that lead to excessive handoffs.

> ### The Serial Loopback** 
> At one company such responsibility divisions led to a long handoff chain that
> ultimately became debilitating to the company. The service had been broken up
> across 20 different Agile teams under the belief that together they could
> deliver everything in one or two 2-week sprints. Unfortunately, the way that
> they were divided left 14 teams with tight library and other dependencies that
> needed to be first delivered by another team before they could confidently
> complete their own tasks. In a number of cases these dependencies were
> cumulative, with a team dependent upon a library from another team that was
> dependent upon another element from yet another team and so on. This
> ultimately serialized the very deliveries they were  trying to speed up, in
> some cases increasing delivery times by upwards of six months. 
>
> What was worse, if a bug or other problem was found midway through the chain,
> the process would effectively have to loop back to the team responsible for
> fixing it and traverse the chain from that point again. 
>
> **Figure 4.8**\ The serial loopback 

 It is important to understand where handoffs exist within your ecosystem.
 Workflow boards like those discussed in Chapter 12, "Workflow," in conjunction
 with the Queue Master discussed in Chapter 13, "Queue Master," can help you
 spot excessive handoffs. I also encourage teams to identify and discuss
 handoffs at retrospectives and Strategic Review sessions.

 Encouraging staff to find ways to reduce handoffs wherever possible improves
 organizational responsiveness and flexibility. It also can improve situational
 awareness, as well as reduce errors and misunderstandings that result in
 wasteful rework.

 ### Waste 6: Partially Done Work

 **Figure 4.9**\
 Partially done work

 In Lean, partially done work is called "work in progress" (WIP). WIP is
 anything that has had work done on it but is not deployed and providing value
 to the customer.

 Partially done work, or WIP, is a common scourge of IT delivery organizations.
 It can appear everywhere across the delivery cycle, from modified code that has
 not been checked in, through unbuilt/unintegrated code, untested packages,\
 unreleased software, released but turned off code, to partially completed\
 operations tickets.

 There are a lot of problems with partially done work. It is easy to focus on
 how it can create a lag in gaining value from the work, or how not checking in
 a big batch of code delays potentially useful feedback. Both are meaningful.
 But perhaps the worst problem with WIP is that it tends to create *more* work
 for people who believe what they are doing is making them more efficient.

 Think through a time when you were juggling multiple pieces of work. Each time
 you cycled to the next item you had to put in some effort to regain context.
 Where did you leave it? In what direction were you trying to take the activity?

 Did something change while you were not attending the task that altered the
 dynamics enough that you have to course correct or even throw away what you
 have?

 Another issue with temporarily losing context is that it creates an opening for
 mistakes. Dynamics can change in ways that you might not notice until it is too
 late. We can also misremember what was going on or what we were doing in ways
 that introduce unintentional defects or rework.

 The best way to tackle partially done work is by making it and its effects
 visible. Workflow boards that show the amount of work in progress are one good
 form. This is also where Queue Masters are extremely helpful. They can spot not
 just when WIP is happening, but also some of the patterns that might be causing
 it.

 This can help teams find ways to work together to break their bad habits

 One such common bad habit is our next waste: task switching.

 ### Waste 7: Task Switching

 **Figure 4.10**\
 Task switching

 Whether you are building, testing, or operating services, IT work requires a
 lot of deep concentration and building up context. Interruptions are hazardous
 for both. Yet in the desire to maximize output, we willingly accept frequent
 task switching as normal, whether in the form of interruptive fault
 troubleshooting or the sudden reprioritization of work.

 It is easy to fall for task switching, and it often goes hand in hand with
 partially done work. Some love the thrill of racing off to be the hero in an
 outage firefight.

 Others feel that by having several activities on the go at the same time they
 are somehow more indispensable to the organization. Often an organization is
 particularly bad at prioritizing and tracking work, and every task becomes an
 opportunity for someone to lobby hard for it to be done immediately.

 Switching between tasks is not just distracting, it fractures context, which
 slows our progress and degrades efficiency as partially done work builds up in
 the queue. Task switching also erodes our situational awareness, our ability to
 spot patterns, and ultimately our ability to learn and improve. Not only do we
 end up losing track of what is going on, but we risk losing touch with the
 outcomes that we need to accomplish. At best this can result in higher-priority
 items being delayed or neglected. At worst our ability to make sensible
 decisions fails.

 Many IT teams, especially those with a heavy operational support element,
 resign themselves to widespread task switching. It is easy to believe that it
 is simply the nature of the job, but, as we will demonstrate later with the
 Queue Master role, restructuring the way that work hits the team can greatly
 reduce disruption. By being the entrance point for work, the Queue Master also
 can see across the ecosystem, noticing patterns and ultimately helping the team
 learn.

 Workflow visualization techniques can also help uncover task switching,\
 including lingering tasks and a build-up of work in progress. It is also
 important to actively look for and reduce the number of sources of task
 switching. As discussed in Chapter 13, "Queue Master," I encourage Queue
 Masters to help the team investigate ways of restructuring long-running
 people-intensive tasks, as well as work that seems to flow in circles between
 teams or requires a great deal of back and forth.

 ### Waste 8: Excessive Processes

 **Figure 4.11**\
 "Why do I have to fill out all these forms to replace my keyboard?"

 Processes can be helpful. They standardize the shape and direction of work to
 ensure a reliably repeatable outcome. If deployed and maintained properly,
 processes can reduce errors and rework. They also are good ways of capturing
 knowledge that can enhance the capabilities of the team.

 However, you can have too much of a good thing. For IT, having and following
 the processes can become more important than the customer outcome, sometimes to
 the point where it is even declared as the objective that the customer is
 looking for. This is true even when the processes themselves do not seem to do
 much to improve delivery or service effectiveness.

 Some of the worst process waste is done under the banner of "industry best
 practice," even when it is clear that the process is hindering the business.
 Over time, this divergence in purpose can reduce an organization's ability to
 respond in a timely and flexible way to the demands placed upon it. Learning
 and improvement seem to slow to the point where there is nothing significant
 that directly correlates to improved effectiveness and progress toward customer
 needs. Tensions and stress rise from increased frustration, workloads, and\
 rework.

 Excessive processes tend to develop one or more of the following attributes:

 - **Inflexibility:** IT lives in an ever more dynamic ecosystem. Customer and
 business needs can shift at an even faster rate than technology. The
 combination of condition changes means processes need to be continually
 reviewed, altered, and sometimes even eliminated in order to stay aligned.
 Inability or resistance to adapt processes reduces their efficacy and creates
 waste.

 - **Excessively prescriptive:** A useful process is typically a repeatable
 pattern that helps us understand the situation and navigate toward a successful
 outcome.

 However, excessively prescriptive processes can be so detailed that they become
 a mindless straightjacket that actively prevents people from adjusting to
 changing conditions. Such processes should be reviewed to determine whether the
 process is a workaround hiding a larger problem.

 - **Demonstrate little to no discernible customer value:** Some processes are
 put in place with the best of intentions. However, due to either habit or\
 misunderstanding of the actual need, they struggle to provide any appreciable
 value. These processes are typically poorly constructed or are ill fitting for
 their deployed environment. Sometimes they have been taken verbatim from
 another environment or official list of "best practices." For instance, one
 company required physical signatures for certain change procedures. There were
 no legal or regulatory requirements for the procedure, and later I found that
 the only

 reason it was there was because the process had been copied from a company that
 did have such requirements.

 Such processes should be reviewed to determine what problem they are trying to
 solve and whether the problem exists and needs solving in the target\
 environment. If it does, the process should be altered to make the intended
 desired value far more apparent. If it doesn't, the process should be thrown
 out.

 It is far safer to have no process than to shoehorn in one that is not fit for
 purpose.

 - **Execution-knowledge mismatch:** Sometimes a process ends up being\
 executed by people who either do not understand the underlying reasons for it
 or lack the knowledge, awareness, or skills required for executing it. IT\
 organizations are often filled with such processes, and they don't just occur
 at the junior support technician level. In fact, in my experience they are most
 common where a process requires sign-off by senior management, like change
 board approvals and official governance processes. The lack of sufficiently
 shared situational awareness degrades the approver's ability to effectively
 execute their intended procedural duties. It can be caused by ineffective
 internal communication flows as well as poorly structured information.

 When mismatches happen, it is imperative to quickly find out how they have
 developed so they can be rectified. Is there a more appropriate way of\
 achieving the intent behind the process? Perhaps the process can be executed at
 a level where the right situational awareness exists, or the quality and flow
 of information can be improved such that the approver can effectively perform
 his or her duties.

 - **Regularly broken or circumvented:** Sometimes processes seem to be
 regularly broken or circumvented. One very common one is breaking a purchase
 into a lot of small transactions in order to work around a very slow process
 for anything over a particular value. Another is reusing old code or systems to
 avoid having to spend lots of time porting to some substandard"official"
 technology.

 These are all symptoms that a bigger problem exists. Rather than resorting to
 strict enforcement, the process needs to be reviewed to see why it is not
 followed.

 It is possible that the process is overly cumbersome, doesn't match actual
 conditions, or that its value is not understood by those who should be using
 it.

 Occasionally, much like the fact that certain statutes require that some
 financial transactions use fax technology, the process is simply no longer
 needed.

 Each of these symptoms is a good indicator that you have excessive processes.
 It is important to review processes regularly, whether or not there are obvious
 signs of problems. I usually encourage teams to look at whether any processes
 appear problematic or questionable at regular cycle sync points like
 retrospectives and strategic reviews, as discussed in Chapter 14, "Cycles and
 Sync Points."

 Good processes need to clearly contribute to the larger objectives, the ones
 that the customer cares about. Processes that do not do that in the most
 effective way need to be changed or removed entirely.

 ## Muri (Overburden)

![](images/4.6.png)
 **Рисунок 4.12**\
 "Surely there is room for just one more package in the release!"

 Not every form of problematic friction is a form of "pure waste." One such form
 is known in Lean as *Muri*, or overburden.

 Scientific Management and cost accounting have long trained managers to think
 of inputs as sunk costs that need to be fully exploited in the name of
 efficiency and cost management. People with such a mindset believe that
 anything less is"waste."

 Such overburdening is never good, and it can take many forms. Most people
 concern themselves with overburdened systems and machines, knowing that their
 reliability degrades with each little push beyond what is reasonable. However,
 there are two often overlooked forms of overburden that can damage our ability
 to deliver and make effective decisions: *overburdening people* and
 *overburdening releases*.

 ### Overburdening People

 Overburdening people is extremely common. Not only are managers frequently
 cajoling their staff to give it their all, many who are ambitious or nervous
 about losing their jobs also want to be seen going the extra mile. But such
 behavior is actually quite risky. There are, of course, the challenges that it
 can lead to burnout and leave little slack to compensate for any problems that
 occur. However, a far more pressing issue is the way that it damages decision
 making.

 When people are stressed or otherwise overburdened, they unconsciously narrow
 their attention to only the most critical aspects of the immediate task at
 hand. This forced myopia keeps the person from becoming overwhelmed, but at a
 significant cost.

 Less awareness makes it far more difficult to notice important facts or
 changing conditions across the ecosystem, limiting people's ability to learn
 and adjust. Research suggests that overburdened people are less productive and
 make more mistakes.[^2] Overwork also can cause those affected to miss important
 decision points along the way.


 [^2]: https://www.uclan.ac.uk/news/tired-and-overworked-employees-pose-huge-risk-to-business-data

 Another fact that many miss is that even one overburdened team member can
 affect decision making for the entire team. An overburdened team member is
 likely to feel too busy to share what information they do have, weakening the
 awareness of those around them. They are also more prone to miss deadlines and
 important sync points, and are typically far less willing to "waste time"\
 reviewing a situation or aiding their own learning and that of others. They
 don't have to step back, consider the big picture, and find a better approach.

 I run into overburdened people all the time. The worst part is that they are
 usually those that an organization can least afford to lose.

 So how do you fix overburdening your teams?

 It starts by making sure that the overburdened people attend the sync points,
 especially retrospectives and strategic reviews. They will try to refuse, which
 is when managers and teams can stage an intervention, sometimes even using a
 review session as a way to figure out how to redistribute or otherwise reduce
 workloads. It is also good to rotate those people to other areas that are new
 or different to them within the team's scope. Their insight will usually be
 valuable, and it will give them time to step back and realize for themselves
 the damage they were causing to themselves and others in their efforts to help
 the team succeed.

 ### Overloading Releases

 Having occasional big releases consisting of lots of changes bundled together
 can seem like a good thing. It gives developers more time to work on meatier\
 problems and gives testers more time to test. Operations people like the fact
 that there will be fewer release interrupts to worry about, while for customers
 a surge in new features can make a new release seem compelling.

 So why are big releases a bad thing?

 Rather perversely, many who favor the big release approach over having more
 frequent smaller ones usually end up increasing the very risk and delivery
 friction that many claim they are attempting to avoid. For starters, having
 fewer releases doesn't necessarily equate to less risk. In fact, bundling many
 changes means a thicket of new and different interactions. This creates a thick
 fog that obscures everyone's situational awareness. Which of the many changes
 might be the root cause of a new problem? It could be one or the interaction of
 many. If developers haven't fully thought out how each change might interact
 with others or, worse, if changes were made by several different teams, it
 could make troubleshooting and fault resolution far more difficult and time
 consuming.

 Having fewer releases doesn't really help reduce delivery friction, either.
 Giving developers longer to work on features can encourage long-lived branches
 and fewer check-ins. This reduces transparency and can result in a painful
 integration problem down the road. It also lets developers off the hook from
 thinking defensively about changes and how they might interact in the ecosystem
 if they go live before they are complete.

 Longer release cycles do not help testing, either. Shorter cycles require
 really understanding what is of high value to test. They also create an
 incentive to invest in improving test cycle times, allowing the organization to
 get more feedback more frequently. Longer cycles encourage generic testing with
 poorer focus and longer feedback cycles. This results in a poorer understanding
 of the health of the code, and often results in releases going live with lots
 of known bugs.

 The same goes for governance processes. Those used to working with large
 releases often fool themselves into believing that the only way any
 organization can have robust governance is to require many checkpoints full of
 reviews and detailed documentation in order to spot and mitigate potential
 risk. However, having necessarily heavy governance processes can actually make
 it more difficult to manage risk. Nobody likes having to justify everything
 they do, and the documentation process can be tedious and feel wasteful for
 everyone involved. When change tracking is limited and governance boards are
 run by managers who are not deeply technical or into the detailed minutiae,
 many smaller changes are simply missed or obfuscated in the name of expediency.

 There is also a time penalty. Change happens in more than software. People,
 usage patterns, business requirements, and regulatory requirements can all
 change, sometimes unexpectedly. More time means more opportunity for these
 changes to affect the operating environment of the service. A release that
 reflects the earlier conditions from when the project was started may be
 unsuited for current needs. Holding onto changes longer also delays customers
 and the business benefiting from their value, if their value isn't eroded away
 by changing conditions.

 What to do?

 All of these types of Muri can be avoided by looking at how work flows through
 each part of your system. As discussed in Chapter 12, "Workflow," visualizing
 workflow through effective use of Kanban boards and Queue Master rotations can
 go a long way to help spot problematic bottlenecks, including long wait times,
 deep queues, and lots of work in progress.

 Another useful measure is to look at code repository structures and statistics,
 as well as build, test, and deployment statistics. Does work get trapped on
 long-lived branches? Are certain tasks always handled by a tiny minority of the
 team? Are there long integration and test cycles with complex conflicts and
 seemingly intractable long-lived bugs? Do deployments touch a lot of different
 areas? Is it expected that there will be unstable periods after a production
 release?

 Understanding flow and Muri can help us create a sustainable balance that
 promotes the very awareness and learning needed to make better decisions and
 achieve our target outcomes.

 ## Mura (Fluctuation and Irregularity)

 **Figure 4.13**\
 *"*Well, this isn't much fun!"

 *Mura* means unevenness, irregularity, or lack of uniformity in Japanese. For
 manufacturing, unexpected shifts in customer demand, uncontrolled variability
 in products, unreliable equipment, and poor training can cause irregularity or
 fluctuation that can lead to organizational stress, quality problems, unhappy
 customers, and waste.

 IT also suffers from a variety of forms of fluctuation and irregularity, from
 sudden demand spikes to unexplained loading and configuration drift that
 hinders service delivery function and performance. This has become an even
 greater problem as IT services have become more demand based. Not only have
 service stacks become far more complex, potentially causing delivery and
 operational workload fluctuations, they are also shared, meaning that problems
 that once

 were localized, such as misconfigurations or instance failures, can have a
 widespread effect. Also, with shared usage, user uptake and usage patterns can
 compound in unique ways. This can lead to wild load fluctuations that can occur
 with little to no warning. These can cause large, complicated problems that can
 cripple a service and be challenging to rectify.

 The biggest mistake that people make is believing mura is both inevitable and
 unavoidable. It is not. Mura itself is caused by a situational awareness gap
 interacting with friction points in the ecosystem. This unknown can be caused
 by anything from an externally driven demand to an irregularity within the\
 ecosystem itself. The unexpected fluctuation or irregularity only causes a
 discernable problem when it catches on one or more friction points it
 encounters along the way.

 Another interesting aspect of mura is that the way we respond to the problem
 can heavily influence the severity of the outfall from the variation. In fact,
 it is one of the most common places where our instinctive reaction to the
 problem is likely to cause a further cascade of irregularity and friction that
 can compound the damage caused.

 As we will see, the best way to eliminate mura is to aggressively find and
 close situational awareness gaps wherever possible, all while simultaneously
 removing friction points and exploiting bottlenecks in the ecosystem.

 To better understand, let's take a deeper look at the two most common patterns:
 *unexpected demand variability* and *unmanaged variability*.

 ### Unexpected Demand Variability

 We are all familiar with the concept of fluctuating demand. Demand inevitably
 ebbs and flows throughout the day, week, or even year. Most variability is only
 noticed when a bottleneck, such as a store checkout queue or a traffic backup,
 creates some sort of noticeable delay or failure. Such variability, while\
 unpleasant, is tolerable when it follows predictable patterns that we can make
 adjustments for in advance to ease the pain.

 It is a very different story when demand shifts unexpectedly. Whether it is a
 lack of toilet paper or a suddenly overloaded web service, customer frustration
 builds to the breaking point as suppliers scramble to respond and adjust.

 For IT, demand-triggered variability is often a sign that the delivery arm has
 somehow become disconnected from the customer and their target outcomes. This
 loss in awareness makes it difficult to foresee even gradual changes until

 they cause a real problem. Crisis then ensues when the organization's response
 hits friction that makes it difficult to adjust sufficiently to deal with the
 situation.

 These sorts of awareness gaps tend to have two common causes.

 First, in some instances, Sales, Marketing, Product, and Support teams that do
 have regular contact with the customer want to reduce potential distractions
 and have more control over managing delivery team priorities by acting as a
 proxy between customer and delivery. While the reasoning can be sound, it often
 leads to information delays and context gaps. The end result is the delivery
 team seeing a stream of jobs that lack much of the important context of the
 actual outcome desired or the obstacles in the customer's way in reaching it.
 Not only do they have no easy means to build an understanding, they have no way
 of catching any mismatches that develop. This leaves a system full of awareness
 gaps and friction points where variability will thrive.

 Second, awareness gaps more commonly form around the fragmentation of
 organizational silos. Looking at the ecosystem from their fragmented
 perspective, neither the business nor the delivery sides can be fully aware of
 the customer or of the dynamics that drive behavior in their environment. This
 is never a great spot to be in, but really becomes a serious issue when one or
 both sides fully *believe* they have the true picture and that any
 misalignments are just noise or the other side's fault. The problem gets
 compounded by a lack of understanding of the health of the delivery side or its
 ability to handle demand shifts.

 In both cases, when the crisis hits, a cascade of problems erupts. Teams can
 become overwhelmed (*Muri*) or defensively fragment along functional lines
 (*Muda*) to avoid blame. The stress slows everything down, mistakes increase,
 and the organization's ability to deliver becomes severely disrupted.

 Even in the most minor cases the team will not completely recover. Previously
 promised work will be missed or suffer quality issues. Unless actively
 countered, trust will further erode while the facts of what happened are hidden
 or obscured for fear of blame. This further degrades situational awareness and
 puts severe limits on organizational learning and improvement. The stress of
 the event can also leave people stressed and create bad feelings across teams,
 adding further delivery friction.

 This may sound bad, but the problem rarely ends there. The awareness gap that
 caused the initial crisis often makes us misread what happened as a pure
 resourcing issue. Our instinctual response pushes us to make further\
 inappropriate decisions that only exacerbate the actual problem. The C-suite is
 particularly vulnerable to this. In most cases the reality on the ground has
 been

 obfuscated by the streams of cheery reports C-suite members receive and heavily
 managed interactions they have with their subordinates, meaning that often they
 too have lost their situational awareness.

 Let's take a look at what happens and why we often make things go from bad to
 worse.

 ### The Bullwhip Effect

 **Figure 4.14**\
 "Snap!"

 A variability-triggered crisis can seem very scary. When first reactions prove
 to be insufficient and everything appears to be sliding further into chaos, it
 is tempting to overreact and throw resources at the problem. This can be in the
 form of more infrastructure, more people, additional project time, extra
 features, or even more teams and software.

 On the surface, this response makes sense. More servers, software, and hands
 available to throw at a problem may feel like insurance, even if it increases
 costs and complexity. But the extra padding does little to solve the
 underlying\
 problems. Awareness is, at best, no better. In fact, the extra resources may
 simultaneously *increase* friction and *degrade* awareness. This can further
 compound the original problem and provide the necessary fuel to create a
 *bullwhip effect*.

 The bullwhip effect is a classic supply chain friction problem. It begins with
 a sudden unexpected shift in demand. This shift can start from a steady state
 or, as happened during the COVID-19 pandemic, be preceded by an abrupt demand

 drop that forces production to be dramatically reduced to a lower baseline. As
 you will see, the problem is not that there has been a demand shift but how
 much friction an organization needs to overcome to spot and adequately adjust
 to it.

 In IT these shifts typically take the form of load spikes and feature demand.
 IT teams respond by frantically trying to increase supply. For capacity, it
 might be panic buying and setting up new capacity or stealing it from other
 areas. For code, it could be hiring lots of developers or outsourcing large
 swaths of development.

 As demand hits the supply chain, the bulge hits friction points on the delivery
 side, creating a ripple effect of stress and delay. The more time and focus
 that growing capacity takes, the more the pressure to complete will build. Such
 stress inevitably will compel those in the supply chain to act without spending
 sufficient time investigating what is driving the demand, how long it might
 last, or the repercussions of their actions on other elements of the ecosystem.

 This is where the real damage kicks in.

 Once the situation has become stabilized, delivery friction now makes it\
 expensive and painful to change direction and bring things back to normal. This
 forces the organization into an untenable situation. If you ordered new
 resources (servers, people, software, etc.) you still need to take delivery
 even though they may be of little use. If you stole resources from somewhere
 else, you need to find a way of dealing with those ramifications. If you
 temporarily outsourced much of your development, you will need to figure out
 how to cost-effectively understand the state of the code and how best to manage
 and support it moving forward.

 The worst part of all of this is that there may be so much built-in friction
 that reversing any decisions made or mitigating the damage they might cause is
 often difficult or impossible. Budgets and project schedules are often blown,\
 sometimes in ways that incur high ongoing costs, with little to show for it.

 Another damaging element of the bullwhip effect is that, despite creating a
 whole new set of issues, the underlying problem that created the initial
 cascade remains unsolved. Until those friction and awareness gaps are
 addressed, there is nothing to stop this cycle from repeating over and over,
 wasting ever more precious resources as customers continue to feel neglected
 and underserved.

 ### Unmanaged Variability

 Not all variability is sudden or demand driven. It can just as easily live in
 our services and the wider environment. It might be caused by a slightly
 different

 configuration over here, subtle differences in understanding over there,
 customers with divergent usage patterns or needs, or even aberrations caused by
 differences in the ordering of events. These quietly build like so many layers
 of paint and grime on a wall, obfuscating the real state of the ecosystem in
 ways that make it increasingly less predictable and reproducible.

 Rising complexity in technology stacks, along with the growing adoption of
 virtualization and containers, has only increased the number of opportunities
 for variability. Everything from varying hardware components in computers,
 differences in compiler-generated byte code and software patch version, to
 unseen resource contention that varies the sequence and timing of operations
 can cause subtle yet important variations in behavior. Even differences in
 client endpoints and the way they access services can have a noticeable effect.

 Increasing the number of moving parts only adds to the risk.

 The growth and fragmentation of organizations hasn't helped matters.

 Organizational silos can create drift in interpretations and implementation
 details. It only takes one misunderstanding between individuals or teams to
 create havoc that can easily disrupt the service.

 Despite this growing complexity, many in IT seem to approach these challenges
 optimistically unaware. Those who do concern themselves with unmanaged
 variability often mistakenly believe that it can be fixed simply by forcing
 everyone to follow prescriptive processes.

 ### The Snowflake

 **Figure 4.15**\
 Snowflakes are all unique and fragile in their own special way.

 As children we are told that every snowflake is different. This makes its
 fragile beauty special because it is both one of a kind and ephemeral. Few
 would suggest that these are qualities that we want in our IT services. Yet,
 the ways in which many organizations build and manage environments make
 snowflakes in IT frighteningly common.

 In 2012 Martin Fowler wrote a blog post that coined the term "snowflake
 server."[^3] Snowflakes are server and software configurations that have
 organically grown and changed over time to the point where it is nearly
 impossible to exactly duplicate them. They can happen anywhere, from server and
 data configurations to external environment factors such as hidden resource
 contention in virtualized or containerized environments.

 [^3]: https://martinfowler.com/bliki/SnowflakeServer.html

 More often than not this drift happens through special "one-off" tweaks, such
 as manual modifications to fix a problem and get things working. Other times
 the drift is caused by poor packaging and patching that leaves installation and
 update detritus scattered about. With the "job done," people often forget about
 the details of what or how it was done. As one-offs build, it becomes harder
 and harder to figure out everything that makes them different from what we
 think they should be. They become increasingly unpredictable and dangerous,
 sometimes to the point of paralyzing improvement and putting the business at
 risk.

 Those who are faced with having to reproduce unknown one-off configurations
 often try to overcome the problem by simply imaging the disks of the deployed
 instances bit by bit. But as Fowler notes, such hacks not only perpetuate the
 buildup of cruft, they also do nothing to ensure consistent and understandable
 behavior.

 ### Minimizing Mura

 The best way to minimize mura is to look at tackling its root causes. That
 doesn't mean trying to avoid shifts and change. Ecosystem change is
 unavoidable.

 However, we can do something about minimizing problematic friction.

 The first and most important thing to do is eliminate any avoidable gaps in
 situational awareness throughout your environment wherever possible.

 Regardless of whether we are a junior staff member or the CEO, we all
 unintentionally do things that can create false assumptions, communication
 breaks, and misunderstanding.

 The following are some questions that you and the rest of your team might want
 to consider asking yourselves in an effort to minimize mura:

 - Do organizational silos exist and, if so, are they necessary? If they do and
 they are somehow unavoidable, can software and infrastructural dependencies
 that cross team boundaries be minimized? Can work be restructured to improve
 transparency and communication across organizational boundaries in a way that
 improves situational awareness, collaboration, and trust?

 - Have you eliminated all knowledge "single points of failure"? These are
 places where only a small number of people know an element within your\
 environment. This could be code, configuration, how to deploy, how to use, how
 to troubleshoot, or anything else that is important within the service
 lifecycle. The best way to test this is to see how well tasks can be rotated
 among people in the team. If only a small fraction can do the work, they should
 pass on their skills so that others can do it as well as they can.

 - Does every API have an owner? If so, do the owners ensure that API\
 compatibility and coupling best practices are in place to allow for changes to
 be made by one team with minimal impact to others?

 - Have similar things been done at the data level, where every piece of data
 has an owner, and the data quality, rate of change, and importance are
 understood?

 Have dependencies been minimized wherever possible so that they can be easily
 managed?

 - Are there ways that you can authoritatively know what is out in your
 environment, including how everything is configured?

 - Can everything be easily reproduced exactly without resorting to imaging?

 - Can software be deployed and configured atomically?

 - Are differences between deployments and versions captured, known, and
 understood?

 - Do you avoid uncontrolled one-offs? The best way to test this is to check
 that every release and patch is fully version controlled, all changes made by
 scripts are fully transparent, logged, and auditable, and if shell access
 cannot be eliminated, that write and execute privileges are both minimal and
 fully logged and auditable.

 Minimizing variation wherever possible does help. Unfortunately, eliminating
 all of it is nearly impossible. Your services may depend upon shared
 infrastructure and services that you neither control nor have full transparency
 into. You may be dependent upon technologies and data that you do not have
 direct access to examine, or your customers may be unwilling to reveal enough
 about what they are doing and why to help you forecast patterns ahead of time.
 You may even have legacy "snowflake" servers, software, and processes. One
 thing you can do is design your environment to be resilient to chaos. I refer
 to this as the "Defend against the Madman" approach.

 The way this model works is simple. If your service has an element that lacks
 sufficient transparency, imagine that it is in the hands of a madman and try to
 figure out the worst damage that that element can do, and how it might do it,
 to the parts of your service that you know. If it is a cloud service, imagine
 someone taking resources away randomly or loading things down where clock ticks
 become distorted. How would you track its effect and engineer against it? What
 sorts of user activity could be dangerous, how could you spot that activity,
 and what could you do to manage the situation? If the component or service
 lives in a snowflake configuration, imagine a malicious and crazed person
 running through

 the halls and in the data center with an ax. What could that person destroy
 that would be difficult, painful, or just plain impossible to replace or
 recover from? Is there a server or disk array that is really important and
 difficult to replicate? Are there particular people who have knowledge or
 skills that no one else possesses?

 As equipment goes offline, what are users experiencing with the service? How
 can you make any friction visible, and what can you do to mitigate it?

 All of this probably sounds improbable, but it does the job of breaking the
 overly optimistic happy-path approach that seems to pervade the IT industry. If
 you take it seriously, you begin to approach challenges defensively, thinking
 through failure modes and how variability might strike. This also moves us
 closer to reducing the level of variability that we, and ultimately our
 customers, are exposed to.

 This concept is hardly new in our industry. It goes to the root of much of the
 thinking behind test-driven development (TDD), where you write the tests first
 that capture the various use cases that your code might eventually be exposed
 to before you write your code. This helps with thinking through the problem set
 before you code rather than being colored by the way you put it together after
 the fact.

> #### Netflix and Their Variability Monkeys
>
> **Figure 4.16**\
>  Are your services resilient against the Simian Army?
>
> Anyone who has been dependent upon a supplier for critical infrastructure or
> services has probably experienced at some point problems with service
> predictability and reliability. Some of the more famous ones, such as the
> datacenter power outages at 365 Main in 2007, the severed undersea cables off
> of Egypt in December 2009, and some of the larger AWS outages, caused major
> disruptions for thousands of businesses and millions of people.
>
> As services become ever more complex, chances are that variability will get
> worse. Anyone who has built infrastructure at massive scale can tell you, the
> more moving parts that you have, the higher the probability that something
> will fail. Urs Hölzle, VP of Technical Infrastructure at Google, once gave a
> metric that if you have a cluster of 10,000 servers, each consisting of
> components with a rated Mean Time Between Failure (MTBF) of 10,000 days, you
> can expect at least one failure a day.[^4] When you combine outsourcing and
> scale, the chances of having a failure that you have little control over can
> become extremely high.
>
> [^4]: The Datacenter as a Computer: An Introduction to the Design of
> Warehouse-Scale Machines* (p. 77), Luiz Andre Barroso and Urs Hölzle, 2009
>
> Fortunately, few of us work at a scale with mission-critical services where
> such failures are severe enough to be fatal to a business. That said, with the
> growth in adoption of cloud services stacks, this problem is becoming more and
> more prevalent to enterprises. Netflix is an extreme example of a company that
> has taken such concerns into account and come up with a novel solution for
> dealing with them.
>
> Not long after Netflix began to offer video streaming services, they looked to
> leverage external infrastructure providers to allow them to more rapidly and
> elastically scale. At the time, demand for streaming services was unclear. In
> such conditions investment in lots of expensive infrastructure could prove
> fatal to the business.
>
> However, outsourcing core services can also be dangerous. Outsource providers
> may not sufficiently understand your business or may provide services that do
> not quite meet customer expectations. Netflix decided to depend heavily upon
> Amazon's AWS cloud services. This exposed large parts of Netflix's streaming
> business to the risk of service delivery shortfalls from AWS.
>
> Rather than optimistically expect stability and reliability, Netflix took a
> different path. Their early work with AWS made them realize that there would
> be a lot of instability. They saw that AWS's co-tenancy model was not set up
> to provide the level of predictability or reliability Netflix's complex
> workload required. Such variability meant Netflix could not rely on having
> sufficient integrity for every process.
>
> Instead, Netflix decided to build their services to expect and accommodate
> failure at any level. To this end, they built a series of tools they called
> the Simian Army that roam over their services, randomly killing and degrading
> servers and applications to ensure failure. They feel that if they are not
> constantly testing their ability to succeed despite failure, then it is not
> likely to work in the event of an unexpected outage when it matters most.
>
> Unlike most companies who try to do this in protected test environments,
> Netflix runs these tools in production. That way, they remove all the
> uncertainty that simulation creates, and firmly ensconce in the minds of
> engineers that their code will be put to the test in circumstances that matter
> and that they will have to pay attention > to. Engineers have to build far
> more defensively, understand what will happen when things go wrong, and put in
> safeguards to recover. By dealing with the variation as a given, it stops
> being an issue, resulting in far more robust and resilient services.

## See the Whole

 **Figure 4.17**\
 "I think that dolphin over there wants us to dive in and play!"

 As you might imagine, it is rare for most sources of friction in the service
 ecosystem to neatly fit in one category or have one simple root cause. Often,
 they layer on top of one another, creating a tangled mess of dysfunction.

 For this reason, Lean embraces examining the whole value stream from the time
 an order is received until a solution is delivered to address it. Leaders are
 encouraged to walk the floor ("go to the Gemba") to look at the end-to-end flow
 with their own eyes. They do this not to tell people on the floor how to do
 their

 jobs, but to help find the impediments that reduce awareness within the
 workspace as well as across the line.

 To improve awareness and reduce bottlenecks, the structure of work in Lean
 organizations tends to be more fluid, with fewer sharply defined roles. In Lean
 Manufacturing, people are encouraged to work together to make adjustments to
 the structures of their work stations and their way of working to improve flow
 and reduce errors. Information can flow naturally, allowing workers flexibility
 and awareness that helps shape meaningful continuity between their work and the
 end product.

 Lean organizations also reach out to customers and suppliers in order to
 understand and work together toward achieving the desired outcome. When Toyota
 decided to enter the US minivan market, they had their design team drive around
 the US in a minivan to understand the needs and desires of the market.

 Similarly, they drove European luxury cars in Europe and the US before
 embarking on Lexus. Toyota also regularly works with suppliers to help them
 understand and adopt Lean practices, knowing that their improvements will help
 both Toyota and their customers in the end.

 ## Summary

 Focusing only on improvements that increase delivery speed and throughput does
 little to ensure you and your team deliver effectively. Friction "wastes" in
 your delivery ecosystem can damage responsiveness and increase team workload
 all while reducing your ability to deliver the outcomes that your customers
 expect and your organization needs to be successful.

 As you will see in the next chapter, gaps in your situational awareness caused
 by friction and your inability to understand your delivery ecosystem also have
 a significant impact on delivery and service operational risk in ways that
 reduce the efficacy of traditional IT risk management mechanisms.
