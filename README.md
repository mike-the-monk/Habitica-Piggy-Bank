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
6. Start over, but clicking the Piggy Bank Creation reward.

Currently, this is a work in progress and does not yet work. It is not yet ready for testing.
