<!-- Generated by documentation.js. Update this documentation by updating the source code. -->

### Table of Contents

-   [Common][1]
    -   [setChain][2]
    -   [setHardfork][3]
    -   [\_chooseHardfork][4]
    -   [\_getHardfork][5]
    -   [\_isSupportedHardfork][6]
    -   [param][7]
    -   [paramByBlock][8]
    -   [hardforkIsActiveOnBlock][9]
    -   [hardforkGteHardfork][10]
    -   [hardforkIsActiveOnChain][11]
    -   [activeHardforks][12]
    -   [activeHardfork][13]
    -   [hardforkBlock][14]
    -   [isHardforkBlock][15]
    -   [consensus][16]
    -   [finality][17]
    -   [genesis][18]
    -   [hardforks][19]
    -   [bootstrapNodes][20]
    -   [hardfork][21]
    -   [chainId][22]
    -   [chainName][23]
    -   [networkId][24]

## Common

Common class to access chain and hardfork parameters

**Parameters**

-   `chain` **([String][25] \| [Number][26])** String ('mainnet') or Number (1) chain representation
-   `hardfork` **[String][25]** String identifier ('byzantium') for hardfork (optional)
-   `supportedHardforks` **[Array][27]** Limit parameter returns to the given hardforks (optional)

### setChain

Sets the chain

**Parameters**

-   `chain` **([String][25] \| [Number][26])** String ('mainnet') or Number (1) chain representation

### setHardfork

Sets the hardfork to get params for

**Parameters**

-   `hardfork` **[String][25]** String identifier ('byzantium')

### \_chooseHardfork

Internal helper function to choose between hardfork set and hardfork provided as param

**Parameters**

-   `hardfork` **[String][25]** Hardfork given to function as a parameter
-   `onlySupported`  

Returns **[String][25]** Hardfork chosen to be used

### \_getHardfork

Internal helper function, returns the params for the given hardfork for the chain set

**Parameters**

-   `hardfork` **[String][25]** Hardfork name

Returns **Dictionary** 

### \_isSupportedHardfork

Internal helper function to check if a hardfork is set to be supported by the library

**Parameters**

-   `hardfork` **[String][25]** Hardfork name

Returns **[Boolean][28]** True if hardfork is supported

### param

Returns the parameter corresponding to a hardfork

**Parameters**

-   `topic` **[String][25]** Parameter topic ('gasConfig', 'gasPrices', 'vm', 'pow', 'casper', 'sharding')
-   `name` **[String][25]** Parameter name (e.g. 'minGasLimit' for 'gasConfig' topic)
-   `hardfork` **[String][25]** Hardfork name, optional if hardfork set

### paramByBlock

Returns a parameter for the hardfork active on block number

**Parameters**

-   `topic` **[String][25]** Parameter topic
-   `name` **[String][25]** Parameter name
-   `blockNumber` **[Number][26]** Block number

### hardforkIsActiveOnBlock

Checks if set or provided hardfork is active on block number

**Parameters**

-   `hardfork` **[String][25]** Hardfork name or null (for HF set)
-   `blockNumber` **[Number][26]** 
-   `opts` **[Array][27]** 
    -   `opts.onlySupported` **Array.Boolean** optional, only allow supported HFs (default: false)

Returns **[Boolean][28]** 

### hardforkGteHardfork

Sequence based check if given or set HF1 is greater than or equal HF2

**Parameters**

-   `hardfork1` **[Number][26]** Hardfork name or null (if set)
-   `hardfork2` **[String][25]** Hardfork name
-   `opts` **[Array][27]** 
    -   `opts.onlyActive` **Array.Boolean** optional, only active HFs (default: false)
    -   `opts.onlySupported` **Array.Boolean** optional, only allow supported HFs (default: false)

Returns **[Boolean][28]** 

### hardforkIsActiveOnChain

Checks if given or set hardfork is active on the chain

**Parameters**

-   `hardfork` **[String][25]** Hardfork name, optional if HF set
-   `opts` **[Array][27]** 
    -   `opts.onlySupported` **Array.Boolean** optional, only allow supported HFs (default: false)

Returns **[Boolean][28]** 

### activeHardforks

Returns the active hardfork switches for the current chain

**Parameters**

-   `blockNumber` **[Number][26]** up to block if provided, otherwise for the whole chain
-   `opts` **[Array][27]** 
    -   `opts.onlySupported` **Array.Boolean** optional, limit results to supported HFs (default: false)

Returns **[Array][27]** Array with hardfork arrays

### activeHardfork

Returns the latest active hardfork name for chain or block or throws if unavailable

**Parameters**

-   `blockNumber` **[Number][26]** up to block if provided, otherwise for the whole chain
-   `opts` **[Array][27]** 
    -   `opts.onlySupported` **Array.Boolean** optional, limit results to supported HFs (default: false)

Returns **[String][25]** Hardfork name

### hardforkBlock

Returns the hardfork change block for hardfork provided or set

**Parameters**

-   `hardfork` **[String][25]** Hardfork name, optional if HF set

Returns **[Number][26]** Block number

### isHardforkBlock

True if block number provided is the hardfork (given or set) change block of the current chain

**Parameters**

-   `blockNumber` **[Number][26]** Number of the block to check
-   `hardfork` **[String][25]** Hardfork name, optional if HF set

Returns **[Boolean][28]** 

### consensus

Provide the consensus type for the hardfork set or provided as param

**Parameters**

-   `hardfork` **[String][25]** Hardfork name, optional if hardfork set

Returns **[String][25]** Consensus type (e.g. 'pow', 'poa')

### finality

Provide the finality type for the hardfork set or provided as param

**Parameters**

-   `hardfork` **[String][25]** Hardfork name, optional if hardfork set

Returns **[String][25]** Finality type (e.g. 'pos', null of no finality)

### genesis

Returns the Genesis parameters of current chain

Returns **Dictionary** Genesis dict

### hardforks

Returns the hardforks for current chain

Returns **[Array][27]** Array with arrays of hardforks

### bootstrapNodes

Returns bootstrap nodes for the current chain

Returns **Dictionary** Dict with bootstrap nodes

### hardfork

Returns the hardfork set

Returns **[String][25]** Hardfork name

### chainId

Returns the Id of current chain

Returns **[Number][26]** chain Id

### chainName

Returns the name of current chain

Returns **[String][25]** chain name (lower case)

### networkId

Returns the Id of current network

Returns **[Number][26]** network Id

[1]: #common

[2]: #setchain

[3]: #sethardfork

[4]: #_choosehardfork

[5]: #_gethardfork

[6]: #_issupportedhardfork

[7]: #param

[8]: #parambyblock

[9]: #hardforkisactiveonblock

[10]: #hardforkgtehardfork

[11]: #hardforkisactiveonchain

[12]: #activehardforks

[13]: #activehardfork

[14]: #hardforkblock

[15]: #ishardforkblock

[16]: #consensus

[17]: #finality

[18]: #genesis

[19]: #hardforks

[20]: #bootstrapnodes

[21]: #hardfork

[22]: #chainid

[23]: #chainname

[24]: #networkid

[25]: https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/String

[26]: https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Number

[27]: https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Array

[28]: https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Boolean