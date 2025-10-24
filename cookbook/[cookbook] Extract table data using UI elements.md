# Extract table data using UI elements

Code like this can be used to extract data from cells in a table displayed in a web browser or any window.

```
print.clear();
var w = wnd.find(1, "HTML Tables - Google Chrome", "Chrome_WidgetWin_1");
var rows = w.Elm["web:TABLE", prop: "@id=customers"]["ROW", prop: "level=0"].FindAll(); //find the table and get its rows
for (int ir = 0; ir < rows.Length; ir++) { //for each row
	if (ir == 0) continue; //header
	var a = rows[ir].Elm[prop: "level=0"].FindAll(); //get cells in this row
	//print.it(rows[ir]); print.it(a.Select(o => $"\t{o.Role},  {o.Name,-30},  {o.Rect}")); //debug
	print.it(a[0].Name, a[1].Name, a[2].Name); //get data from UI elements
	//print.it(a[1].Navigate("fi").Name, a[2].Elm["LINK"].Find(0).Name); //examples: get or find an element inside the cell
}
```

The above code is for a standard simple HTML table. Example: https://www.w3schools.com/html/html_tables.asp Many HTML tables aren't so simple. Often they are even not true HTML tables (TABLE/ROW/CELL). Often cells contain multiple elements; they are different in each column, and sometimes even different in some rows. Code like the above example can be used with such nonstandard or complex tables too, but may need more editing. In https://www.libreautomate.com/forum you can find some real scripts that extract data from complex tables and solve various problems. Search for posts containing text *elm* and *FindAll*. And of course ask for help if need.

To create code, use the **Find UI element** tool, action **FindAll, table**. Recommended steps:

1. Capture the first row or header of the table. Or capture any element in the row, and in the tree select the row element (which contains the captured element).
2. Uncheck **name** etc (because need to find all rows, not just the selected row). In some cases also may need to set level (usually 0).
3. Check **Add to path**.
4. In the tree select the table element (which contains the row).
5. Check **Add to path**.
6. Click **Test** and make sure it finds a row in that table (any row, or header). If it doesn't, use usual ways to make it find that table, for example use **skip**, **navig**, **Reverse**, HTML attributes, or add more elements to the path.
7. In the action combo box select **FindAll, table**.
8. Click **Insert**. Don't close the tool yet, as it can be useful when editing the inserted code.
9. Run the script to test how it works.
10. Edit the inserted code. For example, a cell may contain multiple elements, and you may want to get one/some of them. Use the tree view in the tool to discover these elements. The tool inserts examples and testing/debugging code.