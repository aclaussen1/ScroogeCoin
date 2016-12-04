# ScroogeCoin

This is the source for my submission for Coursera's [Introduction to Crypto and Cryptocurriences](http://www.coursera.org/learn/cryptocurrency) programming assignment 1. The course was created by Princeton University's Arvind Narayanan, professor of Computer Science. I am taking this course in December 2016.

# The Assignment

The goal is to create ScroogeCoin, a cryptocurrency in which the central authority Scrooge receives transactions from users. As the programmer, I have to implement the logic used by Scrooge to process transactions and produce the ledger. Scrooge organizes transactions into time periods or blocks. In each block, Scrooge will receive a list of transactions, validate the transactions he receives, and publish a list of validated transactions.

# The Test Cases

This assignment is graded algorithmically through 15 test cases administered through the Coursera website. This assignment is pass/fail, where only 10 succes test cases are needed to pass. I stoped at 11 :)

Running 15 tests
Test 1: test isValidTx() with valid transactions
==> passed

Test 2: test isValidTx() with transactions containing signatures of incorrect data
==> passed

Test 3: test isValidTx() with transactions containing signatures using incorrect private keys
==> passed

Test 4: test isValidTx() with transactions whose total output value exceeds total input value
==> passed

Test 5: test isValidTx() with transactions that claim outputs not in the current utxoPool
==> passed

Test 6: test isValidTx() with transactions that claim the same UTXO multiple times
==> passed

Test 7: test isValidTx() with transactions that contain a negative output value
==> passed


Test 8: test handleTransactions() with simple and valid transactions
Total Transactions = 2
Number of transactions returned valid by student = 2
Total Transactions = 50
Number of transactions returned valid by student = 50
Total Transactions = 100
Number of transactions returned valid by student = 100
==> passed

Test 9: test handleTransactions() with simple but some invalid transactions because of invalid signatures
Total Transactions = 2
Number of transactions returned valid by student = 0
Total Transactions = 50
Number of transactions returned valid by student = 2
Total Transactions = 100
Number of transactions returned valid by student = 1
==> passed

Test 10: test handleTransactions() with simple but some invalid transactions because of inputSum < outputSum
Total Transactions = 2
Number of transactions returned valid by student = 2
Total Transactions = 50
Number of transactions returned valid by student = 25
Total Transactions = 100
Number of transactions returned valid by student = 42
==> passed

Test 11: test handleTransactions() with simple and valid transactions with some double spends
Total Transactions = 2
Number of transactions returned valid by student = 2
All transactions returned are not satisfied/valid
Total Transactions = 50
Number of transactions returned valid by student = 50
All transactions returned are not satisfied/valid
Total Transactions = 100
Number of transactions returned valid by student = 100
All transactions returned are not satisfied/valid
==> FAILED

Test 12: test handleTransactions() with valid but some transactions are simple, some depend on other transactions
Total Transactions = 2
Number of transactions returned valid by student = 1
Returned set is not a maximal set of transactions
Total Transactions = 50
Number of transactions returned valid by student = 16
Returned set is not a maximal set of transactions
Total Transactions = 100
Number of transactions returned valid by student = 53
Returned set is not a maximal set of transactions
==> FAILED

Test 13: test handleTransactions() with valid and simple but some transactions take inputs from non-exisiting utxo's
Total Transactions = 2
Number of transactions returned valid by student = 1
Total Transactions = 50
Number of transactions returned valid by student = 12
Total Transactions = 100
Number of transactions returned valid by student = 57
==> passed

Test 14: test handleTransactions() with complex Transactions
Total Transactions = 2
Number of transactions returned valid by student = 1
Returned set is not a maximal set of transactions
Total Transactions = 50
Number of transactions returned valid by student = 11
All transactions returned are not satisfied/valid
Total Transactions = 100
Number of transactions returned valid by student = 48
All transactions returned are not satisfied/valid
==> FAILED

Test 15: test handleTransactions() with simple, valid transactions being called again to check for changes made in the pool
Total Transactions = 2
Number of transactions returned valid by student = 2
Total Transactions = 50
Number of transactions returned valid by student = 50
All transactions returned are not satisfied/valid
Total Transactions = 100
Number of transactions returned valid by student = 100
All transactions returned are not satisfied/valid
==> FAILED


Total:11/15 tests passed!


