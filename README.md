Patch to control printer's power from OpenWRT-based print server with p910nd printing daemon.

Use solid state relay connected to print server's GPIO output.

Additional command-line options:<br />
*-g &lt;gpio&gt;* (GPIO number)<br />
*-t &lt;timeout&gt;* (timeout in seconds to let the printer finish its job; printer will be turned off in ''timeout'' seconds after p910nd finish sending a job to it; default is 300 seconds)

Corresponding /etc/config/p910nd.conf options:<br />
*gpio &lt;number&gt;*<br />
*timeout &lt;seconds&gt;*

Every new job resets the timeout counter.

Usage example: http://www.black-swift.com/wiki/index.php?title=Wireless_Print_Server

Precompiled binary for OpenWRT 14.07, ar71x target architecture: http://files.black-swift.com/files/misc/p910nd_0.95-3-bsb1_ar71xx.ipk
