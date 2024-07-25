# Pandas

Pandas is a powerful Python library for data manipulation and analysis. It provides data structures like DataFrame and Series, which are designed to make data analysis fast and easy in Python.

### Frequently Used Methods

- `df.head(*n*)`: DataFrame의 첫 *n*개의 행을 반환합니다.
- `df.groupby(*column*)[*column*].sum()`: *column*을 기준으로 그룹화하여 숫자 열의 합을 계산합니다.
- `df.merge(*other*, *on=column*)`: *column*을 기준으로 DataFrame을 *other*와 병합합니다.
- `df.info()`: DataFrame에 대한 요약 정보를 표시합니다.
- `df.dropna()`: NaN 값을 포함하는 행을 제거합니다.
- `df.describe()`: DataFrame의 요약 통계를 표시합니다.
- `df.plot(*kind*, *x=*, *y=*)`: 지정된 종류의 그래프를 그립니다.
- `pd.read_csv(*filepath*, *sep=',', *header='infer'*)`: CSV 파일을 DataFrame으로 읽어옵니다.
- `df.to_csv(*filename*, *index=False*)`: DataFrame을 CSV 파일로 저장합니다.
- `df.apply(*function*)`: 함수를 열이나 행에 적용합니다.

### Frequently Used Commands

- `import pandas as pd`: Pandas를 임포트합니다.
- `pd.DataFrame((*data*, *index*, *columns*))`: 데이터에서 새로운 DataFrame을 생성합니다.
- `pd.Series((*data*, *index*))`: 데이터에서 새로운 Series를 생성합니다.
- `pd.concat((*objs*, *axis=0*)`: 객체들을 축을 따라 연결(concatenate)합니다.
- `pd.merge((*left*, *right*, *on=column*)`: 왼쪽 및 오른쪽 DataFrame을 *column*을 기준으로 병합합니다.
- `pd.to_datetime(*arg*, *format*)`: 문자열을 datetime으로 변환합니다.
- `pd.cut(*x*, *bins*)`: 연속형 변수를 여러 구간으로 나눕니다.
- `pd.get_dummies(*data*, *prefix*)`: 범주형 변수를 더미(dummy) 변수로 변환합니다.
- `pd.pivot_table(*data*, *values*, *index*, *columns*)`: 데이터의 피벗 테이블을 생성합니다.
- `pd.isnull(*obj*)`: 객체가 NaN인지 검사하여 불리언 배열을 반환합니다.
