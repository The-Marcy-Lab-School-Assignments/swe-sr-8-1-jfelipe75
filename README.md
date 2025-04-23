# swe-sr-8-1

For guidance on setting up and submitting this assignment, refer to the Marcy lab School Docs How-To guide for [Working with Short Response and Coding Assignments](https://marcylabschool.gitbook.io/marcy-lab-school-docs/fullstack-curriculum/how-tos/working-with-assignments#how-to-work-on-assignments).

## Prompt

![Fullstack Diagram](./client-server-database-diagram.svg)

You’ve been given a diagram (see above) showing the three core layers of a fullstack application:

- Frontend – a React application that users interact with
- Backend – an Express server that handles logic and communication
- Database – a PostgreSQL database that stores persistent data

Imagine you’re explaining how these layers work together by using a real-world example: Instagram.

Your task:

1. Explain how Instagram works using the three-layer diagram.

   - What happens when a user opens the app, scrolls through their feed, likes a post, or uploads a new photo?
   - Walk through how data flows from the frontend to the backend and to the database—and back again.

---

### Answer

When a user initially opens the app, he or she is making a request to instagram's server to serve them the HTML,CSS and JavaScript static files. from the server files instagram will query the most recent posts and user information in the Database to be displayed first.

## If a user likes a picture in his feed, then we would make a INSERT INTO query into a table with four columns, (id, picture, likes, comments) then we would update the like counter using the id of the picture to update the post's like counter

2. Come up with an analogy to help someone new to coding understand these layers.

- You might compare the system to something like a restaurant, a library, or even a post office—anything that helps make the roles of each layer intuitive.
- Make sure your analogy maps clearly to the roles of the frontend, backend, and database.

---

### Answer

Imagine the frontend is the restaurant's menu, Through our frontend users are able to interact with the food items, wether is just reading through them or actually making an order, this all starts in the client layer (frontend).

The backend is the restaurant itself, think of it as the brain connecting everything, We have waiters taking orders from people and sending them to our Chef, our database and then serving each customer the right meal.

## And the database is the chef mixing all the ingredients to formulate queries in order retrieve meaningful data from the database.

3. Reflect on the value of this separation.

- Why do we separate concerns into these layers?
- What would go wrong if we tried to do everything in one layer?

Audience: Imagine you're writing this for someone who's just starting out in web development and wants to understand how modern apps work.

Length: Around 400–600 words.

### Answer
