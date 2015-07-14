# Command line options for 485solar-get #
485solar-get for 123Solar<br>
based on libyasdi from SMA Solar Technology ag<br>
v1.000 2014-09-04 by roland@breedveld.net<br>
<br>
Config file: /etc/yasdi.ini<br>
<br>
Options:<br>
<blockquote>-h show this help<br>
-d show data<br>
-b show debug information, written to errout<br>
-i show info<br>
-e show events<br>
-c show data with comments<br>
-a show alarms<br>
-s show possible status fields<br>
-r show state of Daemon<br>
-S synchrone detection, default is asynchrone<br>
-D start 485solar-get as daemon<br>
-m monitor loop<br>
-x send exit to daemon<br>
-n0-9 deviceNr, default -n0<br>
<br>
<br>
485solar-get project:  <a href='http://code.google.com/p/sma-get'>http://code.google.com/p/sma-get</a><br>
123Solar     project:  <a href='http://www.123solar.org'>http://www.123solar.org</a><br>
YASDI        software: <a href='http://www.sma.de/en/products/monitoring-systems/yasdi.html'>http://www.sma.de/en/products/monitoring-systems/yasdi.html</a><br>
<br>
<h1>When running 485solar-get as a daemon:</h1>
<br>
The client is communicating to the sever by shared memory, actually an IPC-socket, so both should run as the same user.<br>
<br>
When starting daemon mode always give the highest device_nr in the command, otherwise it only communicates with the first inverter.<br>
example if using 4 SMA inverters: 485solar-get -D -n3<br>
<br>
A client process, such as "485solar-get -d", always looks if a daemon is running, if not, it will communicate directly to the SMA device.<br>
<br>
The daemon will shutdown when communication to one of the inverters is interrupted.<br>
This is because the initialization to all invertes should be done again, after one is comming back online again.<br>