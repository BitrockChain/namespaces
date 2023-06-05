# Namespaces
Chain Agnostic Namespaces (CANs) describe a blockchain ecosystem or set of ecosystems as a namespace, relying as much as possible on the [CAIP](https://github.com/ChainAgnostic/CAIPs) specifications to minimize the research needed to interact with assets, contracts, and accounts in that namespace.

# How it works
Each namespace implements one or more [CAIPs](https://github.com/ChainAgnostic/CAIPs). The most important CAIPs to consider for a namespace are:

- [Blockchain ID](https://github.com/ChainAgnostic/CAIPs/blob/master/CAIPs/caip-2.md) - A unique way to represent individual blockchains, also gives the namespace its name
- [Account ID](https://github.com/ChainAgnostic/CAIPs/blob/master/CAIPs/caip-10.md) - Unique representations of blockchain accounts (also used in [DID PKH](https://github.com/w3c-ccg/did-pkh/))
- [Asset Type and Asset ID](https://github.com/ChainAgnostic/CAIPs/blob/master/CAIPs/caip-19.md) - Uniquely refer to assets within the namespace
- [SIWx](https://github.com/ChainAgnostic/CAIPs/blob/master/CAIPs/caip-122.md) - Namespaces that support SIWx can be used with [CACAO](https://github.com/ChainAgnostic/CAIPs/blob/master/CAIPs/caip-74.md)

# Contributing

 1. Review [CAIP-92](https://github.com/ChainAgnostic/CAIPs/pull/92/files).
 2. Fork the repository.
 3. Add your CAIP to your fork of the repository. There [will soon be] a template CAN here.
 4. Submit a Pull Request to Chain Agnostics's [`namespaces` repository](https://github.com/ChainAgnostic/namespaces).

Your first PR should be a first draft of the final CAN, with all applicable CAIPs addressed. An editor will manually review the first PR for a new CAN and assign it a number before merging it. Make sure you include a `discussions-to` header with the URL to a discussion forum or open GitHub issue where people can discuss the CAN as a whole.

If your CAN requires images, the image files should be included in a subdirectory of the `assets` folder for that CAN as follows: `assets/namespace-N` (where **N** is to be replaced with the CAN name). When linking to an image in the CAN, use relative links such as `../assets/namespace-{N}/image.png`.

It is recommended that you render your PR locally to check the Jekyll syntax; to do so, run `bundle exec jekyll serve`.

# CAN Status Terms

* **Draft** - an CAN that is undergoing rapid iteration and changes.
* **Last Call** - an CAN that is done with its initial iteration and ready for review by a wide audience.
* **Accepted** - a core CAN that has been in Last Call for at least 2 weeks and any technical changes that were requested have been addressed by the author.

# CAN Index

- [`eip155`](eip155.md) - Draft
