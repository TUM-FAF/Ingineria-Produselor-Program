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

Problem 2.
---

TBA
