# mm-multi-auth
Authenticate multiple EOAs with MetaMask

This is a demo of how to interact with the MetaMask Wallet API. 
It uses EIP-6963 for provider detection to safely detect MetaMask. 
It then users methods like `eth_getAccounts` and `eth_requestAccounts` to 
interface with permitted accounts. It also uses `wallet_requestPermissions` 
to force a fresh account connection flow even when the website already has 
an active "connection," and listens for the "accountsChanged" event to 
update the set of permitted accounts on the dapp to match changes in MetaMask.
Lastly, it demonstrates how to let the user sign for any account when multiple 
accounts are connected.
