# a function to create random usernames

## Tested against Windows / Python 3.11 / Anaconda

## pip install genranddata



```python
Generate random data using a given function and input data, while ensuring uniqueness and handling exceptions.

Parameters:
	fu (callable): The function used to generate new data.
	data (Union[list, tuple]): The input data to be used in the generation process.
	created_already (list): A list of data that has already been created.
	limit (int): The maximum number of new data to be generated.
	**kwargs: Additional keyword arguments to be passed to the function.

Returns:
	list: A list of randomly generated data, with a length not exceeding the specified limit.
```
	


```python

from genranddata import create_random_data, load_data, save_data, genfunction

u = [
    "Agent",
    "Alex",
    "Alonzo",
    "Amon",
    "Angel",
    "Annie",
    "Anton",
    "August",
    "Bane",
    "Buddy",
    "Calvin",
    "Candyman",
    "Captain",
    "Catherine",
    "Chucky",
    "Colin",
    "Commodus",
    "Count",
    "Cruella",
    "Darth",
    "Davy",
    "Deadly",
    "Death",
    "Dolores",
    "Dr",
    "Elijah",
    "Erik",
    "Ernst",
    "Esther",
    "Frank",
    "Freddy",
    "Ghostface",
    "Godzilla",
    "Gollum",
    "Gordon",
    "Gozer",
    "Green",
    "HAL",
    "Harry",
    "Howard",
    "Immortan",
    "Ivan",
    "Jack",
    "Jason",
    "Jigsaw",
    "John",
    "Joker",
    "Judge",
    "Khan",
    "Koba",
    "Lee",
    "Lex",
    "Lil",
    "Lord",
    "Lots",
    "Maleficent",
    "Margaret",
    "Max",
    "Michael",
    "Miranda",
    "Miss",
    "Mrs",
    "Norman",
    "Nurse",
    "Palpatine",
    "Pazuzu",
    "Pennywise",
    "Predator",
    "Queen",
    "Raoul",
    "Regina",
    "Roger",
    "Roy",
    "Sauron",
    "Scar",
    "Shere",
    "Shooter",
    "T",
    "Terence",
    "Thanos",
    "The",
    "Ursula",
    "Vice",
    "William",
    "Xenomorphs",
]
empty = []
save_data(empty, "c:\\testusername.pkl")
already_created = load_data("c:\\testusername.pkl")
gendata = create_random_data(
    fu=lambda x, **kwargs: genfunction(x, **kwargs),
    data=u,
    created_already=already_created,
    limit=10,
    min_=2,
    max_=4,
    camel_case_percentage=20,
    uppercase_percentage=30,
    lowercase_percentage=30,
    join_values=("x", "_", ""),
    random_number_percentage=30,
    random_number_range=(0, 100),
)
print(gendata)
# ['maleficent_xenomorphs_alex_max', 'queenlexantonnorman', 'DarthxJack', 'WilliamMaxRaoulAlonzo', 'MissxIvanxCaptainxMax', 'SAURONFREDDYAGENTDR', 'CAPTAIN_JOHN_ROGER_GREEN', 'JOKERERIKFREDDYESTHER71', 'scar_roger_1', 'T_GHOSTFACE_ANGEL_4']



```