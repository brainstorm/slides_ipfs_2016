Why (from http://ipfs.io)
-------------------------

1. HTTP is inefficient and expensive (for genomic data distribution).
2. The web's centralization limits opportunity (core facilities, paywalls, long term storage).
3. Our apps are addicted to the backbone (national genomics infrastructure).

Note:
1. IPFS makes it possible to distribute high volumes of data with high efficiency. And zero duplication means savings in storage.
2. The Internet has been one of the great equalizers in human history and a real accelerator of innovation. But the increasing consolidation of control is a threat to that.
3. Developing world. Offline. Natural disasters. Intermittent connections. All trivial compared to interplanetary networking. The networks we're using are so 20th Century.


Distributed infrastructure
--------------------------

![distributed](res/distributed.png)

/via @juanbenet

TCP/IP, BitTorrent, Internet!


Interplanetary File System
--------------------------
  * A Distributed, peer to peer HTTP.
  * Similar to the Web you are used to, plus "new" tech:
    * BitTorrent
    * Git
    * Blockchains


BitSwap
-------
  * P2P filesystem block trading layer: requests/sends blocks among peers fairly:
    lessons learned from BitTorrent + optimizations.
  * Message based instead of response-reply. 
  * Works with wantlists and blocks to be xchg'd via a decision engine.
    1. maximize the trade performance for node and xchg.
    2. prevent freeloaders from degrading the exchange.
    3. be effective and resistant to unknown strategies.
    4. be lenient to trusted peers.
  
Note:
  Upon receiving a wantlist, a node should consider sending out wanted blocks if they have them. Upon receiving blocks, the node should send out a notification called a 'Cancel' signifying that they no longer want the block.


BitSwap (II)
------------

Sketch of the lifetime of a peer connection:
1. Open: peers send ledgers until they agree.
2. Sending: peers exchange want_lists and blocks.
3. Close: peers deactivate a connection.
4. Ignored: (special) a peer is ignored (for the duration
of a timeout) if a node’s strategy avoids sending.

Why u no make sense?: ![why u no make sense](res/search_ipfs_whitepaper.png)


Content-addressed
-----------------

  * Content-addressed. All blocks and files are hashed.
  * Stored in a Merkle DAG, a generalized **Git**: block/list/tree/commit.
    * Files, directories, links are DAG nodes,
  * Duplicates are therefore assigned the same hash, reducing **redundance** and thus saving disk space.
  * Each node stores what they want (unless you pin it or Filecoin it). 

Why u no make sense?: ![why u no make sense](res/search_ipfs_whitepaper.png)


IPFS quickstart
---------------
  1. go get -u -d github.com/ipfs/go-ipfs/cmd/ipfs
  4. cat "foo" | ipfs add
  5. ipfs ls


DAT
---

* Take a peek at DAT (https://datproject.org/) as well 
* And how it works underneath: https://github.com/datproject/docs/blob/master/docs/how-dat-works.md
* IPFS developer used to work there, so several similarities.

Note:

IPFS is a peer-to-peer distributed file system that seeks to connect all computing devices with the same system of files. In some ways, IPFS is similar to the World Wide Web, but IPFS could be seen as a single BitTorrent swarm, exchanging objects within one Git repository. In other words, IPFS provides a high-throughput, content-addressed block storage model, with content-addressed hyperlinks. This forms a generalized Merkle directed acyclic graph (DAG). IPFS combines a distributed hash table, an incentivized block exchange, and a self-certifying namespace. IPFS has no single point of failure, and nodes do not need to trust each other.[4] Distributed Content Delivery saves bandwidth and prevents DDoS attacks which HTTP struggles with.
