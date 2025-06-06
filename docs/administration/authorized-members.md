# Authorized members

**Authorized members** allow to restrict access to an entity to certain users, groups, or organizations within the platform.

Three levels of access are available:

- View: read-only access to the entity.
- Edit: view and modify the entity.
- Manage: view, modify, delete, and administer access to the entity.

Once authorized members are defined, they will be the only ones with access to the entity. To prevent the creation of "ghost" entities—entities that are only accessible in read-only mode without the ability to delete them—it is mandatory to define an administrator. If you attempt to define authorized members without an admin, an error message message will be displayed.

**Authorized members** are available at multiple levels within the platform:

- Custom Dashboards
- Investigations
- Feedbacks
- Reports
- Groupings
- Incident Response
- Request for Information
- Request for Takedown

## Set up authorized members

To define authorized members, you need to click on the '**Manage Access Restriction**' button. This button is visible if you have the '**Manage Authorized Members**' capability.

![authorized-members-manage-access-button.png](assets%2Fauthorized-members-manage-access-button.png)

![authorized-members-pop-up.png](assets%2Fauthorized-members-pop-up.png)

If you grant access to users belonging to an Organization, it is possible since version 6.6 of OpenCTI to restrict access even more specifically to users belonging to one or more groups, in order to provide more granularity in access control.

![authorized-members-group-intersection.png](assets%2Fauthorized-members-group-intersection.png)

For the containers **Report**, **Grouping**, and **Incident Response**, as well as **Case RFT** and **Case RFI**, it is possible to define authorized members directly when creating the entity.

![authorized-members-creation-form.png](assets%2Fauthorized-members-creation-form.png)

## Administrate restricted entities

It is possible to access the list of entities restricted by authorized members via the '**Data > Restrictions**' tab. This tab is accessible to a platform administrator with the '**Bypass**' capability, ensuring that all entities with authorized members are listed without any restriction. Through this tab, it is possible to view the entities restricted by authorized members as well as additional information, such as the date when authorized members were activated. The administrator can also choose to remove the restriction by clicking on the '**Remove Access Restriction**' padlock.
 
![authorized-members-restrictions.png](assets%2Fauthorized-members-restrictions.png)

## Authorized members and organization segregation

!!! tip "Enterprise edition"

    Platform segregation by organization is available under the "OpenCTI Enterprise Edition" license. Please read the [dedicated page](enterprise.md) to have all the information.

Enabling restriction to access to the below containers is under Entreprise edition. But enabling it on dahboard and investigations is not.

For certain container **Reports**, **Groupings**, **Incident Response**, **Case RFI**, and **Case RFT** when segregation by organization is enabled and the container is shared with an organization, it is possible to define authorized members to further restrict access to these members who do not belong to the organization.


**This restriction will only apply to the container and will not cascade to the entities contained within the container.**

Once authorized members are activated for these entities, data segregation by organization is disabled for that specific entity. Only the authorized members will have access to the entity, and the 'Share with an organization' button in the interface is deactivated.

![authorized-members-organization-sharing-deactivation.png](assets%2Fauthorized-members-organization-sharing-deactivation.png)
