## 485solar-get ##

<b>Important notice: because SMA is a registerd trademark, this project is continued from the sma_get from.</b><br><br>
485solar-get is written in C, it is a datacollector for SMA inverters and is developed to work together with other inverters, communication with different protocols and baudrates, on 1  rs485 interface-bus like Power-one's.<br>
I wrote it for Jean-Marc Louviaux's  <a href='http://www.123solar.org/'>123Solar Project</a><br>
It is also working with Martin Diphoorn's <a href='http://www.websolarlog.com/'>WebSolarLog</a><br>
<br>
485solar-get is communicating directly with the SMA Sunny-Boy devices.<br>
The Sunnyboy's don't have an interface from stock, <br>
you have to buy the add-on-board for your device from SMA, the 485PB-NR or, 485PB-MS-NR.<br>
Tip: sometimes you will find it much cheaper on ebay<br><br>
Example of my configuration, with all used components:<br>
<img src='http://solar.breedveld.net/images/installation/Connections.jpg'>

sma_get is based on the <a href='http://www.sma.de/en/products/monitoring-control/yasdi.html'>libyasdi librarys from SMA</a><br>
<br>
485solar-get is output compatible with Curt Blank's <a href='http://www.curtronics.com/Solar/'>aurora command-line tool</a> so it's easy to implement in applications which are using this tool.<br>
YASDI is written by SMA Solar Technology ag under GNU public licences<br>
<br>
Version 1.000 is the current release now.<br>
<br>
Check the wiki pages for instructions and tips.<br>
<br>
For questions tips and ideas, please post it on the <a href='https://groups.google.com/forum/?fromgroups#!forum/485solar-get'>485solar-get Google forum</a><br>
enjoy!<br>
Roland<br>
<br>
You'll see both an Aurora and a Sunny-boy running on <a href='http://solar.breedveld.net'>my solar site</a><br><br>
Download 485solar-get on: <a href='https://sourceforge.net/projects/solarget/files'>sourceforge</a><br>