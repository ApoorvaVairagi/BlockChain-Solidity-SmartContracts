## What is Web3?
The new internet.
Describes the 3rd stage of the web.

web1.0 - netscape, yahoo: all you can do on these websites were to read the info someone else put.
Read only web.

web2.0 - facebook, instagram. Intraction started. User started interacting. 

web3.0 - people started developing building websites, application on the blockchain.

Example:
- Helium is a web3 projec which is providing wireless internet to indiviual people hosting their 5g network earning cryptocurrency.

- Pool lets you participate in no lost lottery, tricking you to save money that takes everybody's money makes the interest and pays it to the one lucky winner. The money you put in never gets lost and you can withdraw whenever you want to.

- Build games play them trade the characters and earn.


## How does Blockchain exactly works?
Blockchain is a Ledger.

Record of who owns who how much money.
Consensus - Which transaction should go into the ledger.
Trust - Who keeps a copy of the ledger? Can we trust the transaction history?

What we need is to make the history of this ledger immutabl, so lock it so cant be changed? How can we do that? Using encryption. Simplest of one is Caesar Cipher.
Caesar cipher demo to see how it works.
But in this all you need to know is the shift number and you can decrypt the message.

There are many types of Encryption techniches. 
But they can be decrypted easily. And thats how its not secure.

That's why -
Blockchain uses Hashing.
Similar to encryption but with some notable differences.
A mathematical formula also called hashing function is used to change the message to a hash code.
Going forward is very easy, but going backwards to decrypt is way difficult considering the current computaion power people have access to.

If you want to go to the message from the hash its hard.

How it is applied in Blockchain?
We have a piece of data, that is encoded into a block for that we create a hash. Now to add a block to the blockchain there are some predetermined req. This could be the hash has to start with 3 zeros. We have nonce a number which is used with the data to create the hash. 

You can choose the block difficulty, use the mine button to find the value of nonce that creates the valid hash code. The value of nonce is valid for that message only.

This combined thing creates a Block of the Blockchain.
The chain is the combining this different blocks by the hash code of the previous block together.
The first block in the blockchain has 0 value of the previous hashcode, but for the other blocks to be valid it needs to have a nonce combining the message/data with the previous hashvalue to create a hash with the selected difficulty of the block.
When its valid it can be added in the chain.

Now, if the single block is modified the other subsiquent all blocks will become invalid too. Which means the data cant be changed without people knowing about it.

### Distributed part of blockchain

In order to assure the data is not tempered in blockchain, there is another thing blockchain implements.

Distributed part of blockchain.
Solves the problem of - Consensus: Which transactions should go into the ledger?

Everytime a new miner joins the blockchain they are going to get a full copy of the blockchain.
Now by distributing the blockchain to other computer we have a way to ensure the integrity of the data.

## Decentralised Applications

The next iteration of the internet is DApps.
Dapps are the backbone of web3.

Old way - Build -> Raise VC Funding -> IPO
New web3 way - Build -> Release Tokens -> DAO

Token - make people use your application from the day 1. Transform the application to decentralised autonomous orgranization.

In these DAOs you can organize your company, allow users to contribute too, everybody is in line, the token price goes up. 

eg, Dropbox - way to store your file and access from whereever you are.

web3 compititor - Filecoin
Store your files in a decentralized way, hosted accroos millions of computers. more redenduncy. 
They rasied a funding of their token.

Pseudonymity another feature of web3.
Doesn't matter who you are your works gets recognized.
eg. Rari Capital

Large number of DApps are built on Ethereum as its the first one, it was the first chain which has this smart contract and you can write code that can be embedded into a blockchain.
Ethereum has a problem of storing also costly to perform computations.

Which is why a lot of decentralised DApps running on ethereum are actually made of a patch work of different services for example all the css, js, images are hosted in aws.

These is where Internet Computers come in.
The idea is to build a scalable cloud computer that runs on a blockchain which has all the benefits of the decentralised system but it also allows you to perform fast computation store data on blockchain directly.

## The Internet Computer (ICP)

Build DApps using Dfinity's Internet Computer

Goal: To reach Blockchain singularity

To have a powerful secure blockchain, that is capable of running entire base layer of the web. So, everything from hosting, storage, services basically everything in one secure portocol. 

Today's decentralized application are only partially decentralized, they have a very small amount of logic and data that's hosted on a secure blockchain. But the majority of the logic and the daa is all hosted on large web2 companies. for eg, aws or azure or using something like chrome's browser extensions in order to connect a wallet and let users spend and earn tokens.

Than why we are relying on this legacy infrastructure?
The reason is becuase its extremely difficult with the current blockchain for eg ethereum to be able to host large amount of data and carry out a large amount of transactions becuase it was not built for that purpose. Ethereum was built primarily to act as a ledger.

Also, remember that each new block contains transaction data that updates the blockchain. The rate at which transactions can be processed determines hwo fast a blockchain app cn run or how big it can scale. Each new post in a decentralized socail media app is a transaction. That means the number of transactions per second of the blockchain itself will limit how many posts all of your users can make, because the TPS determines how fast your app can update its state. It currently takes something like around 14s to create a new block on the Ethereum blockchain. Ethereum has gradually increased the block size over time so that more data can be stored into a single block. But in the current version of Ethereum we are limited to about 15 transactions per second. 

To solve this issue of blockchain the definity team came up with basicallt a novel consesus algorithm what they call a threshold relay and it allows the Internet Computer to be able to reach much faster sppeds when compared to the other major layer one blockchains that are currenly in existence.

How does it work?
The internet computers aggregates the compute capacity of a large number of independent data centers, and it takes all of these data centers around the world and comibines them using the Internet Computer protocol into a large single decentralized world computer. And this decentralized computer is organized into individual **Canisters** or **Canister Smart Chains**. And these canisters can basically run processes, execute code and store the data for the programs. So as a user, you can tap into the cainsters directly by making the HTTPS requests.

But as a developer, what you need to realize is that this Internet Computer is basically just a whole bunch of Canisters where each canister can hold program and programs state through a web assembly module and a flat memory model called a memory page.
So, you as a developer can write code that compiles into a performant way to run web applications on user hardware using web assembly and you can do that using many languages such as Rust or Difinity's Motoko.

And the really cool thing about these canisters is how they manage memory. Because your program's state,
so the contents of your variables, your collections, your arrays, can actually get stored within the canister.And each of these canisters acts a bit like a process or a code sandbox. It's kind of similar to containers if you're familiar with Docker and that kind of stuff, but essentially, the program state gets preserved, so your canister kind of acts as if it runs forever. So imagine if you run something in CodeSandbox and you click Run and that program never gets killed, then all of your data can just simply be kept in their variables.

So that means you don't even have to think about data persistence or putting things into databases taking things out of databases, because your program behaves like it never gets killed. So this makes canisters not only an evolution in the way that smart contracts work, but even a leap in the way that programs can be written.
Because you as a developer only really have to worry about the logic and the Internet Computer takes care of the rest.

and because everything is on-chain, you can enable some really fascinating new ways of interacting

with these Web applications.

For example, in the decentralized version of TikTok, which is called CanCan, that runs on the
Internet Computer, they have this ability for you to like a video. And then if that video later goes viral, then it looks at who were the first ten or 20 people who liked this video and rewards them with tokens from CanCan, which you can then later spend to buy real products or virtual products or get things from sponsors.

So it's genuinely bringing about a new way that we think about developing web applications and how you can interact with users through these token economics.