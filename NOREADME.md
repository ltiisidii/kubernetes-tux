ansible-playbook selinuxmode.yml

```
PLAY [Ansible Playbook for disabling SELinux and Reboot .] **********************************************************************************************************************************************************************************

TASK [Gathering Facts] **********************************************************************************************************************************************************************************************************************
ok: [192.168.254.50]
ok: [192.168.254.54]
ok: [192.168.254.53]
ok: [192.168.254.51]
ok: [192.168.254.52]

TASK [Disabling SELinux] ********************************************************************************************************************************************************************************************************************
[WARNING]: SELinux state temporarily changed from 'enforcing' to 'permissive'. State change will take effect next reboot.
changed: [192.168.254.51]
changed: [192.168.254.52]
changed: [192.168.254.50]
changed: [192.168.254.54]
changed: [192.168.254.53]

TASK [Print the changes in Configurtion file] ***********************************************************************************************************************************************************************************************
changed: [192.168.254.53]
changed: [192.168.254.50]
changed: [192.168.254.51]
changed: [192.168.254.54]
changed: [192.168.254.52]

TASK [debug] ********************************************************************************************************************************************************************************************************************************
ok: [192.168.254.52] => {
    "sevalue.stdout_lines": [
        "# SELINUX= can take one of these three values:",
        "SELINUX=disabled",
        "# SELINUXTYPE= can take one of these three values:",
        "SELINUXTYPE=targeted"
    ]
}
ok: [192.168.254.54] => {
    "sevalue.stdout_lines": [
        "# SELINUX= can take one of these three values:",
        "SELINUX=disabled",
        "# SELINUXTYPE= can take one of these three values:",
        "SELINUXTYPE=targeted"
    ]
}
ok: [192.168.254.50] => {
    "sevalue.stdout_lines": [
        "# SELINUX= can take one of these three values:",
        "SELINUX=disabled",
        "# SELINUXTYPE= can take one of these three values:",
        "SELINUXTYPE=targeted"
    ]
}
ok: [192.168.254.51] => {
    "sevalue.stdout_lines": [
        "# SELINUX= can take one of these three values:",
        "SELINUX=disabled",
        "# SELINUXTYPE= can take one of these three values:",
        "SELINUXTYPE=targeted"
    ]
}
ok: [192.168.254.53] => {
    "sevalue.stdout_lines": [
        "# SELINUX= can take one of these three values:",
        "SELINUX=disabled",
        "# SELINUXTYPE= can take one of these three values:",
        "SELINUXTYPE=targeted"
    ]
}

TASK [Wait for 5 Second and Reboot] *********************************************************************************************************************************************************************************************************
changed: [192.168.254.52]
changed: [192.168.254.51]
changed: [192.168.254.53]
changed: [192.168.254.50]
changed: [192.168.254.54]

PLAY RECAP **********************************************************************************************************************************************************************************************************************************
192.168.254.50             : ok=5    changed=3    unreachable=0    failed=0    skipped=0    rescued=0    ignored=0
192.168.254.51             : ok=5    changed=3    unreachable=0    failed=0    skipped=0    rescued=0    ignored=0
192.168.254.52             : ok=5    changed=3    unreachable=0    failed=0    skipped=0    rescued=0    ignored=0
192.168.254.53             : ok=5    changed=3    unreachable=0    failed=0    skipped=0    rescued=0    ignored=0
192.168.254.54             : ok=5    changed=3    unreachable=0    failed=0    skipped=0    rescued=0    ignored=0
```

