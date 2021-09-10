Please note, code is backed up on company Bitbucket, not here, as this repo is more for info.

# Test Results Parser

In standup, a Senior QA Engineer in my team mentioned he was looking to create a small project to help him save time when it comes to parsing test results into an Excel file. He mentioned he was trying to find time to start it. I immediately messaged him after saying I could drum something up together for him to help him out. He provided me with details as to what he was after and I implemented it. 

💬 **Feedback from Senior QA Engineer: "Lorna's results parser has been a Godsend!"** 💬

Steps:
1. User selects project, release, artifact
2. Web app unzips artifact locally, parses XML file to Excel, generates file
3. User able to download file

To note:
* Passed results are ignored
* Latest 10 releases shown
* Artifacts containing 'screenshots' are ignored
* Selected artifact is unzipped into local project folder

## Problem
At least once a month, QA go through a manual and very timely process of checking through automation results by copying and pasting data from a single .txt file which is also manually downloaded from said OD release. This whole process can take days.

## Solution
A simple .NET Core MVC project where you can select from a list of OD projects, a release and then which artifact interested in. From here, the artifact is unzipped locally and then parsed into a Excel file ready for download. It takes seconds. 

## Future
* Although aimed for OD currently, trying to keep generic so can cover Azure in the future and perhaps more focus on analysis rather than only table dumps
* Select more than 1 artifact
