# 3.1 A deployment pipeline to heroku

[Project](https://github.com/Muugmaster/covid-tracker-react)

[Config](https://github.com/Muugmaster/covid-tracker-react/blob/main/.github/workflows/main.yml)

# 3.2

-

# 3.3 

[Frontend Dockerfile](./3.3/frontend/Dockerfile)

[Backend Dockerfile](./3.3/backend/Dockerfile)

Tested inside both containers with ``whoami`` and got ``appuser``

# 3.4

### Image sizes:
- Frontend: [1.17GB](./3.3/frontend/Dockerfile) -> [455MB](./3.4/frontend/Dockerfile)
- Backend: [1.01GB](./3.3/backend/Dockerfile) -> [447MB](./3.4/backend/Dockerfile)

# 3.5

### Image sizes:
- Frontend: [1.17GB](./3.3/frontend/Dockerfile) -> [343MB](./3.5/frontend/Dockerfile)
- Backend: [1.01GB](./3.3/backend/Dockerfile) -> [447MB](./3.5/backend/Dockerfile)

# 3.6 Multi-stage

- Frontend: [124MB](./3.6/frontend/Dockerfile)
- Backend: [18MB](./3.6/backend/Dockerfile)