# Assigning a License to a User in Microsoft Entra ID

Assigned a Microsoft Entra Suite license to a user account through the Microsoft 365 Admin Center, working through how license assignment ties back to Entra ID and what that connection actually controls.

## Implementation

Started in the Microsoft Entra Admin Center under Identity > Users > All Users, and opened Chris Green's account. Clicked into Licenses and got a warning there that license assignment is now handled in the Microsoft 365 Admin Center rather than directly in Entra ID.

Followed the link into the M365 Admin Center, went to Active Users, selected Chris Green, and opened Licenses and Apps. Checked the box for Microsoft Entra Suite and saved the change.

Went back to the Entra Admin Center tab, refreshed the Licenses page, and confirmed Microsoft Entra Suite now showed as assigned. Returned to the Overview tab to verify everything applied correctly.

## What I learned

The biggest thing that stood out was that Entra ID doesn't actually own license assignment anymore, it just reflects it. The Entra Admin Center will show you what's assigned, but the assignment itself happens in the M365 Admin Center. That split makes sense once you see it (Entra ID handles identity, M365 handles the license and app entitlements), but it's a distinction I hadn't thought about before actually clicking through it.

It also reinforced that a license and a role are two different things. Assigning Microsoft Entra Suite gives Chris Green access to a set of services, it doesn't hand him any administrative permissions. Those get managed separately through Entra roles. Easy to conflate the two if you haven't worked with both systems side by side.

Refreshing on the Entra ID side after making the change in M365 was a small step but a useful habit, since it's a reminder that these two admin centers don't always sync instantly and verifying the change actually took effect is part of the job, not an afterthought.

---
*Deployed and tested in Azure via [LabITPro](https://labitpro.com/assign-licenses-to-users-in-microsoft-entra-id/)*
