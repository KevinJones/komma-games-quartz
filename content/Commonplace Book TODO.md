#meta 

- [ ] Review notes, add sync, #nosync , or #needs-work tag as appropriate
- [ ] reviw stuff in "Zim Notebooks" folder in documents

Dataview of notes that do not have one of those three tags:
```dataview
table
where !contains(file.tags, "#quartz-sync")
where !contains(file.tags, "#nosync")
where !contains(file.tags, "#needs-work")
limit 20
```


