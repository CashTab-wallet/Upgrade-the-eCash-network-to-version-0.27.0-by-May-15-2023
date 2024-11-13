# Upgrade the eCash network to version 0.27.0 (May 15 2023)
![Logo](https://i.ibb.co/PWW2wLW/Logo-with-dark-blue-text.png)

### Do I need to upgrade my [CashTab wallet](https://ecashtab.org/)?
The network upgrade only affects full nodes. Other eCash software, including wallets such as [CashTab](https://ecashtab.org/)  are not affected by the network upgrade. It is safe to use a wallet during this period

### Exactly when will the upgrade activate?
In order to activate reliably at a predictable time, the network upgrade uses the "Median Time Past" mechanism. The upgrade activates when the median of the last 11 blocks reaches timestamp 1684152000 (12:00:00 UTC on May 15th, 2023). This means that the upgrade doesn't actually activate exactly at that time, but typically about one hour later, when 6 blocks with timestamps greater than the activation time have been produced.

### Who needs to upgrade?
All operators of a Bitcoin ABC full node must upgrade to the latest major version (0.27.x). This includes Avalanche staking nodes, Miners and Exchanges. The up-to-date node version is available at our Releases page.

### How do I upgrade?
The process of upgrading your node is straightforward: simply stop the currently running node, download the new version, and start the new version. Here are some example instructions for upgrading from version 0.26.13 to the latest version (0.27.1) on Linux:

```sh
Shut down the node: ./bitcoin-abc-0.26.13/bin/bitcoin-cli stop
Download the new version archive from the website: wget https://download.bitcoinabc.org/0.27.1/linux/bitcoin-abc-0.27.1-x86_64-linux-gnu.tar.gz
Extract the archive: tar xzf bitcoin-abc-0.27.1-x86_64-linux-gnu.tar.gz
Restart the node with the new version: ./bitcoin-abc-0.27.1/bin/bitcoind -daemon
Clean up old version and archives (optional):
rm -rf bitcoin-abc-0.26.13
rm -f bitcoin-abc-0.26.13-x86_64-linux-gnu.tar.gz
rm -f bitcoin-abc-0.27.1-x86_64-linux-gnu.tar.gz
```
