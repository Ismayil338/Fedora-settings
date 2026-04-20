## Save in MS Office formats
```bash
FILE="$HOME/.config/libreoffice/4/user/registrymodifications.xcu"; \
sed -i '/<item oor:path="\/org.openoffice.Setup\/L10N">/a\
<item oor:path="/org.openoffice.Setup/Office/Factories/org.openoffice.Setup:Factory['\''com.sun.star.presentation.PresentationDocument'\'']"><prop oor:name="ooSetupFactoryDefaultFilter" oor:op="fuse"><value>Impress MS PowerPoint 2007 XML</value></prop></item>\
<item oor:path="/org.openoffice.Setup/Office/Factories/org.openoffice.Setup:Factory['\''com.sun.star.sheet.SpreadsheetDocument'\'']"><prop oor:name="ooSetupFactoryDefaultFilter" oor:op="fuse"><value>Calc MS Excel 2007 XML</value></prop></item>\
<item oor:path="/org.openoffice.Setup/Office/Factories/org.openoffice.Setup:Factory['\''com.sun.star.text.TextDocument'\'']"><prop oor:name="ooSetupFactoryDefaultFilter" oor:op="fuse"><value>Office Open XML Text</value></prop></item>' "$FILE"
```

## SVG icons
```bash
FILE="$HOME/.config/libreoffice/4/user/registrymodifications.xcu"; \
sed -i '/<item oor:path="\/org.openoffice.Office.Common\/Misc"><prop oor:name="FirstRun" oor:op="fuse"><value>false<\/value><\/prop><\/item>/a\
<item oor:path="/org.openoffice.Office.Common/Misc"><prop oor:name="SymbolStyle" oor:op="fuse"><value>breeze_dark_svg</value></prop></item>' "$FILE"
```

## Enable `Ctrl`+`=` and `Ctrl`+`-` for page zoom
Tools -> Customize -> Keyboard -> LibreOffice
