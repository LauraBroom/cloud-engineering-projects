# Managing User Properties in Microsoft Entra ID

Updated an existing user's properties in Microsoft Entra ID, including organizational details, manager assignment, and group membership.

## Details
| Field | Value |
|---|---|
| User | Dave Jones |
| Company | Surf City Boats |
| Department | Finance |
| Office Location | New York |
| Manager | Joey Knish |
| Group Removed | AAD DC Administrators |

## Implementation
Navigated to Identity > Users > All Users in the Microsoft Entra Admin 
Center and selected Dave Jones from the user list. Opened Edit properties 
and updated the Job Information tab, setting company name, department, 
employee ID, and office location. Assigned Joey Knish as manager using 
the Add manager option. Saved the changes, then switched to the Groups 
tab to review Dave's current memberships and removed AAD DC 
Administrators, since that access no longer applied. Returned to the 
Overview tab to confirm all updates were applied correctly.

## What I learned
Made it clear that user management doesn't stop once an account is 
created. Fields like department, office location, and manager aren't 
just for show, they support real organizational functions like 
reporting structures and compliance tracking.

Removing the AAD DC Administrators group was the part that stuck with 
me most. It's a reminder that group membership needs to be reviewed 
over time, not just assigned once and forgotten. Leaving someone in a 
group like that after their role changes is exactly the kind of access 
creep that turns into a security problem later.

I also noticed how much faster this process is when you're editing an 
existing user versus creating one from scratch. Most of the fields were 
already populated, so the task became about accuracy and judgment (what 
needs to change and what doesn't) rather than data entry.

---
*Hands-on practice via [LabITPro](https://labitpro.com/manage-user-properties-in-microsoft-entra-id/)*
