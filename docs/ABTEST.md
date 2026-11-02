## A/B Test 1: Post acc creation nav to network discovery / nav to user profile finish setup ##
User story 1 & 2 - Login / account creation

Metrics: uses HEART metrics of 
  Engagement - how frequently do users interact with the EventDiscovery page
  Adoption - the percent of signed up users who begin using the app's game finding      features
  Task Success - How quickly users find games and complete an action, such as viewing
  game details or signing up.

Hypothesis: This A/B testing is trying to determine if taking users to the EventDiscovery page after logging in increases engagement with the app instead of taking them to the UserProfile page. Our golden path focused on finding games for now so it would make more sense that users wouldn't want to spend too much time fleshing out their accounts vs using the app for its main feature. Taking users to the Event Discovery page after login or sign up would increase user engagement and reduce the number of steps to accessing that feature. Potentially users could verify their accounts in the future.

Experiment: using Firebase remote config, Firebase A/B Testing, Firebase Analytics, we will randomly divide our user base into 2 groups.
  Audience: 50% logged in users will participate. This total includes all users, new
  and returning
  Group A: Users are directed to their account and profile page after logging in
  Group B: Users will be taken to the EventDiscovery page after login/signup
  Duration: Run until enough users give meaningful results
  Things to keep track of with FireBase Analytics Tracking:
    -successful logins
    -which page users are directed to with landing_page parameter
    -game_view parameter for when users open game listing
    -oppertunity_signup parameter for when users signup for a game
    -account_view parameter for visits to user account page

Variation A - User Account redirection (Control)
Users are directed to peronal account page immediatly after login in. From there, they can nav to other pages using app's nav bar at the bottom of the page.

Variation B - Find Events Page (Test)
Users are directed immediately to EventDiscovery page to browse all available listings without needing to navigate away from initial landing page.

If variation B results in more game views and signups, we make the EventDiscovery page the default. If not, we keep the landing page after login/signup on user profile pagee.

## A/B Test 2: Athlete Statistics Display
User story 3 - user profile

**Metrics**
- Engagement: How actively users explore and interact with athlete statistics on the Profile page.
- Task Success: How easily users find and understand specific athlete performance statistics.

**Hypothesis:** This A/B test is trying to determine whether displaying athlete statistics in individual cards instead of a simple list improves the user experience. The current list layout may make it harder for users to quickly identify important performance information. We believe that a card-based layout will make statistics easier to scan, understand, and compare, encouraging users to explore more information on an athlete's profile.

**Experiment:** Using Firebase Remote Config, Firebase A/B Testing, and Firebase Analytics, we will randomly divide users into two groups.
- Audience: Users who visit an Athlete Profile page will be randomly assigned to two groups(50% each).
- Group A: Users see the current list layout(Control).
- Group B: Users see the new card-based layout(Test).
- Duration: Run until enough users provide meaningful results.
Things to keep track of with Firebase Analytics Tracking:
- Profile_view - Visits to an Athlete Profile page.
- statistics_view - Views of the athlete statistics section.

**Variation A - List Layout (Control)**
Athlete statistics are displayed in a simple vertical list, with each statistic shown alongside its corresponding value.

**Variation B - Card Layout (Test)**
Athlete statistics are displayed in individual cards, with each card showing a statistic and its corresponding value. This layout aims to make information easier to scan and understand.

If Variation B results in better user engagement and task success, we will consider adopting the card layout as the default. Otherwise, we will keep the current list layout.

