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
