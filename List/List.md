# List Basic.

1. List는 순서가 있고, 수정 가능한 객체의 집합이다.
2. `[]`를 사용하고, `,`로 내부 원소를 구분한다.
3. Index는 0부터 시작하며, Index 범위를 벗어나면 에러가 발생한다.

    Index는 음수도 가능하며, -1로 가장 마지막 원소를 탐색할 수 있다.

    ```python
    a = [1, 2, 3, 4]
    a[0]
    '''c'''

    a[4]
    '''IndexError: list index out of range'''

    a[-1]
    '''4'''
    ```

4. `list()`, `[]`로 선언할 수 있고, 빈 List를 만들 수 있다.

    ```python
    b = list()
    b
    '''[]'''

    c = []
    c
    '''[]'''
    ```

5. `+`로 List를 합칠 수 있다.

    ```python
    [1, 3, 5] + [7, 9]
    '''[1, 3, 5, 7, 9]'''
    ```

6. `*`로 LIst를 반복할 수 있다.

    List 반복은 얕은 복사이다.

    4가 첫 번째 원소가 아니라 모든 원소에 추가된다.

    ```python
    b = a * 2
    b
    '''[1, 2, 3, 4, 1, 2, 3, 4]'''

    c = [[1, 2, 3]] * 2
    c
    '''[[1, 2, 3], [1, 2, 3]]'''

    c[0].append(4)
    c
    '''[[1, 2, 3, 4], [1, 2, 3, 4]]'''
    ```

7. 마지막 원소 뒤에 `,`를 남겨도 에러가 발생하지 않는다.

    편의를 위해 권장되기도 한다.

    ```python
    ['가',
     '나',
     '다',
     '라',]
    '''['가', '나', '다', '라']'''
    ```

8. List 내에 다른 List를 내포할 수 있다.

    ```python
    [1, [2, 3], 4]
    ```

9. 대괄호 안에 조건문, 반복문을 넣는 것으로 List를 선언할 수 있다.

    반복을 위한 변수가 필요없다면 `_`를 사용한다.

    ```python
    #x = [_ for _ in range(10)]
    x = [for i in range(10)]
    x
    '''[0, 1, 2, 3, 4, 5, 6, 7, 8, 9]'''
    ```

# List Slicing.

```python
y = [1, 2, 3, 4]
y[0:3]
'''[1, 2, 3]'''

y[0:] '''[1, 2, 3, 4]'''
y[:4] '''[1, 2, 3, 4]'''
y[:] '''[1, 2, 3, 4]'''
```

```python
y_ = [1, 2, 3, 4, 5]
y_[::2]
'''[1, 3, 5]'''
```

`[StartIndex : EndIndex-1 : Step]`로 슬라이싱할 수 있다.

Index를 생략할 수 있고, 모든 Index를 생략하면 모든 원소를 가리킨다.

Step을 지정하면 Step만큼 원소를 건너뛴다.

# List & String.

```python
abc = 'one two three'
split = abc.split()
split
'''['one', 'two', 'three']'''

abc2 = 'first;second;third'
split2 = abc2.split(';')
split2
'''['first', 'second', 'third']'''
```

문자열을 Split하여 리스트로 만들 수 있다.

명시적으로 구분자를 넣을 수 있고, Default 값은 빈 칸이다.

# Method.

1. `dir()` : 특정 타입에서 사용할 수 있는 메서드를 확인해보자.

    ```python
    x = list()
    dir(x)
    '''
    ['__add__',
     '__class__',
     '__contains__',
     '__delattr__',
     '__delitem__',
     '__dir__',
     '__doc__',
     '__eq__',
     '__format__',
     '__ge__',
     '__getattribute__',
     '__getitem__',
     '__gt__',
     '__hash__',
     '__iadd__',
     '__imul__',
     '__init__',
     '__init_subclass__',
     '__iter__',
     '__le__',
     '__len__',
     '__lt__',
     '__mul__',
     '__ne__',
     '__new__',
     '__reduce__',
     '__reduce_ex__',
     '__repr__',
     '__reversed__',
     '__rmul__',
     '__setattr__',
     '__setitem__',
     '__sizeof__',
     '__str__',
     '__subclasshook__',
     'append',
     'clear',
     'copy',
     'count',
     'extend',
     'index',
     'insert',
     'pop',
     'remove',
     'reverse',
     'sort']
    '''
    ```

2. `.append()` : List에 원소 하나를 추가한다.

    시간복잡도 O(1)

    ```python
    app = []
    for i in range(10):
        app.append(i)
    app
    '''[0, 1, 2, 3, 4, 5, 6, 7, 8, 9]'''
    ```

3. `.sort()` : List를 오름차순, 내림차순 정렬한다.

    시간복잡도 O(N|logN)

    `reverse` Parameter로 오름차순과 내림차순을 결정한다.

    ```python
    sort_ = [0, 2, 1, 3, 4, 5]
    sort_.sort()
    sort_
    '''[0, 1, 2, 3, 4, 5]'''

    sort_.sort(reverse=True)
    sort_
    '''[5, 4, 3, 2, 1, 0]'''
    ```

4. `.reverse()` : 원소의 순서를 반대로 돌린다.

    시간복잡도 O(N)

    ```python
    rev = ['Sollie', 'am', 'I', 'Hello,']
    rev.reverse()
    rev
    '''['Hello,', 'I', 'am', 'Sollie']'''
    ```

5. `.insert(Index, Value)` : 특정 Index에 원소를 추가한다.

    시간복잡도 O(N)

    ```python
    ins = [1, 3, 4, 5]
    ins.insert(1, 2)
    ins
    '''[1, 2, 3, 4, 5]'''

    ins = [1, 3, 4, 5]
    ins.insert(2, 2)
    ins
    '''[1, 3, 2, 4, 5]'''
    ```

6. `.count(Value)` : 특정 값을 갖는 원소의 개수를 센다.

    시간복잡도 O(N)

    ```python
    cnt = [1, 1, 3, 3, 3, 3]
    cnt.count(1)
    '''2'''

    cnt.count(3)
    '''4'''
    ```

7. `.remove(Value)` : 특정 값을 갖는 원소를 하나 제거한다.

    시간복잡도 O(N)

    ```python
    rem = [1, 2, 3, 3, 4, 5]
    rem.remove(3)
    rem
    '''[1, 2, 3, 4, 5]'''
    ```

# 링크.

[위키독스](https://wikidocs.net/16036)

[[LECTURE] 리스트의 개념 및 특징 : edwith](https://www.edwith.org/python-data/lecture/24389/)