======================
Zabbix Bash Completion
======================

Bash completion for Zabbix commands

To try this out, source the file. For example:

    . zabbix_get-completion
    zabbix_get -<tab><tab>

Also key completion for standard agent items is available. For example:

    zabbix_get -k system.u<tab><tab>
    system.uname      system.uptime     system.users.num
