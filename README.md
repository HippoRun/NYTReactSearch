NYT React Search


Overview

In this activity, you'll create a new React-based rendition of the New York Times Article Search application. This assignment requires you to create React components, work with helper/util functions, and utilize the React mounting lifecycle to query and display articles based on user searches. You'll also use Node, Express and MongoDB so that users can save articles to read later.


Submission on BCS


Please submit both the deployed Heroku link to your homework AND the link to the Github Repository!



Instructions


Check out this mockup image. This explains how your site's components should function.
Create a MongoDB database called nytreact.
Using mongoose, then create an Article schema and model
At a minimum, articles should have each of the following fields:



title (Title of the stored article from nytimes.com)
date (publish date and time of the article)
url (URL of the article on nytimes.com)

Creating documents in your articles collection similar to  

 {
   title: 'Ali Sells Jersey House And Moves to Chicago',
   date: '1974-07-18T00:00:00Z',
   url: 'http://query.nytimes.com/gst/abstract.html?res=9A0DE5D8173FEF34BC4052DFB166838F669EDE'
 }




Create a Node/Express/MongoDB/ReactJS app called nytreact. This will be a recreation of the NYT Articles Search exercise application we built back in Unit 6. Running this application will:




Create a Bootstrap layout similar to that displayed in HW_Assignment.png. This should be a SPA (Single Page Application) that uses react-router-dom to navigate, hide and show your React components without changing the route within Express.


If you want to try out another CSS framework, feel free to use an alternative to Bootstrap.



You'll need several Express routes for your app:



/api/articles (get) - your components will use this to query MongoDB for all saved articles

/api/articles (post) - your components will use this to save an article to the database

/api/articles (delete) - your components will use this to delete a saved article in the database

* (get) - will load your single HTML page (with ReactJS) in client/build/index.html. Make sure you put this after all other GET routes



The layout should include at least two React Components for each page Home and Saved.



Home - contains all of the JSX to be rendered on the homepage. This component may contain other smaller components or JSX that renders plain HTML elements. This component should be able to query the NYT API for articles. It displays the results from the API search in a rendered list that displays the article title, publication date, and allows the user to visit an article's url or save the article to the MongoDB.

Saved - Renders articles that are saved in the MongoDB and allows the user to visit the article's url or delete it from the MongoDB. This page may be made up of multiple smaller components or JSX that renders plain HTML elements.


Deploy your application to Heroku once complete. Feel free to use the Mern Example as a starting point. You must use Create React App and current versions of React and React-Router-Dom for this assignment.









Bonus Live Updates to Saved Articles



Use React routing and socket.io to create a notification or a component that triggers whenever a user saves an article. Your message should include the title of the saved article.


Say you have multiple browsers open, each one visiting your site. If you save an article in one browser, then all of your browsers should notify you that a new article was saved.
Socket.io NPM package









