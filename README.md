# Election-Analysis

## Overview of Election Audit: 
Seth and Tom had an audit to check the voter turnout, percentage of votes, total count and highest turnout for each county. During this analysis we printed the Election Results to command line and saved to a text file. 

## Election-Audit Results: 
* Total votes: 369,711

### The number of votes and the percentage of total votes for each county in the precinct.
* Jefferson: 10.5%(38,855)
* Denver: 82.8%(306,055)
* Arapahoe: 6.7%(24,801)

### The Election Analysis shows that ***Denver*** was the largest number of votes with 306,055 votes. 

### The winning candidate:
* Diana DeGette
* Vote Count: 272,892
* Winning Percentage: 73.8%

## Election-Audit Summary: 

Based on the audit it shows that Denver had the largest turnout as well as Diana DeGett counted with most votes. This script can be for any election if the header format is the same. If not we would have to modify the script to match where to pull data from. This script could also be used to count any poll results, such as favorite Ice Cream flavor in each county with a bit of tweaking. 

        # Add to the total vote count
        total_votes = total_votes + 1

        # Get the candidate name from each row.
        candidate_name = row[2]

        # 3: Extract the county name from each row.
        county_name = row[1]

        # If the candidate does not match any existing candidate add it to
        # the candidate list
        if candidate_name not in candidate_options:

            # Add the candidate name to the candidate list.
            candidate_options.append(candidate_name)

            # And begin tracking that candidate's voter count.
            candidate_votes[candidate_name] = 0

        # Add a vote to that candidate's count
        candidate_votes[candidate_name] += 1

        # 4a: Write an if statement that checks that the
        # county does not match any existing county in the county list.
        if county_name not in county_names:
            # 4b: Add the existing county to the list of counties.
            county_names.append(county_name)

            # 4c: Begin tracking the county's vote count.
            county_votes[county_name] = 0

        # 5: Add a vote to that county's vote count.
        county_votes[county_name] += 1
        
