.. include:: ../Includes.txt

.. _webhook:

=======
Webhook
=======

This section describes how to add webhooks for auto rendering to a repository.

The system currently supports Git as VCS (Version Control System), and the
following hosters:

  - :ref:`webhook-github`
  - :ref:`webhook-bitbucket-cloud` and Bitbucket self-hosted
  - :ref:`GitLab Cloud <webhook-gitlab>` and :ref:`GitLab self-hosted <webhook-gitlab>`

If none of the above is used, a mirror to one of these is recommend. Also the
`Documentation Team <https://typo3.org/community/teams/documentation/>`__ can
setup custom hostings.

The following chapters provide illustrated walkthrough tutorials on how to add
the necessary hook in those systems.

.. _webhook-how-webhook-works:

How webhook works
=================

If that's the first time working with webhooks, take a look at `GitHub developer
<https://developer.github.com/webhooks/>`_. The configuration below triggers
rendering only on push events. In order to trigger a rendering, a push has to
happen.

In order to test the integration, a push to `master` branch or
`documentation-draft` branch can be used, see :ref:`migrate-branches`.

.. _webhook-legacy:

Legacy webhook
==============

If the repository already had a hook, this is considered deprecated. A
compatibility layer is still in place, but will be removed in the future.

An update is necessary.

.. _webhook-github:

GitHub
======

Add auto rendering for a repository via GitHub webhook in five steps:

.. rst-class:: bignums-xxl

#. Go to "Settings" tab within the repository

   .. figure:: /images/webhook/github/repository-start.png
      :width: 932

#. Go to "Webhooks" section within the repository settings

   .. figure:: /images/webhook/github/settings-tab.png
      :width: 932

#. Add webhook

   .. figure:: /images/webhook/github/webhook-section.png
      :width: 932

#. Fill in webhook configuration

   #. Configure URL ``https://docs-hook.typo3.org`` for field "Payload URL".

   #. Select ``application/json`` as "Content type".

   #. Enable "SSL verification".

   #. Select ``Just the push event.`` for "Which events would you like to trigger this webhook?".

   #. Enable "Activate".

   #. Click on "Add webhook"

   .. figure:: /images/webhook/github/webhook-add.png
      :width: 932

#. Webhook was added

   GitHub should show a notice that creation of webhook was successful.

   .. figure:: /images/webhook/github/webhook-added.png
      :width: 932

#. (Optional) visit intercept and check request

   If curious, visit https://intercept.typo3.com/admin/docs/deployments and
   check "Recent actions" (scroll down). The repository should have created a
   "Docs hook ping from github repository".

   .. figure:: /images/webhook/github/intercept-feedback.png
      :width: 932


.. _webhook-bitbucket-cloud:

Bitbucket Cloud
===============

Add auto rendering for a repository via Bitbucket webhook in five steps:

.. rst-class:: bignums-xxl

#. Go to "Settings" section within the repository

   .. figure:: /images/webhook/bitbucket/cloud/repository-start.png
      :width: 932

#. Go to "Webhooks" section within the repository settings

   .. figure:: /images/webhook/bitbucket/cloud/settings-tab.png
      :width: 932

#. Add webhook

   .. figure:: /images/webhook/bitbucket/cloud/webhook-section.png
      :width: 932

#. Fill in webhook configuration

   #. Choose a title for this hook: e.g. "TYPO3 Docs".

   #. Fill URL field with ``https://docs-hook.typo3.org``.

   #. Enable "Active" Status.

   #. Select ``Repository push`` for "Triggers".

   #. Click on "Save"

   .. figure:: /images/webhook/bitbucket/cloud/webhook-add.png
      :width: 932

#. Webhook was added

   Bitbucket should show a notice, which disappears after some seconds, that
   creation of webhook was successful. Also the webhook should be shown in the
   list.

   .. figure:: /images/webhook/bitbucket/cloud/webhook-added.png
      :width: 932

#. (Optional) visit intercept and check request

   If curious, visit https://intercept.typo3.com/admin/docs/deployments and
   check "Recent actions" (scroll down).

   In order to appear, the hook needs to be triggered. Therefore either the
   branch ``master`` can be pushed. Or a new Branch ``documentation-draft`` can
   be created and pushed.

   .. figure:: /images/webhook/bitbucket/cloud/intercept-feedback.png
      :width: 932

.. _webhook-gitlab:

GitLab Cloud and GitLab self-hosted
===================================

Add auto rendering for a repository via GitLab webhook in four steps:

.. rst-class:: bignums-xxl

#. Go to "Integrations" section within the repository

   .. figure:: /images/webhook/gitlab/repository-start.png
      :width: 932

#. Add webhook by filling in webhook configuration

   #. Fill URL field with ``https://docs-hook.typo3.org``.

   #. Select ``Push events`` and ``Tag push events`` for "Trigger".

   #. Click on "Add webhook"

   .. figure:: /images/webhook/gitlab/webhook-add.png
      :width: 932

#. Webhook was added

   The webhook should be shown in the list (scroll down).

   .. figure:: /images/webhook/gitlab/webhook-added.png
      :width: 932

#. (Optional) Trigger webhook and visit intercept to check request

   If curious, visit https://intercept.typo3.com/admin/docs/deployments and
   check "Recent actions" (scroll down).

   In order to appear, the hook needs to be triggered. Therefore either the
   branch ``master`` can be pushed. Or a new Branch ``documentation-draft`` can
   be created and pushed.

   .. figure:: /images/webhook/gitlab/intercept-feedback.png
      :width: 932
