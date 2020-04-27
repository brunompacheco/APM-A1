# Advanced Process Mining Lectures - Assignment 1

> In this part of the assignment you will deal with a hypothetical process of large-scale infection testing and potential treatments. The healthcare institution has extracted a log in csv format that is provided as “log.csv” in the assignment zip file for further analysis. It is your task to make sense out of the data, and, to help the hospital in understanding their process. In doing so, we will be using the Process Mining for Python (PM4Py) library. As we all want to become good data/process scientists, we will carry out our analysis in a python notebook using JupyterLab, that has been setup for you. In addition, you are supposed to deliver a written report.

## Q1. Inductive Miner

In this question you should discover a model for the given event log with a special focus on the Inductive Miner implemented in PM4Py.
1. Apply the Inductive Miner implemented in PM4Py to the given event log and describe the process. Furthermore, give and reason about the fitness and precision results, respectively. On a high level, describe the potential problems of the model and reason how they were caused by the algorithm and the log.
1. From the process owner we know that patients are called in order to control the quarantine and that there are two potential quarantine phases, i.e., before and after a positive test. Implement a function that resolves the duplicate activity Control Call by context sensitive renaming. Discuss the impact on the discovered model. (Hint: The Test activity is not affected by noise)
1. The log contains a considerable amount of noise induced by errors during the event logging. Apply the IM to a DFG filtered for noise. Describe your results and explain why the IM mines a different model. Which type of noise is prominent in the log? (Hint: Have a look at the dfg_filtering module in the source repository)
1. Investigate the DFG of the log after applying the preceding steps. Which activities might be filtered out in order to obtain an improved model that explains most of the process more precisely? Why might this yield better results when applying the IM? Implement a filter and apply the IM to the filtered log. (Hint: Have a look at the basic_filter module in the log utility in the sources of the PM4Py project)
1. Consider the process model for the patients who were prescript the special medication. What do you observe? How is this behavior captured by the complete model in d)?
1. Apply additional miners to the log and compare the results. Which model is the best model?

## Q2. Social Network Analysis

Discover the organizational perspective of the process. For each of the following networks, try to find a clear organizational structure and discuss the structure obtained. If no clear structure is to be found, explain why this is the case.
(Hint: Have a look at the old documentation)

1. Handover-of-Work Social Network
1. Subcontracting Social Network
1. Working-Together Social Network
1. Reassignment Social Network

## Q3. Performance Analysis
Which parts of the process have the biggest influence on the total case duration?

1. Provide and briefly describe results of your performance analysis. Remember to also consider your current results which may give you a good entry point for a deeper analysis.
1. Discuss insights obtained from you analysis, e.g, identify bottlenecks, and discuss their impact.

## Q4. Decision Points
Investigate how patients are referred for further treatment by means of a decision tree. Describe the factors that you observe.
(Hint: Have a look at the old documentation)

1. Create a decision tree of reasonable complexity using the available attributes in the log.
1. Since it is likely that the resources at the treatment facilities are limited, implement a function that assigns a(n) (estimate) of the number of patients at each facility to each event. To this end, you have to decide which event occurs at which facility based on your analysis in question 2. Create a decision tree of reasonable complexity using this derived attribute.
(Hint: There is an easy pattern that might help you to find a proper facility assignment)


## Q5. Process Improvement Suggestions
Based on the information that has been obtained for the previous four questions, are there any opportunities for improving the care process? For each of the above questions can you mention any improvement opportunity? If yes, indicate how the process can be improved. If not, explain why.