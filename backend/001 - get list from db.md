## 001 - Get list from DB - Aggregate

**Status:** Accepted

**Date:** 12/07/2025

---

## Context

Needed to filter products by linked models like (brand/subcategory) which is objectId

---

## Decision

Use MongoDB Aggregate piplines to find items lists

---

## Consequences

- Created utils, for populating, filtering and reshaping, to unify the response, prevent possible syntax errors and to ensure the same response between controllers due to using custom utils.
- Easy to miss some model fields but more flexable to reshape.
- better error handling due to keepming filtering, pagination, reshaping and other process to MongoDB itself.
- In some simple cases going through multiple piplines may affect the performance.
- More complex and long code due to going through multiple piplines.
