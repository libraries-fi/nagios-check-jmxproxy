nagios-check-jmxproxy
=====================

check_jmxproxy Nagios plugin with rate calculation.

Based on [Oliver Faenger's check_jmxproxy](https://www.monitoringexchange.org/inventory/Check-Plugins/Software/check_jmxproxy) plugin.

Requirements
------------
Depends on [Nagios::Plugin::Differences](https://github.com/pplu/Nagios-Plugin-Differences) for the rate calculation in addition to the regular Perl Nagios plugin dependencies. Needs access to Tomcat's jmxproxy.

Example command
---------------

check_jmxproxy -u "$USER" -p "$PASSWORD" -a "$REALM" -U "$URI*:type%3DGarbageCollector%2Cname%3DPS%20MarkSweep" -r CollectionCount,CollectionTime -e CollectionCount,CollectionTime
