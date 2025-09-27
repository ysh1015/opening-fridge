
## 🛠️ 기술 스택

### Backend
* Java 17
* Spring Boot 3.5.6
* Spring Data JPA (Hibernate)
* MySQL
* Lombok

### Frontend
* React 19.1.1
* Vite
* Axios
* React Router DOM
* React Icons

### Common
* Git & GitHub
* IntelliJ IDEA
* Visual Studio Code

##  실행 방법

### 1. 사전 준비

프로젝트를 실행하기 위해 아래 프로그램들이 반드시 설치되어 있어야 함

* Git
* Java (JDK) 17 이상
* Node.js 18 이상 (LTS 버전 권장)
* MySQL Server
* (선택) IntelliJ IDEA, MySQL Workbench

### 2. 초기 설정

1.  **프로젝트 클론**
    ```bash
    git clone [https://github.com/YourUsername/your-repository.git](https://github.com/YourUsername/your-repository.git)
    cd your-repository
    ```

2.  **데이터베이스 생성**
    MySQL에 접속하여 아래 명령어로 프로젝트에서 사용할 데이터베이스(스키마)를 생성
    ```sql
    CREATE SCHEMA `opening-fridge` CHARACTER SET utf8mb4 COLLATE utf8mb4_general_ci;
    ```

### 3. 백엔드 실행 (IntelliJ)

1.  IntelliJ에서 `backend-web` 폴더를 프로젝트로 열기
2.  `src/main/resources/` 경로에 **`application-secret.properties`** 파일을 새로 생성
3.  생성한 파일에 아래 내용을 작성하고, 실제 OpenAI API 키를 입력합니다. (이 파일은 `.gitignore`에 의해 관리되지 않음.)
    ```properties
    # src/main/resources/application-secret.properties
    openai.api.key=sk-xxxxxxxxxxxxxxxxxxxxxxxx
    ```
4.  `src/main/resources/application.properties` 파일을 열어 자신의 MySQL `username`과 `password`가 올바른지 확인
5.  메인 클래스(`...Application.java`)를 찾아 실행(▶️)
6.  콘솔에 `Tomcat started on port(s): 8080` 메시지가 나타나면 성공

### 4. 프론트엔드 실행 (터미널)

1.  새로운 터미널을 열고 프론트엔드 폴더로 이동
    ```bash
    cd frontend-web
    ```

2.  필요한 라이브러리를 설치
    ```bash
    npm install
    ```

3.  개발 서버를 실행
    ```bash
    npm run dev
    ```

4.  웹 브라우저를 열고 주소창에 `http://localhost:5173` 을 입력하여 접속
