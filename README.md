# UiPath RPA Automation Portfolio

Five independent, local-only UiPath Studio projects demonstrating email triage, file organization, Excel analysis, Office/PDF document generation, and browser UI automation.

## Projects

| Project | Purpose | Primary activities |
|---|---|---|
| 01 Email Automation | Classifies sample `.eml` files and writes a report/draft | Read Text File, Assign, If, For Each, Write Text File |
| 02 File Management | Organizes sample files by extension and safely handles duplicates | For Each File in Folder, Path Exists, Create Folder, Move File, Write CSV |
| 03 Excel Automation | Calculates attendance, totals, averages, and improvement flags for 15 students | Use Excel File, Read Range, For Each Row, Write Range |
| 04 Word, PowerPoint and PDF | Generates letters, a presentation outline, and a PDF text summary | Word/PowerPoint/PDF activities, Excel, Append Text, Export to PDF |
| 05 Browser UI | Completes a local HTML student registration form and records confirmation | Use Application/Browser, Type Into, Select Item, Check App State, Get Text, Take Screenshot |

## Requirements

- UiPath Studio Community Edition (Windows-compatible project support)
- Excel and Word activities: `UiPath.Excel.Activities`, `UiPath.Word.Activities`
- Mail activities if extending Project 01 to a mailbox: `UiPath.Mail.Activities`
- UI automation: `UiPath.UIAutomation.Activities`
- System activities: `UiPath.System.Activities`
- PowerPoint/PDF activities as available in your Studio feed: `UiPath.Presentations.Activities`, `UiPath.PDF.Activities`

Each project is intentionally local-only. Project 01 never sends mail; Project 05 uses only `registration.html`. See `DEPENDENCIES.md` and `TEST-REPORT.md` for package and validation details.

## Running

1. Open a project folder in UiPath Studio.
2. Restore dependencies from `project.json`.
3. Review paths in `Main.xaml` and run with **Debug**.
4. Inspect the `Outputs` and `Evidence` folders.

## Structure

Every project contains `project.json`, `Main.xaml`, `Inputs`, `Outputs`, and an `Evidence` folder. The workflows use relative paths based on the project directory where practical.

## Testing status and limitations

The files were structurally reviewed in this environment, but UiPath Studio execution was not available. Therefore no project is claimed as Studio-passed. Excel/Word/PowerPoint/PDF activity availability and Windows package versions can require minor Studio-side adjustments. Sample output placeholders are documented in each project; run the workflows to produce runtime evidence.

## Git upload

```powershell
cd UiPath-RPA-Automation-Portfolio
git init
git add .
git commit -m "Add UiPath RPA automation portfolio"
git branch -M main
git remote add origin https://github.com/<your-user>/<your-repository>.git
git push -u origin main
```
