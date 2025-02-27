---
# generated by https://github.com/hashicorp/terraform-plugin-docs
page_title: "tenablesc_auditfile Resource - terraform-provider-tenablesc"
subcategory: ""
description: |-
  Create and manage Audit Files.
---

# tenablesc_auditfile (Resource)

Create and manage Audit Files.

## Example Usage

```terraform
resource "tenablesc_auditfile" "stig_ubuntu_20_04" {
  # Holding auditfiles in code and uploading them instead of pulling direct from vendor has many advantages.
  # Allows you to uptake recasts at the same time as updated audit files, and have a pinned known-good old version.
  # Keeps history in sync in-repo end-to-end.

  name    = "STIG Ubuntu 20.04"
  content = file("path/in/repo/to/file.audit")
}
```

<!-- schema generated by tfplugindocs -->
## Schema

### Required

- `content` (String) Audit file content
- `name` (String) Audit file Name as presented in SC

### Optional

- `description` (String) Audit File description

### Read-Only

- `id` (String) The ID of this resource.
- `sc_filename` (String) Filename of audit file as stored in SC
