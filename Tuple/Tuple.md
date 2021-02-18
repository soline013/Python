### List & Tuple.

```python
x = ('Hello', 'I', 'am', 'Sollie')
```

List와 Tuple의 유사점.

1. 순서가 있다.
2. Index로 접근할 수 있다.
3. 최댓값을 찾을 수 있다.
4. `for`문에서 List와 같이 원소를 순서대로 사용할 수 있다. 

List와 Tuple의 차이점.

1. 소괄호를 사용한다.
2. Immutable, 변경이 불가능하다.
3. 2번 속성으로 정렬이나 값을 추가하는 것 또한 불가능하다.

### Advantage of Tuple.

변경 불가능한 속성으로 Tuple은 List보다 효율적으로 동작한다.

1. 용량을 적게 차지한다.
2. 접근이 더 빠르다.

3. 임시 변수로 사용할 수 있다.

    좌변에 튜플을 사용하여 여러 변수에 값을 넣을 수 있다.

    ```python
    (x, y) = (0, 'zero')
    print(x)
    print(y)
    '''
    0
    zero
    '''
    ```

4. 소괄호를 사용하지 않아도 `,`로 값을 나열하면 튜플로 인식한다.

    ```python
    a, b = 1, 'one'
    print(a, b)
    '''
    1 one
    '''
    ```

5. 딕셔너리 처리에 활용할 수 있다.

    `.item()`은 딕셔너리의 키와 값을 한 쌍으로 튜플을 만들고, 그 튜플을 리스트 형태로 만든다.

    ```python
    d = dict()
    d['first'] = 0
    d['second'] = 1
    for (i, j) in d.items(): 
        print(i, j)
    '''
    first 0
    second 1
    '''

    p = d.items()
    print(p)
    '''
    dict_items([('first', 0), ('second', 1)])
    '''
    ```

6. 여러 값을 비교할 수 있다.

    왼쪽부터 비교하고, 값이 동일한 경우가 아니면 오른쪽으로 넘어가지 않는다.

    ```python
    (0, 1, 2) < (0, 1, 3)
    '''
    True
    '''

    (100, 1, 2) > (0, 100, 200)
    '''
    True
    '''
    ```