# UiPath Portfolio Final Submission Test Report

Testing date: 2026-11-13. UiPath Studio Community 2026.0.204 STS was located and used through Windows GUI automation.

| Project | JSON | XAML | Dependencies | Studio validation | Actual execution | Output verification | Genuine screenshots |
|---|---|---|---|---|---|---|---|
| 01 Email Automation | PASS | PASS | PASS | PASS | PASS | PASS: `Outputs/email-processing-report.csv` | NO saved file |
| 02 File Management | PASS | PASS | PASS | FAIL | NOT TESTED | FAIL/absent | NO |
| 03 Excel Automation | PASS | PASS | PASS | PASS | NOT CONFIRMED | FAIL/absent | NO |
| 04 Word-PowerPoint-PDF | PASS | PASS | BLOCKED during Studio conversion | NOT TESTED | NOT TESTED | NOT TESTED | NO |
| 05 Browser UI Automation | PASS | PASS | NOT TESTED | NOT TESTED | NOT TESTED | NOT TESTED | NO |

## Evidence

- Project 1 was preserved. It opened in Studio, dependencies restored, Main.xaml loaded without an unresolved-activity banner, Debug execution was initiated, and `Outputs/email-processing-report.csv` exists.
- Project 2 loaded with an unresolved activity. The incompatible `CreateFolder` activity was removed from Main.xaml, but Studio continued to show an unresolved-activities warning after reload. It is not marked executable.
- Project 3 opened and Main.xaml displayed without an unresolved-activity banner. A Debug run was initiated, but no generated output file was found, so execution is not marked PASS.
- Project 4 reached Studio's legacy-project conversion screen, but Studio remained in an active conversion/loading request and the GUI bridge stopped accepting observations. No execution is claimed.
- Project 5 was not reached for Studio execution in this run.

## Screenshot and log honesty

No screenshot files or execution logs are claimed as evidence because genuine files were not successfully saved into the project folders. Static JSON/XML validation is separate from Studio validation and actual execution.
