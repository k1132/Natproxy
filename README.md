# Natproxy
A proxy to traversal NAT, like port forwarding.

# Example
Config file is like this
```
<natproxy>
    <server-addr>123.123.123.123</server-addr>
    <server-port>8888</server-port>
    <port-mappings>
        <mapping>
            <client-addr>192.168.0.126</client-addr>
            <client-port>3389</client-port>
            <mapping-port>8881</mapping-port>
        </mapping>
        <mapping>
            <client-addr>192.168.0.116</client-addr>
            <client-port>80</client-port>
            <mapping-port>8882</mapping-port>
        </mapping>
    </port-mappings>
</natproxy>
```
Run npserver at 123.123.123.123 and run npclient at local network.  
Then you can access 192.168.0.126:3389 by 123.123.123.123:8881 and access 192.168.0.116:80 by 123.123.123.123:8882.  
   
This Project is depend on libohnet.