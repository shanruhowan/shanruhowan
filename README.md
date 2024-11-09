- 👋 Hi, I’m @shanruhowan
- 👀 I’m interested in ...
- 🌱 I’m currently learning ...
- 💞️ I’m looking to collaborate on ...
- 📫 How to reach me ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...

<!---
shanruhowan/shanruhowan is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
import http.client

conn = http.client.HTTPSConnection("wordsapiv1.p.rapidapi.com")

headers = {
    'x-rapidapi-key': "2886fd6e9fmsh87f54e1a6bfc485p174183jsnaf42afad950e",
    'x-rapidapi-host': "wordsapiv1.p.rapidapi.com"
}

conn.request("GET", "/words/lovely/synonyms", headers=headers)

res = conn.getresponse()
data = res.read()

print(data.decode("utf-8"))
