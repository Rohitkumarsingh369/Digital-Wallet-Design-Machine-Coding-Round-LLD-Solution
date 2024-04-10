# Digital-Wallet-Design-Machine-Coding-Round-LLD-Solution

## Requirements of Digital Wallet System

Let’s first understand the requirements and the problem statement.
### Mandatory Requirements
•	You are supposed to create a digital wallet system that allows people to transfer amounts between their wallets.
•	The wallet uses its own currency known as FkRupee(F₹).
•	The account balance cannot drop below F₹ 0.00.
•	The smallest amount that can be transferred between wallets is 0.0001.
•	The user should be presented with options for each action. And the options are as follows:
1.	Create Wallet – This option should create a wallet for the user.
2.	Transfer Amount – This option should enable the transfer of funds from one account to the other.
3.	Account Statement – This option should display the account statement for the specified user.
4.	Overview – This option should display all the account numbers currently in the system. Additionally, it should show the current balances for these accounts.
5.	Exit – The system should exit.
## Optional Requirements
These are the requirements that are not mandatory, but good to have. Let’s go through the optional requirements.
1.	Offer 1 – When the amount is transferred from user A to user B, F₹ 10 must be added to both the sender and receiver wallets if their balance is the same.
2.	Offer 2 – Whenever Offer 2 is selected, the top 3 customers with the highest number of transactions will get F₹ 10, F₹ 5, and F₹ 2 as rewards. If there is a tie between customers, i.e., if customers have the same number of transactions, then the customer having higher account balance should be given preference. If there is still a tie, i.e., the customers have the same balance, then the customer whose account was created first should be given preference.
3.	Add one more option called FixedDeposit <fd_amount>. And whenever the option is selected, an amount equal to <fd_amount> is parked for. If for the next 5 transactions, the account balance for that account remains above <fd_amount>, the user gets F₹ 10 as interest in their account. And if the account balance goes below <fd_amount>, then the FD should be dissolved and the user would need to give the FixedDeposit command again to start a new FD.
4.	Consider another added bonus, display the <fd_amount> and remaining transactions in the Overview and Statement command also.
## Approaching the Problem
During the interview, focus mainly on the mandatory requirements. Because there’s no point in fulfilling optional requirements without taking care of all the mandatory requirements first. So if time permits, you can take a look at the optional requirements. And implement some of these to give you an extra edge. But you should design such that any new changes can be incorporated with as minimal changes as possible.
Now that we have discussed the problem statement, don’t jump down to the solution directly. First, take a moment to think about how you will approach the problem. And think about:
•	Which entities or classes will you include in your design?
•	What will be the data members in these classes?
•	How many service classes do you need in your design?
•	What data structure will you use to store the data?
Better yet, try to come up with a solution of your own first. Since you’ll be able to learn better that way. And after you have a solution ready, you can go through the code below.
## Breaking Down the Requirements
Now that we have all the requirements for a digital wallet design clear, we need to drill down the requirements to understand it better.
Let’s look at the mandatory requirements first.
1.	Create Wallet – We need to accept the name of the user and the amount that should be there in the wallet for the user as inputs from the user.
2.	Transfer Amount – For transfering any amount, we need the sender information, the receiver information, and the amount to be transfered. And these parameters will be taken from the user.
3.	Account Statement – We will need to accept the account number as input. And the account statement should contain the current balance and the list of transactions the user has performed to date.
4.	Overview – We need no other input as it will display the current balances for all the accounts curently in the system.
5.	Exit – Simple to implement. No other inputs needed.
   
Now let’s look at the optional requirements one by one.
1.	Offer 1 can be easily added by comparing the sender and receiver balance and add F₹ 10 to each wallet if the balances are same.
2.	Offer 2 can be incorporated by implementing a priority queue and having the logic for all three conditions in a Comparator.
3.	Fixed Deposit can be implemented by having an extra method to take care of the fixed deposit logic.
4.	Displaying FD amount can be implemented by make small changes in the overview and statement methods.

