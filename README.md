<!---
# SPDX-FileCopyrightText: © 2019-2026 Nadim Kobeissi <nadim@symbolic.software>
# SPDX-License-Identifier: CC-BY-SA-4.0
-->

## BitSherlock

BitSherlock is a fork of Verifpal which is new software for verifying the security of cryptographic protocols. Building upon contemporary research in symbolic formal verification, Verifpal’s main aim is to appeal more to real-world practitioners, students and engineers without sacrificing comprehensive formal verification features.

In order to achieve this, Verifpal introduces a new, intuitive language for modeling protocols that is much easier to write and understand than the languages employed by existing tools. At the same time, Verifpal is able to model protocols under an active attacker with unbounded sessions and fresh values, and supports queries for advanced security properties such as forward secrecy or key compromise impersonation.

#### An Intuitive Protocol Modeling Language
The BitSherlock language is meant to illustrate protocols close to how one may describe them in an informal conversation, while still being precise and expressive enough for formal modeling. Verifpal reasons about the protocol model with explicit principals: Alice and Bob exist and have independent states.

#### Modeling that Avoids User Error
BitSherlock does not allow users to define their own cryptographic primitives. Instead, it comes with built-in cryptographic functions — this is meant to remove the potential for users to define fundamental cryptographic operations incorrectly.

#### Easy to Understand Analysis Output
When a contradiction is found for a query, the result is related in a readable format that ties the attack to a real-world scenario. This is done by using terminology to indicate how the attack could have been possible, such as through a man-in-the-middle on ephemeral keys.


Otherwise, you can:

- *Download and install a release manually*: Releases for Windows, Linux, macOS and FreeBSD are available [here](https://github.com/symbolicsoft/verifpal/releases).
- *Compile from source*: Keep reading!

### Building BitSherlock from Source
You must have [Rust](https://www.rust-lang.org) installed in order to build Verifpal. Please review the [Rust Getting Started](https://www.rust-lang.org/tools/install) instructions in order to understand how to best install Rust for your computer and operating system.

#### Compiling BitSherlock
Simply type `cargo build --release` to build Verifpal. The binary will be available under `target/release/`.

#### Running Tests
Simply type `cargo test --release` to run the full test suite.
