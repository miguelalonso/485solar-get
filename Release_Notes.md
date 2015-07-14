# v0.91 2012-10-14 beta version #
initial test version<br>
<br>
<h1>v0.92 2012-10-15 beta version</h1>
introduced: -b option<br>
this the same as -d (datacollecting) but extended with debug info.<br>
debug info is send to stderr<br>
<br>
Device-scan is now async, with a wait loop after it.<br>
This not optimal yet, but it is much faster<br>
<br>
<h1>v0.93 2012-10-16 beta version</h1>
max exit in detection waitloop, prevents for endless loop<br>
<br>
<h1>v0.94 2012-10-21 beta version</h1>
- mutiple inverters (-n)<br>
- improved debugging options<br>
- date and events printout with comments (-c)<br>
- show possible status fields (-s)<br>
- some minor bigfixes<br>
<br>
<h1>v0.95 2012-10-24 beta version</h1>
- minor bugfixes<br>
- include yasdi libs in compiled version<br>
- install.sh and make_distribution.sh scripts added<br>
<br>
<h1>v0.972 2012-11-28 beta version</h1>
- Pdc in stead of Pac (bug)<br>
- possible to do a synchronous call in stead off async.<br>
- deamon mode, will speed-up requests<br>
- monitor mode added<br>
- much more debugging<br>
- send stop signal to the daemon<br>
- requesting the daemon state<br>
<br>
<h1>v0.980 2012-11-29 beta version</h1>
- deamon request for multiple sma inverters<br>
<br>
<h1>v0.981 2012-12-02 beta version</h1>
- minor bug-fix for 32bit compile<br>
<br>
<h1>v0.982 2013-02-13 beta version</h1>
- not existing inverter in daemon mode will result as 0,<br>
- bugfix for coredump with some SMA models<br>
- detection of A or mA, output will be in Amps<br>
<h1>v1.000 2014-09-04 version</h1>
- New name, going to production version<br>
<br>