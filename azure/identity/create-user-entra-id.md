# Provisioning a User in Microsoft Entra ID

Configured a new user account in Microsoft Entra ID with custom identity 
attributes (UPN, department, job title, usage location), as part of 
building out core identity management skills in Azure.

## Details
| Field | Value |
|---|---|
| User Principal Name | mmitchell@[domain].com |
| Display Name | Mike Mitchell |
| Job Title | HR Manager |
| Company | Surf City Boats |
| Department | Human Resources |
| Usage Location | United States |

## Implementation
Navigated to Identity > Users in the Azure portal and created a new user 
manually. Set the UPN and domain suffix to establish the unique sign-in 
identity, then configured display name and property fields (job title, 
department, company). Set Usage Location to United States and skipped 
role assignment for this exercise, then reviewed and created the user.

## What I learned
This was a good reminder that UPN and display name serve two different 
purposes even though they look similar at first glance. The UPN is what 
the user actually types to sign in, while the display name is just how 
they show up across Microsoft 365 apps like Outlook or Teams. It would be 
easy to confuse the two if you had not set them up yourself.

I also noticed that Usage Location is not just an administrative detail. 
It actually determines whether a user can be assigned certain licenses at 
all, since some Microsoft services are restricted by region. Skipping it 
or leaving it blank could block someone from getting the tools they need 
later on.

Finally, seeing that role assignment is a completely separate step from 
creating the user clarified something for me. Entra ID treats identity 
and access as two different layers. You can create someone's account 
first and decide what they are allowed to touch afterward, which mirrors 
how access control should work in any secure environment.

---
*Hands-on practice via [LabITPro](https://labitpro.com/create-a-new-user-in-microsoft-entra-id)*
