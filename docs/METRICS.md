
# AthleteHub Metrics

## Google HEART Framework

[View AthleteHub HEART Framework](https://docs.google.com/presentation/d/1mOXiwgA1cA9rYEv0ehtLKjBQ5m0XRI-kZqi8VUbsSuw/edit?usp=sharing)


| HEART Category | Metric | Goal |
|---|---|---|
| Happiness | Net Promoter Score (NPS) | Measure athlete satisfaction and willingness to recommend AthleteHub |
| Engagement | Daily Active Users (DAU) | Track how many athletes actively use the app each day |
| Adoption | New User Signups | Measure how many new athletes register |
| Retention | 7-Day Retention Rate | Track how many athletes return after signing up |
| Task Success | Profile Setup Completion Rate | Measure how many athletes successfully finish setting up their profiles |
| Task Success | Get Started Click-Through Rate (CTR) | Measure how many users click Get Started during onboarding |

## How We Will Collect Each Metric

- **NPS:** Ask users how likely they are to recommend AthleteHub on a scale of 0 to 10. Store responses in Firebase and calculate the percentage of promoters minus detractors.
- **Adoption:** Use Firebase Authentication account creation timestamps to count new registered users.
- **DAU:** Use Firebase Analytics activity data to measure unique active users each day.
- **Retention:** Use Firebase Analytics retention reports to measure how many new users return seven days after signup.
- **CTR:** Track a custom Firebase Analytics event when users click the Get Started button. Divide unique users who click by unique users who see the onboarding screen.
- **Profile Setup Completion:** Record a custom event when an athlete finishes profile setup. Divide completed profiles by users who started profile setup.

