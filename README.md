# zk_game_logic.aleo

## Card representation

Cards are represented using 64 bits to represent the value and suit of the card as follows:
A♠ is represented by the integer with the 51st bit set (most significant bit).
A♣ is represented by the integer with the 50th bit set.
... and so on.
This would look something like:
A♠: 0000...1000...0000 (12 zeros followed by 1 one followed by 51 zeros)
A♣: 0000...0100...000 (13 zeros followed by 1 one followed by 50 zeros)
...
The hand where you have both A♠ and A♣ would look like this:
A♠&A♣: 0000...1100...0000 (12 zeros followed by 2 ones followed by 50 zeros)

## About Program

The program receives the hand (can be either 5 cards (all 5 from player private hand) or 7 cards (2 from player private hand + 5 from public river)) which is encoded into u64.
The program checks for what winning combination the hand has. (Note: checks for straight and flushes are not present and will be added in next updates.)
The program returns the winning combination in u64 format.

## Build Guide

To compile this Aleo program, run:

```bash
leo build
```

To execute this Aleo program, run:

```bash
leo run get_hand_ranking_combination 115u64
```


## Get in touch
Discord: Genie#6248
