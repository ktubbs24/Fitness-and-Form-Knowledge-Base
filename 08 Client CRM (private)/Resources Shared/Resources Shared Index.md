---
note_type: resources_shared_index
status: active
public: false
---

# Resources Shared Index

Track which public notes, videos, PDFs, or documents were shared with each client.

## Shared Resources
| Date | Client | Resource | Reason |
|------|--------|----------|--------|
|      |        |          |        |

```dataview
TABLE client, date, resources_shared, related_public_notes
FROM "08 Client CRM (private)/Clients"
WHERE resources_shared
SORT date DESC
```
