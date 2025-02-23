# HackJack

Grab your deck and start hacking.

# Overview

Hackjack is a two-player hacking-themed card game played with a standard 52-card poker deck.

1. Divide the deck.
2. Set up your `servers` and `attack decks`.
3. Decide which player goes first with a `ping test`.
4. Take turns attakcing each other's `servers`.
5. The first player to download both of their opponent's `target cards` wins.

# Divide the Deck

1. Player 1 takes all the red cards: hearts and diamonds.
2. Player 2 takes all the black cards: clubs and spades.

# Server Setup

Both players plan and build their `server` and `attack deck`.

1. Place both of your `target cards` and any three of your `program cards` face down to form the `storage layer`.
2. Place any five `data cards` face down to form the `encryption layer`.
3. Place any six `data cards` face down to form the `firewall layer`.

The remaining 10 cards form your `attack deck`. This deck will contain `program cards` and `data cards` but no `target cards`

> Planning the layout of your server is a strategic part of the game. Do you use your highest data cards to create a stronger defensive firewall or save them for your attack deck? Where do you hide your target cards? For your first games just use any arrangement that follows the rules.

```
Server Layout

= player 1 =

 🂠 🂠 🂠 🂠 🂠             ← storage layer
 🂠 🂠 🂠 🂠 🂠   [upload]  ← encryption layer
🂠 🂠 🂠 🂠 🂠 🂠            ← firewall layer

🂠 🂠 🂠 🂠 🂠 🂠            ← firewall layer
 🂠 🂠 🂠 🂠 🂠   [upload]  ← encryption layer
 🂠 🂠 🂠 🂠 🂠             ← storage layer

= player 2 =
```

# Ping Test

1. Each player chooses and reveals a random card from their opponent's `attack deck`.
2. The player that _owns_ the lower card will go first. In the event of a tie, repeat the ping test.
3. Return the cards to their `attack decks`.

# Turns

The player who won the ping test takes the first turn. On a player's turn they are the `attacker` and their opponent is the `defender`. Players alternate turns until a player wins by downloading both of their opponents `target cards`.

If the `attacker` does not have any cards in their `attack deck` at the beginning of their turn, they add all the cards in their discard pile to their `attack deck`.

Each `turn` consists of one or more `actions`.

IF the attacker removes a card from the defender's server during their `action` AND they have at least one `attack card` THEN they MUST perform another `action`

IF the attacker does not remove a card OR runs out of `attack cards` THEN their turn ends.

An `attacker` might perform several `actions` in a single turn.

# Moves

### Attack Firewall

IF the `attacker` has at least one `data card` in their `attack deck`  
AND there is at least one card in the defender's `firewall layer`  
THEN the `attacker` MAY attack the firewall layer.

1. The `attacker` places a `data card` from their `attack deck` face up below a card in the `defender's` `firewall layer`.
1. The attacker `reveals` the firewall card, if it is not already `revealed`.
1. IF the attack card value is higher than the firewall card value  
   THEN both cards are `removed`  
   ELSE the attack card is `held` and it's value will be added to future attacks on the same firewall card.

### Attack Encryption Layer

IF the `attacker` has at least one `data card` in their `attack deck`  
AND there is at least one `exposed` card in the defender's `encryption layer`  
THEN the `attacker` MAY attack the encryption layer.

1. The `attacker` places a `data card` from their `attack deck` face up in the upload area of the `defender's` `encryption layer`.
1. The `attacker` MAY `reveal` any `exposed` `encryption card`.
1. The `attacker` MAY `remove` any one combination of `upload` and/or `encryption` cards that have a total value of exactly 21.

### Attack Storage

IF the `attacker` has at least one card in their `attack deck`  
AND there is at least one `exposed` card in the defender's `storage layer`  
THEN the `attacker` MAY attack the storage layer.

1. The `attacker` `discards` any card from their `attack deck`.
2. The `attacker` selects any `exposed` card in the `defender's` `storage layer`.
3. The selected card is `revealed`.
4. IF the card is a `data card` THEN the `attacker` downloads the card.
5. IF the card is a `program card` THEN the card's defense program effects are resolved.

### Run a Program

IF the `attacker` has at least one `program card` in their `attack deck`  
THEN the `attacker` MAY run a program.

1. The `attacker` chooses a `program card` from their `attack deck`.
1. The cards attack program effects are resolved.
1. The `program card` is `discarded`.

# Defense Program Effects

**Jacks** Hot Swap

1. The `defender` MAY swap any two positions of a single layer on their `server`. They may swap a card into an empty position.

**Queens** Query

1. The `defender` MAY `reveal` any single card in the `attacker's` `server` OR any two `adjacent` cards in the `attacker's` `encryption` or `firewall` layer.

**Kings** Patch

1. The `defender` chooses any position on their `server` that does not contain a `target card`.
2. IF the position contains a card THEN the `defender` MUST `discard` the card OR add it to their `attack deck`.
3. The `defender` MAY place any card from their `attack deck` or their `discard pile` face down in the selected position.

# Attack Program Effects

**Jacks** Hot Swap

1. The `attacker` swaps any two positions of a single layer on the `defender's` `server`.

**Queens** Query

1. The `attacker` chooses  
   1 `exposed` `storage card`  
   OR 1 or 2 `adjacent` `exposed` `encryption cards` in the `defender's` `server`  
   OR 1 or 2 `adjacent` `firewall cards` in the `defender's` `server`

[alternate for shorter rule]

1. The `attacker` chooses 1 or 2 `adjacent` `exposed` cards from a single layer on the `defender's` `server`.
2. The selected cards are `revealed`.

**Kings** Patch

1. The `attacker` chooses any `firewall` or `exposed` `encryption` card.
2. The selected card is `removed`.

# Winning

The first player to download both of their opponent's `target cards` wins.

# Glossary

- `attacker` = the player whose turn it is
- `defender` = the player whose turn it is not
- `target card` = A
- `program cards` = J, Q, K
- `data cards` = 2, 3, 4, 5, 6, 7, 8, 9, 10
- `remove` = place in the respective player's `discard pile`
- `revealed` = a card on the server that is face up
- `exposed` = A storage card is exposed if the encryption layer position in front of it is empty. An encryption card is exposed if either firewall layer position in front of it is empty. All firewall cards are exposed.
- `attack deck` = the cards the attacker uses to attack the defender's server
- `attack card` = a card from the attacker's attack deck

```
Exposed Card Examples
🃟 = exposed
. = empty

 🂠 🂠 🂠 🃟 🂠             ← storage layer
 🂠 🃟 🃟 . 🃟   [upload]  ← encryption layer
🂠 🂠 . 🂠 🂠 .            ← firewall layer
```

# FAQ

Q: Why aren't there any questions in the FAQ?  
A: We haven't received any questions yet.

Q: Why is this game so confusing?  
A: Well, Grayden if you're finding the game confusing maybe try reading over the instructions again or maybe start with the tutorial game.

# Tutorial Game
- coming soon
