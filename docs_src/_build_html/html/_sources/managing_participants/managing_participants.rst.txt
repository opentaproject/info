.. _intro:

.. include:: ../global.rst



Manage users 
================

* Try out anonymous logins
	* The link ``course-name.opentaproject.com/lti/index`` should now allow anonymous logins 
	* A self registration should be possible after a successful anonymous login
* Make sure the toolbar is visible by clicking ``v`` at the top left
* Click the gear in the toolbar to see the administration interface
	* See who is registered and their status by selecting ``Users``
	* Please don't add or delete fields that are available until you know what you are doing.

Creating additional privileged users
===============
Once an anonymous user has registered, the user is promoted to ordinary student. A superuser can further escalate the privileges. To promote a user to full superuser, do the following

* Go into the admin interface and select ``Users`` and select the user to be promoted
* In the ``Change User`` page
	* Check ``Staff Status`` and ``Superuser status``
	* Remove the user from the ``Student`` and ``AnonymousStudent`` group
	* Add the groups ``Admin``, ``Author`` and ``View``
	* No permissions are necessary; they come automatically with the group
	* Set ``LtiRoles`` to ``ContentDeveloper,Instructor`` i.e. a string with a comma in the middle
* If that is what you want, make user ``SuperUser`` to give full superuser privileges
* Press ``Save``

Deleting Users
=====

* Use the admin interface (gear icon in the header)
* ``Users -> Delete``
* Confirm `All user data will be deleted; all database entries and all submitted files. There will be no records kept at all`
* Another way to disable an individual student is to select the student, then remove the student from all groups.
* A student who is deleted when OpenTA is used in with LTI authentication will be reauthorized upon LTI access. The  student must be removed from Canvas enrollment to disable all further access.

Disable all student access
======

 * To disable all student access, unpublish the course.
