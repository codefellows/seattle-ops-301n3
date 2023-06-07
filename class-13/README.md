# Active Directory

## Overview

ADAC (Active Directory Administrative Center) facilitates the convenient administration of user profiles from any Windows endpoint that can achieve connectivity with the DC. This application acts as a user identity control panel capable of many tasks ranging from user creation to simple password changes.

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

- ADAC/ADUC
  - These are administrative tools provided by Microsoft for managing Active Directory (AD) in Windows Server environments.
  - **Active Directory Administrative Center** is a modern graphical tool that offers a centralized interface for performing various administrative tasks related to Active Directory. It provides an intuitive and user-friendly way to manage users, groups, organizational units (OUs), and domains.
  - **Active Directory Users and Computers** is a tool used for managing user accounts, computers, and groups within an Active Directory environment. It allows administrators to perform tasks like creating, modifying, and deleting user accounts, resetting passwords, managing group memberships, and organizing OUs.

- RSAT
  - **Remote Server Administration Tools** is developed by Microsoft and it allows administrators to control various server roles and features without physically accessing the servers.
  - Administrators can install the necessary management tools on their local machines and remotely manage server components such as Active Directory, DNS, DHCP, Group Policy, File Services, Hyper-V, and more.

- RBAC
  - **Role-Based Access Control** is a widely used approach to provide granular access control by assigning permissions to users based on their roles and responsibilities.
  - In an RBAC system, roles are defined based on job functions or responsibilities within an organization.
  - Permissions or access rights are then assigned to these roles rather than directly to individual users.
  - This simplifies the administration process by allowing administrators to manage access control based on roles rather than individual user accounts.

- ABAC
  - **Attribute-Based Access Control** is an access control model that uses various attributes associated with the user, resource, environment, and other contextual factors, as the basis for making authorization decisions.
  - ABAC evaluates these attributes to determine whether a user should be granted or denied access to a resource.

- What do we know so far?
  - Windows Server is the operating system designed for server environments, while Active Directory is a directory service provided by Windows Server for managing network resources.
  - Domain Controllers are servers running Windows Server that host and manage Active Directory, providing authentication and authorization services.
  - DNS is a separate service that resolves domain names to IP addresses and plays a critical role in network communication.
    - In an Active Directory environment, DNS provides name resolution services, locates domain controllers and other AD-related services, stores SRV records for AD resource location, ensures correct domain name resolution, and integrates closely with Active Directory for proper functioning of the directory service.
  - ADAC is a management tool used to simplify administrative tasks in Active Directory, providing a graphical interface for managing objects.
  - Group Policy is a feature of Windows Server and Active Directory that allows administrators to define and enforce configurations and policies across the network.
    - Active Directory and Group Policy work together by leveraging the directory service capabilities of Active Directory to store and manage information about network objects, while Group Policy utilizes that information to apply configurations and policies to specific computers or users within the Active Directory environment.
    - Group Policy settings can be defined in the Group Policy Management Console (GPMC) and linked to domains, OUs, or individual objects to control settings and enforce policies. The Group Policy processing order, inheritance, and cumulative effects ensure that policy settings are applied based on the configured hierarchy and precedence rules.

- Explore the relationship DNS server has with the endpoint
  - DNS server says "Hey there's a domain now that you can join! I know the DC's IP, let me send you its IP..."
  - When a DNS server detects the creation of a new domain, it informs the endpoints by sending them information about the domain.
  - However, if an endpoint is not configured to use a DNS server that is aware of the domain, any DNS server it is using will not have information about the newly created domain. That means that the endpoint will not be able to access resources within that domain.


#### Execute

- Deploy RSAT software package to endpoint
- Connect ADAC to Windows Server

## Helpful Resources

- [Microsoft Documentation - Active Directory Administrative Center](https://docs.microsoft.com/en-us/windows-server/identity/ad-ds/get-started/adac/active-directory-administrative-center)
