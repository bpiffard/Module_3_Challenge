# Module_3_Challenge
Repository for Module 3 Challenge Deliverables
## Overview of Election Audit
This project was completed for a Colorado Board of Elections. The goal of this project was to report the election results for a congressional seat from different Colorado counties in a particular congressional precinct. This code is meant to be reusable for other elections in this precinct, and possibly others. With modifications that will be discussed later, this code may be applied to other types of elections.

The goals of this project were to report back:
1. The total number of votes cast
2. Return the complete list of candidates in the election
3. Report the total number of votes received by each candidate
4. Calculate the percentage of votes received by each candidate
5. Determine the winner of the election based on popular vote

## Election-Audit Results

- Total number of votes cast in the election: 369,711
- Votes by county:
  - Jefferson: 10.51%, (38,855)
  - Denver: 82.78%, (306,055)
  - Arapahoe: 6.71%, (24,801)
- County with most votes: Denver
- Votes by candidate:
  - Charles Casper Stockham: 23.0% (85,213)
  - Diana DeGette: 73.8% (272,892)
  - Raymon Anthony Doane: 3.1% (11,606)
- Election winner: Diana DeGette
  - Total votes received: 272,892
  - Percentage of votes: 73.8%

## Election-Audit Summary
Now I will discuss 2 different ways that this code could be utilized for other elections.

First, this code could be applied to mayoral races. The only modifications necessary would be to replace mentions of "county" with council districts. If an election is determined by popular vote, there is a list of candidates, and the voters are separated by a type of region, this code can be altered to be used. If not separated by region, the code relating to that can simply be removed, and a popular vote result could still be determined.

Second, this code could be applied to statewide ballot propositions. This would require more extensive modification. The code that counts votes by county would still be valid, though. To create a list of the propositions would require pulling the name data from the header of the dataset. What we would need to pull from the dataset would be an entry of "yes" or "no", or "approve" or "disapprove" depending on the verbiage used on the ballot. A for loop would be created to count up all of these entries by row so that we would have a count of the "yes" votes. Once the "yes" votes are counted for each proposition, we just need to divide that number by the total number of votes. This will return a percentage. With an Ifelse loop, we can return which propositions met a threshold of >50% of the vote, and which didn't. In this If loop we can print the results of this calculation. Total vote counts for these propositions are meaningless so code relating to that would be deleted.

So as you can see, this code is fairly versatile, and as it is relatively simple, it is quite stable. It is also very flexible and light-weight, and can be modified quickly.
