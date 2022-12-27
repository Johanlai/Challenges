# Count the number of occurrences in a list
```python
def count_letters(lst):
    counter = {}
    sorted_counter = {}
    for i in lst:
        if i in counter.keys():
            counter[i] = counter[i]+ 1
        else: counter[i] = 1
    for i in sorted(counter.keys()):
        sorted_counter[i] = counter[i]
    return sorted_counter
```
```python
# Generating test cases
def random_letter():
    alphabet = ['A','B','C','D','E','F','G','H','I','J','K','L','M','N','O','P','Q','R','S','T','U','V','W','X','Y','Z']
    return alphabet[random.randint(0,25)]
def random_letter_list(num):
    lst = []
    for i in range(num):
        lst.append(random_letter())
    return lst

# Checking asnwers sum correctly - this should return 900
a = random_letter_list(900)
sum(count_letters(a).values())
```
