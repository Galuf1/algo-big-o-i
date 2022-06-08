# Big O Answers



## Snippet 1 -
### Big O:
Time Complexity = O(n)
Space Complexity = O(1)
### Explanation:
In the worst case scenario it will loop once through the entire array, so it scales with the size of it.
Same as above, we store one variable that changes value while looping, so it doesn't store any extra space.

```python
def largest(array, value):
  for item in array:
    if item > value:
      return False
  return True 
```


## Snippet 2 -
### Big O:
Time Complexity = O(n)
Space Complexity = O(1)
### Explanation:
The function loops in the worst case twice through the dictionary, making it O(2n) that woudl translate in O(n)
For space complexity we don't add any extra space since we are printing the value each loop.

```python
def info_dump(customers):
  
  print('Customer Names:')
  for customer in customers: 
    print(customer['name'])
  
  print('Customer Locations:')
  for customer in customers: 
    print(customer['country'])
  
```

## Snippet 3 -
### Big O:
Time Complexity = O(1)
Space Complexity = O(1)
### Explanation:
Lists are represented as an array in python, so unless we change the size of the array the time it takes would be just assignign a new value to the space alocated.
Same as TC modifying a list in python doesn't add any space since we don't need to create a copy of it.

```python
def first_element_is_red(array):
  return array[0] == 'red' 
```

## Snippet 4 -
### Big O:
Time Complexity = O(n^2)
Space Complexity = O(n)
### Explanation:
The TC is quadratic because it nests 2 O(n) operations, resulting in O(n^2).
for SC enumerate creates a list of tuples with the index and value, being in worst case scenario as big as the first list. 

```python
def duplicates(array):
  for index1, item1 in enumerate(array):
    for index2, item2 in enumerate(array):
      if index1 == index2:
        continue
      if item1 == item2:
        return True
  return False
``` 

## Snippet 5 -
### Big O:
Time Complexity = O(n^2)
Space Complexity = O(1)
### Explanation:
TC is quadratic because we nest 2 O(n) operations, resulting in O(n^2)
SC if O(1) because we don't store any other data than the input

```python
words = ['chocolate', 'coconut', 'rainbow']
endings = ['cookie', 'pie', 'waffle']

for word in words:
  for ending in endings:
    print(word + ending)

```

## Snippet 6 -
### Big O:
Time Complexity = O(n)
Space Complexity = O(1)
### Explanation:
The for loop only goes once through the list so it's TC is O(n)
For SC it doesn't store anything else than the inputs.

```python
numbers = [1,2,3,4,5,6,7,8,9,10]

def print_array(array):
  for item in array:
    print(item)

```

## Snippet 7 -
### Big O:
Time Complexity = O(n^2)
Space Complexity = O(1)
### Explanation:
TC is quadratic because every element has to be compared with the next (O(n)) and then change the index of potentially all the array (O(n)) so it becomes O(n^2)
For SC it does everything in-place so it doesn't store any extra arrays 

```python
# this is insertion sort
def insertionSort(arr): 
  for i in range(1, len(arr)): 
    key = arr[i] 
    j = i-1
    while j >=0 and key < arr[j] : 
      arr[j+1] = arr[j] 
      j -= 1
    arr[j+1] = key 
```

## Snippet 8 -
### Big O:
Time Complexity = O(n^2)
Space Complexity = O(1)
### Explanation:
TC it nests 2 for loops of O(n) complexity and the rest are all O(1) operations, it becomes O(n^2)
SC is O(1) because it doesn't store anything extra, it just keeps changing values in-place

```python
for i in range(len(my_list)):
  min_idx = i
  for j in range(i+1, len(my_list)):
      if my_list[min_idx] > my_list[j]:
          min_idx = j

  my_list[i], my_list[min_idx] = my_list[min_idx], my_list[i]
```
