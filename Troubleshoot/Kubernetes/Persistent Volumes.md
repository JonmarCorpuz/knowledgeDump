# Troubleshooting Persistent Volumes

Error Message(s)
```JSON
"/csi.v1.Node/NodeUnstageVolume returned with error: rpc error: code = Internal desc = NodeUnstageVolume for volume PERSISTENT_VOLUME_NAME failed: device /dev/disk/by-id/DISK_ID (aka /dev/sdx) is still in use"
```
Explanation(s) 
```Text
The Container Storage Interface driver attempted to unstage (detach and unmount) the persistent volume from a node but failed
```
Potential Root Cause(s):
```Text
1. The volume is still mounted somewhere on the node (*A process has not released it*, *etc.*)
2. Application or system processes may still have open file handles on the device preventing it from being unmounted
3. Some mount points or processes can linger especially if there was a crash or forced deletion
```
Troubleshooting Step(s):
```Bash
# Identify processes using the device and gracefully kill them
sudo lsof | grep /dev/sdx
sudo fuser -m /dev/sdx

# Check for mount points and unmount if mounted
mount | grep /dev/sdx
sudo unmount /dev/sdx

# Ensure no pods are still referencing the volume
kubectl get pods
kubectl describe pod POD_NAME
```

<br>