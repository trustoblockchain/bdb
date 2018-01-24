# Trusto Biometric Document Blockchain (BDB) Protocol

Secure document storage in the blockchain.

The biometric document blockchain implements a kind of storage space
sharing system, in which participants are payed according to the 
space they provide for the network. 

This library implements the core functionality of the document blockchain
which is part of the Trusto system based on 2 parallel blockchains:

*   the transactions blockchain providing high speed transactions
*   the document blockchain providing document storage

It supports transactions blockchain providing storage for transaction data,
storage that is used by the trusto's hybrid biometric smart contracts (HBS)
to validate transactions.

## Installation

The only supported installation method, right now, is from source files,
[stack](http://www.haskellstack.org/).

## Building from source

### Prerequisites

You will need to [download and install stack](https://docs.haskellstack.org/en/stable/README/#how-to-install).

You also need [git](https://git-scm.com/) to get the latest source code.

### Get the source

    git clone https://github.com/trusto/hbs.git
    
### Building

To build the project, you need first to run `stack setup`. This command
will make sure you have the correct haskell compiler, and, if you don't
have it, it will download and install one in a separate location in such
a way to not interract with your existing haskell environment (if you have one):

    #> cd /the/location/of/trusto/hbs
    #> stack setup
    
After the setup (you only need to run setup once) you may build, test or install
the software. To build, simply issue:

    #> stack build
    
To run the tests:

    #> stack test
    
To install it in the stack's install directory, type:

    #> stack install

## Architecture

The Document Block Chain enables sharing storage for documents etirely in the blockchain. Unlike other blockchains,
the storage is shared between participants, it is not copied between all full nodes. Althought there is a redundancy
that assures the data is never lost, the more participants to the network, the more space is available for document
storage.

