# tessel runtime

This is the runtime and JavaScript engine that runs on Tessel, it's kinda crazy and doesn't have a stable API

```
git clone --recursive https://github.com/tessel/runtime.git
```

## API
<!-- generated by https://github.com/tcr/markdocs -->

### Net
Networking

&#x20;<a href="#api-typedef-int-tm_socket_t" name="api-typedef-int-tm_socket_t">#</a> typedef int tm_socket_t  
socket type

&#x20;<a href="#api-tm_socket_t-tm_udp_open-" name="api-tm_socket_t-tm_udp_open-">#</a> tm_socket_t tm_udp_open ()  
open a udp socket

&#x20;<a href="#api-int-tm_udp_close-int-sock-" name="api-int-tm_udp_close-int-sock-">#</a> int tm_udp_close ( `int` `sock` )  
close a udp socket

&#x20;<a href="#api-int-tm_udp_listen-int-ulSocket-int-port-" name="api-int-tm_udp_listen-int-ulSocket-int-port-">#</a> int tm_udp_listen ( `int` `ulSocket`, `int` `port` )  
listen to udp

&#x20;<a href="#api-int-tm_udp_receive-int-ulSocket-uint8_t-buf-unsigned-long-buf_len-uint32_t-ip-" name="api-int-tm_udp_receive-int-ulSocket-uint8_t-buf-unsigned-long-buf_len-uint32_t-ip-">#</a> int tm_udp_receive ( `int` `ulSocket`, `uint8_t` `*buf`, `unsigned` `long` `buf_len`, `uint32_t` `*ip` );  
receive on udp

&#x20;<a href="#api-int-tm_udp_readable-tm_socket_t-sock-" name="api-int-tm_udp_readable-tm_socket_t-sock-">#</a> int tm_udp_readable ( `tm_socket_t` `sock` )  
is socket readable?

&#x20;<a href="#api-int-tm_udp_send-int-ulSocket-uint8_t-ip0-uint8_t-ip1-uint8_t-ip2-uint8_t-ip3-int-port-uint8_t-buf-unsigned-long-buf_len-" name="api-int-tm_udp_send-int-ulSocket-uint8_t-ip0-uint8_t-ip1-uint8_t-ip2-uint8_t-ip3-int-port-uint8_t-buf-unsigned-long-buf_len-">#</a> int tm_udp_send ( `int` `ulSocket`, `uint8_t` `ip0`, `uint8_t` `ip1`, `uint8_t` `ip2`, `uint8_t` `ip3`, `int` `port`, `uint8_t` `*buf`, `unsigned` `long` `buf_len` )  
send on socket

&#x20;<a href="#api-tm_socket_t-tm_tcp_open-" name="api-tm_socket_t-tm_tcp_open-">#</a> tm_socket_t tm_tcp_open ()  
open tcp

&#x20;<a href="#api-int-tm_tcp_close-" name="api-int-tm_tcp_close-">#</a> int tm_tcp_close ()  
close tcp

&#x20;<a href="#api-int-tm_tcp_connect-tm_socket_t-sock-uint8_t-ip0-uint8_t-ip1-uint8_t-ip2-uint8_t-ip3-uint16_t-port-" name="api-int-tm_tcp_connect-tm_socket_t-sock-uint8_t-ip0-uint8_t-ip1-uint8_t-ip2-uint8_t-ip3-uint16_t-port-">#</a> int tm_tcp_connect ( `tm_socket_t` `sock`, `uint8_t` `ip0`, `uint8_t` `ip1`, `uint8_t` `ip2`, `uint8_t` `ip3`, `uint16_t` `port` )  
connect on tcp

&#x20;<a href="#api-int-tm_tcp_write-tm_socket_t-sock-uint8_t-buf-size_t-buflen-" name="api-int-tm_tcp_write-tm_socket_t-sock-uint8_t-buf-size_t-buflen-">#</a> int tm_tcp_write ( `tm_socket_t` `sock`, `uint8_t` `*buf`, `size_t` `buflen` )  
write on tcp

&#x20;<a href="#api-int-tm_tcp_read-tm_socket_t-sock-uint8_t-buf-size_t-buflen-" name="api-int-tm_tcp_read-tm_socket_t-sock-uint8_t-buf-size_t-buflen-">#</a> int tm_tcp_read ( `tm_socket_t` `sock`, `uint8_t` `*buf`, `size_t` `buflen` )  
read on tcp

&#x20;<a href="#api-int-tm_tcp_readable-tm_socket_t-sock-" name="api-int-tm_tcp_readable-tm_socket_t-sock-">#</a> int tm_tcp_readable ( `tm_socket_t` `sock` )  
is socket readable?

&#x20;<a href="#api-int-tm_tcp_listen-tm_socket_t-sock-uint16_t-port-" name="api-int-tm_tcp_listen-tm_socket_t-sock-uint16_t-port-">#</a> int tm_tcp_listen ( `tm_socket_t` `sock`, `uint16_t` `port` )  
listen on port

&#x20;<a href="#api-tm_socket_t-tm_tcp_accept-tm_socket_t-sock-uint32_t-ip-" name="api-tm_socket_t-tm_tcp_accept-tm_socket_t-sock-uint32_t-ip-">#</a> tm_socket_t tm_tcp_accept ( `tm_socket_t` `sock`, `uint32_t` `*ip` )  
accept new incoming connection

&#x20;<a href="#api-uint32_t-tm_hostname_lookup-const-uint8_t-hostname-" name="api-uint32_t-tm_hostname_lookup-const-uint8_t-hostname-">#</a> uint32_t tm_hostname_lookup ( `const` `uint8_t` `*hostname` )  
lookup host


## options

OSX

```
make
./bin/colony test/regex.js
```

Embedded

```
make embed
# use it there
```