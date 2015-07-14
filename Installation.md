# Install 485solar-get #
needed packages: libaio<br>

<h2>for Ubuntu 12.04LTS</h2>
<h3>also tested on Ubuntu 10.04LTS</h3>
<code>download the latest compiled 485solar-get &lt;version&gt;_x86_64_Ubuntu_12_04.tgz from this site,</code><br>
<code>(or for 32bit systems 485solar-get_&lt;version&gt;_i386_Ubuntu_12_04.tgz)</code><br>
place is somewhere like /tmp<br>
extract it:<br>
<blockquote><code>tar xzvf 485solar-get_&lt;version&gt;_x86_64_Ubuntu_12_04.tgz</code><br>
run the install script:<br>
sudo ./install.sh<br></blockquote>

<h2>For other Linux distributions:</h2>
<h3>compiling and installing YASDI</h3>
needed packages: gcc cmake libaio<br>
Download YASDI from the SMA site:<br>
<code>http://www.sma.de/en/products/monitoring-systems/yasdi.html</code><br>
<code>extract it to /usr/local/src/libyasdi_1_8_1</code><br>
<blockquote><code>cd /usr/local/src/libyasdi_1_8_1/</code><br>
<code>cd projects/generic-cmake</code><br>
<code>mkdir build-gcc</code><br>
<code>cd build-gcc</code><br>
<code>cmake ..</code><br>
<code>make</code><br>
<code>sudo make install</code><br>
<code>export LD_LIBRARY_PATH=$LD_LIBRARY_PATH:/usr/local/lib</code><br>
<code>sudo ldconfig /usr/local/lib</code><br>
<br>
test it:<br>
<code>yasdishell /etc/yasdi.ini </code><br>
<br></blockquote>

<h3>compiling and installing 485solar-get</h3>
<code>download the latest 485solar-get_&lt;version&gt;_sources.tgz source from this site</code><br>
extract it:<br>
<blockquote><code>cd /usr/local/src/libyasdi_1_8_1/</code><br>
<code>tar xzvf &lt;location&gt;/485solar-get_&lt;version&gt;_sources.tgz</code><br>
<code>cd /usr/local/src/libyasdi_1_8_1/sma_485solar-get_&lt;version&gt;</code><br>
<code>sudo ./make.sh</code></blockquote>


<h2>example for /etc/yasdi.ini</h2>
<blockquote><code>[DriverModules]</code><br>
<code> Driver0=yasdi_drv_serial</code><br>
<code>[COM1]</code><br>
<code> Device=/dev/ttyUSB0</code><br>
<code> Media=RS485</code><br>
<code> Baudrate=1200</code><br>
<code> Protocol=SMANet</code><br>
<code>[Misc]</code><br>
<code>  DebugOutput=/dev/stderr</code><br></blockquote>


<h2>compiling, installing and generating your own distribution</h2>
<code>download the latest 485solar-get_&lt;version&gt;_sources.tgz source from this site</code><br>
extract it:<br>
<blockquote><code>cd /usr/local/src/libyasdi_1_8_1/</code><br>
<code>tar xzvf &lt;location&gt;/485solar-get_&lt;version&gt;_sources.tgz</code><br>
<code>cd /usr/local/src/libyasdi_1_8_1/485solar-get_&lt;version&gt;</code><br>
<code>change PACKAGE_PAD in make_distribution.sh to your own choice</code><br>
<code>sudo ./make_distribution.sh</code>