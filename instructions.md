# HackJack

Grab your deck and start hacking.

# Overview

Hackjack is a two player hacking-themed card game played with a standard 52-card poker deck.

1. Divide the deck into red and black cards.
2. Both players strategically set up their `servers` and `attack decks`.
3. Decide which player goes first with a `ping test`.
4. Players alternate taking `turns` of one or more `moves` until a player wins by downloading both of their oppenent's `target cards`.

# Divide the Deck

1. Player 1 takes all the red cards: hearts and diamonds.
2. Player 2 takes all the black cards: clubs and spades.

# Server Setup

Both players plan and build their `server`.

1. Place both of your `target cards` and any three of your `program cards` face down to form the `data layer`.
2. Place any five `data cards` face down to form the `encryption layer`.
3. Place any six `data cards` face down to form the `firewall layer`.

The remaining 10 cards form your `attack deck`. This deck will contain `program cards` and `data cards` but no `target cards`

```
Server Layout

= player 1 =

 🂠 🂠 🂠 🂠 🂠             ← data layer
 🂠 🂠 🂠 🂠 🂠   [upload]  ← encryption layer
🂠 🂠 🂠 🂠 🂠 🂠            ← firewall layer

🂠 🂠 🂠 🂠 🂠 🂠            ← firewall layer
 🂠 🂠 🂠 🂠 🂠   [upload]  ← encryption layer
 🂠 🂠 🂠 🂠 🂠             ← data layer

= player 2 =
```

# Ping Test

1. Each player chooses and reveals a random card from their opponents `attack deck`.
2. The player that _owns_ the lower card will go first. In the event of a tie, repeat the ping test.
3. Return the cards to the `attack decks`.

# Turns

The player who won the ping test goes first. Players alternate turns until either player wins by collecting both of their opponents `target cards`.

[introduce `attacker` and `defender`]

If the `attacker` does not have any cards in their `attack deck` at the beginning of their turn, they add all the cards in their discord pile to their `attack deck`.

Each `turn` consists of one or more `moves`. The player MUST make a move.

IF the attacker removes a card from the defender's server during their move AND they have at least one card in their `attack deck` THEN they MUST make another move. Otherwise, their turn is over. An attacker might make several moves in a single turn.

# Moves

### Attack Firewall

IF the `attacker` has at least one `data card` in their `attack deck`  
AND there is at least one card in the defender's `firewall layer`  
THEN the `attacker` MAY attack the firewall layer.

1. The `attacker` places a `data card` from their `attack deck` face up below a card in the `defender's` `firewall layer`.
2. The attacker `reveals` the firewall card, if it is not already `revealed`.
3. IF the attack card value is higher than the firewall card value  
   THEN both cards are `removed`  
   ELSE the attack card is `held` and it's value will be added to future attacks on the same firewall card.

### Attack Encryption Layer

IF the `attacker` has at least one `data card` in their `attack deck`  
AND there is at least one `exposed` card in the defender's `encryption layer`  
THEN the `attacker` MAY attack the the encryption layer.

1. The `attacker` places a `data card` from their `attack deck` face up in the upload area of the `defender's` `encryption layer`.
2. The `attacker` MAY `reveal` any `exposed` `encryption card`.
3. The `attacker` MAY `remove` any one combination of `upload` and/or `encryption` cards that have a total value of exactly 21.

### Attack Storage

### Run Program

# Glossary

- `target card` = A
- `program cards` = J, Q, K
- `data cards` = 2, 3, 4, 5, 6, 7, 8, 9, 10
- `removed` = placed in the respective player's `discard pile`
