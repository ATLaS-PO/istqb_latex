## What is Quality Assistance?
Quality management ties together disciplines like quality control (QC) and testing, quality assurance (QA) and quality improvement, as stated in the Certified Tester Foundation syllabus [@ISTQB:2023]. These disciplines are sets of activities that contribute to quality management. In this context software process improvement (SPI) can be seen as a closely related topic to quality improvement, which consists of activities designed to improve quality. There are approaches to quality management that suggest the use of certain mindsets, methods, processes, and tools. These approaches can vary in the types of activities included under quality management:

* Traditional software quality management has a high focus on QC and QA.
* Total quality management (TQM) is one approach for agile test leadership at scale. In the Lean Lexicon [@lean:2014], TQM is described as a management approach in which all departments, employees, and managers are responsible for continuously improving quality.
* Quality assistance is a mindset and an approach to quality management, which supports business agility. Similar to TQM, it emphasizes continuous improvement activities more than QC activities. Moving from QC to quality assistance is a success factor for businesses[@gartner:2018]. Also similar to TQM, quality assistance strives to improve quality so that products and services meet or exceed customer expectations. This means quality assistance fosters a value-driven organization.

As can be seen from <#figure:QualityAssistance> there are overlaps between the various practices and approaches.

![QualityAssistance](RackMultipart20230716-1-22hy1u_html_4a4dafa5ebf32257.png "Quality assistance as an approach to quality management.")

## Quality Assistance Applied to Test Management

Agile test management draws upon methods and techniques from traditional software quality management and combines these with new mindset, culture, behaviors, methods, and techniques from quality assistance. See <#figure:AgileTestManagement> for the relationships. Judging which aspect to include from each approach is highly context dependent. However, if the organization is striving to increase its business agility, then adopting a quality assistance approach will support this direction.

![AgileTestManagement](RackMultipart20230716-1-22hy1u_html_a551d576e943b9a7.png "Agile test management combines approaches.")

Traditional test management has a tendency to focus on managing and controlling the work of others. Test management in the agile organization has a broader scope than solely focusing on testing the software. By shifting agile test management to a quality assistance approach, agile test leaders spend more time enabling and empowering others to do the test management themselves. The aim of this support is to contribute to the improvement of the organization's QA and testing skills with a view to enabling better cross-functional team collaboration.

Business agility also drives the move away from traditional management roles toward self-empowered delivery teams and enabling leaders (also called servant leaders or leaders who serve). As a consequence, people in roles such as project manager and test manager sometimes struggle to find their place in organizations moving toward business agility. This shift means that traditional roles[^1], such as test managers, test coordinators, QA engineers, and testers, need to dedicate more time and effort to foster the necessary quality management related skills and competencies throughout the organization rather than actually doing all the testing.
[^1]: Naming convention of roles differs from organization to organization.

With business agility there is a move toward preventing rather than finding defects, to optimize quality and flow. Automation, "shift left" approaches, continuous testing, and other quality activities are necessary to keep pace with the incremental deliveries of customer-focused organizations. These practices are often described using the concept called "built-in quality". Additionally, there is also a move to "shift right." "Shift right" practices and activities focus on observing and monitoring the solutions in the production environment and measuring the effectiveness of that software in achieving the expected business outcomes. These practices are often described using the concept called "observability".

Moving to a quality assistance approach provides many opportunities to reinforce the view that quality is a whole-team responsibility across the entire organization. One way is for the organization's management to support collaboration within expert groups, often known as communities of practice (CoP). The expert groups' main goal should be to go to places where the work happens and work with delivery teams to spread knowledge and behavior.

A successful implementation of quality assistance as a quality management approach results in:

* The organization developing a continuous approach to quality with a collaborative quality focus and automated tests
* Less hand-offs for test activities that slow down value delivery
* Less dependence on testing late in the delivery process, which reduces the overall cost of quality

There are many other positive outcomes of quality assistance, which will be covered in later chapters.

## Skills for Quality Assistance

Agile test leaders, and all other leaders in an agile organization, should develop the skills needed to build a quality mindset and culture. This means developing both delivery team competencies and a general understanding of value streams and improvement practices.

Agile test leaders use skills such as quality coaching, facilitation, training, and change leadership based on what is necessary. Examples are:

#. An agile team may need help to understand how their delivery integrates with other teams' deliveries to provide the final solution. The agile test leader can help facilitate a value stream mapping (VSM) workshop with participants from different teams, first training them in the technique and then coaching them by asking questions about the different steps in the value stream (see next chapter).
#. A team's members needs help with improving the way they work during stressful situations, as they have identified that the number of defects increases during these times. The agile test leader can coach the team so they can keep the focus on quality.

Some additional tasks that an agile test leader could become involved with include:

* Helping to create a quality and testing culture
* Providing guidance, inspiration, and motivation for all types of engineers to improve their knowledge and skills about quality and testing
* Advocating the merits and benefits of test-driven development (TDD) and behavior-driven development (BDD) (practices supporting built-in quality)
* Visualizing the impact of quality and testing
* Communicating with product and solution stakeholders
* Being a customer advocate

There are many opportunities for agile test leaders to help people build their competencies. This can be done as short training sessions to solve a concrete problem or as a small series of hands-on training sessions as part of the daily work. Often, the situation occurs without the need for preparation and the agile test leader just needs to identify the opportunity when it occurs and work with the individual or team. In other situations, an agile test leader may establish coaching and training groups with practitioners or experts. These groups can help team members realize they need to learn about subjects they do not know exist or understand the relevance of to the delivery. Shifting the culture and mindset in an organization may require a significant coaching and change leadership effort over a long period of time as a continuous practice. Therefore, the work of an agile test leader differs significantly from the work of a traditional test manager.

The agile test team leader can provide quality assistance in a delivery team, while the agile test leader focuses more across the whole organization to improve quality.

### Change Leadership

Organizations that want to successfully transform to business agility need to have in place effective change leadership that facilitates change management activities. Adopting a quality assistance approach provides support to all members of a team and the whole organization in identifying opportunities and threats, implementing experiments, and dealing with changes. Quality assistance needs to align with the organizational change management program. There are many different models to drive change, e.g., the 8-Step Process for Leading Change [@kotter:2012], ADKAR® model for individual change [@prosci:2021], and Plan-Do-Check-Act (PDCA) [@lean:2014].

It is important to take into account the human aspect, where emotions affect the ability to deal with change. How these emotions are handled plays a significant role in successfully implementing change. Change provides an opportunity for people to grow and therefore change leadership needs to accommodate different learning styles and paces.

Managing change over time requires continuous adaptation to organizational factors and to marketplace volatility. It also requires a balance between top-down and bottom-up management, ensuring employees are empowered to make changes.

Quality assistance helps find improvements by fostering what is called kaizen in lean methodology and is called Nexus sprint retrospective [@scrum:2021]. Agile test leaders and agile test team leaders influence the changes by leveraging their change leadership skills, working with other stakeholders to move toward quality assistance, and involvement in value stream mapping.

An important part of change leadership is to make the changes visible and celebrate achievements. Some examples are:

* Championing component testing for correct test coverage and "shift left" mentality
* Facilitating creation of a library of automated test scripts so that teams can share these assets across teams, promoting reuse
* Introducing common tools across the organization that integrate, provide visibility, and synchronize information

### Quality Coaching

Like other coaching forms, quality coaching is a form of dialog between a coach and one or more of the persons being coached. Quality coaching focuses on identifying and dealing with challenges related to quality, flow of business value, and customer collaboration.

Coaching focuses on helping people to become aware of their values, fears, and any limiting beliefs they might hold. Therefore, coaching is important in organizations that undergo significant change, such as changing from a classic program and project-driven organization to an organization moving toward business agility.

It has been, and to some extent still is, a general approach or principle in coaching that the person being coached implicitly knows the solution to a particular challenge and that the role of the coach is to help the person being coached realize this and hence come to a solution. But coaching can also be performed as a more collaborative dialog between the person being coached and the coach. In the collaborative dialog there is less emphasis on reaching a goal or solution and more emphasis on gaining understanding and insight.

A collaborative dialog requires that the coach and the person(s) being coached are willing to engage in the conversation and to reflect on what they discuss. The coach can put themself in the position

of the person being coached to understand that person's perspective and then link it to the coach's perspective and position in whatever they are exploring.

Quality coaching is an important skill when working with quality improvements. Some agile events and processes are very well suited for collaborative dialog, e.g., retrospectives. Depending on the situation, it may be necessary to supplement existing agile processes with processes dedicated to quality coaching.

Quality coaching can also be used outside team events on a one-to-one basis, e.g., when teaming up with an individual to learn a new skill.

It is important to create a safe space for the person being coached, as quality coaching may explore a person's fundamental values and limiting beliefs.

### Facilitation

Facilitation is a skill used to help people reach an outcome or decision by supporting individuals through interactions. The facilitator's task is to lead people to use their specific knowledge and skills for this purpose.

Facilitation is an essential skill in quality assistance because it allows everyone to participate in discussions about quality and to take ownership of solving quality challenges. With a traditional test management approach, the QA and testing professionals are more inclined to tell other people what they need to do to solve quality problems. They subsequently control the implementation of the improvements and monitor that they remain in place. In an agile organization, all team members share the responsibility for built-in quality. It is crucial that an agile test leader can engage various participants in the processes and conversations about improving quality and will allow others to find and implement solutions to quality problems.

### Training

There are many different training methods, e.g., classroom or online, self-study, on-the-job, simulation, group discussions, mentoring, internship, and peer-to-peer training. It is important that the agile test leader can design different learning experiences suitable for each person, the knowledge they are required to understand, and the skills they need to gain. An important trend is micro learning, where people can incorporate short learning sessions throughout their day.

To really scale learning, the agile test leader can team up with the human resources (HR) department focusing on learning and talent development. Training that helps people build their skills can use all the methods mentioned earlier. Collaboration with HR can be crucial if the training of leaders in the organization needs to be strenghtened to include sufficient knowledge about quality and testing.