The added function EthernetServer::connected() gets a client that is connected to the server but not necessarily has data available, unlike function EthernetServer::available().

The EthernetClient object returned is the client connected.

If there is no client connected, the function returns zero.

Example:

EthernetServer ftpServer( FTP_CTRL_PORT );

EthernetClient client;

...

client = ftpServer.connected();

if( client > 0 )   // A client is connected

...

To install, replace the original files in library/Ethernet/src with the 2 files EthernetServer.cpp and EthernetServer.h of this repository.
