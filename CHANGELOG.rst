=========
Changelog
=========

----------
Git master
----------

--------------------------
Version 1.3.0 (2017-04-20)
--------------------------

- Remove unnecessary ``no_log``.

- Fix warning for template delimiters in a when statement (`#24`_).

- Allow overriding ``solita_jenkins_password_dir``.

--------------------------
Version 1.2.1 (2017-04-12)
--------------------------

- Add support for Jenkins 2.54.

--------------------------
Version 1.2.0 (2017-03-23)
--------------------------

- Add credential management.

- Upgrade ``geerlingguy.jenkins`` to ``2.5.0``.

- Stop Jenkins to create ``config.xml`` if it's missing. This can happen if the
  role execution installs and starts Jenkins for the first time.

- Add tag ``solita_jenkins_plugins`` (`#17`_).

--------------------------
Version 1.1.0 (2016-07-15)
--------------------------

- Fix permission issues due to missing ``become`` options.

- Try to work around ``inventory_dir`` being ``None`` (`#14`_).

- Upgrade ``geerlingguy.jenkins`` to ``2.2.0``.

- Create an SSH key pair for ``jenkins`` and always run Jenkins CLI as
  ``jenkins``. This way all Ansible users have access to the key added to the
  ``solita_jenkins`` Jenkins user.

- Don't change ``solita_jenkins``' password when the default password changes
  (e.g. when ``solita_jenkins_default_password/solita_jenkins`` is deleted or
  the host is provisioned from another Ansible control machine).

- Fix idempotence issues.

- Don't make files containing ``solita_jenkins``' password world-readable.

--------------------------
Version 1.0.2 (2016-07-03)
--------------------------

- Fix issues with ``become_user: jenkins`` on Ansible 2.1.

--------------------------
Version 1.0.1 (2016-07-01)
--------------------------

- Prevent Jenkins restart when variable ``solita_jenkins_restart`` is set to
  ``no``.

--------------------------
Version 1.0.0 (2016-06-29)
--------------------------

- Add support for Jenkins 2.

.. _#14: https://github.com/solita/ansible-role-solita.jenkins/issues/14
.. _#17: https://github.com/solita/ansible-role-solita.jenkins/issues/17
.. _#24: https://github.com/solita/ansible-role-solita.jenkins/pull/24
