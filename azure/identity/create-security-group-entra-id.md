# Creating a Security Group in Microsoft Entra ID

Created a security group in Microsoft Entra ID with assigned membership, then configured ownership and membership separately to reflect how access control is actually structured in the group.

## Implementation

Started in the Microsoft Entra Admin Center under Identity > Groups > All Groups, and clicked New Group. Set the Group Type to Security and named it HumanResources.

For Membership Type, selected Assigned rather than Dynamic, since this group needed manual control over who's in it rather than membership driven by rules.

Assigned Chris Green as owner and added Mike Mitchell as a member, then created the group. After refreshing to confirm it appeared in the group list, opened it back up and checked both the Members and Owners tabs to verify Mike Mitchell and Chris Green were listed correctly under each.

## What I learned

The owner versus member distinction is more important than it looks on the surface. A member gets whatever access the group grants, but an owner can manage the group itself, meaning add or remove members without needing directory wide admin rights. That's a meaningful delegation tool, since it lets you hand off day to day group management without giving someone broader permissions than they need.

Choosing Assigned membership here also made the tradeoff clearer between the two membership types. Assigned gives full manual control but means someone has to remember to update it as people change roles or leave. Dynamic would have handled that automatically based on attributes, at the cost of giving up direct control over exactly who's in the group at any given moment. Picking the right one really depends on how much the group's purpose lines up with attributes you can reliably filter on.

Verifying through both the Members and Owners tabs separately, rather than assuming the creation step worked, reinforced the same habit from the licensing lab: confirm the change actually took effect instead of trusting the confirmation dialog alone.

---
*Deployed and tested in Azure via [LabITPro](https://labitpro.com/create-a-security-group-in-microsoft-entra-id/)*
