# BUG-10: Буруу JSON биеттэй POST хүсэлтэд 400 биш 200 OK буцааж байна

**Орчин:** Уншлагын жагсаалт v2.0, Node.js v24.19.0, Ubuntu Linux, 2026-10-23 14:57
**Урьдчилсан нөхцөл:** `node app.js` ажиллаж байна.

## Дахин гаргах алхам
1. Терминал дээр дараах командыг ажиллуулна:
```bash
mkdir -p evidence

curl -i -X POST http://localhost:3000/api/books \
  -H 'Content-Type: application/json' \
  -d 'буруу оролт' \
  2>&1 | tee evidence/bug-10-curl.txt