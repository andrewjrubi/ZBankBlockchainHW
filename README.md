# ZBankBlockchainHW

## Welcome to the ZBank Blockchain Network

#### To start the network use geth to launch the guccighost ethereum network, which uses a proof-of-authority consensus.
#### Proof-of-authority consensus registers a higher transaction rate than proof-of-work or proof-of-stake algorithms and allows for easy validation of transactions. This is ideal for a test blockchain network for our bank.

#### Using geth in the gitbash terminal, use the following prompts to create and initiate our two test nodes: 
##### ./geth --datadir node5 init guccighost.json
##### ./geth --datadir node6 init guccighost.json
#### This will create our two public key addresses:
##### 0x1B934829E4Ae88deE6f5E3e393c26821EF972467
##### 0x97EC67Cf66f9E3069b715B5AfE0b03Db574655B4

#### With the two public key addresses we will use geth to launch our two nodes in separete gitbash terminals using the following code:
##### ./geth --datadir node5 --unlock "1B934829E4Ae88deE6f5E3e393c26821EF972467" --mine --rpc --allow-insecure-unlock
##### ./geth --datadir node6 --unlock "97EC67Cf66f9E3069b715B5AfE0b03Db574655B4" --mine --port 30304 --bootnodes "enode://5b47529a2607f2218e5b1ec6d56086820ef0947f915eb9aa4e88f41e6f21520b16ea5d7be08fa445bbd9d1daf1b7bafce4f24e2cdac3a6cba90a604d470c0a2f@127.0.0.1:30303" --ipcdisable --allow-insecure-unlock

#### This code will use the rpc port in your local machine to run the nodes as well as allowing the insecure unlock of the nodes. We use the 'sealer one enode address' in the node6 launch code to ensure the mining blocks connect with one another.

#### The node password is 'supergucci' and the chain ID is '444'.

#### Using MyCrypto we created a custom network called 'GucciNet' with the '444' chain ID, the URL: http://127.0.0.1:8545, and 'ETH' as the currency.

#### Once connected to the GucciNet network, we will use the Keystore file that was created when we initiated our node5 and node6. We will use the node5 Keystore file to unlock the account wallet. Ensure to use the network password.

#### Since our account is prefunded with test ETH, we can run a test transaction between our two accounts 'node5' to 'node6'.

#### The screenshots folder shows our network code as well as a pending transaction of 100 ETH.
