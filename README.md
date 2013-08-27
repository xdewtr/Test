Day1 Shuffle note

Day2 BJ NOTES
=============

Since using % might slow down processing speed, I decide to do some tricks to reach the same purpose.
Notice that in JS Math.random() will give out numbers between 0 - 1.
Therefore, I miltiply by a hundred to make it between 0 - 100.

var randnum = parseInt(Math.random() * 100);
var pos = (randnum > 51) ? (randnum - 48) : randnum;

With such a method we can achieve the same goal as modulus operand.

Checksum dealing with double Ace issue can be solved in a quick way.
We know that sum can't exceed 22; thus, from the second ace we get, we should all make it value 1.

Basically the whole structure to get cards is a nested while loop with the following conditions.
At the inner while loop, representing as a round, as long as sum doesn't exceed 17 and cards player 
owns doesn't exceed 5, then player should keep getting cards.

while(deck.length != 0 )
	{
		aRound();
	}
	
May have a better solution. Even though I want to deal with out of cards problem
in the level of round.
