======================
Zabbix Bash Completion
======================

Bash completion for Zabbix commands

To try this out, source the file. For example:

    . zabbix_get-completion
    zabbix_get -<tab><tab>
    
Also key completion for standard agent items is available. For example:

    zabbix_get -k system.<tab><tab>
    system.boottime       system.hw.chassis[    system.swap.out[
    system.cpu.discovery  system.hw.cpu[        system.swap.size[
    system.cpu.intr       system.hw.devices[    system.sw.arch
    system.cpu.load[      system.hw.macaddr[    system.sw.os[
    system.cpu.num[       system.localtime[     system.sw.packages[
    system.cpu.switches   system.run[           system.uname
    system.cpu.util[      system.stat[          system.uptime
    system.hostname[      system.swap.in[       system.users.num
