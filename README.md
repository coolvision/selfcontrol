This is a vesion of SelfControl wich checks time independently of the system time (time_check branch).

Each 10 seconds time is queried with http request to http://google.com/ (using code from https://github.com/freak4pc/NSDate-ServerDate)

It solves the issue of unblocking by system time change (https://github.com/SelfControlApp/selfcontrol/issues/28)

Use at your own risk, it might cause permanent blocking!

I'm currently using (testing) it.
There are a few issues:
- if there is no internet access, blocking will not start (no warnings shown)
- and will not stop (but will stop if internet acces appears and blocking time has expired)
- when the system time is ahead of checked time, negative time value can be displayed (I think it's good because it prompts you to stop meddling with the time settings :)

-----

[SelfControl](http://selfcontrolapp.com)
===========

ABOUT
-----
Is email a distraction? SelfControl is an OS X application which blocks access to mail servers and websites for a predetermined period of time. It can not be undone by the app or by a restart--you must wait for the timer to run out.

CREDITS
-------
Developed by [Charlie Stigler](http://charliestigler.com), [Steve Lambert](http://visitsteve.com), and you?

Translations thanks to: Lukas Bestle, Paul Ishii, Cynthia Lawson, Heather Rasley, and Tian Zheng.

LICENSE
-------
SelfControl is Free Software under the GPL. See source code for more details.

VERSION HISTORY
---------------

* 1.4 - Added translations in Swedish, Spanish, German, and Japanese, fixed crash on Leopard, other minor bug fixes
* 1.3 - Automatic checkup safety system, UI refresh, user-settable block duration/intervals, bug fixes
* 1.2.2 - Automatic host file backups for safety, various stability improvements
* 1.2.1 - Auto-whitelisting of local networks, fix bug causing persistent crash on 10.4
* 1.2 - SelfControl Configuration files, live blocklist additions, whitelist blocking, automatic cache cleaning, IP range blocking, dock badging, bug fixes
* 1.1 - 10.4 Tiger compatibility, automatic updates, port-wide block capability, bug fixes
* 1.0 - works on OS X Leopard.
