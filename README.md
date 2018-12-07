[![GoKEV](http://GoKEV.com/GoKEV200.png)](http://GoKEV.com/)

<div style="position: absolute; top: 40px; left: 200px;">

# GoKEV-set-stats

This is a role which can be fed variables in the array of `role_data` and pass them between steps in a workflow template of Ansible Tower.  This role has no real function and exists only to show capabilities of passing values between steps.  It might be a great jump-off point for someone looking to include this functionality into existing workflows or roles.

## Here's an example of how you could launch this role:
<pre>
ansible-playbook GoKEV-set-stats.yml
</pre>

## Example Playbook called GoKEV-set-stats.yml:

<pre>
---
- name: Run this role
  hosts: localhost

  vars:
    role_data:
      - var_name: First variable
        var_data: First value
      - var_name: Second variable
        var_data: Second value

  roles:
    - GoKEV.set-stats

</pre>

## With a requirements.yml that looks as such:

<pre>
---
- name: GoKEV.set-stats
  version: master
  src: https://github.com/GoKEV/GoKEV-set-stats.git

</pre>

## Troubleshooting & Improvements

- Not enough testing yet

## Notes

  - Not enough testing yet

## Author

This project was created in 2018 by [Kevin Holmes](http://GoKEV.com/).

