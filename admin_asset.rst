Asset Management
=============

一、资产列表
`````````````````
1.1 Manage Asset Tree
Asset tree nodes cannot be renamed, right-click on nodes to add, delete, and rename nodes, and perform asset-related operations

.. image:: _static/img/admin_assets_asset_list.jpg

1.2 Create assets for asset tree nodes
On the asset list page, first select the node to which the asset is to be added, and then select Create Asset on the right
.. image:: _static/img/admin_assets_asset_create.jpg

Domain list
`````````````````


2.1 网域列表
The domain function is a newly added function to solve the problem that some environments (such as hybrid cloud) cannot be directly connected. The principle is to log in through the gateway server.
.. image:: _static/img/admin_assets_domain_list.jpg

2.2 Create a domain
On the Domain List page, select Create Domain on the right
.. image:: _static/img/admin_assets_domain_create.jpg

2.3 Gateway List
.. image:: _static/img/admin_assets_domain_gateway_list.jpg

2.4 Create Gateway
On the domain list page, click the number under the gateway to enter the gateway list, and click Create Gateway. The gateway can be any asset with ssh service
.. image:: _static/img/admin_assets_domain_gateway_create.jpg

Third, manage users
`````````````````````
The management user is the root on the asset (the controlled server) or a user with NOPASSWD: ALL sudo permissions. JumpServer uses this user to push system users and obtain asset hardware information. Windows Please fill in the users in the administrators group

3.1 Manage user list
.. image:: _static/img/admin_assets_admin-user_list.jpg

3.2 Create Administrative User
.. image:: _static/img/admin_assets_admin-user_create.jpg

Fourth, system users`````````````````````

The system user is the user that JumpServer uses to log in to the asset. It can be understood as the user who logs in to the asset, such as web, sa, dba (`ssh web @ some-host`), instead of using a user's username to log in to the server (`ssh xiaoming @ some-host`); To put it simply, users log in to JumpServer with their own username, and JumpServer uses system users to log in to assets. When the system user is created, if the automatic push is selected, JumpServer will use ansible to automatically push the system users to the asset. If the asset does not support ansible, please fill in the account password manually (domain user format: user@domain.com).

4.1 System user list
.. image:: _static/img/admin_assets_system-user_list.jpg

4.2 Create System User
.. image:: _static/img/admin_assets_system-user_create_01.jpg
.. image:: _static/img/admin_assets_system-user_create_02.jpg

Five, label management
````````````````
Label assets for easy query and management. The label information has a name and a value: the name can be a description of the function information, for example: purpose, and the value can be specific information, for example: organization 1-department 1-research and development. When creating a label, you can choose to label the existing asset.

5.1 Label list

.. image:: _static/img/admin_assets_label_list.jpg

5.2 Creating labels

Click the "Create Tag" button in the upper left corner of the page to enter the Create Tag page:

Tag names can be duplicated, and an asset can have multiple tag properties. Tag deletion, tag information on the asset will disappear automatically
.. image:: _static/img/admin_assets_label_create.jpg

Command filtering
````````````````

System users can bind some command filters. A filter can define some rules. When a user uses this system user to log in to an asset, and then execute a command, this command needs to be matched by all the rules of the bound filter. High priority is matched first. When a rule is matched, if the action of the rule is allowed, the command will be released. If the action of the rule is prohibited, the command will be prohibited from executing, otherwise the next rule will be matched, and if no rule is finally matched, the execution will be allowed

6.1 Command filter list
.. image:: _static/img/admin_assets_cmd-filter_list.jpg

6.2 Create a command filter
Click Create Command Filter on the Command Filter List page
.. image:: _static/img/admin_assets_cmd-filter_create.jpg

6.3 Command filter rule list
Click the number below the rule on the command filter list page to enter the rule page

.. image:: _static/img/admin_assets_cmd-filter_rule_list.jpg

6.4 Create rule

Click the number below the rule on the command filter list page to enter the rule page, and click Create Rule
.. image:: _static/img/admin_assets_cmd-filter_rule_create.jpg
