## Save in MS Office formats
```bash
FILE="$HOME/.config/libreoffice/4/user/registrymodifications.xcu"; \
sed -i '/<item oor:path="\/org.openoffice.Setup\/L10N">/a\
<item oor:path="/org.openoffice.Setup/Office/Factories/org.openoffice.Setup:Factory['\''com.sun.star.presentation.PresentationDocument'\'']"><prop oor:name="ooSetupFactoryDefaultFilter" oor:op="fuse"><value>Impress MS PowerPoint 2007 XML</value></prop></item>\
<item oor:path="/org.openoffice.Setup/Office/Factories/org.openoffice.Setup:Factory['\''com.sun.star.sheet.SpreadsheetDocument'\'']"><prop oor:name="ooSetupFactoryDefaultFilter" oor:op="fuse"><value>Calc MS Excel 2007 XML</value></prop></item>\
<item oor:path="/org.openoffice.Setup/Office/Factories/org.openoffice.Setup:Factory['\''com.sun.star.text.TextDocument'\'']"><prop oor:name="ooSetupFactoryDefaultFilter" oor:op="fuse"><value>Office Open XML Text</value></prop></item>' "$FILE"
```

## SVG icons (run second time after reopening LibreOffice)
```bash
FILE="$HOME/.config/libreoffice/4/user/registrymodifications.xcu"; \
sed -i '/<item oor:path="\/org.openoffice.Office.Common\/Misc"><prop oor:name="FirstRun" oor:op="fuse"><value>false<\/value><\/prop><\/item>/a\
<item oor:path="/org.openoffice.Office.Common/Misc"><prop oor:name="SymbolStyle" oor:op="fuse"><value>breeze_dark_svg</value></prop></item>' "$FILE"
```

## `Ctrl`+`=` for zoom in
```bash
FILE="$HOME/.config/libreoffice/4/user/registrymodifications.xcu"; \
sed -i 's|<oor:items[^>]*>|&\
<item oor:path="/org.openoffice.Office.Accelerators/PrimaryKeys/Global"><node oor:name="EQUAL_MOD1" oor:op="replace"><prop oor:name="Command" oor:op="fuse"><value xml:lang="en-US">.uno:ZoomPlus</value></prop></node></item>\
<item oor:path="/org.openoffice.Office.Accelerators/PrimaryKeys/Global"><node oor:name="PAGEUP_SHIFT_MOD1" oor:op="remove"/></item>\
<item oor:path="/org.openoffice.Office.Accelerators/SecondaryKeys/Global"><node oor:name="PAGEUP_SHIFT_MOD1" oor:op="replace"><prop oor:name="Command" oor:op="fuse"><value xml:lang="en-US">.uno:ZoomPlus</value></prop></node></item>|' "$FILE"
```

## `Ctrl`+`-` for zoom out in Writer
```bash
FILE="$HOME/.config/libreoffice/4/user/registrymodifications.xcu"; \
sed -i 's|<item oor:path="/org.openoffice.Office.Accelerators/PrimaryKeys/Global"><node oor:name="PAGEUP_SHIFT_MOD1" oor:op="remove"/></item>|&\
<item oor:path="/org.openoffice.Office.Accelerators/PrimaryKeys/Modules/org.openoffice.Office.Accelerators:Module['\''com.sun.star.text.TextDocument'\'']/org.openoffice.Office.Accelerators:Key['\''SUBTRACT_MOD1'\'']/Command"><value xml:lang="en-US">.uno:ZoomMinus</value></item>|' "$FILE"
```

```bash
FILE="$HOME/.config/libreoffice/4/user/registrymodifications.xcu"; \
sed -i 's|<item oor:path="/org.openoffice.Office.UI.WriterWindowState/UIElements/States/org.openoffice.Office.UI.WindowState:WindowStateType['\''private:resource/toolbar/textobjectbar'\'']"><prop oor:name="Visible" oor:op="fuse"><value>true</value></prop></item>|&\
<item oor:path="/org.openoffice.Office.Views/TabDialogs"><node oor:name="cui/ui/customizedialog/CustomizeDialog" oor:op="replace"><prop oor:name="PageID" oor:op="fuse"><value>keyboard</value></prop><node oor:name="UserData"></node><prop oor:name="WindowState" oor:op="fuse"><value xsi:nil="true"/></prop></node></item>|' "$FILE"
```
