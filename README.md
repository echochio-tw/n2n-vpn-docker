# n2n-vpn-docker

![alt tag](https://camo.githubusercontent.com/f35cee935830315c180ec86e8b0e551fbde2434b/68747470733a2f2f7765622e617263686976652e6f72672f7765622f3230313130393234303833303435696d5f2f687474703a2f2f7777772e6e746f702e6f72672f77702d636f6e74656e742f75706c6f6164732f323031312f30382f6e326e5f6e6574776f726b2e706e67)

# start supernode

     docker run -d -p 192.168.0.70:53:53/udp --name n2n_supernode echochio/n2n /usr/local/sbin/supernode -l 53 -f

# start edge

//node IP 10.9.9.1

     docker run -d --privileged --net=host --name n2n_edge echochio/n2n /usr/local/sbin/edge -d n2n0 -a 10.9.9.1 -c mypbxnet -k mypass -l 192.168.0.70:53 -f
    
//node IP 10.9.9.2

      docker run -d --privileged --net=host --name n2n_edge echochio/n2n /usr/local/sbin/edge -d n2n0 -a 10.9.9.2 -c mypbxnet -k mypass -l 192.168.0.70:53 -f
