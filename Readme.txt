Project - Binary classification to predict if the client will subscribe a bank term deposit 
          + Select the right customers for a telemarketing campaign.

Business background - The Telemarketing Team of a Bank runs campaigns to expand the term deposit portfolio. We are requested to 
enable prioritization for the Telemarketing team, so that overall responses and ROI of the campaign increases.

ROI will increase in 2 ways:-
• Reduction of investment by not calling up everyone
• Increase in rate of response among the prioritized customer list

Entire data response rate - x %
Prioritized list response rate - a %
Expectation from the model-> a > x

The list (and priority order) of customers to be contacted is prepared with the help of ML.

In this problem statement, recall is the important metric, as we dont want to miss out any individual who may go for a Term Deposit.

Data Source
This project is based on "Bank Marketing" UCI dataset
The full description along with dataset is available here at http://archive.ics.uci.edu/ml/datasets/Bank+Marketing



Based on the project, following Recommedations were formed.


#############Recommendations ##################

Phase 1 - Speak to 196 customers who falls in 'Top 2, Higher Age, poutcome=success' segment - their event rate is 70%.
Phase 2 - 'Top 2, Lower Age, poutcome=success' segment - their event rate is 61%.
Phase 3 - Rest of the customers in Top 2 segment - their event rate is ~30% (still much higher than population event rate, ie 11%).
         'Bottom 8, poutcome=success' segment also be included in this phase, as their count is minimal.

If the customer executive team has bandwidth beyond 3 phases, another approach can be taken, ie:
from the 'Bottom 8', next 2 deciles of customers can be chosen.

In case of a real project, as count of customers gets much higher, if the customer executive team has very limited bandwidth, 
instead of splitting into 10 Deciles based on Predicted Probability, split into even finer groups, (say 20) and 
prioritize records in the initial few groups, based on bandwidth.


Entire data response rate - ~11%
Prioritized customer list response rate - 70%, 61% and ~30%
Hence, expectation from the model is met.
