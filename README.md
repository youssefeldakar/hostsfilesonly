# hostsfilesonly

On a glibc system, in /etc/nsswitch.conf, for the 'hosts' database,
assuming 'files' is the first source listed, comment out everything else
if the argument to the 'hostsfilesonly' script is '1' or undo this if
the argument is '0'.  Besides that, the 'pause' script does the
following: execute the 'hostsfilesonly' script with argument '0', wait
for the amount of time indicated by the argument to the 'pause' script
as defined by 'sleep(1)', execute the 'hostsfilesonly' script with
argument '1', then kill all 'firefox' instances.  Both scripts require
root privilege, which may be configured as in the sample
'hostsfilesonly.sudoers' file..

This is useful as a very rudementary way for turning on/off browsing on
a PC.
