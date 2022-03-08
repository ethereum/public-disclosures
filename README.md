# Ethereum Foundation Vulnerability Disclosures
Through its Bug Bounty Program, which allows the Ethereum Foundation (EF) to coordinate and cross-check vulnerabilities across clients, the EF currently accepts vulnerability reports for Nimbus, Teku, Lighthouse, Prysm, Lodestar, Go Ethereum, Nethermind, Erigon and Besu.

While, for example, the Go Ethereum Team have a public Vulnerability disclosure page (parts of which is being used here) and have published vulnerability disclosures for quite some time already, there has not been a coordinated publishing of vulnerabilities for all clients under the scope of the Bug Bounty Program.

Since the creation of the [Execution Layer Bug Bounty Program](https://bounty.ethereum.org) and the [Consensus Layer Bug Bounty Program](https://eth2bounty.ethereum.org), the EF has paid out rewards for multiple reported vulnerabilities.

Most of the vulnerabilities were not previously disclosed publicly, but we have now been [publishing vulnerabilities on GitHub](disclosures/), up until the latest hard fork on each layer.

We aim to further improve the disclosure process, while also attempting to find an appropriate balance between confidentiality and transparency when disclosing vulnerability reports public moving forward:

[Execution Layer Disclosures](disclosures/EL.md)

[Consensus Layer Disclosures](disclosures/CL.md)


#### About disclosures
Traditionally in software, it is often expected for security vulnerabilities to be immediately announced, thus giving operators an opportunity to take protective measure against attackers.

Vulnerabilies typically take two forms:
1. Vulnerabilies that, if exploited, harm the software operator. In the case of an execution layer client or consensus layer client, examples would be:
    * A bug that allow remote reading or writing of OS files
    * Remote command execution
    * Bugs that leak cryptographic keys
2. Vulnerabilies that, if exploited, harm the Ethereum Network. In the case of the execution layer or consensus layer, examples would be:
    * Consensus vulnerabilities which may cause a chain split
    * Denial-of-service during block processing, whereby a malicious transaction could cause the execution or consensus-portion of the network to crash
    * Denial-of-service via p2p networking, whereby portions of the network could be made inaccessible due to crashes or resource consumption

In most cases so far, vulnerabilities in the execution or consensus layer have been of the second type in which the health of the network is the primary concern rather than individual node operators.


#### Why silent patches
In the case of Ethereum, node operators often require a long lead time (weeks, months) to update software even to a scheduled hard fork. If a release publicly contains important consensus or DoS fixes, an attacker may attempt to execute the public vulnerability before operators have adequate time to upgrade. Delaying a potential attacker by obfuscating a vulnerability fix contained in a release in an effort to gain heard immunity in many cases is worth the temporary loss of transparency.

The primary goal for the EF is the health of the Ethereum network as a whole, and the decision as to when to publish details about a serious vulnerability boils down to minimizing the risk and/or impact of discovery and exploitation.


## Ethereum Foundation Public Disclosure Timelines
The Ethereum Foundation aims to publicly disclose bugs reported through its bug bounty program in 90 days. There may be cases, such as if a vulnerability is being actively exploited in production, in which the EF may opt to disclose a reported vulnerability sooner or later than 90 days depending on circumstances surrounding the vulnerability. In addition, the EF will always communicate and discuss plans with the affected client teams prior to a public disclosure so an optimal course of action is taken with respect to all affected software.


## Ethereum Foundation Vulnerability Catalogue
The Ethereum Foundation maintains a list of publicly disclosed vulnerabilities and incident reports for targets within the bug bounty program. The list of publicly disclosed vulnerabilities and incidents can be accessed at https://github.com/ethereum/public-disclosures/.


## Vulnerability Disclosure Process
Reports received through the Ethereum Bug Bounty Program are evaluated, cross-checked, and then shared with affected client teams.

The Ethereum Foundation also requests that vulnerabilities found by client teams or vulnerabilities reported directly to client teams are sent to the EF through each client team's preferred method of contact.

The EF requests such a notification to be able to evaluate if the vulnerability affects other clients in the ecosystem and to assist with coordination/communication efforts with the client team(s).

The EF will not disclose the vulnerability to other client teams or third parties prior to the public disclosure with the exception if a client is also found to be affected by the same vulnerability.

The process is split into five phases:
### 1. Discovery phase
A vulnerability may be discovered and reported in one of many ways:
- Discovered by a member of a client team
- Discovered by the Ethereum Foundation
- Discovered by a third party and reported directly to the client team
- Discovered by a third party and reported through the Ethereum Bug Bounty Program

### 2. Cross-Check phase
In the event that the vulnerability is reported through the Ethereum Foundation's Bug Bounty Program, by the Ethereum Foundation directly, or forwarded by a client team, the EF will cross-check to evaluate if other client software is vulnerable to the same issue.

### 3. Preparation and testing phase
The Ethereum Foundation will remain in active communication with the client team(s) as the team(s) privately prepares a fix for the vulnerabily. Generally, these fixes are hidden through various means to obfuscate that there is a vulnerability being patched.

### 4. Release phase
Client teams normally use their coordination channels such as Twitter, Discord, Reddit and Blogs to inform about the new update being available. The Ethereum Foundation will reach out to inform relevant stakeholders where feasible and necessary, such as maintainers of critical libraries and services.

### 5. Public Disclosure phase
The Ethereum Foundations aims to disclose vulnerabilities no longer than 90 days after the initial report by adding it to the Ethereum Foundation Vulnerability Catalogue, preferably in collaboration with the affected client team(s).

If you think you’ve found a security vulnerability or any bug, please submit a bug report to the [execution layer](https://bounty.ethereum.org/) or [consensus layer](https://ethereum.org/en/eth2/get-involved/bug-bounty/) bug bounty program! 💜🦄
