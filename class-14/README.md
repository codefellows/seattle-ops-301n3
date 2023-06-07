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