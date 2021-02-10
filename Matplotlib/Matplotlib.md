# Matplotlib.

일반적으로 Numpy Array를 사용하는데, 사용하지 않아도 내부적으로 변환된다.

## matplotlib.pyplot

```python
import matplotlib.pyplot as plt
```

1. Matplotlib은 List의 값을 y값이라 생각하고, x값을 자동으로 만든다.

    ```python
    plt.plot([1, 2, 3, 4])
    plt.ylabel('y-label')
    plt.show()
    ```

2. 2개의 인자를 주면 x, y값이 되어 그래프를 그린다.

    ```python
    plt.plot([1, 2, 3, 4], [1, 4, 9, 16])
    plt.ylabel('y-label')
    plt.show()
    ```

3. 선의 색상과 형태를 지정할 수 있고, 축의 범위를 지정할 수 있다.

    ```python
    plt.plot([1, 2, 3, 4], [1, 4, 9, 16], 'ro')
    plt.axis([0, 6, 0, 20])
    plt.show()
    ```

    `.plot()`의 기본 포맷은 'b-'로 파란색(b)과 선(-)이다.

    'ro'는 빨간색(r)과 원형(o)이다.

    `.axis()`는 [xmin, xmax, ymin, ymax]로 사용한다.

4. 여러 개의 그래프를 그릴 수 있다.

    ```python
    import numpy as np

    t = np.arange(0., 5., 0.2)

    plt.plot(t, t, 'r--',
    				 t, t**2, 'bs',
    				 t, t**3, 'g^')
    plt.show()
    ```

## Method Archive.

- `.plot()`

    포맷: rgb, --, s, ^, o, -

- `.ylabel()`
- `.show()`
- `.asix()`

## 링크.

[위키독스](https://wikidocs.net/book/5011)