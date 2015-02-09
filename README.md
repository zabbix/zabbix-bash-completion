Zabbix Bash Completion
======================

Bash completion for Zabbix commands

To try this out, source the file. For example:

    . zabbix_get-completion
    zabbix_get -<tab><tab>

For zabbix_get, item key completion is available. Available item keys are hardcoded. For example:

    zabbix_get -k system.u<tab><tab>
    system.uname      system.uptime     system.users.num

For zabbix_agentd, item key completion is available.
Available item keys are read from the agent binary that is specified. For example:

    zabbix_agentd -t system.u<tab><tab>
    system.uname      system.uptime     system.users.num
