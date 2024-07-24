# Salary Word Salad
### Zeke Abuhoff

## Rationale
Pay transparency is not a universal norm when it comes to job listings. Some states require that a job listing include salary information, but many don't. Many listings rely on implication and euphemism to convey how much compensation an applicant can expect - a norm that favors employers who wish to let new epmployees come in with below market salary expectations. If a model could estimate what a role's pay would be when it's not stated explicitly, that could help countless job seekers find the right position and negotiate for what they deserve.

## Research Question
Can the title and description of a job listing predict the role's pay?

#### Data Sources
Database of LinkedIn job listings (https://www.kaggle.com/datasets/arshkon/linkedin-job-postings).

#### Methodology
I have built a sentiment regression model that infers pay correlation from tokens in the description of a job listing.

Preparing the description data required tokenizing and lemmatizing job descriptions. I had to filter out listings that lacked any salary information. Of those that remained, I focused salary information to one number, using a single number if available, otherwise averaging the upper salary bound and lower salary bound. I also had to account for differences in currency and pay period, removing non-dollar rows and multiplying pay numbers as needed to be for the year.

#### Results
It has been difficult to crack a score of 0.7.

#### Next steps
I may try using an ensemble to take advantage of other models' strengths.