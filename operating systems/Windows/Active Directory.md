---
tags:
  - os
  - networking
  - windows
---
# Active Directory

>[Reference video](https://www.youtube.com/watch?v=VLWt0-8BOV4&list=PLG49S3nxzAnna96gzhJrzkii4hH_mgW4b&index=29&t=1s).

This is a "directory service" developed by Microsoft for Windows networks. It stores information about objects on a network (such as printers, computers, users, etc.) in a hierarchical structure to easily manage permissions and control access to network resources.

Note that this is Windows only. However, I'm sure that there are Linux plugins or packages for this too for management. If not, you could use something like [Ansible](https://www.ansible.com/).

>Active Directory runs on a Windows Server that's connected to your network.

It is a centralized database of everything that's configured in a corporate structure. This includes:

- computers
- user accounts
    - reset passwords
    - add or remove users
- file shares
- printers
- groups
- user permissions
- group permissions
- etc

>The way to interface with this service is via. Group Policy.

This is the most efficient way to manage a large number of Windows machines for a corporation.

## Organizational Unit (OU)

This is a way to keep your active directory structure organized. By creating smaller chunks that manage certain aspects of your network. For example, you can create an OU for accounting, development, IT, etc. to manage permissions for all employees. Or, create an OU for each country, state, building, department, etc.

Finally, you can apply different policies to different OUs.

>I'm assuming that these policies will affect all substructures and not just that current grouping.

## Login Scripts

>Submenu: User Configuration > Policies > Windows Settings > Scripts

These are very handy, they're basically like `.bashrc` files or shell scripts that run on startup. You can add batch scripts or PowerShell scripts that will run whenever a user logs in on a given computer.

Some use cases:

- add a mapped drive
- add printers
- add permissions

You can assign scripts to:

- users
- groups
- [[#Organizational Unit (OU)|organizational units]]

>As far as I'm aware, these scripts are stored on the active directory server and not the local machine.

Here's an example login script that mounts a fileshare:

```bat
net use G: \\SGC-AD\files
net use [mount-point] \\[domain-name]\[file-share|path]
```

## Home Folders

You can assign a user's home folder to a network folder, this allows you to manage and backup files from the network and avoid storing files on the local computer.

This is useful in case a user's computer gets lost or stolen or, they accidentally delete a file.

## Folder Redirection

>Submenu: User Configuration > Policies > Windows settings > Folder Redirection.

Some users and applications use Windows Library folders such as `Desktop/`, `Documents/`, `Music/` and `Downloads/`. You can redirect these folders to somewhere in the active directory service.

## Security Groups

This is how you assign permissions to a group, this is like a template where groups or users can have multiple security groups that add permissions to them.

There are some built-ins:

- users
- guests
- remote management users
- event log readers
