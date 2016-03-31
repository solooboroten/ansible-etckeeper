# ansible-etckeeper

Install and configure etckeeper.

Forked from [groover.etckeeper](https://github.com/silpion/ansible-etckeeper).

## Requirements

None.


## Installation

To install it, run:

    ansible-galaxy install https://github.com/solooboroten/ansible-etckeeper.git


## Role Variables

* ``etckeeper_vcs``: Configure the VCS etckeeper shall use (string, default: ``git``, values: [``git``, ``mercurial``, ``bzr``, ``darcs``])
* ``etckeeper_git_commit_options``: Configure Git commit options for etckeeper (string, default: "")
* ``etckeeper_hg_commit_options``: Configure Mercurial commit options for etckeeper (string, default: "")
* ``etckeeper_bzr_commit_options``: Configure Bazaar commit options for etckeeper (string, default: "")
* ``etckeeper_darcs_commit_options``: Configure Darcs commit options for etckeeper (string, default: "")
* ``etckeeper_avoid_special_file_warning``: Configure etckeeper to set AVOID_SPECIAL_FILE_WARNING=1 (bool, default: ``false``)
* ``etckeeper_avoid_daily_autocommits``: Configure etckeeper to set AVOID_DAILY_AUTOCOMMITS=1 (bool, default: ``false``)
* ``etckeeper_avoid_commit_before_install``: Configure etckeeper to set AVOID_COMMIT_BEFORE_INSTALL=1 (bool, default: ``false``)


## Example Playbook

    - hosts: servers
      roles:
         - { role: etckeeper, etckeeper_vcs: darcs }


## License

Apache Version 2.0


## Integration testing

This role provides integration tests using the Vagrant.

    # run the complete test suite with Vagrant
    vagrant up


## Author information

[Aleksey Avdeev](https://github.com/solooboroten)

### Contributions

Thanks for their thoughts and work goes to...

* Mark Kusch @mark.kusch silpion.de (the author of the original `groover.etckeeper`)
* [Karl Goetz](https://github.com/goetzk)
* [ypid](https://github.com/ypid)


<!-- vim: set nofen ts=4 sw=4 et: -->
