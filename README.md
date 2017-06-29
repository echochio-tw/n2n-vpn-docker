# n2n-vpn-docker



# start supernode

// foreground mode

    docker run --privileged --net=host -p 53/udp --rm -ti echochio/n2n /usr/local/sbin/supernode -l 53 -f


// daemon mode

     docker run -d --privileged --net=host -p 53/udp --name n2n_supernode echochio/n2n /usr/local/sbin/supernode -l 53 -f

# start edge

// foreground mode

    docker run --privileged --net=host --rm -ti echochio/n2n edge -d /usr/local/sbin/n2n0 -a 10.9.9.1 -c mypbxnet -k mypass -l <supernode_host>:<port> -f

// daemon mode

    docker run -d --privileged --net=host --name n2n_edge echochio/n2n edge -d /usr/local/sbin/n2n0 -a 10.9.9.1 -c mypbxnet -k mypass -l <supernode_host>:<port> -f


