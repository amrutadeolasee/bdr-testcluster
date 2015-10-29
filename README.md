This Ansible playbook collection provides scaffolding for automating
launch and teardown of pglogical node groups for testing purposes.

It's oriented toward testing from git, but can be easily adapted
to test packaged releases too.

Currently it's focused on running pglogical on multiple ports on the
same host, but it's simply extensible to run on top of libvirt
hosts (statically or dynamically provisioned), on AWS, etc.

**Do not use this for any data you care about**. It is entirely
happy to `rm -rf` your data directory. This is a *testing tool only*.

Usage
---

    ansible-playbook pglogical_output.yml


Some handy debug commands
---

    - name: debug groups
      debug:
        var: groups

    - name: debug host
      debug:
        var: host

    - name: debug first host
      debug:
        var: hostvars[groups['outputnodes'][0]]

---

