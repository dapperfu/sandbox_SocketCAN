# Setup Linux

### Bring up one interface

     modprobe vcan # Needs done one.
     ip link add dev vcan0 type vcan
     ip link set up vcan0


### Bring up 10 interfaces.

```
for iface_number in `seq 0 9`; 
do 
ip link add dev vcan${iface_number} type vcan
ip link set up vcan${iface_number}
done
```
