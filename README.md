ALFA [ALFA] CORE
================================

5 Tier Masternode/POW/POS

Specifications:
--------------

- Algorithms:        Neoscrypt
- Blocktime:         120 seconds
- P2P port:          8180
- RPC port:          8181
- Maturity:          80 Blocks
- Stake Minimum Age: 36 Hours
- MN start Block:    2000
- pos start Block:   2000

- PoW (proof of work)
- Blockreward (PoW):
- Block 1 to 5760 :  5 ALFA


- PoS (proof of stake)
- Blockreward (PoS):
- 2 ALFA

- Masternode ( 5 tier masternode )
- Masternode Collaterial - 3000   - Masternodes Rewards  = 3   ALFA - 0% 
- Masternode Collaterial - 10000  - Masternodes Rewards  = 10  ALFA - 0%
- Masternode Collaterial - 25000  - Masternodes Rewards  = 26  ALFA - 4% 
- Masternode Collaterial - 88000  - Masternodes Rewards  = 95  ALFA - 7%
- Masternode Collaterial - 490000 - Masternodes Rewards  = 575 ALFA - 15%


Linux Build Instructions and Notes
==================================

Dependencies
----------------------
1.  Update packages

        sudo apt-get update

2.  Install required packagages

        sudo apt-get install build-essential libtool autotools-dev automake pkg-config libssl-dev libevent-dev bsdmainutils
        sudo apt-get install libboost-all-dev git
        sudo apt-get install libminiupnpc-dev libgmp3-dev

3.  Install Berkeley DB 4.8

        sudo apt-get install software-properties-common
        sudo add-apt-repository ppa:bitcoin/bitcoin
        sudo apt-get update
        sudo apt-get install libdb4.8-dev libdb4.8++-dev


Build
----------------------
1.  Clone the source:

        git clone https://github.com/alfapr0ject/alfa

2.  Build alfa:

    Configure and build.

        cd alfa
        cd src/
        make -f makefile.unix   



Masternode configuration is very similiar to other Masternodes coins.
----------------------

edit alfa.conf

      rpcuser=alfarpc
      rpcpassword=putyourpasswordhere
      rpcallowip=127.0.0.1
      rpcport=8181
      masternode=1
      masternodeaddr=159.65.4.224:8180
      port=8180
      masternodeprivkey=putyourkeyhere
      daemon=1

