<h1 align="center"> Snapshot User Guide </h1>
<h3 align="left"> The node snapshot is taken once a day, at 03:00 UTC +2. </h3>

The snapshot is implemented through the tar archiver and compressed with lz4. To unpack the snapshot, it is necessary to install lz4.
```
sudo apt update
sudo apt install snapd -y
sudo snap install lz4
```
Download the snapshot:
```
wget -O NibiruTest.tar.lz4 https://ytwofund.pro/snapshot/NibiruTest/NibiruTest.tar.lz4 --inet4-only
```
Stop the node:
```
systemctl stop nibid.service
```
Reset the node's data:
```
nibid tendermint unsafe-reset-all --home $HOME/.nibid --keep-addr-book
```
Unpack the snapshot to the location of your database:
```
lz4 -c -d NibiruTest.tar.lz4  | tar -x -C $HOME/.nibid/data/
```
Restart the node:
```
systemctl restart nibid.service
```
Request the logs to make sure the node is working and synchronization has started:
```
sudo journalctl -u nibid -f
```
To save space, delete the downloaded snapshot:
```
rm -rf NibiruTest.tar.lz4
```
If everything is done correctly, synchronization with the network will start, but it may take some time.

If you have any problems, please let us know at ytwofund@gmail.com.
