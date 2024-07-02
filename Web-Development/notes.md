
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
