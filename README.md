# Hackjack

Grab you deck and get hacking.


## What it is

Hackjack is a two player hacking-themed card game played with a standard 52-card deck.


## How to Play

### Game Sequence Overview

1. Divide the deck into red and black cards. One player takes all the red cards, and the other takes the black.
2. Both players strategically set up their **Servers** and **Attack Decks**.
3. Decide which player takes a turn first with a **Ping Test**.
4. Players alternate taking **Turns** until a player wins by downloading both of their oppenents Aces.


### Server Setup

At the begining of the game each player sets up their "server" by placing cards from their deck in three rows. The first row represents the "firewall" and contains 6 numbered cards. The second row represents the "encryption layer" and contains 5 numbered cards. The thrid row represents your data and contains two aces and three **Honeypot** face cards.

```asci
Firewall:     # # # # # #
Encryption:    # # # # #
Data:          F F F F F
```

### Programs + Honey Pots

- Jacks
>Architecture Program: Swap 2 cards in play

- Queens
>names: Query
>Reveals cards

- Kings 
>name options: Archive, Backup, Restore
>Swap a card from attack deck with a position on the server

### Attack Deck

When you have fully set up your server you will have 10 cards left over. These cards form your **attack deck**. Cards from your **attack deck** are played during your **Turn** to penetrate your opponents defenses and defend your own server.

### Ping Test

Both players randomly draw a card from their opponents deck. The player whose deck had the lower card goes first. Break ties with redraw. Note that this also gives each player some info about the other player's hand.


### Taking a turn

Play an attack card on the firewall.

Play an attack card on an exposed ecryption card.

Upload an attack card to the ecryption layer.

Play a face card/program.

- Jacks
- Kings
- Queens

### Ending a turn

A failed attack.

Downloading an Ace or accessing a Honeypot card.

Voluntarily

### Winning

The moment that a player downloads both their opponent's Aces, they win.

### Terms

Exposed

Revealed



### Things to Play Test/Variations

Discarded cards don't go back into your hand until you are completely out of cards

Must play/burn a card to reveal final data or honey pot cards

Use numbered/attack cards as data cards, allows ace to be another type of special card

Mixing Honey pots into firewall and encryption layers

Using the suits of the cards somehow, perhaps the suits match up. (on the firewall only a diamond can beat a club; only a heart can beat a spade?)

Garbage File!


