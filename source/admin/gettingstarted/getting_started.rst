.. _intro:

Known bugs
===========

* History in xml is not working
* Thumbnails sometimes do not show in student images
* Password reset from canvas fails since it demands old password


Login for the first time
============

.. include:: ../global.rst


* Obtain access to your course |hostname|
* Login to to the server ``|hostname|`` that servers your course ``|coursename|`` and login with your email and password which is probably your email. You will probably have to change your password. 

.. |baseimage| image:: /front/mobile_exercise.png





Create the first exercise
=============
* After login , several buttons are visible.  ``ShowAll`` shows or hides unpublished exercises. 
* Select the ``ShowAll`` button to make it black.  You will now see a "+" with Exercise name. 
* Fill in file name of some exercise. What that filename is is unimportant. 
* Hit return.

You will now have a new example exercise.

Edit the exercise
===============
* Click the exercise and select the ``v`` tab at the top left of thte page to reveal a toolbar. 
* Select ``LiveEdit``

You will now have a split screen with the formatted exercise on the left and the xml on the right. 

* Press the "Assets" button on the top
* Press the camera icon to upload a jpg or png file 
* Change the field ``UPLOAD-ME-OR-ERASE-THIS-LINE.png`` to the name of the image file you uploaded.  *Use a small file, a few 100Kb at most*

* Change the field ``exercisnename`` tag  to the name you want the exercise to have.

If you are impatient to improvise on the file by editing the xml, note the following basic points.

* Delete any sections you want; make sure xml remains legal
* You can try some standard html syntax. Remember though 

	* all tags must be closed. 
	* not all html is implemented.
	* all text and html belongs inside the ``<text>`` tags

* The tag ``expression``  is the correct answer to the question
* All variables in ``expression`` must receive numerical assignments in the ``global`` directive
* All question keys must be unique in the exercise
* All choices keys must be unique in the multiple choice question.
* ``vi``  mode is enabled if you choose ``Switch keymap default``. 
* ``<right>`` is to right justify figure on the page. Delete the entire line if you are not going to use a figure
* Mathematical expressions are interpreted through `KaTeX <https://khan.github.io/KaTeX/>`_., which is a subset of `latex` for the web. 


Save the exercise
========

* You will not be able to save if there  are xml errors
* Press ``Save`` when there are no error.

* In case you make a mess of the xml and can't recover
	* Try ``Reload``, the blue button next to the ``Save`` in the editing box
	* Start over completely and reload the question
	* If the xml is really messed up , try ``XML & assets`` instead of ``Live Edit``


Publish the exercise
======

* Press ``Options`` in the toolbar, which is next to `LiveEdit` in the blue toolbar.
* Select ``Published`` 
* Press ``Save`` to publish the exercise


Publish the course
==================

Make sure the toolbar shows; if not press the ``v`` in the top left corner

* Choose ``Course`` abc |hostname| efg
* Choose ``Options`` 
* Fix up course Options
	* Put in your own email in ``email reply to``
	* check yourself and ``super`` as owners
	* choose a name for your course unless you want to keep it your cid
	* check ``Allow anonymous student`` if you want to permit anonymous logins. (You can disaable this later and remove anonymously registered students if you want.) 
* Choose ``Save``
* See what the course looks like for students by checking ``Student view``


More examples
======

Login to `examples.opentaproject.com <https://examples.opentaproject.com/lti/index>`_ ( anonymous login is enabled )

Let others see your website
================

* Try out anonymous logins
	* The link ``course-name.opentaproject.com/lti/index`` should now allow anonymous logins 
	* A self registration should be possible after a successful anonymous login
* Make sure the toolbar is visible by clicking ``v`` at the top left

See who has used your site 
=======

* Click the gear in the toolbar to see the administration interface
	* See who is registered and their status by selecting ``Users``
	* Please don't add or delete fields that are available until you know what you are doing.



Panic: Exercises are messed up
=======

Recover from a broken state

* Choose ``Exercises -> Reload Exercises`` and choose ``OK``

