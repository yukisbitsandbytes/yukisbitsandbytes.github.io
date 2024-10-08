---
title: "Active Directory Domain Services"
layout: post
date: 2024-08-27
feature_image: images/activedirectory.png
tags: [ad, activedirectory, networking]
---

! NOTICE! Due to the nature of github pages, this page remains a draft until 9/20/24. 

*Writeup summarizing my learning experience with Active Directory.*

<!--more-->

<br>
<div align="center">.・。.・゜✭・.・✫・゜・。. </div>
<br>

## Table of Contents

1. [AD Overview](#ad-overview)

<br>
<div align="center">.・。.・゜✭・.・✫・゜・。. </div>
<br>

┌──❀*̥˚───────────────────────────────────────────────❀*̥˚─┐
### AD Overview
✧. ┊ ⁭ [tbd](#ೃ⁀-tbd) ✧ [tbd](#ೃ⁀-tbd) ✧ [tbd](#ೃ⁀-tbd) ⁭ ⁭┊ .✧

<br>
####  ೃ⁀➷ What is Active Directory?
Active Directory is a Microsoft database tool that allows companies to manage their IT infrastructure and can manage users, objects, domains, devices, and groups. AD DS allows for a hierarchical directory and a way for network admins to apply configuration and security settings for user accounts easily. 

<br>
- Schema: Definitions of object types and attributes for objects
- Domain: Contains objects like users and computers. Shares network configuration. 
- Domain Tree: Collection of domains that have a root and DNS namespace (hierarchical tree)
- Forest: A collection of 1+ domains that have the same root, schema, and global catalog
- OU: Organizational Unit is a container object that holds users, groups, and computers. Links GPOs (Group Policy Objects). They can represent an org's organizational chart and also nest inside of each other. 
- Container: Object for organization. Can not link GPOs. OUs cannot be created within a container.

<br>
- User Account: All users that need access to network resources should have a user account which can authenticate to the AD DS domain in order to access the resources. User accounts have a username, password, and groups. User objects can be created or managed with the AD Administrative Center, AD Users and Computers, Windows Admin Center, PowerShell, or dsadd.
- Managed Service Accounts: Services that run at startup or other events and don't require user interaction can use a service account to start up and authenticate. 
- Groups: Group users together to easily assign permissions and rights. Security groups are security enabled. Distribution groups are not security enabled, and can be used for email applications. Groups also have a scope such as local (local workstation), domain-local (all workstations in local domain), global (for a department or specific geographic location), and universal (assign anywhere in forest). 
- Objects: Contains objects like users, computers, servers, clients, hardware, shared files/folders, etc

<br>
 ```dsa.msc``` is the command to open AD Users and Computers
```Net user``` is a built in Windows command to manage and create users. EX: ```net user yukisbytes P@ssw0rd /add``` or ```net user yukisbytes``` to view information.
```gpupdate``` is the command to update group policy


INCLUDE A DIAGRAM OF AD HIERARCHY (forest, tree, domain, OU, users, computer, etc)


└───❀*̥˚───────────────────────────────────────────────❀*̥˚┘


<br>
<div align="center">.・。.・゜✭・.・✫・゜・。. </div>
<br>



#### Sources & References
