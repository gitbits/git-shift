git-shift
=========

Synopsis
--------

* git-shift - shifts timestamps of commits after the fact

Requirements
------------

- Perl >= 5.8

- Time::Piece >= 1.16

    Only Perl >= 5.14 comes with a reasonably new version.

How to use
----------

        usage: git shift [options] {[<time>][<timediff>][timezone]|<datetime>} <rev-list>...

            -v, --verbose         be verbose
            -n, --dry-run         dry run
            -k                    skip errors

            <time>                substitute this value for the time part(s) of
                                  current commit time(s)
                                  one of:
                                    - "HH:MM:SS"
                                    - "HH:MM" (= "HH:MM:00")

            <timediff>            add this time span to current commit time(s)
                                  in regexp: /^[-+]([0-9]+[wdhms])+$/
                                  e.g.
                                    +1d -12h 30m -1h30m -600s

            <timezone>            in regexp: /^[-+][01][0-9][0-5][0-9]$/

            <datetime>            set this date time as commit time(s)
                                  one of:
                                    - ISO-8601 date time string
                                    - date(1) format in C locale
                                    - number of seconds since the Unix epoch

            <rev-list>            speficy commits to modify which must be on the
                                  current branch; a single commit <committish> or
                                  a range of commits <committish1>..<committish2>
                                  (*both inclusive*)

Author
------

Copyright (c) 2010, 2012, 2013 Akinori MUSHA.

Licensed under the 2-clause BSD license.  See `LICENSE.txt` for
further details.
