credit card pg 1
=====
balance = 4213
annualInterestRate = 0.2 
monthlyPaymentRate = 0.04
month = 1
totalPaid = 0

while month <= 12:
      minPayment = monthlyPaymentRate * balance #Compute the monthly payment, based on the previous month's balance.
      balance -=  minPayment #Update the outstanding balance by removing the payment,
      balance += (annualInterestRate/12.0)*balance #then charging interest on the result.
      print 'Month:',month #Output the month,
      print 'Minimum monthly payment:',round(minPayment,2) #the minimum monthly payment
      print 'Remaining balance:',round(balance,2) #and the remaining balance.
      totalPaid += minPayment #Keep track of the total amount of paid over all the past months so far.
      month += 1
print 'Total paid:', round(totalPaid,2) #Print out the result statement with the total amount paid
print 'Remaining balance:', round(balance,2) #and the remaining balance.
