---
toc: False
layout: post
hide: False
title: My CPT Plans
courses: {compsci: {week: 19}}
type: plans
---
## Message board
In our clash royal themed project, my feature will be to create a place where all publicly shared desks can be seen. Upon clicking on one of them you will be able to read and review comments about this specific deck. Additionally there will be a rating system where each user leaves a /5 rating and this data can be averaged for sorting. A function will go through each comment to find keywords or characters that indicate a rating. In the "publicly shared" tab ther will be the option to view by newest uploaded, most popular, and highst rated.


Database Setup:

Set up a database to store comments related to each Clash Royale deck. Ensure you have a table that links comments to specific decks, and includes fields for comment content, user ID, timestamp, etc.
Backend/API Implementation:

Develop a backend/API to handle requests related to comments. Create endpoints for adding, retrieving, and updating comments.
Implement authentication mechanisms to ensure that only authorized users can leave comments.
User Interface Integration:

Integrate the comment system into the user interface of your Clash Royale project. This may involve adding a comment section to each deck's detail page.
Comment Form:

Create a form on the UI that allows users to input their comments. Include fields for the comment content and any other relevant details.
Comment Submission:

Implement a mechanism to submit comments to the backend when users fill out the comment form. Ensure that the necessary data (deck ID, user ID, comment content) is sent to the backend.
Backend Processing:

Develop server-side logic to process incoming comments. This includes validating input, associating comments with the correct deck, and storing them in the database.
Retrieving Comments:

Implement functionality to retrieve and display comments associated with a specific Clash Royale deck. This may involve making API requests to fetch comments when a user views a particular deck.
Displaying Comments:

Design a layout to display comments on the UI. Include user information, timestamp, and the comment content. Ensure that the comments are presented in a user-friendly and readable format.
Updating and Deleting Comments:

Implement features to allow users to edit or delete their own comments. Ensure that only authorized users can perform these actions.
Image: https://docs.google.com/drawings/d/10fjbCSRd3wqy5j-LwtVze9CZh1MSEpGAUOCRf8AUPFw/edit?usp=sharing