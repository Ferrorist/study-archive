# 1주차 학습 목표

## Index
* [2025.11.24. - Python 문법 감 회복](#day-2025-11-24-python)
  * [List/Dict Comprehensions](./1week.md/#listdict-comprehensions)
  * [lambda 함수](./1week.md/#lambda-함수)
  * [enumerate](./1week.md/#enumerate)
  * [zip](./1week.md/#zip)
* [2025.11.25. - Numpy 기본](#day-2025-11-25-numpy)
  * [Numpy란?](./1week.md/#numpy란)
  * [ndarray 생성과 구조 이해](./1week.md/#ndarray-생성과-구조-이해)
  * [슬라이싱(Slicing)](./1week.md/#슬라이싱slicing)
  * [배열 연산](./1week.md/#배열-연산)
  * [브로드캐스팅(Broadcasting)](./1week.md/#브로드캐스팅broadcasting)
  * [Boolean Indexing (조건 필터링)](./1week.md/#boolean-indexing-조건-필터링)
  * [reshape와 axis 개념 (심화)](./1week.md/#reshape와-axis-개념-심화)
* [2025.11.27. - Pandas](#day-2025-11-27-pandas)


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

### Numpy란?
- NumPy는 Numerical Python의 약자로, 벡터화 연산, 브로드캐스팅, 다양한 수학 함수 등을 지원하여 데이터 분석, 머신러닝, 컴퓨터 비전 등 다양한 분야에서 널리 사용됩니다.
- 다차원 배열 객체인 **ndarray**를 제공하며, 대규모 데이터 처리를 효율적으로 수행할 수 있습니다.

> `ndarray` 는 연속된 메모리 블록을 사용하고 C 기반으로 수행되어 매우 빠르며 벡터 연산(배열 전체 연산)이 지원됨.<br>
그에 반면, 파이썬의 기본 리스트는 포인터 배열로 구현되어 있어 메모리 사용이 비효율적이고 속도가 느리며, 벡터 연산을 지원하지 않는다.

### ndarray 생성과 구조 이해

#### ndarray 생성
- numpy 배열은 `numpy.array()` 함수를 사용하여 생성할 수 있습니다.
```python
import numpy as np

a = np.array([1, 2, 3, 4, 5])  # 1차원 배열
b = np.array([[1, 2, 3], [4, 5, 6]])  # 2차원 배열
```

#### ndarray 주요 속성

| 속성 | 설명 |
| --- | --- |
| `ndarray.ndim` | 배열의 차원 수를 반환합니다. |
| `ndarray.shape` | 배열의 각 차원의 크기를 튜플로 반환합니다. |
| `ndarray.dtype` | 배열의 데이터 타입을 반환합니다. |
| `ndarray.size` | 배열의 총 요소 수를 반환합니다. |
| `ndarray.itemsize` | 배열의 각 요소가 차지하는 바이트 수를 반환합니다. |
| `ndarray.nbytes` | 배열이 차지하는 총 바이트 수를 반환합니다. |

예시)
```python
import numpy as np
arr = np.array([[1, 2, 3], [4, 5, 6]])
print(arr.ndim)      # 출력: 2
print(arr.shape)     # 출력: (2, 3)
print(arr.dtype)     # 출력: int64 (시스템에 따라 다를 수 있음)
print(arr.size)      # 출력: 6
print(arr.itemsize)  # 출력: 8 (int64 기준)
print(arr.nbytes)    # 출력: 48 (6 * 8)
```

### 슬라이싱(Slicing)
- Numpy 배열은 파이썬 리스트와 유사한 방식으로 슬라이싱할 수 있습니다.

```python
import numpy as np
arr = np.array([0, 1, 2, 3, 4, 5])
arr[1:4]    # [1, 2, 3]
arr[:3]     # [0, 1, 2]
arr[::2]    # [0, 2, 4]
```

- 다차원 배열의 경우, 각 차원에 대해 콤마(,)로 구분하여 슬라이싱할 수 있습니다.

```python
import numpy as np
arr = np.array([[0, 1, 2], [3, 4, 5], [6, 7, 8]])
arr[0, 1]      # 1
arr[1:, :2]    # [[3, 4], [6, 7]]
arr[:, 1]      # [1, 4, 7]
arr[::2, ::2]  # [[0, 2], [6, 8]]
```

### 배열 연산
- Numpy는 배열 간의 산술 연산을 지원하며, 이는 요소별로 수행됩니다.

```python
import numpy as np
a = np.array([1, 2, 3])
b = np.array([4, 5, 6])
print(a + b)  # [5, 7, 9]
print(a - b)  # [-3, -3, -3]
print(a * b)  # [4, 10, 18]
print(a / b)  # [0.25, 0.4, 0.5]
```

### 브로드캐스팅(Broadcasting)
  - 서로 다른 크기의 배열 간에도 연산이 가능하도록 자동으로 크기를 맞춰주는 기능입니다.

```python
import numpy as np
a = np.array([1, 2, 3])
b = 2
print(a + b)  # [3, 4, 5]

c = np.array([[1, 2, 3], [4, 5, 6]])
d = np.array([10, 20, 30, 40])
print(c + d)  # [[11, 22, 33], [14, 25, 36]]
```

### Boolean Indexing (조건 필터링)
- Boolean Indexing은 조건에 맞는 요소들만 선택할 때 사용됩니다.

```python
import numpy as np

arr = np.array([3, 8, 12, 4, 7])

arr > 5  # [False, True, True, False, True]

arr[arr > 5]  # [8, 12, 7]
```

```python
arr[arr % 2 == 0]  # [8, 12, 4]
arr[(arr > 3) & (arr < 10)]  # [8, 4, 7]
arr[(arr < 5) | (arr > 10)]  # [3, 12, 4]
```

- 다차원 배열에서도 동일하게 적용됩니다.

```python
import numpy as np
arr = np.array([[1, 2, 3], [4, 5, 6], [7, 8, 9]])
arr[arr > 4]  # [5, 6, 7, 8, 9]
```


### reshape와 axis 개념 (심화)

#### reshape 함수
- reshape 함수는 배열의 형태를 변경할 때 사용됩니다. 단, 전체 요소 수는 동일해야 합니다.

```python
import numpy as np
arr = np.array([[1, 2, 3], [4, 5, 6]])
reshaped_arr = arr.reshape(3, 2)  # (2, 3) -> (3, 2)

print(reshaped_arr)
# 출력:
# [[1 2]
#  [3 4]
#  [5 6]]
```

```python
import numpy as np
arr = np.array([1, 2, 3, 4], [5, 6])
reshaped_arr = arr.reshape(-1, 2)  # 자동으로 행 크기 계산
print(reshaped_arr)
# 출력:
# [[1 2]
#  [3 4]
#  [5 6]]
```

#### axis 개념
- axis는 다차원 배열에서 연산을 수행할 축을 지정하는 데 사용됩니다.
- axis=0은 행 방향(세로), axis=1은 열 방향(가로)을 의미합니다.

```python
import numpy as np
mat = np.array([1, 2, 3], [4, 5, 6])

mat.sum(axis=0)  # [5, 7, 9] - 각 열의 합
mat.sum(axis=1)  # [6, 15] - 각 행의 합
```


<a id="day-2025-11-27-pandas"></a>
## 2025.11.27. - Pandas

