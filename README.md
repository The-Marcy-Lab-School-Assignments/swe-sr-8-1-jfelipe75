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

## If a user likes a picture in his feed, then we would make a INSERT INTO query into a table with four columns, (id, picture, likes, comments) then we would update the like counter using the id of the picture to update the post's like counter

2. Come up with an analogy to help someone new to coding understand these layers.

- You might compare the system to something like a restaurant, a library, or even a post office—anything that helps make the roles of each layer intuitive.
- Make sure your analogy maps clearly to the roles of the frontend, backend, and database.

---

## And the database is the chef mixing all the ingredients to formulate queries in order retrieve meaningful data from the database.

3. Reflect on the value of this separation.

- Why do we separate concerns into these layers?
- What would go wrong if we tried to do everything in one layer?

Audience: Imagine you're writing this for someone who's just starting out in web development and wants to understand how modern apps work.

Length: Around 400–600 words.

### Article

# Understanding a Fullstack Application Through Instagram

## How Instagram Works Across Three Layers

When a user opens Instagram, they are making a request to Instagram’s server to deliver the static files — **HTML**, **CSS**, and **JavaScript** — that make up the **frontend**. These files allow the user to interact with Instagram’s platform.

Once the frontend is loaded, if the user scrolls through their feed, likes a post, or uploads a photo, the frontend sends requests to the **backend**, an Express server in a typical fullstack setup. The backend processes the user’s actions, translates them into operations, and communicates with the **database**.

For example:

- **Scrolling the feed**: The frontend sends a request to the backend, which queries the database for the latest posts, and sends them back to be displayed.
- **Liking a post**: The frontend sends a like action. The backend updates the likes count in the database for that particular post (likely identified by a unique ID).
- **Uploading a photo**: The frontend sends the photo to the backend, which saves it (often in cloud storage) and stores metadata (such as user ID, time, and description) in the database.

Thus, data flows like this:
**Frontend ➔ Backend ➔ Database ➔ Backend ➔ Frontend**

---

## A Helpful Analogy: The Restaurant Model

Imagine the three layers as parts of a restaurant experience:

- **Frontend (Menu and Waiter)**: The menu is like the user interface. It shows users (diners) what they can do (order food, ask for water, etc.). The waiter takes your orders and serves you, acting as the user’s connection to the kitchen.
- **Backend (Kitchen Operations)**: The kitchen is the backend. It receives orders from the waiter (frontend), processes them (prepares food), and sends back the final dishes.
- **Database (Ingredients in the Pantry)**: The pantry holds all the raw ingredients needed to make the food. It’s the database storing persistent information (posts, users, likes).

When you order food, the waiter (frontend) communicates with the kitchen (backend), which pulls ingredients (data) from the pantry (database) to prepare your meal and serve it to you.

---

## Why the Separation Matters

Separating concerns into three layers keeps the system clean, efficient, and maintainable.

- **Frontend** focuses only on the user experience.
- **Backend** focuses only on business logic and communication.
- **Database** focuses only on data storage and retrieval.

If everything were lumped into a single layer, it would be chaotic:

- UI changes could break backend logic.
- Database issues could crash the whole app.
- Updating features would become incredibly difficult.

By maintaining clear boundaries, developers can work on the user interface without worrying about database queries, and database engineers can optimize storage without breaking the app’s look and feel. It enables teams to move faster, build more complex applications, and create better user experiences.

---
