# general #
When encountering issues, first every should be fine without using the Daemon mode.<br>
stop the daemon with<br>
485solar-get -x<br>
be shure there are no alter commands running, so stop all software which is using the same interface, like 123solar, etc.<br>

<h1>bind address in use</h1>
If you change the user which 485solar-get (and Daemon) runs, you have to remove the socket file:<br>
rm -f /var/tmp/485solar-get_socket<br>

<h1>debug 485solar-get</h1>
use the -b option to show debug output:<br>
485solar-get -s -b <br>
or:<br>
485solar-get -b -d -i -e -a -s <br>
<br>
try synchronous detection, by adding the -S option<br>

<h1>first test Yasdi itself, while 485solar-get is using its library's</h1>
yasdishell /etc/yasdi.ini<br>
b1<br>
when device is detected:<br>
z<br>
look at the outputs of:<br>
d<br>
a1<br>
p1<br>
t1 (probably empty)<br>

<h3>When the rs485 interface won't respond, try to zero it:</h3>
<blockquote>setserial -z  /dev/ttyUSB0<br>
Get state of rs485 device:<br>
setserial -G  /dev/ttyUSB0<br>
this wil give something like:<br>
/dev/ttyUSB0 uart unknown port 0x0000 irq 0 baud_base 24000000 spd_normal low_latency<br>
Check baudrate:<br>
stty -F /dev/ttyUSB0<br>
Set baudrate:<br>
stty -F /dev/ttyUSB0 1200<br></blockquote>

<h3>cannot open shared object</h3>
if you get this message after installing the binary version:<br>
485solar-get: error while loading shared libraries: libyasdimaster.so.1: cannot open shared object file: No such file or directory<br>
<br>
This means /usr/local/lib is not in the library path.<br>
there are 2 solutions:<br><br>
setting the path before running, only for this session:<br>
<blockquote>export LD_LIBRARY_PATH=$LD_LIBRARY_PATH:/usr/local/lib<br>
Make it permanent:<br>
sudo ldconfig /usr/local/lib<br></blockquote>

<h3>Debugging and tracing</h3>
If you can't get enough data from the -b (debug) option, you can use strace:<br>
<blockquote>strace -f -o 485solar-get.strace 485solar-get -d -b<br>
All trace info will be written to 485solar-get.strace<br>
For monitoring the serial data:<br>
strace -s9999 -o 485solar-get.strace -eread,write,ioctl  485solar-get -d -b<br>