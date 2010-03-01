git-shift
=========

Synopsis
--------

* git-shift - shifts dates of specified commits by a specified amount of time

How to set up
-------------

Assuming you are installing these scripts in ~/bin, run the following
commands:

	install -m 755 git-shift ~/bin/
	git config --global alias.shift '!$HOME/bin/git-shift "$@"'

How to use
----------

        git shift <offset> <commit_id> [<commit_id> ...]

        Time offset format can be described in this extended regexp:

            /^[-+]?(([0-9]+[wdhm])+|[0-9]+)$/

        Some example values:

            +1d -12h 30m -1h30m 60 (omission of unit implies seconds)
    
        Each commit ID is a 40-byte hexadecimal commit object name, or
        a partial prefix matching a single commit.

License
-------

	Copyright (c) 2010 Akinori MUSHA
	
	All rights reserved.
	
	Redistribution and use in source and binary forms, with or without
	modification, are permitted provided that the following conditions
	are met:
	1. Redistributions of source code must retain the above copyright
	   notice, this list of conditions and the following disclaimer.
	2. Redistributions in binary form must reproduce the above copyright
	   notice, this list of conditions and the following disclaimer in the
	   documentation and/or other materials provided with the distribution.
	
	THIS SOFTWARE IS PROVIDED BY THE AUTHOR AND CONTRIBUTORS ``AS IS'' AND
	ANY EXPRESS OR IMPLIED WARRANTIES, INCLUDING, BUT NOT LIMITED TO, THE
	IMPLIED WARRANTIES OF MERCHANTABILITY AND FITNESS FOR A PARTICULAR PURPOSE
	ARE DISCLAIMED.  IN NO EVENT SHALL THE AUTHOR OR CONTRIBUTORS BE LIABLE
	FOR ANY DIRECT, INDIRECT, INCIDENTAL, SPECIAL, EXEMPLARY, OR CONSEQUENTIAL
	DAMAGES (INCLUDING, BUT NOT LIMITED TO, PROCUREMENT OF SUBSTITUTE GOODS
	OR SERVICES; LOSS OF USE, DATA, OR PROFITS; OR BUSINESS INTERRUPTION)
	HOWEVER CAUSED AND ON ANY THEORY OF LIABILITY, WHETHER IN CONTRACT, STRICT
	LIABILITY, OR TORT (INCLUDING NEGLIGENCE OR OTHERWISE) ARISING IN ANY WAY
	OUT OF THE USE OF THIS SOFTWARE, EVEN IF ADVISED OF THE POSSIBILITY OF
	SUCH DAMAGE.
