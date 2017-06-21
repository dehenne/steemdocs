# Reputation Score

The score on the Steemit profile is a condensed version of the \(huge\) value stored in the Steem blockchain. The original score is a number starting in the millions, going up to trillions, positive or negative. The simplified number ranges from -25 to around 75. New member always start with a score of 25.

## Math

* log10 of the base score

*  substract 9

* multiply by 9

* add 25

* round down to nearest integer


**Example (JS)**

    const calculateReputationScore = reputation => {
     return Math.floor(Math.max(Math.log10(Math.abs(reputation)) - 9, 0) * 9 + 25);
     }; 
