IPP Lab 1. Design patterns.
===
**Deadline: November 1st**

Problem 1.
---

1. Write a simple application (web, mobile or desktop) that has several buttons.
  Clicking on a button should start a unique time-consuming computation.
  For example, you could create 10 buttons that would download 10 different vides from the internets.
  Don't bother with separating threads, we will just need a set of unique time-consuming operations.
2. Refactor the application you just wrote by introducing the Proxy Pattern.
  Upon pressing a button, the request is not fired off immediately, but sent to the Proxy object.
  The proxy collects the time-consuming operations and fires them off in a batch after some time.
  Thus, you will be able to click 5 buttons and then see how the proxy fetches 5 videos.
3. Modify the proxy object so that it would become a caching proxy.
  The caching proxy should store the result of the time-consuming operation and return it on repeated requests without computing the result (this technique is also called *memoization*).
  Therefore, if the user presses the buttons A and B, the videos are fetched. Now, if the user presses buttons B and C, only C is fetched, but both are returned.

---

## Problem 2.

Let's create a game using the mediator pattern.
The application will be a game where the players are given half a minute to compete for who will press a button more times than the other.
Player 1 competes by pressing 1 and player 2 presses 0. A scoreboard is updated with the current score.

The entities within such a system would be:

- Player 1
- Player 2
- Scoreboard
- Mediator

The mediator knows about all other objects.
It communicates with the input device, handles keypress events, determines which player has a turn, and notifies it.
The player plays and notifies the mediator that he's done.
The mediator communicates the updated score to the scoreboard which in turn updates the display.
Note that other than the mediator, none of the objects knows anything about any other object.
That makes it trivial to update the game, for instance, by adding a new player or another display showing the remaining time.

For an approximate structure, refer to the diagram below.


![Diagram](http://i.imgur.com/86JKTWa.png)


---

## Problem 3.

Implement the same keypress game, but using the observer pattern.
This time, let it accept an unlimited number of players.
In problem #2, the mediator object knew about all other participating objects and called their methods.
In this case, the main object (let's call it `game`) will not do that.
The `game` object will leave it to other objects to subscribe to interesting events.
You have to analyze the problem domain and see what events do you have and what data is sent on each event.
(for instance, the `scoreboard` object will surely subscribe to the `scorechange` event)

