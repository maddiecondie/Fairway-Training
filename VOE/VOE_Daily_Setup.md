# CURRENT VOE WORKFLOW
    
# Making the VOE Report
Generate VOE-TODO from Public reports in Encompass.

### ADDING FORMATTING:
Select Borr Self Employed Column.
Home > Conditional Formatting > Highlight Cells Rules > Equal To > "Y" turn PINK

Select Closing Date or Funding Date column.
Home > Conditional Formatting > Manage Rules > Use a formula to determine which cells to format > Input formula and pick corresponding color


#### CLOSING DATE

+ `= AND(AND(((TODAY() - 6) <= E1), (TODAY() + 7) > E1), OR(NOT(ABS(E1 - K1) <= 7), ISBLANK(K1)))` - LIGHT PINK
+ `=AND(TODAY() = E1, OR(NOT(ABS(E1 - K1) <= 7), ISBLANK(K1)))` - DARK PINK



#### FUNDING DATE
+ `=AND(AND(WORKDAY(TODAY(),3) > F1, TODAY() <= F1), E1 <= F1)` - LIGHT PINK
+ `=AND(WORKDAY(TODAY(),1) = F1, E1 <= F1)` - DARK PINK
+ `=AND( F1 = TODAY(), E1 <= F1)` - RED

Insert new column right before Borrower Name: VOE Team Member.

### SORTING AND FILTERING
Click top left small grey triangle THEN click Sort & Filter in top right. Click Filter.
Sort Closing Date oldest to newest then sort Funding Date oldest to newest.

Filter VOE Missing Alert column to only show cells with "1".

Assign each loan to proper person.

### COLOR CODING
Color codes for VOE team names column: 
Green - Completed
Yellow - Begun But Ran Into Problem / Waiting
Blue - Currently In Progress

Color codes for borrower name column:
Purple - URGENT

Color codes for business address column:
Orange - Even or west of Utah
Blue - East of Utah

### TIME MANAGEMENT
Prioritize your day by getting done with Funding today and tomorrow first (going east to west preferably).

### CLOUD EDITING
Once you've created and formatted the report, upload it to your Fairway OneDrive account, and then upload that file from OneDrive into this chat.
If you've got the OneDrive app set up on your local machine, you can drag the file from there into the chat box here in this channel.
