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

- Red Hat Enterprise Linux 8<sup>1</sup>
- Red Hat Enterprise Linux 9<sup>1</sup>
- RockyLinux 8
- RockyLinux 9
- OracleLinux 8
- OracleLinux 9
- AlmaLinux 8
- AlmaLinux 9
- SUSE Linux Enterprise 15<sup>1</sup>
- openSUSE Leap 15
- Debian 11 (Bullseye)
- Debian 12 (Bookworm)
- Ubuntu 20.04 LTS
- Ubuntu 22.04 LTS
- Ubuntu 24.04 LTS
- Fedora 40
- Fedora 41

Note:
<sup>1</sup> : no automated testing is performed on these platforms

## Role Variables
### defaults/main.yml
<pre><code>

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

### defaults/family-RedHat.yml
<pre><code>
# List of OS packages
auditd_packages:
  - audit

# Lsit of OS services
auditd_services:
  - auditd
</pre></code>

### defaults/family-Suse.yml
<pre><code>
# List of OS packages
auditd_packages:
  - audit

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
