# Security Policy Overview

* Can be defined on the project, folder, and organization level, as well as on some resources
* Inherited downwards

<br>

# Resource Hierarchy

```Text
OrganizationNode
|__ Folder
|____ Project
|______ Resources
```

## Organization Node

* There are special permissions that only exist at the organizational level
* The creation of an organization depends on whether or not the company is already a Google Workspace customer (*Google Workspace customers will have their projects automatically belong to your organization node and non-Google Workspace customers must use Cloud Identity to create the organization node*)

## Folder

* The resources within a folder will inherit its applied policies and permissions
* Can contain subfolders

## Project

* Projects are separate entities under the Organization node

| Identifying attribute | Description |
| --- | --- |
| Project ID | A globally unique ID that can't be changed after creation |
| Project Name | A name you give to your project and that can be changed when desired |
| Project Number | A globally unique number that can't be changed after creation |

## Resources