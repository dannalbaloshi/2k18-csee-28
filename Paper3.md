# 2k18-csee-28 Danish Jalbani

Title: 
           “Knowledge Transfer in Modern Code Review”

Author:
Maria Caulo1, Bin Lin2, Gabriele Bavota2, Giuseppe Scanniello1, Michele Lanza2


Conference Name: 
          International Conference on Program Comprehension (ICPC) 2020

Introduction and Motivation:
Knowledge transfer is one of the main goals of modern code review, as shown by several studies that surveyed and interviewed developers. While knowledge transfer is a clear expectation of the code review process, there are no analytical studies using data mined from software repositories to assess the effectiveness of code review in “training” developers and improve their skills overtime. We present a mining-based study investigating how and whether the code review process helps developers to improve their contributions to open source projects over time. In this paper, we present Topias — a tool for the visualization of methods change frequency consistent with the version system data. It had been implemented as a plugin for IntelliJ IDEA supporting
Java programing language and Git VCS. These limitations come from the Refactoring Miner tool that we use to detect applied refactorings. If there have been similar tools for other languages or VC, the plugin could easily be extended to support other IDEs built on IntelliJ Platform.

STUDY DESIGN:
  Hypothesis
          Software development may be a knowledge-intensive activity. Qualitative research provided evidence that code review plays a pivotal role in knowledge transfer among developers. However, no quantitative evidence exists in support of this claim. During this study, we mine software repositories to quantitatively assess the knowledge
Transfer happening because of code review.

Study Context:
The study context consists of 728 developers, 4,981 software repositories. They contributed to, and 77,456 closed PRs.

Developer’s selection:
   To run our study, we collected information about GitHub users. Who created their account in 2015? This was done to collect at least four years of contribution history for each developer.
Since data was collected in September 2019, we can observe ∼4 years of contributions even for users who created their GitHub account in December 2015. A four-year time window is long enough to observe enough PRs submitted by developers and, consequently, to study the knowledge transfer over time.
Pull requests collection and filtering:
We collected all the “closed” PRs submitted by the 818 subject developers from the day they joined GitHub until the end of September 2019, when we Collected the data. This led to a total of 77,456 PRs spanning 9,845 repositories. For each PR, we collected the
Following information:
(1) Creation date: the date during which the PR was submitted.
(2) Acceptance: whether the closed PR was accepted.
(3) Closing date: the date during which the PR was closed.
(4) ASCII text file comments: the comments left by the reviewers that are explicitly linked to parts of the code submitted for review. Comments left by the PR author are excluded.
(5) General comments: all the comments left within the PR discussion by all the developers aside from the PR author, excluding source code comments. These comments are generally wont to invite clarifications or to elucidate why a PR should be accepted/rejected.
Source code comments, instead, reports explicit action items for the PR author to enhance the submitted code. We separate the source code comments and therefore the general comments, as there might be different levels of technical details in these two categories.
(6) Author: the author of the PR.
(7) Contributors: all the developers who are involved within the Discussion and handling of the PR.

Measures:
To verify our hypothesis, we use proxies to measure the knowledge transfer experienced by developers through their past reviewed PRs and to assess the quality of developers’ contribution over time. 
Knowledge measures. We use the number of reviewed PRs developer contributed (authored) in the past (i.e., before the current PR) as a proxy of the amount of knowledge transferred to her thanks to the code review process. That is, we assume that the more closed and peer-reviewed PRs a developer has, the more knowledge the developer gained. In our study, we consider that peer-reviewed PRs are those which received at least one comment by non-bot users. The rationale behind this choice is that if no comments are given by other developers, we assume that the PR was not subject of a formal review process and, thus, it is not interesting for our goals, since no transfer knowledge can happen in that PR.


Data Analysis:
         Contribution quality measures. We assume that with the knowledge transfer one of the major benefits developers receive is the improvement of the quality of their contributions (i.e., PRs) over time. While there are a few existing metrics to evaluate code quality some limitations
Hinder their applications in our study context: 1) the software repositories involved can be written in different programming languages, making it impossible to set universal thresholds for CK metrics, let alone not all programming languages are object-oriented. 2) Metrics like bug count rely on the assumption that bugs can be identified thanks to the consistent usage of issue tracking systems, which is not always the case. General comments received. The number of general comments received
From all the developers other than the PR author. We expect
That with the increase of past reviewed PRs (i.e., with more knowledge
Transfer the developer benefited of), fewer discussions will be
Triggered by the PR, leading to a reduction of general comments.
Source code comments received. The number of source code comments received from all the developers other than the PR author. Similarly to general comments received, we would expect that the source code comments received will decrease over time as well. Acceptance Rate. The rate of the past PRs acceptance. We expect that the percentage of accepted PRs over time will increase. Accepted PR closing time. The time (expressed in minutes) between the creation and the closing of the accepted PRs. We expect that the time needed to accept PRs will decrease over time. Sentiment of source code comments. The sentiment polarity of all source code comments in the PRs. We expect that with the increase of contribution quality more appreciation will be received in the code review. Thus, the sentiment of the developer embedded in the comments should be increasingly positive over time. Sentiment of general comments. The sentiment polarity of all the general comments in the PRs. Similarly to source code comments, we expect general comments will also be more positive over time. Sentiment analysis. To calculate the sentiment polarity of the comments in the PRs, we adopted SentiStrength-SE.

Data Analysis:
               Our hypothesis suggests that developers, who benefited of higher knowledge transfer thanks to the past reviewed PRs they submitted, are also the ones contributing higher quality PRs in the project. We verify this hypothesis thanks to the data previously extracted. Each peer-reviewed PRi submitted by any of the studied developers represents a row in our dataset, reporting (i) the knowledge transfer measures, meaning the number of past reviewed PRs performed by the developer before PRi as well as our control variable, represented
By the number of commits she performed in the past.

RESULTS:
The box plots in Figures 1, 2, 3, and 4 show the trends of the dependent variables (i.e., the contribution quality measures), for both the cross- (left) and single- (right) project scenarios, with respect to the two independent variables (i.e., the knowledge measures).In particular, the top part of each figure reports the results obtained when splitting developers into “knowledge groups “based on the past reviewed PRs they submitted, while the bottom part shows the same results when grouping developers based on the number of past commits they performed. The red dot represents the mean value in each box plot.
PRs Acceptance Rate:
By looking at the boxplots reported in Fig. 1 (a) and (b), we can observe an almost flat trend of the Acceptance Rate (expressed in percentage) of PRs when the past reviewed PRs submitted by developer serve as a proxy for her knowledge. That is, at least by looking at Fig. 1 (top part), we did not observe any effect of the knowledge transfer on the likelihood of future PRs to be accepted.
Accepted PRs Closing Time:
As for the accepted PR closing time, the top part of Fig. 2 is also quite flat, for both cross- and single-project scenarios. This finding is also supported by the results of the statistical analysis, reporting negligible effect sizes for all performed comparisons.
Comments Posted in PRs:
We discuss together our findings for both the number of general comments (Fig. 3) and source code comments (Fig. 4) posted in the PRs submitted by different groups of developers. We first focus on
The top part of both figures (i.e., results related to the past reviewed PRs).
Answering our Research Question:
Our study led to what we can define a negative result. For most of the analyzed dependent variables we did not find any strong impact of the knowledge transfer in the code review process on
The quality of the contributions submitted by developers in open source projects. In particular, for the PRs acceptance rate, we did not observe any positive effect in the cross-project scenario when using past PRs as a proxy for knowledge transfer. Instead, an increase of experience over time might be more important for the improvement of the PRs acceptance rate, as demonstrated by the results achieved when using past commits as independent variable.

CONCLUSIONS
           We presented a quantitative study to investigate knowledge transferrin code review. Our results were mostly negative: we were not able to capture the positive role played by code review in knowledge
Transfer among developers, as was previously suggested in the literature [2].This came to us as a surprise, as we were confident those at least significant traces of the knowledge transfer, because despite not supporting the findings of Bachelor and Bird [2] given our results, we actually are convinced that their claims are correct. This raises a number of questions that we have addressed impart throughout the latter part of the paper, where we conjecture possible fallacies in our experiment design and notable threats to
Validity that are difficult to fully address, especially those regarding the measures we used to quantify the impact of knowledge transfer. A
