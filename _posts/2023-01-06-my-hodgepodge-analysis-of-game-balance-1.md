---
layout: post
title:  "My hodgepodge analysis of game balance 1"
date:   2023-01-06 15:00:00 +0900
categories: games 
---

You very rarely hear about some major sport like football or basketball changing their rules in a major way. 
You essentially never hear about rules of Chess or Go changing. Yet, these established "canonical" games don't receive criticism about balance.

On the other hand, competitive e-sports titles like Overwatch or League of Legends receives a "balance patch" every month or two.
Yet, the strategical environment, or _meta_, created by each change seldom receive praise from players for brining balance to the game.
Despite the great lengths developers go to reach a fair playingfield, e-sports titles always seem to never quite reach that elusive point of balance.

I've personally played a fair bit of Overwatch.
I stopped playing shortly after the release of Brigitte, upset with how frustrating the game was to play.
But with the release of OW2, I returned to the game and am personally really enjoying it.
Having undergone this change of heart, I contemplated more about the idea of game balance and why video games feel like they never quite get it.

Obviously it's a very complicated topic and I don't plan on writing all my thoughts on this post. 
I'll split it up into mutiple steps, and because this is the first step, I want to start out by discussing a simple, arguably contrived example.

## Mirror 1 v 1
Providing players with the choice of hero/character inherently brings unfairness to the table.
To show this, I first offer an unreasonable but perfectly balanced game: a simple 1 v 1 game with a clear optimal choice.
I'm going to try to use some botched logic math, but bear with me.

All descriptions that follow are assuming the hero is played perfectly. 
We can define a balanced game as a game where if an infinite number of games are played, one player will have the most wins (I'll get back to this shaky definition later).
Let S be the set of heroes in this game. A player is defined as a 1 x n dimension vector where n = |S|. 
Each element of the vector describes the aptitude of a player with the corresponding hero with a higher number indicating a higher aptitude with the hero.

Let **Opti** be defined as a hero which can beat all other heroes in S and ties with itself.
Then, assuming that the pro players are skilled enough to reach a nearly perfectly, this is a balanced game where whoever plays better, even by a little, will win. 

This game operates identically to canonical games since choice is just an illusion. 
Reasonable pros will always select **Opti** since **Opti** is clearly the best and the game is always a mirror match.
But this game is likely not very fun or commercially successful because of the lack of variety. 
Additionally, **Opti** one-trick players greatly advantaged in this model, which would further detract from the game's enjoyment.
So, let's introduce the idea of counterpick.

## Rock Paper Scissor 1 v 1
We can define a new hero **Count**, who can defeat **Opti** but is defeated by at least one hero in the hero pool (i.e., the set **Count** is a member of).
The latter restraint is in place because **Count** should not be **Opti** as well.
Let S' be the set S with **Count** appended.
By definition of **Count**, there must be some hero that defeats **Count**: let's call it **Tri**.
And thus, we have a triangle where Count beats Opti beats Tri beats Count beats ...
Once such a chain of counters is formed, the game becomes undisputedly balanced to _technically_ balanced.
More specifically, if indeed an infinite number of games were to be played, the best player would come out on top. 
But until then, rankings will shift based on luck, since a player must guess what the other player will select to try to counter via picking the right hero.

This model too, however, leads to a rather boring system since the result of a non-mirror-picked round will be blatant as soon as each player's choice is revealed.
It's like watching a game of Rock Paper Scissor!

But all this is in an ideal game where all players play nearly perfectly. If players were not perfect, how would the game play out then? I'll discuss that in the next post.
