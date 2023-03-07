# Variables

- MONGODB_USERNAME=my_user
- MONGODB_PASSWORD=password123
- MONGODB_DATABASE=my_database

- ALLOW_EMPTY_PASSWORD=yes
- MONGODB_ENABLE_JOURNAL=true

# Dockerfile

Run:

```bash
docker run --name mongodb bitnami/mongodb:latest
```

# docker-compose

```yaml
version: '3'

services:
  mongo:
    image: bitnami/mongodb:5.0.9
    network_mode: bridge
    environment:
      - ALLOW_EMPTY_PASSWORD=yes
      - MONGODB_DATABASE=nabu
      - MONGODB_USERNAME=ChaosHead
      - MONGODB_PASSWORD=Kaliber44
    ports:
     - '27017:27017'
    volumes:
      - ./mongo/data:/bitnami/mongodb/data

```
