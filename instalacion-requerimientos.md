# Installing requirements

Installation is usually very simple and just takes a few steps, but we could try different options.

We must bear in mind that HarperDB **runs on NodeJS**, so if we don't have it installed we would need to install it first.

### Install and start HarperBD

Then you can install HarperDB with NPM and start it:

``$ npm install -g harperdb``\
``$ harperdb``

HarperDB will automatically start after installation.

### Offline Install

We can install HarperDB compiling from source or using npm to install HarperDB.

**Using npm:**
``npm install -g harperdb-X.X.X.tgz harperdb install``

**Installing from source:**

First, we need to download the package [install package](https://products-harperdb-io.s3.us-east-2.amazonaws.com/index.html)

**Note:** if we want to compile from source, we need the following dependencies:

- Go: version 1.19.1
- GCC
- Make
- Python v3.7, v3.8, v3.9, or v3.10