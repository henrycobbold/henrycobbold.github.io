---
title: "Final Year Dissertation"
date: 2019-08-14
tags: [dissertation, major project, usability, testing, prototype]
header:
  #image:
excerpt: "Prototype Application, UXD, Usability Testing"
# mathjax: "true" UNCOMMENT THIS IF USING ALGEBRAIC EXPRESSION
---

# Introduction

Developed a prototype mobile application for Great Western Railway's (GWR) maintenance division in partnership with the engineering team at Laira train depot in Plymouth to help digitalise and support their Just-In-Time (JIT) provision of tools and equipment for maintenance work on Intercity 125 trains. This project involved repeated requirement gathering, wireframing, heuristic evaluation and user testing before final prototype development within the academic time frame.

Working closely with Great Western Railway (GWR) on a Just-in-Time component and maintenance tool with an on-site team in Plymouth really challenged and motivated me. I believe that building a strong relationship with this customer was an important step towards developing a viable prototype product.

The JIT theory is based on the concept that an efficient flow of materials provides greater agility, responsiveness and reduced costs.

*“We got the idea of viewing the earlier process in a production line as a kind of store. The later process (customer) goes to the earlier process (supermarket) to acquire the needed parts (commodities) at the time and in the quantity needed. The earlier process immediately produces the quantity just taken (re-stocking the shelves)”* [14],[26].


Below is a brief discussion of the different steps of the project with particular notes of interest and comment.

## Usability

*“The extent to which a system, product or service can be used by specified users to achieve specified goals with effectiveness, efficiency and satisfaction in a specified context of use”* [65],[77],[84]

It is widely documented that "useable" software fulfils a range of qualities. This can be seen in Morville's honeycomb, a useful metric for evaluating a product [95].

<img src="{{ site.url }}{{ site.baseurl }}/images/morville_honeycomb.jpg" alt="linearly separable data">

## Development Methodology

The development methodology selected for the project was feature-driven development, one of the most popular agile methods. This framework aims to construct the feature list into feature sets containing client-valued product functionality. By then assigning the design and development of each feature set to a particular group or individual for construction working software takes precedence.
<img src="{{ site.url }}{{ site.baseurl }}/images/FDD_method.png" alt="linearly separable data">

The value of this method in this project scenario can be seen below in the following table.

<img src="{{ site.url }}{{ site.baseurl }}/images/fdd_methodology_traits.png" alt="linearly separable data">

The flow diagram below shows in more detail how the impact of project deadlines in integral to this Agile method. By concentrating on prioritised (MoSCoW) software feature sets the most important features are delivered first - those that are less significant can be developed if time allows.

<img src="{{ site.url }}{{ site.baseurl }}/images/FDD_Iteration_Element.png" alt="linearly separable data">
## Requirement Gathering, Understanding Users and Feature Prioritisation

The initial requirement gathering process is one of the crucial tasks associated with the development of a new IT product or service. In contact with a team of engineers at Laira Maintenance Facility, I was able understand the current processes and systems used to order, store and allocate resources to rail vehicles (HST power cars and trailer stock).

A range of system requirements were noted during this process over several visits which involved access to internal documents and discussion sheets. Whilst this is a publicly accessible portfolio of work, these communications will not be made public (and any reference to content within these later in the project will be blanked)

On collection of requirements these can be prioritised in accordance to the popular MoSCoW framework. This format places each requirement against its appropriate level of system importance - in this scenario features in this structure have been separated further by system attribute (*Usability*, *Performance*, *Features* and *Processing*)

<img src="{{ site.url }}{{ site.baseurl }}/images/MoSCoW.png" alt="linearly separable data">

This process was aided by the construction of employee personas so as to clearly understand the products various user groups.

<img src="{{ site.url }}{{ site.baseurl }}/images/Personas.png" alt="linearly separable data">

## Full-colour Interface Mock-ups

<img src="{{ site.url }}{{ site.baseurl }}/images/mockup_login.png" alt="linearly separable data">

<img src="{{ site.url }}{{ site.baseurl }}/images/mockup_main_menu.png" alt="linearly separable data">

<img src="{{ site.url }}{{ site.baseurl }}/images/mockup_search_order_schedule.png" alt="linearly separable data">

<img src="{{ site.url }}{{ site.baseurl }}/images/mockup_job_details.png" alt="linearly separable data">

<img src="{{ site.url }}{{ site.baseurl }}/images/mockup_order_details.png" alt="linearly separable data">

<img src="{{ site.url }}{{ site.baseurl }}/images/mockup_new_order.png" alt="linearly separable data">

## Database and Information Architecture Design and Development

<img src="{{ site.url }}{{ site.baseurl }}/images/blanked_UML.png" alt="linearly separable data">

This architecture is similar then referenced in a database entity relationship diagram, only part of which is depicted to illustrate the similarities and differences between database and class-based system models.

<img src="{{ site.url }}{{ site.baseurl }}/images/database_ERD.png" alt="linearly separable data">

sql code block:
```sql
 Order_ID [INT] IDENTITY(1,1) NOT NULL CONSTRAINT PK_Order_ID PRIMARY KEY,
```

sql code block:
```sql
DBCC CHECKIDENT ('Maintenance_Job', RESEED, 0); GO
```

The database with the above schema was created in SQL - extracts of which are shown below including table creation and population

Creating a central table:
```sql
CREATE TABLE Maintenance_Job(
	  Job_ID [INT] IDENTITY(1,1) NOT NULL CONSTRAINT PK_Job_ID PRIMARY KEY,
    Job_Vehicle_No VARCHAR(5) NOT NULL, FOREIGN KEY (Job_Vehicle_No) REFERENCES Vehicle(Vehicle_TOPS_ID),
    Vice_Vehicle_No VARCHAR(5), FOREIGN KEY (Vice_Vehicle_No) REFERENCES Vehicle(Vehicle_TOPS_ID),
    Depot CHAR(2) NOT NULL, FOREIGN KEY (Depot) REFERENCES Depot(Depot_ID),
	  Vehicle_Due_Stop_DateTime DATETIME, --nullable: vehicle stop could be corrective/unplanned
    Vehicle_Act_Stop_DateTime DATETIME, --nullable: vehicle might not actually stop for maintenance as scheduled
    Exam_Due_Start_DateTime DATETIME, --nullable: vehicle stop could be corrective/unplanned w/ no due start
    Exam_Act_Start_DateTime DATETIME, --nullable: vehicle might not actually stop for maintenance w/ no actual start date
    Exam_Due_End_DateTime DATETIME, --nullable: vehicle stop could be corrective w/ no anticipated end date
    Exam_Act_End_DateTime DATETIME, --nullable: vehicle might not actually stop for maintenance w/ no actual end date
    Vehicle_Due_Return_DateTime DATETIME, --might be no due return date
    Vehicle_Act_Return_DateTime DATETIME, --nullable: vehicle might not actually stop for maintenance
    Total_Job_Hours DEC(4,1) NOT NULL, --'0' if not undertaken. Only includes work times, not total vehicle stop time
    Staff_Signed_Off INT NOT NULL, FOREIGN KEY (Staff_Signed_Off) REFERENCES Staff(Staff_ID),
    Signed_Off_DateTime DATETIME NOT NULL, --must have a signed off date, even if maintenance didn't occur
    Staff_Approved_Job INT NOT NULL, FOREIGN KEY (Staff_Approved_Job) REFERENCES Staff(Staff_ID),
    Job_Comments VARCHAR(MAX), --comments field
    CONSTRAINT CHK_Vehicle_Swap
        CHECK(Vice_Vehicle_No != Job_Vehicle_No), /*check added to FK fields to ensure vehicle IDs are not the same,
        must be different vehicle going out (if a vehicle is returning after maintenance)*/
);
```

Populating a central table:
```sql
/* A Exam */ INSERT INTO Maintenance_Job (Job_Vehicle_No, Vice_Vehicle_No, Depot, Vehicle_Due_Stop_DateTime, Vehicle_Act_Stop_DateTime, Exam_Due_Start_DateTime, Exam_Act_Start_DateTime, Exam_Due_End_DateTime, Exam_Act_End_DateTime, Vehicle_Due_Return_DateTime, Vehicle_Act_Return_DateTime, Total_Job_Hours, Staff_Signed_Off, Signed_Off_DateTime, Staff_Approved_Job, Job_Comments) VALUES ('43010', '43196', 'LA', '26-Oct-2018 02:00', '25-Mar-2018 11:00', '26-Mar-2018 15:00', '26-Mar-2018 09:00', '26-Mar-2018 00:00', '26-Mar-2018 11:00', '27-Mar-2018 02:00', '27-March-2018 02:00', '7.5', 9, '26-Mar-2018 00:00', 13, null);
/* Corrective Job */ INSERT INTO Maintenance_Job (Job_Vehicle_No, Vice_Vehicle_No, Depot, Vehicle_Due_Stop_DateTime, Vehicle_Act_Stop_DateTime, Exam_Due_Start_DateTime, Exam_Act_Start_DateTime, Exam_Due_End_DateTime, Exam_Act_End_DateTime, Vehicle_Due_Return_DateTime, Vehicle_Act_Return_DateTime, Total_Job_Hours, Staff_Signed_Off, Signed_Off_DateTime, Staff_Approved_Job, Job_Comments) VALUES ('43140', '43087', 'LA', null, '26-Mar-2018 22:00', null, '27-Mar-2018 02:00', null, '27-Mar-2018 12:00', null, '27-Mar-2018 17:30', '5.5', 1, '27-Mar-2018 19:25', 12, null);
/* C4 Exam */ INSERT INTO Maintenance_Job (Job_Vehicle_No, Vice_Vehicle_No, Depot, Vehicle_Due_Stop_DateTime, Vehicle_Act_Stop_DateTime, Exam_Due_Start_DateTime, Exam_Act_Start_DateTime, Exam_Due_End_DateTime, Exam_Act_End_DateTime, Vehicle_Due_Return_DateTime, Vehicle_Act_Return_DateTime, Total_Job_Hours, Staff_Signed_Off, Signed_Off_DateTime, Staff_Approved_Job, Job_Comments) VALUES ('42092', '42067', 'LA', '25-Mar-2018 19:00', '25-Mar-2018 03:00', '25-Mar-2018 22:30', '25-Mar-2018 04:00', '29-Mar-2018 22:00', '29-Mar-2018 19:30', '29-Mar-2018 22:30', '30-Mar-2018 05:15', '190', 6, '29-Mar-2018 20:00', 2, 'C4 Exam + T/T + Vestibule A door 1 reported sticking repaired');
);
```

a single database audit table can be used to record DDL actions performed by database users, as shown below in this solution originally presented by
Jack Worthen [178].

```sql
CREATE TABLE WholeSystemLog(
    LogID [INT] IDENTITY(1,1) NOT NULL CONSTRAINT Pk_Log_ID PRIMARY KEY, --unique ID for each change in a database contents
    DatabaseName VARCHAR(256) NOT NULL, --in which db did this change occur?
    EventType VARCHAR(50) NOT NULL, --"ADD / ALTER / DROP" then type [_procedure/table/function/view]
    ObjectName VARCHAR(256) NOT NULL, --procedure name, table name, function name or view name
    ObjectType VARCHAR(25) NOT NULL, --its either a procedure, table, function, view
    TSQLCommand VARCHAR(MAX) NOT NULL, --copies in the code that was ran, (MAX) size of up to 2GB rather than 256
    EventDateTime DATETIME NOT NULL CONSTRAINT Df_Events_Log_GetDateTime DEFAULT (GetDate()), --type of eventTime is DateTime, set 'GetDate()' as field format
    LoginName VARCHAR(256) NOT NULL --database user running tsqlcommand
);
```

The integrity of this table can be tested by executing a DDL action, in this scenario an 'ALTER_TABLE' statement, to ensure the event type is recorded along with the target object name (table name), DATETIME of SQL execution and the associated login name.

```sql
ALTER TABLE Job_Order ADD Order_AcceptedDateTime DATETIME;
```

A simple 'SELECT (all)' statement is used to return all the entries in the log table.

```sql
SELECT * FROM WholeSystemLog WHERE EventType = 'ALTER_TABLE'
```

## Interface Development

<img src="{{ site.url }}{{ site.baseurl }}/images/finaldesign_main_menu.png" alt="linearly separable data">

In numerous places the limited development options restricted the changes available to me when I performed the cognitive walkthrough. For this reason, I look back on the project with some mixed emotions. The form-based structure provided by *Appenate* was certainly what I was looking to achieve, but elements of its built-in functionality provided challenges which were difficult to overcome and created a disparity between the initial wireframes and the first prototype system.

Although the prototype was destined for an iPad screen size most screen views were taken from an iPhone (SE).

Edit an existing record or create new

<img src="{{ site.url }}{{ site.baseurl }}/images/finaldesign_create_new_order.png" alt="linearly separable data">

Order details page

<img src="{{ site.url }}{{ site.baseurl }}/images/finaldesign_order_details.png" alt="linearly separable data">

Searchable checkboxes allowing a user to view two product IDs contained in an existing component order (Order "12").

<img src="{{ site.url }}{{ site.baseurl }}/images/finaldesign_search_order_schedule.png" alt="linearly separable data">

Changes made to records in this application are contained locally and placed in "Saved Entries" before they can be pushed back to the Appenate server.

<img src="{{ site.url }}{{ site.baseurl }}/images/finaldesign_saved_changes.png" alt="linearly separable data">

A view of several controls clearly identified in the wireframe design stage:

<img src="{{ site.url }}{{ site.baseurl }}/images/finaldesign_picker_control.png" alt="linearly separable data">

<img src="{{ site.url }}{{ site.baseurl }}/images/finaldesign_text_control.png" alt="linearly separable data">

## Cognitive Walkthrough

For each Personas associated User Story a walkthrough of the steps required to fulfil the user’s goal can now be performed. This is often performed before user testing so as to “clean up” the interface of fundamental design errors, such as missing control buttons or navigational inconsistencies. This process will help to make subsequent user testing more successful as it will help to allow *“users [to] focus on the experience of pursuing their goals”* [181] during task-based user tests.

This understanding can be gained by asking four questions of a user at any location in the system:

Q1: Does the user know what needs to be done? Is the user aware of what they want or need to do? [183],[184]
Q2: Can the user see a control to do that? Is there anything visible that the user feels can help them perform this action? [183],[184]
Q3: Is it obvious how the control works? Is it clear how the on-screen visual should be used to achieve successful interaction? [183]
Q4: Does the user understand the feedback they have been given? Can the user make sense of the outcome of the system interaction? [183],[184]

<img src="{{ site.url }}{{ site.baseurl }}/images/cognitive_walkthrough_tables.png" alt="linearly separable data">

Having evaluated these initial wireframe designs from a developer-perspective, a series of changes were required to ensure that the colour-wireframes passed this evaluation stage. The next step is to then to understand how users react to, and perform, tasks in these preliminary designs. To do this usability test scripts were key.

To quickly and efficiently gather both qualitative and quantitative data Brooke's *"quick and dirty"* 'System Usability Scale' [186] was used alongside the universally popular Krug [187],[191] framework - devised and refined by Steve Krug.

Below shows the format of the Krug script, a popular and highly adaptable framework for user-based testing of which a considerable number of professionals have adopted and manipulated over time.

<img src="{{ site.url }}{{ site.baseurl }}/images/krug_intro.png" alt="linearly separable data">

<img src="{{ site.url }}{{ site.baseurl }}/images/krug_intro_1.png" alt="linearly separable data">

<img src="{{ site.url }}{{ site.baseurl }}/images/krug_homepage.png" alt="linearly separable data">

<img src="{{ site.url }}{{ site.baseurl }}/images/krug_user_test.png" alt="linearly separable data">


These printed scripts were used by the interviewer to note down the key outcomes of the testing, a task aided by screen capture software, as seen below in this capture of one such interview. For this scenario 'Silverback' for OSX was ideal.

<img src="{{ site.url }}{{ site.baseurl }}/images/silverback_recording_example.png" alt="linearly separable data">

At the end of the process a test user was invited to complete the SUS form, as well as talk the interviewer through the supporting reasons. One filled form is illustrated below.

<img src="{{ site.url }}{{ site.baseurl }}/images/brookes_SUS_form.png" alt="linearly separable data">

In this scale a score of usability is calculated with the contribution of questions 1/3/5/7/9 the scale position indicated minus one. Questions 2/4/6/8/10 carrying forward a score 5 minus that indicated by the test subject on the form. The sum of the 10 fields are then totalled and multiplied by 2.5 to provide a score out of 100. 68 or above is suggested to represent above average system usability [186].

This combination of soft user opinion and harder statistical data can now be more systematically documented in order to clearly identify the important trends experienced during the user testing; a process eased with access to the screen capture and microphone for reference.

For this process I used a simple report format, as illustrated below.

<img src="{{ site.url }}{{ site.baseurl }}/images/formal_test_documentation.png" alt="linearly separable data">





### Work(s) used in project summary

[65] F. Nayebi, J.-M. Desharnais, and A. Abran, “The state of the art mobile application usability evaluation,” in *2012 25th IEEE Canadian Conference on Electrical and Computer Engineering (CCECE)*, 2012, pp. 1–4.

[77] International Organisation for Standardisation (ISO), “Ergonomics of human-system interaction - Part 11: Usability: Definitions and Concepts,” Geneva, Switzerland, 2018.

[84] N. Bevan and M. Macleod, “Usability measurement in context,” *Behav. Inf. Technol.*, vol. 13, no. 1, pp. 132–145, 1994.

[14] W. J. Hopp and M. L. Spearman, “To Pull or Not to Pull: What Is the Question?,” *Manuf. Serv. Oper. Manag.*, vol. 6, no. 2, pp. 133–148, 2004.

[26] T. Ohno, *Toyota Production System, Beyond Large Scale Production Systems.* Cambridge, MA:
Productivity Press, 1988.

[95] P. Morville, “User Experience Design,” *Semantic Studios*, 2004. [Online]. Available: https://semanticstudios.com/user_experience_design/. [Accessed: 18-Dec-2018].

[178] J. Worthen, “Creating A Log Table To Track Changes To Database Objects In SQL Server,” *SQL Server*, 2018. [Online]. Available: https://jackworthen.com/2018/03/19/creating-a-log-table- to-track-changes-to-database-objects-in-sql-server/. [Accessed: 15-Mar-2019].

[181] C. M. Barnum, *Usability Testing Essentials: Ready, Set... Test!,* 1st ed. Burlington, MA: Morgan Kaufmann, 2010.

[183] N. E. Jacobsen and B. E. John, “Two Case Studies in Using Cognitive Walkthrough for Interface Evaluation,” in *CMU-CS-00-132*, 2000.

[184] M. H. Blackmon, *Cognitive Walkthrough Cognitive Walkthrough Methodology*, vol. 1. Great Barrington, MA: Berkshire Publishing Group, 2004.

[186] J. Brooke, “SUS - A quick and dirty usability scale,” *Smart Phone Appl. People with Brain Inj.*, vol. Smart phon, pp. 1–8, 2011.

[187] S. Krug, *Rocket surgery made easy: The do-it-yourself guide to finding and fixing usability problems*, 1st ed. Berkeley, CA: New Riders, 2010.

[191] S. Krug, *Don’t make me think, revisited: a common sense approach to Web usability*, 3rd ed. San Francisco, CA: New Riders, 2014.


<!--

COMMENTED OUT SECTION WHEN REQUIRED THAT CONTAINS ALL FORMATTING SYNTAX NEEDED:

## H2 Heading

### H3 Heading

Here's some basic text.

And here's some *italics*

Here's some **bold** text.

What about a [link](https://github.com/dataoptimal)?

Here's a bulleted list:
* First item
+ Second item
- Third item

Here's a numbered list:
1. First
2. Second
3. Third

Python code block:
```python
    import numpy as np

    def test_function(x, y):
      z = np.sum(x,y)
      return z
```

R code block:
```r
library(tidyverse)
df <- read_csv("some_file.csv")
head(df)
```

Here's some inline code `x+y`.

Here's an image:
<img src="{{ site.url }}{{ site.baseurl }}/images/perceptron/linsep.jpg" alt="linearly separable data">

Here's another image using Kramdown:
![alt]({{ site.url }}{{ site.baseurl }}/images/perceptron/linsep.jpg)

Here's some math:

$$z=x+y$$

You can also put it inline $$z=x+y$$ -->
