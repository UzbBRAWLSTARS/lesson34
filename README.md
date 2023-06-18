# lesson34
data = {"Model" : "Malibu", "Rang" : "Qora", "Yil":2020, "Narh":40000}
data = {"Model": "Malibu", "Rang": "Qora", "Yil": 2020, "Narh": 40000}
data_json = json.dumps(data, indent=4)

# 2
@@ -21,24 +21,23 @@
print(f"{talaba['ism']} {talaba['familiya']}")

# 3
with open('javoblar/data.json','w') as f:
    json.dump(data,f)
with open("javoblar/data.json", "w") as f:
    json.dump(data, f)

with open('javoblar/talaba.json','w') as f:
    json.dump(talaba,f)
with open("javoblar/talaba.json", "w") as f:
    json.dump(talaba, f)

# 4 Students
with open('javoblar/students.json') as f:
with open("javoblar/students.json") as f:
    data = json.load(f)

for item in data['student']:
    print(f"{item['name']} {item['lastname']}."
          f" Faculty of {item['faculty']} ")
for item in data["student"]:
    print(f"{item['name']} {item['lastname']}." f" Faculty of {item['faculty']} ")

# 5 Wikipedia

with open('javoblar/wikipedia.json') as f:
with open("javoblar/wikipedia.json") as f:
    wiki = json.load(f)

print(wiki['query']['pages']['13801']['title'])
print(wiki['query']['pages']['13801']['extract'])
print(wiki["query"]["pages"]["13801"]["title"])
print(wiki["query"]["pages"]["13801"]["extract"])
