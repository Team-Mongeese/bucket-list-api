## An explanation of the what the app does and how it works.
Bucket List is an app for adventurers of all stripes to be able to track items in their bucket list to help them achieve their life’s goals.
Using Mongoose, the user is able to create “Goals” and add it to their MongoDB database. 
## Front end repo
Front end repository: https://github.com/Team-Mongeese/bucket-list-client
## Deployed Site links
client: https://team-mongeese.github.io/bucket-list-client/

heroku api: https://powerful-meadow-13173.herokuapp.com/
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
* MonogDB

## List unsolved problems which would be fixed in future iterations.
Restrict the viewing of Goals to only the owner of the goal.
## Document your planning, process and problem-solving strategy
Link to Entity Relationship Diagram (ERD) - https://imgur.com/a/4kVBZt8
We began with a team meeting to nail down our process. We assigned roles and pairs to handle the frontends and backend.
In pairs, we assigned a pilot and a navigator. We first completed the routes and models. We initially had issues restricting viewing to just the owners of the resources but made a decision to leave that as a reach goal.
After completing the back end we deployed it so that the front end team could incorporate both parts.

| verb   | path             | parameters                                                          |
|--------|------------------|---------------------------------------------------------------------|
| POST   | /sign-up         | `credentials` with `email`, `password`, and `password_confirmation` |
| POST   | /sign-in         | `credentials` with `email`, and `password`                          |
| PATCH  | /change-password | AUTH `passwords` with `old` and `new`                               |
| DELETE | /sign-out        | Auth                                                                |
| GET    | /goals           | Auth                                                                |
| GET    | /goals/:id       | AUTH                                                                |
| PATCH  | /goals/:id       | AUTH, OWNER `goal` with `title` and `description`                   |
| DELETE | /goals/:id       | AUTH, OWNER                                                         |