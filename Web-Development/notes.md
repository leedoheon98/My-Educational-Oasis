# Contents
 1. [Flask](#Flask)
 2. [HTML](#HTML)

## Flask

### 주요 메서드
1. **render_template()**
    - **역할**: HTML 파일을 렌더링하여 클라이언트에게 반환합니다.
    - **사용성**: 주로 템플릿 파일(HTML)을 사용하여 웹 페이지를 구성하고 데이터를 삽입할 때 사용합니다.
    - **예시**:
      ```python
      from flask import Flask, render_template

      app = Flask(__name__)

      @app.route('/')
      def home():
          return render_template('index.html', title='Home Page')
      ```

2. **redirect()**
    - **역할**: 사용자를 다른 URL로 리다이렉트합니다.
    - **사용성**: 사용자가 특정 작업을 수행한 후 다른 페이지로 이동시키거나, 특정 조건 하에서 URL을 변경할 때 사용합니다.
    - **예시**:
      ```python
      from flask import Flask, redirect

      app = Flask(__name__)

      @app.route('/')
      def home():
          return redirect('/new-url')
      ```

3. **url_for()**
    - **역할**: Flask 애플리케이션 내의 함수 이름을 사용하여 URL을 생성합니다.
    - **사용성**: URL 하드코딩을 피하고 동적으로 URL을 생성할 때 사용합니다.
    - **예시**:
      ```python
      from flask import Flask, url_for

      app = Flask(__name__)

      @app.route('/')
      def home():
          return 'Home Page'

      @app.route('/about')
      def about():
          return 'About Page'

      with app.test_request_context():
          print(url_for('home'))  # Output: /
          print(url_for('about'))  # Output: /about
      ```

4. **request**
    - **역할**: 클라이언트로부터 전달된 HTTP 요청 데이터를 접근할 수 있게 해줍니다.
    - **사용성**: GET, POST 등의 요청 데이터에 접근하고 처리할 때 사용합니다.
    - **예시**:
      ```python
      from flask import Flask, request

      app = Flask(__name__)

      @app.route('/submit', methods=['POST'])
      def submit():
          username = request.form['username']
          return f'Hello, {username}!'
      ```

5. **jsonify()**
    - **역할**: JSON 응답을 생성하여 클라이언트에게 반환합니다.
    - **사용성**: API 엔드포인트에서 JSON 데이터를 반환할 때 사용합니다.
    - **예시**:
      ```python
      from flask import Flask, jsonify

      app = Flask(__name__)

      @app.route('/api/data')
      def get_data():
          data = {'name': 'Alice', 'age': 30}
          return jsonify(data)
      ```

이 메서드들은 Flask 애플리케이션 개발에서 매우 유용하게 사용되며, 각 메서드는 특정한 역할을 수행합니다. Flask의 유연성과 간결함 덕분에 빠르고 효율적인 웹 애플리케이션을 개발할 수 있습니다.

---------------------------------------------------

## HTML

### HTML에서 자주 사용되는 주요 태그들


1. **`<p>`**: 단락(paragraph)을 나타내는 태그로, 텍스트를 문단 단위로 구분합니다.

2. **`<a>`**: 앵커(anchor) 태그로, 하이퍼링크를 생성합니다. `href` 속성을 통해 링크 대상을 지정할 수 있습니다.

3. **`<img>`**: 이미지를 삽입하는 태그입니다. `src` 속성으로 이미지 파일의 경로를 지정하고, `alt` 속성으로 대체 텍스트를 제공합니다.

4. **`<ul>`**, **`<ol>`**, **`<li>`**: 순서 없는 목록(unordered list), 순서 있는 목록(ordered list), 리스트 아이템(list item)을 각각 나타냅니다.

5. **`<div>`**: 구역을 나누는 데 사용되는 블록 요소입니다. 주로 CSS 스타일링을 위해 사용되며, 그 자체로는 시맨틱 의미가 없습니다.

6. **`<span>`**: 인라인 요소로, 특정 부분의 텍스트나 인라인 요소들을 그룹화하는 데 사용됩니다.

7. **`<form>`**, **`<input>`**, **`<textarea>`**, **`<button>`**: 웹 폼을 생성하는 데 사용되는 태그들입니다. `<form>`은 폼을 정의하고, `<input>`은 입력 필드를, `<textarea>`는 여러 줄의 텍스트 입력을, `<button>`은 버튼을 생성합니다.

8. **`<table>`**, **`<tr>`**, **`<td>`**: 테이블을 생성하는 태그들로, 각각 테이블 전체, 행, 셀을 나타냅니다.

9. **`<header>`**, **`<footer>`**, **`<nav>`**, **`<main>`**, **`<section>`**: HTML5에서 도입된 시맨틱 요소들로, 각각 문서의 헤더, 푸터, 내비게이션, 주요 콘텐츠 영역, 섹션을 나타냅니다.

10. **`<strong>`**, **`<em>`**: 강조를 나타내는 태그로, 각각 굵은 글씨체와 이탤릭체를 사용하여 텍스트를 강조합니다.

11. **`<br>`**, **`<hr>`**: `<br>`은 줄바꿈을, `<hr>`은 수평선을 삽입합니다.

---------------------------------------------------
