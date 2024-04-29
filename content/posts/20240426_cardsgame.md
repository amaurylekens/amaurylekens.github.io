+++
title = "Pydecklib: a cards game python package"
date = "2024-04-26T00:56:24+01:00"
author = "amaurylekens"
authorTwitter = "" #do not include @
cover = "/img/cards_game_python.jpg"
tags = ["python", "package"]
keywords = []
description = "Presentation of a card game python package that I've developed"
showFullContent = false
readingTime = false
hideComments = false
color = "" #color from the theme settings
+++

I've developed a small Python package called pydecklib that enables the use 
of a deck of cards in Python scripts. To install it, simply run:


```bash
pip install pydecklib
```

Here is an example of how to create a deck and use it:

{{< code language="python" title="Use a deck" id="1" expand="Show" collapse="Hide" isCollapsed="false" >}}
from src.pydecklib.deck import Deck

deck = Deck()

for card in deck.draw(5)
    print(card)
{{< /code >}}

You can use comparison operators on cards. Additionally, you have the option to
configure whether the suits are ordered.

{{< code language="python" title="Compare cards" id="2" expand="Show" collapse="Hide" isCollapsed="false" >}}
from src.pydecklib.deck import Card

card = Card()

card_a = Card(Suit.SPADES, Value.EIGHT)
card_b = Card(Suit.DIAMONDS, Value.EIGHT)

print(card_a == card_b) # True

Card.suit_ordered = True

print(card_a == card_b) # False
{{< /code >}}