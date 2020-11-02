# Developing Testnet Blockchain
<p align="center">
<img src="https://user-images.githubusercontent.com/62320593/97817287-5a79af00-1c69-11eb-8133-c41e0c6a8558.jpg" width="750" height="370"/>
</p>


## Background
For this assignment, I take on the role of a new developer at a small bank. My goal is to set up a testnet blockchain for my organization. Therefore, I have to create a custom testnet blockchain, make transaction to test it out, and write an instruction on how to use it.

## My Solution
### Tools
To achieve my goal, first I needed to install:

[MyCrypto](https://mycrypto.com/account)- a free, open-source, client-side interface that allows one to interact directly with the blockchain.

[Go Ethereum](https://geth.ethereum.org/)- one of the three original implementations of the Ethereum protocol. It is written in Go, fully open-source and licensed under the GNU LGPL v3.

### Creating the blockchain
Since I will be used the Proof of Authority (PoA) algorithm, I needed to generate two new nodes with new account addresses that will serve as pre-approved sealer addresses. I named the first node as "test1" and the second as "test2". I created only two nodes because two is enough to create a chain and would enough for testing purposes as well. I ran these two lines of commands below to create Create accounts for two nodes for the network with a separate datadir for each using geth.

./geth --datadir test1 account new
./geth --datadir test2 account new
