.. Copyright 2017 FUJITSU LIMITED

.. _workspaceComment-dislike:

workspaceComment_dislike
------------------------

.. function:: DELETE /orgs/{oid}/workspaces/{wid}/comments/{cid}/likes

.. sidebar:: Summary

	* Method: ``DELETE``
	* Response Code: ``204 / 200``
	* Response Formats: 
	* Since: ``UForge 3.6``

Dislike a comment in a workspace.

Security Summary
~~~~~~~~~~~~~~~~

* Requires Authentication: ``true``
* Entitlements Required: ``appliance_create``

URI Parameters
~~~~~~~~~~~~~~

* ``wid`` (required): the id of the :ref:`workspace-object`
* ``oid`` (required): the id of the :ref:`org-object`
* ``cid`` (required): the id of the :ref:`comment-object`

HTTP Request Body Parameters
~~~~~~~~~~~~~~~~~~~~~~~~~~~~

None

Example Request
~~~~~~~~~~~~~~~

.. code-block:: bash

	curl "https://uforge.example.com/api/orgs/{oid}/workspaces/{wid}/comments/{cid}/likes" -X DELETE \
	-u USER_LOGIN:PASSWORD -H "Accept: application/xml"

.. seealso::

	 * :ref:`comment-object`
	 * :ref:`workspace-api-resources`
	 * :ref:`workspaceComment-create`
	 * :ref:`workspaceComment-delete`
	 * :ref:`workspaceComment-deleteAll`
	 * :ref:`workspaceComment-dislike`
	 * :ref:`workspaceComment-get`
	 * :ref:`workspaceComment-like`
	 * :ref:`workspaceComment-reply`
	 * :ref:`workspaceComment-reportAbuse`
	 * :ref:`workspaceComment-update`
	 * :ref:`workspaceComments-getAll`
