# Overview

<div style="text-align: center">

[![Java CI with Gradle](https://github.com/astrapi69/tree-api/actions/workflows/gradle.yml/badge.svg)](https://github.com/astrapi69/tree-api/actions/workflows/gradle.yml)
[![Open Issues](https://img.shields.io/github/issues/astrapi69/tree-api.svg?style=flat)](https://github.com/astrapi69/tree-api/issues)
[![Maven Central](https://maven-badges.herokuapp.com/maven-central/io.github.astrapi69/tree-api/badge.svg)](https://maven-badges.herokuapp.com/maven-central/io.github.astrapi69/tree-api)
[![Javadocs](http://www.javadoc.io/badge/io.github.astrapi69/tree-api.svg)](http://www.javadoc.io/doc/io.github.astrapi69/tree-api)
[![MIT License](http://img.shields.io/badge/license-MIT-brightgreen.svg?style=flat)](http://opensource.org/licenses/MIT)
[![Donate](https://img.shields.io/badge/donate-❤-ff2244.svg)](https://www.paypal.com/cgi-bin/webscr?cmd=_s-xclick&hosted_button_id=GVBTWLRAZ7HB8)
[![Hits Of Code](https://hitsofcode.com/github/astrapi69/tree-api?branch=develop)](https://hitsofcode.com/github/astrapi69/tree-api/view?branch=develop)
[![Lines Of Code](https://tokei.rs/b1/github/astrapi69/tree-api)](https://github.com/astrapi69/tree-api)

</div>

## Tree Data Structure Overview

A **tree** is a hierarchical data structure made up of nodes, starting from a root node and branching out into subnodes.
Each node contains a value and can have multiple children, with the rule that no child points back to the root or shares
any duplicate connections. This structure forms a recursive, non-linear representation of data, ideal for modeling
hierarchical relationships.

**Key Terminology:**

* **Node**: A single element in the tree.
* **Edge**: A connection between two nodes.
* **Root**: The topmost node with no parent.
* **Parent**: A node connected to one or more successors.
* **Child**: A successor node connected to its parent.
* **Leaf**: A node without children.
* **Path**: The sequence of nodes connecting one node to another.
* **Height**: The number of edges between a node and its furthest descendant.
* **Depth**: The number of edges between the root and a specific node.
* **Sibling**: Nodes that share the same parent.
* **Subtree**: A node and all of its descendants.

**Tree Traversal Methods:**

* **Pre-order**: Visit the current node, then recursively traverse its subtrees from left to right.
* **Post-order**: Recursively traverse each subtree from left to right, visiting the current node last.

**Tree Representation Methods:**

1. **Array-of-Pointers**: Each node holds an array of references to its children. This allows quick access to any child
   but can be inefficient if many pointers are null.
2. **Leftmost-Child—Right-Sibling**: Each node points to its leftmost child and right sibling, providing an efficient
   way to traverse through siblings.

**Expression Trees:**
Expression trees represent mathematical expressions in a structured way, where operators and operands are arranged to
clarify precedence. Traversing this tree using pre-order or post-order traversal helps evaluate or transform the
expressions into infix, prefix, or postfix forms.

**Structural Induction:**
A method for proving the correctness of tree-related algorithms. It involves proving a base case (a tree with a single
node) and then showing the correctness of the recursive case (a tree with subtrees).

## ITree Interface Overview

The `ITree<V, T>` interface provides a generic structure for representing trees where each node can hold a value of type
`V` and have children of type `T`. This flexible design allows for building complex hierarchical models while keeping
the structure modular and reusable.

### Key Features of the ITree Interface:

* **Node Management**: Add, remove, and manage children of a node.
* **Tree Traversal**: Traverse nodes in pre-order and post-order, ensuring each node is visited systematically.
* **Sibling Navigation**: Access sibling nodes in relation to their parent node.
* **Parent-Child Relationships**: Easily navigate between parent and child nodes, and determine the depth and level of
  nodes in the tree.

> Please support this project by simply putting a Github <a class="github-button" href="https://github.com/astrapi69/tree-api" data-icon="octicon-star" aria-label="Star astrapi69/tree-api on GitHub">
> Star ⭐</a>
>
> Share this library with friends on Twitter and everywhere else you can
>
> If you love this project
> [![Donation](https://img.shields.io/badge/donate-❤-ff2244.svg)](https://www.paypal.com/cgi-bin/webscr?cmd=_s-xclick&hosted_button_id=GVBTWLRAZ7HB8)

## Note

No animals were harmed in the making of this library.

## License

The source code comes under the liberal MIT License, making tree-api great for all types of applications.

## gradle dependency

Replace the variable ${latestVersion} with the current latest version: [![Maven Central](https://maven-badges.herokuapp.com/maven-central/io.github.astrapi69/tree-api/badge.svg)](https://maven-badges.herokuapp.com/maven-central/io.github.astrapi69/tree-api)

You can first define the version in the ext section and add than the following gradle dependency to
your project `build.gradle` if you want to import the core functionality of tree-api:

define version in file gradle.properties

```
treeApiVersion=${latestVersion}
```

or in build.gradle ext area

```
    treeApiVersion = "${latestVersion}"
```

then add the dependency to the dependencies area

```
    implementation("io.github.astrapi69:tree-api:$treeApiVersion")
```

## Maven dependency

Maven dependency is now on sonatype.
Check out [sonatype repository](https://oss.sonatype.org/index.html#nexus-search;gav~io.github.astrapi69~tree-api~~~) for latest snapshots and releases.

Add the following maven dependency to your project `pom.xml` if you want to import the core
functionality of tree-api:

Then you can add the dependency to your dependencies:

    <properties>
            ...
        <!-- tree-api version -->
        <tree-api.version>${latestVersion}</tree-api.version>
            ...
    </properties>
            ...
        <dependencies>
            ...
            <!-- tree-api DEPENDENCY -->
            <dependency>
                <groupId>io.github.astrapi69</groupId>
                <artifactId>tree-api</artifactId>
                <version>${tree-api.version}</version>
            </dependency>
            ...
        </dependencies>

# Donations

This project is kept as an open source product and relies on contributions to remain being
developed. If you like this library, please consider a donation

over paypal:
<br>
<br>
<a href="https://www.paypal.com/cgi-bin/webscr?cmd=_s-xclick&hosted_button_id=MJ7V43GU2H386" target="_blank">
    <img src="https://www.paypalobjects.com/en_US/GB/i/btn/btn_donateCC_LG.gif"
        alt="PayPal this"
        title="PayPal – The safer, easier way to pay online!"
        style="border: none" />
</a>
<br>
<br>
or over bitcoin(BTC) with this address:

bc1ql2y99q7e8psndhcc3gferk03esw3qqf677rhjy

<img src="https://github.com/astrapi69/jgeohash/blob/master/src/main/resources/img/bc1ql2y99q7e8psndhcc3gferk03esw3qqf677rhjy.png"
alt="Donation Bitcoin Wallet" width="250"/>

or over FIO with this address:

FIO7tFMUVAA9cHiPPqKMfMXiSxHrbpiFyRYqTketNuM67aULuwjop

<img src="https://github.com/astrapi69/jgeohash/blob/master/src/main/resources/img/FIO7tFMUVAA9cHiPPqKMfMXiSxHrbpiFyRYqTketNuM67aULuwjop.png"
alt="Donation FIO Wallet" width="250"/>

or over Ethereum(ETH) with:

0xc057D159D3C8f3311E73568b334FF6fE82EB2b7D

<img src="https://github.com/astrapi69/jgeohash/blob/master/src/main/resources/img/0xc057D159D3C8f3311E73568b334FF6fE82EB2b7D.png"
alt="Donation Ethereum Wallet" width="250"/>

or over Ethereum Classic(ETC) with:

0xF708cA86D86C246B69c3F4BAe431eBbe0c2bfddD

<img src="https://github.com/astrapi69/jgeohash/blob/master/src/main/resources/img/0xF708cA86D86C246B69c3F4BAe431eBbe0c2bfddD.png"
alt="Donation Ethereum Classic Wallet" width="250"/>

or over Dogecoin(DOGE) with:

D5yi4Um8cpakd6yPRm2hGWuQ5nrVzhSSW1

<img src="https://github.com/astrapi69/jgeohash/blob/master/src/main/resources/img/D5yi4Um8cpakd6yPRm2hGWuQ5nrVzhSSW1.png"
alt="Donation Dogecoin Wallet" width="250"/>

or over Monero(XMR) with:

49bqeRQ7Bf49oJFVC72pqpe5hFbb62pfXDYPdLsadGGF81KZW2ZfrPZ8PbAVu5X2v1TYAspeczMya3cYQysNS4usRRPQHVw

<img src="https://github.com/astrapi69/jgeohash/blob/master/src/main/resources/img/49bqeRQ7Bf49oJFVC72pqpe5hFbb62pfXDYPdLsadGGF81KZW2ZfrPZ8PbAVu5X2v1TYAspeczMya3cYQysNS4usRRPQHVw.png"
alt="Donation Monero Wallet" width="250"/>

or over flattr:

<a href="https://flattr.com/submit/auto?fid=r7vp62&url=https%3A%2F%2Fgithub.com%2Fastrapi69%2Ftree-api" target="_blank">
<img src="http://api.flattr.com/button/flattr-badge-large.png" alt="Flattr this" title="Flattr this" style="border: none" />
</a>

or over the donation buttons at the top.

## Semantic Versioning

The versions of tree-api are maintained with the Semantic Versioning guidelines.

Release version numbers will be incremented in the following format:

`<major>.<minor>.<patch>`

For detailed information on versioning you can visit the [wiki page](https://github.com/lightblueseas/mvn-parent-projects/wiki/Semantic-Versioning).

## What can i do to support this project

You can donate or contribute solve issues or pull request. Every support are welcome.

## Want to Help and improve it? ###

The source code for tree-api are on GitHub. Please feel free to fork and send pull requests!

Create your own fork of [astrapi69/tree-api/fork](https://github.com/astrapi69/tree-api/fork)

To share your changes, [submit a pull request](https://github.com/astrapi69/tree-api/pull/new/develop).

Don't forget to add new units tests on your changes.

## Contacting the Developers

Do not hesitate to contact the tree-api developers with your questions, concerns, comments, bug reports, or feature requests.
- Feature requests, questions and bug reports can be reported at the [issues page](https://github.com/astrapi69/tree-api/issues).

## Similar projects

## Credits
