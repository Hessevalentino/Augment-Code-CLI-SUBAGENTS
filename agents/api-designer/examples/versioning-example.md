# API Versioning Example

This document demonstrates best practices for API versioning and backward compatibility.

## Version History

### v1.0.0 (Initial Release)
**Released:** 2025-01-15

Initial API release with basic user management.

**Endpoints:**
```
GET    /api/v1/users
GET    /api/v1/users/{id}
POST   /api/v1/users
PUT    /api/v1/users/{id}
DELETE /api/v1/users/{id}
```

**User Schema (v1):**
```json
{
  "id": "123",
  "name": "John Doe",
  "email": "john@example.com",
  "created_at": "2025-01-15T10:00:00Z"
}
```

---

### v1.1.0 (Backward Compatible Addition)
**Released:** 2025-03-20

Added optional profile fields - **BACKWARD COMPATIBLE**

**Changes:**
- ✅ Added optional `profile` object
- ✅ Added optional `status` field
- ✅ No breaking changes

**User Schema (v1.1):**
```json
{
  "id": "123",
  "name": "John Doe",
  "email": "john@example.com",
  "status": "active",           // NEW: Optional field
  "profile": {                   // NEW: Optional nested object
    "bio": "Developer",
    "avatar": "https://..."
  },
  "created_at": "2025-01-15T10:00:00Z"
}
```

**Migration Guide:**
- No changes required for existing clients
- New fields are optional and can be ignored
- Clients can start using new fields when ready

---

### v1.2.0 (Deprecation Notice)
**Released:** 2025-06-10

Deprecated `name` field in favor of `first_name` and `last_name`.

**Changes:**
- ✅ Added `first_name` and `last_name` fields
- ⚠️ Deprecated `name` field (still supported)
- ✅ Backward compatible

**User Schema (v1.2):**
```json
{
  "id": "123",
  "name": "John Doe",            // DEPRECATED: Use first_name + last_name
  "first_name": "John",          // NEW: Preferred
  "last_name": "Doe",            // NEW: Preferred
  "email": "john@example.com",
  "status": "active",
  "profile": {
    "bio": "Developer",
    "avatar": "https://..."
  },
  "created_at": "2025-01-15T10:00:00Z"
}
```

**Response Headers:**
```
Deprecation: true
Sunset: Sat, 31 Dec 2025 23:59:59 GMT
Link: <https://api.example.com/docs/migration-v2>; rel="deprecation"
Warning: 299 - "The 'name' field is deprecated. Use 'first_name' and 'last_name' instead."
```

**Migration Guide:**
1. Update your code to use `first_name` and `last_name`
2. Test with both old and new fields
3. Deploy before sunset date (2025-12-31)

---

### v2.0.0 (Breaking Changes)
**Released:** 2026-01-15
**Sunset for v1:** 2026-12-31

Major version with breaking changes.

**Breaking Changes:**
- ❌ Removed deprecated `name` field
- ❌ Changed `id` from string to UUID format
- ❌ Changed `created_at` to ISO 8601 with timezone
- ❌ Made `status` field required
- ✅ Added `role` field (required)

**User Schema (v2):**
```json
{
  "id": "123e4567-e89b-12d3-a456-426614174000",  // BREAKING: Now UUID
  "first_name": "John",
  "last_name": "Doe",
  "email": "john@example.com",
  "role": "user",                                 // NEW: Required
  "status": "active",                             // BREAKING: Now required
  "profile": {
    "bio": "Developer",
    "avatar": "https://..."
  },
  "created_at": "2026-01-15T10:00:00+00:00"      // BREAKING: ISO 8601 with TZ
}
```

**Migration Guide:**

1. **Update ID handling:**
   ```javascript
   // Old (v1)
   const userId = "123";
   
   // New (v2)
   const userId = "123e4567-e89b-12d3-a456-426614174000";
   ```

2. **Update name fields:**
   ```javascript
   // Old (v1)
   const name = user.name;
   
   // New (v2)
   const fullName = `${user.first_name} ${user.last_name}`;
   ```

3. **Handle required status:**
   ```javascript
   // Old (v1) - status was optional
   const status = user.status || 'unknown';
   
   // New (v2) - status is always present
   const status = user.status;
   ```

4. **Update date parsing:**
   ```javascript
   // Old (v1)
   const date = new Date(user.created_at);
   
   // New (v2) - includes timezone
   const date = new Date(user.created_at);  // Same, but more precise
   ```

---

## Versioning Strategy

### URL Versioning (Recommended)

**Format:** `/api/v{major}/resource`

**Examples:**
```
https://api.example.com/v1/users
https://api.example.com/v2/users
```

**Pros:**
- ✅ Clear and explicit
- ✅ Easy to route and cache
- ✅ Simple to test
- ✅ Works with all HTTP clients

**Cons:**
- ❌ Multiple codebases to maintain
- ❌ URL changes between versions

### When to Create a New Version

**Major Version (v1 → v2):**
- Removing fields or endpoints
- Changing field types
- Changing field names
- Making optional fields required
- Changing response structure
- Changing validation rules (stricter)

**Minor Version (v1.0 → v1.1):**
- Adding new optional fields
- Adding new endpoints
- Relaxing validation rules
- Adding new query parameters

**Patch Version (v1.0.0 → v1.0.1):**
- Bug fixes
- Performance improvements
- Documentation updates

---

## Backward Compatibility Checklist

### ✅ Safe Changes (Backward Compatible)

- [ ] Adding new optional fields to responses
- [ ] Adding new endpoints
- [ ] Adding new optional query parameters
- [ ] Relaxing validation rules
- [ ] Adding new enum values (if clients handle unknown values)
- [ ] Improving error messages
- [ ] Adding new HTTP headers

### ❌ Breaking Changes (Require New Version)

- [ ] Removing fields from responses
- [ ] Removing endpoints
- [ ] Renaming fields
- [ ] Changing field types
- [ ] Making optional fields required
- [ ] Changing response structure
- [ ] Stricter validation rules
- [ ] Changing HTTP status codes
- [ ] Removing enum values

---

## Deprecation Process

### Step 1: Announce Deprecation
- Update API documentation
- Add deprecation notice to changelog
- Communicate to API consumers

### Step 2: Add Deprecation Headers
```http
Deprecation: true
Sunset: Wed, 31 Dec 2026 23:59:59 GMT
Link: <https://api.example.com/docs/migration>; rel="deprecation"
```

### Step 3: Provide Migration Guide
- Document all breaking changes
- Provide code examples
- Offer migration tools if possible

### Step 4: Monitor Usage
- Track usage of deprecated endpoints
- Contact remaining users
- Send reminders before sunset

### Step 5: Sunset
- Remove deprecated version
- Return 410 Gone for old endpoints
- Redirect to migration guide

---

## Best Practices

1. **Version in URL** - Use `/api/v1/` format
2. **Semantic Versioning** - Follow major.minor.patch
3. **Long Deprecation Period** - Minimum 6-12 months
4. **Clear Communication** - Document all changes
5. **Migration Guides** - Provide detailed examples
6. **Monitor Usage** - Track deprecated endpoint usage
7. **Sunset Dates** - Set and communicate clearly
8. **Backward Compatibility** - Maintain within major versions
9. **Test Both Versions** - Ensure smooth migration
10. **Support Multiple Versions** - At least 2 major versions simultaneously

