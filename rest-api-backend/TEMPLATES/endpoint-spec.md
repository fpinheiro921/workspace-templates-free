# Endpoint Spec — [METHOD /path]

**Status:** Draft / Approved  
**Date:** YYYY-MM-DD  

---

## Overview
**Method:** GET / POST / PUT / PATCH / DELETE  
**Path:** `/api/v1/[resource]`  
**Auth required:** Yes / No  
**Description:** [One sentence]

## Request

### Headers
| Header | Required | Value |
|---|---|---|
| `Authorization` | Yes | `Bearer <token>` |

### Path Parameters
| Param | Type | Description |
|---|---|---|

### Query Parameters
| Param | Type | Required | Description |
|---|---|---|---|

### Body (JSON)
```json
{
  "field": "type — description"
}
```

## Response

### Success (2xx)
```json
{
  "success": true,
  "data": {},
  "meta": {}
}
```

### Error Responses
| Status | Code | Description |
|---|---|---|
| 400 | VALIDATION_ERROR | |
| 401 | UNAUTHORIZED | |
| 404 | NOT_FOUND | |

## Notes
- 
