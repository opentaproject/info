.. _intro:

.. include:: ../global.rst


More Course Options
==================

Make sure the toolbar shows; if not press the ``v`` in the top left corner

* Choose ``Course`` 
* Choose ``Options`` 
* Fix up course Options ; beginners ``Use LTI is unchecked``
	* ``Published`` check to publish
	* ``Course name`` a short name suitable for links without spaces or special charcters
	* ``Course long name`` descriptive name on web pages
	* ``Url``  - the full url of the course
	* ``Motd`` - short message for web pages; typically blank
	* ``Difficulties`` - Choices of badges to decorate exercises
		* ``+:Recommended,*:Easy ..`` for instance makes a badge '+' correspond tot the label recommended etc.
		* This can be anything you want; choices appear later in exercise options
	* ``Deadline time`` - time of day when exercises are due
	* ``Use lti`` - unchecked 
	* ``Registration by password`` - allow password for registration
	* ``Registration domains`` - domains from which to allow registration. Wildcard '*' OK. 
	* ``Use email`` - Enable email
	* Put in your own email in ``email reply to``
	* Ignore the following settings for opentaproject.com sites
		* ``Email host user`` - smtp ; ignore to use opentaproject sites
		* ``Email username`` - smtp username; ignore for opentaproject sites
		* ``Email host password`` - email password ; stored unencrypted
	* ``Use autotranslation`` - unchecked
	* ``Languages`` - default ``en`` ; language codes separated by comma, for instance ``sv,en,de``. Not particularly useful without auto translation. 
	* 
	* check yourself and ``super`` as owners plusChoose  whoever else should be able to view unpublished
	* `Only if you do not plan to use LTI i.e. Canvas or Moodle`
		* check ``Allow anonymous student`` to allow anonymous logins
* Choose ``Save``
* See what the course looks like for students by checking ``Student view``

Enable LTI i.e. Canvas or Moodle
=========

`This section is relevant only to those who will be using OpenTA from an LTI CMS such as Canvas or Moodle.`

`Important note:` do not allow students to first authenticate outside of canvas if that's how they will be expected to login later. The students identities must be first verified by the LTI. You cannot migrate a student into Canvas if the identity is not first established that way.

This assumes that you are able to install an LTI app in Canvas or Moodle. 

* In the ``Canvas`` interface, choose 
* Choose ``Settings -> Apps``
* Choose ``View App Configurations -> +App -> Configuration Type ->``
* Choose ``Configuration Type -> ByURL``


* In another tab or window, in OpenTA choose ``Course Options``
* Check ``Use LTI`` and ``Save`` and go back to ``Options``
* Copy the (OpenTA) entire config URL , including the ``https://`` into (LTI) ``Config URL``
* Copy the entire (OpenTA) ``Lti key`` into the LTI ``Consumer Key`` 
* Copy the entire (OpenTA) ``Lti secret`` into the LTI ``Shared Secret``
* Choose (Canvas) ``Submit``
* If all went well, the App has been added to Canvas.
* To allow students to easily break OpenTA out from the Canvas frame:
	*Add the canvas app `Redirect Tool` and point it to |hostname|

* `Instructions only for those whose superuser identity coincides with your Canvas identity`
	* Create a new superuser identity for yourself so it will be different from the identity you have in Canvas.
	* Note that you can assign yourself a password in the admin interface (click the gear icon in the header)
	* **Make sure you can login as the new superuser**
	* Then delete the original user so that identity can be recreated with an LTI login
	

* Try to login through the LTI. 
* Notes: 
	* Canvas opens OpenTA in a frame, not only taking valuable desktop space with sidebars and headers, but also causing security issues through third-party cookies.  Some admin features may not work in the Canvas frames, so it  is best to administer the course as superuser via direct login and not through canvas. 


	* `If you already have a user identity that coincides with that from canvas, change username and email of the old superuser to allow a new identity to be created from Canvas. If you want the Canvas identity to be superuser, change the user in the admin interface. It can be useful to retain a student identity when used through Canvas.`
	* To guard against misconfigurations by LTI admins, an LTI authenticated user will never automatically have access other than Student in OpenTA even if they are examiner or CourseDeveloper. The superuser must provide suitable non-student access to LTI authenticated users manually.

* Suggestion on dealing with course assistants and other admins
	* The best way to proceed is that the course createor obtains a new superuser identity, including password and then, after it is verified working,  deletes the original identity.  Then course creator logs in **through canvas**. The superuser login is then used to provide whatever privileges is desired to the new identity. Same procedure with course assistants; first the course assistant logs in through Canvas, then superuser promote privileges. 

	* This could of course have been done automatically if OpenTA respected a Canvas identity such as Examiner or CourseDeveloper. However, we have chosen not to rely on that, since a misconfiguration of roles from University Canvas services could mistakenly compromise the OpenTA site.
