# Read-write Excel files with ClosedXML

[ClosedXML](https://github.com/ClosedXML/ClosedXML) is a library for reading/writing Excel files (`.xlsx`). NuGet: ClosedXML.

```
/*/ nuget -\ClosedXML; /*/
using ClosedXML.Excel;

var file = folders.Temp + "ClosedXML.xlsx";
using (var workbook = new XLWorkbook()) {
	var worksheet = workbook.Worksheets.Add("Sample Sheet");
	worksheet.Cell("A1").Value = "Hello World!";
	worksheet.Cell("A2").FormulaA1 = "=MID(A1, 7, 5)";
	workbook.SaveAs(file);
}
run.it(file);
```