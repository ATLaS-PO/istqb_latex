# Fundamentals of Testing

## Showcase of the LaTeX template for ISTQB documents

### Regular text

Regular parapgraphs and senteces are written without any formatting. New line is depited by two spaces at the end of the line and a new line.

Nunc cursus ultrices magna, eget accumsan sem facilisis vitae. Proin eget facilisis velit. Praesent tortor arcu, sodales ut auctor eget, tempor ut justo. Nunc sed lorem in nisl venenatis ornare sodales quis massa. In molestie hendrerit sagittis. Duis id sem at enim laoreet tincidunt non eu quam. Suspendisse potenti. Etiam luctus efficitur tortor. Vivamus a justo libero.  

Ut a metus sed quam ornare sagittis nec a velit. Donec vehicula purus nibh, eget tempor mauris laoreet rhoncus. Nullam vehicula eu velit quis mollis. Vestibulum venenatis turpis odio, eget gravida nulla mattis eu. Praesent feugiat risus in ante feugiat blandit. Curabitur et odio sed sapien suscipit vestibulum. Mauris viverra neque vitae arcu tempus lobortis. Maecenas vulputate elit quis nisi facilisis ultrices. Aenean imperdiet nibh a mauris efficitur pretium. Donec posuere sodales augue sed scelerisque. In hac habitasse platea dictumst.  


### Lists

Unordered list starts with some sentence, following a new line. Asterisk (`*`) depict each list item. 

* This is the first item in the list
* Folowed by a second one
* And so on, until you have them all here

Numbered lists are the same, but uses number sign dot to add a list item.

#. This is the first item in the list
#. Folowed by a second one
#. And so on, until you have them all here

### Section references

If you want to reference the section, it have to have an [header attribute](https://witiko.github.io/markdown/#option-headerAttributes). So for this section it would be not only text `### Section references` but also a header attribute so it will be define like `### Section references {#section-references}`

Section references without a custom text are done like this:

- Link to <#section:seven-testing-principles> should redirect you to the section Seven Testing Principles in this MD document.  
- Link to <#section:fundamentals-of-testing> will redirect you to the the head of another MD document.

Section references with custom text:

- You can add link to the section with custom text like this [testing principles](#section:seven-testing-principles). And it doesn't matter if the section is in this or any other MD document.

For more information, see the documentation of the Markdown package for \TeX{} referenced in section *Further Reading* at the end of this document.

### Figures

Here is an example image that is loaded from the `img/` folder:

 ![example](istqb-logo.png "Here is a caption describing the image."){width=3cm}

You can reference the image from the text of the document as follows: <#figure:example>.

### Tables

Here is an example table:

 | Right | Left | Default | Center |
 |------:|:-----|---------|:------:|
 |   12  |  12  |    12   |    12  |
 |  123  |  123 |   123   |   123  |
 |    1  |  1   |   1     |     1  |

 : Here is a caption describing the table. \label{table:label}

You can reference the table from the text of the document as follows: <#table:label>.

### References

Here are example citations for standards [@iso-iec:2022], ISTQB documents [@istqb:2023], books [@beizer:1990], journal articles [@brykczynski:1992], and web pages [@marick:2013]. For instructions on writing your own references to `example.bib`, see the Bib\LaTeX{} manual [@kime:2023, Chapter 2]. The full list of references is shown at the end of this document.

### Indexing

To index a term, write `[term]{.index}`. For example, [0-switch coverage]{.index}, [component integration testing]{.index}, or [functional appropriateness]{.index}. All indexed terms are shown at the end of this document.

## What is Testing?

Software systems are an integral part of life [@beizer:1990], from business applications (e.g., banking) to consumer products (e.g., cars). Most people have had an experience with software that did not work as expected. Software that does not work correctly can lead to many problems, including loss of money, time, or business reputation, and even injury or death. Software testing is a way to assess the quality of the software and to reduce the risk of software failure in operation.

A common misperception of testing is that it only consists of running tests, i.e., executing the software and checking the results. As described in section 1.4, software testing is a process which includes many different activities; test execution (including checking of results) is only one of these activities. The test process also includes activities such as test planning, analyzing, designing, and implementing tests, reporting test progress and results, and evaluating the quality of a test object.

Some testing does involve the execution of the component or system being tested; such testing is called dynamic testing. Other testing does not involve the execution of the component or system being tested; such testing is called static testing. So, testing also includes reviewing work products such as requirements, user stories, and source code.
Another common misperception of testing is that it focuses entirely on verification of requirements, user stories, or other specifications. While testing does involve checking whether the system meets specified requirements, it also involves validation, which is checking whether the system will meet user and other stakeholder needs in its operational environment(s).  


Test activities are organized and carried out differently in different lifecycles (see section 2.1). 


### Typical Objectives of Testing
For any given project, the objectives of testing may include:  

* To prevent defects by evaluate work products such as requirements, user stories, design, and code 
* To verify whether all specified requirements have been fulfilled 
* To check whether the test object is complete and validate if it works as the users and other stakeholders expect 
* To build confidence in the level of quality of the test object 
* To find defects and failures thus reduce the level of risk of inadequate software quality 
* To provide sufficient information to stakeholders to allow them to make informed decisions, especially regarding the level of quality of the test object 
* To comply with contractual, legal, or regulatory requirements or standards, and/or to verify the test object’s compliance with such requirements or standards


The objectives of testing can vary, depending upon the context of the component or system being tested, the test level, and the software development lifecycle model. These differences may include, for example:

* During component testing, one objective may be to find as many failures as possible so that the underlying defects are identified and fixed early. Another objective may be to increase code coverage of the component tests.
* During acceptance testing, one objective may be to confirm that the system works as expected and satisfies requirements. Another objective of this testing may be to give information to stakeholders about the risk of releasing the system at a given time.

### Errors, Defects, and Failures 
A person can make an error (mistake), which can lead to the introduction of a defect (fault or bug) in the software code or in some other related work product. An error that leads to the introduction of a defect in one work product can trigger an error that leads to the introduction of a defect in a related work product. For example, a requirements elicitation error can lead to a requirements defect, which then results in a programming error that leads to a defect in the code.

If a defect in the code is executed, this may cause a failure, but not necessarily in all circumstances. For example, some defects require very specific inputs or preconditions to trigger a failure, which may occur rarely or never.

Errors may occur for many reasons, such as:

* Time pressure
* Human fallibility
* Inexperienced or insufficiently skilled project participants
* Miscommunication between project participants, including miscommunication about requirements and design
* Complexity of the code, design, architecture, the underlying problem to be solved, and/or the technologies used
* Misunderstandings about intra-system and inter-system interfaces, especially when such intrasystem and inter-system interactions are large in number
* New, unfamiliar technologies

In addition to failures caused due to defects in the code, failures can also be caused by environmental conditions. For example, radiation, electromagnetic fields, and pollution can cause defects in firmware or influence the execution of software by changing hardware conditions. 

Not all unexpected test results are failures. False positives may occur due to errors in the way tests were executed, or due to defects in the test data, the test environment, or other testware, or for other reasons. The inverse situation can also occur, where similar errors or defects lead to false negatives. False negatives are tests that do not detect defects that they should have detected; false positives are reported as defects, but aren’t actually defects. 

### Defects, Root Causes and Effects

The root causes of defects are the earliest actions or conditions that contributed to creating the defects. Defects can be analyzed to identify their root causes, so as to reduce the occurrence of similar defects in the future. By focusing on the most significant root causes, root cause analysis can lead to process improvements that prevent a significant number of future defects from being introduced.

For example, suppose incorrect interest payments, due to a single line of incorrect code, result in customer complaints. The defective code was written for a user story which was ambiguous, due to the product owner’s misunderstanding of how to calculate interest. If a large percentage of defects exist in interest calculations, and these defects have their root cause in similar misunderstandings, the product owners could be trained in the topic of interest calculations to reduce such defects in the future.

In this example, the customer complaints are effects. The incorrect interest payments are failures. The improper calculation in the code is a defect, and it resulted from the original defect, the ambiguity in the user story. The root cause of the original defect was a lack of knowledge on the part of the product owner, which resulted in the product owner making an error while writing the user story. The process of root
cause analysis is discussed in ISTQB-CTEL-TM and ISTQB-CTEL-ITP. 

## Seven Testing Principles {#seven-testing-principles}

A number of testing principles have been suggested over the past 50 years and offer general guidelines common for all testing.  
  
#. **Testing shows the presence of defects, not their absence:**
  Testing can show that defects are present, but cannot prove that there are no defects. Testing reduces the probability of undiscovered defects remaining in the software but, even if no defects are found, testing is not a proof of correctness.  
#. **Exhaustive testing is impossible:**
  Testing everything (all combinations of inputs and preconditions) is not feasible except for trivial cases. Rather than attempting to test exhaustively, risk analysis, test techniques, and priorities should be used to focus test efforts.  
#. **Early testing saves time and money:**
  To find defects early, both static and dynamic test activities should be started as early as possible in the software development lifecycle. Early testing is sometimes referred to as shift left. Testing early in the software development lifecycle helps reduce or eliminate costly changes (see section 3.1).  
#. **Defects cluster together:**
  A small number of modules usually contains most of the defects discovered during pre-release testing, or is responsible for most of the operational failures. Predicted defect clusters, and the actual observed defect clusters in test or operation, are an important input into a risk analysis used to focus the test effort (as mentioned in principle 2).  
#. **Beware of the pesticide paradox:**
  If the same tests are repeated over and over again, eventually these tests no longer find any new defects. To detect new defects, existing tests and test data may need changing, and new tests may need to be written. (Tests are no longer effective at finding defects, just as pesticides are no longer effective at killing insects after a while.) In some cases, such as automated regression testing, the pesticide paradox has a beneficial outcome, which is the relatively low number of regression defects.  
#. **Testing is context dependent:**
  Testing is done differently in different contexts. For example, safety-critical industrial control software is tested differently from an e-commerce mobile app. As another example, testing in an Agile project is done differently than testing in a sequential software development lifecycle project (see section 2.1).  
#. **Absence-of-errors is a fallacy:**
  Some organizations expect that testers can run all possible tests and find all possible defects, but principles 2 and 1, respectively, tell us that this is impossible. Further, it is a fallacy (i.e., a mistaken belief) to expect that just finding and fixing a large number of defects will ensure the success of a system. For example, thoroughly testing all specified requirements and fixing all defects found could still produce a system that is difficult to use, that does not fulfill the users’ needs and expectations, or that is inferior compared to other competing systems.  
  
See Myers 2011, Kaner 2002, Weinberg 2008, and Beizer 1990 for examples of these and other testing principles. 
