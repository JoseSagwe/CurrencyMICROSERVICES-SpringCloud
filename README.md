# CurrencyMICROSERVICES-SpringCloud
# Currency Exchange and Conversion Microservices

This project is a microservices-based application for currency exchange and conversion. It includes multiple microservices, a naming server, and an API gateway.

## Project Structure

The project is structured as follows:

- **currency-exchange-service**: A microservice responsible for providing currency exchange rates.
- **currency-conversion-service**: A microservice for currency conversion using exchange rates from the exchange service.
- **api-gateway**: The API gateway for routing requests to the appropriate microservices.
- **naming-server**: A naming server (Eureka) for service discovery.
- **LoggingFilter**: A global filter for logging requests in the API gateway.

## Microservices

### Currency Exchange Service

The currency exchange service provides exchange rates for various currencies. It exposes REST endpoints to retrieve exchange rates.

### Currency Conversion Service

The currency conversion service performs currency conversion based on exchange rates obtained from the exchange service. It provides REST endpoints for currency conversion.

### API Gateway

The API gateway acts as a central entry point for all requests. It routes requests to the appropriate microservices and includes a custom logging filter for request logging.

### Naming Server

The naming server is responsible for service discovery within the microservices architecture. It allows services to locate each other without hardcoding service URLs.

### Logging Filter

The logging filter is a global filter within the API gateway that logs incoming requests, providing visibility into request paths.

## Usage

1. Clone the repository to your local machine.

2. Start the naming server, currency exchange service, currency conversion service, and API gateway by running their respective Spring Boot applications.

3. Access the API gateway for routing requests to the appropriate services.

Example request for currency conversion:
```
GET /currency-conversion/from/{from}/to/{to}/quantity/{quantity}
```

Example request for currency conversion using Feign:
```
GET /currency-conversion-feign/from/{from}/to/{to}/quantity/{quantity}
```
