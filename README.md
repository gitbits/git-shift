git-shift
=========

Synopsis
--------

* git-shift - shifts dates of specified commits by a specified amount of time

How to set up
-------------

Just place this script in one of the directories in your `PATH`, and
you are done.

How to use
----------

        git shift <offset> <commit_id> [<commit_id> ...]

        Time offset format can be described in this extended regexp:

            /^[-+]?(([0-9]+[wdhm])+|[0-9]+)$/

        Some example values:

            +1d -12h 30m -1h30m 60 (omission of unit implies seconds)

        Each commit ID is a 40-byte hexadecimal commit object name, or
        a partial prefix matching a single commit.

Author
------

Copyright (c) 2010, 2012 Akinori MUSHA.

Licensed under the 2-clause BSD license.  See `LICENSE.txt` for
further details.
