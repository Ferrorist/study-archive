# 1주차 학습 목표

## Index
* [2025.11.24. - Python 문법 감 회복](#day-2025-11-24-python)
  * [List/Dict Comprehensions](./1week.md/#listdict-comprehensions)
  * [lambda 함수](./1week.md/#lambda-함수)
  * [enumerate](./1week.md/#enumerate)
  * [zip](./1week.md/#zip)
* [2025.11.25. - Numpy 기본](#day-2025-11-25-numpy)

<br><br>

<a id="day-2025-11-24-python"></a>
## 2025.11.24. - Python 문법 감 회복


### List/Dict Comprehensions

- List Comprehensions

해당 문법은 리스트를 간결하게 생성할 수 있는 방법입니다.
<br>주 표현식은 아래와 같습니다.
```python
[expression for item in iterable if condition]
```

예시 1) 1~10까지의 홀수 수의 제곱 리스트 생성
```python
squares = [x**2 for x in range(1, 11) if x % 2 != 0]
```

예시 2) 짝수만 뽑아서 리스트 생성
```python
evens = [x for x in range(31) if x % 2 == 0]
```


<br><br>

- Dict Comprehensions

딕셔너리를 간결하게 생성할 수 있는 방법입니다.<br>
주 표현식은 아래와 같습니다.
```python
{key_expression: value_expression for item in iterable if condition}
```

예시 1) 숫자 -> 제곱 딕셔너리 생성하기
```python
squares_dict = {x: x**2 for x in range(1, 11)}
```

예시 2) 문자열 리스트를 {문자열: 길이} 딕셔너리로 변환하기
```python
words = ['apple', 'banana', 'cherry']
word_dict = {word: len(word) for word in words}
```

예시 3) 0~10 숫자 중 홀수는 “odd”, 짝수는 “even”으로 매핑한 딕셔너리를 만들기
```python
odd_even_dict = {x: "odd" if x % 2 != 0 else "even" for x in range(11)}
```


### lambda 함수
- lambda 함수는 익명 함수로, **한 줄로 간단한 함수를 정의**할 때 사용됩니다.
- 기본 문법은 다음과 같습니다.

```python
lambda arguments: expression
```

예시 1) 입력된 값에 1을 더한 결과를 반환하는 함수
```python
lambda x: x + 1
```


* lambda 함수를 바로 실행하는 방식은 다음과 같습니다.
```python
(lambda x: x + 1)(5)  # 결과: 6
```


* **변수에 담아서 사용하는 방식** 또한 존재합니다.
```python
add_five = lambda x: x + 5
result = add_five(3)  # 결과: 8
```

<br><br>

이러한 lambda 함수를 흔히 사용하는 패턴은 아래와 같습니다.

1) 리스트 정렬 기준(key)으로 사용
```python
nums = [(1, 3), (2, 1), (5, 2)]
sorted_nums = sorted(nums, key=lambda x: x[1]) # 두 번째 요소를 기준으로 정렬됨.
```
<br>

2) map 함수와 함께 사용
- map 함수의 경우, 리스트의 각 요소에 대해 동일한 함수를 적용할 때 유용합니다.
- map의 return 값은 map 객체이므로, 이를 리스트로 변환하려면 list() 함수를 사용해야 합니다.
```python
nums = [1, 2, 3, 4]
result = list(map(lambda x: x * 2, nums)) # [2, 4, 6, 8]
```


<br>

3) filter 함수와 함께 사용
- filter 함수는 리스트에서 특정 조건을 만족하는 요소만 걸러낼 때 사용됩니다.
- filter의 return 값은 filter 객체이므로, 이를 리스트로 변환하려면 list() 함수를 사용해야 합니다.
```python
nums = [1, 2, 3, 4, 5, 6]
evens = list(filter(lambda x: x % 2 == 0, nums)) # [2, 4, 6]
```

<br>

4) Pandas와 함께 사용
- apply 함수는 DataFrame의 각 요소에 대해 함수를 적용할 때 사용됩니다.
```python
import pandas as pd # Pandas 라이브러리 임포트
df = pd.DataFrame({'A': [1, 2, 3], 'B': [4, 5, 6]})
df['C'] = df['A'].apply(lambda x: x * 10)  # 'A' 열의 값을 10배로 하는 'C' 열 생성
```

### enumerate
- enumerate는 리스트를 반복하면서 **(index, 값) 2개를 동시에** 다루고 싶을 때 사용합니다.<br>
기본 형태는 아래와 같습니다.
```python
for idx, value in enumerate(iterable, start=0):
    # index와 value를 사용한 코드
```

예시 1) 인덱스와 함께 값을 출력하기
```python
fruits = ['apple', 'banana', 'cherry']
for i, f in enumerate(fruits):
    print(i, f)
```
<br>

### zip
- zip 함수는 **두 개 이상의 리스트를 동시에 순회**하고 싶을 때 사용합니다.<br>
기본 형태는 아래와 같습니다.
```python
for a, b in zip(list1, list2):
    # a와 b를 사용한 코드
```

```python
for a, b, c in zip(list1, list2, list3):
    # a, b, c를 사용한 코드
```

예시 1) 두 리스트 병렬 처리
```python
names = ["Tom", "Amy", "John"]
ages = [20, 25, 22]

for n, a in zip(names, ages):
    print(f"{n} is {a} years old.")
```
<br>

예시 2) 세 리스트 병렬 처리
```python
names = ["Tom", "Amy", "John"]
ages = [20, 25, 22]
heights = [175, 160, 180]

for n, a, h in zip(names, ages, heights):
    print(f"{n} is {a} years old and {h} cm tall.")
```

<br>

예시 3) zip으로 딕셔너리 만들기
```python
keys = ['name', 'age', 'city']
values = ['Alice', 30, 'New York']

result = {k: v for k, v in zip(keys, values)}

result2 = dict(zip(keys, values))
```


<br>

예시 4) enumerate와 zip 조합
```python
names = ["Tom", "Amy", "John"]
ages = [20, 25, 22]

for idx, (name, age) in enumerate(zip(names, ages)):
    print(f"{idx}: {name} is {age} years old.")
```
zip 함수는 Iterator를 반환하므로 enumerate와 조합할 수 있는 것이며,<br>
필요에 따라 list()나 dict()로 변환하여 사용할 수 있습니다.

<br><br>

<a id="day-2025-11-25-numpy"></a>
## 2025.11.25. (화) - Numpy 기본
