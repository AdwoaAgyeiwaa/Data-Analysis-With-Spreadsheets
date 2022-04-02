# Analyzing Data
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
