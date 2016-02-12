=========================================================
Tahoe-LAFS Weekly News, issue number 57, February 12 2015
=========================================================

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
.. _look: https://tahoe-lafs.org/~marlowe/TWN57.html

Nuts and Bolts
==============

Nuts and Bolts is held regularly at 1700Z on Tuesdays and Fridays. You
can attend the Hangout at the `following Hangout URL`_.

Friday, 02/05/16
----------------

Attendees: Brian Warner, Daira Hopwood, Patrick R McDonald

Disclaimer: Lost my notes, so this is from memory

Brian and Daira worked on closing tickets for 1.10.3 and resolving the last of
the buildbot errors.

Tuesday, 02/09/16
-----------------

Attendees: Brian Warner, Daira Hopwood, Chris Wood, meejah, Patrick R McDonald,
Zooko Wilcox

Currently Google Hangouts is not providing the optimal functionality we need
across various operating systems for Nuts and Bolts.  We hope our readers can
provide us with some solid alternatives. If you know some, please reply on the
mailing list.

The Current tahoe trunk doesn't always build on OS-X or Linux (`#2728`_). The
workaround is to build in a virtualenv, pre-install some packages, but then
zetuptoolz conflicts with other requirements.  We're considering performing the
zetuptoolz-ectomy (`#1582`_) *before* the 1.10.3 release, rather than immediately after
that would make "pip install ." (well, with --editable) be the recommended way
to hack on tahoe from source.  This will need some docs changes, probably some
new CI tests.  It might be a big enough change to justify calling it 1.11
instead of 1.10.3. In addition, using 'pip install' and virtualenvs would
probably close a lot of our packaging tickets.

Zooko and Warner are figuring out how to get a windows buildslave running on
EC2.

.. _`following Hangout URL`:
  https://plus.google.com/hangouts/_/calendar/YTEwYW1vbGxxMG10cmMwbGU0ZXM3N2IxODRAZ3JvdXAuY2FsZW5kYXIuZ29vZ2xlLmNvbQ.unccip97qin95ihpk6l3nknumo?authuser=0

.. _`#2728`: https://tahoe-lafs.org/trac/tahoe-lafs/ticket/2728
.. _`#1582`: https://tahoe-lafs.org/trac/tahoe-lafs/ticket/1582

Mailing List
============

Brian `upgraded tahoe-lafs.org to the latest Ubuntu LTS`_.

Based on a previous Nuts and Bolts discussion, Stuart Card introduced
`membranes`_. Membranes attempts to resolve the issue of cap revocation and
controlling further delegation of a capability.

.. _`upgraded tahoe-lafs.org to the latest Ubuntu LTS`:
  https://tahoe-lafs.org/pipermail/tahoe-dev/2016-February/009674.html
.. _`membranes`:
  https://tahoe-lafs.org/pipermail/tahoe-dev/2016-February/009676.html

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

