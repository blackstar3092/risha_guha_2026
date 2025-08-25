---
layout: post
title: JavaScript Learnings and AI Evidence
description: What I Learned about JavaScript and How AI Helped Me
permalink: /sprint/1/javascript
menu: nav/sprint_1.html
toc: True
comments: True
---

## Overview

This sprint I deepened my understanding of **JavaScript frontend basics** and **Object-Oriented Programming (OOP)** through our Solitaire game project. By working with classes, encapsulation, inheritance, and composition, I learned how JavaScript structures can model real-world rules.  

Alongside my coding, I also experimented with **AI-assisted development**. I used prompts to generate starting points for methods, but I also made corrections when the output wasn’t accurate or didn’t match our team’s design.  

This blog highlights both my **code learnings** and **AI evidence in work**.

---

## JavaScript Frontend Basics

One of my main tasks was translating OOP concepts into working **UI components** that players could interact with.

### Example: Card Class

```js
class Card {
    constructor(suit, rank, color, value) {
        this.suit = suit;     // '♠', '♣', '♦', '♥'
        this.rank = rank;     // 'A', '2', ... 'K'
        this.color = color;   // 'red' or 'black'
        this.value = value;   // 1..13
        this.faceUp = false;
        this.id = `${rank}${suit}`;
    }

    describe() {
        return `${this.rank} of ${this.suit} (${this.color})`;
    }
}
```

**What I learned:** Every card becomes an independent object with properties and helper methods.

**Frontend connection:** These card objects map directly to DOM elements in the UI (<div>s styled with CSS).

### Example: Encapsulation in Piles

```js
class Pile {
    constructor(type) {
        this.type = type;
        this.cards = [];
    }

    push(card) { this.cards.push(card); }
    pop(n = 1) { return this.cards.splice(-n, n); }
    top() { return this.cards[this.cards.length - 1]; }

    get isEmpty() {
        return this.cards.length === 0;
    }
}
```

**Lesson learned:** Keep data private and only allow access through controlled methods like push() and pop().
**Impact on UI:** This made it easier to prevent invalid moves when dragging and dropping cards.

## AI Evidence in Work

AI played a role in my learning, but not as the final answer.

- It provided helpful starting points, like suggesting structures or example methods.
- I made fine adjustments, improving the code so it worked correctly in our Solitaire project and matched our team’s style.

This combination made me faster while still ensuring I understood the logic and details.

## Reflection

The biggest lesson I learned in JavaScript this sprint is that objects define behavior. Seeing OOP principles directly control Solitaire’s gameplay solidified my prior knowledge of this concept.

AI was a helpful assistant for brainstorming and scaffolding, but I learned the most when I adjusted its outputs myself. Those small refinements made me think critically about syntax, rules, and design—helping me grow as a coder.

In the end, combining **JS fundamentals**, frontend interactivity, and **AI assistance** gave me both a working game and a deeper understanding of how to design maintainable code.
