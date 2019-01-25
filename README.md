# Elevens 7

Follow the instructions provided for Activity 7 in the student lab guide. This is more of an exploratory lab, so you will not need to copy any of your previous code into the repo. Answer the questions from the Student Guide in this document and ensure that you save and push the repo. You have one week to complete this lab.

1. What items would be necessary if you were playing a game of Elevens at your desk (not on the computer)? List the private instance variables needed for the `ElevensBoard` class.

    * Answer: private instance variables would be cards(with point value), deck, and discard pile

2. Write an algorithm that describes the actions necessary to play the Elevens game.

    * Answer:
    1) deal 9 cards
    2) if 2 selected cards equal 11 OR 3 separate face cards are selected -> add to discard pile and replace from deck
    3) while step 2 is possible, continue game
    4) else end game with "you lose"

3. Now examine the partially implemented `ElevensBoard.java` file found in this repository. Does the `ElevensBoard` class contain all the state and behavior necessary to play the game?

    * Answer:
    yes

4. `ElevensBoard.java` contains three helper methods. These helper methods are private because they are only called from the ElevensBoard class.

  * a. Where is the `dealMyCards` method called in ElevensBoard?

      * Answer:
      It is called in the newGame() method

  * b. Which `public` methods should call the `containsPairSum11` and `containsJQK` methods?

      * Answer
      isLegal() and anotherPlayIsPossible()

  * c. It’s important to understand how the `cardIndexes` method works, and how the list that it returns is used. Suppose that `cards` contains the elements shown below. Trace the execution of the `cardIndexes` method to determine what list will be returned. Complete the diagram below by filling in the elements of the returned list, and by showing how those values index `cards`. Note that the returned list may have less than 9 elements.

    * `cards`

| 0  | 1  |  2   | 3  |  4   |  5   | 6  | 7  |  8   |
|:--:|:--:|:----:|:--:|:----:|:----:|:--:|:--:|:----:|
| J♥ | 6♣ |`null`| 2♠ |`null`|`null`| A♠ | 4♥ |`null`|

   *  * Answer - This list should contain the indices of the cards, not the cards themselves

| 0  | 1  | 2  | 3  | 4  | 5  | 6  | 7  | 8  |
|:--:|:--:|:--:|:--:|:--:|:--:|:--:|:--:|:--:|
| J♥ | 6♣ | 2♠ | A♠ | 4♥ |    |    |    |    |

  * d. Complete the following `printCards` method to print all of the elements of cards that are indexed by `cIndexes`.
```java
public static printCards(ElevensBoard board) {
    List<Integer> cIndexes = board.cardIndexes();

    /* Your code goes here. */
    for (Integer i : cIndexes) {
      System.out.println(board.cards[i].toString());
}
}
```

  *  * Answer

  * e. Which one of the methods that you identified in question 4b above needs to call the `cardIndexes` method before calling the `containsPairSum11` and `containsJQK` methods? Why?

      * Answer
      anotherPlayIsPossible()

## Feedback
4.c is slightly off
19/20
