Hello! Thank you for taking the time to interview with us.

# Details

Work on this by yourself, in an environment representative of your regular work environment.  Treat this like a regular work assignment: manage your time judiciously.

Please use javascript as your primary language for implementation. You are free to use whatever tools and frameworks you wish, provided that we are able to build, run, and test your solution. You may also use whatever external resources you wish, provided that the work you submit is your own.

There are both required tasks and bonus tasks. Complete as much as you can, but don't worry if you don't finish any bonus tasks.

## Confidentiality

Please keep this challenge and your solution to yourself. If you push your solution to a remote repository, please make sure that the repository is private.

# Prompts

## Part 1: Required

### Background

[A simple definition of a blockchain](https://bitsonblocks.net/2015/09/09/gentle-introduction-blockchain-technology/): "a blockchain system is a package which contains a normal database plus some software that adds new rows, validates that new rows conform to pre-agreed rules, and listens and broadcasts new rows to its peers across a network, ensuring that all peers have the same data in their databases." Except, in a blockchain data isn't organized into rows, it is organized into blocks.

Blocks contain data about new transactions that are being validated on the blockchain, data necessary for understanding the state of the blockchain at the time the block was created, and data necessary for adding and validating future blocks.

### Task: A Block History List App

Your task is to implement an app that retrieves and displays a list of data about recent blocks on the Ethereum blockchain.

You have to set up both a front end UI and a backend server.

The backend server should be responsible for:

- Retrieving data about the latest block from a third party api (more details below).
- Storing that data in a database. We encourage you to use the simplest possible database necessary to get the app to work.
- Expose a HTTP API for retrieving blocks. The API should be capable of returning a list of all blocks in the database.
- Periodically checking the third-party API for a new latest block and updating the database accordingly.

The frontend UI should retrieve the block from the server and show information about them in a list to the user. 
- The user should see information for the latest block when first loading the app.
- The user should see new blocks added to the list periodically. Roughly 20 seconds is a good interval.
- Each item in the list should include the follow data fields for its respective block: `size`, `number`, `timestamp`, `nonce`, `gasLimit`, `hash`
  - Each item in the list should include a label and value for each of these pieces of data.

#### Retrieving Data About Latest Blocks

You can retrieve data about recent blocks using the `getBlockByNumber` method that is callable via Infura's API, described here: https://infura.io/docs/ethereum/json-rpc/eth_getBlockByNumber

- This API will return a new result for `getBlockByNumber` every 10-20 seconds.
- You can use `9d1b5930f82f479d89cf87310d59b51b` as `YOUR-PROJECT-ID`.
- Please consult the above link for more details.

#### Basic UI Example

A very simple UI for the list might look like:

![](https://i.imgur.com/3zXOOrP.png)

## Part 2: Bonus Tasks

If you finish [Part 1](#part-1-required) in under 6 hours, please complete as many of the following additions to your app as you can. Correctly implementing Part 1 is more important than completing any bonus tasks.

Please complete these tasks in the order provided. Do A before B, B before C, etc.

- **A.** Persist your data so that blocks are shown on refreshing or after opening and closing the app.
- **B.** Provide buttons or a dropdown selection menu that allows the user to sort the list by field. Sorting can be alphanumeric. Allow the user to select both descending and ascending sorts. If the list is currently sorted according to one of the fields, and a new block is added to the list, ensure it is added in corrected sorted order.
- **C.** Allow the user to delete blocks from the list. Allow them to delete the whole list at once or one block at a time.
- **D.** For the `size`, `number` and `gasLimit` fields of each block, show the user those values as decimal numbers when they are clicked. Allow the user to toggle back and forth between decimal and hexadecimal numbers with successive taps.
- **E.** For the `timestamp` field, show it as a human readable date and time when it is clicked. Allow the user to toggle back and forth with successive taps.
- **F.** Make whatever UI improvements you can to ensure a nice visual presentation and pleasant experience for users.

## Submission Instructions

You should aim to finish within 10-12 hours of receiving this gist. These are open-ended problems, don't worry if what you submitted doesn't feel done. If you need a little extra time to make finishing touches, that's fine.

**(1)** If you have not already done so, create a git repository and commit your work

- Initialize a git repository
```
 git init
```
- Create a `.gitignore` file and remove dependency files or others we do not need to build, run and test the project from git
- Commit your work

**(2)** Bundle your git repo

```
git bundle create wifisoft-challenge.bundle HEAD
```
**(3)** E-mail your `wifisoft-challenge.bundle` file to m.igbinedion@gmail.com

------------------------------------------------

Have fun, and write some beautiful code!

Regards