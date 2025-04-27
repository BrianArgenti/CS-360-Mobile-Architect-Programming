# CS-360-Mobile-Architect-Programming
- **Briefly summarize the requirements and goals of the app you developed. What user needs was this app designed to address?**

  For this event-tracking app I was required to create a login screen that would support entering a username and password. A second requirement was to have a sign-up function for those who are using the app for the first time. A database consisting of two tables were needed, one to hold the user's login information and another to hold the data for the events that would be entered. Once logged in, the app would need to transition to a screen that showed the user their upcoming events in a grid form. A way to add and remove events were necessary, as well as a function to notify the user on the day of the event via SMS text. The event data itself required a details field and datetime field in order to populate the event list page. 

---
- **What screens and features were necessary to support user needs and produce a user-centered UI for the app? How did your UI designs keep users in mind? Why were your designs successful?**

  To support user needs and create a user-centered UI, I first designed a login and signup screen that would appear immediately when the app was activated. This screen featured two text fields with hint text, guiding users to enter their username and password. Beneath the fields, two buttons allowed users to either sign in or sign up, depending on whether they had previously registered. Once logged in, users were taken to another activity that displayed their upcoming events. If no events were scheduled, a simple message informed the user. Otherwise, their events were presented in a scrollable list, with each list item including a delete button for removing events that were no longer relevant. A floating action button positioned near the bottom-right corner of the screen gave users a quick way to add new events. Tapping this button brought them to a form where they could input event names, details, and date-time information through clearly labeled text fields. A checkbox allowed users to opt-in for SMS text notifications about their events. Below the form were two buttons—one to submit the event and another to return to the event list.

  The design kept the user in mind by maintaining simplicity and minimizing distractions. Clear navigation and straightforward layouts made it intuitive for users to know where to enter their information. Keeping the event list as a scrollable grid ensured that all event information remained on a single screen, reducing the need for users to navigate through multiple pages. This focus on clarity and accessibility helped make the design successful in meeting user needs.

---

- **How did you approach the process of coding your app? What techniques or strategies did you use? How could those techniques or strategies be applied in the future?**

    I began the coding process by carefully interpreting the user requirements and using them to create a wireframe of the app. Building the wireframe allowed me to visualize the structure of the app and how the code would need to be implemented. Using the wireframe as a guide, I developed the view layer within the .xml files, successfully recreating the models I had sketched out. This preparation made it much easier to transition into writing the Java code that would handle user inputs and interactions.

  For the event list feature, I implemented a RecyclerView, which allowed me to create a scrollable, dynamic list of user events. RecyclerView is a powerful and versatile tool that can be applied in many future projects where organized, efficient list displays are needed. It offers flexibility and performance benefits that make it ideal for handling larger data sets within an app.

  I also implemented an SQLite database and built a controller to manage user-supplied information, inserting it into the appropriate data tables. To improve data integrity and security, I added validation statements to ensure usernames were unique and that users could not sign in without first registering. These strategies introduced important error-handling measures and helped secure the app's data. Moving forward, this approach of combining wireframing, modular development, and early validation techniques will be valuable for building more complex and secure applications.

---

- **How did you test to ensure your code was functional? Why is this process important, and what did it reveal?**

  I tested the code manually by running different scenarios, such as attempting to sign up with two accounts using the same username or trying to sign in with a username that wasn’t already in the database. These tests helped me verify that the validation logic and error handling were working as intended. Although I would have liked to automate the testing process, the short timeline for building the app, along with its relative simplicity, made manual testing the most practical approach. To stay on track, I tested each major function as I implemented it, which helped me catch issues early without falling behind schedule.

  However, I recognize that this is not the ideal long-term strategy. Manual testing can miss subtle bugs, especially as the complexity of an application grows. I am aware there are likely some bugs that I did not catch through manual testing alone. This experience reinforced the importance of thorough and continuous testing throughout the entire development process. Comprehensive testing is critical for ensuring not only that the code works as expected, but also that edge cases and rare issues are identified before they become major problems. In future projects, I plan to incorporate more structured and automated testing techniques, such as writing unit tests and using testing frameworks, to make the apps I develop more robust and reliable.

---

- **Consider the full app design and development process from initial planning to finalization. Where did you have to innovate to overcome a challenge?**

  When first conceptualizing the app, my initial idea was to display the list of items in a grid layout that would show only a preview of each event. Clicking on an event would then expand it to reveal additional details and options, such as the ability to delete the event. However, as I began planning the implementation, I quickly realized that this functionality would require much more complex code. It also raised usability concerns; hiding important functions like the delete option might confuse or frustrate users especially when first using the app.

  Recognizing these potential issues, I decided to rethink the approach. I innovated by choosing to use a RecyclerView, which provided a cleaner and simpler way to display a scrollable list of events while maintaining good performance. Instead of hiding actions within expanded views, I moved the delete button directly onto each event card, positioning it clearly at the lower-right corner. This adjustment greatly improved the user experience by making important actions immediately visible and accessible, while also significantly reducing the complexity of the code I needed to write.

---

- **In what specific component of your mobile app were you particularly successful in demonstrating your knowledge, skills, and experience?**

   I was particularly successful in demonstrating my knowledge, skills, and experience when implementing the SQL database and creating the necessary tables for the app. Setting up the database structure, inserting user data, and managing queries were especially satisfying milestones to achieve. Although I had previous experience working with SQL and SQLite, I had never applied them in a mobile development context where the database needed to directly interact with a user interface and support user login and registration.

  One of the biggest successes was being able to store usernames and passwords securely and perform validation checks during the login process. Ensuring that users could not sign in without registering first, and verifying that no duplicate usernames could be created, showed that I could apply both the theoretical knowledge from class and practical database management techniques in a real-world app environment.

  Successfully integrating the database without encountering major issues made me feel confident that I had fully understood the concepts taught throughout the course. It also reinforced my ability to troubleshoot and think critically about data management in app development. This experience will be extremely valuable in future projects where reliable data storage, user authentication, and smooth backend integration are essential parts of the app’s functionality.
