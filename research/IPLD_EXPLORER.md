# IPLD Explorers

**Abstract**: IPLD is the underlying data structure for IPFS. It is a huge hash-linked directed acyclic graph, with all files, git repos, blockchains, etc., within it. IPLD is the heart of IPFS. The tooling for manipulating IPLD directly has recently landed into both go-ipfs and js-ipfs under the API/commands `ipfs dag`. What we need next is to be able to make it nicer for humans to interact with IPLD directly. For this purpose, we have a few different "graph explorers" in mind. You can think of them similar to a visual explorer for a git repo (eg rendering the commit graph), or file explorers, or blockchain explorers. We aim to create several graph explorers, (1) one based on a traditional programming REPL, (2) another based on JSON tree explorers, (3) another based on a column-based tree viewer, (4) and a graphical version using d3 graph plotting, and (5) one in 3D which allows VR exploration.

### Table of Contents
* [Introduction](#introduction)                                                                                                                                                                                                                     
* [Explorers](#explorers)                                                                                                                                                                                                                           
    * [Explorer 1. IPLD REPL](#explorer-1-ipld-repl)                                                                                                                                                                                                
    * [Explorer 2. tree explorers](#explorer-2-tree-explorers)                                                                                                                                                                                      
    * [Explorer 3. column-based viewer](#explorer-3-column-based-viewer)                                                                                                                                                                            
    * [Explorer 4. graphical version](#explorer-4-graphical-version)                                                                                                                                
      * [D3](#d3)                                                                                                                                                                                                                                     
          * [D3: Quick Introduction](#d3-quick-introduction)                                                                                                                                                                                          
          * [D3: Prior Art in IPFS Ecosystem](#d3-prior-art-in-ipfs-ecosystem)                                                                                                                                                                        
      * [GraphViz](#graphviz)                                                                                                                                                                                                      
          * [Dot: Prior Art in IPFS Ecosystem](#dot-prior-art-in-ipfs-ecosystem)                                                                                                                                                                      
          * [GraphViz in D3](#graphviz-in-d3)                                                                                                                                                                                                         
    * [Explorer 5. 3D VR Explorer](#explorer-5-3d-vr-explorer)                                                                                                                                                                                      
* [How to Implement](#how-to-implement)                                                                                                                                                                                                             
    * [Path in the anchor and history](#path-in-the-anchor-and-history)                                                                                                                                                                             
    * [Navigation path](#navigation-path)                                                                                                                                                                                                           
* [Relevant API](#relevant-api)                                                                                                                                                                                                                     
    * [Example: ipfs.dag.ls](#example-ipfsdagls)                                                                                                                                                                                                    
    * [Example: ipfs.dag.tree](#example-ipfsdagtree)                                                                                                                                                                                                
    * [Example: ipfs.dag.get](#example-ipfsdagget)

## Introduction

To learn more about IPLD, please check out:

- https://github.com/ipld/ipld
- https://github.com/ipld/cid
- [IPLD: Enter the Merkle Forest](https://www.youtube.com/watch?v=Bqs_LzBjQyk) - conceptual talk from @jbenet
- [IPFS, IPLD, Blockchain Fun](https://www.youtube.com/watch?v=bi-4YGZXxwA&t=333s) - demo talk from @whyrusleeping
- http://ipld.io/ 
  - website is outdated and will change soon to reflect important API changes, but explains the ideas ok. Talks may be better.

**The ["Relevant API" section in this document](#relevant-api) gives examples on ipfs node calls to make.**

## Explorers

### Explorer 1. IPLD REPL

![](https://binary-studio.com/wp-content/uploads/2015/05/node-repl.png)

Examples:
- `node`
- https://repl.it/languages/javascript
- https://binary-studio.com/wp-content/uploads/2015/05/node-repl.png


The first idea is to part from a very simple REPL. The REPL would be primarily about hashes and content. It would have a few "builtin" functions:

- `resolve(<path>)` - walk down a path and return the object found there
- `ls(<path>)` - list the entries in a path
- `tree(<path>, <depth>)` - list all entries starting from path, and up to `<depth>` graph depth. (may be useful)
- `get(<path>)` - walks down a path and returns that path

Entering `<path>` is the equivalent of `get <path>`, and every non-path value is added to ipfs, hashed, and its CID is returned.

A more advanced version would allow:

- `eval(<path>)`, which would load the value at `<path>`, interpret it as javascript, and eval it, adding it to the current context \o/.

### Explorer 2. tree explorers

![](http://www.webandsay.com/images/json-diff-released/jsondiff.png)

Examples:
- https://shrimpworks.za.net/assets/projects/json-explorer/jsonex.png
- http://www.webandsay.com/images/json-diff-released/jsondiff.png
- http://visualizer.json2html.com/
- http://www.jsoneditoronline.org/

Structured explorers:
- https://blockexplorer.com/block/00000000000000000156c68693b097733b83084f327a10a591948b9dec54032e
- https://explorer.zcha.in/blocks/000000006263c2e8a35c0e950f5d139be1b6060554895f4327c81db4b1f00813


The tree explorer builds a very similar editor to traditional JSON tree explorers. This may be overkill for now.



### Explorer 3. column-based viewer

![](https://i.stack.imgur.com/j1v4A.jpg)

File browsers / explorers:
- https://en.wikipedia.org/wiki/File_manager
- https://tawus.files.wordpress.com/2011/08/filebrowser.png
- https://i.stack.imgur.com/j1v4A.jpg <-- columns

The column-based file system exploration fits our graphs very well, as well. This sould perhpas be the easiest to get working well. There's many examples and libraries out there.


### Explorer 4. graphical version

- https://camo.githubusercontent.com/23d4bbfccd8aeb42dc9374827d364707c0e17981/68747470733a2f2f7261772e6769746875622e636f6d2f6b6573736c65722f7374617469632f6d61737465722f6e6f64652d6a736f6e2d6578706c6f7265722e706e67


#### D3

D3 was already used in some of [our prior art](https://github.com/ipfs-shipyard/pm-ipfs-gui/blob/master/proj-descriptions/IPLD_EXPLORER.md#explorer-4-graphical-version-using-d3-graph-plotting) and probably will end up using it directly or indirectly. 

Open technical questions that probably do not belong to design discussion: what will be the data format? should D3 be used in raw form, or via a library? are there any alternatives to D3 ecosystem?
We will answer them during the implementation, raising them here just for the record.

##### D3: Quick Introduction

D3→Shapes→Links:  https://github.com/d3/d3-shape#links  
Live demo with annotated sources:  https://bl.ocks.org/mbostock/4339184

##### D3: Prior Art in IPFS Ecosystem

This version visualizes the IPLD graph using d3:

![old ipfs dataviz demo](https://camo.githubusercontent.com/bee179fc7d2635f40607516ed1402533b67a8d05/68747470733a2f2f63646e2e7261776769742e636f6d2f697066732f6461746176697a2f363032316365613765343932323462316261623738346365303465366566373031396265363235622f776562617070732f747265652d6c74722f646f632f697066732d636f72652e706e67)

[ipfs dataviz](https://github.com/ipfs/dataviz) is currently working, and showing _files_. It should also show _the raw data_. Now that IPLD is out, the project could be updated. Though because having access to the file graph is useful, we may want to copy the visualization and remix it to navigate on nodes, instead of files.

Live Demo: https://ipfs.io/ipfs/QmX5smVTZfF8p1VC8Y3VtjGqjvDVPWvyBk24JgvnMwHtjC/viz#QmX5smVTZfF8p1VC8Y3VtjGqjvDVPWvyBk24JgvnMwHtjC

![screenshot-2018-3-29 http 127 0 0 1 1](https://user-images.githubusercontent.com/157609/38059257-03499c82-32e6-11e8-834b-b42000587518.png)

Dead Demo (trying to load big flat directory with XKCD archive): https://ipfs.io/ipfs/QmX5smVTZfF8p1VC8Y3VtjGqjvDVPWvyBk24JgvnMwHtjC/viz#Qmb8wsGZNXt5VXZh1pEmYynjB6Euqpq3HYyeAdw2vScTkQ

Given enough time it will eventually render [this mess](https://user-images.githubusercontent.com/157609/38059146-a7eb3b2a-32e5-11e8-8abe-1c2b976a61c5.png).

#### GraphViz

(Does not really support dynamic transformations in web browser, but mentioning it for the record)  
Why mentioning GraphViz and Dot format? People can easily reuse it in papers, publications etc. 

##### Dot: Prior Art in IPFS Ecosystem

Prior art exists in IPFS ecosystem, see notes on [Graphing Objects](https://ipfs.io/ipfs/QmYNQJoKGNHTpPxCBPh9KkDpaExgd2duMa3aF6ytMpHdao/docs/examples/example-viewer/example#../graphmd/README.md):

![graph](https://user-images.githubusercontent.com/157609/38058901-cc854cd8-32e4-11e8-89bd-228ecc3ef0a6.png)


##### GraphViz in D3

Web Version implemented in D3 exists: https://github.com/mstefaniuk/graph-viz-d3-js


Examples: 
- http://graphviz.it/#/gallery/unix.gv
- http://graphviz.it/#/gallery/records.gv




### Explorer 5. 3D VR Explorer

Blockchain explorers:
- in 3d: https://www.youtube.com/watch?v=3ujUIz9hQ7c
- http://www.bitcoinlinks.net/files/styles/card_image__320x240_/public/img/bitbonkers_0.png?itok=2vKUm481

This explorer is a native way to look at the bitcoin blockchain; it's just done on a 3D environment! This is possibly super cool, but we'd love to let users navigate and explore, jumping from block to block.

![](https://acom.azurecomcdn.net/80C57D/cdn/mediahandler/acomblog/media/Default/blog/iStock_000004202329_092215.jpg)

![](http://i.imgur.com/q9uOXm8.jpg)

![](https://i.ytimg.com/vi/E3q0wbNKmkQ/maxresdefault.jpg)

## How to Implement


All of these explorers do one thing: traverse the graph. Therefore, we only need a couple of api calls to do this: `ipfs.dag.ls`, and `ipfs.dag.get`. See more in the [Relevant API](#relevant-api) section below.


### Path in the anchor and history

All explorers have to do with a given path. It is important to keep this path in the hash/anchor of the html page, as we want to be able to link to exact locations in the graph.


### Navigation path

Another thing all explorers track is navigation path. While this may be multiple nodes open in some explorers, it is enough to keep track of a single string path for the others. It would be useful if this navigation path is also given through the URL bar, so that people can link each other to the exact same location and "path used to get there". 


## Relevant API

All of the explorers here will use the following api calls:

- `ipfs.dag.ls`
- `ipfs.dag.get` 

See [the DAG API](https://github.com/ipfs/interface-ipfs-core/tree/master/API/dag#dagget), which works in both js-ipfs and js-ipfs-api.

### Example: `ipfs.dag.ls`

```js
var IPFSAPI = require('ipfs-api')
var ipfs = IPFSApi('/ip4/127.0.0.1/tcp/5001')

// given an object such as: 
//
// var obj = {
//     "a": 1,
//     "b": [1, 2, 3],
//     "c": {
//         "ca": [5, 6, 7],
//         "cb": "foo"
//     }
// }
// 
// ipfs.dag.put(obj, function(err, cid2) {
//     assert(cid == zdpuAkxd9KzGwJFGhymCZRkPCXtBmBW7mB2tTuEH11HLbES9Y)
// })

ipfs.dag.ls('zdpuAkxd9KzGwJFGhymCZRkPCXtBmBW7mB2tTuEH11HLbES9Y', function(err, result) {
    for (var i in result.entries) {
        console.log(result.entries[i])
    }
})
// Returns:
// a
// b
// c

ipfs.dag.ls('zdpuAkxd9KzGwJFGhymCZRkPCXtBmBW7mB2tTuEH11HLbES9Y/c', function(err, result) {
    for (var i in result.entries) {
        console.log(result.entries[i])
    }
})
// Returns:
// ca
// cb

ipfs.dag.ls('zdpuAkxd9KzGwJFGhymCZRkPCXtBmBW7mB2tTuEH11HLbES9Y/c/ca', function(err, result) {
    for (var i in result.entries) {
        console.log(result.entries[i])
    }
})
// Returns:
// 0
// 1
// 2
```

### Example: `ipfs.dag.tree`

```js
var IPFSAPI = require('ipfs-api')
var ipfs = IPFSApi('/ip4/127.0.0.1/tcp/5001')

// given an object such as: 
//
// var obj = {
//     "a": 1,
//     "b": [1, 2, 3],
//     "c": {
//         "ca": [5, 6, 7],
//         "cb": "foo"
//     }
// }
// 
// ipfs.dag.put(obj, function(err, cid2) {
//     assert(cid == zdpuAkxd9KzGwJFGhymCZRkPCXtBmBW7mB2tTuEH11HLbES9Y)
// })

ipfs.dag.tree('zdpuAkxd9KzGwJFGhymCZRkPCXtBmBW7mB2tTuEH11HLbES9Y', function(err, result) {
    for (var i in result) {
        console.log(result[i])
    }
})
// Returns:
// a
// b
// b/0
// b/1
// b/2
// c
// c/ca
// c/ca/0
// c/ca/1
// c/ca/2
// c/cb

ipfs.dag.tree('zdpuAkxd9KzGwJFGhymCZRkPCXtBmBW7mB2tTuEH11HLbES9Y/c', function(err, result) {
    for (var i in result) {
        console.log(result[i])
    }
})
// Returns:
// ca
// ca/0
// ca/1
// ca/2
// cb
```


### Example: `ipfs.dag.get`

```js
var IPFSAPI = require('ipfs-api')
var ipfs = IPFSApi('/ip4/127.0.0.1/tcp/5001')

// given an object such as: 
//
// var obj = {
//     "a": 1,
//     "b": [1, 2, 3],
//     "c": {
//         "ca": [5, 6, 7],
//         "cb": "foo"
//     }
// }
// 
// ipfs.dag.put(obj, function(err, cid2) {
//     assert(cid == zdpuAkxd9KzGwJFGhymCZRkPCXtBmBW7mB2tTuEH11HLbES9Y)
// })

function errOrLog(err, result) {
    if (err) console.error('error: ' + err)
    else console.log(result)
}

ipfs.dag.get('zdpuAkxd9KzGwJFGhymCZRkPCXtBmBW7mB2tTuEH11HLbES9Y/a', errOrLog)
// Returns:
// 1

ipfs.dag.get('zdpuAkxd9KzGwJFGhymCZRkPCXtBmBW7mB2tTuEH11HLbES9Y/b', errOrLog)
// Returns:
// [1, 2, 3]

ipfs.dag.get('zdpuAkxd9KzGwJFGhymCZRkPCXtBmBW7mB2tTuEH11HLbES9Y/c', errOrLog)
// Returns:
// {
//   "ca": [5, 6, 7],
//   "cb": "foo"
// }

ipfs.dag.get('zdpuAkxd9KzGwJFGhymCZRkPCXtBmBW7mB2tTuEH11HLbES9Y/c/ca/1', errOrLog)
// Returns:
// 6
```
