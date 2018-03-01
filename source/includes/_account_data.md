### Result Data Fields

Field | Type | Description
------|------|------------
id | int | Unique id of account for this family & team. **Note** Our data model is transitioning to provide more clear separationg between families on the same team. In the interim, the id for the account may be the same as the organization, but the account_id should be used.
organization_id | int | Globally unique id for this organization.
organization_name | string | Name of organization / team. (16 characters max.)
organization_full_name | string | Full (long) name for organization. May be same as organization_name.
organization_abbreviation | string | 1-5 character abbreviation for this team.
organization_type | string | Identifies type of organization. Please see organization_type lookup codes.
organization_site_url | string | URL to website associated with this team.
organization_logo_urls | object | JS object/hash/dictionary mapping the keys "icon" (48x48), small" (80x80), "medium" (200x100), "large" (300x150) to associated logo image URLs in those sizes.
