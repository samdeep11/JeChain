<div align="center">
	<br/>
	<img src="./assets/extended-logo.png"/>
	<br/>
	<div><b>An experimental smart contract blockchain network</b></div>
	<br/>
	<a href="https://github.com/nguyenphuminh/JeChain/blob/master/LICENSE.md"><img src="https://img.shields.io/badge/license-GPLv3-blue.svg"/></a>
	<a href="https://github.com/nguyenphuminh/JeChain/releases"><img src="https://img.shields.io/github/package-json/v/nguyenphuminh/JeChain?label=stable"></a>
	<a href="https://snyk.io/test/github/nguyenphuminh/JeChain"><img src="https://snyk.io/test/github/nguyenphuminh/JeChain/badge.svg"/></a>
	<a href="https://github.com/nguyenphuminh/JeChain/stargazers"><img src="https://img.shields.io/github/stars/nguyenphuminh/JeChain?color=gold"></a>
	<a href="https://github.com/nguyenphuminh/JeChain/blob/main/.github/PULL_REQUEST_TEMPLATE.md"><img src="https://img.shields.io/badge/PRs-welcome-brightgreen.svg"></a>
</div>

## What is JeChain?

JeChain is a blockchain network platform that supports smart contracts and can act as a payment system/cryptocurrency. It is originally and still is made for experimental and educational purposes, you can have a brief look at its core ideas through its [unfinished whitepaper](https://nguyenphuminh.github.io/jechain-whitepaper.pdf).


## Setup a node

### Dependencies 

* NodeJS v16 or higher.
* Latest release of npm.

### Requirements

A system that is running Windows, Linux, or MacOS with a dual-core CPU and 8GB of RAM with a mediocre SSD/HDD should be enough.

### Installation

First, download the latest release from: https://github.com/nguyenphuminh/JeChain/releases.

Extract the zip file, in the `JeChain` folder, open up your terminal and install the required packages through `npm`:

```
npm install
```

### Generate your keys

If you haven't had a JeChain key pair before, hop over to `./utils/`, on the command line, type:

```
node keygen.js
```

And it will generate an address, a public key and a private key for you.

### Configure your node

In `config.json`, change the props for your needs:

```js
{
    "PORT": /*PORT that your node will run on, default is 3000*/,
    "RPC_PORT": /*PORT that the RPC server will run on, default is 5000*/,
    "PEERS": /*An array containing peers' address that the node will connect with, default is an empty array*/, 
    "MY_ADDRESS": /*A string containing the node's address, default is "localhost:3000"*/,
    "PRIVATE_KEY": /*A string containing a private key*/,
    "ENABLE_MINING": /*Leave true if you want to mine, default is false*/
    "ENABLE_LOGGING": /*Leave true if you want to log out contract logs, default is false*/,
    "ENABLE_RPC": /*Leave true if you want to run a RPC server, default is false*/,
    "ENABLE_CHAIN_REQUEST": /*Leave true if you want to sync chain from others, default is false*/
}
```

To see an example, `config.json` already has some data set for you to have a look at.

### Running the node

After everything is all set, simply type `node .` to run the node.

### Interacting with the node through JSON-RPC apis

This process will need you to run an RPC server, basically leave `true` in `ENABLE_RPC` in `config.json` to enable it.

To properly interact with the node, you should use the JSON-RPC apis, especially if you are creating dapps. To get started, check out [docs for JSON-RPC APIs here.](./JSON-RPC.md)

**Note: This feature is still in its early stages, things might change when a stable release is ready.**

### Run JeChain node publicly

Just do some port-forwarding, drop your public IP + the port you forwarded in and you are set!

If you don't know how to forward port, just search it up online, each router model should have its own way to do port-forwarding.


## Smart contracts?

Smart contract is still a fairly new feature in JeChain. It is only a proof of concept currently and is likely going to change in the future, but for now, you can read [this document](./CONTRACT.md) on creating smart contracts using a small language I have created called `jelscript`.

Remember to only use it for experimental purposes, I can not guarantee that this feature will be changed or not in the future. The language is also really limited and far from ready.


## Economy 

Note that this is an experimental project which is still under development, and an agreed JeChain network hasn't been formed yet, so this section is mainly just for fun.

### Units

| Unit       | Jem                       |
|------------|---------------------------|
| Jem        | 1                         |
| KJem       | 1,000                     |
| MJem       | 1,000,000                 |
| GJem       | 1,000,000,000             |
| MicroJelly | 1,000,000,000,000         |
| MilliJelly | 1,000,000,000,000,000     |
| Jelly      | 1,000,000,000,000,000,000 |

### Tokenomic

* 100000000 Jelly is minted originally.
* Current mining reward is 0.202297 Jelly.
* Minimum transation fee is 1000000000000 Jem.
* Minimum contract execution fee is 10000000 Jem. 


## Todos 

To see a full list of todos for JeChain, visit: https://github.com/nguyenphuminh/JeChain/projects/3


## Support the project!

I have been maintaining the project in my free time, if you like JeChain and want to support, you can just leave a star and feel free to open issues and pull requests!


## Using the project's source code

JeChain is 100% open-source, but if you are integrating its source code into your own project, it would be lovely if you credit the original JeChain, I would really appreciate it!


## Copyrights and License

Copyrights © 2021 Nguyen Phu Minh.

This project is licensed under the GPL 3.0 License.
