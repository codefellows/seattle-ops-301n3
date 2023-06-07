# Group Policy

## Overview

Systems administrations can use OUs (Organizational Units) and GPOs (Group Policy Objects) to apply computer configurations to specific departments or teams in the organization. Group policy can be used to protect user data by applying folder redirection to the Windows user files.

## Class Outline

- Course Overview
- Review Previous Lab
- Review Previous Ops Challenge
- Demo Today's Ops Challenge
- Lecture Today's Lab Topic
- Demo Today's Lab Topic
- Lab

## Learning Objectives

### Students will be able to

#### Describe and Define

- OU
- GPO
- Group Policy Editor
- Group Policy management (GPMC or AGPM)

#### Execute

- Create a Group Policy
- Push a Group Policy to an endpoint
- Test a folder redirection policy

## Helpful Resources

- [Group Policy Planning and Deployment Guide](https://docs.microsoft.com/en-us/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc754948(v=ws.10))
- [Back to Basics: Groups vs Organizational Units in Active Directory](http://techgenix.com/back-basics-groups-vs-organizational-units-active-directory/)


## Notes

- How to create an OU
  1. Launch Windows Server 2012. On the Start page click Active Directory Administrative Center.
    - Alternatively you can press `WIN+R` to get the Run window, type `dsac.exe`, and click `OK`.
  2. Right-click the domain, and select New ➢ Organizational Unit
  3. Enter the OU name.
    - Recommended to enable the "Protect object from accidental deletion" option to prevent unintentional removal of the OU.
  4. Click OK and your OU is created and viewable under globex (local) object in the left panel.

- Group Policy Hierarchy
  - By default, Group Policy in an Active Directory environment follows a hierarchical structure and is inherited by containers, such as sites, domains, and organizational units (OUs).
  - Group Policy is inherited, meaning that policy settings applied at higher levels of the hierarchy are passed down to lower-level containers.
  - Additionally, Group Policy is cumulative, meaning that policy settings from multiple GPOs can accumulate and be applied to an object.
    - Conflicting policy settings are resolved based on the processing order.
  - GPOs are processed in the following order:
    - The local GPO is applied.
      - The local GPO is stored on the individual computer and contains policy settings specific to that machine. It takes precedence over any other GPOs.
    - GPOs linked to sites are applied.
      - GPOs linked to network sites are processed. Sites are logical groupings of computers based on their physical or network location.
      - GPOs at the site level are typically used to apply policies specific to a particular location or network segment.
    - GPOs linked to domains are applied.
      - GPOs linked to the domain level are processed.
      - These GPOs affect all objects within the domain, including computers and users.
    - GPOs linked to organizational units are applied.
      - For nested organizational units, GPOs linked to parent organizational units are applied before GPOs linked to child organizational units are applied.
        - When OUs are nested (i.e., when one OU is a child of another OU), GPOs linked to the parent OU are applied first, followed by GPOs linked to child OUs.
        - This order ensures that parent-level policies are applied before child-level policies.

- "When applying policy, the system queries the directory service for a list of GPOs to process. Each GPO is linked to an Active Directory container in which the computer or user belongs. By default, the system processes the GPOs in the following order: local, site, domain, then organizational unit. Therefore, the computer or user receives the policy settings of the last Active Directory container processed." -[MS Docs](https://docs.microsoft.com/en-us/previous-versions/windows/desktop/policy/applying-group-policy)

- "When processing the GPO, the system checks the access-control list (ACL) associated with the GPO. If an access-control entry (ACE) denies the computer or user access to the GPO, the system does not apply the policy settings specified by the GPO. If the ACE allows access to the GPO, the system applies the policy settings specified by the GPO." -[MS Docs](https://docs.microsoft.com/en-us/previous-versions/windows/desktop/policy/applying-group-policy)