# python-task2
portfolio = {}
def add_stock(ticker, shares):
 portfolio[ticker] = portfolio.get(ticker, 0) + shares
def remove_stock(ticker):
 if ticker in portfolio:
 del portfolio[ticker]
def show_portfolio():
 print("Your Portfolio:")
 for ticker, shares in portfolio.items():
 print(f"{ticker}: {shares} shares")
while True:
 print("\n1. Add Stock\n2. Remove Stock\n3. View Portfolio\n4. Exit")
 choice = input("Enter choice: ")
 if choice == '1':
 t = input("Ticker: ").upper()
 s = int(input("Shares: "))
 add_stock(t, s)
 elif choice == '2':
 t = input("Ticker to remove: ").upper()
 remove_stock(t)
 elif choice == '3':
 show_portfolio()
 elif choice == '4':
 break
