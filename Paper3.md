# 2k18-csee-28 Danish Jalbani

Title:
           "Transferring information to Modern Code Update"
Author:
             Maria Caulo1, Bin Lin2, Gabriel Bavota2, Giuseppe Scanniello1, Michele Lanza2

Conference Name:
               International Conference on Cognitive Strategy (ICPC) in 2020
Introduction and Inspiration:
Information transfer is one of the main objectives of the latest code review, as shown by several studies that evaluated and interviewed developers. While data transfer may also be the obvious expectation of a code review process, there are no analytical studies that use tagged data from software to test the performance of code reviews for training “developers” and to improve their overtime skills. We present a mineral-based study investigating how the code review process is helping and developers have strengthened their offerings to open source projects over time. At the time of this paper, we were introducing Topics - a tool for identifying ways to change common patterns associated with system data. Used as an IntelliJ IDEA support plugin
Java programming language and Git VCS. These limitations come from the Refactoring Miner tool we use to obtain effective refinement. If there are similar tools for other languages ​​or VC, the plugin can be easily expanded to support other IDEs built into the IntelliJ Platform.

STUDY ARTICLE:
  Hypothesis
          Software development can be an informative activity. Evaluation studies have provided evidence that code reviews play a very important role in transmitting information between developers. However, there is not much evidence to support the claim. During this study, we mined our software to test the information in bulk
Express appreciation for what happens in the code review.

Subject Content:
The study context contains 728 developers, 4 981 software repositories. They contributed to it, and 77,456 closed PRs.
Developer options:
   To conduct our study, we collected information about GitHub users. Who created his account in 2015? This is designed to collect a minimum of 4 years of donor history for each developer.
As data collected in September 2019, we will be looking at inyaka4 year contributions even for users who created their GitHub account in December 2015. A four-year window is enough to view PRs submitted by developers and, as a result, update information submissions over time.
Drag application collection and filter:
We have collected all "closed" PR submitted by 818 topic developers from the day they joined GitHub up to September 2019, as soon as we collected data. This resulted in a total of 75,456 PRs receiving 9,845 vacancies. for each PR, we collect
The following details:
(1) Creation date: PR installation date.
(2) Approval: whether closed PR is accepted.
(3) Closing date: the date PR closed.
(4) ASCII document commentary: comments left by reviewers clearly linked to portions of the code submitted for review. Comments left by a PR author are not included.
(5) General comment: all comments left in the PR discussion by all developers next to the PR author, except the ASCII document documents. These comments are usually invited to clarify or clarify why PR should be accepted / rejected.
Source code comments, instead, report explicit material from the PR author to validate the imported code. We separate the ASCII document commentary and therefore the general ideas, because there may be different levels of technical detail in these two categories.
(6) Author: PR author.
(7) Providers: all developers participating in Discussion and PR hosting.
Steps:
To substantiate our point of view, we use proxies to measure the transmission of information by developers through their revised PRs and to evaluate the quality of developer contributions over time.
Methods of information. We use the amount of revised PRs developer provided (written) within the past (i.e., prior to this PR) as a liability for the amount of information transferred to it as a result of the code review process. That is, we think that the PRs are closed and the most revised engineers have, the more information the developer has gained. In our study, we found that peer-reviewed PRs were the ones that received at least 1 comment by non-bot users. The reason for this choice is that if no comments are given to other developers, we assume that PR was not limited to a proper review process and, therefore, is not happy with our intentions, because no transfer information is possible when PR.


Data analysis:
         Quality delivery methods. We think that through the transfer of information one of the benefits for developers is the improvement of the quality of their offerings (e.g., PR) over time. While there are a few metrics available to move a certain code to certain limits
Block their programs according to our study content: 1) the software involved is often written in several programming languages, making it difficult to bend global CK network tracks, including not all input languages ​​focused on something. 2) Metrics like bug count believe that an idea is often identified as a result of the constant use of problem tracking systems, which is not the case. Recent comments received. number of general comments received
From all the developers except the PR author. We are waiting
That is with the increase in revised PRs (e.g., for more information
Forwarded developer (won), a few conversations are about to take place
Created by PR, which leads to a reduction in standard comments.
Received source code comments. the number of ASCII document comments received from all developers except the PR author. Similarly to the general comments received, we can expect that the views of the ASCII documents received will diminish over time as well. Acceptance value. the speed of acceptance of past PRs. We expect that the share of accepted PRs over time will increase. PR hour adopted. Time (expressed in minutes) between creation and thus closure of accepted PRs. We expect that the time required to easily adopt PRs will decrease over time. ASCII document comment concept. The emotional unity of all ASCII documentary ideas within PRs. We expect that with the increase in the quality of donations receive acceptance within the code review. Therefore, the feelings of the developer embedded within the comments should get better over time. The feeling of common comment. The emotional unity of all the common comments within PRs. Similarly in the comments of the ASCII document, we expect that general comments will also be optimistic over time. Conceptual analysis To calculate the sound unity of comments within PRs, we have adopted SentiStrength-SE.
Data analysis:
               Our hypothesis suggests that developers, who have benefited from the transfer of high-quality information due to previous revised PRs who have moved, also contribute higher-quality PR to the project. We confirm this hypothesis because of the previously released data. Each peer-reviewed PRi submitted by any of the other advanced developers represents a line in our database, reporting (i) information transfer methods, i.e. the number of previous revised PRs made by the engineer before PRi and as our control variants
With most of the work he did internally in the past.
RESULTS:
The box structures in Figures 1, 2, 3, and 4 show the tendency for reliable variables (i.e., donation quality methods), in both crosses ((left) and single project conditions, (right) in relation to different independent variables (i.e., information methods) However, the best neighbor of each figure reports the results obtained when dividing developers into "information groups" based on the revised PRs they sent while the lower part shows the same results when team engineers support the amount of previous work they did.
Value for PRs:
By looking at the robots reported in Fig. 1 (a) and (b), we will consider the similarity of the Approval Percentage (indicated by percentage) of PRs when previous PRs reviewed PRs submitted by the developer for his information. That is, the minimum viewing of Fig. 1 (upper part), we did not see any effect on the transfer of information on future PRs opportunities to be accepted.
Accepted Closing Time:
As for the accepted PR hour, the best neighbor of Fig. 2 moreover he is flat, in both cross- and single-project scenes. These findings are supported by the results of statistical analysis, reported size sizes that are not desirable for all comparisons made.
Comments Posted on PRs:
We discuss together our findings both the majority of common comments (Figure 3) and comments of the ASCII document (Figure 4) submitted within the PRs submitted by various groups of developers. We started specifically
The first is a neighbor of both figures (e.g., results related to PRs recently reviewed).
To answer our research question:
Our study has led to what we will describe as a negative outcome. in other analysis-dependent variables we did not find any significant effect on the transmission of information within the code review process.
Level of contributions submitted by developers to open source projects. in particular, in terms of the acceptance of PRs, we did not see any positive impact within the context of the project project when we used previous PRs as a proxy to transfer information. Instead, the increase in experience over time may be more important in the event of the level of acceptance of PRs, as evidenced by the results obtained when using previous practice as an independent variant.
CONCLUSIONS
           We presented a quantitative study to research knowledge transferrin code review. Our results were mostly negative: we weren't able to capture the positive role played by code review in knowledge
Transfer among developers, as was previously suggested within the literature [2].This came to us as a surprise, as we were confident those a minimum of serious traces of the knowledge transfer, because despite not supporting the findings of Bachelor and Bird [2] given our results, we actually are convinced that their claims are correct. This raises sort of questions that we've addressed impart throughout the latter a neighborhood of the paper, where we conjecture possible fallacies in our experiment design and notable threats to
Validity that are difficult to completely address, especially those regarding the measures we used to quantify the impact of knowledge transfer. 
