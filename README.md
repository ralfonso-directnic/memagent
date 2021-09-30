# Memagent
Automatically exported from code.google.com/p/memagent
从https://code.google.com/p/memagent/ 导过来的。memcached的agent。提高mc的可用性


simple but useful proxy program for memcached

magent is a simple but useful proxy program for memcached servers.

It features:
keeps connections to memcached servers
supports following memcached commands
get gets
delete
incr decr
add set replace prepend append
cas
event-driven by using libevent library
supports ketama algorithm
backup servers farm
unix domain socket
Usage:
-h this message -u uid -g gid -p port, default is 11211. (0 to disable tcp support) -s ip:port, set memcached server ip and port -b ip:port, set backup memcached server ip and port -l ip, local bind ip address, default is 0.0.0.0 -n number, set max connections, default is 4096 -D do not go to background -k use ketama key allocation algorithm -f file, unix socket path to listen on. default is off -i number, max keep alive connections for one memcached server, default is 20 -v verbose

Changelog:
2010/4/14: memcached agent 0.6 1. add connection keepalive handler 1. bug fix, more robust, more debug messages

Examples:
magent -s 10.1.2.1 -s 10.1.2.2:11211 -b 10.1.2.3:14000 -v
