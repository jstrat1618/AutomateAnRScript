# How to Schedule an R Script


## Schedule a script with a Batch File
The batch script myBatchFile.bat runs the script myscript.R, which produces a text file called MyFile.txt with the date and time the myBatchFile was run. If you are on Windows you can follow the instructions I've outlined using Task Scheduler.



Open Task Scheduler.

Go to Action -> Create Task

Give a name of the script. I also recommend making sure the boxes "Run whether user is logged on or not" and "Run with the highest privileges" are checked.

Go to Trigger -> New
Select the conditions appropriate for your task.

Go To Actions -> New
Make sure "Start a program" is selected under "Action".  Then browse to your batch file or paste the full file path under "Program/script". Then Select "Ok".

Go to Conditions and make sure the conditions match the scenario you want. The first time I tried to schedule a batch script my laptop was not plugged into an outlet, and it took me forever to realize why. If this is your case make sure "Start the task only if the computer is on AC power" is UNCHECKED.

Likewise check the Settings. I recommend checking the box "If the task is not scheduled to run again, delete it" is checked with the approriate days supplied just so your task library doesn't get too full. 



See this blog:
https://www.r-bloggers.com/new-rstudio-add-in-to-schedule-r-scripts/


Also check out: https://stackoverflow.com/questions/2793389/scheduling-r-script
And Check out: https://www.youtube.com/watch?v=EInOL6D5f3Q

Batch Scripting Resource: http://steve-jansen.github.io/guides/windows-batch-scripting/