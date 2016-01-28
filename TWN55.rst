========================================================
Tahoe-LAFS Weekly News, issue number 55, January 27 2015
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
.. _look: https://tahoe-lafs.org/~marlowe/TWN55.html

Announcements and News
======================

New Foolscap
------------

Brian Warner released `two`_ `new versions`_ of Foolscap.  The details
of the release can be read below.

"This release is compatible with Twisted-15.3.0 through 15.5.0. A change
in 15.3.0 triggered a bug in Foolscap which produced a somewhat-infinite
series of log messages when run under `twistd`. This release fixes that
bug, and slightly changes the semantics of calling `log.msg()` with
additional parameters. (`#244`_)

Foolscap no longer claims compatibility with python-2.6.x .
Twisted-15.5.0 was the last release to offer 2.6 support, and subsequent
releases actively throw errors when run against 2.6, so we've turned off
Foolscap's automated testing for 2.6. It may remain compatible by
accident for a while. (`#245`_)

.. _`two`:
  https://tahoe-lafs.org/pipermail/tahoe-dev/2016-January/009666.html
.. _`new versions`:
  https://tahoe-lafs.org/pipermail/tahoe-dev/2016-January/009662.html
.. _`#244`: http://foolscap.lothar.com/trac/ticket/244
.. _`#245`: http://foolscap.lothar.com/trac/ticket/245

Changes to TWN
==============

TWN on Github
-------------

If you are interested in TWN in an easy to update format, we will be
hosting `TWN on Github`_.  Now you can update your copy of the news with
a git pull.

TWN Attends Nuts and Bolts
--------------------------

I finally made good on my promise and attended Nuts and Bolts on both
Tuesday (01/26/16) and Friday (01/22/16).  I had a fantastic time with
both of these meetings.  I really appreciate the developers at
Tahoe-LAFS providing such an open forum to the development process.

Nuts and Bolts
==============

Nuts and Bolts is held regularly at 1700Z on Tuesdays and Fridays. You
can attend the Hangout at the `following Hangout URL`_.

Friday, 01/22/16
----------------

Attendees: Daira Hopwood, David Stanton, Zooko Wilcox

Much discussion was had on the way forward.  We have a potentially
good idea to simplify Magic Folders conflict-detection and separate
conflict detection more from history-preservation and from networking
(i.e. a reader talking interactively to all of the different writers).
David absolutely made my day with my favorite example, me taking years
away to sail around New Zealand.  Note to the reader, you can bribe the
author with the ability to sail the world with his better half. Daira
will be posting notes on the result of the design discussion and I will
update this newsletter when I receive them.

Tuesday, 01/26/16
-----------------

Attendees: Brian Warner, Chris Wood, Daira Hopwood, David Stanton, Leif
Ryge, Mike Warren, Patrick R McDonald, and Zooko Wilcox

Daira graciously volunteered to be the release manager for 1.10.3.
Brian will be the assistant release manager.  Daira will review the
"introless-multiintro" branch (`#68`_) to decide whether it will be landed
in 1.10.3 or 1.11.0.  Brian will resolve the Foolscap issues for 1.10.3.
Daira will have all tickets for 1.10.3 triaged by this Friday (1/29/16).

A large issue with being able to do timely releases is the lack of
Windows users, developers, and build machines. If you can donate
resources to help with this issue, please let us know.

Leif is hacking on the `branch`_ which will replace all the
build/setup/dependency stuff (`#1582`_).

Chris Wood spoke about `gridsync`_, his project. Chris is working with
Gus Andrews of `SimplySecure`_ to create a desktop GUI client for Linux,
OS X, and Windows.  Gus provided an `excellent review of gridsync`_.
Gridsync creates a single-file executable on OS X and Windows, which
will not depend upon locally-install Python or other libraries.

.. _`following Hangout URL`:
  https://plus.google.com/hangouts/_/calendar/YTEwYW1vbGxxMG10cmMwbGU0ZXM3N2IxODRAZ3JvdXAuY2FsZW5kYXIuZ29vZ2xlLmNvbQ.unccip97qin95ihpk6l3nknumo?authuser=0
.. _`branch`: https://github.com/tahoe-lafs/tahoe-lafs/pull/216
.. _`#68`:
  https://tahoe-lafs.org/trac/tahoe-lafs/ticket/68
.. _`#1582`:
  https://tahoe-lafs.org/trac/tahoe-lafs/ticket/1582
.. _`gridsync`:
  https://github.com/gridsync/gridsync
.. _`SimplySecure`: https://simplysecure.org
.. _`excellent review of gridsync`:
  https://medium.com/@gusandrews/expert-review-gridsync-a-secure-cloud-app-built-on-tahoe-lafs-c290252b15bb#.70ex5ycko)

Mailing List
============

Freelab initiative had `questions concerning Windows and Debian ARM
clients`_.

.丶Ever experienced `an issue with zfec`_. Zooko and Ramakrishnan
Muthukrishnan were able to `resolve the issue`_.

David Stanton requested Brian Warner's assistance with the `Magic
Folder roadmap`_.

.. _`questions concerning Windows and Debian ARM clients`:
  https://tahoe-lafs.org/pipermail/tahoe-dev/2016-January/009656.html
.. _`an issue with zfec`:
  https://tahoe-lafs.org/pipermail/tahoe-dev/2016-January/009663.html
.. _`resolve the issue`:
  https://tahoe-lafs.org/pipermail/tahoe-dev/2016-January/009668.html
.. _`Magic Folder roadmap`:
  https://tahoe-lafs.org/pipermail/tahoe-dev/2016-January/009664.html

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

