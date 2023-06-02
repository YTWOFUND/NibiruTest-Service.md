<h1 align="center"> State-Sync Peer for Nibiru. </h1>
To synchronize, you can use our peer by adding it to the config.toml file.

```
89fb5a76129a723260371547ef1c25e1e97cabd0@188.172.228.225:26636
```
To add the peer, you can use the following instructions:
```
PEERS=89fb5a76129a723260371547ef1c25e1e97cabd0@188.172.228.225:26636
sed -i.bak -e "s/^persistent_peers =./persistent_peers = "$PEERS"/" $HOME/.quicksilverd/config/config.toml
```

Alternatively, you can add it manually.
Open the config.toml file with the nano editor.
```
nano .nibid/config/config.toml
```
Add the peer YTWOFUND to the "persistent_peers" line.
