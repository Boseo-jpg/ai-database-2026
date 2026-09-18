# FastAPI

## 개요

- FastAPI - Python으로 API 서버를 만드는 웹 프레임워크
- API - Application Programing Interface
- 사용자(클라이언트)가 웹, 모바일, 앱에서 요청을 하면 FastAPI 서버가 요청을 처리, 결과를 돌려줌
- JSON 타입으로(파이썬 딕셔너리와 유사) 결과 리턴

  * 예시
    ```plaintext
    사용자(클라이언트)
    -> GET /students 요청
    -> FastAPI 서버에서 DB 조회
    -> 학생목록 결과 JSON으로 응답
    ```
- 클라이언트(요청 Request) -> 서버(응답 Response)

### FastAPI 특징

- Python 문법으로 API를 만들 수 있음
- 비교적 코드가 간결
- 실행속도가 빠름
- 테스트를 위한 UI를 자동으로 만들어줌
- Pydantic 사용, 요청과 응답 데이터를 검증할 수 있음
- PostSQL, MySQL, Oracle 등 여러 DB와 연동이 쉬움

### API 서버

클라이언트 요청을 받아 필요한 작업을 수행, 그 결과를 클라이언트에게 돌려주는 프로그램

## 개발환경 설정

### FastAPI 패키지 설치

```bash
pip install fastapi uvicorn
```

- 현재 파이썬에 fastapi와 unicorn 패키지를 설치
- fastapi 개발 가능

```bash
pip list
```

- 패키지 설치 확인

### 기초 FastAPI 서버

- 소스 작성
- VS Code

### 문제해결

- 설치한 uvicorn.exe 위치가 Python 설치 위치와 상이
- C:\Users\User\AppData\Roaming\Python\Python314\Scripts 경로가 시스템 경로에 등록되어있어야 함
- 시스템 속성(sysdm.cpl) - 환경변수 - 시스템변수 - path - 새로만들기 - 파이썬 경로 추가( C:\Users\User\AppData\Roaming\Python\Python314\Scripts )
- VS Code, 터미널 재시작

### FastAPI 서버 시작

```bash
uvicorn main:app --reload --port 8000
```

- `--reload` : 수정되면 곧바로 반영되어 서버 재시작
- `--port 8000` : 서버를 시작할 포트 지정
- http://127.0.0.1:8000 메세지 확인
  * 127.0.0.1 -> localhost