Download given excel file and unzip it.
```$unzip leaked_credentials.xlsx ```
You will see following files.
```Archive:  leaked_credentials.xlsx
  inflating: [Content_Types].xml     
  inflating: _rels/.rels             
  inflating: docProps/app.xml        
 extracting: [trash]/0000.dat        
  inflating: xl/_rels/workbook.xml.rels  
  inflating: xl/drawings/_rels/drawing1.xml.rels  
  inflating: xl/drawings/drawing1.xml  
  inflating: xl/sharedStrings.xml    
  inflating: xl/styles.xml           
  inflating: xl/theme/theme1.xml     
  inflating: xl/workbook.xml         
  inflating: xl/worksheets/_rels/sheet1.xml.rels  
  inflating: xl/worksheets/sheet1.xml  
  inflating: docProps/core.xml    ```
  
  I searched in all folders.Finally when I read xl/workbook.xml, I saw a name in "url="C:\Users\bhonehtetx0x1\Desktop\""
  ```<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<workbook xmlns="http://schemas.openxmlformats.org/spreadsheetml/2006/main" xmlns:r="http://schemas.openxmlformats.org/officeDocument/2006/relationships" xmlns:mc="http://schemas.openxmlformats.org/markup-compatibility/2006" mc:Ignorable="x15" xmlns:x15="http://schemas.microsoft.com/office/spreadsheetml/2010/11/main"><fileVersion appName="xl" lastEdited="6" lowestEdited="6" rupBuild="14420"/><workbookPr/><mc:AlternateContent xmlns:mc="http://schemas.openxmlformats.org/markup-compatibility/2006"><mc:Choice Requires="x15"><x15ac:absPath url="C:\Users\bhonehtetx0x1\Desktop\" xmlns:x15ac="http://schemas.microsoft.com/office/spreadsheetml/2010/11/ac"/></mc:Choice></mc:AlternateContent><bookViews><workbookView xWindow="-120" yWindow="-120" windowWidth="20736" windowHeight="11160"/></bookViews><sheets><sheet name="Sheet1" sheetId="1" r:id="rId1"/></sheets><calcPr calcId="162913"/><extLst><ext uri="{140A7094-0E35-4892-8432-C4D2E57EDEB5}" xmlns:x15="http://schemas.microsoft.com/office/spreadsheetml/2010/11/main"><x15:workbookPr chartTrackingRefBase="1"/></ext></extLst></workbook>
  ```
  MCSC{bhonehtet0x1}</br>
  
  
  
