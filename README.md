# Habitica-Piggy-Bank
Piggy Bank Script for Habitica

This is a google script for Habitica that allows you to create "Piggy Banks". A Piggy Bank in this term is a reward that you can "pay down". Essentially, set your goal, and as you earn gold, you can incrementally keep going until you've reached your goal. 

What's the script flow like?

Once the user configures the script with the needed api information and weburl information, the following steps will need to take place:

1. User clicks a '0' gold reward made by the script. This creates a new 'Piggy Bank'.
2. User edits the Piggy Bank details, careful not to remove any identifiers in the reward.

   a. Piggy Bank Title
   
   b. Goal Amount
   
   c. How much you've saved (should be zero to start).
   
   d. Reward amount to purchase incrementally (100-200 gold should generally suffice).
   
3. Click the new reward's purchase button, and it will change the Saved amount by an addition of that amount.
4. When you reach your goal, the goal will change the description to add a picture and celebratory phrase (variable)
5. Click the reward's purchase button again to have it removed.
6. Start over, by clicking the Piggy Bank Creation reward.

Currently, this is a work in progress and does not yet work. It is not yet ready for testing.


```
Coding outline:



*api information
*acript author information
*constants for "create" button
*constants for "piggy bank" button
*increment alias
*error message constants

*doOneTimeSetup function
	*Create button
	*Create webhook
	*set script "cookie"
*doPost function
	*check button alias
		*If button base is true (i.e. not a new button)
	*find index locations of each search term (goal, saved, title, increment, should delete button)
	*check formatting
	*split into substrings 
	*validate numbers are numbers
	*create notes for button
	*Build new button
	*create button
*When clicking an existing bank button
	*get GP value of button
	*check if button should be deleted
		*if it should, delete and refund gold
	*check string formatting
	*find semicolons
	*split into substrings
	*check if they're numbers
	*add gp value to amount saved
	*check if new amount saved exceeds goal
	*VICTORY DANCE (update button details)
	*Create updated notes section for the button
	*return htmlservice create html output
*api_createNewTaskForUser function
*apiMult_createNewWebHookNoDuplicates function
*getWebHooks function
*createNewWebHook function
*initScriptProperties function (sets initial properties that will be used/saved later)
*findIndex function
*findIndexSemicolon function (for formatting an adding offset) (what is this??)
*checkStringFormatting function (verify format and number of semicolons)
*checkSearchTerms function (If the notes and title are all wrong, it throws an error)
*checkSemicolons function (ensures the proper order of items)
*checkOrder function (verifies order)
*createSubstring function (gets rid of whitespace)
*checkIfNumber function (verifies if substring is a number)
*sendPrivateMessageAlways function (send notifications always)
*getAuthenticatedUserProfile function (grabs user information like mana, xp, level, etc.)
*getUserTasks function (grabs all the user's tasks)
*updateUser function (updates the user's information?)
```
