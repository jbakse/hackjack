# Hackjack

Grab you deck and get hacking.

# Outline

- General Description including objective
  - Two Player
  - Standard Deck
  - Players design servers
  - take turns trying to exploit server to retreive data cards
  - first to capture both of oponents data cards wins

- Game Sequence
- Glossary / Card States / Playfield Diagram

- Server Setup
- Ping Test
- Turns
  - Moves
    - Attack Firewall
    - Attack Encryption
    - Attack Storage
    - Play Program Card
- Program Cards
  - Jacks
  - Queens
  - Kings
  - Joker?



Program cards: J,Q,K
Data cards: ace
Code cards: 2-10
Protected
Exposed
Revealed (unlocked)
Concealed (locked)
Held
Uploaded
Honeypots


Attack Deck
Discard Pile
Attacker
Defender

Access?







## What it is

Hackjack is a two player hacking-themed card game played with a standard 52-card deck. Jokers are not used.


## How to Play

### Game Sequence Overview

1. Divide the deck into red and black cards. One player takes all the red cards, and the other takes the black.
2. Both players strategically set up their **Servers** and **Attack Decks**.
3. Decide which player takes a turn first with a **Ping Test**.
4. Players alternate taking **Turns** until a player wins by downloading both of their oppenent's Aces.


### Server Setup

At the begining of the game each player sets up their **server** by placing cards from their deck face down in three rows. The first row represents the "firewall" and contains 6 numbered cards. The second row represents the "encryption layer" and contains 5 numbered cards. The thrid row represents your server storage and contains your **data cards**—the two aces—and your **program cards**—three face cards of your choosing. The three remaining face cards and seven remaining numbered cards form your **Attack Deck**. 

Your server setup is secret
it is strategy
don't worry first time

```asci
Firewall:     # # # # # #
Encryption:    # # # # #
Data:          F F F F F
```

### Programs

The face cards represent programs. Programs can be activated in two ways. First, a player may play a program on their turn. Second, a program in the server is activated whenever it is reavealed.

- Hot Swap (Jacks)
  Swaps two server cards.

  When Played from the Attack Deck: The attacker may choose two positions from a single row on the opposing player's server. The cards in these positions are swapped. There does not need to be a card in both position, you can swap a card into an empty position.

  When revealed on the server: The defender may choose any two positions from a single row on their own server and swap them.

  - Swap 2 cards in play. names: Architect, Glitch, Loop, Recompile

- Query (Queens)
  Safely reveals cards.

  When Played from the Attack Deck: The attacker chooses a single target card or a pair of cards to reveal. At least one position in front of each target card must be open. Only a single storage card may be targeted. Either a single or adajance pair of encryption cards may be targeted. Either a single or adjacent pair of firewall cards may be targeted. 
  
  When revealed on the server: The defender may choose any single storage card, pair of adjance encryption cards, or pair of adjance firewall cards, on their opponents server and reveal them. Must be exposed?
  
- Reveals cards. names: Query, Crack 

- (Patch) Kings 
  - Swaps a card between the attack deck and the server
  
 When Played from the Attack Deck: The attacker may choose any encryption or firewall card, the defender then removes the card from the server and adds it to their discard pile. 
  
  When revealed on the server: The defender may choose any position on his server, pick up the card (if any) at that position adding it to their attack deck or discard, and then play any card from their Attack Deck or Discard Pile (must be the same place you put the server card) face down on that position. If you place a card from the discard pile, you should show it to your opponent first. The defender may not pick up a data card. Must be a legal card for that position.


  - Swap a card from attack deck with a position on the server. names: Patch, Archive, Backup, Restore, jury rig, Reboot 

- Ace 
  - names: Payload, Data, ---- AI, ICE, Backdoor, Easter Egg


## Reveal

A revealed card is flipped face up, and left in position. When a program card is revealed, it is immediately run. If the a program card is revealed by the Query card, the program is not run.

### Attack Deck

When you have fully set up your server you will have 10 cards left over (3 face cards, 7 numbered). These cards form your **attack deck**. Cards from your **attack deck** are played during your **Turn** to penetrate your opponents defenses.

### Ping Test

Both players randomly draw a card from their opponents attack deck. The player whose deck had the lower card goes first. Break ties with redraw. Note that this also gives each player some info about the other player's hand. After the ping test the drawn cards are returned to the Attack Deck.


### Taking a turn

Play an attack card on the firewall.

Play an attack card on an exposed ecryption card.

Upload an attack card to the ecryption layer.

Play a face card/program.

### Ending a turn

A failed attack.

Downloading an Ace or accessing a Honeypot card.

Voluntarily

### Winning

The moment that a player downloads both their opponent's Aces, they win.

### Terms

#### Exposed
An exposed card is a card that is no longer protected by the cards in front of it. 

###  Revealed

A revealed card is flipped face up, and left in position. When a program card is revealed, it is immediately run. If the a program card is revealed by the Query card, the program is not run.


### Misc Rules (format into above)
When cards are removed from the server they are placed into the discard pile. If a hacker runs out of cards their turn is over. ~strike: During a hackers turn they may end their turn early to collect their cards from the discard.~ (should the hacker be able to collect their cards from the discard if they have no cards but still have a 'move': example the hacker plays their last card and beats a honey pot? answer: no)

Hackers must play a card to reveal any other card. Cards played on the encryption layer are uploaded to the encryption layer and count towards the encyption tally.



### Honeypots/Traps
optional: Honeypots can be defeated by playing a card of the opposite suit of the honeypot. Opposite/matching suits are: Hearts + Spades and Diamonds + Clubs.

optional: Honeypots can be placed anywhere in the Server




### Things to Play Test/Variations

Use numbered/attack cards as data cards, allows ace to be another type of special card

Garbage File!

## Kickstarter Reward and Stretch Goal ideas
character cards give special bonuses to players
  - telecommuter: doesn't have to wear pants for duration of game
  - hack the planet: people have to call you zero cool, crash override
  - glasshole:
  - drone:
  - botnet:
  - social network: can ask friends for help
  - god love secret sex:
  - praetorian: gets to control the light switch
  - unix system: i know this!
  - gambler/kenny rogers/double down: can put money down on table and make bets
  - N00B
  - LEET/1337
  - one more thing....
  - 
break out into seperate file

rule cards

custom decks with rule cards foil printing

playing mats

soundtrack

iphone app


### Attacking the Firewall

Play a numbered card onto a firewall card. The firewall card is revealed. If the number on the attacking card is higher, both cards are removed to their respective player's discard piles, and the attacker may make another play. If the number on the attacking card is lower, the attackers turn is endened, the attacking card stays on server, and its value will be added to future attacks on that card.  

### Attacking the Encryption layer

Play a card from your Attack Deck to the upload area
Reveal on exposed encryption card (if any)
If any combination of ecryption and uploaded cards totals 21, the attacker may remove those cards, and make another play.
If no combinations that total 21 are available, the attacker's turn ends

### Attacking the Storage layer

The Attacker burns a card, placing it face up on the discard pile.
The attacker can then choose one exposed card in the storage layer to reveal.
If the revealed card is data, it is immediately captured by the attacker and removed from the server. The attacker can then make another play.
If the revealed card is a program, it is immediately run, and the attackers turn is over.




Railroad diagram of play or turn



can king and jack affect unexposed cards?
is a storage card exposed if the ecnrypiont card is removed, but the fire wall cards are both in place

meta rules no rules should vilolate these:
nothing should allow an attacker to remove a card from a server that was not exposed
nothing should allow an attacker to reveal a card that is not exposed

the attacker must play a card before any card can be removed from the server



Expansions:
Special character abilities (play as "hack the planet", "fixer", etc.)
Zero and 1 Cards (8 cards 4 x 1, 4 x 0)


Joker:
honeypot that gets an ace back
joker starts in the discard pile, so you get it as an attack card only after you pickup your discard
some kind of wild?
maybe borrows the value of the discard



collect data during play

who started
how many turns each
who won
how many moves each turn
what turn the discard got picked up


