# Correlating Transaction Speeds and Network Integrity in Cryptocurrency Networks
CS 482 - Data Mining

Group Members: Dominic Mozeika, Nirav Patel, Khoa Nguyen

# INTRODUCTION

As private financial institutions and governments have grown to hold power over the global economy, there has been an excess of development in decentralized finance over the past ten years. Specifically, since the birth of Bitcoin in 2008, computer programmers have been able to create renowned forms of payment processing not controlled by any private entity. This disruptive technology has made its way into the global economy; integrated into public investment portfolios and even accepted as a native currency in select countries. As we go on to discuss how cryptocurrency evolved to where it is today, we will be focusing on its underlying network architecture that shapes the reliability, security, and speed of transactions on the most popular cryptocurrency networks to date.

Cryptocurrency exchanges have been around since the early days of its creation, allowing anybody to buy, trade, and transfer funds in the form of digital assets. However, cryptocurrency became much more popular when bitcoin’s value increased 2,000% in 2017, followed by a 85% decrease in 2018 (coinmarketcap.com). As this trend was followed by many cryptocurrencies being developed at this time, the high volatility sparked much curiosity in both software developers and investors alike. Throughout 2022, the overall market capitalization across all cryptocurrency markets has been in the trillions of dollars, maxing at nearly $3 trillion in august of 2021 (Fortune.com). As the crypto market inches closer to accounting for 10% of the world’s economy, there is still plenty of skepticism from famous investors and international moguls who question the integrity of the technology and the current valuations of digital assets. Moving forward we will focus on the fundamentals of select network protocols that govern how funds are securely transferred, as there is generally a tradeoff between governance and transaction speed.

To understand our research, we construct a model that analyzes the scalability and speed of select cryptocurrency networks. Here we see the tradeoffs that come with decentralized finance, including slower processing times and higher fees as market volume increases. Although we have made extensive progress in advancing network protocols that govern these outcomes, blockchain development is still in its infancy. Today there is a stronger workforce of network engineers than ever before who continue to rise to the challenge of competing with traditional monetary systems to process and handle more transactions in less time.

# RELATED WORK

Bitcoin’s technical architecture is robust in terms of security, as it uses a hashing algorithm to verify transactions in the network powered by random computers racing to solve each transaction hash. This consensus model is known as Proof-of-Work (PoW) and ensures the integrity of the network transactions. Originally, bitcoin was created for transactional use, and the anonymous creator incorporated a limited supply cap of bitcoins that can be issued on the network. By limiting how many new blocks can be issued on the blockchain over time, this supply cap was meant to act as a hedge against inflation, as an unlimited supply can create high fluctuations in future price (learn.bybit.com). To mitigate the rate at which the supply is issued, a protocol referred to as “halving” was instructed to cut the amount of new blocks in half every time a certain amount of transactions are verified. Like the creator intended, this halving mechanism has proven to fight the inflation rate of bitcoin, as the inflation rate has dropped substantially with every halving (livemint.com). 

Although the bitcoin network has proven to be secure and paved the road for blockchain development, modern finance still outperforms bitcoin in terms of scalability; i.e network bandwidth and transaction speeds. It is the secure consensus methods and limited block sizes that hurt the network speed as it grows in size. Bitcoin’s blockchain grows in a linear fashion, so it is prone to be bottlenecked when applied to practical applications at scale. This makes it nearly impossible to compete with the rate of transactions processed by a centralized network such as Visa. We can better understand this by computing how many transactions complete a full block:

Transactions Per Block = Block Size (Bytes) / Avg. Transaction Size (Bytes)

But the speed at which blocks are created is determined by the consensus algorithm, which we know is governed to issue less and less bitcoins per block over time. It is clear that bitcoin’s original network protocol was not built to compete with banks at scale, but to be a secure and stable medium of exchange. The only way for Bitcoin to compete with Visa’s network scalability is to either change the block size or the block generation time, which are both restricted by the network’s decentralized consensus algorithm (towarddatascience.com). 

The scalability problem was most evident at the end of the 2017 crypto bull run mentioned above, as network delays and transfer fees increased dramatically along with the price. And it wasn’t just Bitcoin’s network that was struggling from the increased market volume; the Ethereum network (claiming to be the faster and cheaper network at this time), was also bottlenecked with slower rates and insanely high ETH (gas) fees. There were many unanswered questions about the blockchain network architecture, as well as the transparent money trail left public for anyone to analyze. Needless to say, research and development has skyrocketed since then, resulting in a huge community of open source developers putting their heads together to build scalable solutions. With such recognition comes more active development, and many new consensus models have been proven to increase scalability in networks such as Ethereum. The most effective way to increase speed and lower fees is switching the protocol from a PoW algorithm to Proof-of-Stake (PoS), where token holders can use their own nodes (or blocks) to verify the transactions on the network. This method removes the need of block generation, as dedicated balances are used to process transactions with existing blocks. We must account for the tradeoffs that come with an entirely new governance model, since PoW enforces decentralization of the blockchain, PoS becomes more vulnerable to a DDoS 51% attack (medium.com).

# DATA

Comparing currency’s network statistics

1. Bitcoin
2. Ethereum
3. Binance Smart Chain
4. Polygon (layer 2 ethereum)
5. Ripple
6. Visa

<table>
  <tr>
   <td>
Currency
   </td>
   <td>Market Cap
   </td>
   <td>Tx Per Second
   </td>
   <td>Confirm Speed
   </td>
   <td>Daily Volume
   </td>
   <td>Supply
   </td>
   <td>Block Time
   </td>
  </tr>
  <tr>
   <td>BTC
   </td>
   <td>$755B
   </td>
   <td>3
   </td>
   <td>40 min
   </td>
   <td>$17.7B
   </td>
   <td>19M
   </td>
   <td>10 min (PoW)
   </td>
  </tr>
  <tr>
   <td>ETH
   </td>
   <td>$356B
   </td>
   <td>13
   </td>
   <td>5 min
   </td>
   <td>$9.3B
   </td>
   <td>120M
   </td>
   <td>15s (Hybrid)
   </td>
  </tr>
  <tr>
   <td>BNB
   </td>
   <td>$65B
   </td>
   <td>50
   </td>
   <td>seconds
   </td>
   <td>$1.2B
   </td>
   <td>163M
   </td>
   <td>3s (PoS)
   </td>
  </tr>
  <tr>
   <td>MATIC
   </td>
   <td>$10B
   </td>
   <td>42
   </td>
   <td>seconds
   </td>
   <td>$414M
   </td>
   <td>7.8B
   </td>
   <td>1s (PoS)
   </td>
  </tr>
  <tr>
   <td>XRP
   </td>
   <td>$33B
   </td>
   <td>1,500
   </td>
   <td>seconds
   </td>
   <td>$1.1B
   </td>
   <td>48B
   </td>
   <td>-
   </td>
  </tr>
  <tr>
   <td>VISA
   </td>
   <td>$450B
   </td>
   <td>1,700
   </td>
   <td>seconds
   </td>
   <td>$590M
   </td>
   <td>$450B
   </td>
   <td>-
   </td>
  </tr>
</table>

# METHODS

When applying our data to mathematical methods we will focus on understanding what factors are contributing the most to overall transaction speeds. The problem of scalability in PoW consensus models comes from the underlying fundamentals of a limited amount of blocks that are generated. Generally, the scalability of the networks is based solely on the physical capabilities of a computer network, such as throughput and latency. In the graph below we can see that as more traffic is coming through the network, there is a threshold where the throughput is capped and the network delays begin to get backed up.

 ![](/threshold.png)

In comparison to a proof-of-stake consensus model, we will see a much higher threshold as we are not constrained on a certain amount of time needed to create new blocks. Instead, the network can handle these transactions internally, as the nodes responsible for validating the transactions are rewarded privately in smaller amounts. This is a key difference between PoW and PoS, as the latter consensus model does not need to wait on the network to generate blocks at a high cost. Instead, it simply awards previously validated blocks to verify transactions faster and lower cost to the network.

# EXPERIMENTS

The model in which examined gives us insight to how each network protocol operates and affects transaction speeds. We notice some key takeaways from the data we generated; first and foremost we prove that the PoW consensus algorithm is bounded by the time it takes the network validators to process new blocks. In bitcoin’s case, blocks are limited and gradually slow down the generation of new blocks, lowering the odds of it becoming inflationary. The opposite is true for other cryptocurrency networks that allow unlimited amounts of supply to be generated. From our data we can derive that PoW consensus models can not handle high speeds at scale, with PoS models processing transactions 5-20x faster. And even faster than that, we see private networks such as Ripple and Visa practically handling transactions instantaneously.

 ![](/txspeed.png)

We see such high transaction rates in private networks such as ripple because the consensus model uses subnetworks that are collectively trusted within the whole network. The protocol is executed every few seconds to ensure correctness of the network. After consensus is reached, the ledger becomes closed. This ledger is constantly cross checked when a new transaction occurs, assuring that all past transactions are valid and the network size and value are accurate (ieee.org).

# CONCLUSION

We have gathered an abundance of data to better understand the integrity of each currency's network. Looking backwards on our research, we can conclude that there is a direct tradeoff between blockchain security protocols and the upper limit of network speed. As our bar chart shows above, the more robust the blockchain consensus protocol, the slower the transaction rate on the network. In theory, a slow PoW network can be enhanced by grouping transactions and handling them off chain. This follows a similar protocol as Ripple, using subnetworks to group verified blocks and deploying them in bulk to the network to reduce latency. The main takeaway from this research is that different networks are being built for unique use cases. Depending on the purpose of the network the users may favor speed over security, but in terms of the global economy, both are equally important. As the present circumstances hold, a decentralized blockchain is simply not scalable to compete with traditional banking systems. Instead of building such a network from the ground up, an approach such as Ripples may be more effective by enhancing a centralized network from the top down with such consensus models.

# REFERENCES

General info on transaction speed:

https://blog.tezro.com/cryptocurrency-transaction-speeds/

Scalability research:

https://towardsdatascience.com/the-blockchain-scalability-problem-the-race-for-visa-like-transaction-speed-5cce48f9d44

Citing overall market cap (March 2022):

https://fortune.com/2022/03/02/crypto-market-cap-2-trillion/

Market data:

https://coinmarketcap.com

Bitcoin supply cap & inflation rate:

https://www.livemint.com/money/personal-finance/what-is-bitcoin-halving-and-will-it-affect-the-rate-11610295621496.html

Polygon & layer 2 overview:

https://forkast.news/what-is-polygon-matic-ethereums-internet-blockchains/

PoW vs. PoS:

https://medium.com/@EdChain/pow-vs-pos-a-comparison-of-two-blockchain-consensus-algorithms-f3effdae55f5

Ripple consensus compared to other networks:

https://ieeexplore.ieee.org/abstract/document/8632190

