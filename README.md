# Parler and Twitter Users Analysis

This repository contains data and code supporting a Columbia Journalism School thesis project about Parler users who were suspended from other platforms, particularly those users who indicated support for or affiliation with far-right extremist groups. The project was completed on August 13, 2021. See below for details.

## Data

The analysis explores Parler user data downloaded from the social media platform before its shutdown in January. The data was released in February as part of a study performed by Aliapoulios, et al. and downloaded from [Zenodo](ADD LINK HERE!!). 

The `parler_data` directory contains the following:

### Total users

- `parler_users.csv`, which includes all 13.25 million users available for download.

### Users mentioning far-right groups

- `filtered_users_right.csv`, which includes users who mention the Proud Boys, Three Percenters, Oath Keepers and/or Boogaloo Bois in their bios
- `right_short_users.csv`, which includes the above users whose usernames did not exceed 16 characters for the Twitter API analysis
- `right_users_final.csv`, which includes the above users and their Twitter account statuses to be reviewed manually
- `right_active_users.csv`, which includes the above users with a corresponding active Twitter account
- `right_active_twitter_info.csv`, which includes the above information on active Twitter users merged with the `right_active_users.csv`

### Users mentioning social media suspensions

- `banned_users.csv`, which includes users who mentioned a ban or suspension from a social media site in their bios.
- `banned_short_users.csv`, which includes the above users whose usernames did not exceed 16 characters for the Twitter API analysis.
- `banned_users_final.csv`, which includes the above users and their Twitter account statuses to be reviewed manually. 
- `banned_active_users.csv`, which includes the above users with corresponding active Twitter accounts.
- `banned_active_twitter_info.csv`, which includes the above information on active Twitter users merged with the `banned_active_users.csv`.

## Twitter API

The account statuses of Parler users in the above dataset were found using Twitter API. The `api_data` directory contains the following:

- `right_api_results.csv`, which includes the Twitter account statuses of the users from the right_short_users.csv
- `right_active_api_results.csv`, which includes active users' bios, followers count and tweet count from Twitter API
- `banned_api_results.csv`, which includes the Twitter account statuses of the users from the `banned_short_users.csv`
- `banned_active_api_results.csv`, which includes active users' bios, followers count and tweet count from Twitter API

## Analysis

The `parler_users_subset1.ipynb` notebook loads the Parler user data, identifies trends in the dates users created accounts on the platform and filters users to a subset who mention support for or affiliation with the Proud Boys, Three Percenters, Oath Keepers and/or Boogaloo Bois in their bios. It outputs the CSV used to identify this subset's account status on Twitter. It also loads the Twitter API results and exports a CSV of users with active accounts for further analysis. 

The `parler_users_subset2.ipynb` notebook loads the Parler user data and filters the users to a subset who mention a suspension from a social media platform in their bio. It also outputs the CSV used to identify this subset's account status on Twitter. 

The `twitter_user_search.ipynb` notebook uses the Parler user data described above to identify users with the same usernames on Twitter and retrieve the status of their accounts. For those with active Twitter accounts, this notebook includes code to retrieve the bios and follower counts. 

## Contact

If you have any questions about this repository, you can reach out to Sheridan Wall at [slw2177@columbia.edu](mailto:slw2177@columbia.edu).
