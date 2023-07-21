## Facilitate Value Stream Mapping
Quality and testing are important aspects to consider when identifying and optimizing both operational and development value streams (see details in [What is a Value Stream?](#section:what-is-a-value-stream)). Therefore, it is essential that people in testing roles, and all others who contribute to the value stream, understand the concepts and thinking behind value streams as described in lean methodology.

Lean thinking and practices focus on maximizing the value outcome by looking at the entire system or flow of value from start to end. This differs from looking at each part of the value stream in isolation, which can lead to local optimization such as only within one functional area. Local optimization can lead to a reduction in total value outcome and hence a sub-optimization of the full value stream. In value-driven organizations, people working in quality and testing functions help to optimize the whole value stream, not just testing activities.

### What is a Value Stream? {#what-is-a-value-stream}
Avalue stream is a group or collection of working steps, including the people and systems that they operate, as well as the information and the materials used in the working steps. Each of the working steps should be a value-adding activity to the previous ones, and together the working steps will create a flow of value for customers.

Avalue stream starts with people's ideas, the customer's needs, or problems to be solved. Peopleworking within a value stream organize and structure the working steps in the value stream to create aproduct ora solution for the customerin anefficient way. The flow shouldbe optimized continuouslyto reduce non-value-adding activities.

All value streams include actions to process information from the customer and actions to transform the product on its way to the customer. Because testers must gain a deep understanding ofthe customer's domain as part of their job, they are often well equipped to help identify points of collaboration with customers and see how information from customers affects delivery or development. Anyone within the agile team should have access to the customer in order to be able to contribute to improving the value stream. Treating everyone within the organization that you aredelivering a product to as if they were customers follows lean thinking. Where direct contact is not possible, then finding alternative customer representatives may be a solution.

Value streams can be categorized as operational or development.

Operational value streams are all the working steps and people required to bring a product from[@lean:2014]. For example, a telco operator messaging service contains five working steps, from client subscription to the delivery of its message. This could be visualized as in the diagram at <#figure:MessagingService>.

![MessagingService](fig/example-of-messaging-service.eps "Example of messaging service.")

Development value streams take a product from concept to market launch [@lean:2014]. This could be visualized as in the diagram at <#figure:DevelopmentValueStream>.

![DevelopmentValueStream](fig/example-of-development-value-stream.eps "Example of a development value stream (simplified).")

In some cases, the operational and development value streams can be the same, e.g., a company that develops and delivers IT solutions. Agile test leaders participate in identifying and analyzing value streams.

It is part of quality assistance to help others to take a broader perspective on quality and testing. By collaborating with others to identify and analyze value streams, agile test leaders improve both quality and the flow of value.

If the work to identify and describe value streams is already done, then the next step is to analyze the value streams to optimize quality and flow (see [Analyze a Value Stream from a Quality and Testing Perspective](#section:analyze-a-value-stream-from-a-quality-and-testing-perspective) for details). If the description of the value streams is missing or if the description is at a high level and needs further details, then QA and testing professionals can facilitate that the work is done using value stream mapping (see [Value Stream Mapping] (#section:value-stream-mapping)).

### Value Stream Mapping {#value-stream-mapping}
VSM is a technique for visualizing and analyzing the working steps in a value stream, including the flow of work products (materials) and information needed to produce a product or service. It gives an overview of:

* Value-adding activities
* Non-value-adding but needed activities
* Non-value-adding activities (waste)

Value-adding is determined from the perspective of the customer. Some activities are not value- adding from a customer perspective. Some of these are activities needed for the company to build and deliver the product, e.g., system testing. Others can be eliminated or reduced without negatively impacting the end product.

When used for the first time, VSM results in a high-level process map of the current state and a similar map showing the desired future state. In addition, it results in identifying improvement initiatives needed to move from the current state to the desired state.

The benefit of VSM is an improved flow of value, done by constantly improving the value-adding activities and especially by removing or redesigning the non-value-adding activities. As low quality leads to rework and delays, VSM can help improve quality throughout the value stream. It can also give a shared understanding of how much and how fast the value stream needs to deliver to fulfill customer demand. For development value streams this is closely linked to the continuous delivery pipeline. However, it is not as easy to quantify in software development as in manufacturing, because software is constantly changed. This applies to the needs or requirements (inputs), the work that needs to be done to come from the backlog item to a product increment (transformation rules), the product increment itself (output), and the market in which the product increment is launched (outcome). Lastly, value stream mapping can increase the visibility and understanding of how the work of different people, teams, and functions contribute and hence improve collaboration.

There are different notations used in VSM. The technique was first used to analyze and improve manufacturing systems, but has since been adapted to fit other industries such as software development and product development. As a starting point, one suggestion is to use a simple notation suitable for service or product development. See the example in <#figure:TotalLT>.

|
 ![workingStep](fig/working-step.eps) |
A working step or process activity. |
| --- | --- |
|
 ![ProductUnderDevelopment](fig/product-under-development.eps) | Product under development moving from one working step to another one. |
| ![PerformingActivities](fig/people-team-function.eps) |
People, team(s), or function(s) performing the activities in the working step. |
|
 ![ContainsMetrics](fig/contains-metrics.eps) | Data about a working step. Contains metrics and their values, which are required to understand the system; e.g., lead time (LT)= 22 hours and processing time (PT) = 1 hour. For the definition of LTand PT, see section [Metrics for Analyzing a Value Stream] (#section:metrics-for-analyzing-a-value-stream). |
|
 ![Inventory](fig/Inventory.eps)
 | Inventory between two working steps, e.g., the number underneath the symbol indicates the number of tasks piling up, which is 30. For the definition of inventory, see section [Identify Non-Value-Adding Activities (Waste)](#section:identify-non-value-adding-activities). |
|
 ![TimelineForWorkingStep](fig/Inventory.eps) |
Timeline for each working step, usually comprises wait time andPT. |
|
 ![TotalLT](fig/all-working-step.eps "Simple notation for value stream mapping.") |
Sum of all working steps for the entire value stream, e.g., total LT and total PT. |

As the concept is coming from manufacturing, there are a lot more symbols available, especially to represent material and information flow.

Additional notation can be added depending on the improvement context once a first current state value stream map has been created. For example, to understand formal and informal information flows in more detail, VSM could be combined with additional mapping. In the case study described in "FLOW-assisted value stream mapping in the early phases of large-scale software development" [@binali:2016], they identified problems with the first current state value stream map. To solve some of the problems they used additional information flow modeling (FLOW).

As VSM is used in different industries, the steps and the content of each step may vary. The following is a high-level description of typical steps in VSM:

#. Determine whether the focus is on an operational or development value stream.
#. Define the start point and end point of the value stream as well as the groups of products or service to be mapped.
#. Create a value stream map of the current situation (the as-is state) starting with steps from either the beginning or the end of the value stream.
#. Add key performance measures to each step and identify bottlenecks, delays, quality problems, and non-value-adding steps (detailed information in section [Analyze a Value Stream from a Quality and Testing Perspective](#section:analyze-a-value-stream-from-a-quality-and-testing-perspective)).
#. Create a future state value stream map including changes to steps and performance measures.
#. Agree and plan improvement initiatives to optimize the value stream with regard to bottlenecks, delays, quality problems, and non-value-adding steps.

The current state (as-is state) can be visualized as in the diagram at <#figure:DevelopmentDiagram> (the metrics are explained in section [Metrics for Analyzing a Value Stream] (#section:metrics-for-analyzing-a-value-stream)).

After doing VSM for the first time, the progress is measured and monitored on a regular basis. Once the initial future state is reached, or after a period, the technique can be repeated. Alternatively, the technique can be used to map other value streams in the organization or other products or service groups in the same value stream. The key is to map and analyze value streams iteratively. By doing so, current state and future state maps will visualize data that supports continuous improvement of the value stream.

From a QA and testing perspective, VSM can be used to improve QA and testing activities in a broader context than a single agile team. The technique works best when used in a small group consisting of people who work and understand the different working steps in the value stream and include leaders who should help sponsor and prioritize the improvement efforts [@liker:2006].

In the context of QA and testing, VSM can be used as part of a continuous improvement cycle (see [Continuous Improvement of Quality and Testing](#section:continuous-improvement-of-quality-and-testing)). It is also frequently used in organizations to understand how to organize around the flow of value to avoid functional silos. This can be done as part of team retrospectives where teams optimize continuously or a VSM workshop could be the agenda of retrospectives. It is important that the perspective of quality and testing is included when deciding how to organize people in teams.

As VSM focuses on a higher level of abstraction than a single process, the technique should not be used for analyzing processes in detail. Equally, the technique requires a broad perspective and should not be used by a single person or a small group that includes people representing only one function or one working step in the value stream.

![DevelopmentDiagram](fig/basic-as-is-diagram.eps "Basic as-is diagram for a development value stream.")

If VSM is not yet used in the organization (e.g., facilitated by a scrum master, leader, agile coach, or other type of facilitator), there may be opposition to it. As it requires different people to participate, it is important to get the buy-in from these people and potentially from their leaders.

Getting and using performance measurements consistently throughout the value stream can also be a challenge. Typical metrics and measurements and how to use them to analyze the value stream are covered in the next section.

## Analyze a Value Stream from a Quality and Testing Perspective {#analyze-a-value-stream-from-a-quality-and-testing-perspective}

QA and testing activities can help identify defects in every working step of product development. Traditionally, testing activities have focused on examining the quality of the functional and non-functional requirements at the beginning of product delivery and toward the end when examining to what extent the delivered system would fulfill the stated requirements and also fulfill the needs of the customer. In agile at scale, by including quality assistance as an important part of the teams' overall responsibility for quality, agile test leaders and agile test team leaders should also examine the quality of the processes in collaboration with people contributing to the value stream(s).

Visualizing the value stream has many benefits, as described in the previous section. However, to understand where there may be problems or room for improvement it is key to measure and analyze the performance of the value stream. This is an iterative activity.

Optimizing a value stream focuses on the flow of value and on quality. Therefore, value stream analysis can be a powerful "tool" for anyone who takes a quality assistance approach to quality and testing. It requires awareness of the full picture. Therefore, agile test leaders and agile test team leaders can help others to understand quality and testing problems from a broader value stream perspective. Of course, it is also important to identify value-adding activities and continue to do these well.

### Metrics for Analyzing a Value Stream {#metrics-for-analyzing-a-value-stream}

Organizations want their products to flow to the market at a good pace and with the expected quality required by the customers. This requires a clear understanding of the product flow characteristics at all levels.

To analyze a value stream, it is important to gather data about each working step. The purpose is to look for places to improve both the effectiveness and the efficiency of the value stream. It cannot be stressed enough, though, how important it is to avoid local optimization, which results in sub-optimization of the full value stream. The goal is to enhance the effectiveness and efficiency of delivering value to to customers within the value stream. This often involves improving quality management and testing activities.

The following metrics are typical in software development for analyzing the flow through a value stream:

* Processing time (sometimes called touch time) is the time it takes to complete all the activities in a working step. It is the time when someone is working on the product and adding value to it.
* Wait time (sometimes called delay time) is the time between when a working step iscompleted and the following working step is started. Sometimes, even within a working step, there are wait times between tasks or activities, e.g., the product owner is not available to provide clarification when needed to proceed with a task.
* Lead time is the duration from when the activities in a working step can begin to when they have been completed, and the product is ready for the next working step. In other words, lead time consists of the wait time before the working step and the processing time for the working step.The lead time of individual working steps contributes to the overall lead time of the value stream. In software development this could be the time from a product owner introducing a user story to a development team until the moment where the first customer uses the developed feature.

Flow efficiency, also known as process cycle efficiency or activity ratio, is a measure that compares the total processing time to the total lead time of a value stream. In software development, flow efficiency can increase through automation, such as continuous integration (CI), or when software architectural changes reduce dependencies and waiting time among teams.

Processing time, wait time, and lead time can be measured for both a working step and for the whole value stream.

Typical metrics for analyzing quality are:

* Percent complete and accurate (%C&A) is the percentage of times when the work product in the preceding working step is complete and accurate so that people in the next working step can complete their activities without having to rework parts or find information that should have been provided.
* Rolled %C&A(sometimes called rolled throughput yield) shows how likely a work product can pass through the entire value stream without rework or finding additional information.

with "" as percent complete and accurate for working step 1, as percent complete and accurate for working step 2, and as percent complete and accurate for working step n.

* Phase Containment Effectiveness (PCE) is the percentage of defects[^2] created in a working step that is found in the same working step compared with the total number of defects introduced in the working step and identified both in that working step and later working steps. The metric is different from Defect Detection Percentage (DDP) as the focus is not on a test level but a working step in a value stream and it only includes defects that were created in the working step for which PCE is measured.

[^2]: The ISTQB® definitions of an error, a defect,and a failure differ fromthe ones in common lean literature, e.g., [@lean:2014]. Here the meaning of a defect is according to the ISTQB® Glossary.

where is defects introduced and found in working step 1 and is defects found in subsequent working steps that were introduced in step 1

The diagram in <#figure:StateDiagram> is an example of a value stream map where basic measurements havebeen added for each working step.

Metrics are vital for analyzing a value stream, but it can be a challenge to measure consistently throughout the value stream.As a starting point, use the data that is available. If data is missing, the group doing VSM need to find relevant people who can help estimate the data that is not yet measured and collected.

![StateDiagram](fig/basic-current-state-diagram.eps "Basic current state diagram with flow and quality measurements.")

The group should literally "go and see" how the people throughout the value stream work. This is also called [@wikipedia:2021]. By observing and talking with the people, team(s), and function(s) working in the value stream, the group doing value stream analysis can:

* Understand the working steps and how those working steps are connected to each other
* Discuss data collected by the people in each working step or the need for measuring
* Observe non-value-adding activities (waste)
* Identify the reasons behind the non-value-adding activities
* Collaborate on improvement areas

Quality metrics such as %C&A and PCE are useful for highlighting quality problems in a working step. In the example in <#figure:StateDiagram> the group can discuss why the %C&A for both Define Solution and Build Solution are lower than for Gain User Insight and Launch Solution and how this affects the lead time and the total flow. In the example in <#figure:PhaseContainmentEfficiency> the discussion can focus on the significant percentage of the defects that are detected in downstream working steps. This could include conversations about how QA and QC activities are done.

In the same manner, high wait times resulting in a low flow efficiency can be analyzed to identify bottlenecks. Bottlenecks may be directly or indirectly related to quality and testing. For example, if test execution is done manually and the teams are not controlling the flow of things to test, then more and more things have to wait before they are tested.

As always with metrics, special care should be taken to ensure that everyone understands:

* The purpose of the selected metrics
* How the metrics should be used and how to avoid misuse
* Who should perform the measurements and how to measure

Some metrics used for value stream analysis are only used for a limited period of time to help analyze specific problems and measure the result of an improvement. PCE could be such a metric.

###  Identify Non-Value-Adding Activities (Waste) {#identify-non-value-adding-activities}
There are several ways that non-value-adding activities can be identified in quality and testing activities.

The following are examples from the eight types of waste.

* Transport: Moving work in process (WIP) from place to place in a process [@liker:2006]. It can be movement of products, information, and material, e.g., several remotetesters exchange too much information via emails in addition to all the team meetings they attend.The excessive movement of information may lead to errors and rework.
* Inventory: More than the minimum stock necessary [@lean:2014].This can be whatever is waiting for an input to progress within a process, or waiting because nobody is working on it, e.g., testers create detailed tests for future use but important architectural decisions about the system are pending.The decisions are not expected to be made in the short term, so the tests become inventory and may require additional work once the decisions are made.

![PhaseContainmentEfficiency](fig/example-of-phase-containment-efficiency.eps "Example of Phase Containment Efficiency")

* Motion: Unnecessary movement or activities in a working step or between working steps that do not add value to the product [@lean:2014], e.g., being forced to change the state of a defect report because the workflow in the defect management tool does not allow steps to be skipped even if it does not help coordinate the work through the defect's lifecycle.
* Waiting: Operators standing idle [@lean:2014]. Any person waiting for something (information, work done by others, access to a machine or resource), e.g., testers not progressing in their work because of the network slowing down or because downtime of the test environment interrupts test execution.
* Overproduction: Producing ahead of what is actually needed by the next process or customer [@lean:2014], e.g., a test manager creates large test plans and test reports which nobody reads or are not living documents.
* Over-processing: Unnecessary or incorrect processing [@lean:2014]. Too many actions in a working step or unneeded working steps, e.g., before launching a new feature, the release needs to be approved by many different authorities in the company. Some of the authorities are only a formality.
* Correction: Inspection[^3], rework, and scrap [@lean:2014]. Note that what lean calls inspection could include a late system test level, which might be avoided. Scrap includes defects passed through the value stream resulting in rework and, e.g., an agile test team lead finds that the configuration parameters of a test environment always need a lot of correction cycles.
* Non-utilized talent: Failing to use feedback from employees to improve the process, and not giving people the opportunity to change for the better [@brito:2019]. It also includes not supporting people to grow in their work, through gaining new skills and competencies, e.g., not making use of an employee's skills, experience, and knowledge when assigning employees to specific roles.

[^3]: The ISTQB®definition ofinspection differs from theones in common lean literature,e.g., [@lean:2014].

Agile test leaders and agile test team leaders need to adopt lean thinking to analyze and optimize the organization's value streams. VSM can help identify waste in both an operational and a development value stream. In the situation of poor effectiveness or inefficiency, there are a few typical strategies to identify waste along a value stream:

* Look for work products piling up before and after each working step.This could result from waitingtimeofthe handoffsbetweenteam members.Forexample, deficientsignaling (lack of visual management) that work products are ready for the next working step and how informationflowsmayleadtoinefficienthandoffs.Therefore,reducingandeveneliminating these problems will help to reduce lead time.
* For each working step, observe the work products and the people creating them, and this may reveal opportunities to reduce processing time. It may also reveal the opposite, where important testing or quality activities are deferred that result in quality debt and a lower PCE.
* Search for and quantify defects before and after each working step. A high number of defects indicate waste. If the processing time increases but the number of defects remains the same, it could indicate that there are undiscovered defects or technical debt in a working step. So quantifying defects helps to identify opportunities to introduce built-in quality activities, especially for development value streams.
* Look at the number of support requests from customers or other stakeholders, which might come from quality issues. Handling such requests may interrupt the focus on current product delivery work andnegativelyaffect theleadtime andprocessing time.

The diagram in <#figure:FutureStateMap> is an example of a future state map where issues have been identified. The group has defined some targets for how the performance should be improved.

The future state map is a goal and not an in-depth analysis of how to reach the future state with all the improvement initiatives. The main objective is to identify the critical points along the value stream and develop knowledge on how to use them for more value, especially better quality and reduced

lead time, at lower costs. How to identify, plan, and conduct the improvement steps using a structured problem-solving approach is covered in [Continuous Improvement of Quality and Testing](#section:continuous-improvement-of-quality-and-testing).

Analyzing and improving value streams essentially relies on learning to see working flows and empowering people to act differently regarding quality issues. Therefore, agile test leaders should contribute in a number of ways, for example:

* Promote a holistic view when analyzing problems and optimize the value stream
* Help people grow in their work and understand how quality and testing may impact the performance of a value stream
* Facilitate and coach a built-in quality approach, for example:

  * Encourage the development of in-depth knowledge of the product in the people creating it to find the defects before the clients find them, in the shortest lead time
  * Advocate and support implementation of a test-driven development approach
  * Promote a "stop, fix it first" culture to ensure continuity in the value creation to the customer instead of extensive testing at the end
  * For critical defects, swarming may need to be introduced for those features in order to contain the problems. In the context of multiple agile teams doing frequent deliveries, it prevents the loss of any critical information because of fast-changing circumstances. It also prevents the addition of any new blockers to software creation that might introduce new defects
  * Do root causes analysis of defects as part of the shift left approach; this creates opportunity to change the way people are developing and testing, for better product delivery

* In the context of an operational value stream, help identify quality problems in a customer journey
* Support the inclusion of customers or end-users in a value stream, e.g., through:
  * Interactions with beta customers
  * Regular collaboration in acceptance test-driven development (ATDD) user story workshops
  * Exploratory testing sessions involving customers or end-users

Agile test leaders and agile test team leaders can help devise improvement initiatives to reduce waste through a number of PDCA cycles (see section [Structured Problem-Solving Approach for Testing and Quality Activities](#section:structured-problem-solving-approach-for-testing-and-quality-activities)). 

If the organization understands the importance of quality assistance, then value stream mapping can be a powerful technique to introduce as part of the quality assistance effort.

![FutureStateMap](fig/example-of-future-state-map.eps "Example of future state map with improvement goals highlighted in red")  
