This role defines a base PostgreSQL server - currently compiled from git.

To stop "make clean" from being performed, add postgres_make_clean to your
`--skip-tags`.

Checks out, builds and installs postgres_server of 9.4, 9.5 and 9.6 versions

tags:

* postgres_make_clean: "make clean" before building
* postgres_install: installation phase, getting binaries in place
