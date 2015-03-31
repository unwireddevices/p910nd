Patch to control printer's power from OpenWRT-based print server with p910nd printing daemon.

Use solid state relay connected to print server's GPIO output.

Additional command-line options:
''-g <gpio>'' (GPIO number)
''-t <timeout>'' (timeout in seconds to let the printer finish its job; printer will be turned off in ''timeout'' seconds after p910nd finish sending a job to it; default is 300 seconds)


Corresponding /etc/config/p910nd.conf options:
''gpio <number>''
''timeout <seconds>''

Every new job resets the timeout counter.
