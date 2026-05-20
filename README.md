# HR Onboarding Config

Centralized configuration repository for the HR Onboarding microservices project.

## Default Ports

| Service | Default Port | Environment Override |
|---|---:|---|
| api-gateway | 8080 | `API_GATEWAY_PORT` |
| auth-service | 8081 | `AUTH_SERVICE_PORT` |
| employee-service | 8082 | `EMPLOYEE_SERVICE_PORT` |
| application-service | 8083 | `APPLICATION_SERVICE_PORT` |
| housing-service | 8084 | `HOUSING_SERVICE_PORT` |
| email-service | 8085 | `EMAIL_SERVICE_PORT` |
| eureka-server | 8761 | `EUREKA_SERVER_PORT` |
| config-server | 8888 | `CONFIG_SERVER_PORT` |

## Notes

- Do not commit real secrets, passwords, API keys, JWT secrets, or production database URLs.
- Use environment variables for sensitive values.
- Service config files must match each service's `spring.application.name`.
  - Example: `employee-service` loads `employee-service.yml`.
- Shared settings should go in `application.yml`.
- Service-specific settings should go in `<service-name>.yml`.
