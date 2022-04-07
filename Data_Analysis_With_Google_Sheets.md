# Organizing Data
## Sorting from the Data Tab
This method uses the Data tab in the menu of your spreadsheet program.
### Sort by Sheet
When Sort Sheet is used, it sorts all of the data in a spreadsheet by the conditions of a single column, but the related information across each row stays together. This method is used more often than sorting by range.
1. On your computer, open a spreadsheet in Google Sheets.
2. At the top, right-click the letter of the column you want to sort by. 
3. Click Sort sheet A to Z or Sort sheet Z to A.

### Sort by Range
The information across rows is not kept together when using a sort range. When you sort a range, you are limiting the sorting to a specific collection of cells or a range. Except for the specified cells, nothing else on the spreadsheet is rearranged.
1. On your computer, open a spreadsheet in Google Sheets.
2. At the top, right-click the letter of the column you want to sort by. 
3. Click Sort range A to Z or Sort sheet Z to A.<br>
*Useful links:
https://www.youtube.com/watch?v=VcRBHXBMKBU*

### Custom Sort
1. On your computer, open a spreadsheet in Google Sheets.
2. Highlight the group of cells you'd like to sort.
3. If your sheet includes a header row, freeze the first row.
4. Click Data and then Sort range and thenAdvanced range sorting options.
5. If your columns have titles, click Data has header row.
6. Select the column you'd like to be sorted first and choose a sorting order. 
7. To add another sorting rule, click Add another sort column.
8. Click Sort.<br>
*Useful links:
https://www.youtube.com/watch?v=2dO4SDHKoPE*

## Sorting by Function
When you sort by function, you are actually changing the existing dataset, as opposed to rearranging the data in the original dataset when you use the Data tab in the menu.<br>
You do this by performing the following steps:
1. Type the equal sign, and then write SORT after it in an empty cell.
2. After your first open parenthesis, reference or type the range of your data.
3. Write a comma to separate the range from what we're sorting by.
4. Reference the corresponding column number you are sorting by and add another comma.
5. Decide whether you want the data in this column to be in ascending or descending order by typing TRUE or FALSE and close parenthesis: A TRUE statement is in ascending order, and FALSE is descending.
It should look something like this:<br>
`=SORT(range,sort_by_column_number,TRUE(or FALSE))`

# Formatting and Adjusting Data
## Combining Multiple Data in Different Cells
We can use the CONCAT function to combine multiple values in cells by typing the following function in an empty cell:<br>
`=CONCAT(cell1,cell2,...)`<br>
For spaces between values, we use:<br>
`=CONCAT(cell1," ",cell2)`

## Converting Data from One Unit of Measurement to Another
We perform the following function to convert from one unit of measurement to the other using the CONVERT function:<br>
`=CONVERT(cell,"unit_of_measurement1","unit_of_measurement2")`

## Validating Data
You can regulate what can and can't be entered in your spreadsheet with data validation in spreadsheets. Data validation is commonly used to provide drop-down lists to cells with specified alternatives for users to select. Because you have complete control over what is entered into the worksheet, you will spend less time afterwards cleaning up the data.<br>

## Conditional Formatting

# Manipulating Strings
## Finding the Length of a Textstring
We can use the `LEN` function to find the length of a textstring:<br>
`=LEN(cell)`<br>

## Finding a Particular Character Within a Textstring
We can use the `FIND` function to locate the position of a specific character(such as `" "`, `"&"`,`"t"`) or substring in a textstring. Keep in mind that this is case sensitive, thus make sure to input substrings correctly:<br>
`=FIND("character",cell)`

## Isolating a Substring from a Textstring
We can use the `LEFT` and `RIGHT` functions to select which parts of the string we want to isolate in a new column.<br>
The `RIGHT` function is to isolate a substring on the right side of the textstring.<br>
`=RIGHT(cell,position_of_last_character_substring_counting_from_the_end_of_the_textstring)`<br><br>
Likewise, the `LEFT` function is to isolate a substring on the left side of the textstring.<br>
`=LEFT(cell,position_of_last_character_substring_counting_from_the_beginning_of_the_textstring)`

# Data Aggregation using `VLOOKUP`
The process of gathering data from numerous sources and combining it into a single summarized collection is known as data aggregation. Data aggregation can provide you with a wealth of information about the data you're viewing.<br>
VLOOKUP is an abbreviation for vertical lookup. It is just a function that searches for a specific value in a column and returns the corresponding piece of information.

## Preparing for VLOOKUP
We must ensure that our data is appropriately prepared before using VLOOKUP to prevent getting errors. Clean data is significantly more likely to yield reliable findings.

### Converting Text to Numeric Values
To convert a text string that represents a number to a numerical value, the `VALUE` function can be used:<br>
`=VALUE(cell)`

### Removing Extra Spaces
When data is copied from one source to another, a few leading or trailing spaces may be included. We can use the `TRIM` function to get rid of this. TRIM automatically removes any additional spaces that have been added to the cell:
`=TRIM(cell)`

### Removing Duplicates of Data
If there are duplicate rows in the search, VLOOKUP will return only the first match it finds.`Remove duplicates` is a tool that searches for and removes duplicate entries from a spreadsheet automatically.<br>
1. Select the dataset from which you want to remove the duplicate records.
2. Click the Data option in the menu.
3. Click on the Remove Duplicates option.
4. In the Remove Duplicates dialog box, make sure ‘Data has header row’ is selected (in case your data has the header row).
5. Make sure ‘Select All’ is selected (in the ‘Columns to Analyze’ section).
6. Click on the ‘Remove duplicates’ button.

## VLOOKUP
Even if there are several possible matches, VLOOKUP only returns the first match it finds. It's also worth noting that VLOOKUP can only return a value from the data on the right - it can't look left.<br>
`=VLOOKUP(lookup_value, table_array_using_absolute_referencing, column_index_num, FALSE)`<br>
The argument `FALSE` returns an exact match while `TRUE` returns a close match. We will almost always want to return an exact match.<br><br>
Using VLOOKUP to populate data in one spreadsheet from another:<br>
`=VLOOKUP(lookup_value,'sheet_name'!table_array_using_absolute_referencing,column_index_num,FALSE)`

# Data Calculations
## Common calculation formulas
SUM
AVERAGE
MIN
MAX
## Functions
COUNTIF
SUMIF
## Conditions
