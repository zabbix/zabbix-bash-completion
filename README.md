Zabbix Bash Completion
======================

Bash completion for Zabbix commands

To try this out, source the file. For example:

    $ . zabbix_get-completion
    $ zabbix_get -<tab><tab>

For zabbix_get, item key completion is available. Available item keys are hardcoded. If the currently completed key ends
 with an opening square bracket, space is not appended to allow adding positional parameters. For example:

    $ zabbix_get -k system.u<tab><tab>
    system.uname      system.uptime     system.users.num

For zabbix_agentd, item key completion is available. If the currently completed key ends with an opening square bracket,
 space is not appended to allow adding positional parameters. Available item keys are read from the agent binary that is
 specified. For example:

    $ zabbix_agentd -t system.u<tab><tab>
    system.uname      system.uptime     system.users.num

For all daemons, runtime options are completed. For log level changing:
* PID list is completed by the parent PID from the configuration file, if supplied. If not supplied, all processes on
 the system that match the currently completed processes are listed
* Process name completion uses a hardcoded process list. For processes that have a space in the name, backspace-escaped
 space is support. Doublequoting the parameters is not supported. For processes where more than one process is possible,
 trailing space is not added to allow specifying process number (not completed yet). For example:


    $ zabbix_agentd -R log_level_increase=
    active\ checks  collector       listener

For all completions, parameters are supported via space. Specifying them right away or via an equal sign (like -pvalue
 or --param=value) is not supported.

# Requirements

* awk
* ip
* bash-completion

# Troubleshooting

* _get_comp_words_by_ref: command not found

  Package bash-completion must be installed
