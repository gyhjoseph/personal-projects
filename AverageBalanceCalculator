qns = input("Is it for this month? ")

if qns.upper()=="YES":
  today = date.today()
  today_str = today.strftime("%Y %m")
  year = int(today_str.split()[0]) # today's year in int
  month = int(today_str.split()[1]) # today's month in int
  mrange = monthrange(year, month)
  total_days = mrange[1]
else:
  year = int(input("Year? ")) # Year in four digits
  month = int(input("Month? ")) # Month in int from 1 to 12
  mrange = monthrange(year, month)
  total_days = mrange[1]

avgbal = float(input("Average balance required: ")) # What is the average balance
currentbal = float(input("What is your current balance? "))

uniquebalance = 0
qns1 = int(input("How many unique balance do you currently have? ")) # determining how many balance user has
current_total_days = 0
current_total_balance = 0

while uniquebalance < qns1:
  bal1 = float(input("balance: "))
  days = int(input("no. of days: "))
  current_total_days += days
  current_total_balance += bal1 * days
  uniquebalance += 1

fullmonthbalance = avgbal * total_days
balanceavg = (fullmonthbalance - current_total_balance) / (total_days - current_total_days)
totopup = balanceavg - currentbal
print("You need to maintain an average balance of:", balanceavg)
print("To top up this amount in order to maintain:", totopup)
