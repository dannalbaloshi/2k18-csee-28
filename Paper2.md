# 2k18-csee-28 Danish Jalbani

Title::
"Visualization Methods Based on VCS data"

Author:
Sergey Svitkov, Saint-Petersburg State University
Timofey Bryksin, JetBrains Research, St. University-State University


Conference Name:
Mining Software Repositories (MSR) 2020 Conference

Introduction and motivation:
          Software developers have a great set of tools and techniques that can help them improve their code, but still, many bugs are not available. While this paper leaves the impression that if certain pieces of code are changed frequently, they may be caused by certain technical or construction problems, therefore, this piece needs more attention from developers. Many teams these days use version control programs to track changes in their code and organize interactions between developers. We suggest using data from version control systems to track the number of changes of each method during a period of project and display this information within the IDE code editor. Software product development can be a very complex process that requires the collaborative work of many software developers. Various methods and processes have been introduced to help maintain quality code, including static code processing or a complete code update, but still, bed bugs are no longer available. Several papers report a high association between the frequent discovery of bed bugs in certain parts of the code and the way in which fragments are often changed over time. The method or function can often change thanks to a specific technical, construction or external problem.

Research Methods:
To use the proposed tool, the following steps should be appropriate
Taken:
read the history of commitment (each committed individually and each fully);
keep the account history data processed internally to stop the restart of each IDE implementation;
create syntax trees for all files and all content
identify the event-based approach to revitalize the internal model well when the route is reversed (for example, when the route has been renamed);
Display the frequency change data obtained within the IDE editor. This section describes the components of the IntelliJ Platform and external libraries that help open the project.

IntelliJ platform:
System System Domain. The Interface2 System (PSI) architecture is the foundation of the IntelliJ Platform. Provides a standard application interface (API) for encryption in different Program languages.
Git4Idea. Git4Idea module3 is part of the IntelliJ Platform that allows it to work with Git. Provides Aciform directly to object with branches, changes history, file updates, etc. A single commitment is expressed in the GitCommit section, keeping track of changes made with promise, hash code, date and time, author time and comment message.
Editor. Editor is a working API and text editor for IntelliJ Platform-based IDEs. Provides access to various features such as working with currently opened file text, modification of various viewing elements, event management, etc. The visual properties of the editor are represented by its Inlay Model feature, which has a variety of ways to add, remove, and edit them.

Refactoring miner:
As mentioned in Section 2, reworking can create problems by updating the data collection model. To prevent data loss when, for example, the method was renamed, cases like these could be tracked and deliberately processed. Various detection tools are available, such as Refined, JDEvAn, Refactoring Crawler, or Refactoring Miner.

Implementation:
             Data processing is monitored when opening either the project in IDE or the commitment is made through the IDE user interface. In the latter case, the tool continues with the acquisition acquisition step. In the previous case, if the project is new, all the commitments at the selected time are considered sequentially. In addition, each new commitment is tested to have already been considered in advance by comparing its hash codes with the hash codes of previously performed tasks. When the first discovery is not detected, the first detection step begins.
Detected detection
 Recurring events are exposed to factors that threaten the Refactoring Miner's API. After the acquisition, the handler returns the Refactoring Data item, holding it
Details of affected methods before and after duplication. When all decreasing cases found within a single gift are processed, a set of Data Connected Items is there for analysis.
Analysis of bond changes.
The next step is to analyze the changes being made. The plugin takes file updates before and after and creates PSI trees in its content to promote details about the options in the modified file. It is then used to update the internal model of the plugin memory: a collection of Method Info items that contain information about the paths within this particular file.
Use of redesigned events. If the acquired collection of items called Refactoring Data is empty, the Way Info data collection is updated and is consistent with the type of recurring acquisition.

The proposed plugin:
The plugin is outside the Jet Brains plugin Repository, 5 its source code is located at Github.6
When a developer opens a project within the IDE, plugins check that the translation system has been hired. If no VCS root directory is available, a warning message is displayed, the plugin is turned off and remains in this state until the project opens or the VCS root is about the current project. All data retrieval from VCS history is completed in the background.
A complete history of commitment has just been passed on to them as soon as the project opens for the first time. After that, it probably has no effect on the normal operation of the IDE.

Conclusion:
In this paper, we present Tobias — a tool for the visualization of   Methods change frequency consistent with the version system data. It had been implemented as a plugin for IntelliJ IDEA supporting Java programing language and Git VCS. These limitations come from the Refactoring Miner tool that we use to detect appliedrefactorings. If there have been similar tools for other languages or VCS, the plugin could easily be extended to support other IDEs built ofIntelliJ Platform.
