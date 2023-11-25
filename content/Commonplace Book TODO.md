#meta 

- [x] Refactor references to "gamerecs/" folder to "Game Recs/"
- [x] Refactor "#sync" to "quartz-sync"
- [ ] Review notes, add #quartz-sync , #nosync , or #needs-work tag as appropriate

Dataview of notes that do not have one of those three tags:
```dataview
table
where !contains(file.tags, "#quartz-sync")
where !contains(file.tags, "#nosync")
where !contains(file.tags, "#needs-work")
limit 20
```


