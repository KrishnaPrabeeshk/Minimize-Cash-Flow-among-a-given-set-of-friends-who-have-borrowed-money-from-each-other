# Minimize-Cash-Flow-among-a-given-set-of-friends-who-have-borrowed-money-from-each-other
Problem statement : Given a number of friends who have to give or take some amount of money from one another. Design an algorithm by which the total cash flow among all the friends is minimized. 
Example :
   1k
p0------>p1
\        /
 \2k    /5k
  \    /
    p2
Above debts can be settled in following optimized way  

p0       p1
\        /
 \3k    /4k
  \    /
    p2
Algorithm : 
1: Compute the net amount for every person. The net amount for person ‘i’ can be computed by subtracting sum of all debts from sum of all credits.
2: Find the two persons that are maximum creditor and maximum debtor. Let the maximum amount to be credited maximum creditor be maxCredit and maximum amount to be debited from maximum debtor be maxDebit. Let the maximum debtor be Pd and maximum creditor be Pc.
3: Find the minimum of maxDebit and maxCredit. Let minimum of two be x. Debit ‘x’ from Pd and credit this amount to Pc
4: If x is equal to maxCredit, then remove Pc from set of persons and recur for remaining (n-1) persons.
5: If x is equal to maxDebit, then remove Pd from set of persons and recur for remaining (n-1) persons.
