- Matplotlib 에서 color 확인하기
```
import matplotlib.colors as mcolors

print(mcolors.CSS4_COLORS.keys())
```

---

- Google Colab에서 Matplotlib을 사용할 때 한글 깨짐 현상을 해결하는 법
```
# install fonts-nanum
!sudo apt-get install -y fonts-nanum
!sudo fc-cache -fv
!rm ~/.cache/matplotlib -rf

# 사용 예시
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
