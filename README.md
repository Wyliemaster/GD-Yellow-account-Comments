# GD Yellow account Comments
 a save injector which allows you to have yellow account comments

 ## What does this do?

 Generally, account comments in geometry dash are hard-coded to not change colour at all however, due to an incredibly dumb oversight by mister topala, it is possible to give yourself yellow account comments. An example is shown below

![example](https://pbs.twimg.com/media/ExFChY9WYAI1mDw?format=jpg&name=medium)

## What is this oversight?

In regards to comments, there are `3` main checks that determine colour

- isRobtop
- hasRatePower
- isLevelOwner

The `isLevelOwner` check is what allows this to happen. The condition is `if(commentAuthorUid == levelAuthorUid)` however, since account comments don't return a Uid, the check is essentially `if(undefined == levelAuthorUid)`. By injecting a level which allows this condition to be true, you can then get yellow account comments.