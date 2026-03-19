# API Design Resources

Curated list of resources, tools, and standards for API design.

## 📚 Standards & Specifications

### OpenAPI / Swagger
- [OpenAPI Specification 3.1](https://spec.openapis.org/oas/latest.html) - Official specification
- [OpenAPI 3.0 Guide](https://swagger.io/docs/specification/about/) - Swagger documentation
- [OpenAPI Examples](https://github.com/OAI/OpenAPI-Specification/tree/main/examples) - Official examples

### GraphQL
- [GraphQL Specification](https://spec.graphql.org/) - Official GraphQL spec
- [GraphQL Best Practices](https://graphql.org/learn/best-practices/) - Official best practices
- [Relay Specification](https://relay.dev/docs/guides/graphql-server-specification/) - Relay cursor pagination

### REST & HTTP
- [RFC 7231 - HTTP/1.1 Semantics](https://tools.ietf.org/html/rfc7231) - HTTP methods and status codes
- [RFC 7807 - Problem Details for HTTP APIs](https://tools.ietf.org/html/rfc7807) - Standard error format
- [RFC 6570 - URI Templates](https://tools.ietf.org/html/rfc6570) - URI template syntax
- [JSON:API Specification](https://jsonapi.org/) - JSON API standard

### API Design Guides
- [Microsoft REST API Guidelines](https://github.com/microsoft/api-guidelines)
- [Google API Design Guide](https://cloud.google.com/apis/design)
- [Zalando RESTful API Guidelines](https://opensource.zalando.com/restful-api-guidelines/)
- [PayPal API Design Guidelines](https://github.com/paypal/api-standards/blob/master/api-style-guide.md)

## 🛠️ Tools

### Documentation
- [Swagger UI](https://swagger.io/tools/swagger-ui/) - Interactive API documentation
- [Redoc](https://github.com/Redocly/redoc) - Beautiful OpenAPI documentation
- [Stoplight Studio](https://stoplight.io/studio) - Visual OpenAPI editor
- [GraphQL Playground](https://github.com/graphql/graphql-playground) - GraphQL IDE
- [Apollo Studio](https://www.apollographql.com/docs/studio/) - GraphQL platform

### API Testing
- [Postman](https://www.postman.com/) - API development and testing
- [Insomnia](https://insomnia.rest/) - REST and GraphQL client
- [HTTPie](https://httpie.io/) - Command-line HTTP client
- [curl](https://curl.se/) - Classic command-line tool

### Code Generation
- [OpenAPI Generator](https://openapi-generator.tech/) - Generate clients/servers from OpenAPI
- [Swagger Codegen](https://swagger.io/tools/swagger-codegen/) - Code generation tool
- [GraphQL Code Generator](https://www.graphql-code-generator.com/) - Generate TypeScript types

### Validation & Linting
- [Spectral](https://stoplight.io/open-source/spectral) - OpenAPI/JSON linter
- [OpenAPI Validator](https://github.com/IBM/openapi-validator) - IBM's validator
- [GraphQL ESLint](https://github.com/B2o5T/graphql-eslint) - GraphQL linting

### Mock Servers
- [Prism](https://stoplight.io/open-source/prism) - OpenAPI mock server
- [JSON Server](https://github.com/typicode/json-server) - Quick REST API mock
- [MSW](https://mswjs.io/) - API mocking library

## 📖 Books

- **"RESTful Web APIs"** by Leonard Richardson & Mike Amundsen
- **"REST API Design Rulebook"** by Mark Massé
- **"API Design Patterns"** by JJ Geewax
- **"Designing Web APIs"** by Brenda Jin, Saurabh Sahni, Amir Shevat
- **"GraphQL in Action"** by Samer Buna

## 🎓 Learning Resources

### Courses
- [REST API Design Best Practices](https://www.udemy.com/course/rest-api/) - Udemy
- [GraphQL: The Big Picture](https://www.pluralsight.com/courses/graphql-big-picture) - Pluralsight
- [API Design](https://www.coursera.org/learn/api-design) - Coursera

### Articles & Blogs
- [API Design Guide](https://apiguide.readthedocs.io/) - Comprehensive guide
- [REST API Tutorial](https://restfulapi.net/) - REST fundamentals
- [GraphQL Best Practices](https://graphql.org/learn/best-practices/)

## 🔍 API Design Patterns

### Pagination
- **Offset-based**: `?page=2&limit=20`
- **Cursor-based**: `?after=cursor&limit=20` (recommended for large datasets)
- **Keyset pagination**: Using last seen ID

### Filtering & Sorting
- **Simple**: `?status=active&sort=-created_at`
- **Advanced**: `?filter[status]=active&filter[role]=admin`
- **GraphQL**: Arguments on fields

### Rate Limiting
- **Headers**: `X-RateLimit-Limit`, `X-RateLimit-Remaining`, `X-RateLimit-Reset`
- **Status Code**: `429 Too Many Requests`
- **Retry-After**: Header with seconds or date

### Versioning
- **URL**: `/api/v1/users` (recommended)
- **Header**: `Accept: application/vnd.api+json; version=1`
- **Query**: `?version=1`

### Error Handling
- **RFC 7807**: Problem Details format
- **Consistent structure**: `{ "error": { "code": "...", "message": "..." } }`
- **Validation errors**: Array of field-specific errors

## 🔐 Security

### Authentication
- **JWT**: JSON Web Tokens for stateless auth
- **OAuth 2.0**: Industry standard for authorization
- **API Keys**: Simple service-to-service auth

### Best Practices
- Always use HTTPS
- Validate all inputs
- Rate limiting per endpoint
- CORS configuration
- Security headers (HSTS, CSP, etc.)
- Input sanitization
- SQL injection prevention
- XSS protection

### Resources
- [OWASP API Security Top 10](https://owasp.org/www-project-api-security/)
- [JWT.io](https://jwt.io/) - JWT debugger and libraries
- [OAuth 2.0](https://oauth.net/2/) - Official OAuth documentation

## 📊 Performance

### Caching
- **HTTP Caching**: `Cache-Control`, `ETag`, `Last-Modified`
- **CDN**: CloudFlare, Fastly, AWS CloudFront
- **Application Cache**: Redis, Memcached

### Optimization
- **Compression**: gzip, brotli
- **Pagination**: Limit response size
- **Field Selection**: Sparse fieldsets (`?fields=id,name`)
- **GraphQL**: Avoid N+1 queries with DataLoader

### Monitoring
- **APM**: New Relic, Datadog, AppDynamics
- **Logging**: ELK Stack, Splunk
- **Metrics**: Prometheus, Grafana

## 🧪 Testing

### Types of Tests
- **Unit Tests**: Individual endpoint logic
- **Integration Tests**: API contract testing
- **E2E Tests**: Full user flows
- **Load Tests**: Performance under load
- **Security Tests**: Penetration testing

### Tools
- **Jest**: JavaScript testing framework
- **Supertest**: HTTP assertion library
- **Pact**: Contract testing
- **k6**: Load testing tool
- **Artillery**: Load and functional testing

## 🌐 API Gateways

- **Kong**: Open-source API gateway
- **AWS API Gateway**: Managed service
- **Azure API Management**: Microsoft's solution
- **Apigee**: Google Cloud API management
- **Tyk**: Open-source gateway

## 📝 Documentation Best Practices

1. **Complete OpenAPI/GraphQL schemas** - Single source of truth
2. **Examples for every endpoint** - Request and response samples
3. **Error documentation** - All possible error codes
4. **Authentication guide** - How to authenticate
5. **Rate limiting info** - Limits and headers
6. **Changelog** - Version history and breaking changes
7. **Migration guides** - For version upgrades
8. **Getting started guide** - Quick start tutorial
9. **SDKs and libraries** - Client libraries in popular languages
10. **Interactive playground** - Try API in browser

## 🎯 API Design Principles

### RESTful Principles
1. **Client-Server**: Separation of concerns
2. **Stateless**: Each request contains all needed information
3. **Cacheable**: Responses explicitly indicate cacheability
4. **Uniform Interface**: Consistent resource identification
5. **Layered System**: Client doesn't know if connected to end server
6. **Code on Demand** (optional): Server can extend client functionality

### GraphQL Principles
1. **Hierarchical**: Queries match data structure
2. **Product-centric**: Driven by client requirements
3. **Strong typing**: Schema defines capabilities
4. **Client-specified queries**: Clients request exactly what they need
5. **Introspective**: Clients can query schema

### General Best Practices
1. **Developer Experience First**: Easy to understand and use
2. **Consistency**: Predictable patterns across API
3. **Versioning**: Plan for evolution
4. **Documentation**: Comprehensive and up-to-date
5. **Security**: Built-in from the start
6. **Performance**: Optimized for scale
7. **Error Handling**: Clear and actionable errors
8. **Testing**: Thoroughly tested
9. **Monitoring**: Observable and debuggable
10. **Backward Compatibility**: Don't break existing clients

