# blockchain-setup

#  Note

   Blockchain is already running at both instance this is for info we can use  http://ec2-34-231-121-179.compute-1.amazonaws.com:8545 for front-end implamentation.


Basic setup. Is already installed via pdf with minor changes in genesis.json file.


# 1)  ssh access to node-1
# 2)  run geth --datadir ~/eth-dev/ --networkid 45634 --verbosity 3 --ipcdisable --rpc --port 30301 --rpcport 8545 --rpcaddr 
#      //PublicDNS address of your Node 1 console 2>> ~/eth-dev/eth.log
# 3)  open new terminal   
# 4)  ssh access to node-2
# 5)  run geth --datadir ~/eth-dev/ --networkid 45634 --verbosity 3 --ipcdisable --rpc --port 30301 --rpcport 8545 console 2>> ~/eth-dev/eth.log
# 6)  miner.start(); if shows error then run this miner.setEtherbase("node-1 coin base address");
# 7)  run miner.start() again
# 8)  go to node-1  check balance its increase with this  web3.fromWei(web3.eth.getBalance(web3.eth.accounts[0]), 'ether');
# 9)  now we can connect our client app to this Public DNS address of your Node-1:8454 for use blockchain   node-1; 
# 10)  if you want to run geth in background use nohup then command in line 2 . same as for node2
# 11)   install chrome extension metamask  and connect with this example url :  http://ec2-34-231-121-179.compute-1.amazonaws.com:8545



