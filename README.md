This Ansible playbook collection provides scaffolding for automating
launch and teardown of BDR node groups for testing purposes.

It's oriented toward testing from git, but can be easily adapted
to test packaged releases too.

Currently it's focused on running BDR on multiple ports on the
same host, but it's simply extensible to run on top of libvirt
hosts (statically or dynamically provisioned), on AWS, etc.

**Do not use this for any data you care about**. It is entirely
happy to `rm -rf` your data directory. This is a *testing tool only*.

Usage
---

    ansible-playbook bdr.md
