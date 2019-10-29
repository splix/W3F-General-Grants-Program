# Dshackle Smart Load Balancer

## Project Description
Dshackle is an Open Source load balancer for blockchain APIs. 

The main goal of the project is:

- allow to separate application clusters and blockchain servers
- make blockchain access more compatible with modern microservice oriented architecture
- provide secure access to a blockchain, on both protocol and data level

The main features compared to other load balancers:

- leveraging gRPC and HTTP2 protocols, with server push and asynchronous communications, to simplify and optimize standard access patterns
- targeting Kubernetes architecture
- automatically distributing access to API through multiple different target nodes, taking into account their current availability and status
- allowing to build a mesh network of routers in different regions sharing a set of underlying nodes, with automatic rebalancing and smart routing
- caching verified data on the edge
- providing monitoring (ex. Prometheus) and externalizable logging
configurable access authentication and authorization, including TLS certificates

It's currently in the initial phase of development, and some of the features mentioned above are in development though the project is already used in production by a couple of projects.  At this moment, it supports only Ethereum and Ethereum Classic blockchains, plus their testnets. This proposal is offering to add support for the Polkadot project.

The current project is based on lessons learned from previously developed closed source (and more straightforward) load balancer for Ethereum RPC API, which was in production for the previous 2 years. 

Such Load Balancer is an essential element of building a robust and secure backend infrastructure for a blockchain service, such as exchange, wallet, or other service requiring reliable access to a blockchain. 

Project Link: https://github.com/emeraldpay/dshackle

## Team Experience
Igor Artamonov, lead developer. He has a master's degree in Computer Science, is a professional software developer since 2001, has been writing code since 1995. The main focus of his work has been on scalable, decentralized, distributed, and fault-tolerant applications; on projects storing and processing big data; on user authentication and security.

For the past few years, he got involved in blockchain space. From 2016 through the end of 2018, he was leading the development of Ethereum Classic blockchain. He was also working on a Block Explorer, integration libraries for Ethereum, and Emerald Wallet. He is knowledgeable of tech aspects of blockchain implementations, APIs, and usage scenarios of blockchain. He is currently working on a decentralized infrastructure for cryptocurrency transactions. Dshackle Load Balancer is a part of this work.

Links:

- https://www.linkedin.com/in/igorartamonov/
- https://github.com/splix

## Legal Structure

Swiss GmbH

## Development Roadmap

The scope of the project is adding support of Polkadot specific API and features into Dshackle Smart Balancer. It's expected that the project could take up to 12 weeks of work. 

### Milestones

#### Integrate Polkadot API - 4 weeks
It includes extending Dshackle architecture, commands, protocol, and configuration structure with the new type of blockchain. 

Deliverables:

- can configure Polkadot upstream
- run balancer and subscribe to the current status on Polkadot
- a Docker based usage demo

#### Full API access through balancer - 4 weeks

Deliverables:

- execute any commands supported by Polkadot though balancer
- Docker-based quick-start example configuration

#### Caching, monitoring, JS API - 4 weeks

Deliverables:

- balancer caches data in memory and/or local Redis
- Prometheus compatible endpoint for gathering current metrics related to Polkadot access and upstream
- Kubernetes compatible health-checking endpoint
- RPC provider for polkadot-js
- Individual tutorial covering setup and use of Polkadot balancer

### Notes

Milestones will also include changes to the general documentation coming with the project.

The Emerald team has long term plans on the Dshackle Load Balancer project and is going to continue to maintain and develop it after finishing Polkadot integration.

