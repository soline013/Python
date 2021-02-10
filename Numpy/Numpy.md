# Numpy.

Python에서 행렬이나 다차원 배열을 쉽게 처리할 수 있도록 배열 작업을 제공하는 라이브러리이다.

Pandas가 Numpy를 기본으로 한다.

ndarray라는 특수 데이터 타입을 사용한다.

## Method Achive.

- `.array(Array)` : ndmin으로 임의 차원 생성.

    ```python
    a = np.array([[1, 2, 3], [4, 5, 6], [7, 8, 9]])

    '''
    [[1, 2, 3],
     [4, 5, 6],
     [7, 8, 9]]
    '''
    ```

- `.shape` : Print shape of array.

    ```python
    a.shape
    '''(3, 3)'''
    ```

- `.ndim` : 배열의 차원 확인.

    ```python
    a.ndim
    '''2'''
    ```

- `.size` : Print only the number of value.

    ```python
    a.size
    '''9'''
    ```

- `.arange()` : Like Python's range, but returns an array.
- `.linspace(A, B, n)` : Create an array with n equally spaced points starting with A and ending with B.
- `.sqrt(Array & Value)` : $\sqrt{}$ Operation.

    ```python
    sq = np.array([[4, 9, 16, 25, 36]])
    np.sqrt(sq)
    '''
    array([[2., 3., 4., 5., 6.]])
    '''
    ```

- `.sin(Array & Value)` : sin Operation.

    ```python
    sin = np.array([[1, 2, 3, 4, 5]])
    np.sin(sin)
    '''
    array([[ 0.84147098,  0.90929743,  0.14112001, -0.7568025 , -0.95892427]])
    '''
    ```

- `.cos(Array & Value)` : cos Operation.

    ```python
    cos = np.array([[1, 2, 3, 4, 5]])
    np.cos(cos)
    '''
    array([[ 0.54030231, -0.41614684, -0.9899925 , -0.65364362,  0.28366219]])
    '''
    ```

- `.tan(Array & Value)` : tan Operation.

    ```python
    tan = np.array([[1, 2, 3, 4, 5]])
    np.tan(tan)
    '''
    array([[ 1.55740772, -2.18503986, -0.14254654,  1.15782128, -3.38051501]])
    '''
    ```

- `.zeros(Int & Shape)` : Create an array with int, all value is 0.

    ```python
    zero = np.array([[0, 1, 2], [3, 4, 5]])
    np.zeros(zero.shape)
    '''
    array([[0., 0., 0.],
           [0., 0., 0.]])
    '''
    ```

- `.ones(Int & Shape)` : Create an array with int, all value is 1.

    ```python
    one = np.array([[0, 1, 2], [3, 4, 5]])
    np.ones(one.shape)
    '''
    array([[1., 1., 1.],
           [1., 1., 1.]])
    '''
    ```

- `.eye(Int)` : nxn의 단위 배열 생성.

    ```python
    np.eye(5)
    '''
    array([[1., 0., 0., 0., 0.],
           [0., 1., 0., 0., 0.],
           [0., 0., 1., 0., 0.],
           [0., 0., 0., 1., 0.],
           [0., 0., 0., 0., 1.]])
    '''
    ```

- `np.reshape(a, Shape, Order)` `a.reshape(Shape, Order)`

    Returns a new shape.
    
    Shape: (Layer, Row, Column)

    ```python
    re = np.array([[0, 1, 2], [3, 4, 5]])

    '''
    [[0, 1, 2],
     [3, 4, 5]]
    '''

    np.reshape(re, (3, -1))
    re.reshape((3, 2))
    '''
    array([[0, 1],
    			 [2, 3],
    			 [4, 5]])
    '''
    ```

    [numpy.reshape - NumPy v1.19 Manual](https://numpy.org/doc/stable/reference/generated/numpy.reshape.html)

- `.argmax()` : 입력 값으로 들어온 매트릭스의 각 행/열의 최댓값의 인덱스를 산출한다. Axis = 를 추가하면 열별(0) 혹은 행별(1) 최댓값 위치를 알 수 있다.
- `.T` : 백터를 Transpose 한다.

    ```python
    trans = np.array([[0, 1, 2], [3, 4, 5]])
    trans.T
    '''
    array([[0, 3],
           [1, 4],
           [2, 5]])
    '''
    ```

- `.random.rand(Int)` : n개의 실수 랜덤 생성.

    ```python
    np.random.rand(10)
    '''
    array([0.41004371, 0.91811612, 0.00207011, 0.59976347, 0.63789971,
           0.61340129, 0.87340208, 0.71286851, 0.78616908, 0.1695464 ])
    '''
    ```

- `.random.randn(Int)` : n개의 Gaussian 랜덤 생성.

    ```python
    np.random.randn(10)
    '''
    array([-0.35474985, -0.65075913, -1.18868158,  2.49054771, -0.98557701,
           -0.3647411 ,  0.79287963, -2.10699111,  0.74246506, -0.37143223])
    '''
    ```

- `.random.randint()`
- `.random.choice(n, m)` : 0 ~ n-1까지 숫자에서 중복을 포함하여 m개 선택.

    n은 정수이고, m에는 정수나 Shape을 사용할 수 있다.

    `replace=False`로 중복을 제거할 수 있다..

    `p=[]`로 확률을 지정한다.

    ```python
    np.random.choice(11, (5, 5))
    '''
    array([[ 9,  0,  9, 10,  4],
           [10,  7,  9,  7,  4],
           [ 9,  2,  1,  9,  2],
           [ 2,  9,  6,  2,  3],
           [ 2,  4,  3,  8,  9]])
    '''
    ```

- `.matmul()` : 행렬곱, `dot()`과는 고차원에서 차이가 있다.

    ```python
    x = np.random.rand(100).reshape((25, 4))
    w = np.random.rand(4).reshape((4, 1))
    np.matmul(x, w)
    '''
    array([[0.6449001 ],
           [0.99408303],
           [0.96405953],
           [0.69654436],
           [0.58150398],
           [0.28720983],
           [0.69909046],
           [0.42956958],
           [0.93871271],
           [0.9800108 ],
           [0.6254399 ],
           [0.52119103],
           [0.6898989 ],
           [0.86724435],
           [0.59989556],
           [0.37699432],
           [0.30600389],
           [0.8138587 ],
           [0.68190398],
           [0.73888991],
           [0.48896222],
           [0.4016816 ],
           [0.22528171],
           [1.10922737],
           [0.9996311 ]])
    '''
    ```

- `.dot()` : 행렬곱, `matmul()`과는 고차원에서 차이가 있다.

    ```python
    x_ = np.random.rand(100).reshape((25, 4))
    w_ = np.random.rand(4).reshape((4, 1))
    np.dot(x_, w_)
    '''
    array([[0.67915413],
           [0.20920437],
           [0.59246331],
           [1.16759548],
           [0.36421287],
           [0.79071213],
           [0.93781223],
           [0.52232919],
           [1.05894393],
           [0.99955061],
           [0.53736207],
           [0.45980341],
           [0.38131211],
           [1.24101434],
           [1.12468511],
           [0.79666945],
           [1.0139016 ],
           [1.37849185],
           [0.64201136],
           [0.7696302 ],
           [0.69805316],
           [0.6775801 ],
           [0.75776226],
           [0.93272334],
           [1.24549546]])
    '''
    ```

- `.cross` : 벡터의 외적