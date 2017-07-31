# Final DApp
This is the final DApp developed in the Etheruem Class.

## Scope
The scope of the DApp is to show the usage of Truffle, 

* demonstrate how to work with the Ethereum Blockchain 
* Web3 
* Listen and react to specific events
* Write Test Cases
* Deploy the DApp
* Work with MIST
* Integrate Angular into Truffle

## Install Instructions

Developing for Ethereum is sometimes frustrating, because things change at fast pace. If something does not work as described here, please:

1. try a google search as you are 100% not alone with your problem
2. inform the instructors of the course so they can correct the problem
3. if you have the time, it would be awesome if you'd make a pull-request here

### Windows

1. Download Python:
 https://www.python.org/downloads/release/python-2712/

2. .Net Packages
 https://www.microsoft.com/en-US/download/details.aspx?id=49982

 https://www.microsoft.com/en-us/download/details.aspx?id=30653

3. SSL
 https://slproweb.com/products/Win32OpenSSL.html

4. and eventually you also need the Visual Studio, because of the C++ Compiler:
 https://www.visualstudio.com/vs/

 After downloading the Visual Studio make sure to open one time _a new c++ project_.

5. Install the Git-Bash as it comes with a mingw:
 https://git-scm.com/downloads

6. Install NodeJS and the Node Package Manager (NPM)
 https://nodejs.org/en/download/


### Ubuntu

1. Install necessary packages:
```
sudo apt-get update && sudo apt-get upgrade
sudo apt-get install curl git vim build-essential
```

2. Install NodeJS and NPM
```
 curl -sL https://deb.nodesource.com/setup_6.x | sudo -E bash -
 sudo apt-get install -y nodejs
 sudo npm install -g express
```


### Other Necessary Files

Download the Genesis File either from [here](genesis.json) or directly from the [go-ethereum github page](https://github.com/ethereum/go-ethereum#operating-a-private-network). It is advised to take it directly from the official github page, as it is probably more up to date.

## Run the Project

On any OS you need Truffle

```
npm install -g truffle
```

and then **clone this repository**
```
git clone https://github.com/tomw1808/truffle_eth_class1.git
```
and run

```
bower install
```

which installs the angular components.

and then run

```
npm install
```

which installs the node components.

Additionally you need to have a geth node running (or the ethereumjs-testrpc), then you can simply:

```
truffle migrate
```

and

```
truffle build
```

or

```
truffle serve
```

which opens an HTTP Server on http://localhost:8080

## Known Issues

### Error when running truffle test/migrate

If something like this pops up:
```
dependency_path = source.resolve_dependency_path(import_path, dependency_path);
```

or

```
/usr/lib/node_modules/truffle/node_modules/truffle-compile/profiler.js:120
        if (ancestors.length > 0) {
                     ^

TypeError: Cannot read property 'length' of undefined
    at walk_from (/usr/lib/node_modules/truffle/node_modules/truffle-compile/profiler.js:120:22)

```

then try to install truffle 3.1.9:

```
npm install -g truffle@3.1.9
```


