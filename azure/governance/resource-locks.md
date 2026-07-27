# Adding and Removing Resource Locks in Azure

Applied a Delete lock to a virtual machine to prevent accidental removal, then tested and removed the lock to confirm the protection behaved as expected.

## Details

| Field | Value |
|---|---|
| Target Resource | DC01 virtual machine |
| Lock Name | NoDelete |
| Lock Type | Delete |

## Implementation

Navigated to the DC01 virtual machine and opened the Locks section under Settings. Added a new lock named NoDelete and set the lock type to Delete, which blocks removal of the resource while leaving normal configuration and management operations untouched.

Tested the lock by attempting to delete the virtual machine and submitting the request, which Azure rejected with an error confirming the resource was protected.

Once the lock behavior was confirmed, removed NoDelete from the Locks section to restore full delete access.

## What I learned

A Delete lock protects a resource from removal without restricting day to day management, which makes it a low friction way to safeguard critical infrastructure like a domain controller or shared production system.

I also saw how the lock surfaces directly at the point of deletion rather than failing silently, which matters for troubleshooting and for explaining behavior to a client if a request ever gets blocked.

Locks work independently of role based access, so they add a layer of protection that holds even for users who otherwise have permission to delete the resource.

---
*Deployed and tested in Azure via [LabITPro](https://labitpro.com/adding-and-removing-resource-locks-in-microsoft-azure/?utm_source=udemy&utm_campaign=az104_course)*
