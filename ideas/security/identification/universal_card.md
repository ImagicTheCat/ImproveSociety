
# Current identification methods

Today, a human individual is mostly identified by:
* an identity card, a marked and protected piece of paper
  * name/firstname
  * birth date/location
  * serial number
  * face picture (physical traits)
* a physical address (home)
* human relatives (secondary)

This way of identifying people is not very accurate and can easily be by-passed and produce problems: 
* letter sender is written by the sender itself, easy to usurp
* identifying people is mostly based on human trust, which is not very scalable
* the Id card can be stolen and/or modified without too much difficulties
* identities are valid for a specific administration, if the administration has a failure point, every identities could be usurped

This imply that our needs of identification wasn't very high, because we started from villages, to build cities, located in specific countries, and born related to specific individuals. Now with the increase of population and Internet, the need to build an universal and impersonal identification system is much more present.

# Proposals

## Universal card

* like a credit card
* asymetric encryption (like RSA)
  * the private key, password protected, is written in the card
  * the public key could be "displayed" on the card
* a way to unlock the card (using the password) for the next operation
* not necessarily self powered, can be used as a RFID or an USB
* no framework, no persistent memory
* simple API to generate identification message, get the public key and decrypt/encrypt messages

The private key and the card operation should be written/hard-coded with the most fundamental and complexe to read way. 
The card could be unlocked without regular methods, using a mechanical password.
The card will never directly transmit the password-encrypted private key, every computation is done in the card using the hard-coded circuit.

Failure points (non-exhaustive):
* losing the card loses the identity
* stolen password and card
* identity collision (the identity collision is unlikely and the benefit from this collision would be minor)

In case the card is lost or stolen:
* we could imagine that we know a very costly method to generate a unique private key for each individual (using DNA or something else), so that no one could do it on his own and allowing to recreate a card with a different password with the same identity for the individual
* if the password is also stolen, a unique private key for each individual would offer unlimited usurpation, so it will be better to generate a new card with a new private key, meaning that an administration keeps track of who is who, losing one of the interests to create this card in the first place

## Body chip

Ideally, humans would generate a private key at their birth by themselves, remember it and be able to generate the public key at will. We don't have access (yet) to other minds, but we do have access to our own minds, so it would be one of the best security. Security is only about how hard it is to break something, nothing is unbreakable, but if it's too difficult to do so, we may want to reconsider breaking it.

Instead of a card, placing a chip in the body would prevent the accidental loss of it. The failure point would be to lose the body part where the chip is, increasing the difficulty for someone to steal it considering the consequences.

If we constrain the chip in a vital area, like the brain, which is also defining our individuality, losing the chip could mean to lose life. A second chip, placed in the hand, could communicate with the brain chip for fast practical identification (passing the hand in front of something) and also be used for the chip unlocking mechanism (like a fast complexe hand movement listened by the hand chip and transmitted to the brain chip).

We can imagine a dystopia based on this where people murder others just to access their data, but it is not different from torturing people to make them speak (unless for the capacity to choose what to say, but we can imagine an unlock level for the chip).

# Advantages

Using the card or the chip, having this way of identification would be far more functional than we actually have, if well designed to avoid mass scale failure points.

## Communication / Transactions

Sending letters would be obsolete and communication could be encrypted between every peers.

You could also get rid of the bank system, which is already the case with cryptocurrency.

# NOTE

This is a first draft, clarification and deepening of the ideas is required.
