## Establish an Organizational Test Strategy

Test strategies exist on different levels of abstraction:

* On the operational level agile teams decide how to approach testing and how to integrate testing tasks into the overall workflow of their iterations.
* On the product level multiple agile teams working together decide how to establish the right quality at the right time to improve the overall effectiveness and efficiency of their value streams.
* On the organizational level strategic decisions are made to establish the testing capabilities and skills needed to foster a quality mindset and culture which supports business agility.

This certification focuses on test strategy on an organizational level. An organizational test strategy needs to be aligned with and contribute to the achievement of the business objectives of a value-driven organization. Hence it often covers a similar time horizon which is typically 3-5 years and is adjusted as objectives are met or capabilities sufficiently improved. The smaller adjustments could happen on a 1-year rolling wave basis. Test strategies on lower levels evolve much quicker due to the faster feedback and learning cycles of product releases (product level) and iterations (operational level).

Some organizations also have a test policy. In that case, the organizational test strategy should align with the test policy and conversely experience from implementing the organizational test strategy may influence the test policy. Test policy is covered in Expert Level Test Management [@ISTQB:2011].

### Important DevOps Practices 

A value-driven organization that uses DevOps as an approach aims to deliver value more frequently and in small changes through all steps of a value stream. Hence, testing should be designed to foster this frequent flow of value. This has a direct impact on team organization, processes, tools and competencies - i.e., it has an impact on the organizational test strategy.

To improve a test strategy in the context of DevOps, it is important to have a picture of the current maturity state and a vision for a future state. The organization needs to select which areas to improve and gradually increase maturity.

A common visualization for DevOps is to represent the development and operations stages as one cycle in an infinite loop. The loop highlights a key DevOps goal of reducing lead time and delivering value faster. The individual stages in the loops are represented differently depending on the context. A generic version is shown in <#figure:devOpsInfiniteLoop>.

![devOpsInfiniteLoop](example-image "Generic version of the DevOps infinite loop.")

DevOps accelerates delivery of value by optimizing the loop's key elements: operation, monitoring, exploration, coding, integration and release. As DevOps maturity advances, frequent code deployments and faster lead times into staging and production environments speed up the cycle. Improved incident recovery and reduced change failure rates further enhances this process.

Many alternative representations of stages exist and are often used in specific contexts. "Plan" in agile product development refers to the continuous exploration of customer and stakeholder requirements. In ATLaS terminology, "deploy" precedes "release", and even "release" may not always mean production release. Two practical examples of a mapping between ATLaS and other representations of the DevOps stages can be found in table 4.1. The market offers different maturity models that can be adapted to organizational needs, see section 4.1.3 for details. In the SAFe framework, there are 16 so-called aspects in a DevOps maturity model, which Example 2 in Table 4.1 maps to.

| **ATLaS** | **Example 1: Deploy after release** | **Example 2: SAFe aspects** |
| --- | --- | --- |
| operate | operate | respond, stabilize |
| monitor | monitor | monitor, measure |
| explore | plan | learn, hypothesize, collaborate & research, architect, synthesize |
| code | build | develop, build |
| integrate | test, release (release to staging environments) | test end-to-end, stage |
| release | deploy (activate in production environments after release, in this case called deploy) | deploy, verify, release |

: Examples of representations of DevOps model. \label{table:DevOpsModel}

Explanations of the infinite loop can start with every stage. This chapter starts with explaining the operations aspect on the right-hand side of DevOps, as its shift right components exhibit the most substantial differences compared to approaches that do not emphasize DevOps. The chapter will not delve deeply into shift left aspects, as continuous testing is now well-known and covered in other syllabi. Note that the absence of a test section in the middle is intentional. Although testingbefore release can be important in practical scenarios, many mature software architectures and team organizations eventually eliminate the need for it.

**Operating in DevOps**

A primary objective of operations is maintaining stable production environments. Traditional development approaches often steer clear of using production environments for testing, aside from exceptions like beta testing. To create an effective organizational test strategy for DevOps, organizations must determine how to best utilize production environments without compromising stability.

Aspects relevant for the operate section of DevOps include:

* Building relationships: A central approach is to build relationships between development and operations which often would not exist in traditional development approaches. Building a communication path is not just about talking to people, although that is a good start. A path develops by gradually introducing collaborative activities.
* Testing in production: Traditionally besides beta testing, testing in production has been considered a bad practice because defects should be found as early as possible. However, DevOps offers new ways of testing in production while mitigating risks of causing down-time or degradation in the service provided. So, testing also needs to shift-right in value-driven organizations. Not all testing in production concentrates on defect detection. Users are often asked to provide direct feedback during a beta test, but they also provide feedback through their actions. Automated feedback from production environments provides valuable insights which can lead to the discovery of defects, prevention of failures, and information for future exploration beyond what users can observe. There are different techniques used to support testing in production. A/B testing is a technique that compares two different versions of an application simultaneously with different subsets of users. Canary releases allow for testing functional suitability, alarms, monitoring, analytics, events, and logging on a subset of users. Feature toggles help to establish testing and rollback opportunities for both staging and production environments by disabling features without having to make a new deployment.
* Optimizing operations for resilience: generating and using the advantages of resilient production environments. DevOps system environments are built for resilience. Chaos engineering is a technique that fosters resilience by deliberately introducing chaos into both test and production environments thus providing a learning opportunity. Other techniques for resilience are described below in section "Releasing in DevOps".

**Monitoring in DevOps**

DevOps monitoring is essential for enhancing problem-solving in production environments. Since this reduces risks, it can help to reduce efforts related to detect and resolve regressions. Monitoring also generates valuable data for understanding value created, further exploration and planning phases. Analytic tools provide feedback that can be used to inform planning and testing activities. Mean time between failures and service availability are examples for production information that is often well monitored in DevOps environments.

**Exploring in DevOps**

During exploration the product backlog for agile planning gets valuable input. An important aspect can be to integrate hypothesis-driven development. That can mean that features are refined with an additional hypothesis statement that is testable, as soon as the feature is delivered. A Minimum Viable Product (MVP) helps to gain data from operations as soon as possible. An MVP is an early and minimal version of a new product or business solution that is used to accept or reject hypotheses about the benefits of a solution. Agile test leaders need to explain that exploring customer needs through experimentation is also part of testing as a discipline.

Useful collaborative approaches used in exploration are for example acceptance test-driven development (ATDD), specification by example (SBE), behavior-driven development (BDD).

A/B testing results produced during operation can be an excellent input for exploring. Exploration can use UI-mockups, storyboards and models.

**Coding and integrating in DevOps**

The coding and integrating stages are about the core development activities like writing code, deploying in test environments and performing end-to-end tests on staging environments. How to advance built-in quality in a continuous integration pipeline is already covered in [Agile Tester/CTFL].

BDD and ATDD test cases that were collaboratively created during exploration can be established as automated tests as an integral part of the DevOps pipeline during these stages.

**Releasing in DevOps**

For releasing stage, a central element is to always improve the control and automation degree of test environments.

Technologies for managing containers and other virtualization can be used to effectively manage environments. For organizations where virtualization is a new capability the organizational test strategy should outline the first improvement goal and the initial steps to get there from a quality and testing perspective. Even without virtualization technologies, it is vital to improve the management of test and production environments. One way to do that is to utilize infrastructure as code as described in CTFL. Environment management has to prefer self-service approaches to processes that include requesting and approving changes. Differences between test environments and production environments should be minimized step by step and verifying the underlying infrastructure with automated tests can be a big help.

Blue/green deployment is another approach that improves resilience and offers exceptional rollback capabilities. This blue/green deployment strategy maintains two identical production environments, known as "blue" and "green," with one actively serving users while the other remains idle. Both chaos engineering and blue/green deployment help build more robust and reliable systems, enabling increased testing in production without compromising stability.

Enhancements in the releasing stage can directly improve the resilience of operations and thus enable frequent and early releases in the production environment.

### Create and Implement an Organizational Test Strategy {#create-and-implement-an-organizational-test-strategy}

An organizational test strategy for a value-driven organization should not be developed and implemented by testers in isolation but instead as a collaborative effort across the organization. Creating the organizational test strategy does not need to start from scratch and can begin by reusing elements of an existing test strategy and then evolve through adaptations based on experience and experimentation.

Some of the traditional test strategies are particularly relevant and inspiring in agile at scale:

* Consultative test strategy: The idea is to go out and discuss testing with different experts from the organization who would not normally be regarded as testers or join a testing CoP. Architects, business domain experts or technology experts can provide valuable input based on their unique knowledge and perspective. In addition, they also need to help build and sustain a quality mindset and culture.
* Regression-averse test strategy: Regression of existing product capabilities can be largely avoided by defining tests at an early stage to guide the design and implementation of new features and then automating the tests to run regularly within the continuous integration cycle. Automating tests for the most critical parts where feasible is a must. Otherwise, it is impossible to perform QC in the short timeframes needed to make frequent changes.
* Model-based test strategy: In Model-Based Systems Engineering (MBSE) models are used to define, design and document product characteristics. This has two advantages from a testing point of view:
  * Models allow stakeholders to explore product characteristics before the actual implementation thus enabling early validation of requirements and design decisions.
  * Once a model is declared valid, test cases can be derived in order to verify the implemented product against the model.

Creating an organizational test strategy, one can draw inspiration from the Definition of Done (DoD). The DoD is set of criteria used to determine if a product increment is releasable. The DoD can be an organizational standard in which case all agile teams must follow it as a minimum (i.e., they may choose to apply stricter criteria but must not use less rigorous criteria).

Elevating the DoD to a standard an organization defines the minimum quality level expected from all product increments before release. Accordingly, the organizational test strategy should address these quality goals and elaborate how to check their fulfillment.

Making the DoD an organizational standard can also help operationalizing the organizational test strategy: Essential elements of the organizational test strategy (the MUST-DOs expected from every team) should be put into the DoD to emphasize their binding character.

The DoD can also serve as an example of how to create a less prescriptive more useful kind of documentation:

* A Definition of Done is usually a short document with a concise list of criteria.
* An organizational test strategy is traditionally much more elaborate making it hard to find useful information between all those definitions and prescriptions.

By being inspired by DoD, it is possible to split the organizational test strategy into small documents that are easy to use. The organizational test strategy should be a "living" artefact rather than shelf ware.

Additionally, the organizational test strategy should provide guidance for teams when determining their team's Definition of Ready (DoR). Although teams may not focus on concepts like MVPs in the DoR, the organizational test strategy should offer general direction on testing topics as described in the exploration stage of the DevOps cycle. Some more team-oriented aspects of that, like using ATDD User Story workshops when decided necessary in a refinement meeting, should manifest in the DoRs of the teams.

One approach for tailoring up the content of a test strategy is by involving one or more Communities of Practice. CoPs are a great arena for discovering new improvements as they promote teamwork and discussion. Furthermore, they develop the capabilities and knowledge of individuals being active in the CoP.

A CoP can be composed based on roles or topics.

Examples of role-based CoPs could be:

* Tester, agile test leader or agile test team lead CoP
* Solution architect CoP
* Project manager CoP
* Product manager CoP
* User experience and User interface designer CoP
* Data scientist CoP
* DevOps engineer CoP

However, a role-based CoP where participants are only invited based on their role will not generate the same shared responsibility and behavior described in the organizational test strategy, as the topic-based CoP. This does not mean that role-based CoPs are not relevant and valuable. If you e.g., need to develop a template for creating manual test cases, a role-based CoP with peers would probably provide more fruitful discussions than asking the members of an architect CoP who might not have any experience with creating manual test cases.

In case an organization only has role-based CoPs then the agile test leader needs to collaborate with several CoPs to get a broader set of perspectives. Alternatively, the agile test leader could set up a small CoP or taskforce with the sole purpose of getting the organizational test strategy developed and operationalized.

Invitations to topic-based CoP should be extended to everyone interested in improving a certain area. Examples of topic-based CoPs related to QA and testing can be found in table 4.2 below. Notice how the examples of participants transcend professions and fields, allowing everybody interested in the topics to contribute.

| **Topic** | **Description** | **Examples of participants** |
| --- | --- | --- |
| Test Automation | Depending on the maturity of test automation the CoP could focus on e.g.:
* Designing and implementing automation framework
* Creating templates for scripts or documentation
* Selecting or presenting useful tools
 | Agile test leader,test engineers, developers and architects |
| Building-in quality | This CoP could focus on how to implement new techniques, tools or processes or improve existing ones, e.g.:
* Refinement of features or user stories
* TDD or BDD
* Requirements engineering
* DoD
 | Agile test leader,scrum masters, test analyst and business analysts |
| DevOps
 | Depending on the maturity of the current CI/CD the CoP could focus on establishing or improving e.g. :
* CI
* CD
* Continuous delivery
-
 | Agile test leader,test engineers, developers, operations, system delivery manager and architects |

: Examples of topic-based CoPs related to QA and testing \label{table:CoPsRelatedToQA}

The agile test leader can facilitate the evolution of the organizational test strategy by leveraging the CoPs that cover the relevant topic. The CoP should be self-lead and -managed but the agile test leader could request to lead a CoP meeting in order to gain insight. This does not mean that every improvement should be unanimously approved by the CoP as this would result in slow or no progress. The agile test leader is responsible for making potentially hard discissions in order to ensure the desired progress of the evolution of the organizational test strategy, while also fostering ownership and shared responsibility for quality in its users.

**How to involve the CoP**

Regardless of whether the CoP is based on roles or topics the possible approaches for involving them in the development and operationalization of the organizational test strategy can be similar. As described in chapter 1 quality is everyone's responsibility, and an agile test leader is a natural catalyst. Furthermore, leaders or managers with formal responsibilities in the organization are expected to ensure that CoPs have the opportunity to work effectively as intended. This may involve making necessary adjustments to the organizational setting to foster an environment where CoPs can thrive and contribute to the overall quality processes. In some environments sponsorship or steering committees can help to foster the necessary management support for CoPs. However, it does not mean that leaders and managers need to micromanage quality, quite the opposite.

**Approaches for Creating and Implementing an Organizational Test Strategy**

Examples of approaches which can be used by themselves or combined to create and implement an organizational test strategy are:

* Workshops
* Backlog and road map
* PDCA cycles

**Workshops**

Workshops can be conducted with relevant stakeholders, including testers, developers, business analysts, and other project team members. By planning the workshop, the facilitator can ensure that the attendees can contribute with knowledge and best practices for a shared organizational test strategy that is applicable to the entire company. Hence fostering a sense of commitment and responsibility.

**Backlog and Road Map**

An organization could start by determining the goals for implementing the organizational test strategy and subsequently identify backlog items. The implementation of the backlog items can then be visualized in a road map based on priority and their interdependencies. This approach provides a clear direction for the implementation of the organizational test strategy and to manage the overall progress. Furthermore, the plan can easily be communicated and followed by the people involved and relevant stakeholders.

**Plan-Do-Check-Act Cycle**

Another approach for improving the test strategy by utilizing the CoP is PDCA cycles. The agile test leader will facilitate continuous exploration and recognition of opportunities and planning continuous PDCA cycles. A small-scale trial can be conducted for a suitable project or team. Usual a team will volunteer or the agile test leader needs to persuade a team to conduct a pilot. A review and analysis of metrics used for the trial will uncover whether the change is beneficial for the organization. Based on this the organizational test strategy is revised to achieve the identified benefit.

See more about how to embed PDCA in the organization in section [Structured Problem-Solving Approach for Quality and Testing Activities](#section:structured-problem-solving-approach-for-testing-and-quality-activities).

**Approaches to Implementing an Organizational Test Strategy through**  **tailoring**

It is the responsibility of the entire organization to implement the organizational test strategy. This means that people and teams throughout the organization need to identify and plan how they contribute. How the strategy is implemented may follow a tailoring-down or a tailoring-up approach.

In tailoring-down agile teams start with a large number of suggested practices and work products and then selectively remove unnecessary elements. Traditional organizations usually apply a tailoring-down approach. Their organizational test strategy typically contains many practices and work products classified as mandatory or highly recommended. As a result, people are expected to either perform these practices and create these work products or to carefully explain why this is not necessary or helpful in their situation.

In tailoring-up agile teams start with a minimal set of mandatory elements, for example a common definition of done for all agile teams, and then selectively add optional practices and work products depending on their context and needs.

To select the appropriate tailoring approach is crucial during a transition from a traditional to a more agile and value-driven organization.

**Advantages and Disadvantages of Tailoring-up**

A tailoring-up approach results in an organizational test strategy being less prescriptive. The important cultural difference with respect to a traditional organization is that teams are not expected to explain themselves for not pulling these optional elements. Tailoring-up makes it easy for teams to establish a lightweight test strategy and experiment with it which is more adapted toan agile value-driven organization.

**Tailoring-up has some disadvantages:**

In the beginning, there might not be a lot of guidance of how agile teams need to improve quality and testing to support the business strategy.

If the organization is not able to collect input and feedback from the agile teams and create a strategic direction based on that, there might not be an organizational test strategy which addresses structural and systemic challenges.

**Advantages and Disadvantages of Tailoring-down**

On the other hand, there may also be situations where tailoring down is more appropriate. Tailoring up assumes that mature agile teams are fully committed to product quality and capable of managing product risks efficiently across entire value streams. If teams are reluctant to accept this responsibility, tailoring up can result in shallow testing because of teams limiting their test efforts to the absolute minimum. In this case tailoring down forces teams to consider practices for deeper testing and to make a conscious and justifiable choice about these practices. At the same time coaching should be applied to teach teams that minimizing their local test effort will result in disproportionate amounts of rework further down the value stream.

Tailoring-down may also be more appropriate if a comprehensive agile framework (such as SAFe®) is used to guide the transition from a traditional to an agile value-driven environment. For example, if there are teams with responsibility for dedicated test levels or dedicated tools or dedicated processes, it might be helpful to tailor-down their responsibilities step by step.

Opting for tailoring down will allow a more continuous transition but also has two significant disadvantages from the point of view of a value-driven organization:

- A lot of effort may be needed to explain why a predefined approach is not adequate instead of focusing on practices or work products that might be helpful. This justification overhead will be greatest for relatively simple value streams where a lightweight test strategy would suffice.
- There is a risk that in an attempt to have a lightweight test strategy agile teams omit essential elements of the organizational test strategy which only appear to be unnecessary from a local perspective

**Implementing the organizational test strategy**

In traditional organizations work on the organizational test strategy focuses very much on creating a defining document. Once written such documents often become shelf-ware and are either ignored by teams or treated as nonnegotiable organizational constraints. From the point of view of a value driven organization both scenarios are wasteful:

- Ignoring the organizational test strategy obviously defeats its purpose.
- Blindly following the organizational test strategy denies the organization the potential to evolve and improve the organizational test strategy based on experience and feedback from the teams.

To avoid these problems value driven organizations should take an experimental approach to implementing their organizational test strategy: Practices from the organizational test strategy should be seen as hypotheses to be validated by successful experimentation within the teams. The definition of the organizational test strategy should be user friendly in order to encourage experimentation. So rather than creating a large document full of formal definitions the focus should be on providing small, helpful assets that are easy to use such as mind maps, how-to guides, templates with examples or a technology radar for test tools.

While publishing such helpful assets is a good start, it will often not suffice to get the teams involved. So agile test leaders need to go out, present these assets and provide training and coaching to people. Above all discussions of the organizational test strategy should not be limited to stakeholders who consider themselves testers but also include other roles such as developers, architects, technology experts, business analysts, user experience (UX) experts. As people in such roles do not often show a strong interest in testing from the very beginning, active change management will be necessary to get them involved. A useful approach to that effect is the ADKAR model which summarizes the essential outcomes of successful change management:

* Awareness
* Desire
* Knowledge
* Ability
* Reinforcement

Active discussion and experimentation on the organizational test strategy beyond the testing community makes it a living strategy, that is adaptable to the changes of the value driven organization.

### Validate Alignment of Test Practices with Business and Technical Needs 

An important aspect of implementing the organizational test strategy is to be able to assess whether or not it helps the organization to deliver on the organization's business and technical strategy.

There are different assessment techniques. The assessment techniques can differ on several aspects:

* Purpose
* Who performs the assessment
* How the assessment is performed
* How frequently the assessment is repeated
* Tools available to support the process

In value-driven organizations quality and testing should be embedded in the organization and the assessment of test practices should happen in the context of development and not as a separate area. An agile test leader can help ensure that quality and testing practices are covered in assessments focusing on DevOps, team agility or organizational agility.

It is common to use a maturity model when assessing an organization's capabilities or the competencies of an organizational unit or a single team. A maturity model describes a set of criteria and levels of development in selected areas. The areas are key for achieving a goal or fulfilling a purpose, e.g.,

* A maturity model for DevOps capabilities and practices covers areas related to explore, code, integrate, release, operate, and monitor
* A maturity model for team agility covers areas like DevOps but usually not in the same level of details as other areas like planning and roadmaps, leadership, and culture is also covered
* A maturity model for organizational agility covers areas related to quality metrics, customer involvement, technical excellence

There are existing maturity models focusing on the test process. For more details regarding test process improvement models see Expert Level Improving the Testing Process [@ISTQB:2011].

An assessment, especially on an organizational level, often follows a formal process and is often performed by an external assessor. The teams or roles being assessed may get a list of improvement suggestions or actions which they should implement within a given timeline. One of the disadvantages of such an approach is that the people who should improve may not agree with the improvement suggestions and therefore not take full ownership of implementing them.

In a value-driven organization it is better to use an assessment method which has a lower risk of disempowering and disengaging the teams. It is also natural that it is the teams who define what to improve and how to improve. This kind of assessment is often conducted with the help of a facilitator and includes input from a broader group of people who can provide useful input and guidance. It is therefore recommended to use either a full self-assessment or a facilitated self-assessment. When selecting how to do assessment it is useful to consider the following aspects:

* The organizational scope of the assessment,
* The maturity of the teams and
* The culture of the organization, especially related to psychological safety

Another important aspect is what to assess. One the one hand, assessments should focus on what is important to understand a given challenge. On the other hand, it is important to take a holistic view to avoid jumping to conclusions or falling into the trap of local optimization. Typical areas are outcomes, outputs, and maturity, see section [Test and flow related metrics](#section:test-and-flow-related-metrics) for more details.

It is important that the people being assessed find the areas covered in the assessment relevant for their context. On the other hand, it can be helpful to have a common assessment if there are multiple places in the organization that want to use the assessment. Creating an assessment from a blank sheet of paper can take significant time and effort. Another approach is to start with an existing assessment and modify it where needed. Some frameworks for scaling agile offer assessments covering different aspects of the organization. There are also commercial assessment methods available. Some of them include a platform to support the entire assessment process, The disadvantage of using an existing assessment as a starting point is that it might raise resistance because all the questions were not selected by the people.

Due to the different aspects to consider, there is no universal process or method for conducting an assessment. The following describes typical steps in a facilitated self-assessment when it is conducted the first time. The example is using a questionnaire as a basis for gathering input. Some steps might be omitted when the assessment is repeated at a later point in time.

Planning self-assessment

* Engage teams who want to do a self-assessment.
* Engage leaders of the teams who should provide input and participate in concluding the assessment.
* Decide what to assess and design questionnaire.
* Prepare teams, facilitators and tool for self-assessment.
* Schedule self-assessments

Conducting self-assessment

* Distribute questionnaire to people outside the team to collect input
* Fill out the questionnaire together in the team or distribute in advance
* Analyze the input in the team regarding alignment of test practices with business and technical needs
* Discuss and decide which areas to improve in the team
* Define improvement actions for the team and add to team backlog
* Define improvement actions for organizational leaders and add to organizational backlog

Concluding self-assessment

* Decide in the team how much is shared with people outside the team
* Go through the conclusions with relevant stakeholders and team leaders and/or people leaders
* Gather insights across teams and discuss with organizational leaders
* Agree when to conduct the next self-assessment to analyze trends in the different areas

Conducting assessments provides value if it helps teams understand and evaluate their ways of working, the outputs they produce and the outcomes they achieve. Powerful assessments result in the teams taking action to close gaps between test practices and the business and technical needs. The facilitator's role is to help the team get the most benefit from doing self-assessments.

## Fit Agile Test Leadership in a Value-Driven Organization

### Organizational, Product and Operational Level

Agile test leadership can support organizations using an agile scaling framework on different levels.

![agileAtScale](example-image "Link between level in organization and Agile at Scale.")

**Organizational Level**

Agile test leadership is needed on a strategic level to ensure that the organization continuously develops the quality and testing capabilities needed to deliver quality products and services. The quality and testing capabilities are typically described in the organizational test strategy, which must be aligned with and support the business strategy. Regardless of the framework used for scaling, leading the effort to create and evolve an organizational test strategy is one area where test leadership is needed. See section 4.1.2 (#section:create-and-implement-an-organizational-test-strategy) for more information on how to create and implement an organizational test strategy.

Evaluating the current quality and testing capabilities on an organizational level is another area where an agile test leader can contribute. The agile test leader can question ineffective or inefficient practices and facilitate a possible adjustment of the organizational test strategy. In SAFe® for example, the agile test leader could help define and take ownership of portfolio epics if a larger, coordinated effort is needed to improve an existing capability or build a new one. An example is the capability to anonymize production data before it is used as test data. This could be a larger initiative which would require significant funding and not something an agile team or even a team of teams would have the means to do. Similarly, in LeSS managers provide an improvement service to the teams. The managers could help build an improvement backlog based on the needs of the teams ([https://less.works/less/management/improvement-service](https://less.works/less/management/improvement-service)).

Agile test leaders can also help justify investments in quality and testing improvements. This requires close collaboration with and coaching of business stakeholders when initiatives are shaped. In SAFe®, this would happen when epics are reviewed and analyzed and could be captured in a lean business case (https://www.scaledagileframework.com/epic/). Equally important is to define leading indicators that will help determine if the improvements are happening.

Another important aspect on organizational level to which an agile test leader may contribute is the budgeting process. An agile test leader can help analyze trade-offs related to quality and testing. To be effective, the agile test leader needs to participate in parts of the organizational budgeting process. In a traditional budgeting process a budget is created based on input from the leaders of the organizational departments once a year and adjusted after the first 6 months. In a value-driven organization, the budgeting process may include a broader set of participants so more aspects are considered when allocating budgets. One version of this is what SAFe® calls participatory budgeting (https://www.scaledagileframework.com/lean-budgets/).

**Product Level**

On the product level teams of agile teams need to reach a shared understanding of how to establish the right quality at the right time to improve the overall effectiveness and efficiency of their value streams.

Agile test leaders can support this mission in different ways:

* Be a practice leader (lean thinking manager teacher) within the testing community of practice (CoP) as described in section 4.1.2 Create and Implement an Organizational Test Strategy.
* Help teams to identify waste using value stream mapping (VSM).
* Guide teams to capture product quality aspects in their Definition of Ready (DoR) and Definition of Done (DoD).
* Teach teams systems thinking to reduce the risk of local optimization (i.e., changes that will improve testing but result in a decrease of the total value delivery).
* Facilitate multi-team retrospectives and process improvement.
* Help teams with continuous improvement of their quality capabilities applying skills from quality assistance like quality coaching, conduct training, facilitation skill.

In some organizations an agile test leader provides system QA and testing expertise to agile teams by leading or supporting a specialized service group (e.g., Shared Services or System Team in SAFe or Undone Department in LeSS). The role of such supportive teams is characterized in "team topologies" [@scaledAgile-organizing:2023], which distinguishes "complicated subsystem teams", "platform teams" and "enabling teams". Such a specialized team could provide test related services including: (https://www.scaledagileframework.com/system-team/)

* Redesign/Refactoring of a test automation framework
* Integration of automated tests into the continuous delivery pipeline
* Management of test infrastructure (e.g., test environments, test data) and test tools
* End-to-end testing
* Non-functional testing

Help to find the optimum balance between decentralized testing done by agile teams and centralized testing done by the system team (SAFe) or the Undone Department (LeSS). For example, to help avoid bottlenecks when only the system team has important competencies (like performance efficiency testing or test automation) that other teams depend on when releasing a value.

**Operational Level**

On the operational level an agile test leader can be a coach or mentor to teams of agile teams (called ARTs in SAFe or areas in LeSS Huge) and offer guidance on test related subjects such as:

* Test techniques
* Testing quadrants
* Test tools
* Use of metrics
* Test effort estimation
* Risk-based testing
* Pairing and peer reviews
* Test-first approaches
* Design for testability

Details on these subjects can be found in: ISTQB CTFL, ISTQB Agile Tester and ISTQB CTAL TM.

### Transition from Traditional Test Management to Agile Test Leadership at Scale

For a traditional test manager the agile transformation involves a shift of responsibilities away from management towards leadership. This means that a traditional test manager has to adopt some new responsibilities as an agile test leader and lay down some of their old responsibilities as a test manager. But there is also continuity as some of the traditional test manager responsibilities remain valid for agile test leaders.

New responsibilities

Moving from test manager to agile test leader, people must engage across the organization in order to foster a quality mindset and culture which supports business agility. To achieve this, they typically need to:

* Influence strategic decisions to help shaping the organization's testing capabilities and skills to support business agility
* Use value stream mapping and systems thinking
* Involve various disciplines along the entire value stream
* Speak up in case of dysfunctions

Compared to traditional test managers, agile test leaders must focus more on the organizational level where they need to influence strategic decisions such as:

* Which testing capabilities and skills are needed to support business agility?
* How to establish and sustain these capabilities and how to allocate budgets for funding them?
* Which testing practices should be consolidated or centralized in order to create synergies between teams and reusable assets?

Anti-patterns

Moving from test manager to agile test leader, people should be careful to avoid "command and control" type management behavior, which would undermine the idea of self-organized and responsible agile teams. Therefore, agile test leaders should no longer perform traditional test management activities such as

* Test effort estimation
* Scheduling tests
* Assignment of testing tasks
* Monitoring test progress
* Taking corrective action to compensate for delays
* Reporting the test status to stakeholders

These activities become a team responsibility, so rather than performing these tasks for agile teams, agile test leaders should guide and coach the teams to perform the tasks.

The same is also relevant for creating and implementing an organizational test strategy. The agile test leader has to balance between self-management and a centralized guidance from and alignment within the organization. Again, "command and control" behavior would be counterproductive here so the agile test leader should avoid the following anti-patterns:

* "Standardize everything" i.e., squeeze all testing into a formalized process with mandatory roles, activities, artifacts and tools.
* "Be the testing police" i.e., rigorously enforce the organizational test strategy without empathy for the situation or context of people. "If you don't follow the rules, you're doing it wrong."

Rather than imposing constraints on agile teams it is often more effective to respond to challenges they are facing and offer helpful advice.

Continuing responsibilities

Fortunately, the traditional test manager role is not all about "command and control". In fact, test managers focusing more on participatory management are often more successful in the long run. Therefore, many responsibilities of traditional test managers remain relevant for agile test leaders.

Agile test leaders can empower testers by

* Coaching testers
* Fostering testing CoPs
* Showing career paths
* Offering training
* Suggesting test process improvements

Agile test leaders can be an escalation point for issues like

* Test automation framework needs to be revised
* Unstable test environment
* Insufficient review of test cases
* Principle "Quality is everyone's responsibility" is not yet internalized

Agile test leaders can provide guidance regarding

* Organizational test strategy
* Test plan
* Test techniques
* Test automation
* Test tools
* Quality metrics and reporting
* Test effort estimation
* Risk-based testing

Agile test leaders can represent testing within the organization by:

* Demonstrating the business value of testing
* Establishing an overview of capability and maturity levels in testing
* Supporting the building of testing capacity within the organization
* Estimating the necessary budget for testing services