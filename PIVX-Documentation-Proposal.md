# PIVX - Project User Documentation

## Current state - high-level assessment
Documentation for the project is currently scattered across multiple places:

**1. PIVX Forum:**
* Hosts User documentation/tutorials (as forum articles)
* Content is pertinent and of good quality but the forum format has a couple of drawbacks:
	* Documentation **should not be delivered via an interactive medium** as it blurs the boundaries between documentation and support
	* A forum keeps history; hence **outdated documentation remains online** indefinitely, confusing users
* Users also use the forum for support & general questions. It is monitored less closely than the #Support Discord chat (with a few user questions left unanswered).

**2. PIVX Website:**
* The documentation page on the website links to forum articles (https://pivx.org/user-guides).
* Again, this is quality content, but that approach makes it difficult to use and maintain for both users and maintainers:
	* The articles are not presented in a structured manner/with a **user learning curve in mind**; users most likely have to use a search engine to find what they need
	* That **structure requires at least 2 users** to make any change (a documentation writer + a web dev).

**3. FAQ in wallet itself.**
* The FAQ in wallet is pertinent/useful/up-to-date.
* It is also multi-language, which makes the overall **user-experience very consistent** across the Wallet.
* Having documentation embedded in the Core Wallet code also **has an impact on Core development resources** for changes. 

**4. PIVX Crypto Youtube account:**
* The PIVX Crypto YouTube account contains numerous short-format video tutorials (on how to setup wallet, staking etc). I think it’s a pertinent media to keep but it **could be made easier to find/access for users**.
* I haven’t looked at the content in detail (I’m not a video person) but what I’ve noticed is that the playlists contained deprecated videos that could be moved to an ‘archive’ section

**5. Documentation in GitHub wiki:**
* This documentation is mostly targeted at ‘power users’:
	* RPC API Reference
	* Command-line client parameters
	* SPMT Masternode tool
* The wiki is **not up-to-date at the moment**

**6. Discord:**
* Discord is used for interactive support.

## Objectives for the proposed changes
These are the objectives my proposal aims at meeting:
1. Have **all user documentation aggregated in one place** (technical and non-technical documentation)
2. Offer a structure that is easy to navigate for both new and advanced users:
* A **chronological journey for new users**
* A clean structure allowing **easy access to any section** of the documentation
* Good **search capabilities**
3. Support **multiple formats** of documentation (Text/Videos)
4. Make maintenance easy and **accessible to persons with limited technical knowledge**; reduce/**suppress dependency on Core Developers** for maintenance
5. **Use existing resources** as much as possible

## Proposed PIVX documentation structure 
n.b. This document/proposal is **limited to user documentation; contributors/ developers documentation is not in scope.**

**Proposed medium/format:**
* The recommended format is a **Wiki**, either on Github or self-hosted.
* A wiki format **meets all the objectives** listed above.
* It allows **anyone to contribute** while still allowing **core maintainers to retain control** via approval of pull requests (if Github) or user permissions (if self-hosted)

**Proposed Structure (high-level):**
* Introduction to PIVX/Main Concepts
  * Intro to PIVX (short with links to whitepaper where relevant)
  * How to get/Store my PIV (presentation of difference between core wallet, HW wallets, exchanges)
* Getting started
  * Is using a Core Wallet the right choice for me?
  * Security Considerations
  * Downloading the wallet
  * Installation
  * Startup / initial synchronisation
  * Spending / Receiving PIV (Transparent/Shielded/confirmations etc.)
* Using the QT Core Wallet
  * Description of UI
  * How-to
	  * Spending / Receiving PIV
	  * Other wallet functions on separate pages
  * Advanced configuration / Wallet debugging options
  * Troubleshooting (Common issues/FAQ)
* Staking
  * How staking works (hot / cold when available)
  * Self-hosted staking vs. staking via a shared platform
  * Configuring a Core Wallet for staking
  * Troubleshooting (Common issues/FAQ)
* Using the Command Line Core Wallet
  * Installation / setup
  * command line options
* RPC Client
  * JSON-RPC API Reference
  * RPC commands
* Governance
  * Intro
  * Creating a proposal
  * Voting on a proposal
* Masternodes
  * Requirements
  * How to set-up a masternode
  * Troubleshooting (Common issues/FAQ)
* Best Practices / FAQ
* Glossary

**Steps to transition:**
1. Define a structure and create wiki map/placeholder pages
2. Migrate all up-to-date articles from the forum to the new pages
3. Suppress or archive the deprecated content (forum posts, youtube videos)
4. Review the questions on the Support forum/Discord and incorporate the frequent ones into the doc articles/troubleshooting sections
5. Where video tutorials are available on Youtube, embed the video on the corresponding wiki page
6. Update the website to have all pages related to documentation point to the wiki

## Other ideas:
*	Update the Core Wallet to include a link to documentation
*	Update the Core Wallet FAQ to point to a wiki page to simplify maintenance
*	Have a bot repost the messages from the support section of the forum on Discord to ensure all support requetes are seen by the team
