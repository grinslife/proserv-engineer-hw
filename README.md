# Professional Services Engineering Homework

## Instructions

Please clone this repository and deliver your solutions in an archive format of your choice (e.g. zip or tarball), including the entire contents of this repo along with your answers.
 _Do not submit your solution via pull request to this repository._


## Questions

1. Download http://www.google-analytics.com/ga.js to a file named ga_local.js on your machine.
   1. How did you accomplish this?
   1. This file is full of a lot of gibberish. Are there more instances of the character a or g? How many of each? How did you determine this?
   1. Google has sensibly chosen size over readability for this file. Suppose that for your local copy, however, you wanted to rename the variables a, b, c, and g to apple, banana, carrot, and grapefruit. How would you do this?


1. Use the HTML and CSS files in the src folder for the following tasks. Make changes to the HTML and CSS files as needed. Attach your modified versions of the code with your answer sheet when returning it to Opower.
   1. The HTML file doesn’t have any styling right now. Add a snippet of code to navigation.html to load the style.css file.
   1. The navigation is boring. Add one or two subnavigation tabs below the active tab which appear only when you hover over the main tab. Change the HTML or CSS files as needed.
   1. There are some bits of CSS that are currently unused between these two files. How would you find this unused code? And can you identify the who made the commit?

1. Use the customer_email_template.html in the src folder for the following questions.  Make changes to the html file as needed.  Attach your modified version of the code with your answer sheet when returning it to Opower.
   1. This email does not use a basic but important accessibility feature.  What is it?  Please correct this issue.
   1. This email is not responsive for smaller displays such as phone screens.  Please add some styling that will kick in for screen sizes smaller than 500 pixels.
   1. Note the use of both inline styling and CSS embedded in the <style> tag.  Explain the reasoning behind this.
   1. What about the structure of layout ensures that it will be consistent across as many email clients as possible?
   1. Add pre-header text to the html so that it will display in email clients, but not in the html itself.

4. Write standard SQL syntax that will create a ‘users’ table, including indexes, with the following structure:

   ```
   id (integer, primary key)
   username (string)
   email (string)
   signup_date (date)
   ```

   1. Imagine that this table does not enforce uniqueness on username. An application that uses this table has allowed the table to be “corrupted” by allowing multiple users to sign up with the same username. Write SQL that would generate a list of the usernames and the most recent signup_date for that username, for all usernames that have multiple instances in the table.
   1. Write SQL that will generate a list of unique email addresses for all the usernames returned in (i)
   1. Imagine your schema includes a second table ‘user_actions’ that contains a ‘user_id’ column that is a foreign key to the ‘users.id’ column. Write SQL that will return the usernames and emails for all users in the ‘users’ tables that have no rows in the ‘user_actions’ table.
   1. Imagine your “corrupted” table has magically been cleaned such that no username exists on multiple rows in the table. Write SQL that will modify the structure of the table that will enforce that the multiple username scenario cannot reoccur.


1. For the two endpoints https://api.github.com/users/opower/repo and https://api.github.com/users/opower/repos
   1. What are the returned status codes for both? And which is the valid one?
   1. Github's API by default is limited to 30 items being returned. Using the github API docs (found here https://developer.github.com/v3/) how would you increase the number of items returned by the valid endpoint?
   1. Using this parameter is it possible to get 200 repos returned in one API call? What can you do to have all repos returned
   1. Create an algorithm to parse out the names returned for all repos
