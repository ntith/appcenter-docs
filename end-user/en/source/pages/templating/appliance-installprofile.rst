.. Copyright (c) 2007-2016 UShareSoft, All rights reserved

.. _appliance-install-profile:

Updating the Install Profile
----------------------------

The ``Install Profile`` on the ``Stack`` page allows you to customize the questions asked when the image is booted for the very first time (or during installation for an ISO image). The install profile is mandatory.

You can define the following as part of the install profile:

* ``Root User``: The root user password by default is prompted during the first boot of the machine image i.e. ``ask during installation``. However, you can pre-set a root  password. You can all enter an SSH key to allow users to login as root. If you select ``Disable root password login via SSH``, root will still be able to login from the console.
* ``Users and Groups`` (optional): you can add operating system users and groups. See :ref:`appliance-install-profile-users-groups` for more information
* ``Internet Settings``: default is “set automatically”
* ``Partitioning``: default is “set automatically”. You can modify the disk and swap size for the automatic set up, ask during install, or set up ``Advanced Partitioning`` (for several disks). For more information see :ref:`appliance-install-profile-partitioning`.
* ``Kernel Parameters``. You can add kernel parameters by clicking add and save.
* ``Keyboard``: default is “ask during installation”
* ``Licenses``: default is “accept licenses during installation”
* ``Time Zone``: default is “set automatically to London”
* ``Welcome Message``
* ``Services``: Firewall is set to "Off" by default. This parameter allows you to activate or deactivate the firewall present in the filesystem when launching the appliance (regardless of whether the firewall is iptables or other).

.. _appliance-install-profile-users-groups:

Adding Users and Groups
~~~~~~~~~~~~~~~~~~~~~~~

You can add operating system users and groups to the appliance Install Profile. These will be integrated to the appliance template.

.. warning:: The users and groups created in UForge are not linked. If you create a user and list it as part of a specific group, you must then also create the group; otherwise the image generation will fail. 

To add a user to an appliance:

	1. Select the appliance template you want to modify.
	2. From the ``Stack`` page, click on ``Install Profile`` in the toolbox.
	3. Select ``Users and Groups``.
	4. Click ``add``, next to the top table. The ``Create User`` page will be displayed.

	.. image :: /images/install-profile-create-user.jpg

	5. Enter a user name.
	6. If you want to manually enter the user ID, deselect ``set the user id automatically`` and enter the ID number.
	7. If you want to manually create the primary group the user is part of, deselect ``automatically create primary group for user`` and enter the group name. 
	8. Click ``create``

.. warning:: If you create a user and list it as part of a specific group, you must then also create the group; otherwise the image generation will fail. 


To add a group to an appliance install profile:

	1. Select the appliance template you want to modify.
	2. From the ``Stack`` page, click on ``Install Profile`` in the toolbox.
	3. Select ``Users and Groups``.
	4. Click on ``add`` next to Group table at the bottom. The ``Create Group`` page will be displayed.

	.. image:: /images/install-profile-create-group.jpg

	5. Enter a group name.
	6. Check if you want this group to be a system group.
	7. If you want to manually enter the group ID, deselect ``set the group id automatically`` and enter the group ID number.
	8. Click ``create``.
