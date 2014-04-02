Tau Game
========

This is Tau ([currently deployed version](https://github.com/jasharpe/websockettau) reimplemented using Websockets by [jasharpe](http://github.com/jasharpe)): [http://taugame.com/](http://taugame.com/)

Tau is an online multiplayer card game. The game is pure web application – no plugins or applets are required.

Objective
---------

Find Taus and remove them from the table. If you found the most when the deck runs out, you win.

Rules
-----

Each card has four properties (color, number, shape, fill), and each property has three choices. The choices are:

* Color: red, blue, green
* Number: one, two, three
* Shape: triangle, square, circle
* Fill: clear, shaded, solid

There exists exactly one card for every unique combination of properties. Thus, there are 81 = 3^4 cards in a deck.

A Tau is a set of three cards such that for each property, the values of the property for the three cards are either all the same or all different.

**TIP:** Another way of saying it is: if two cards are and the other isn’t, then it’s not a Tau.

For example, if a Tau contains two cards of the same color, the third card must also be the same color. If a Tau contains two cards of different numbers, the third card must have a number different from the other two cards. It is possible to have Taus where there are one, two, three, or four properties that are all different, and the rest common. However, there is no Tau where no properties are different and all four properties are common, since every card is unique.

Here is an example of a Tau where all four properties are all different:

![](http://taugame.com/images/example-all-different.png)

Here is an example of a Tau where three properties are different and one is common:

![](http://taugame.com/images/example-one-common.png)

While there are cards remaining in the deck, the dealer will always put 12 cards on the table, and if there is no Tau in those 12, the dealer will deal batches of three cards until there is a Tau. When the deck runs out, you keep finding Taus until there are none left on the table, and then the game is over.

**TIP:** If the dealer had to put more than 12 cards on the table, this means every Tau on the table must involve one of the three most recently-dealt cards.

Controls
--------

There are two ways to select cards: using the mouse and using the keyboard. When you have selected three cards that form a Tau, then the cards are removed from the board, you get a point, and another three cards are dealt if appropriate. Selected cards have a red border around them.

#### Using the Mouse
Left-click a card to select it, and left-click it again to unselect it.

#### Using the Keyboard
The left side of the keyboard can be used as a grid. Pressing a key toggles selection of a card.

    Q W E R ...
    A S D F ...
    Z X C V ...


