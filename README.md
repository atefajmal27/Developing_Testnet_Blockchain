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

`./geth --datadir test1 account new`</br>
`./geth --datadir test2 account new`

<img src="https://user-images.githubusercontent.com/62320593/97825932-1fd63d80-1c8e-11eb-85ad-a902e13970d3.png" width="700" height="300"/>

Next, I generated genesis block as shown below. I named the network as "chained" and used the addresses from the previous step to pre-fund the accounts. Although I ran into two errors, while exporting genesis configurations, I only needed to chained.json for this network.

<img src="https://user-images.githubusercontent.com/62320593/97826030-7f344d80-1c8e-11eb-985e-cf789aec0764.png" width="700" height="380"/>
<img src="https://user-images.githubusercontent.com/62320593/97826740-6a58b980-1c90-11eb-9ee3-1459bc53830e.png" width="700" height="150"/>

After the genesis block creation was completed, it was time to initialize the nodes with the genesis' json file as shown below followed by commanding the nodes to start mining. 

<img src="https://user-images.githubusercontent.com/62320593/97832125-0ccc6900-1ca0-11eb-9b9d-3ccb87795a67.png" width="700" height="200"/>
<img src="https://user-images.githubusercontent.com/62320593/97832137-10f88680-1ca0-11eb-9c09-3808ded94817.png" width="700" height="450"/>
<img src="https://user-images.githubusercontent.com/62320593/97832154-18b82b00-1ca0-11eb-9e10-1b4dd8724443.png" width="700" height="450"/>

With the private PoA blockchain and the nodes up and running, it was time to add the network to MyCrypto. So I created a custom network for chained and connected with the account with pre-funded balance.

<img src="https://user-images.githubusercontent.com/62320593/97832428-cc211f80-1ca0-11eb-9e53-3e7302a08feb.png" width="700" height="330"/>
<img src="https://user-images.githubusercontent.com/62320593/97832444-d0e5d380-1ca0-11eb-9a9e-efb58bc0c1ea.png" width="700" height="330"/>





