## 확률

### 데카르트의 곱(Cartesian Product)
> Python : `itertools.product()`

데카르트의 곱(Cartesian product)은 두 집합 사이의 모든 가능한 조합을 나타내는 수학적 연산입니다. 데카르트의 곱은 두 집합 A와 B가 있을 때, A의 각 원소와 B의 각 원소를 순서쌍(pair)으로 묶어 모든 조합을 만들어내는 것입니다.

수학적으로 데카르트의 곱은 다음과 같이 표현됩니다:

\[ A \times B = \{(a, b) \mid a \in A, b \in B\} \]

여기서 \((a, b)\)는 순서쌍(pair)을 나타내며, \(a \in A\)는 집합 A의 원소를 의미하고, \(b \in B\)는 집합 B의 원소를 의미합니다.

예를 들어, 집합 A가 \(\{1, 2\}\)이고 집합 B가 \(\{a, b, c\}\)일 경우, 이 두 집합의 데카르트의 곱은 다음과 같습니다:

\[ \{ (1, a), (1, b), (1, c), (2, a), (2, b), (2, c) \} \]

즉, 모든 가능한 조합을 나열한 것입니다.

파이썬에서는 `itertools.product()` 함수를 사용하여 두 개 이상의 iterable(반복 가능한 객체)의 데카르트의 곱을 구할 수 있습니다. 예를 들어:

```python
import itertools

A = [1, 2]
B = ['a', 'b', 'c']

cartesian_product = list(itertools.product(A, B))
print(cartesian_product)
```

이 코드는 리스트 A와 리스트 B의 데카르트의 곱을 구하여 출력합니다.
