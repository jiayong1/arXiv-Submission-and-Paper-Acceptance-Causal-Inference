# Using Causal Inference in Determining the Influence of arXiv Submission on Paper Acceptance


For various computer science conferences, people have been discussing variousways to improve the submission policy including double-blind reviews, 1-month non-anonymized preprint submission, etc. In this work, we are interested in answering the question of whether uploading paper on arXiv before conferencesubmission can influence paper acceptance to computer science conferences. To answer this question, we constructed a causal graph and adapted causal inferencetechniques to measure the causal effect. Data were collected from Open-Review, arXiv and Google Scholar through web scripting. We then implemented and calculated the causal effect using a famous framework "DoWhy". Our final result shows a reasonably significant inference between arXiv submission and Paper Acceptance, though there are more future works required to prove it.

## Intro
Since 2018, many computer science conferences, such as ACL, EMNLP, NAACL, TACL, AACL, IJCNLP, and EACL, announced a new submission policy notified that “submission will not be considered anonymized if the author post (or update) a non-anonymized preprint version within an anonymity period lasting from 1 month before the submission deadline until the time of notification (or withdrawal)” [1], any violation on this policy may result in a reject paper submission. This new policy was made for protecting double-blind reviews. During the discussion progress of policymaking, some people argued that posting non-anonymized preprints such as posting on arXiv(an open-access archive for scholarly articles) before or during the submission period should be forbidden, while some claim that posting papers on arXiv are a crucial way to help authors to write better papers.

This argument also raises interesting questions: can arXiv submission have influences on paperacceptance to conferences? If so, then how large is the influence? On the other hand, though we would like to conduct experiments to study these questions, it is almost impossible to perform randomized experiments on real conference submissions. It is unfair to ask some authors to post their papers to arXiv while forbidding others. Thus in order to answer those questions from observational data, we adapt techniques from causal inference. With a carefully constructed causal graph, we are able to answer the question – how large is the effect of arXiv submission on paper acceptance to conferences with only observational data.

In this work, we try to answer this question through the following steps:
• Constructed the causal graph for our problem.
• Found methodology on how to block out the confounding variables in our causal graph.
• Collected data to estimate each variable.
• Executed our methodology to find out the causal effect.
