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

## A/B Test 2: Contact Button Display
User story 3 - user profile

**Metrics**
- Engagement: How actively users interact with other athletes through the Contact button.
- Task Success: How easily users find and use the Contact option on an athlete's profile.

**Hypothesis:** This A/B test aims to find out whether adding a Contact button to athlete profiles encourages more interaction between users. We believe that a visible Contact button will make it easier for users to contact other athletes and increase social interaction.

**Experiment:** Using Firebase Remote Config, Firebase A/B Testing, and Firebase Analytics, we will randomly divide users into two groups.
- Audience: Users who visit an Athlete Profile page will be randomly assigned to two groups(50% each).
- Group A: Users do not see a Contact button (Control).
- Group B: Users see a Contact button(Test).
- Duration: Run until enough users provide meaningful results.

Things to keep track of with Firebase Analytics Tracking:
- Profile_view - Visits to an Athlete Profile page.
- contact_button_click - Clicks on the Contact button.
- contact_action - Successful contact actions.

**Variation A - Without Contact Button (Control)**
The Athlete Profile page does not display a Contact button. Users can view athlete information and statistics, but cannot directly contact other athletes through the profile.

**Variation B - With Contact Button (Test)**
The Athlete Profile page displays a Contact button. Users can click the button to contact or connect with another athlete. This feature aims to make communication easier and encourage more interaction.

If Variation B results in higher engagement and more contact actions, we will consider adding the Contact button as a default feature. Otherwise, we will keep the current profile layout.

