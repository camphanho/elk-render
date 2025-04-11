# ELK Stack on Render

## Components:
- Elasticsearch (runs as Background Service)
- Kibana (runs as Web Service)

## Deploy Guide:
1. Fork this repo
2. Update `render.yaml` with your GitHub repo URL
3. Go to Render.com > "New Blueprint" > Paste your repo
4. Deploy services

## Test Logs:
You can test sending a log like this:

```bash
curl -X POST http://<your-elasticsearch-url>:9200/app-logs/_doc -H "Content-Type: application/json" -d '{
  "timestamp": "2025-04-11T10:00:00Z",
  "level": "INFO",
  "message": "Test log",
  "service": "test-service"
}'

