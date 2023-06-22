<h1 align="center"> State-Sync Peer for Nibiru. </h1>
To synchronize, you can use our peer by adding it to the config.toml file.

```
613e133355a43be28b31d33d13c8814d6ea0c99f@185.216.176.209:13656
```
To add the peer, you can use the following instructions:
```
PEERS=613e133355a43be28b31d33d13c8814d6ea0c99f@185.216.176.209:13656
sed -i.bak -e "s/^persistent_peers =./persistent_peers = "$PEERS"/" $HOME/.nibid/config/config.toml
```

Alternatively, you can add it manually.
Open the config.toml file with the nano editor.
```
nano .nibid/config/config.toml
```
Add the peer YTWOFUND to the "persistent_peers" line.
