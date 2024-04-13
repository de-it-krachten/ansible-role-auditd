[![CI](https://github.com/de-it-krachten/ansible-role-auditd/workflows/CI/badge.svg?event=push)](https://github.com/de-it-krachten/ansible-role-auditd/actions?query=workflow%3ACI)


# ansible-role-auditd

Installs/configures auditd



## Dependencies

#### Roles
None

#### Collections
None

## Platforms

Supported platforms

- Ubuntu 20.04 LTS
- Ubuntu 22.04 LTS

Note:
<sup>1</sup> : no automated testing is performed on these platforms

## Role Variables
### defaults/main.yml
<pre><code>

</pre></code>

### defaults/family-RedHat.yml
<pre><code>
# List of OS packages
auditd_packages:
  - audit

# Lsit of OS services
auditd_services:
  - auditd
</pre></code>

### defaults/family-Debian.yml
<pre><code>
# List of OS packages
auditd_packages:
  - auditd

# Lsit of OS services
auditd_services:
  - auditd
</pre></code>




## Example Playbook
### molecule/default/converge.yml
<pre><code>
- name: sample playbook for role 'auditd'
  hosts: all
  become: 'yes'
  tasks:
    - name: Include role 'auditd'
      ansible.builtin.include_role:
        name: auditd
</pre></code>
