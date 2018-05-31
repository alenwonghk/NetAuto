Collect facts from each device and a report
device name
serial number
device software version
uptime
memory info
interfaces
ip addresses


facts['ansible_sysname']
facts['ansible_net_serialnum']  <- no serial number
facts['ansible_net_version']
facts['ansible_sysuptime']
facts['ansible_net_memfree_mb']
facts['ansible_net_memtotal_mb']
facts['ansible_all_ipv4_addresses']



{{facts.ansible_sysname}}
{{facts.ansible_net_serialnum}}
{{facts.ansible_net_version}}
{{facts.ansible_sysuptime}}
{{facts.ansible_net_memfree_mb}}
{{facts.ansible_net_memtotal_mb}}
{{facts.ansible_all_ipv4_addresses}}