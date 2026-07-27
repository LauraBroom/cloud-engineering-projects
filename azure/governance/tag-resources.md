# Tagging Resources in Microsoft Azure

Applied Environment tags to two virtual machines to categorize them by deployment stage, then used tag based filtering to locate resources by that classification.

## Details

| Field | Value |
|---|---|
| Resource 1 | DC01, tagged Environment = Production |
| Resource 2 | WEB01, tagged Environment = Development |
| Filtering | By Environment: Production and Environment: Development |

## Implementation

Opened DC01 and navigated to Tags, then created a new tag with the name Environment and the value Production, applying it directly to the resource.

Opened WEB01 next and added a tag using the same Environment name, which was already available from the prior entry, and set the value to Development.

With both resources tagged, used the global search bar to pull up all tagged resources, then filtered by Environment: Development to confirm WEB01 appeared and by Environment: Production to confirm DC01 appeared.

## What I learned

Tags turn resource organization into something searchable rather than something you have to remember or track separately.

Reusing an existing tag name across resources, instead of creating a new one each time, keeps the taxonomy consistent and makes filtering actually useful at scale.

This maps directly onto how I think about client environments in my current role, where knowing at a glance which systems are production versus non production matters for avoiding mistakes during troubleshooting or maintenance windows.

---
*Deployed and tested in Azure via [LabITPro](https://labitpro.com/tag-resources-in-microsoft-azure/?utm_source=udemy&utm_campaign=az104_course)*
