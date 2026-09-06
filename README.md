⚠️ Error-Copy
Quickly copy errors, warnings, and problems from any file in VS Code to your clipboard.

Instead of manually copying problems from the Problems panel, Error Copy collects the diagnostics from the selected file and prepares a clean, structured report ready to paste into ChatGPT, Claude, Gemini, or any other AI coding assistant.

Features :

⛔ Copy Errors :
Copies only ERROR diagnostics from the selected file.

The report includes:

Error type
Line number
Column number
Error message
Diagnostic source
Previous line
Error line
Next line


⚠️ Copy Warnings :

Copies:

Warnings
Information
Hints
from the selected file.


⚠️ + ⛔ Copy All 

Copies all Problems reported for the selected file.

This includes:

Errors
Warnings
Information
Hints
Works With Any File Type
Error Copy is not limited to Python.

It works with any file type for which VS Code or an installed language extension provides diagnostics.

Examples:

Python
JavaScript
TypeScript
PHP
HTML
CSS
JSON
Java
C#
C++
and many others
File-Specific
Error Copy only reads Problems belonging to the selected file.

It does not collect Problems from other files in the workspace.

For example:

project/
├── main.py        ← selected
├── database.py
├── utils.py
└── config.py

If you choose:

⛔ Copy Errors

while main.py is selected, only errors belonging to main.py are copied.

Smart Duplicate Handling

The extension removes only true duplicates.

Different diagnostics on the same line are preserved.

For example:

ERROR
Expected expression


ERROR
Expected ":"

Both problems are kept because they are different diagnostics.

Sorted Problems

Problems are automatically sorted by:

Line number
Column number

This makes the generated report easier to read and understand.

Code Context

For every problem, Error Copy includes the surrounding code:

CODE:
      14 | previous line
>     15 | line containing the problem
      16 | next line

This gives an AI assistant enough context to understand the problem without copying the entire file.

Example

A copied report looks like:

ERROR REPORT
============


FILE: test.py
PATH: e:\WORK\Gulffix.com\WEBSITE\Gulffix\test.py
TOTAL: 2


======================================================================


PROBLEM #1
----------------------------------------------------------------------
TYPE: ERROR
LINE: 16  COLUMN: 3
MESSAGE: Expected expression
SOURCE: Pylance


CODE:
     15 |
>    16 | if
     17 |

The report is automatically copied to the Windows clipboard.

Simply press:

Ctrl + V

to paste it into your preferred AI assistant.

Designed for AI-Assisted Development

Error Copy was designed with modern AI coding workflows in mind.

Copy your problems and paste them directly into:

ChatGPT
Claude
Gemini
GitHub Copilot
Other AI coding assistants

No screenshots are required.

No need to manually copy each error.

Context Menu

Right-click inside the editor or on a file in Explorer.

You will see:

⛔ Copy Errors
⚠️ Copy Warnings
⚠️ + ⛔ Copy All
Lightweight

Error Copy has no external runtime dependencies.

It uses the VS Code API to read diagnostics and the built-in clipboard API to copy the generated report.

Requirements
Visual Studio Code 1.90.0 or newer
A language extension or VS Code feature that provides diagnostics
Privacy

Error Copy does not send your code or diagnostic information to an external server.

All processing is performed locally inside VS Code.

The generated report is copied directly to your local clipboard.

Version

Current version:

0.0.4

Changelog

See CHANGELOG.md for the release history.

License

MIT License.

<img width="1365" height="738" alt="image" src="https://github.com/user-attachments/assets/cbe7dcac-9c6b-4197-aebd-d09ae016c1c8" />
<br> <br> <br>

<img width="1366" height="768" alt="image" src="https://github.com/user-attachments/assets/92ef3924-adad-49d0-8fba-a8d034b5f3bf" />

