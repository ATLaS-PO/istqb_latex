## Test Processes

There are some test processes which are challenging to enable in an agile process. This section covers typical processes and provides suggestions on how to organize them to avoid or successfully address problems.

### Testing challenges in scaled agile product development

When scaling the agile product development in a value-driven organization some issues arise that are not present in a classic organization. Some typical challenges are:

* Agile teams cannot test the full solution independently and when responsibility for performing cross-team test activities becomes **ambiguous** this can result in testing being neglected. See the section 5.1.2 for more information.
* Changing the mindset throughout the organization to allow testers to move into early product development when forming hypothesis and exploring user needs
* Determining if certain types of testing should be organized in one or multiple teams and determining when to switch between the two concepts. See section 5.1.5 for more information.
* Establishing transparency for stakeholders across self-organized teams using classic test metrics. See the section 5.1.3 for more information.
* Slicing up test activities to fit them into an iteration and avoid pushing test efforts forward, resulting in not being able to finish all activities before a release. See the section 5.1.4 for more information.
* Coordinating and synchronizing test efforts across agile and non-agile teams both internal and external to enable the delivery of one common solution. See the section 5.1.2 for more information.

### Coordinate testing efforts across agile and non-agile teams

If QA and testing are treated as separate activities, it becomes more challenging to establish a shared understanding and responsibility for them, identify and minimize dependencies between teams, and enable teams to prioritize tasks effectively.

Coordination of tests between teams can be challenging, particularly if some teams are non-agile, in agile transition or from a third party. The following proven agile practices are examples of how to coordinate testing across agile and non-agile teams.

* One backlog / cross-team refinement
* Big room planning (e.g., PI planning)
* Scrum of Scrums
* Demo of integrated and tested product increments
* Retrospective / inspect & adapt
* Impediments and risk boards
* Debt handling
* Technical enablers

### Test and flow related metrics
To assess the effectiveness and efficiency of value delivery across the organization, it is necessary to align on a set of metrics. Subsequently, all teams across the value stream should regularly measure and share their results.

Classic testing metrics focus on coverage, product quality and effectiveness of testing, but not on the flow of value. Agile test leaders and agile test team leaders should also use other types of metrics that help measure the full value stream. As mentioned in chapter 4, metrics cover three aspects:

* Outcomes in terms of business value.
* Outputs in terms of delivery and performance
* Maturity in terms of people and processes

Outcomes in terms of business value.

Organizations often focus on the things which increase the value for the organization itself when measuring outcomes in terms of business value. However, cost reductions which increase value for the organization, do not necessarily result in added value for the customers and can decrease value for customers. If the organization is not ready to define and measure business value it is better to start with delivery and performance metrics.

Outputs in terms of delivery and performance

To help organizations accelerate delivery and performance, there are four key metrics ([https://cloud.google.com/blog/products/devops-sre/using-the-four-keys-to-measure-your-devops-performance](https://cloud.google.com/blog/products/devops-sre/using-the-four-keys-to-measure-your-devops-performance)):

* Deployment frequency
* Lead time for changes
* Change failure rate
* Time to restore a service

When selecting which metrics to use it is helpful to think about leading and lagging indicators. The advantage of leading indicators is that they give early feedback. Leading indicators help show if the expected results will be achieved. Lagging indicators measure the actual results.

Regardless of the types of metrics which the organization starts with it is important that agile test leaders and agile test team leaders focus on the same metrics.

### Structure challenging test activities and test processes 

Test activities and test processes need to be structured so they fit into agile at scale. Agile Tester (ISTQB Agile Tester), recommends converting test levels into test activities. But this approach is typically not sufficient when scaling. Quality assistance can help to address those challenges.

Structuring test activities

Except for component testing, test activities can be difficult to fit into iterations because establishing the infrastructure takes more time and a coordinated effort.

Such test activities can be clustered based on their purpose:

* Testing functional integration is traditionally done in test levels such as system testing, system integration testing and acceptance testing.
* Testing technical integration is based on architecture design and interface specifications. One challenge is to accompany emerging technologies like asynchronous architectures (often called microservices). If microservices were very well encapsulated, agile teams could successfully test technical integration with a big bang approach, because there would hardly be a need for troubleshooting across teams in order to isolate defects. In practice technical integration testing involves quite a bit of troubleshooting which can be harder with asynchronous architectures.
* Testing non-functional quality characteristics such as performance efficiency, reliability, security and accessibility.

Some of these test activities may be performed outside iterations but agile teams need to retain ownership of and responsibility for testing. Teams should prefer testing within iterations since deferring tests to a separate level weakens their definition of done. To support the teams handling some of these activities within a sprint, test automation can play an important role.

Handling deployment and release cycles

If deployments and releases are not synchronized between agile teams there will be a wasteful number of extra configurations to be tested. So, all teams should work on the same rhythm and plan together what to implement and collaboratively test in each iteration. To counter the risk that this aligned plan is derailed by delays within individual teams, dependencies between teams should be reduced. Agile test leaders and agile test team leaders should be familiar with common approaches for reducing dependencies.

Managing organizational risk

Planning risks for cross-team testing should be managed using typical agile procedures. A shared risk board enhances visibility, and agile practices such as big room planning, synchronization meetings and reviews can be used for risk mitigation.

Establishing working agreements with non-agile teams or functions

Value-driven organizations often have non-agile or less agile units.

These units may lack the ability to make frequent deliveries, respond quickly to feedback and to regularly inspect and adapt their processes. So, a successful collaboration will require working agreements.

Coordination of agile and non-agile teams has been described in section 5.1.2.

Alignment with vendors, suppliers or partners may be particularly challenging. Agile test leaders can participate in the tender process and help describe the parts of the request for proposal related to quality and testing.

For existing vendors, suppliers or partners, a strategic initiative may be needed to modify contracts or even choose other vendors, suppliers or partners.

### Test activities performed by stream-aligned teams and specialized teams 

An agile test leader and agile test team leader need to organize test activities in different manners depending on the type of activities and the complexity of the solution and organization. Teams can be classified as a stream-aligned, complicated-subsystem, enabling or platform team. How a team is organized impacts on what testing activities are effective and how it collaborates with other teams.

Agile test leaders and agile test team leaders must understand how the different types of teams interact and support each other.

Test activities in different types of teams:

Test activities which are typically performed by a **stream-aligned team** are:

* Traditional test activities related to feature development
* Hypothesis testing
* Test activities due to technological changes on corporate level or general organizational risks

Test activities which are typically performed by a **platform team** as a service are:

* Services to reduce the number of things which a stream-aligned team needs to handle
* Shared test tools and other test infrastructure
* Shared common components for testing purposes

Test activities which are typically performed by **a complicated-subsystem team** through collaboration are:

* Help with providing special types of testing which are too complicated to be dealt with by a stream-aligned team or platform team.
* Help with testing special sub-systems which are too complicated to be dealt with by a stream-aligned team or platform team.

Test activities which are typically performed by an **enabling team** in a consultative manner:

* Temporary test activities which often require specialized knowledge and skills which the other teams do not have or have not yet fully mastered
* Research and experiment with new methods and tools for improving testing on behalf of the other teams

Analyzing team structure related to test activities

Depending on the test activity and the knowledge and competencies in the existing teams, different team structures could be useful. Some of the common aspects to consider are:

* Non-functional testing
  * Having a platform team or enabling team could be helpful
* The need for independent testing
  * Not necessarily obtained by formal organizational boundaries
* The structure and complexity of the technical solutions
  * Platform teams, complicated-subsystem teams and enabling teams may become more relevant
* Collaboration with non-agile teams and functions.
  * One way is to treat them as enabling teams providing knowledge
  * A second possibility can be platform teams which enhance self-service options
  * Another way is to make interdependencies as visible as possible

How to manage test activities when some of the teams are agile and others are less agile is covered in section 5.1.4. Structure challenging test activities and test processes.