*Introduction to Currency Converter Code*                    
This code is a simple currency converter tool that allows users to convert amounts between different currencies using current exchange rates. It utilizes the `forex_python` library to access real-time exchange rates and provides a user-friendly interface for input and output.

*Key Features:*

- Converts between various currencies using current exchange rates
- Supports a wide range of currencies
- Displays the result with the currency symbol

*How to Use:*

1. Install the `forex_python` library using `pip install forex_python`.
2. Run the code and follow the prompts to enter the currency to convert from, the currency to convert to, and the amount.
3. The code will display the converted amount with the currency symbol.                                
*What the code does:*

1. Asks you to enter:               
    - The currency you want to convert *from* (e.g., USD).
    - The currency you want to convert *to* (e.g., EUR).
    - The amount you want to convert (e.g., 100).
2. Uses a special library (forex_python) to get the current exchange rate.
3. Converts the amount using the exchange rate.
4. Shows you the result (e.g., 100 USD = 88 EUR €).

*How it works:*

1. We import the library that helps us with currency conversions.
2. We ask the user for input (currencies and amount).
3. We use the library to convert the amount.
4. We show the result.          This code is a simple tool that helps you convert currencies using current exchange rates. 
# Currency-converter-using-python from forex_python.converter import CurrencyRates, CurrencyCodes

print("Currency Converter")
print("Supported currencies: https://forex-python.readthedocs.io/en/latest/currencysource.html")

c = CurrencyRates()
cc = CurrencyCodes()

from_currency = input("Enter the currency to convert from (e.g., USD, EUR, INR): ").upper()
to_currency = input("Enter the currency to convert to (e.g., USD, EUR, INR): ").upper()
amount = float(input("Enter the amount: "))

result = c.convert(from_currency, to_currency, amount)
symbol = cc.get_symbol(to_currency)

print(f"{amount} {from_currency} = {result} {to_currency} {symbol}")
