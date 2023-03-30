# Election_Analysis

## Project Overview
A Colorado Board of Elections employee has given you the following tasks to complete the election audit of a recent local congressional election.

1. Calculate the total number of votes cast.
2. Get a complete list of candidates who received votes.
3. Calculate the total number of votes each candidate received.
4. Calculate the percentage of votes each candidate won.
5. Determine the winner of the election based on popular vote.

## Resources
- Data Source: election_results.csv
- Software: Python 3.11, Visual Studio Code, 1.75.1

## Summary
The analysis of the election shows that:
- There were 369,711 votes cast in the election.
- The candidates were:
    - Charles Casper Stockham
    - Diana DeGette
    - Raymon Anthony Doane
- The candidate results were:
    - Charles Casper Stockham received 23.0% of the vote and 85,213 votes.
    - Diana DeGette received 73.8% of the vote and 272,892 votes.
    - Raymon Anthony Doane received 3.1% of the vote and 11,606 votes.
- The winner of the election was:
    - Diana DeGette, who received 73.8% of the vote and 272,892 votes.

## Challenge Overview
The election commission has requested data about county turnout, including:
- The voter turnout for each county
- The percentage of votes from each county out of the total count
- The county with the highest turnout

## Challenge Summary
Further analysis of the election shows that:
- The county results were:
    - Jefferson received 10.5% of the vote and 38,855 votes.
    - Denver received 82.8% of the vote and 306,055 votes.
    - Arapahoe received 6.7% of the vote and 24,801 votes.
- The county with the largest turnout was:
    - Denver, which received 82.8% of the vote and 306,055 votes.

The program can be modified for use in any election by changing the indices in the following code to the appropriate column numbers as needed.

```python
        # Get the candidate name from each row.
        candidate_name = row[2]

        # 3: Extract the county name from each row.
        county_name = row[1]
```

Furthermore, there could be more columns to count, such as if there are multiple positions to vote for. More variables can be used here, as follows:

```python
        # Get the candidate name from each row.
        candidate_president_name = row[2]

        # Get the candidate name from each row.
        candidate_senate_name = row[3]

        # 3: Extract the county name from each row.
        county_name = row[1]
```

Votes for additional positions also need their own code similar to the following code.

```python
        # If the candidate does not match any existing candidate add it to
        # the candidate list
        if candidate_name not in candidate_options:

            # Add the candidate name to the candidate list.
            candidate_options.append(candidate_name)

            # And begin tracking that candidate's voter count.
            candidate_votes[candidate_name] = 0

        # Add a vote to that candidate's count
        candidate_votes[candidate_name] += 1
```
