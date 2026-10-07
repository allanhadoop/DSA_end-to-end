
#------------------Access rules-----------------

| Structure                | Called                   | How to access                      |
| ------------------------ | ------------------------ | ---------------------------------- |
| `[1, 2, 3]`              | List of numbers          | `for x in data`                    |
| `["Sam", "Tim"]`         | List of strings          | `for x in data`                    |
| `[[1,2], [3,4]]`         | List of lists            | `for row in data` → `row[0]`       |
| `[(1,2), (3,4)]`         | List of tuples           | `for a,b in data`                  |
| `[{"a":1}, {"b":2}]`     | List of dictionaries     | `for d in data` → `d.items()`      |
| `[{1,2}, {3,4}]`         | List of sets             | `for s in data` → `for x in s`     |
| `{"a": 1, "b": 2}`       | Dictionary               | `data["a"]` / `data.items()`       |
| `{"a":[1,2], "b":[3,4]}` | Dictionary of lists      | `data.items()` → loop through list |
| `{"a":{"x":1}}`          | Nested dictionary        | `data["a"]["x"]`                   |
| `[{"a":[1,2]}]`          | List → dictionary → list | `for d in data` → `d["a"]` → loop  |

| Code     | Type       | Meaning                        |
| -------- | ---------- | ------------------------------ |
| `(1, 2)` | Tuple      | Two values in a fixed sequence |
| `{1, 2}` | Set        | Two unique values              |
| `{1: 2}` | Dictionary | Key `1` → Value `2`            |


#----------------Hash Map-----------The Hash Map acts like our memory of previously seen numbers.---------

| Scenario                 | Simplified meaning                               | Example                                 |   |
| ------------------------ | ------------------------------------------------ | --------------------------------------- | - |
| Store a person's details | Key → Value                                      | `{"name": "John", "age": 30}`           |   |
| Student ID lookup        | Find a value using an ID                         | `{101: "Rahul", 102: "Priya"}`          |   |
| Product price            | Product → Price                                  | `{"Laptop": 75000, "Mouse": 1200}`      |   |
| Count items              | Keep track of how many times something occurs    | `{"apple": 3, "banana": 2}`             |   |
| Check existence          | Quickly check whether something exists           | `"Rahul" in students`                   |   |
| Word frequency           | Count how often each word appears                | `{"AI": 5, "Python": 3}`                |   |
| Remove duplicates        | Keep only unique values                          | `{101, 102, 103}`                       |   |
| Group data               | Put related items together                       | `{"Pune": ["A", "B"], "Mumbai": ["C"]}` |   |
| Find duplicates          | Identify values appearing more than once         | `[10,20,10,30,20]` → `10,20`            |   |
| Two-sum problem          | Find two numbers that add to a target            | `[2,7,11,15]`, target `9` → `2+7`       |   |
| Cache                    | Remember previously calculated results           | `{"100+200": 300}`                      |   |
| User session lookup      | Find user information using session ID           | `{"ABC123": "John"}`                    |   |
| Anagram detection        | Check whether two words contain the same letters | `"listen"` / `"silent"`                 |   |
| Sliding window           | Track information in a moving section of data    | Last 5 transactions                     |   |
| LRU Cache                | Keep frequently/recently used data               | Browser/API cache                       |   |
| Graph representation     | Store connections between objects                | `{"A": ["B","C"]}`                      |   |
| Dependency lookup        | Find what depends on what                        | `{"Python": ["NumPy","Pandas"]}`        |   |
| Database-style indexing  | Quickly find records using an ID                 | `patient_id → patient_record`           |   |
| Distributed caching      | Store/retrieve data across multiple servers      | User/session → server data              |   |
| AI/RAG metadata lookup   | Quickly connect documents/chunks to metadata     | `chunk_id → document/page/source`       | _ |


#-----------Dictionary methods ------------
| Method              | Simple explanation                | Example                        | Result                    |
| ------------------- | --------------------------------- | ------------------------------ | ------------------------- |
| **`.get()`**        | Get a value safely                | `d.get("age", 0)`              | `25` or `0` if missing    |
| **`.keys()`**       | Get all keys                      | `d.keys()`                     | `name, age`               |
| **`.values()`**     | Get all values                    | `d.values()`                   | `John, 25`                |
| **`.items()`**      | Get key + value pairs             | `d.items()`                    | `name → John`, `age → 25` |
| **`.update()`**     | Add or change multiple values     | `d.update({"age": 30})`        | Updates age               |
| **`.pop()`**        | Remove a key and return its value | `d.pop("age")`                 | `25`                      |
| **`.popitem()`**    | Remove the last key-value pair    | `d.popitem()`                  | `("age", 25)`             |
| **`.setdefault()`** | Get value; if missing, create it  | `d.setdefault("city", "Pune")` | Adds city if missing      |
| **`.clear()`**      | Remove everything                 | `d.clear()`                    | `{}`                      |
| **`.copy()`**       | Make a copy                       | `d.copy()`                     | New dictionary            |
| **`.fromkeys()`**   | Create dictionary from keys       | `dict.fromkeys(["a","b"], 0)`  | `{"a":0,"b":0}`           |

#-------Difference between set and hash map 
|                  | Set                     | Dictionary / Hash Map                   |
| ---------------- | ----------------------- | --------------------------------------- |
| Stores           | Values                  | Key → Value                             |
| Example          | `{101, 102, 103}`       | `{101: True, 102: True, 103: True}`     |
| Duplicate values | Automatically removed   | Duplicate **keys** removed              |
| Lookup           | `101 in my_set`         | `101 in my_dict`                        |
| Useful when      | Only need unique values | Need unique values **plus information** |
| Hashing used?    | ✅ Yes                   | ✅ Yes                                   |
