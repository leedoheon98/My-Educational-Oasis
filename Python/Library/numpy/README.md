## `np.random.normal`과 `np.random.randn` 함수의 차이점

- `np.random.normal`은 평균과 표준편차를 직접 지정할 수 있어 편리합니다.
- `np.random.randn`은 표준 정규 분포를 생성하며, 다른 평균과 표준편차가 필요한 경우 변환이 필요합니다.
  
### `np.random.normal`

`np.random.normal` 함수는 평균과 표준편차를 명시적으로 지정할 수 있는 정규 분포를 생성합니다.

```python
np.random.normal(loc=0.0, scale=1.0, size=None)
```

- `loc`: 정규 분포의 평균 (기본값은 0.0)
- `scale`: 정규 분포의 표준편차 (기본값은 1.0)
- `size`: 생성할 샘플의 크기 (예: (m, n) 형태로 지정 가능)

### `np.random.randn`

`np.random.randn` 함수는 평균이 0이고 표준편차가 1인 표준 정규 분포를 생성합니다. 이 함수는 `size` 인자만 받을 수 있습니다.

```python
np.random.randn(d0, d1, ..., dn)
```

- `d0, d1, ..., dn`: 생성할 샘플의 크기

### 비교 예제

#### `np.random.normal` 사용

```python
mean = 50
std_dev = 10
num_samples = 100
data = np.random.normal(mean, std_dev, num_samples)
```

위 코드는 평균이 50, 표준편차가 10인 정규 분포에서 100개의 샘플을 생성합니다.

#### `np.random.randn` 사용

`np.random.randn` 함수는 표준 정규 분포(평균 0, 표준편차 1)에서 값을 생성하므로, 원하는 평균과 표준편차로 변환해야 합니다.

```python
mean = 50
std_dev = 10
num_samples = 100
data = mean + std_dev * np.random.randn(num_samples)
```

위 코드는 먼저 평균이 0, 표준편차가 1인 표준 정규 분포에서 100개의 샘플을 생성한 후, 이를 원하는 평균과 표준편차로 변환합니다.
