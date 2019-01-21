<p align="center">
  <img src="https://neo-cdn.azureedge.net/images/neo-logo/144.png" width="144px;" alt="NEO">
</p>

<h3 align="center">NEO Smart Economy Workshop</h3>

# Challenges

You will pick one challenge to solve with your team, if you have any time left then feel free to choose another challenge.

## Challenge 1

```
Challenge: Create your own Hello World contract
Difficulty: Medium
```

Use the [hello world example contract](https://github.com/SmartEconomyWorkshop/workshop/tree/master/examples/1_hello_world) to get an idea about how a contract should look. Now use this concept
to create your own contract, but give it a little twist. Allow users to tell the contract their name, let the contract store the name in the blockchain. Now next time that a user is saying hello
to the contract, it can respond with *Hello Thomas* instead. Use the build_run feature to test you contract before deploying.

* Contract should be deployed on our private net
* Contract should accept at least two commands
* Contract should accept an array of arguments
* Contract should use Storage and CheckWitness API's

## Challenge 2

```
Challenge: Create your own NEP-5.1 token contract
Difficulty: Easy
```

Use the [EUR token contract](https://github.com/SmartEconomyWorkshop/workshop/tree/master/examples/2_token) as an example. Now create your own token. You have to change the name and the ticker
to be unique and you should change the total supply. Read the code to learn how to initialize the token and finish by sending some tokens to other workshop users.

* Contract should be deployed on our private net
* Contract should remain NEP-5.1 compliant, so do not change the basic functions
* On the private net, the contract should be initialized and tokens should be distributed
* You can be creative and add other features to the contract as well

## Challenge 3

```
Challenge: Create a chain of trust contract
Difficulty: Hard
```

For this challenge there is no example, but you can still use the examples of the previous challenges to see how a contract is written. The goal of this contract is to create a chain of trust.
Any user can invoke the contract to claim that they trust another user. If that user is also trusting another user, then you are creating a chain of trust. An off-chain mechanism is
needed to learn about these connections and calculate the amount of vectors and the shortest vector between any two users. You can be creative in adding additional features.

* Contract should be deployed on our private net
* Contract should have several main functions
* Contract should take an array or arguments for each function
* Users should be able to create and delete a trust connection with another user
* CheckWitness should be used to authenticate the user
* Storage should be used to make trust connections available in the blockchain

For bonus points:

Create an event-listener based on [this Python example](https://github.com/CityOfZion/neo-python/blob/master/examples/smart-contract.py) to catch and process events in the smart contract. You could
store the events in a MongoDB database for example.

**Good luck!**
