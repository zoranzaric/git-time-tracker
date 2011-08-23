git-time-tracker
================

A script that parses git commit messages and evaluates time commands of the
form `#time 2h 30m` and `#time 2:30`.  It sums up times and prints a summary for
days and tickets.

Requires dulwich, a git library implemented in python.


Example commit message:

    ------>3--->3--->3--->3--->3--->3--->3--->3--->3--->3--->3--->3------
    FOO-23: Fix some random stuff

    There was something broken, doing stuff I don't remember anymore solved the
    problem.
    #time 0:15
    ------3<---3<---3<---3<---3<---3<---3<---3<---3<---3<---3<---3<------

This commit message would result in 15 minutes beeing tracked for the ticket
"FOO-23" for the day the commit was made.

