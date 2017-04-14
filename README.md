# Build a CRUD clone of Ebay
Forked from Dev Bootcamp, completed April 12, 2017.
Project time-frame: completed in an afternoon in 4 hours.
Completion - through release 8, did not implement user feedback/validation on whether their bid was successful or not.

## Summary
Project challenge: build a web-stack application including controllers, views, user authentication, database migrations, model validations, associations, etc.

## Skills Utilized
- Database/Schema design
- ActiveRecord, PostgreSQL
- Ruby, Sinatra
- HTML5/CSS3
- HTTP/REST/CRUD

### Web Application Overview
Goal was to build a simplified version of a blind auction site; in a blind auction, bidders do not see how much other bidders have bid.  Users will be able to register with the site, list items for auction, bid on items, etc.  We'll build the site one feature at a time.  The requirements for each feature are described in more detail in the *Releases* section.

### Release 0: User Registration
On the homepage, add a "register" link.  Clicking the link takes the user to a page with a form for creating a new account.  Users must register with an e-mail address, a username, and a password.  The e-mail address and username must be unique.


### Release 1: Login/Logout
Now that users can register, allow them to login and logout.  On the homepage, add a "login" link next to the "register" link.  Clicking the link takes the user to a page with a form for logging in.  Users sign in with an e-mail address and password.

Clicking the "logout" link logs the user out and redirects the user back to the homepage.

### Release 2: User Profile Page
Now that the application supports users, let's create a page to show a user's profile.  On the homepage, if a user is logged in, make the username a link.  Clicking the link takes the user to the profile page, which for now is a simple page welcoming the user.

### Release 3: List Items for Auction
Add a feature to allow users to list items available for auction.  Use the profile page for listing a user's items.

On the user profile page, add a link for listing a new item.  Clicking the link takes the user to a form.  The form should collect data like the item's name, the item's condition, and a description of the item.  It should also collect start and end times for the auction.

If listing the item is successful, the user should be redirected to the profile page where the item is listed by name.

### Release 4: Updating Items
If a user lists an item, they might wish to later make changes to that item:  change the name, the description, etc.  Let's add a feature, allowing users to edit their items.

On the profile page where a user's auctions are listed, create an "edit" link for each item.  Clicking the link takes the user to a form for editing the item.  The form should be populated with the item's current details.  Submitting the form makes a request to update the item.

### Release 5: Deleting Items
In the same way that users might need to edit an item, they might also need to delete an item.  Add a feature that allows users to delete items which they've previously listed.

On the profile page, add a "delete" button next to the "edit" link for each item.  Clicking the button should delete the item and redirect the user back to the profile page.

### Release 6:  Appropriate Behaviors per User and Route
Consider:
* Who can access the form to add an item?
* Who can access the form to edit a specific item?
* Who can edit a specific item?
* Who can delete a specific item?
* Who can view a specific user's profile?


### Release 7: Browsing Items
It's time to let users browse the items on our site.  Add a feature that lists the names of items that are currently up for auction and allows users to view a specific item's details.  Only list items for which the auction has started but not finished.  In other words, if the auction hasn't started yet, don't list the item.  If the auction is over, don't list the item.

On the homepage, list the name of each item that is currently up for auction.  The name should be a link.  Clicking the link should take the user to a page showing the details of that item auction.  Show the item's name, condition, and description along with when the auction ends.

### Release 8: Bidding
Add a feature that allows users to bid on items.  Bidding will occur on the page showing an item's details.

On the page showing an item's details, add a bidding section.  Include the number of bidders for the item and a form that accepts new bids.  When submitting if the bid is successfully created, the user should be redirected to the item's show page.  Instead of seeing a form for placing a new bid, the user should see the details of the bid.
