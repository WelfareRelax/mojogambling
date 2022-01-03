# mojogambling

Code in Chialisp that can be used to for instance recreate satoshidice in Chialisp. What is needed is that the solution variables for the spend are announced.
These values can then be asserted by the coin that interacts with this coin, so we can verify that a coin has actually been spent. Kind of like how there is a check in a JackVegas machine, where a game doesn't start without a coin.

In addition we can use the block header and a secret plaintext as a source of randomness and hash the values and cast them to integers. This is done deterministically so the players can verify after the game, that they haven't been cheated by checking the hashes. These values can then be curried in which means that we are pre-commiting to these values so that they can't be changed after. The only values that aren't curried are the ones that we get from our user, which is the puzzlehash and the bet size. Meaning that these values needs to be secured.

There is also another file called listoperations.clsp that contains operations for handling lists, that is to get elements and add elements. The original plan was to combine main.clsp and listoperations.clsp and that this eventually could become a lottery. 
