---
layout: default
title: Automatic testplaying on the computer ! - Open Design Games
tw:
  description: 1.How do you run your game automatically ? / 2.Define the game for programming / 3.Although...
  image_url: 
---

## Automatic testplaying on the computer !

[(日本語版はこちら)](testplay_2_on_the_computer.html)

We(the game designers) want to test for our games more and more, if we can. But most players don't hope it. They want to play "products" (not a immature).
What should we do ?
Because I am a programmer, I think it better to test our games on the computer. So if you wish, you can test it 10,000 times !

### 1.How do you run your game automatically ?

If you want to test your game 10,000 times, you must develop a software plays your game *automatically*.

At first, you must develop a program to deputize players.
It is a function. The player is a function that select (or not select) his/her action from actions he/she can play.

But the player doesn't drive a game. The player can only switch a game.
So what does drive a game ? It is a rules !

On the basis of the above I'll defined the game for automatic testplaying.

### 2.Define the game for programming

*The game has rules and continues to apply all rules until it ends.*

And I'll try to consider the other elements of the game.

**Rule**

The rule is a function. The rule makes a new game context from previous one.
If I show you an example program, it is like this...

Ex) The rule is named "dealAllCards"

```
// Before the rule is applied
print context['deck'].length; // 16
print context['player1']['hands'].length; // 0

next_context = dealAllCards(context);

// After the rule is applied
print context['deck'].length; // 0
print context['player1']['hands'].length; // 4
```

In this definition, the context is reliant on previous context only.
This means the program is capable of parallel processing.

**Player**

As mentioned previously, the player is a function that select his/her action from actions he/she can play.

Ex) The player of "Old Maid"

```
actions = [
  drawCard(prev_player['hand'][0]), // Draw the first card of previous player from the left
  drawCard(prev_player['hand'][1]), // Draw the second card of previous player from the left
  ...
];
selected_action = player1(actions);
```

If you give it a order or weight of the judgement conditions as parameters (or something else), you can get personalized players.

**Component**

The components is defined and its instance is used in a play.

Ex) The Definition of playing cards

```
cards = [
  { "suit": "spade", "number": 1 },
  ...
];
```

**Deck, Hands, Trush and Any Fields on the board**

Deck, hands, trush and any fields are just a label.

Ex) The Fields of "Old Maid"

```
oldMaidContext = {
  'players': [
    'player1': {
      'hands': [] // Hands of player1
    },
    ...
  ],
  'trash': []
};
```

### 3.Although...

Although I have defined the game above, it is not efficient that everyone develops a testplaying program under its definition.
So I am developing a testplaying framework now.

→ 3. [aglab - Testplaying framework](testplay_3_framework_en.html)

→ [Go to top](board_game_design_advent_calendar_2014-12-25.html)
