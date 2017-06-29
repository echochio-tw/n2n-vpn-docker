# n2n-vpn-docker



# start supernode

     docker run -d -p 192.168.0.70:53:53/udp --name n2n_supernode echochio/n2n /usr/local/sbin/supernode -l 53 -f

# start edge

    docker run -d --privileged --net=host --name n2n_edge echochio/n2n /usr/local/sbin/edge -d n2n0 -a 10.9.9.1 -c mypbxnet -k mypass -l 192.168.0.70:53 -f
