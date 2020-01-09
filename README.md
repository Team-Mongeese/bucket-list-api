## An explanation of the what the app does and how it works.
Bucket List is an app for adventurers of all stripes to be able to track items in their own, individual bucket list to help them achieve their life’s goals.
Using Mongoose, the user is able create an account with email and password, that only they can see. From there, they can create “Goals” on their bucket list and add it to their MongoDB database. These "Goals" can be updated with new "titles" or "descriptions" if the user provides id of the goal (available of the "bucket list" index). They are also able to update the status to Complete, yes, if they have crossed it off their list. If the user no longer has passion for one of their goals, they can also delete the goal completely. While accessing their account, they can change their passwords and then ultimately log out so they can go pursue their dreams! 
## Front end repo
Front-end Repository: https://github.com/Team-Mongeese/bucket-list-client
## Deployed Site links
Client: https://team-mongeese.github.io/bucket-list-client/

Heroku API: https://powerful-meadow-13173.herokuapp.com/
## List of technologies used:
* Node js
* packages
  * bcrypt
  * cors
  * dotenv
  * express
  * jsonwebtoken
  * mongodb
  * mongoose
  * passport
  * passport-http-bearer
* Mongoose
* MongoDB

## List unsolved problems which would be fixed in future iterations.
- Add a GPS location feature to each goal item on a user's bucket list.
## Document your planning, process and problem-solving strategy
Link to Entity Relationship Diagram (ERD) and Wireframes - https://imgur.com/a/4kVBZt8
We began with a team meeting to nail down our process. During this meeting, we assigned roles to each delta and pairs to handle the frontend and backend at the same time without merge conflicts issues.
In pairs, we assigned a pilot and a navigator. For the backend pair, we first completed the routes and models. We initially had issues restricting viewing to just the owners of the resources, but made a decision to leave that as a reach goal, which we did complete during the timeframe of our project deployment.
After completing the back end, we deployed it so that the front end team could incorporate both parts to get a version 1 of the application.
Everyday consisted of three 15 minute stand-ups where we touched base about how far along we came in a Sprint (Sprints were approximately 3 hours long) at 9:05A, 11:45A, 3:30P. During the process, we ended up adding an unofficial meeting at the end of day 4:40P, as well.
There ended up being no merge conflicts on the backend of our repo.

| verb   | path             | parameters                                                          |
|--------|------------------|---------------------------------------------------------------------|
| POST   | /sign-up         | `credentials` with `email`, `password`, and `password_confirmation` |
| POST   | /sign-in         | `credentials` with `email`, and `password`                          |
| PATCH  | /change-password | AUTH `passwords` with `old` and `new`                               |
| DELETE | /sign-out        | Auth                                                                |
| GET    | /goals           | Auth                                                                |
| GET    | /goals/:id       | AUTH                                                                |
| PATCH  | /goals/:id       | AUTH, OWNER `goal` with `title` and `description` and `status`                   |
| DELETE | /goals/:id       | AUTH, OWNER                                                         |
