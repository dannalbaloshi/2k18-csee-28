# 2k18-csee-28 Danish Jalbani

Title: 
“Visualization of Methods Changeability Based on VCS Data”
Author:
Sergey Svitkov, Saint-Petersburg State University
Timofey Bryksin,JetBrains Research, Saint-Petersburg State University


Conference Name: 
The Mining Software Repositories (MSR) conference 2020
Introduction and motivation:
          Software engineers have a good sort of tools and techniques that can help them improve the standard of their code, but still, a lot of bugs remain undetected. During this paper we repose on the thought that if a specific fragment of code is modified too often, it could be caused by some technical or architectural issues, therefore, this fragment requires additional attention from developers. Most teams nowadays use version control systems to trace changes in their code and organize cooperation between developers. We propose to use data from version control systems to trace the amount of changes for each method during a project for a specific period of time and display this information within the IDE’s code editor. Development of software products may be a very complex process that often requires the joint work of multiple software developers. Various practices and techniques have introduced that help to stay the quality of code at a suitable level, including static code analysis or thorough code reviews, but still, tons of bugs remain undetected. Several papers report a high correlation between how often bugs are found in certain code fragments and the way often these fragments are changed over time. A way or a function could change frequently thanks to some technical, architectural or maybe external issue.
Research Methodology:
In order to implement the proposed tool, the subsequent steps should
Be taken:
read the commit history (each commit individually and every one of them as a whole);
store the processed commit history data internally to stop recalculation on each IDE restart;
build syntax trees for every file and every commit’s content;
detect method refactoring events so as to update the interior model correctly when a way is modified (for example, when a way is renamed);
Show the obtained change frequency data within the IDE’s editor. This section describes IntelliJ Platform’s components and external libraries that help to unravel these tasks.
IntelliJ Platform:
Program Structure Interface. Program Structure Interface2 (PSI) is the IntelliJ Platform’s core. It provides a common application programming interface (API) for working with code in different Programming languages.
Git4Idea. The Git4Idea module3 is a part of IntelliJ Platform that allows it to work with Git. It provides a rich object-oriented Aciform working with branches, changes history, revisions of files, etc. A single commit is represented by the GitCommit class, storing the information about changes made in a commit, commit’s hash code, date and time, its author and a comment message.
Editor. Editor is an API for working with the text editor ofIntelliJ Platform-based IDEs. It provides access to various features like working with currently opened file’s text, modification of different visual components, events handling, etc. Visual elements of the editor are represented by its Inlay Model object, which has a wide variety of methods for adding, removing, and editing them.
Refactoring Miner:
As was mentioned in Section 2, refactoring could cause issues with updating the collected data model. So as to avoid data loss when, for example, a way was renamed, cases like this could be deliberately tracked and processed. Several refactoring detection tools exist, like Refined, JDEvAn, Refactoring Crawler, or Refactoring Miner.
IMPLEMENTATION:
             Commit data processing is triggered when either a project is opened in the IDE or a commit is made via the IDE’s user interface. In the latter case, the tool proceeds with refactoring detection step. In the former case, if the project is new, all commits for a selected time period4 are sequentially processed. Otherwise, each new commit is checked for having been already processed before by comparing its hash code against hash codes of previously processed commits. When the primary unseen commit is found, the refactoring detection step begins.
Refactoring’s detection.
 Refactoring events are represented by objects wrapping Refactoring Miner’s API. After the detections finished, the handler returns a Refactoring Data object, holding
Information about affected methods before and after the refactoring. When all refactoring cases detected within one commit are processed, a set of Refactoring Data objects is out there for further analysis.
Analysis of commit changes. 
Subsequent step is that the analysis of the commit changes. The plugin takes the before and after revisions of the file and builds PSI trees from their content so as to urge information about methods within the changed file. Then it's used to update the plugin’s current in-memory model: a set of Method Info objects holding information about methods during this particular file.
Application of detected refactoring events. If the obtained collection of the Refactoring Data objects isn't empty, the gathering of Method Info objects is updated again consistent with the sort of the detected refactoring.

THE PROPOSED PLUGIN:
The plugin is out there at Jet Brains Plugin Repository, 5 its source code is out there on Github.6
When a developer opens a project within the IDE, the plugin checks if a version system is employed. If no VCS root directory is found, a warning message is shown, the plugin turns off and remains in this state until a replacement project is opened or a VCS root is about for the current project. All data retrieval from a VCS history is completed within the background.
The full commit history for a specific period of time is merely browsed through once when a project is opened for the primary time. Then, there is almost no impact on the general IDE performance.
CONCLUSIONS:

In this paper, we present Tobias — a tool for the visualization of   Methods change frequency consistent with the version system data. It had been implemented as a plugin for IntelliJ IDEA supporting Java programing language and Git VCS. These limitations come from the Refactoring Miner tool that we use to detect appliedrefactorings. If there have been similar tools for other languages or VCS, the plugin could easily be extended to support other IDEs built ofIntelliJ Platform.
