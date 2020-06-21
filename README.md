ubuntu_workstation
==================

This is my idea on how to bootstrap an Ubuntu workstation ready to work as a devops, sysadmin and (at least partiall) developer.
It is tailored to meet my specific needs, but it is a verbose one.
Here you can find packages and configuration that I assume I may need for working purposes.
This also includes the most common messengers that you may need in work.

From clouds I will start with AWS and Azure CLIs, Google stuff may become available in future.

I may come up with entertainment related packages too in future, but this is not the main goal.
Don't expect steam / playonlinux / lutris and/or others here soon.

Staring / watching the project will motivate me to put more efforts into this playbook.

:warning: WARNING :warning:
-------

:rotating_light: :rotating_light: :rotating_light: :rotating_light: :rotating_light:

Ensure that you understand what is going on in this playbook.
It contains potentially dangerous operations like forced firmware update or installation of tfswitch with the use of curled script piped to bash.
There is no warranty that no malicious operations can happen in future in curled scripts piped to bash and updating firmware on low battery can damage your hardware (this is why you need to use --force to update firmware), so make sure you understand this warning, don't just run it blindly!

:rotating_light: :rotating_light: :rotating_light: :rotating_light: :rotating_light:

Credits
-------

As the initial idea of creating and opensourcing this role came from myself long time ago already, I have started in June 2020.
By that time many other similar roles were published already and I owe everyone a credit for any smallest piece of code I might have used.
I hope I haven't missed anyone.

So credits and thanks to:
* [Patrick Bulteel](https://github.com/pbulteel/ansible-laptop)

Requirements
------------

Requirements are simple - everything has to be in latest version - I will not keep it backward compatible.

How to use
----------

You need to review and tune the variables to fit your needs.
Don't blame me if something is added, removed or configured that you did not want to happen.

To start bootstraping just run:
`ansible-playbook workstation.yml -K`
Remember you have to meet dependencies - it may work if they are unmet, but I don't guarantee that.
I also recommend checking the playbook with dry run first:
`ansible-playbook workstation.yml -K --check`
Although it will fail on some steps now as no tests are prepared - they may be introduced in future or never.

The idea is to bootstrap current instance and playbook is prepared in such way - see `ansible.cfg` and `workstation.yml` for details.

Dependencies
------------

To start using this playbook you need to have latest Ubuntu with latest Ansible installed

License
-------

MIT

Author Information
------------------

You can contact me on telegram: https://t.me/tymikk
