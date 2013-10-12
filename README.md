Munin-MyBB
==========

A set of Munin plugins for monitoring a MyBB forum.

Note that a regular expression is used to extract the information from the main page so if the forum uses a language other than English or . instead of , as a thousands seperator then it will not function. The plugins will need to be edited to extract the right data.

Installation and Configuration
------------------------------

* Copy the plugins to the munin plugins directory (Generally on Debian/Ubuntu, put them in `/usr/share/munin/plugins/` and symlink to `/etc/munin/plugins`)
* Edit the munin node configuration to add the board_url environment variable, this must be the main forum listing, with stats at the bottom

```
[mybb_*]
env.board_url http://my.forum.com/index.php
```

* Restart the munin node service
