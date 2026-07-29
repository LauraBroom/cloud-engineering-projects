# Creating a Custom RBAC Role for Action Group Management
Built a custom Azure role from scratch, scoped specifically to managing action groups, instead of relying on a built in role.

## Details
| Field | Value |
|---|---|
| Permissions granted | Create, delete, update, and read for Microsoft Insights action groups |
| Default scope | Resource group |
| Additional scope added | Subscription |
| Assigned to | Test user |

## Implementation
Opened the Access Control (IAM) pane for the resource group and selected Add, then Custom role.

Started the role from scratch rather than cloning an existing role or using a JSON template, then named it and added a description.

Action groups do not appear under their own category in the permissions picker, so I navigated into the Azure Monitor grouping to find them. Action groups fall under the Microsoft Insights namespace, the same resource provider Azure Monitor uses.

Within Microsoft Insights, located the action group permissions specifically and selected create, delete, update, and read, keeping the role scoped narrowly instead of granting broader access.

Added the subscription as an additional assignable scope alongside the default resource group scope, then reviewed and created the role.

Confirmed the role appeared under custom roles, then assigned it to a test user.

## What I learned
Building a role from scratch instead of cloning gave me full control over exactly which permissions it included, rather than trimming down an
