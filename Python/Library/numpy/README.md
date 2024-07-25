# NumPy

NumPy is a fundamental package for numerical computing in Python. It provides support for large, multi-dimensional arrays and matrices, along with a collection of mathematical functions to operate on these arrays efficiently.

### Frequently Used Methods

- `np.array(*object*)`: 객체(예: 리스트)에서 배열을 생성합니다.
- `np.mean(*array*, *axis*)`: 지정된 축을 기준으로 배열의 평균을 계산합니다.
- `np.random.rand(*dims*)`: 지정된 차원의 난수 배열을 생성합니다.
- `np.zeros((*shape*,), *dtype*)`: 지정된 모양과 타입의 0으로 채워진 배열을 생성합니다.
- `np.sum(*array*, *axis*)`: 지정된 축을 기준으로 배열의 합을 계산합니다.
- `np.argmax(*array*, *axis*)`: 지정된 축을 기준으로 배열의 최댓값의 인덱스를 반환합니다.
- `np.concatenate((*arrays*, *axis*)`: 배열들을 지정된 축을 기준으로 연결(concatenate)합니다.
- `np.linalg.inv(*array*)`: 배열의 역행렬을 계산합니다.
- `np.fft.fft(*array*)`: 배열의 고속 푸리에 변환을 수행합니다.
- `np.where(*condition*, *x*, *y*)`: 조건에 따라 배열의 요소를 선택합니다.

### Frequently Used Commands

- `import numpy as np`: NumPy를 임포트합니다.
- `np.arange(*start*, *stop*, *step*)`: 지정된 간격으로 일정한 값을 가진 배열을 생성합니다.
- `np.linspace(*start*, *stop*, *num*)`: 지정된 개수의 점들이 균일하게 분포된 배열을 생성합니다.
- `np.reshape(*array*, *newshape*)`: 배열의 모양을 변경합니다.
- `np.save(*filename*, *array*)`: 배열을 디스크에 저장합니다.
- `np.loadtxt(*filename*, *delimiter*)`: 파일에서 데이터를 읽어 배열로 반환합니다.
- `np.corrcoef(*array*)`: 배열의 상관 계수 행렬을 계산합니다.
- `np.mean(*array*)`: 배열의 평균을 계산합니다.
- `np.std(*array*)`: 배열의 표준 편차를 계산합니다.
- `np.argmax(*array*)`: 배열에서 최대값의 인덱스를 반환합니다.
