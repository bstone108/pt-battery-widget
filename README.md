# pt-battery-widget
development for an lxde battery widget

for now, the the widget will be targeted towards lxde but latter we can expand to other window managers

work just now starting,  anyone familure with building widgets please contribute!

the original battery monitor is the one built into lxde, working on modifying source for the pitop to use as a dropin replacement.

things we know.
the battery communicates over ic2 which in most distrobutions requires root. pi-top has a script for pulling battery info via commands
so at most we just need this plugin to parse data from the script,  at best we could use ic2 to get info ourselves.

calling /usr/bin/pt-battery output when discharging
State: Discharging
Remaining time: 656 mins
Capacity: 100%

when charging/charged
State: Charging
Remaining time: Error

arguments supported;
all [asumed if no arguments provided] returns state time and capacity
state returns charging state
time is estimated time remaining [seems to return error if fully charged]
capacity is how charged it is in %.
