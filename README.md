# i18n Excel Converter

Convert excel to resx and json

# Electron

This library is compatible with Electron and should just work out of the box.
The demonstration uses Electron 9.0.5.  The library is added via `require` from
the renderer process. Note that Electron now requires `nodeIntegration: true`
in order to `require('XLSX')` in the renderer process. It can also be required
from the main process, as shown in this demo to render a version string in the
About dialog on OSX.

The standard HTML5 `FileReader` techniques from the browser apply to Electron.
This demo includes a drag-and-drop box as well as a file input box, mirroring
the [SheetJS Data Preview Live Demo](http://oss.sheetjs.com/js-xlsx/)

The core data in this demo is an editable HTML table.  The readers build up the
table using `sheet_to_html` (with `editable:true` option) and the writers scrape
the table using `table_to_book`.

