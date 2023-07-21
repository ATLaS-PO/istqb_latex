## Test Processes

### Testing challenges in scaled agile product development

The test process as defined by the Foundation Level syllabus [@ISTQB:2023] generally applies to all kinds of organizations, products and development frameworks. However, scaling agile development beyond the level of a single team, introduces new challenges for the implementation of the test process that do not exist in product development with one agile team or non-agile product development:

**Cross-Team-Testing**

With large products requiring the combined development effort of several teams, locally testing the output of individual teams will not result in a done integrated solution. The traditional strategy for end-to-end integration is to conduct centralized tests in a separate stage before releasing the product. Such an end-to end test level run by a specialized team often turns into a major bottleneck for value chains. In an attempt to enhance flow some organizations simply discard dedicated end-to-end testing, hoping that agile teams will figure out how to integrate and test the full solution without guidance. The risk with this approach is that responsibility for performing cross-team testing becomes ambiguous and that the full solution is insufficiently tested. See section 5.1.2 below for more information.

**Business Hypotheses Testing**

One important idea of agile testing is to test if there is a shared understanding of a business problem. Due to the size and complexity of IT systems it can take significant time and effort to implement a technical solution to explore a business need and determine if it solves the right problem. Implementing a solution only to learn that it solves the wrong problem becomes a serious risk. Therefore, formulating and testing business hypotheses needs methods which require less investment. Typical methods are market research, customer feedback using light-weight techniques like mock-ups, prototypes, and pilots.
It is often a significant mindset change for organizations to involve testers in early product development when forming business hypotheses and exploring business needs. To help product owners build a good backlog, testers need to shift their focus from testing implemented features towards testing business hypotheses. Professional testers are qualified for this task by a number of relevant skills including solid knowledge of the business domain empathy with the concerns of users and design techniques for robust and conclusive experiments.

**Need for Specialized Test Teams**

Ideally agile teams should perform all tests necessary to ensure their collective output results in a releasable integrated solution. Consequently, agile teams should also make these tests part of their Definition of Done (DoD). Work that is necessary for a releasable integrated product but not covered by the DoDs of agile teams is known as undone work and can be interpreted as a shortfall of the DoDs [@less:2021]. So, value-driven organizations should generally prefer making tests the responsibility of agile teams.
Nevertheless, in some cases it can be more practical to have specialized teams for certain testefforts:

* Testing nonfunctional quality criteria such as security or performance efficiency.
* Handling complex staging environments for system integration testing.
* Establishing and maintaining a test automation framework.

Possible setups for such specialized service teams will be further discussed in (#section:test-activities-performed-by-stream-aligned-teams-and-specialized-teams) in the form of team topologies..The overall challenge for agile test leaders is to identify, foster, facilitate and coordinate test activities between teams of different topologies. Finding a good team setup supporting the value chains of a business agile organization often requires an iterative and experimental approach supported by change leadership and systems thinking

**Establish transparency for stakeholders with respect to flow, quality and value-delivery**

To make informed decisions, stakeholders in a value-driven organization need to have insight into the flow of value chains, product quality, and the delivery of business value. A comprehensive assessment of these aspects requires input from multiple teams and an alignment of metrics between teams. Metrics are further discussed in {#section:#test-and-flow-related-metrics}.

**Fitting test activities into iterations**

Tests not performed within iterations, are usually postponed which can result in a significant backlog of undone tests threatening planned releases of the solution. Slicing independent user stories that are testable within an iteration can be demanding depending on technology and automation capabilities. To facilitate testing within time-boxed iterations, improvements may be needed regarding tooling, processes, infrastructure etc. See section 5.1.4 for more information.

**Coordinate and synchronize test efforts across agile and non-agile teams**

Delivering business value with a done integrated solution requires tests to be conducted by teams of agile teams and sometimes non-agile teams. Coordinating these test efforts can be challenging due to differences in goals, priorities, working periods, release cycles, lead times etc. See (#section:coordinate-testing-efforts-across-agile-and-non-agile-teams) for details.

### Coordinate testing efforts across agile and non-agile teams {#coordinate-testing-efforts-across-agile-and-non-agile-teams}

It is important to incorporate QA and testing in the normal agile processes. If QA and testing are handled as separate activities, it is harder to get a shared understanding and responsibility for them, to identify and minimize dependencies between teams and to assign tasks to teams.

Coordination of tests between teams can be challenging, particularly if some teams are non-agile, in agile transition or from a third party. In these cases, it is important to understand the non-agile or external party's ways of working and find an agreement for collaboration and coordination that suits both parties.

The following proven agile practices are examples how to coordinate testing across agile and non-agile teams.

**One Backlog / Cross-Team Refinement**

Everyone needs the same view on how the backlog is ordered. Cross-team refinement is a way to decompose the backlog identifying and reducing cross-team dependencies. Testing across teams is a typical challenge to be discussed in this context. The expected outcome is that high priority backlog items become actionable work for agile teams. Cross-team refinement also helps to forecast which teams will collaborate to implement and test which features in the coming period.

**Planning Interval (PI) Planning / Big room planning**

Release planning in scaled agile usually differs significantly from one-team approaches (see for example Foundation Level syllabus). Big Room Planning is a face-to-face event, where agile teams figure out, how to decompose work (including testing) and handle dependencies. When dependencies are visualized the teams can discuss how to conduct testing spanning multiple teams. The expected outcome is for the teams to commit to a shared goal for the next period. Non-agile teams can be involved in quarterly planning.

**Scrum of Scrums (SoS)**

The Scrum of Scrums is a virtual team composed of delegates from agile teams. Focus is on which tasks are likely to be picked up by which team, how to handle dependencies between teams and how to ensure each sprint results in a done integrated product increment. The SoS event helps to handle impediments related to testing, impacts of delays, changes in scope and testing related product and project risks.

If non-agile teams do not participate in regular SoS events, a delegate from the SoS could participate in relevant status meetings of non-agile teams as an alternative.

**Demo of integrated and tested product increments**

With every review a done integrated and tested product increment is demoed. The purpose is to elicit stakeholder feedback on the quality and business value delivered by the new increment. Failures happening during the demo should trigger a discussion, how to improve the coordination of quality and testing activities between teams.

**Retrospective / Inspect & Adapt**

If issues and opportunities related to QA and testing impact multiple teams, they should normally be addressed within a multi-team retrospective. In some situations (e.g., if non-agile teams need to be involved), it may be necessary to organize a separate retrospective.

**Impediment boards and risk boards**

Visualizing impediments and risks on a board is a good way to raise problems and to get the attention and help of others. Making problems visible across the boundaries of agile teams, enables the teams to work out solutions in a collective effort which will not only increase the chances of solving the problem but also create synergies because other teams can often reuse the solution when faced with a similar situation.

**Debt handling / Technical enablers**

Other efforts that often benefit from coordination between teams include the reduction of technical debt and the implementation of enablers. Technical debt is a metaphor for the additional rework effort caused by choosing easy but limited solutions and not getting enough time and resources in maintaining adaptability and quality. Such "quick and dirty" solutions may work in the short term but are often not sustainable and tend to decrease the velocity of agile teams until refactoring work is done to create a sustainable solution. Examples of technical debt include poor architecture and inefficient code. Test related issues can also be considered technical debt, e.g., insufficient test automation or unstable test environments.

Visualizing technical debt across teams with impediment boards or risk boards creates awareness and helps to identify situations where several teams are accumulating similar debts. Those situations offer a great potential for synergies if the teams reduce technical debts in a joint effort.

Managing technical debt is one of the important components of technology strategy in value-driven organization [@highsmith:2019]. The work necessary to reduce technical debt and to support an efficient and sustainable delivery of business value needs to be visible in order to get budgeted, prioritized, planned and done. This transparency is especially important for improvements requiring initiatives on a larger scale like refactoring a test automation framework or establishing test environments as a service. SAFe uses the term enabler for work products that do not deliver business requirements directly but support the efficient and sustainable delivery of future business requirements [@scaledAgile-thinking:2021]. Just like any other value-adding activity enablers are managed using agile artifacts like backlogs or Kanban boards.

### Test and flow related metrics {#test-and-flow-related-metrics}
Although teams in a value stream are working as autonomously as possible, they still deliver value together. To understand how the organization performs as a whole each team needs to contribute data and information to create a bigger picture. It is necessary to have a minimum set of common metrics that are collected on a regular basis and that can provide both a snapshot of the situation and trends over time.

Typically, traditional testing metrics focus on coverage, product quality and the effectiveness of testing, see ISTQB CTAL TM for metrics used to measure progress of testing and ISTQB CTEL TM for metrics measuring product quality and effectiveness of testing.

Organizations using a traditional project management model have a tendency to measure on completed activities and outputs. The following metrics are examples of metrics which fit with a traditional project management model:

| **Aspect** | **Metrics** |
| --- | --- |
| Activities
 | Specifications reviewedTest cases createdTest runs completed |
| Outputs | Defined test casesDefect reportsRisk assessments |

: Examples of metrics which fit with a traditional project management model. \label{table:projectManagementModel}

As covered in chapter 2, it is important that an agile test leader and an agile test team leader help to optimize the flow of value to customers throughout the entire value stream. To do that, an agile test leader and an agile test team leader should support and use a broader set of metrics covering the following three aspects:

* Outcomes in terms of business value
* Outputs in terms of delivery and performance
* Maturity in terms of people and processes

The following image shows where different types of metrics can be measured:

![metricsOnValueStream](example-image "Metrics on value stream")

To get a better understanding of quality issues an agile test leader and agile test team leader can foster additional testing metrics. Here are examples of metrics covering the three aspects:

| **Aspect** | **Metrics** |
| --- | --- |
| Outcomes in terms of business value
 | Lead time for customer value, revenue, market share, cost savings, reduced risk, customer satisfaction, delivery time |
| Outputs in terms of delivery and performance | Deployment frequency Lead time for changes Change failure rate Time to restore a service |
| Maturity in terms of people and processes | Adoption rate of agile processesTeam happinessDegree of self-organization |

: Examples of metrics covering the three aspects described in this learning objective. \label{table:learningObjective}

The Agile test leader must understand the difference between customer value and value for the organization. Value from the organization's perspective can be both top-line, such as revenue and market share, and bottom-line, such as cost savings, e.g., reducing the number of calls to the customer service desk, and profit. An increase in value for the organization does not necessarily result in an increase in customer value. Likewise, to increase customer value an organization might have to incur more costs and thereby have an immediate decrease in value for the organization. However long term an increase in customer value should result in either retained or increased value for the organization over time.

Maturity metrics show how the organization is performing in terms of process, culture and leadership. These aspects do not directly indicate how well the products or services deliver value. In other words, these metrics cannot be used as measures of overall success. If an organization is struggling with maturity, this may explain challenges in outputs and/or outcomes.

When selecting metrics to measure, it is important to use a mix of leading and lagging indicators. Leading indicators allow to predict results before they are fully accomplished. Lagging indicators can confirm the expected results after they have been accomplished. Despite their obvious advantage of providing an early indication, leading indicators are more dependent on assumptions. They may also tend to overemphasize short-term effects over long-term outcomes. An example set of leading indicators designed to drive long-term outcomes are the DORA metrics as propagated in [https://cloud.google.com/blog/products/devops-sre/using-the-four-keys-to-measure-your-devops-performance](https://cloud.google.com/blog/products/devops-sre/using-the-four-keys-to-measure-your-devops-performance). (Deployment frequency, Lead time for changes, Change failure rate, Time to restore a service). The general advise is, to treat early indicators as hypothesis and continuously monitor and revise which metrics are used and how the information is interpreted. For the revision a proper set of outcome metrics and maturity assessments as exemplified above can help.

### Structure challenging test activities and test processes 

One of the challenges in business agility is to organize test activities and test processes so they fit into these frameworks and disciplines. A recommendation from ISTQB Agile Tester is to treat test levels as concurrent test activities rather than sequential phases. While generally helpful this advice does not address all the challenges of structuring test activities in a scaled agile context.

Quality assistance is an essential factor in mastering these challenges because it facilitates a culture of continuous learning and helps to spread both testing and technological knowledge between teams. Quality assistance also helps to establish and, if necessary, revise the split of responsibilities between teams. One example would be a scenario where agile teams are supposed to develop for a range of hardware platforms without having the resources or expertise to address all platforms.

**Structuring test activities**

Component testing should naturally be done within each iteration by the individual teams. Other test activities can be difficult to fit into iterations because establishing the infrastructure (e.g., test tools, test data, test environments) takes more time and a coordinated effort.

Such test activities can be clustered based on their purpose:

* Testing functional integration is traditionally done rather late in the software development lifecycle within test levels such as system testing, system integration testing and acceptance testing. Here the end-to-end functionality of use cases or business processes is tested from the perspective of a business user. A prerequisite for these tests to proceed swiftly is that the successful communication of systems or subsystems across various interfaces has been verified from a technical point of view (see testing technical integration).
* Testing technical integration is based on architecture design and interface specifications. Here testers and test leaders have to find ways to accompany emerging technologies like asynchronous architectures (often called microservices). Ideally, if microservices were very well encapsulated, such architectures would allow agile teams to successfully perform technical integration testing using a big bang approach. The idea is that minimal coupling between microservices would effectively eliminate the need for troubleshooting across teams in order to isolate defects. In practice, since ideal encapsulation is hard to achieve, technical integration testing typically involves quite a bit of troubleshooting which can be harder with asynchronous architectures since asynchronous behavior is usually more difficult to debug [Link Fowler: [https://martinfowler.com/articles/microservice-testing](https://martinfowler.com/articles/microservice-testing)].
* Testing non-functional quality characteristics such as performance efficiency, reliability, security and accessibility. In scaled agile non-functional testing can undergo significant changes. Investments in testability may require more centralized support for a transient period, where a new toolset is ramped up, while responsibility for certain non-functional tests still rests with dedicated teams. As maturity grows and teams learn to better handle non-functional quality risks, central support can possibly be reduced to tool support and a self-service platform.

Some of these test activities may be performed more conveniently outside iterations but it is important to maintain ownership and responsibility for testing within the agile teams. Also, teams should prefer testing within iterations (both individually and across teams) since deferring tests to a separate timebox would weaken their definition of done. This will be further discussed in section 5.1.5.

Test automation can help teams perform some of the above-mentioned activities within a sprint. Therefore, it is important to include test automation activities in the teams and across teams. Advantages of test automation include:

* Higher stability of test environments
* Reduction in the time spent running regression tests

See ISTQB Test Automation Engineer for more details on test automation.

Often test process improvements will depend on investments for infrastructure and tooling. The need for or the potential of new tooling can be identified by agile teams or by other parts of the value-driven organization. In both cases a quality assistance approach helps to establish structures and a culture that enable organizational solutions. Some agile scaling frameworks warn that central tooling decisions can inhibit flow, while other frameworks emphasize that common tooling is a success factor for scaled agility. A quality assistance approach has to consider both aspects. Identifying waste holistically in the value stream is crucial to overcome local optimizations that may for example simply try to reduce license costs, see chapter 2 for more details on Value Stream Mapping.

**Handling deployment and release cycles**

If deployments and releases are not synchronized between agile teams it can result in an excessive number of configurations that need to be tested. One way of addressing this problem is to have teams work at the same rhythm and align their plans of what to implement and what to collaboratively test in each iteration. Still, there isa risk that delays in one team derails the aligned plan because the collective output of all teams cannot be tested as intended. In order to plan testing across teams in a more robust way it is desirable to reduce dependencies between teams. Options to reduce dependencies include:

* Refine the backlog into small and independent items
* Design architecture and infrastructure to support independent test and release of system components by:
  * upward-/downward-compatible system-components (no version toggle required),
  * system components with version-toggles,
  * enabling and disabling of features (Introducing "feature toggles" for enabling and disabling features is not just a development task; it also adds complexity to test automation.),
  * both roll-forward and roll-backward procedures (When DevOps environments are designed for resilience, testing roll-forward and roll-backward procedures before they are actually needed is a testing task.),
  * highly flexible, configurable, and automated test environments (e.g., by some container technology)

Ideally a business agile organization should be able to release on demand at any time with any team involved. A down-to-earth approach to this ideal requires many small steps such as delivering with more built-in quality, integrating earlier or advancing technology that has less dependencies throughout the whole value stream. Quality assistance is needed to facilitate all of these steps.

**Managing organizational risk**

Risks involved in planning and coordinating tests spanning multiple teams should not be seen as an isolated challenge specific to testing. Rather than inventing test-specific approaches to manage organizational risks, standard agile processes can be applied. Putting organizational risks on a risk board shared throughout the value stream creates visibility and agile practices like big room planning, synchronization meetings and reviews can be used to manage organizational risk.

Some test impediments cannot be easily assigned to individual agile teams. Just like organizational risks, such impediments should also be visible on a prioritized backlog and addressed by agile teams or other support structures.

**Establishing working agreements with non-agile units**

Even in value-driven organizations there may be non-agile or less agile units such as

* corporate IT,
* requirement engineering department,
* utsourcing partners,
* non-agile business areas,
* suppliers and vendors.

Therefore, a successful collaboration will require establishing certain working agreements across all teams:

* establish a minimum shared set of test-related activities(e.g., defect management, risk management (e.g., risk board) and impediment handling (e.g., impediment backlog))
* agree to a minimum set of interfaces with respect to processes, communication and tools
* encourage non-agile teams to participate in topic-based Communities of Practice
* align deployment and release cycles, but also reduce the number of touch points

There are different approaches to achieve alignment with non-agile units:

If for example the collaboration with non-agile units is generally trusting and successful, agile teams may just need an occasional reminder to put more focus on system testing before a major release since the non-agile teams will rely much more on system testing.

Alignment with external vendors, suppliers or partners may be particularly challenging as their organization might have a completely different development methodology to ensuring quality at scale. When acquiring new external vendors, suppliers or partners Agile test leaders can therefore participate in the tender process and help write parts of the request for proposal related to quality and testing. It is important to cover both quality requirements of the solution and an agile approach to collaboration that fits with the organization. Quality can also be included and weighted heavier in the criteria used for evaluating the proposals and hence help attract the vendors, suppliers or partners that fit the organization.

Furthermore, it is key to ensure that the process for collaboration is clear in the tender material and that it supports frequent alignment and coordination. Key capabilities which the vendor, supplier or partner should possess, such as collaborative requirement specification and test automation, should also be clearly specified. The metrics outlined in section 5.2 are also key to ensure transparency across organizations.

For existing vendors, suppliers, or partners, it may be necessary to change the ways of working or even consider alternative vendors if there is evidence of failure to integrate them into the agile processes at scale, resulting in quality and delivery problems. It may require a strategic initiative to modify contracts or even to choose other vendors, suppliers or partners. First step could hence be to collaborate with procurement to see what is feasible both short term and long term.

Lastly, the request for proposal process itself can be geared towards a more agile approach which allows the organization, requesting the proposal, to gather input for the request and ensure alignment with the proposing vendors, suppliers or partners. However, changing the process for requesting proposals is not always possible and will depend largely on the country and organization you are in and collaboration with procurement is therefore advised.

### Test activities performed by stream-aligned teams and specialized teams {#test-activities-performed-by-stream-aligned-teams-and-specialized-teams}

It is ideal to organize agile teams to align with a value stream that focuses on how to maximize the flow of business value. However, handling all the technological and organizational complexity within a single stream-aligned team can be hard to achieve. These challenges may be addressed by having some of the activities being performed by specialized teams. These specialized teams do not cover end-to-end, full value delivery like stream-aligned teams often do. Specialized teams may look and act differently. Some could be organized as platform teams, enabling teams and complicated-subsystem teams.

The following figure shows team topologies and their key behaviors in organizations undergoing agile transformation.

![differentTypesOfTeams](example-image "Example of different types of teams in an organization.")

The following table shows the advantages, disadvantages, and typical behavior for the four types of teams:

| **Type** | **Typical Behavior** | **Advantages**
 | **Disadvantages/Risks**
 |
| --- | --- | --- | --- |
| Stream-aligned | Building-in quality Business-facing testing | Strong focus on business value and flow
 | Handling everything (software, hardware, technology and business domain) within one team can be too complex
 |
| --- | --- | --- | --- |
| Platform | Make maintaining easier for everybody Build platforms the testers and developers like to use
 | Unification of development and test tools and frameworks

Unification of common components used (e.g., gateways, integration interactions, pipelines) Reducing the cost of testing

Provide services to reduce the number of things a stream aligned team needs to care for
 | It takes a long time to develop and implement a platform solution at the organization level

High cost of support and development of platform solutions

Usually a tool-centered approach. Stream aligned teams need to understand the tools and accept them as being useful.
 |
| Complicated-subsystem
 | Cooperate with stream aligned teams

Operate interfaces
 | Technical challenges are well addressed by a dedicated team

Complexity of subsystem is encapsulated behind an interface

Reduce complexity for stream aligned teams
 | Lack of understanding of the overall product or business domain

Integration risk between subsystems

The complicated subsystem team can be a bottle neck for flow
 |
| Enabling | Incent innovation

Provide possibility's for learning
 | Empowerment: Responsibility for and ownership of testing stays with stream aligned teams

Enabling teams can facilitate improvements that stream aligned teams would not find on their own
 | Empowerment takes more time than using specialized testing services

Recruiting and maintaining such a team for temporary needs and tasks can be expensive

Can make sense in agile software development as long term solution, if they help stream aligned teams to concentrate on their domain.
 |

: Advantages and disadvantages of typical teams behavior. \label{table:advantagesAndDisadvantages}

Each type of team is suited for specific types of testing activities, depending on the context of the organization.

Test activities which are typically performed by a **stream-aligned team** are:

* Traditional testing activities related to feature development

  * Component testing
  * System testing and system-integration testing (SIT)
  * Feature testing (business logic and etc.)
  * User acceptance testing (UAT)
  * Non-functional testing (if the team has enough time and competence)

* Hypothesis testing

  * To test a version of the application with new features on a limited number of users, and based on positive feedback, expand the release to a larger number of users

* Testing activities due to technological changes or general organizational risks
  * Closing security risks. E.g., when vulnerabilities are found in the components used and it is necessary to immediately test and release a version with a fix
  * Closing of technical debt. E.g., non-functional testing during migration from one type of database to another (or operation system)

**A platform team** helps stream-aligned teams with test activities:

* Provide services and solutions to reduce the number of things a streamlined team needs to worry about
  * The platform team provides a ready and tested solution at the organization level for logging, auditing, monitoring, authentication and authorization. Streamlined teams can adopt such solutions for themselves without wasting time on development and testing, allowing them to focus on their core business.

  * The platform team can provide a test automation platform, which offers benefits such as increased usability for testers and developers, ongoing support and maintenance. In the ideal case platforms should be provided as self-service solutions. It should be avoided, to foster central platforms by simply making them mandatory. Rather they should thrive due to their helpfulness and because agile teams want to use them. Platform teams providing the means are a better concept as a long-term solution than complicated subsystem teams doing the work, since they can help stream aligned teams to concentrate on their domain and still have full responsibility.
* Testing infrastructure that affect many teams at once
  * Improve test automation platform, run a staging environment
* Shared test tools
  * A common load testing tool provided at the organization level and taking into account the technical stack of stream aligned teams
  * A unified portal for working with test environments, which allows teams to monitor the availability of test environments, create incidents, plan work and inform about outages. Workability, support is provided by the platform team
* Shared common components for testing purposes
  * Adapters, Gateways, integration interactions which are provided and tested by the platform team and can easily be implemented by stream-aligned teams

Test activities that might be performed by a **complicated-subsystem team** are:

* Provide special types of testing that are too complicated for a stream-aligned team or platform team to handle.
  * Security testing
  * Performance testing
  * Running system integration testing that cannot currently be dealt with in stream aligned teams
* Provide testing of special sub-systems which are too complicated to be dealt with by a stream-aligned team or platform team.
  * Artificial Intelligence solution
  * Face recognizing solution
  * Run complex hardware setups
  * Market risks, complex business logic

Test activities which are typically performed by an **enabling team** :

* Temporarily foster testing activities which require specialized knowledge and skills which other teams do not have or have not yet fully mastered
  * Introduce a new technology. E.g., help stream-aligned teams when organization switches from an existing technology to a new technology stack or to a new architecture (monolith to microservices). For example, when stream aligned teams switch from monolith to microservice architecture, test approaches change not only from an organizational point of view, but also from a technical one
* Research and experiment with new methods and tools for improving testing
  * Assistance in moving to unified test tools like new tools for generating test data, a new defect management tool
  * The enabling team conducted research work on the use of existing tools for creating test stubs and provided the results for the platform team. Based on this data, the platform team will decide develop its own tool within the organization for all stream-aligned teams
  * Help teams with assessing or self-assessing testing maturity

Depending on the organizational structure, the complexity of the solutions, knowledge and skills of the teams, risks and general activities at the corporate level using one or a combination of the team types may be preferred.

Non-functional testing is often more difficult to deal with than functional testing in a value-driven environment. Having a platform team that can test quality characteristics as a self-service may be a solution. Alternatively, the platform team could focus on the non-functional testing which covers the solution as a whole while the other types of teams cover their part of the solution.

An enabling team is also useful for helping the other types of teams build the knowledge and skills required to perform the relevant non-functional testing. Enabling teams complements communities of practice as a way to ensure knowledge transfer.

Another way would be to build a platform by stream aligned teams working together, without any separate team. For example, to proceed complex type of non-functional testing (load testing during integration, penetration testing, fuzz testing) together. In this case a CoP as outlined in chapter 4 can be very helpful.

Below are examples of how teams can help with non-functional testing in the organization:

* The platform team maintains a common test environment for conducting complex types of testing. For example, load testing during integration. In which dozens of teams can participate
* The enabling team creates a common testing methodology or standard at the organization level that teams can use if they need to conduct non-functional types of testing
* The platform and enabling team are working to reduce the cost of conducting chaos engineering:
  * how often should such testing be carried out
  * solve technical issues that may block such testing (access, role model, security issues, common tools)
  * Provide a unified tool for launching, conducting and generating reports for chaos engineering

In value-driven organizations, testers are often part of the agile teams and not necessarily organized in a separate test department or test function. However, having all test activities decentralized in stream-aligned teams is not always optimal nor feasible in large organizations due to complexity.

It is important for an agile test leader to remember that the more the testers and activities that are added at the corporate level, the more the complexity of relationships in the organization grows at an exponential rate.
Practices from systems thinking are used for analysing test activities in the organization e.g., positive reinforcing feedback and causal loops [@senge:1990]. For more information, see Chapter 3.

In value-driven context where we use different types of team's agile test leaders can use a platform team to have the benefits of centralization while ensuring the team provides a service to the other teams.

Teams can conduct traditional types of functional and even non-functional testing on their own.

For example, teams that develop a product using a microservice approach can conduct load testing on their own. A member of the team with competencies and the role of load testing could be a developer or tester, or they could work on such activities together.

But to conduct complex types of testing (e.g.,load testing during integration, chaos engineering, penetration testing) it is better to involve platform and enabling teams.

Another aspect to consider when organizing testing activities is the independence of testing. In value-driven organizations the independence of testing is not necessarily secured by formal organizational boundaries. Instead, agile test leaders promote an independent testing mindset. This requires a decent level of psychological safety regardless of team type. The agile test leader should recognize typical factors that support such a psychological safe environment.

The organization of testing also depends on how the solutions are built and maintained. It may not be possible to establish stream-aligned teams consisting of people from the customer organization and the supplier organization. In those situations, platform teams, complicated-subsystem teams and enabling teams may become more relevant. The supplier of the system may be seen as a platform team from the customer perspective and the team performing acceptance testing may resemble a complicated-subsystem team.

Involving non-agile functions in testing can also be a challenge. One way is to organize them as enabling teams which provide knowledge and skills to the other types of teams. Another way is to organize them as platform teams. Both ways carry a risk of separating stream-aligned and complicated-subsystem teams from the sources of important knowledge and resulting in more handovers. For organizations that employ release planning meetings, a frequent suggestion is to include non-agile functions in these meetings to expose and clarify interdependencies to everyone.

In certain situations, it may be necessary to involve non-agile functions, such as sales and marketing departments, in testing activities. However, this can introduce challenges related to different working approaches and knowledge transfer.

For example, the team that develops the product seeks help from company employees who use the product in company offices located throughout the country (for example, banking applications in local offices). Local offices employees are very familiar with the application your team is developing. But you will need to deal with the following possible challenges/risks:

* Employees in local offices do not work according to agile. They are engaged in operations every day. Their approaches and experiences are different from yours (run activities, day plan, mindset)
* Before teams can help with test activities, your team needs to spend time and resources learning the basics it needs to work.
* Need to choose the type of daily/weekly testing meeting that suit both types of teams (agile and non-agile)
* Non-agile teams won't be able to spend 100% of their time helping you with test activities. The agile test leader needs to choose the right schedule for the test activities, depending on the organizational context.
* Organize verification of legal requirements where legal needs to be involved
* Organize user testing and gathering user feedback

#### How to manage testing activities when some of the teams are agile and others are less agile is covered in section 5.4.1 Structuring challenging test activities and test process using a quality assistance approach.