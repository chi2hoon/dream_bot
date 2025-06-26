# MLX API 서버 실행 가이드

`mlx_api_server.py`는 로컬에서 MLX 언어 모델을 제공하기 위한 FastAPI 기반 서버입니다. 
클라우드 앱 또는 다른 애플리케이션에서 HTTP 요청을 통해 이 서버를 호출하여 LLM 기능을 사용할 수 있습니다.

## 실행 방법
1. 필요한 패키지 설치
   ```bash
   pip install -r requirements.txt
   ```
2. 서버 실행
   ```bash
   python mlx_api_server.py
   ```
   기본 포트는 `8000`이며 `MLX_SERVER_PORT` 환경 변수로 변경할 수 있습니다.
3. API 문서 확인
   브라우저에서 `http://localhost:8000/docs`에 접속하면 Swagger UI가 열립니다.

## 주요 엔드포인트
- `GET /` : 헬스 체크 및 모델 정보 반환
- `POST /generate` : 프롬프트를 받아 텍스트 생성
- `POST /chat` : ChatGPT 스타일 채팅 인터페이스

해당 서버를 로컬에서 실행한 뒤, 필요에 따라 ngrok 등으로 외부에 노출하여 클라우드 환경과 연동할 수 있습니다.
