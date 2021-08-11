This playbook outputs the uptime command from your inventory:

TASK [get uptime] ***********************************************************************************************************
changed: [upstairs]
fatal: [gameroom]: UNREACHABLE! => {"changed": false, "msg": "Failed to connect to the host via ssh: ssh: Could not resolve hostname gameroom: Temporary failure in name resolution", "unreachable": true}
changed: [downstairs]
changed: [switch16]
changed: [switch24]
changed: [gateway]

TASK [debug] ****************************************************************************************************************
ok: [gateway] => {
    "out.stdout_lines": [
        " 09:27:50 up 103 days, 20:28,  1 user,  load average: 0.22, 0.22, 0.18"
    ]
}
ok: [switch16] => {
    "out.stdout_lines": [
        " 09:27:50 up 4 days, 11:43,  load average: 1.55, 1.67, 1.67"
    ]
}
ok: [switch24] => {
    "out.stdout_lines": [
        " 09:27:50 up 4 days, 11:39,  load average: 0.55, 0.66, 0.67"
    ]
}
ok: [upstairs] => {
    "out.stdout_lines": [
        " 09:27:50 up  1:09,  load average: 0.04, 0.08, 0.08"
    ]
}
ok: [downstairs] => {
    "out.stdout_lines": [
        " 09:27:50 up 103 days, 20:28,  load average: 0.47, 0.48, 0.51"
    ]
}

PLAY RECAP ******************************************************************************************************************
downstairs                 : ok=2    changed=1    unreachable=0    failed=0    skipped=0    rescued=0    ignored=0   
gameroom                   : ok=0    changed=0    unreachable=1    failed=0    skipped=0    rescued=0    ignored=0   
gateway                    : ok=2    changed=1    unreachable=0    failed=0    skipped=0    rescued=0    ignored=0   
switch16                   : ok=2    changed=1    unreachable=0    failed=0    skipped=0    rescued=0    ignored=0   
switch24                   : ok=2    changed=1    unreachable=0    failed=0    skipped=0    rescued=0    ignored=0   
upstairs                   : ok=2    changed=1    unreachable=0    failed=0    skipped=0    rescued=0    ignored=0  
