---
title: "UXD - Prototype Campus Companion App - Part 2"
date: 2019-09-03
tags: [Processes, Steps, Responsibilities, UX, Interaction Design]
header:
  image: #no header image
excerpt: "Wireframes, User Testing, App Data, Behaviour Graph, Information Architecture, Usability Experience Questionnaire"
---

# Introduction

It is widely documented that the usability and user-experience testing process associated with new software is highly protracted. In the previous report the developer produced a series of initial designs for campus ‘companion application’ for the FACE faculty – the testing of which raised several structural and cognitive discrepancies. This report aims to fix these issues and demonstrate the application interface suitability by performing a second round of user-based testing. Having completed this process, the product can then be evaluated to understand how suitable the refined product can be considered and offer how, by means of further data collection, the application interface or information architecture could be further developed with future iterations. Full-colour mockups can now be produced and feedback gathered on the use of colour.

## Briefly recapping user-test discrepancies

<img src="{{ site.url }}{{ site.baseurl }}/images/colour_campus_app_wireframes/user_test_recap.png" alt="linearly separable data">

### Addressing interface discrepancies

Having written up these key findings the developer can then go back to extend and modify the formative wireframe designs in order to perform a second round of testing with participants from the same representative user groups. Key changes made to the interface mockups during this second iteration are outlined below.

1. "Quick Request"

A primary concern express was associated with the processes of rapidly reserving physical library resources. To correct this issue the developer believes that it was the word “Quick” that caused users to mistake the action of requesting a book for a fast, easier way of taking out a resource. For the second round of tests the developer would like to see how users respond to a “Request Book” button instead – it is expected that users will understand that this allows them to take out a library resource that they have already added to their list of saved resources by contacting their academic librarian. The revised text and icon; designed to more clearly represent a user ‘clicking’ to request an item.

<img src="{{ site.url }}{{ site.baseurl }}/images/colour_campus_app_wireframes/request_book.png" alt="linearly separable data">

2. Internal and external library repositories

The library menu also confused users when they were asked to perform tasks associated with the Universities internal library catalogue and link to external subject-specific database repositories. To ease understanding the original button layout has been altered, as shown below, to state “UWTSD” and “External” subject databases. It is expected that adaptation will more clearly convey the controls “clarity of purpose” [1] in regards to the service this button is offering.

<img src="{{ site.url }}{{ site.baseurl }}/images/colour_campus_app_wireframes/library_resource_controls.png" alt="linearly separable data">

3. Revised pinned footer actions

During tasks that involved users to move between paths of interaction participants were looking for a “Home” button. This new version of the page has removed the footer button text so that the user has the option to both “Search” and return “Home”. Several users during the first round of testing also suggested that the ability to customise this service would make the app more useful for students - allowing them to quickly access the tools and platforms that mattered to them. These changes to the footer are illustrated below.

<img src="{{ site.url }}{{ site.baseurl }}/images/colour_campus_app_wireframes/revised_footer_controls.png" alt="linearly separable data">

### Adding colour

The background colour selected is the FACE blue (#194772), text and secondary button control text in white and primary controls in the UWTSD yellow (#6FCB3D). Whilst there are minor exceptions to this theme the most notable change can be seen in the print screen. To allow users to select, remove and print files from their smartphone the screen comprises various action buttons. To ensure that these controls are universally recognisable, precise colour schemes endorsed by the Bootstrap’s web usability guidelines have been used [1]. This convention provides single shade colours for controls that represent different types of user action ranging from basic or standard system control through to the feedback colours of “success”, “warning” and “danger” [1]. The primary yellow control colour is a different, darker shade to that of a button of “btn-warning” (hex value #E59A3D)

<img src="{{ site.url }}{{ site.baseurl }}/images/colour_campus_app_wireframes/print_controls.png" alt="linearly separable data">

### Interface Mockup feedback and usability testing

### Scenario specific factors

In order to collect valuable feedback, the second round of summative evaluation must be conducted with representative system users, similar those asked during the initial testing process [2]. The following key statements reiterate the core user groups and those for which app use represents an everyday task within University; this process also re-states the features that requirements elicitation raised as most important as a way of ensuring this prototype application.

• The application is not just to be used by students on computing courses
• The engineering faculty is as large a student base as that of computing
• Architecture students also need to be considered, though they do represent a smaller population percentage.
• The age and IT skillset range in some faculties in the SA1 campus is broad – the first round of testing attempted to elicit feedback across this divide.
• The developer is aware of the needs of part-time students and post-graduate students that have different needs.

As large and as varied a sample size will be used as possible within the development timeframe to produce a broad set of test results and observation material. Turner, Lewis and Nielsen [3], based on previous works, assert that a large proportion of usability inconsistencies will be picked up by as few as three to five test subjects – as many as can be reasonably carried out in this usability analysis. Whilst time and financial capacity are considerable factors in selecting and executing user-testing activities, software-related factors have contributed to the testing of these full-colour digital interface mock-ups - as recognised by Nielsen and Landauer [4].

• The composition of the subject application. Given the lightweight, but concentrated features, this application demands extensive testing and evaluation in order to comprehensively understand its usefulness
• “Stage in the usability lifecycle the application is tested in” – “whether early in the design phase or after several iterations of test and redesign” [3]. This report documents the second development iteration and attempts to rectify known system issues.
• “The skills of the evaluator” [3]. This is key. The evaluator in this development is not a commercially experienced or UX professional but has acquired a diverse and varied testing skillset to allow ample scope for accurate testing and an insightful system evaluation.

### Testing methods

The methods used to test and evaluate a software product can be broken down into three broad areas that, whilst ensuring task rigidity and timely session progression, allows for additional evaluator exploration. To provide as comprehensive a set of test results as possible a combination of “inquiry’ [5] and “formal usability testing” [5] will be used. This structure provides a mixed balance of qualitative and quantitative methods results by means of interpretive opinion-based exploration and specific user tasks.

For the preceding wireframe evaluation process the industry-grade Krug [6] format was referenced and adapted to more capture scenario-specific data from the test participants – such as altering the initial set of user questions to understand student use of university software.
Importantly questions asked by the developer during the first set of testing can also now be further refined and re-worked to see how successful changes incorporated into the second development iteration are at rectifying usability inconsistencies. This is shown below where a test scenario has been altered to provide more clarity and see how uses react to a modified control.

<img src="{{ site.url }}{{ site.baseurl }}/images/colour_campus_app_wireframes/krug_edited_script.png" alt="linearly separable data">

If users do not specifically answer this then direct questions have been prepared in the Krug script format.

<img src="{{ site.url }}{{ site.baseurl }}/images/colour_campus_app_wireframes/krug_script_direct_user_prompt.png" alt="linearly separable data">

Whilst an adapted Krug [6] script is useful for understanding the general trends of system improvement a system evaluator cannot rely solely on such subjective personal experiences.

Similar to the first round of testing a LIKERT scale is a valuable tool. The "User Experience Questionnaire" [7],[8]. This 26-question framework asks questions that aim to understand five aspects of system usability that are broadly categorised under "Pragmatic Quality" (including "Perspicuity", "Efficiency" and "Dependability") or "Hedonic Quality" (covering "Stimulation" and "Novelty").

• Attractiveness: To what degree do test users express their like or dislike of the subject prototype system? [7],[8]. This is broad gauge of system usability - but one of considerable significance.
• Perspicuity: Aims to understand the ‘learnability’ of the product. “Is it easy to get familiar with”?
[7]
• Efficiency: Covers the broad area of a test users goal fulfilment. “Can users solve their tasks without
unnecessary effort?” [7],[8]
• Dependability: Dependability describes the extent of system rigidity and predictability. “Does the
user feel in control of the [given] interaction?” [7]
• Stimulation: This metric aims to understand the subjective feelings of enjoyment when using a
prototype system – is the software “exciting and motivating?” [7]
• Novelty: This is a metric of mixed value, and so its importance is likely to vary between testing and
development projects. It is of value in this scenario however because it is critical that the new application is fresh and has a good chance of “catch[ing] the interest of users” [7].

<img src="{{ site.url }}{{ site.baseurl }}/images/colour_campus_app_wireframes/user_experience_questionnaire.png" alt="linearly separable data">

## Understanding test results and feedback

### User test feedback

1. The addition of a "Home" button proved popular

During this round of testing no participant attempted to use the “Search” icon in the screen footer. From this test it can be concluded that, at least these users, preferred to start at the application “Home” screen when moving between different areas and sub-menus of the main application homepage. It seems this change has had a positive effect and has seen users speed up between sub-menu navigation, though it is of note that the developer believes it worthwhile to retain the “Search” icon. The degree to which the "search control" continues to be used will need to be evaluated in further user testing but the option to search for a menu or page is still a useful feature.

2. Library resource and subject database is still causing confusion

Again this produced mixed results with students on various courses unsure of the difference between the UWTSD library and other subject databases. This area of the application could now require a complete rethink due to the such vast use students make of academic resources.

3. Printing options were clear and obvious.

the developer wanted to understand from this activity was the suitability of the print page colour-scheme. All users consulted clearly understood the steps involved with selecting printing and optionally replacing device files on the print page itself – but users struggled to locate the precise page. Unclear as to which menu this functionality was likely to be found users were torn between ‘My Programs and Apps’ and ‘Library Services’.
This structure caused the developer some confusion as document printing is an everyday task - but it comes under the library umbrella within the existing University structure.

4. Colour and control layout was generally popular - but requires further evaluation.

Alongside some tweaks to button text, icon use and navigational structure the most visible change is the addition of colour. Whilst one comment read “[this system] looks like something students would use” it is difficult to understand the premise or foundations of this statement and again, in retrospect, the interviewer needed to ask additional follow up questions to understand why these views were expressed.

### Usability Experience Scale

The Usability Experience Scale [7],[8] results have been placed into a spreadsheet tool provided by Hinderks [7], a format that offers a range of statistical and graphical conclusions to be drawn from the original questionnaire in regards to the applications success in each facet of application usability it measures.

<img src="{{ site.url }}{{ site.baseurl }}/images/colour_campus_app_wireframes/user_experience_scores_table.png" alt="linearly separable data">

From the table below it can be clearly seen that in all areas of usability the application is “Above Average”. For a campus app for students it can be suggested that the most valuable metrics are those of activity efficiency and user dependability and familiarity – both areas of which the overall scores for the application are said to be “Excellent”.
The next most valuable, especially in as varied a student landscape as University is learnability. This softwares trait is said to be borderline “Good” to “Excellent”.
Alongside these valuable system and contextual factors there are facets that have reduced significance. “Novelty” is of reduced importance for some application contents; such as VLE 'Moodle' where continuity is of more importance than innovative design.

<img src="{{ site.url }}{{ site.baseurl }}/images/colour_campus_app_wireframes/user_experience_questionnaire_facet_graph.png" alt="linearly separable data">

## Colour wireframe designs

*i. For the purposes of this design process the mobile device used is the iPhone X/10 screen size. this screen size has been selected to represent a ‘typical’ mobile device.*

*ii. Currently stand-alone mobile applications already exist for Moodle, Outlook and OneDrive but it is assumed that the companion app will integrate these, as illustrated below, to avoid the need to install each individual app.*

*iii. Where controls appear below the bottom of the screen a downwards scroll is inferred.*

The initial designs have been refined by test users and colour can now be introduced for users. Commonly, at least two or three more development iterations will take place to incrementally refine and settle on a first product release. The second designs are shown below and would, time permitting, form the basis of further user-based testing.

*--splasher screen--*
<img src="{{ site.url }}{{ site.baseurl }}/images/colour_campus_app_wireframes/splasher_screen.png" alt="linearly separable data">

*--sign in screen--*
<img src="{{ site.url }}{{ site.baseurl }}/images/colour_campus_app_wireframes/sign_in_screen.png" alt="linearly separable data">

*-sign in screen--*
<img src="{{ site.url }}{{ site.baseurl }}/images/colour_campus_app_wireframes/sign_in_keyboad.png" alt="linearly separable data">

*--enable touch id to sign in--*
<img src="{{ site.url }}{{ site.baseurl }}/images/colour_campus_app_wireframes/sign_in_touch_id.png" alt="linearly separable data">

*--main app menu--*
<img src="{{ site.url }}{{ site.baseurl }}/images/colour_campus_app_wireframes/main_menu.png" alt="linearly separable data">

*--moodle menu--*
<img src="{{ site.url }}{{ site.baseurl }}/images/colour_campus_app_wireframes/moodle_menu.png" alt="linearly separable data">

*--module view--*
<img src="{{ site.url }}{{ site.baseurl }}/images/colour_campus_app_wireframes/moodle_view_dbms.png" alt="linearly separable data">

*--my programs and app integration menu--*
<img src="{{ site.url }}{{ site.baseurl }}/images/colour_campus_app_wireframes/my_programs_menu.png" alt="linearly separable data">

*--library menu--*
<img src="{{ site.url }}{{ site.baseurl }}/images/colour_campus_app_wireframes/library_menu.png" alt="linearly separable data">

*--print menu--*
<img src="{{ site.url }}{{ site.baseurl }}/images/colour_campus_app_wireframes/print_menu.png" alt="linearly separable data">

*--TSDSU menu--*
<img src="{{ site.url }}{{ site.baseurl }}/images/colour_campus_app_wireframes/tsdsu_menu.png" alt="linearly separable data">

*-- and customisable menus--*
<img src="{{ site.url }}{{ site.baseurl }}/images/colour_campus_app_wireframes/main_menu_moodle_favourite.png" alt="linearly separable data">

### Work(s) used in project summary

[1] Bootstrap, “Buttons · Bootstrap,” *Bootstap Button Documentation*, 2019. [Online]. Available: https://getbootstrap.com/docs/4.0/components/buttons/. [Accessed: 14-May-2019].

[2] J. Scholtz, “Usability Evaluation User-Centered Evaluations,” *Natl. Inst. Stand. Technol.*, vol. 1, 2004.

[3] C. W. Turner, J. R. Lewis, and J. Nielsen, “Determining Usability Test Sample Size,” in *International Encyclopedia of Ergonomics and Human Factors*, 2nd ed., vol. 3, W. Karwowski, Ed. Boca Raton, FL, 2006, pp. 3084–3088.

[4] J. Nielsen and K. Landauer, Thomas, “Model of the Finding of Usability Problems,” in *Proceedings of the INTERACT’93 and CHI’93 conference on Human factors in computing systems*, 11993, pp. 206–213.

[5] J. (2001) Battleson, B., Booth, A., & Weintrop, “Usability testing of an academic library Web site: A case study. Journal of Academic Librarianship,” *J. Acad. Librariansh.*, vol. 27, no. 3, pp. 188-198., 2001.

[6] S. Krug, *Rocket surgery made easy: The do-it-yourself guide to finding and fixing usability problems*, 1st ed. Berkeley, CA: New Riders, 2010.

[7] A. Hinderks, “User Experience Questionnaire Handbook,” *Die UX KPI - Wunsch und Wirklichkeit*, pp. 1–15, 2017.

[8] B. Laugwitz, T. Held, and M. Schrepp, “Construction and Evaluation of a User Experience Questionnaire,” in *Symposium of the Austrian HCI and Usability Engineering Group*, 2008, pp. 63–76.



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
