# IT102.FINAL.Project3
Debugging existing code

This is a debugging project. The script below has exactly 4 errors. Two of these are syntax errors, One is an error in code logic. The other is an error in game play functionality. (The desired game play is defined in the comment at the top of the script.)

You will receive 20 points for each syntax error you correctly identify and fix. You will receive an additional 20 points for submitting a cleaned up version of the script that runs correctly. Test output should look like this:

TestOutputFinalProject3.PNG

Write comments in the code to show where the bugs are. For example:

// for (i=0; i<6, i++)  //syntax error - comma instead of semi-colon

for (i=0; i<6; i++)  //corrected

---------------------------------------------------------------------

                             Script to Debug

---------------------------------------------------------------------

<!DOCTYPE html>
<html>
<body>

<script>

/* *************POKER DICE ***************

Creates 5 dice with A, K, Q, J, 10, 9.
Dice all roll.
Roll gives results of each of the 5 dice.

*************POKER DICE *************** */

function Die(sides) {
this.sides = sides;

this.values = [];
for (i= 0; i<this.sides; i++)
{this.values[i]=i;}

this.roll = function () {
var showing = Math.ceil(Math.random()*this.sides);
return this.values[showing];
};

var pokerSide = ["A", "K", "Q", "J", "10","9"];
this.poker = function () {
for (i= 0; i<this.sides; i++)
{this.values[i] = pokerSide[i];}
};

var myDie = [];

for (c=0; c<5; c++){
myDice[c] = new Die(5);
myDice[c].poker();
}

var output = "";
for (k = 0; k< 5; k++){
output+=myDice[k].roll();
output+=" ";
}

alert(output);

</script>

</body>
</html>
