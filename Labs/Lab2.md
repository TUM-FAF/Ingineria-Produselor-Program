## Lab Work #2: Test Driven Development

Due December 20th

## Problem 1

You're developing an ordering system for Pizza Adriano. Pizza Adriano has several specifics:

- Any ordered pizza can have a set of extra ingredients
- The extra ingredients are placed in three groups: Cheeses, Vegetables, Meat
  - Cheeses (up to 3):
    - Feta
    - Parmesan
    - Mozarella
    - Dor Blue
    - Edam
    - Brânză
  - Meat (up to 2):
    - Bacon
    - Prosciutto
    - Salami
    - Chicken Breast
    - Ham
  - Vegetables (up to 5):
    - Fresh mushrooms
    - Smoked mushrooms
    - Red onion
    - Tomatoes
    - Garlic
    - Rucola
    - Marinated Gogoshars
    - Corn
    - Parsley
    - Chili pepper
- Any group of ingredients has a limit of components that can be had in an order
- Every component has a price ranging from 1 lei to over 9000 lei. Feel free to set a random price.

The ordering workflow for the user is as follows:

1. The user inputs their name
2. The user can select the components of a pizza
3. The user looks at the order and its price
4. The order can be disapproved and reviewed by the user (clicking 'back')
5. The user can finalize the order
6. When the order is finalized, a unique 3-digit ID is generated for the order

Develop a **desktop** application that would allow the user to go through all the steps. Isolate the UI and the underlying logic. Provide tests for the logic.

Since it's quite tricky to automate the acceptance testing for desktop apps, you'll have to only provide the integration and unit-level tests. For instance, depending on your implementation, an integration test might go through the whole order process state machine and test that the outcoming price and components are correct, whereas the unit test will cover the PriceCalculator correctly.

Remember, the point is to get the hang of tests in a non-trivial app. Having more test code than actual code is actually a good thing.

## Grading policy

You'll get 80% of the points for a working app
You'll get 90% of the points for a non-complete app, but completely covered by tests
You'll get 100% of the points for a working, semi-covered app
You'll get 80% of the points if all you have are tests and an app skeleton and they run correctly.
