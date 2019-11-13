---
title: "UXD - Prototype Campus Companion App"
date: 2019-09-03
tags: [Processes, Steps, Responsibilities, UX, Interaction Design]
header:
  image: #no header image
excerpt: "Discussion, UXD, Usability, Interaction Design, Evaluation, Responsibilities"
---

# Introduction

Roto, Rantavuo and Väänänen-Vainio-Mattila [1] suggest that a high degree of user experience (UX henceforth) satisfaction “comes from the value and meaning of the product concept itself” [1], a deeper-routed notion than UI that concentrates on a “means of interact[ion]” [1]. Despite this clear separation they are inexplicably linked, an idea that can be clearly seen in the case of the existing UWTSD website, an evaluation of which will help design a campus application for students of the FACE faculty that provides a quality user experience by fulfilling the diverse motivations of Computing, Engineering and Architecture students of various ages and technical proficiency within the SA1 Campus.

## Requirement Gathering and User Research

The process of re-designing a system used by such a diverse audience presents several key challenges, ideologies that traditional, developer-centric methodologies can struggle to provide. As such a paradigm, the User- Centred Design [2] (UCD hereafter) is of genuine value given its nature of “structure[ing] the development process around users and their practises” [2]. It is suggested by Tidwell [3] that “users and clients typically speak to you in terms of desired features and solutions, not of needs and problems” that they currently experiencing. However, this statement for this scenario could be considered slightly misleading thanks to the specialised nature of one target user group. By developing an application for FACE students, within which Computing students make up a noteworthy percentage, several individuals have expressed their requirements not as idyllic features, but as precise solutions to niche problems that they are currently experiencing.

There are various requirement gathering approaches used to help tease out the feature’s user groups want in a new digital product or service. In some design scenario’s, such as the development of entirely new systems, the use of extreme characters can be used [4]. This concept of developing grossly over-exaggerated user personas adds extra burden on the design and development team(s), a dynamic that works in the designers favour insomuch as software solutions produced, albeit unlikely to fulfil the needs of an “exaggerated personality” [4] that is unlikely to ever use the platform, is more likely to fulfil the needs of the far more representative user groups. The idea of defining highly precise user personas provides added complications on the developer, aimed at helping to improve the decisions made in the design of an application for all user groups [4] as a designer is trying to develop a single interaction and reduce the likelihood of user mistakes occurring on their path to goal realisation.

### Focus Groups and Brainstorming

The exercise of brainstorming is of value given its capacity to generate new ideas, especially when this group activity includes potential users from a range of different backgrounds, such as course, faculty or level of study as throwing ideas into a central ‘melting pot’ can bring up functionality, or even specific design elements [5]. This is particularly powerful as “the most creative or effective ideas often result from combining seemingly unrelated ideas” [5], formulating unusual or original suggestions. Caution here is advised however as a brainstorming process should also highlight features that are not of primary interest to those in a particular group.
This process, taking the form of an informal discussion driven by the question and response sheet, has been handed to individuals as a requirement gathering sheet, and undertaken as a group with several participants concurrently.

<img src="{{ site.url }}{{ site.baseurl }}/images/mono_campus_app_wireframes/app_req_sheet.png" alt="linearly separable data">

<img src="{{ site.url }}{{ site.baseurl }}/images/mono_campus_app_wireframes/app_req_sheet_2.png" alt="linearly separable data">

Having collected the thoughts and opinions of several FACE students some key trends can be highlighted that must be considered in the development of initial wireframe designs. These are discussed below in the same order as raised on the requirement gathering forms.

1. Understanding Current Software Usage

Several respondents that completed the first requirements elicitations survey highlighted specialist software for their course that they currently use, such as “Visual Studio Enterprise and “Proteus”, whilst those that filled out the revised form generally noted more generic, wider software related to their University life such as the Microsoft package and Mendeley referencing software. From this it can be deduced that the ability to access core software, be it for download or license keys, and more niche course related packages need to be available in an application aimed at providing students with their software tools for study. This slight variation was only seen in several respondents where respondents listed just core module software--that was considered by one  student “compulsory for the course” [male, 29].

2. Assessing the Existing University Website

This question was included so that an understanding could be gained on existing issues with the university website and help identify elements that should be improved in a streamlined campus application. By asking an individual what they like and dislike in the current website, and importantly why, the designers can pay close attention to ensuring they are central to a new application. Several of the survey group highlighted the “Quick Links” page as something that they liked about the existing site because it they felt that it helped them “navigate to the relevant pages faster” [male, 26]. Alongside broad design elements there were precise user problems such as the fact it “doesn’t keep you logged in” [male, 26] and with the same individual believing that this made the logging in process “cumbersome”. Interestingly however that was the only real criticism received by this person about the university site, suggesting that overall it “combines into a good user experience”.
Others highlighted far more obvious issues such as the number of pages and complexity of the site, so much so by one student he had no complaints about the system because he does not use it enough to properly comment – instead bookmarking every core page he regularly. Another raised the point that some navigation was broken or incorrectly linked, simply refreshing the existing page. Others had issues with colour and design continuity, an element of relative importance in developing a useful and credible app for students.

3. Potential of a Campus App

The general response to the question, “Would you be interested in a companion app” was positive with most students stating that they liked the idea, and most, when asked about some primary features listed platforms and sites that are central to a student’s day at University such as Email, Moodle and the library. Particular reference was made to the access of software and academic journal resources by several students, with one individual stressing the need for ‘search’ functionality for the library resources. The responses here clearly show how the study participants value tools that are integral to daily study. Of interest two people raised the issue of adverts. Given the nature of university software this would not be likely but illustrates how students in some cases could have applied their own experiences of other applications to this scenario.
Overall the need for a streamlined and uncluttered program was shared by most correspondents who said the app should be clear, easy to navigate and only show the most relevant information; two fundamental objectives of the proposed system if it is to be considered useful and valuable.

### Developing User Personas

By accurately understanding how a user aims to use a system a developer can more clearly evaluate the suitability of mock-up screen designs [6],[7] with Microsoft believing that using user personas have helped to “make our assumptions about the target audience more explicit” [8]. In this scenario it is anticipated that the campus companion application will be used primarily by FACE students that study in the Swansea SA1 campus but, given the diverse nature of ‘students’ and individuals studying an array of courses across various sites such an application should be designed in such a way that it is open to extendibility. For the purpose of this application the target user groups all study a FACE course, but the same format of user persona could be developed for a student studying at another campus in Swansea, or in Carmarthen or Lampeter.

<img src="{{ site.url }}{{ site.baseurl }}/images/mono_campus_app_wireframes/face_app_persona.png" alt="linearly separable data">

<img src="{{ site.url }}{{ site.baseurl }}/images/mono_campus_app_wireframes/face_app_persona_2.png" alt="linearly separable data">

<img src="{{ site.url }}{{ site.baseurl }}/images/mono_campus_app_wireframes/face_app_persona2.png" alt="linearly separable data">

<img src="{{ site.url }}{{ site.baseurl }}/images/mono_campus_app_wireframes/face_app_persona2_2.png" alt="linearly separable data">

### User Stories

User stories typically take place after a range of example users have been documented. The purpose of this activity is to be aware of how a given user could wish to interact with the system being developed and crucially how an individual’s goals, use of devices and potential frustrations help the developer design the configuration of system information [9]. Given the sometimes ‘fuzzy’ nature of a user’s perspective on a system this process does not
concentrate on how a developer should solve design quandaries, just that they need considering in the new or revised system. The purpose of a scenario is to “concretely describe” [10] the use of a system, allowing the development team to attempt to most closely replicate the route that users take in a system to achieve a certain outcome. This “essence of an interaction design” takes an individual and creates a narrative in which the users, often identified in a physical state, describe and demonstrate their motivations, actions, current understanding and controls and/or interfaces that they “encounter and manipulate” [10] during this journey; often following the follow format:

“As a *<type of user>* I want to *<some goal>* so that *<some action>*” [11]

A user story can now be developed for each persona identified above, outlining the mental and physical processes involves with completing a task that is appropriate for the activities associated with that individual.

--
*Ollie has arrived in University at 8:30 on a Tuesday morning and has a morning free of lectures. He is in early so as to continue with assignments that he has to hand in later in the month, so is looking for somewhere quiet to study in peace. He finds a space in the library and decides he first wants to open a PowerPoint presentation from one of lectures yesterday to pick up the notes from where he left off. He logs on to his Windows laptop and firstly opens his preferred browser, Chrome. In the URL bar he enters the following link, https://moodle.uwtsd.ac.uk so as to go to Moodle without using the University website at all. He has been doing this for the last 1 and a half years because he quickly learnt this link. Now Ollie is presented with the Moodle login page where he sees that he must log in to his university IT account. He duly completes his details with his ‘P’ number and password, clicking ‘Log In’ when complete. With success his is now shown the main Moodle page with this year’s module tiles arranged underneath a bar of other primary university links, such as Email and MyTSD. Ollie scrolls downwards to find the module he desires, Database Management Systems in this case, clicking on the tile to open it up. Once inside the module he scrolls downwards again to select the correct lecture notes to view – expanding the tile and clicking on the PowerPoint file to download it to his machine. As he keeps local backups of each week’s content, he wishes to save the file to his OneDrive, and so navigates to the corresponding folder in the “Save to” file explorer window. He clicks save when in the correct directory and minimises Moodle and the browser window so as to view the PowerPoint file – duly continuing with his note taking.*
--

## Information Architecture

The Information architecture is of utmost significance in the development of software applications as it shapes the design and development of subsequent software components and front-end interfaces used, the latter an element of software that a user will ultimately interact with [12]. As such, user displeasure at being unable to find the desired information is aimed, commonly, at its ‘invisible’ composition [12]. The information architecture used in this application is relatively shallow because of the number of clicks required to access the desired information [13]. One of the primary issues with the existing website is the complexity of its information architecture and the number of menus, sub-menus and corresponding clicks necessary to access certain pages, especially those related to lecturer contact information which is particularly deep despite the fundamental need students and other lecturers have to find this information.

The structure of this system is polyhierarchical [13] for the reason that it accommodates the multi-route nature of mobile application use. In many instances’ users expect to be able to access certain menus from various, or in some instances, any given page - user settings being a prime example. The concept of ‘everything in 3 clicks’ has traditionally been a fundamental design rule but is often very difficult to maintain, instead helping to raise the importance of a “comfortable path” [13] whereby users can clearly understand and evaluate the demands of the interaction [13], a now standard approach to design problems. An all-encompassing definition of information architecture is offered by Rosenfeld, Morville and Arango [12] as:

“The synthesis of organisation, labelling, search and navigation systems within digital, physical and cross-channel systems” [12].

Rosenfeld, Morville and Arango justify their reference of several definitions highlighting the incredibly diverse nature of information structures that underpin “digital products and services” [12]. Alternatively the Information Architecture Institute (IAA) have simplified this possible definition down to “The structural design of shared information environments” [14]. In terms of the scope of information architecture its composition is widely understood to revolve around three main components “Users”, “Content” and Context” [12]. This principle is seen in the IA Venn diagram, shown below, which illustrates how an information architecture is directly influenced by how the various facets interact with each other, a factor clearly seen in development of the university website as the focus of the main homepage is clearly centred towards promoting the establishment with less focus on providing easy access to student software services.

<img src="{{ site.url }}{{ site.baseurl }}/images/information_architecture_venn_diagram.png" alt="linearly separable data">


The task facing many systems is the need to develop an information architecture that provides a “foundation for rapid response” [15] and the continual change of digital platforms today. This element of flexibility has a reduced significance in the development of a campus companion app thanks to the relatively rigid nature of core student platforms and services that are unlikely to change on a regular basis. Below a possible IA structure is presented.

<img src="{{ site.url }}{{ site.baseurl }}/images/example_app_information_architecture.png" alt="linearly separable data">

## Interface Designs

### Learning Lessons from the existing UWTSD sites

Before offering conceivable mobile device designs it is important to first inspect existing interface designs. Evaluating the UWTSD University website highlights several key interface design elements that a new mobile-based platform should avoid in order to offer a suitable experience for students on and off-campus.

1. The menu structure is inconsistently arranged and displayed from a from hierarchical and design perspectives respectively. The use of two top menu bars, the primary one for current student resources being ‘Quick Links’, is far from prominent and located directly above the primary page menu. The on- site resources students use rely on, such as Moodle and student email, will need to be central in the mobile application design in order to provide easy access to core services used frequently by staff and students alike.

2. The existing website concentrates heavily on advertising the university to new students. A suitable mobile application for current students on campus will not need to include as much information on the university and its courses. A good application should include options to search and view course, faculty and staff information, but this functionality should not be considered a primary goal of a user.

3. In the adjusted UWTSD website below the Welsh language option is of considerable value but could benefit from added visibility and centrality. The option to view the site and its content in Welsh should also be of considerable note for a campus companion app.

Below a reworked version of the current UWTSD website is shown, created in Balsamiq. This is a nice lightweight wireframing tool that allows speedy interface mockups.

<img src="{{ site.url }}{{ site.baseurl }}/images/mono_campus_app_wireframes/Reworked_existing_UWTSD_website.png" alt="linearly separable data">

## Wireframe designs

*i. For the purposes of this design process the mobile device used is the iPhone X/10 screen size. this screen size has been selected to represent a ‘typical’ mobile device.*

*ii. Currently stand-alone mobile applications already exist for Moodle, Outlook and OneDrive but it is assumed that the companion app will integrate these, as illustrated below, to avoid the need to install each individual app.*

*iii. Where controls appear below the bottom of the screen a downwards scroll is inferred.*

*--splasher screen--*
<img src="{{ site.url }}{{ site.baseurl }}/images/mono_campus_app_wireframes/splasher_screen.png" alt="linearly separable data">

*--sign in screen--*
<img src="{{ site.url }}{{ site.baseurl }}/images/mono_campus_app_wireframes/sign_in_screen.png.png" alt="linearly separable data">

*-sign in screen--*
<img src="{{ site.url }}{{ site.baseurl }}/images/mono_campus_app_wireframes/sign_in_screen_copy.png" alt="linearly separable data">

*--enable touch id to sign in--*
<img src="{{ site.url }}{{ site.baseurl }}/images/mono_campus_app_wireframes/sign_in_(w_touch_id).png" alt="linearly separable data">

*--main app menu--*
<img src="{{ site.url }}{{ site.baseurl }}/images/mono_campus_app_wireframes/main_menu.png" alt="linearly separable data">

*--moodle menu--*
<img src="{{ site.url }}{{ site.baseurl }}/images/mono_campus_app_wireframes/moodle_menu.png" alt="linearly separable data">

*--module view--*
<img src="{{ site.url }}{{ site.baseurl }}/images/mono_campus_app_wireframes/module_view.png" alt="linearly separable data">

*--my programs and app integration menu--*
<img src="{{ site.url }}{{ site.baseurl }}/images/mono_campus_app_wireframes/my_programs_menu.png" alt="linearly separable data">

*--library menu--*
<img src="{{ site.url }}{{ site.baseurl }}/images/mono_campus_app_wireframes/library_menu.png" alt="linearly separable data">

*--print menu--*
<img src="{{ site.url }}{{ site.baseurl }}/images/mono_campus_app_wireframes/print_menu.png" alt="linearly separable data">

*--TSDSU menu--*
<img src="{{ site.url }}{{ site.baseurl }}/images/mono_campus_app_wireframes/tsdsu_menu.png" alt="linearly separable data">

A new system should be intuitive to use, an important attribute to respect when designing an application to help streamline life on and off campus for FACE students. A piece of software can be considered intuitive if ‘the users’ subconscious application of prior knowledge leads to effective interaction” [16]. Given the day-to-day experience most students have with core software applications and platforms within university, a degree of prior understanding and knowledge can been built up over time, a stem of system understanding noted below, and categorised as a sensorimotor process as this level is described as “general knowledge” [16]. The level of student familiarity and understanding of sites such as Moodle and Outlook can also be placed in this model as a cultural influence. This can be most clearly seen in various FACE faculties as the nature of university systems used, and the beliefs associated to their usefulness will vary by faculty.

<img src="{{ site.url }}{{ site.baseurl }}/images/mono_campus_app_wireframes/intuitive_knowledge_levels.png" alt="linearly separable data">

## User Testing

To help evaluate the suitability of the application interface, the use of a user acceptance testing, typically through mediums such as evaluations and practical tasks. Whilst the latter is of importance to understand the thought process of target user groups its benefits are limited thanks to the limited nature of initial wireframe designs and the relative extent to which users can explore the initial application designs in the process of test task fulfilment so as to demonstrate “conceptual integrity”, and "underlying consistency" [17].

The use of Likert-based model, such as offered by Brooke [18], discussed at greater length in my dissertation highlights or the and illustrated in its entirety below is suitable due to the precise, distinct responses received to questions about system usability, attractiveness and continuity. As discussed in greater length in my dissertation highlights this matrix is designed to produce a single number that reflects usability.

<img src="{{ site.url }}{{ site.baseurl }}/images/mono_campus_app_wireframes/usability_evaluation_questionnaire.png" alt="linearly separable data">

Alongside this method is the far less quantifiable user testing, a valuable activity that gives an individual the space to act ‘normally’ allows them to perform in a more natural manner, meaning the results collected are more accurate of the users experience with the system [19].. This system provides users with typical system tasks to evaluate the degree of goal fulfilment, again based on Krug's [19] customisable framework, whereby users as asked questions such as *"How would you find _____?"*. Below are a series of sheets from these sessions, revised after the interview by revisiting the screen capture and microphone for any missed points.

<img src="{{ site.url }}{{ site.baseurl }}/images/mono_campus_app_wireframes/krug_script_scribbled_notes.png" alt="linearly separable data">

*Main Test Outcome(s)*

1. UWTSD internal library and external subject-specific databases were being confused
This feedback was not noted during the completion of any tasks, but as a question and comment for the interviewer when completing the exercise of quickly requesting a known book in the library.
The labelling here is therefore misleading as is and needs alteration, despite the presence of small icons which were not considered helpful in this instance.

<img src="{{ site.url }}{{ site.baseurl }}/images/mono_campus_app_wireframes/library_button_control.png" alt="linearly separable data">

2. “Search” might be being overlooked
When required to move from one flow of interaction to another very few users opted to quickly use this feature - despite its constant position in the bottom bar. One user, quickly identifying its potential discounted the functionality, suggesting such controls often “do not provide the results that I am looking for” [Male, 24]. Furthermore they suggested that an ever-present option to go “Home” instead would enable a user to quickly and easily jump back to the start and begin a new flow of interaction.

<img src="{{ site.url }}{{ site.baseurl }}/images/mono_campus_app_wireframes/search_control.png" alt="linearly separable data">

3. During the requirements gathering phase the idea of a quick request system, designed to help speed up the task of reserving a book, was generally supported. However, in this first development iteration its purpose and functionality has caused some misunderstanding and has raised a number of questions.

“Do I already need to have a book saved in order to quickly request it?” [Female, 21]
“Do I need to find the book in the app first?” [Male, 32]
“What’s quick request?” [Female, 21 and Male, 32]

Issues were also expressed with the choice of the icon here, intending to show an out-stretched hand about to receive a book one user believed “it looks like a stop or halt hand” [Female, 30].

<img src="{{ site.url }}{{ site.baseurl }}/images/mono_campus_app_wireframes/quick_request_control.png" alt="linearly separable data">

The requirement gathering and testing of a set of initial monochrome mockup wireframes designs is only the first stage of the development process. Designed to gauge the suitability of the designers initial interpretation *at least* one more iteration of requirement analysis, mockup design and user testing will be required - a process that is designed to repeat until the desired product has been produced. Part 2 of this project will revise the application and perform this second round of testing to improve the both the interfaces usefulness and user experience.

### Work(s) used in project summary

[1] V. Roto, H. Rantavuo, and K. Väänänen-Vainio-Mattila, “Evaluating User Experience of Early Product Concepts,” in *International Conference on Designing Pleasurable Products and Interfaces*, 2009, no. October, pp. 1–10.

[2] A. L. Massanari, “Designing for imaginary friends: Information architecture, personas and the politics of user-centered design,” *New Media Soc.*, vol. 12, no. 3, pp. 401–416, 2010.

[3] J. Tidwell, *Designing Interfaces*, 1st ed. Sebastopol, CA: O’Reilly Media, Inc., 2005.

[4] P. T. A. Junior and L. V. L. Filgueiras, “User modeling with personas,” in *Proceedings of CLICH’05*, 2006, pp. 277–282.

[5] R. R. Young, “Recommended Requirements Gathering Practices,” *CrossTalk J. Def. Softw. Eng.*, no. April, pp. 9–12, 2002.

[6] Y. Chang, Y. Lim, and E. Stolterman, “Personas: From Theory to Practices,” in *Proceedings: NordiCHI 2008: Using Bridges*, 2018, no. August 2015, pp. 105–114.

[7] S. Mulder and Z. Yaar, *The User is Always Right: A Practical Guide to Creating and Using Persona’s for the Web*. Berkely, CA: The New Riders, 2007.

[8] J. Pruit and J. Grudin, “Personas : Practice and Theory,” *Proc. Conf. Des. user Exp.*, pp. 1–15, 2003.

[9] J. Marsh, *UX for beginners*. Sebastapol, CA: O’Reilly, 2016.

[10] M. B. Rossen and J. M. Carroll, “Scenario-Based Design,” in *The Human-Computer Interaction Handbook: Fundamentals, Evolving Technologies and Emerging Applications*, Lawrence Erlbaum Associates, 2002, pp. 1032–1050.

[11] R. M. Chopade and N. S. Dhavase, “Agile Software Development: Positive and Negative User Stories,” in *2017 2nd International Conference for Convergence in Technology (I2CT)*, 2017.

[12] L. Rosenfeld, P. Morville, and J. Arango, *Information Architecture: For the web and beyond*, 4th ed. Sebastapol, CA: O’Reilly Media, Inc., 2015.

[13] D. Spencer, *Information Architecture*, 1st ed. Penarth, UK: Five Simple Steps, 2009.

[14] Information Architecture Institute, *What is IA?* Beverly, MA: Information Architecture Institute, 2013.

[15] B. R. Allen and A. C. Boynton, “Information Architecture: In Search of Efficient Flexibility,” *MIS Q.*, vol. 15, no. 4, pp. 435–445, 1991.

[16] J. Hurtienne and L. Blessing, “Design for Intuitive Use: Testing Image Schema Theory for User Interface Design,” in *International Conference on Engineering Design (ICED’07)*, 2007, no. August, pp. 1–12.

[17] T. Badgett, T. M. Thomas, and C. Sandler, *The Art of Software Testing*, 2nd ed. Hoboken, NJ: John Wiley & Sons, Inc., 2004.

[18] J. Brooke, “SUS - A quick and dirty usability scale,” *Smart Phone Appl. People with Brain Inj.*, vol. Smartphone, pp. 1–8, 2011.

[19] S. Krug, *Rocket surgery made easy: The do-it-yourself guide to finding and fixing usability problems*, 1st ed. Berkeley, CA: New Riders, 2010.



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
