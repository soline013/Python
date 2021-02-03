Python에서 행렬이나 다차원 배열을 쉽게 처리할 수 있도록 배열 작업을 제공하는 라이브러리이다.

Pandas가 Numpy를 기본으로 한다.

ndarray라는 특수 데이터 타입을 사용한다.

# Function Achive.

`.array()` : ndmin으로 임의 차원 생성.

`.ndim` : 배열의 차원 확인.

`.arange()` : like Python's range, but returns an array.

`.linspace(A, B, n)` : create an array with n equally spaced points starting with A and ending with B.

`.sqrt()` : $\sqrt{}$ Operation.

`.sin()` : sin Operation.

`.cos()` : cos Operation.

`.tan()` : tan Operation.

`.zeros(int)` : Create an array with int, all value is 0.

`.ones()`

`.eye()` : nxn의 단위 배열 생성.

`np.reshape(a, shape, order)` `a.reshape(shape, order)` : Gives a new shape.

- shape: (layer, row, column)

- e.g.
    (100, ) → (2, 50)
    (100, ) → (4, -1) → (4, 25)

- [numpy.reshape - NumPy v1.19 Manual](https://numpy.org/doc/stable/reference/generated/numpy.reshape.html)


`.shape` : print shape of array.

`.size` : print only the number of value.

`.argmax()` : 입력 값으로 들어온 매트릭스의 각 행/열의 최댓값의 인덱스를 산출한다. Axis = 를 추가하면 열별(0) 혹은 행별(1) 최댓값 위치를 알 수 있다.

`.T` : 백터를 Transpose 한다.

`.random.rand()` : n개의 실수 랜덤 생성.

`.random.randn()` : n개의 Gaussian 랜덤 생성.

`.random.randint()`

`.random.choice(n, m)` : 0~n-1까지 숫자에서 중복 포함하여 m개 선택. replace=Flase로 중복 제거. p=[]로 확률 지정.

`.matmul()` : 행렬곱

`.dot()` : 행렬곱

`.cross` : 벡터의 외적