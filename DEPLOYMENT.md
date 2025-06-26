# MLX API 서버 사용 가이드

`app/mlx_api_server.py`는 FastAPI 기반의 로컬 LLM API 서버입니다. 
로컬 환경에서 모델을 띄운 뒤, 별도의 클라우드 애플리케이션에서 HTTP로 접근할 때 활용합니다.

## 실행 방법

```bash
python app/mlx_api_server.py --port 8000
```

서버가 시작되면 `/generate` 엔드포인트로 POST 요청을 보내 문장을 생성할 수 있습니다.

```bash
curl -X POST -H "Content-Type: application/json" \
     -d '{"prompt": "안녕하세요"}' \
     http://localhost:8000/generate
```

`Ctrl+C`로 서버를 종료합니다.

