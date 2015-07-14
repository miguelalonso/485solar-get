#output examples for 485solar-get

# 485solar-get -d (request data) #
20130712-15:32:55 172.000000  3.107000  534.404000  0.000000  0.000000  0.000000  234.400003  2.083000  488.000000  49.989999  91.364437  0.000000  0.000000  0.000000  0.000000  0.000000  0.000000  0.000000  889.486042  0.000000  OK

# 485solar-get -d -c (request data in column format) #
Date            20130712-15:39:04<br>
Upv-Ist         V      172.000000 <br>
Ipv             A      3.494000 <br>
Pdc                    600.968000 <br>
dummy                  0.000000 <br>
dummy                  0.000000 <br>
dummy                  0.000000 <br>
Uac             V      234.000003 <br>
Iac-Ist         A      2.346000 <br>
Pac             W      549.000000 <br>
Fac             Hz     49.989999 <br>
Effcy                  91.346629 <br>
dummy                  0.000000 <br>
dummy                  0.000000 <br>
dummy                  0.000000 <br>
dummy                  0.000000 <br>
dummy                  0.000000 <br>
dummy                  0.000000 <br>
dummy                  0.000000 <br>
E-Total         kWh    889.537042 <br>
dummy                  0.000000 <br>
State           OK<br>
<br>
<h1>485solar-get -e (events)</h1>
169.000000  169.000000  0.000000  0.000000  169.000000  0.000000  0.000000  3.000000  233.900003  233.900003  233.900003  49.989999  1200.000000  0.000000  0.000000  0.000000  0.000000  0.000000  0.000000  0.000000  0.000000  0.000000  0.000000  0.000000  0.000000  466.000000  0.000000  0.000000  0.000000  0.000000  0.000000  OK<br>
<br>
<h1>485solar-get -c -e (events in column format)</h1>
Upv-Ist         172.000000<br>
Upv-Ist         172.000000<br>
dummy           0.000000<br>
dummy           0.000000<br>
Upv-Ist         172.000000<br>
dummy           0.000000<br>
dummy           0.000000<br>
Riso            3.000000<br>
Uac             234.000003<br>
Uac             234.000003<br>
Uac             234.000003<br>
Fac             49.959999<br>
Plimit          1200.000000<br>
dummy           0.000000<br>
dummy           0.000000<br>
dummy           0.000000<br>
dummy           0.000000<br>
dummy           0.000000<br>
dummy           0.000000<br>
dummy           0.000000<br>
dummy           0.000000<br>
dummy           0.000000<br>
dummy           0.000000<br>
dummy           0.000000<br>
dummy           0.000000<br>
Pac             582.000000<br>
dummy           0.000000<br>
dummy           0.000000<br>
dummy           0.000000<br>
dummy           0.000000<br>
dummy           0.000000<br>
State           OK<br>
<br>
<h1>485solar-get -i (info)</h1>
1   WR12-061 SN:2002116358<br>
Software-BFR 4.090000 <br>
SMA-SN 2002116358.000000 <br>
Default 8.000000 BE/C10/11<br>
Status Mpp<br>
Betriebsart Mpp-Betrieb<br>
485solar-get v1.000 daemon: Running<br>

<h1>485solar-get -a (alarms)</h1>
Fehler -------<br>
<br>
<h1>485solar-get -s (possible status fields)</h1>
All possible status texts for Status:<br>
( 0): 'Offset'<br>
( 1): 'Stop'<br>
( 2): 'Netzueb.'<br>
( 3): 'Warten'<br>
( 4): 'U-Konst'<br>
( 5): 'Turbine'<br>
( 6): 'Mpp-Such'<br>
( 7): 'Mpp'<br>
( 8): 'Stoer.'<br>
( 9): 'Fehler'<br>
(10): 'Mpp-Peak'<br>
(11): 'Derating'<br>
All possible status texts for Fehler:<br>
( 0): '-------'<br>
( 1): 'NUW-UAC'<br>
( 2): 'NUW-FAC'<br>
( 3): 'B3'<br>
( 4): 'K1-Trenn'<br>
( 5): 'B5'<br>
( 6): 'EEPROM dBh'<br>
( 7): 'ROM'<br>
( 8): 'B8'<br>
( 9): 'B9'<br>
(10): 'B10'<br>
(11): 'B11'<br>
(12): 'B12'<br>
(13): 'EeRestore'<br>
(14): 'B14'<br>
(15): 'B15'<br>
(16): 'B16'<br>
(17): 'B17'<br>
(18): 'AC'<br>