


This test index page uses the **Data View** plugin for Obsidian. When you go to Preview mode, the queries execute.

***
Table of all from a Folder with a specific series sorted descending date
	note: this involves a hack to rename the first column from the default of "File". Use Group By and then reference the fields as "rows" eliminates the column named "File" and then the link is manually aded back in.

### Thursday OGM (series) Calls by Date:
```dataview
table
rows.file.link as "Meeting",
rows.date as "Meeting Date",
rows.file.size as "File Size"
from "Test Meetings"
where meeting-series ="OGM Thursday"
sort date desc
group by file.path

```


***
Table of all with a specific file name "Meeting" (does not have to be in a specific  folder) sorted descending date 

### All OGM Calls:
```dataview
table
meeting-series as "Meeting Series",
file.size as "File Size"
from ""
where contains(file.name, "Meeting")
sort date desc
```



***
Table of all within two different folders  sorted descending date (does not care about file name)

### All OGM Calls:
```dataview
table
meeting-series as "Meeting Series",
file.size as "File Size"
from "Test Meetings/OGM General Meetings" OR "Test Meetings/OGM Stewards Meetings"
sort date desc
```






***
Table of all from a Folder with a specific series sorted descending date

### Thursday OGM Calls:
```dataview
table
date as "Meeting Date",
file.size as "File Size"
from "Test Meetings"
where meeting-series ="OGM Thursday"
sort date desc

```




***
EXAMPLE: List all from a Folder with a specific series.

Thursday OGM Calls:
```dataview
list
from "Test Meetings"
where meeting-series ="OGM Thursday"

```



***
EXAMPLE: List all from a Folder
```dataview
list
from "Test Meetings"

```


***
List All Notes (long)
```dataview
list

```

