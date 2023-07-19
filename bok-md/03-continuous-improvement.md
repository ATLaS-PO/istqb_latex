## Structured Problem-Solving Approach for Testing and Quality Activities {#structured-problem-solving-approach-for-testing-and-quality-activities}

Problem-solving in a value-driven organization may need to span multiple agile teams and sometimes even multiple value streams, as discussed in Chapter 2. This requires a problem-solving approach that both aligns with lean and agile practices and takes a holistic view. Therefore, agile test leaders and agile test team leaders need to be able to understand and use theories and techniques from systems thinking to identify root causes in complex environments.

### Plan-Do-Check-Act Cycle
The PDCA cycle is a practical problem-solving and continuous improvement approach. PDCA can be used for local improvement experiments, e.g., reducing web-interface performance efficiency testing lead time. In the same way, broader improvement initiatives may also use PDCA cycles, e.g., several interdependent agile teams working on the same products want to reduce the number of defects.

Usually, PDCA starts with a gap analysis, which describes the goal and then describes the actual situation. The difference between the two is the gap. Such gaps could, for example, be to achieve a new goal, or to fix underperformance in the present set-up. Then it is possible to address the gap by using the PDCA cycle through a series of step improvements.

PDCA is closely connected to quality management. By using PDCA, an organization can effectively manage and continually improve its effectiveness and the quality of its deliveries, and thereby the value delivered to its customers. In an agile at scale context, where people see quality as a shared responsibility, PDCA has several benefits, such as:

* Minimizing recurring quality problems.
* Supporting people to form fact-based insights to derive improvement actions. It helps to rationalize effort for the whole organization while moving toward business agility.
* Leading to a systematic and in-depth observation throughout the value streams. As a result, people develop a better understanding of their organization's performance and quality.
* When PDCA cycles are repeated, they generate knowledge for people and their organizations.

A fundamental principle of PDCA is iteration. A PDCA cycle begins with the Plan step, where the key activity is to develop an appropriate understanding of the problem or business opportunity and come up with a plan (hypothesis) for implementation, including how to check if the hypothesis is valid using some metric.

In the Do step, the previously created plan is put into action as outlined.

The purpose of the Check step is to measure the effects of the actions implemented during the Do step. A check requires comparison of the actual results against the target results and predictions that were defined during the Plan step. Negative results will often lead to the start of a new PDCA cycle. Additionally, results that are better than expected or targeted, can provide opportunities for new PDCA cycles.

During the Act step, based on the findings, measures are taken to make sure implementation of new ways of working are sustainable. This may involve the standardization of processes.

Here is an example of how PDCA can be used in solving problems across multiple agile teams in an organization:

Two teams have received negative feedback about non-functional quality aspects of a product from an important customer they both develop for.

* Plan: The agile test leader sees the feedback as an opportunity to identify and discuss the perceived problem with the product owner (PO). They come up with the hypothesis that one root cause of the problem is the lack of concrete and customer-relevant performance efficiency requirements, which leads to poor implementation and testing. The test leader talks to the two teams and to the customer contacts they both have and comes up with a plan to try a workshop format that involves team members and customer representatives. The Plan step of PDCA is to run a workshop and check that:
  * Teams confirm the format fundamentally improves understanding of the areas that are performance critical to the customer
  * Such workshop formats produce testable performance efficiency criteria
  * The customer gives positive feedback that participating on a regular basis is an acceptable investment for them
  * The ongoing development after the workshop uses the workshop results for testing, and therefore produces relevant results
* Do: The workshop is held, and the two teams use the performance criteria of the workshop in development and testing of the next iterations.
* Check: In a retrospective after the release, all of the criteria set up in the Plan step are met. Additional feedback from team members is that, in some areas, customer feedback was too narrow for some kinds of performance efficiency testing.
* Act: A wiki description of the workshop format is documented and the PO organization agrees to hold at least one workshop on non-functional criteria with a customer each quarter. This last decision can be seen as the Plan step into another PDCA cycle. Furthermore, the teams collaborate with product owners for using additional industry benchmarks as performance efficiency acceptance criteria, which are set as a standard.

Here is an example where the Act step is skipped because the expected improvements would not be realized based on the pilot results:

The use of the company's test management tool is called into question by some agile teams. The tool seems old-fashioned and is not kept up to date. However, despite the obvious shortcomings, the tool is not being officially discontinued. Some teams have already looked for an alternative tool to help them connect their tests with the continuous integration (CI) pipeline; some say that the existing tool is the only way to get an overview of system tests for maintaining the regression test suite. Three teams hold separate retrospectives about the test management tool and decide that they will see if they can find a replacement tool by running proof of concepts, where each team will use a different tool.

* Plan: An agile test leader confers with the scrum masters of the different teams and they hold a multi-team retrospective. They develop a plan with the goal of finding a test management tool that would become mandatory to use for all the agile teams. It is decided to stop one of the team's pilots, which was based on technology that could not be used by other teams, and let the other two pilots proceed. It is also decided that both proof of concept pilots will each be reviewed by another team.
* Do: In the Do step both teams continue with their pilot, documenting the good and bad experiences with the respective tools they have chosen. Both teams come to the conclusion that they would like to continue with their tool.
* Check: Each team reviews the pilot results and conclusions made by the other team. However, the team that has not tried the tool themselves does not come to the same positive conclusion based on the findings of the other team. The results are discussed in a workshop to see if continuing with two tools could be a long-term solution. Since the agreement was that it should be one common tool, the teams do not continue to the Act step. Instead, it is agreed that a new plan is needed.

In a quality assistance context, an agile test leader may facilitate a PDCA cycle to resolve a large number of "not complete and accurate" work products throughout a value stream. While defining a future state value stream map, teams may test some assumptions and validate their actions in the context of different PDCA cycles, e.g., the high number of "not complete and accurate" work products might be one of the main causes for the high lead time.

For further elaboration of different methods for test process improvement, see Expert Level in _Improving the Testing Process_ [@ISTQB:2011].

### Embedding PDCA in the Organization
As mentioned before, PDCA can be used for local improvement experiments and for broader improvement initiatives.

In agile scaling frameworks, the typical organizational settings for running PDCA for software development and testing are:

* Multi-team retrospectives
* Project and program level improvement boards
* Time boxes for improvement efforts during release planning meetings

Running PDCA in the context of business agility requires:

* Shared understanding of what a problem is before starting a PDCA cycle. A problem is a performance gap between an expectation and the current reality, e.g., a surprising number of defects, an additional lead time for a release, or an unsatisfied customer are all problems. Numbers are essential when expressing a performance gap. Therefore, we start a PDCA cycle regarding customer satisfaction only when we know the current satisfaction rating (e.g., 8) and the target (e.g., 9).
* Describing a problem correctly is critical, e.g., a client representative may describe a missed milestone as a lead time gap—we spent 23 days instead of the 10 originally planned. Everybody should learn the ability to report accurately by practicing within the organization. A quality assistance approach supports putting that in motion.
* Ability to find problems or opportunities throughout the organization. Everyone should be able to identify problems anywhere and resolve them appropriately as soon as they arise. This requires an environment where people feel safe to reveal errors .Aculture of accepting errors , which sees errors as an opportunity to learn, is essential to implement improvement at the organizational level.

A problem or opportunity for which it is appropriate to conduct a PDCA cycle has to have a direct impact on customers. Resolving such a problem increases the organization's ability to deliver more value to its customers.

Agile teams can conduct a PDCA cycle over several retrospectives. For example, during the first session, a team could agree and define the problem, perform observations, and devise a plan. Then, during the iteration , they execute the actions as previously devised. So, the subsequent retrospective could be about the Check of the PDCA cycle.

The actions that we devised and executed during the Plan step generates conclusions during the Act step. Primarily, this step is about making necessary changes to the process moving forward. The outcome is typically to create work standards that everyone will use until the next PDCA cycle defines something better [@liker:2006]. A way to spread a work standard over an organization is to use formal and practical training sessions in pair mode.

Embedding PDCA in an organization is a lot about finding opportunities to learn. Opportunities can arise from everyday work, or they can be actively identified for by comparing the current situation with examples from other teams, companies, or models that try to measure agile maturity.

Many agile scaling frameworks try to measure, and hence make transparent, organizational effectiveness. This needs a safe, transparent environment, otherwise measuring team and value stream maturity can push people and teams to hide what is going on so as not to be considered inefficient. If a company has crafted a fitting maturity model, on the other hand, this can help to spot opportunities for PDCA cycles.

Teams that "Do" local improvement efforts should also go through the following steps:

* Identify, for example:
  * Define a test metric which can be used by others in a different part of the organization
  * Analyze responses from a user help desk ticketing system and document the result in the knowledge management system so that it is visible for all
  * Conduct detailed analysis as to what kind of coverage really is measured in the CI pipeline and write an article describing it in the company's knowledge management system
* Align, for example:
  * Actively facilitate discussions with software architects about testability
  * Share the identified problem with a testing community of practice and encourage their input in the improvement efforts
* Realize, for example:
  * Write transparent (just enough) documentation as part of the realization of the improvement experiments
* Signpost local PDCA experiments across the organization in order to allow implementation of improvements where helpful and generate organizational learning
  * Let a community of practice know the results of experiments
  * Use big openly visible monitors showing dashboards of the CI pipeline
  * Make sure that improvement experiments and results are accessible in knowledge management systems beyond the team
  * Include results of team improvement efforts in discussions at multi-team retrospectives

To identify, align, realize, and signpost can be seen as a second cycle within the Do step [@bendek:2018].

To sum up, supporting conditions for a good PDCA culture on an organizational level can mean: :

* Teams behave in a way that fosters the potential for organizational improvements.
* Official meetings and processes for improvement beyond the team level are encouraged across the organization.
* There is management support for multi-team PDCA meetings and processes, since, without that, local improvement initiatives will mostly fail to have broader impact.

## Systems Thinking and Analysis of Root Causes {#systems-thinking-and-analysis-of-root-causes}

Leading a quality assistance approach on an organizational and strategic level requires a broader view than a single delivery, project, or department. Systems thinking and root cause analysis are important disciplines that provide many different techniques to analyze complex problems. An agile test leader needs to participate in and facilitate analysis of complex problems to help the organization grow and optimize its value streams.

### Systems Thinking

Systems thinking is a crucial discipline when scaling agile from a software development approach used primarily by IT teams to a value-driven approach that includes everyone in the organization. Some of the frameworks for scaling agile have systems thinking as one of the key principles, e.g.,LeSS [@less:2021] and SAFe [@scaledAgile-thinking:2021].

Although there are many different definitions of systems thinking, they all have some characteristics in common. The following list is summarized from [@stave:2007]:

* Recognizing interconnections: Seeing the whole system and understanding how the parts of the system relate to the whole.
* Identifying feedback: Identifying cause-and-effect relationships between parts of a system, describing chains of causal relationships, recognizing that closed causal chains create feedback, and identifying polarity of individual relationships and feedback loops.
* Understanding dynamic behavior: Understanding that feedback is responsible for generating the patterns of behavior exhibited by a system, defining system problems in terms of dynamic behavior, seeing system behavior as a function of internal structure rather than external disturbance, understanding the types of behavior patterns associated with different types of feedback structures, and recognizing the effect of delays on behavior.
* Differentiating types of flows and variables: Understanding the difference between being able to identify rates, levels, material, and information flow, and understanding the way different variables work in a system.
* Using conceptual models: Synthesizing and applying the concepts of causality, feedback,and types of variables.
* Creating simulation models:By describingsystem connections inmathematical terms[^4].
* Testing policies: Using simulation models to identify leverage points and test hypotheses fordecision making.

[^4]: Some authors regard creating simulation models as anadvanced component of systems thinking.Other authors regard it as beyond the definition of systems thinking [@stave:2007].

In systems thinking, a value stream is one type of system in an organization [@scaledAgile-thinking:2021]. It is essential that the full value stream is optimized and not just one of its parts. The organization is also a type of system, as well as the technical systems [@scaledAgile-thinking:2021]. Systems thinking includes identifying and understanding systems, predicting their behaviors, and devising modifications to them in order to produce desired effects [@arnold:2015].

Peter Senge has described systems thinking as the essentialdiscipline needed to build a learning organization. One of the challenges with learning is that cause and effect are not always closely linked in time and space. The most critical decisions made in many organizations have system-wide consequences that stretch over years or decades [@senge:1990].

Systems thinking techniques help to [@less:2021]:

* Understand system dynamics
* Identify root causes in complex systems
* Challenge existing mental models
* Avoid local optimization

As mentioned earlier in [Quality Assistance](#section:quality-assistance) and [Improve Quality and Flow in a Value-Driven Organization](#section:improve-quality-and-flow-in-a-value-driven-drganization), when adopting a quality assistance approach, agile test leaders help optimize the full system and not just a team or department of testers. If agile test leaders do not have basic skills in systems thinking, there is a risk of local optimization (i.e., changes that will improve testing but result in a decrease of the total value delivery). The risk is higher when using a traditional development approach because quality and testing activities are often handled as part of each development level. Especially when the test level follows the development, it can be hard to optimize holistically.

System thinking can be used in many different situations, e.g., problem solving, decision making, multi-team retrospectives, and process improvement. Two techniques used in systems thinking are covered next.

### Root Causes

As is discussed in the Foundation Level syllabus [@ISTQB:2018], root cause analysis is essential for good retrospectives.

When multiple agile teams need to collaborate in order to implement a system or a solution, some of the QA and testing activities will span multiple teams and the responsibility for delivering a working solution is normally shared between the teams. When problems occur, the agile teams need to collaborate to understand what is causing the problems and how to solve them effectively. If a single team tries to fix a problem without having a full picture of the solution, this may cause new problems for the other agile teams or only work in limited situations.

Potential problems that often span multiple teams include:

* Failed releases in production
* Unstable and/or shared test environments
* Fragile test automation
* Design for testability
* Integration with systems or solutions delivered by external partners or suppliers
* Certain levels and types of tests due to dependencies (e.g., system testing, system integration testing, hardware– software integration testing, system of systems testing, and field testing)
* How to validate business hypotheses

Besides problems, there are other good reasons for focusing on QA and testing across multiple agile teams:

* Reducing license costs or other costs connected to tools, equipment, or other things needed for QA and testing purposes
* Identifying and leveraging synergies by aligning on tool suites and processes
* General improvement and optimization of QA and testing activities
* Continuous attention to important areas (high business risk) to keep them at their current level and avoid regression
* Creating knowledge and common understanding of the system and processes

Finding bottlenecks in a value stream often means a root cause for waste has been found. The theory of constraints (TOC) described in The Goal [@goldratt:2004] gives practical advice on how to look for bottlenecks in different systems. If the organization moves from a traditional to an agile set-up there may be bottlenecks in the development value stream. Here are examples in order of rising maturity:

#. Environment creation: Testers can help by providing methods used for automated set-up of test environments for the whole value stream. Testers might need to learn about new technological trends, such as infrastructure as code. Test environments that are available as self- service can avoid bottlenecks.
#. Code deployment: Testers can help with automating deployment safely, securely, and reliably.
#. System testing: A countermeasure can be to massively automate and parallelize system tests. Another countermeasure is to shift left tests to component testing and component integration testingand only rely on system tests if strictly necessary. Test data for complex system test environments that is available as a self-service can avoid bottlenecks.
#. Software architecture: Moving from tight to loosely coupled architectures can reduce lead times. Testers can support developers practicing domain-driven design with their domain knowledge (see [@ISTQB:2019]). Testers might have to learn new technologies such as microservice architecture.

There is a range of approaches found in lean (Lean Six Sigma or other lean bodies of knowledge) that can also be used in software development. The most basic root-cause analysis technique in lean is the "Five Whys." This is a practice of asking "Why?" repeatedly whenever a problem is encountered in order to get beyond the obvious symptoms and discover the root cause. Two other frequently used techniques are Pareto charts and fishbone diagrams.

Sometimes, static models (like the fishbone diagram) do not dig deep enough to really understand root causes in dynamic systems. For a technical example common in "system under tests" software that testers encounter, think of defects introduced by timing problems, which can be very hard to capture and understand. Causal loop diagram is a tool for representing the feedback structure of systems. The diagram can be used for modeling technical systems as well as systems that are built from human interactions. A CLD originates from flow diagrams, which were used to analyze industrial dynamics.

### Causal Loop Diagram

As explained at the beginning of [Systems Thinking and Analysis of Root Causes](#section:systems-thinking-and-analysis-of-root-causes), systems thinking is crucial for understanding, analyzing, and changing complex systems, such as a value stream, a part of the organization, or the system landscape. One way of doing that is by using a CLD, which is also sometimes called a system model [@larman:2016].

A CLD is a thinking tool that helps visualize and analyze cause-and-effect relationships and feedback loops in a system. It shows how different variables affect each other and create reinforcing or balancing loops.

The benefit of a CLD is that it reveals the non-obvious causes and effects and their interconnectedness in a broader system. It helps to see beyond the immediate, visible symptoms and thereby to find more effective and long-lasting solutions to problems. Unlike other, simpler, techniques for root cause analysis, CLD can include details that help explain the system's complexity, e.g., delays in feedback and how the goals that the organization is pursuing affect the system. In the latter case, revising the goal is sometimes the most effective and efficient solution. Other benefits of CLD are:

* Getting started isthe only requirement to draw together
* Learning to see systems dynamics
* Building a shared understanding of complex problems
* Eliciting and capturing the mental models of individuals or teams
* Communicating the important causal loops that could be responsible for a problem

A CLD consists of four basic elements: variables; the links between variables; a plus or minus sign on the links, which show how the variables are interconnected; and loop markers, which show what type of behavior the system will produce [@sterman:2000]. There are different notations used in CLD. <#table:label> is an example of CLD notation elements. <#figure:genericCLDnotation> is a generic example of a CLD to show the basic notation.

To create a CLD it is important to have a group of people with different perspectives of the problem or system at hand. The main steps, which are repeated as the discussion evolves, are:

#. Define variables
#. Define causal relationships between variables
#. Describe what effect one variable has on another
#. Add other factors that affect the system (e.g., delays and goals)
#. Identify and describe reinforcing and balancing causal loops
#. Identify possible interventions to resolve the problem

| ![variable](RackMultipart20230716-1-22hy1u_html_902808437bd60a20.png)
 | Variable. An important aspect of the system.Typicallysomething that is quantifiable, e.g., velocity (rate of delivery) of features, quality of the code , number of defects. |
| --- | --- |
| ![causalLink](RackMultipart20230716-1-22hy1u_html_afe01db51566e718.png)

 | Causal link. Shows that there is a relation between variables, e.g., if the number of defects increases, then the amount of waste increases, and vice versa. |
| ![plusSign](RackMultipart20230716-1-22hy1u_html_f33bc89d1db42a6f.png)
 | Plus sign (+). Shows that a change in one variable leads to a change in the second variable in the same direction, e.g., if the number of testers available to work decreases, the organizational productivity will also decrease. |
| ![minusSign](RackMultipart20230716-1-22hy1u_html_8d3a83ddc56e112.png) | Minus sign (-). Shows that a change in the first variable causes a change in the opposite direction in the second variable, e.g., if the number of experienced testers goes down, then the number of defects goes up, and vice versa. |
| ![delay](RackMultipart20230716-1-22hy1u_html_b8101bb0748796c5.png) | Delay. If there is a significant time delay between the changeof a variable and the influence on the depending variable, this is marked with "DELAY" on the arrows. |
| ![balance](RackMultipart20230716-1-22hy1u_html_48bbdbf55340cf1b.png)
 | Balance (B).The causal influences in the loop keep things in balance.Loops with an odd number of minus signs are balancing. |
|
 ![reinforce](RackMultipart20230716-1-22hy1u_html_d496fbcb70de2be9.png) | Reinforce (R).The causal relationships within the loop createexponentialgrowth.Loops with an even number of minus signs are reinforcing. |
|
 ![goal](RackMultipart20230716-1-22hy1u_html_73db38e85e39efa6.png)

goal:desiredquality




 | Goal.The outcome that someone wants to achieve. Teams,people, complex systems, and organizations have goals. |

: Notation and examples in casual loop diagrams. \label{table:label}

![genericCLDnotation](RackMultipart20230716-1-22hy1u_html_c2aef9ea74b8d9e6.png "Example of a generic CLD notation.")

It can take several sessions to visualize a complex system. One important aspect is to qualify the effects with data from real life. Otherwise, the model may just reinforce existing mental models and not show the flaws they might have.

Tips that help to visualize CLDs concisely and meaningfully are:

* Select good variable names (use nouns, use variables which represent quantities that can vary over time, choose the more positive sense of variable names)
* Include possible, unintended consequences as well as the expected outcomes
* Include goals (e.g., a short loop which states that "actions to improve quality" raise "quality" and "quality" reduces "the number of actions to improve quality" may not be clear)

One could add "quality gap" and "desired quality" to <#figure:diagramWithoutGoal> to emphasize that "quality" reduces "quality gap" and "quality gap" is a driver for "actions to improve quality."

![diagramWithoutGoal](RackMultipart20230716-1-22hy1u_html_44a3da2aa7d34d12.png "Example of a simple causal loop diagram without a goal.")

![diagramWithSpecifiedGoal](RackMultipart20230716-1-22hy1u_html_25bbbf1409bc1db0.png "Example of a causal loop diagram with a specified goal.")

In <#figure:diagramWithSpecifiedGoal>, the "desired quality" box is added outside the loop to show that it should not be changed during a quality cycle.

* It can be helpful to distinguish between perceived and actual states (e.g. "perceived quality" and "actual quality").
* It can be helpful to start with variables that sum up multiple aspects for a first understanding (e.g., "test automation maturity" can be a starting variable and later be split in "percentage of test scripts automated", "test environment maturity", "number of test automation katas held").
* Add additional larger loop cycles if needed to add long-term to short-term consequences (e.g., "independent test assessment" raises "quality", but, as shown in <#figure:causalLoopDiagram>, an additional path might be "perceived pressure in the teams" adds to "hiding of problems" that lowers "overall quality," since root causes are hidden by teams and become less visible for the organization).

![causalLoopDiagram](RackMultipart20230716-1-22hy1u_html_7ef86585302c17f1.png "Example of a causal loop diagram with short-term and long-term consequences.")

* If a link requires too much explanation it can be refined adding extra variables (e.g., if it is unclear why "market demand" lowers "quality," a new variable, "pressure to release," could be added).
* A CLD should concentrate on genuine causal relationships (e.g., a diagram should avoid stating that the "number of test cases" raises "product sales." It could, on the other hand, argue that the "number of opportunities to find and fix gaps" that can be found in the development process raises the "overall number of test cases" on the one hand and raises "product quality" and hence "product sales" on the other hand).

When collecting and analyzing the results of an overall retrospective or multi-team retrospective, it is easy to fall into local optimization pitfalls, e.g., if a bottom-up approach is used for collecting and analyzing results, it is sometimes forgotten that the system is not the sum of its parts. The focus should be on the system (e.g., value-driven organization, large-scale system).

CLD can be used on different types of agile retrospectives (e.g., multi-team and overall retrospective),because the focus of each retrospective should be on the system [@larman:2016]. CLD is conceptually simple but is not easy to apply without the appropriate experience and support.