# actions logger

### Install dependencies
```bash
npm install
```

### Prepare database
collection: `actions`

indexes:
```json
{"id": 1}
```

```json
{"text": 1}
```

```json
{"text": "text"}
```

### Run
```bash
APP_PORT=3000 JWT_KEY=jwtsecretkey JWT_TTL=2592000 ADMIN_TOKEN=admintokenkey MONGODB_URI=mongodb://ubuntu-server:27017 node index.js
```

### Create account
```bash
curl -X POST \
  http://localhost:8080/api/auth/register \
  -H 'Connection: keep-alive' \
  -H 'Content-Length: 71' \
  -H 'Content-Type: application/json' \
  -H 'Host: localhost:8080' \
  -d '{
	"username":"admin",
	"password":"pasword",
	"token":"admintokenkey"
	
}'
```
