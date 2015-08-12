Because Ansible is bad at concurrency and interaction, this role
has to be used several times with different conditions. You can't
pass tags to a role so we use plain variables.

Usage:


roles:
  { role: bdr_check, bdr_check_stage: create_table }
  { role: bdr_check, bdr_check_stage: insert_rows }
  { role: bdr_check, bdr_check_stage: check_rows }
