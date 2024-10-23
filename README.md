- 👋 Hi, I’m @Galal010
- 👀 I’m interested in ...
- 🌱 I’m currently learning ...
- 💞️ I’m looking to collaborate on ...
- 📫 How to reach me ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...

<!---
Galal010/Galal010 is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
response = requests.get(url, params=params)
if response.status_code == 200:
    data = response.json()
    if data:
        coin = data[0]
        print(f"Name: {coin['name']}")
        print(f"Symbol: {coin['symbol']}")
        print(f"Current Price: ${coin['current_price']}")
        print(f"Market Cap: ${coin['market_cap']}")
        print(f"24h Change: {coin['price_change_percentage_24h']}%")
    else:
        print("Cryptocurrency not found!")
else:
    print("Failed to fetch data!")
