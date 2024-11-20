---
sticker: emoji//1f31f
---
```dataview
table Without ID
	file.link as "Paper",
	시작일 as "Date",
	choice(진행상태=false, "X", "O") as "Status",
	tags as "tags"
from "HCI" or "VIS"
sort file.ctime desc
```

