# Contents
1. [Pandas](#Pandas)
2. [MatplotLib](#MatplotLib)
3. [Seaborn](#Seaborn)

## Pandas

### DataScience 에서 25%, 50%, 75% 의 범위를 중요하게 여기는 이유  
  > *=사분위 범위 (IQR, Interquartile Range)*
  
#### 데이터 분포 이해

1. **중앙값 (50퍼센타일)**:
   - 중앙값은 데이터의 중간 지점을 나타내며, 데이터의 중심 경향을 나타냅니다.
   - 중앙값은 특히 데이터에 극단값(outliers)이 있을 때 평균보다 더 신뢰할 수 있는 척도입니다.

2. **1사분위수 (25퍼센타일)와 3사분위수 (75퍼센타일)**:
   - 이 값들은 데이터의 하위 25%와 상위 25%를 구분합니다.
   - 데이터의 범위와 분포를 이해하는 데 도움을 줍니다.
   - 1사분위수와 3사분위수의 차이인 사분위 범위(IQR)는 데이터의 산포도를 측정하는 데 사용됩니다.

#### 이상치 탐지

- **사분위 범위 (IQR)**:
  - IQR은 1사분위수와 3사분위수의 차이로, 데이터의 중간 50%를 포함합니다.
  - IQR을 이용해 이상치를 탐지할 수 있습니다. 일반적으로, 데이터가 \( Q1 - 1.5 \times IQR \) 보다 작거나 \( Q3 + 1.5 \times IQR \) 보다 큰 경우 이상치로 간주됩니다.

#### 데이터의 분포와 변동성 파악

- 퍼센타일을 통해 데이터가 어떻게 퍼져 있는지, 중심으로부터 얼마나 분산되어 있는지를 알 수 있습니다.
- 이러한 정보는 데이터의 변동성을 이해하고, 데이터 분석 및 모델링 시 중요한 결정을 내리는 데 도움을 줍니다.

#### 실용적인 예시

- **예산 관리**: 가구 소득의 25퍼센타일, 50퍼센타일, 75퍼센타일을 분석하면 소득의 분포를 이해하고, 정책 결정을 내릴 때 참고할 수 있습니다.
- **의학 연구**: 환자의 검사 결과에서 25퍼센타일, 50퍼센타일, 75퍼센타일을 확인하여 일반적인 건강 상태를 평가할 수 있습니다.
- **교육 데이터**: 학생 성적의 퍼센타일을 통해 성적 분포를 파악하고, 교육 프로그램의 효과를 평가할 수 있습니다.

#### 결론

Pandas가 `describe()` 함수에 25퍼센타일, 50퍼센타일, 75퍼센타일을 포함시키는 이유는 이러한 통계가 데이터의 분포, 중심 경향, 변동성을 이해하는 데 중요한 역할을 하기 때문입니다. 이러한 통계는 데이터 분석에서 기본적이고 필수적인 정보를 제공하며, 데이터의 특성을 파악하고 분석 결과를 해석하는 데 큰 도움을 줍니다.


---
### How to Handle Input and Output in Pandas

pandas.DataFrame  <-->  csv | excel  file
```
# read_csv()
import pandas as pd
df = pd.read_csv('data.csv')

# to_csv()
import pandas as pd
df = pd.to_csv('data.csv', index=False)   # index=True로 할 시 csv나 excel 파일에 의도치 않은 임의 인덱스가 추가될 수 있음.

# read_excel()
import pandas as pd
df = pd.read_excel('data.xlsx')

# to_excel()
import pandas as pd
df = pd.to_excel('data.xlsx', index=False)   # index=True로 할 시 csv나 excel 파일에 의도치 않은 임의 인덱스가 추가될 수 있음.
```
DataFrame Browse
```
# head
df.head()        >> Args : n= ( number, default=5 )

# tail
df.tail()        >> Args : n= ( number, default=5 )

# describe       >> Generate descriptive statistics
df.describe()

# info           >> Print a concise summary of a DataFrame
df.info()
```


## MatplotLib

- Matplotlib 에서 color 확인하기
```
import matplotlib.colors as mcolors

print(mcolors.CSS4_COLORS.keys())
```

---

- Google Colab에서 Matplotlib을 사용할 때 한글 깨짐 현상을 해결하는 법
```
#### install fonts-nanum
!sudo apt-get install -y fonts-nanum
!sudo fc-cache -fv
!rm ~/.cache/matplotlib -rf

#### 사용 예시
import matplotlib.pyplot as plt
plt.rc('font', family='NanumBarunGothic')
```
### 명령어 설명

1. `!sudo apt-get install -y fonts-nanum`
    - `sudo apt-get install`: 새로운 소프트웨어 패키지를 설치하는 명령어입니다.
    - `-y`: 사용자에게 설치 여부를 묻지 않고 자동으로 "예"라고 응답하는 옵션입니다.
    - `fonts-nanum`: 설치하려는 특정 폰트 패키지입니다. 여기서는 나눔 폰트를 설치합니다.
    
    이 명령어는 나눔 폰트를 설치하여 `matplotlib`에서 한글 폰트를 사용할 수 있도록 합니다.

2. `!sudo fc-cache -fv`
    - `fc-cache`: 시스템의 폰트 캐시를 재생성하는 명령어입니다.
    - `-f`: 강제로 캐시를 재생성하는 옵션입니다.
    - `-v`: 상세한 정보를 출력하는 옵션입니다.
    
    이 명령어는 설치된 폰트를 시스템에 인식시키기 위해 사용됩니다.

3. `!rm ~/.cache/matplotlib -rf`
    - `rm`: 파일이나 디렉토리를 삭제하는 명령어입니다.
    - `~/.cache/matplotlib`: `matplotlib`의 캐시 디렉토리입니다.
    - `-r`: 재귀적으로 디렉토리와 그 안의 모든 파일을 삭제하는 옵션입니다.
    - `-f`: 강제로 삭제하는 옵션입니다.
    
    이 명령어는 `matplotlib`의 캐시를 삭제하여 폰트 설정이 제대로 반영되도록 합니다.

### 한글 깨짐 현상의 원인

구글 코랩과 같은 환경에서 시각화를 할 때 한글이 깨지는 이유는 기본적으로 설치된 폰트에 한글이 포함되지 않아서입니다. 따라서 `matplotlib`이 기본적으로 사용하는 폰트가 한글을 지원하지 않아 한글이 깨져 보이는 것입니다.

### 이 코드를 새로운 파일에서 매번 실행해야 하는 이유

구글 코랩의 경우, 세션이 종료되면 설치된 패키지나 폰트 설정이 초기화됩니다. 따라서 세션이 다시 시작될 때마다 한글 폰트를 다시 설치하고 설정해야 합니다. 매번 새로운 파일을 만들 때 이 코드를 실행하는 이유는 그 때문입니다.

### 요약

- `sudo apt-get install -y fonts-nanum`: 나눔 폰트를 설치합니다.
- `sudo fc-cache -fv`: 폰트 캐시를 재생성합니다.
- `rm ~/.cache/matplotlib -rf`: `matplotlib` 캐시를 삭제하여 변경된 폰트 설정을 반영합니다.
- 구글 코랩에서 시각화 도구를 사용할 때 한글 깨짐 현상이 발생하는 이유는 기본 폰트가 한글을 지원하지 않기 때문입니다.
- 세션이 종료되면 설정이 초기화되므로, 새로운 파일에서 시각화를 할 때마다 폰트 설정 코드를 실행해야 합니다.

이렇게 하면 구글 코랩에서 `matplotlib`을 사용할 때 한글이 정상적으로 표시될 것입니다.

---





## Seaborn
- Seaborn 에서 color 확인하기
```
import seaborn as sns

sns.palettes.SEABORN_PALETTES.keys()
```
