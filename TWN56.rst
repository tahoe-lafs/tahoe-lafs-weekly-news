========================================================
Tahoe-LAFS Weekly News, issue number 56, February 4 2015
========================================================

Welcome to the Tahoe-LAFS Weekly News (TWN).  Tahoe-LAFS_ is a secure,
distributed storage system. `View TWN on the web`_ *or* `subscribe to
TWN`_.
If you would like to view the "new and improved" TWN, complete with pictures;
please take a `look`_.

.. _Tahoe-LAFS: https://tahoe-lafs.org
.. _View TWN on the web:
  https://tahoe-lafs.org/trac/tahoe-lafs/wiki/TahoeLAFSWeeklyNews
.. _subscribe to TWN:
  https://tahoe-lafs.org/cgi-bin/mailman/listinfo/tahoe-lafs-weekly-news
.. _look: https://tahoe-lafs.org/~marlowe/TWN56.html

Nuts and Bolts
==============

Nuts and Bolts is held regularly at 1700Z on Tuesdays and Fridays. You
can attend the Hangout at the `following Hangout URL`_.

Friday, 01/29/16
----------------

Attendees: Brian Warner, David Stainton, Leif Ryge, meejah, Patrick R McDonald,
Zooko Wilcox

There was a large amount of discussion centered tradeoffs between
reliability/availability vs the ability to revoke or unshare something. Leif and
David brought up the excellent point that once you provide another person which
a cap, you currently do not have a reliable method to revoke access to the data
associated with that cap. This may be one of the reasons for the slowness in
Tahoe-LAFS' adoption. Users have trouble understanding that access controls in
Tahoe-LAFS are not handled by a third party to allow for easy revocation.

Tuesday, 02/02/16
-----------------

Attendees: Brian Warner, Chris Wood, Daira Hopwood, David Stainton, Leif Ryge,
meejah, Patrick R McDonald, Zooko Wilcox

Account creation on Tahoe Trac is resolved thanks to Brian. Hopefully it will
remain resistant to spammers for awhile.

Zooko will merge github.com/zooko/pycryptopp  master and
github.com/tahoe-lafs/pycryptopp master and version and tag it as 0.7.1

A large amount of time was spent on ticket triage. Below are the results of the
triage.

* `#2534`_ - The problem will be resolved by either an upgrade of Foolscap or an
  upgrade to Tahoe-LAFS 1.10.3. Brian will the latest Foolscap a dependency
  (`#2722`_) of Tahoe-LAFS.
* `#1949`_ and `#2137`_ appear to have the same underlying cause
* `#2543`_ -  To be resolved for 1.10.3
* `#2709`_ - Moved out of the release
* `#517`_, `#1007`_ and `#1010`_ - Are moved to the 1.11.0
* `#1349`_ - Brian and Leif will work to resolve this
* `#2045`_ - Adding 1.11

After the meeting, Daira fixed `#2724`_, `#1949`_, `#2137`_, and `#2543`_.

The buildbot is mostly red right now. The failures (and steps-to-resolve) are:
    
* "Daira Win7-64": failing tests because of windows lacking time.tzset, Daira is
  investigating
* "FreeStorm CentOS6": using py2.6 (no longer supported), Brian will remove
* "MM netbsd5": using py2.6, Brian will remove
* "Marcus Cygwin WinXP": using py2.6, Brian will remove
* "Ubuntu trusty 14.04": cffi version mismatch, Daira might spin up VM to
  reproduce
* "clean", "memcheck-32": same (runs on same vm)
* "Warner OS-X 10.11": current pycryptopp won't compile, Zooko will make new
  release of pycryptopp to fix
* "memcheck-64": build fails, looking for obsolete distribution "twisted-web",
  Brian will investigate
  * known bug in recent Debian packaging:
  https://bugs.debian.org/cgi-bin/bugreport.cgi?bug=811392

After the meeting, the following updates were made:

* py2.6 builders removed
* cffi mismatch resolved (added a virtualenv to isolate tahoe tests from host
  packages)
* memcheck-64 Debian bug fixed, waiting for new package to appear on mirrors,
  should be installed on 02/04/2016

.. _`following Hangout URL`:
  https://plus.google.com/hangouts/_/calendar/YTEwYW1vbGxxMG10cmMwbGU0ZXM3N2IxODRAZ3JvdXAuY2FsZW5kYXIuZ29vZ2xlLmNvbQ.unccip97qin95ihpk6l3nknumo?authuser=0
.. _`#2534`:
  https://tahoe-lafs.org/trac/tahoe-lafs/ticket/2534
.. _`#2722`:
  https://tahoe-lafs.org/trac/tahoe-lafs/ticket/2722
.. _`#1949`:
  https://tahoe-lafs.org/trac/tahoe-lafs/ticket/1949
.. _`#2137`:
  https://tahoe-lafs.org/trac/tahoe-lafs/ticket/2137
.. _`#2543`:
  https://tahoe-lafs.org/trac/tahoe-lafs/ticket/2543
.. _`#2709`:
  https://tahoe-lafs.org/trac/tahoe-lafs/ticket/2709
.. _`#517`:
  https://tahoe-lafs.org/trac/tahoe-lafs/ticket/517
.. _`#1007`:
  https://tahoe-lafs.org/trac/tahoe-lafs/ticket/1007
.. _`#1010`:
  https://tahoe-lafs.org/trac/tahoe-lafs/ticket/1010
.. _`#1349`:
  https://tahoe-lafs.org/trac/tahoe-lafs/ticket/1349
.. _`#2045`:
  https://tahoe-lafs.org/trac/tahoe-lafs/ticket/2045
.. _`#2724`:
  https://tahoe-lafs.org/trac/tahoe-lafs/ticket/2724

*The Tahoe-LAFS Weekly News is published once a week by The Tahoe-LAFS*

The Tahoe-LAFS Weekly News is published once a week by The Tahoe-LAFS
Software
Foundation, President and Treasurer: Peter Secor |peter|. Scribes: Patrick
"marlowe" McDonald |marlowe|, Zooko Wilcox-O'Hearn , Editor Emeritus:
|zooko|.
Send your news stories to `marlowe@antagonism.org`_ - submission deadline:
Monday night.

.. _`marlowe@antagonism.org`: mailto:marlowe at antagonism.org
.. |peter| image:: psecor.jpg
   :height: 35
   :alt: peter
   :target: http://tahoe-lafs.org/trac/tahoe-lafs/wiki/AboutUs
.. |marlowe| image:: marlowe-x75-bw.jpg
   :height: 35
   :alt: marlowe
   :target: http://tahoe-lafs.org/trac/tahoe-lafs/wiki/AboutUs
.. |zooko| image:: zooko.png
   :height: 35
   :alt: zooko
   :target: http://tahoe-lafs.org/trac/tahoe-lafs/wiki/AboutUs

