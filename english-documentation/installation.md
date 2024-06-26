# Installation Procedure
We're going to perform an installation by binary compilation:

First, we need to download the package [install package](https://products-harperdb-io.s3.us-east-2.amazonaws.com/index.html)

**Note:** if we want to compile from source, we need the following dependencies:

- Go: version 1.19.1
- GCC
- Make
- Python v3.7, v3.8, v3.9, or v3.10

After downloading the package, we need to excecute: 

``npm install -g harperdb-X.X.X.tgz harperdb install``

**Steps for installation:**
1. In the system terminal, we go to the directory where the HarperDB installation package is located.

    ``[geralduwu@geraldtop harperdb]$ ls``\
    ``harperdb-4.2.0.tgz``

**Note:** is mandatory to have installed NodeJS for installing HarperDB.

2. We start the installation:

    ``[geralduwu@geraldtop harperdb]$ npm install -g harperdb-4.2.0.tgz``

![Installation-process](./images/installation.png)

3. After the installation we would see a promt like this:
   
    ``added 1 package in 1m``

4. After the installation, we can start HarperDB running this command: ``harperdb`` or ``harperdb start``