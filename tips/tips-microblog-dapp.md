# Tips: Microblog Dapp

### Microblog Dapp

This project will build a microblogging **Dapp** (_decentralized application_) using the Ethereum blockchain and the following technologies: `Solidity`, `Ethers.js`, and `Next.js`.

#### Prerequisites

Before you begin, you'll need the following installed:

* _`Node.js`_
* _`npm`_
* _`Truffle`_
* _`Ganache`_
* _`A text editor`_

#### Overview

We will create a microblogging Dapp on the Ethereum blockchain, using Solidity for smart contract development, Ethers.js for interacting with the Ethereum blockchain, and Next.js for the front-end. The goal is to create a decentralized application that allows users to post and read messages.

* **Step 1**: Smart Contract The first step is to create the smart contract that will manage the microblogging functionality. We will use Solidity to write the smart contract. The contract will have the following features:

A `post()` function that allows users to post a message to the microblog.\
A `getPost()` function that allows users to retrieve a post from the microblog.\
A `getPosts()` function that allows users to retrieve all posts from the microblog.

* **Step 2**: Deploy Smart Contract Once the smart contract is written, we need to deploy it to the Ethereum blockchain. We will use Truffle and Ganache to deploy the smart contract.
* **Step 3**: Interact With Smart Contract Once the smart contract is deployed, we need to be able to interact with it. We will use Ethers.js to interact with the smart contract. We will create functions for posting, retrieving, and viewing posts.
* **Step 4**: Create Front-End Finally, we will use Next.js to create the front-end of the application. We will create a simple user interface that allows users to post, view, and read posts.

### Conclusion

In this project, we built a microblogging Dapp on the Ethereum blockchain using Solidity, Ethers.js, and Next.js. The goal was to create a decentralized application that allows users to post and read messages. We created a smart contract, deployed it to the Ethereum blockchain, and wrote functions for interacting with the smart contract. Finally, we created a simple user interface using Next.js.

***

### Frontend (nextjs)

* Posting To post a new post, simply enter your content into the text field and hit the Submit button. Your post will be automatically added to the list of posts.
* Viewing To view your post, simply select it from the list of posts. You will then be able to see the post in markdown format.
* Reading To read a post, simply select it from the list of posts. You will then be able to read the post in markdown format.
