TAFT ELIGIBILITY CHECKPOINT — VERSION 1

WHAT IT DOES
- Stores student roster locally in IndexedDB on the device/browser.
- Imports CSV and Excel (.xlsx/.xls) files.
- Expected columns: Last Name, First Name, Student ID, Status.
- Status values: Approved or Denied.
- Replace roster or merge/update by Student ID.
- Add/edit individual students.
- Scan using an attached barcode scanner (keyboard-style input) or type an ID.
- Green flash + approval tone for Approved.
- Red flash + denial tone for Denied.
- Displays student name and ID.
- Stores scan history separately and persistently.
- Downloads history and roster backups as CSV.
- Clear History happens only when you click the button and confirm.
- Camera scanning is included where the browser supports BarcodeDetector and camera access.

PRIVACY
The roster and scan history are stored in your browser's local IndexedDB database. The app has no student database on a server and does not upload roster or scan history anywhere.

IMPORTANT
1. Do not clear the browser/site data for this app unless you intend to erase locally stored data.
2. Export a roster backup before major roster changes.
3. Data stored on one device/browser does not automatically appear on another device.
4. Excel parsing loads the SheetJS JavaScript library from jsDelivr when internet access is available. The student spreadsheet itself is processed locally in the browser and is not uploaded to jsDelivr. CSV import does not require that library.
5. For a fully offline package with no third-party library request at all, use CSV files or bundle SheetJS locally in a future version.

QUICK TEST
1. Open index.html in a modern browser.
2. Go to Import / Update.
3. Select a CSV/XLSX roster.
4. Click Replace Roster.
5. Go to Scan.
6. Scan/type a Student ID and press Enter.

INSTALLABLE PWA
The included manifest.json and sw.js support installation when the folder is served over HTTPS or localhost. Opening index.html directly from Files/file:// will run the core app, but browsers do not permit full PWA installation or service workers from file://.
