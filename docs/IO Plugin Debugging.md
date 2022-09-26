Placeholder document to document common errors and their causes.
# IO Plugin Common Errors and Solutions
Common DRAD errors encountered while developing plugins and navigating the DRAD environment.

## System Configuration Editor Cannot Load PE Into Block Diagram
The SCE is unable to load a PE into the block diagram, while displaying the text above.
./bin/SCE Adas Config Error.png

### Solution
1. Open the PE, right click **Build Specifications -> [PE Name]**, and select build.  Close and reopen SCE and try to place the PE on the block diagram.
2. If the first solution did not work, **HOW DO I SOLVE THIS!!**

## 1498 Error Thrown on PE Startup When Running the DRAD Main App
This is a generic error caused by an issue with a PE's dependencies when DRAD is run.

### Solution
1. Sometimes DRAD cannot access dependencies with the required file permissions. To solve this close DRAD and open with administrative priviledges.
2. If DRAD or PE dependencies are not the correct version (or missing) some dependencies could be saved in unexpected locations. To solve this simply update (or install) dependencies to the correct version. PE dependencies are documented in each plugin directory.
3. If the PE source code (LV projects) are opened in the wrong version of labview the PE dependencies will be reset to the file versions for that version of LabVIEW. This is commonly seen with dependencies located in the vi.lib directory. The solution is to open labview 2020, *then* the LV project to reset dependencies to the 2020 versions.  Opening the project directly from the file explorer will open the last version of LV opened - even if you specifically select LV 2020.
