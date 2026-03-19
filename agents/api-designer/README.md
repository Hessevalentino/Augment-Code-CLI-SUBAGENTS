# API Designer

Expert API architect for RESTful design, OpenAPI/Swagger documentation, GraphQL schemas, versioning strategies, and backward compatibility.

## Purpose

This agent specializes in designing robust, scalable, and developer-friendly APIs. It helps teams create well-structured API contracts following industry best practices, with comprehensive documentation and proper versioning strategies. The agent focuses on developer experience, backward compatibility, and long-term API evolution.

## Core Capabilities

### RESTful API Design
Proper resource modeling with clear hierarchies and relationships. Correct usage of HTTP methods (GET, POST, PUT, PATCH, DELETE) and status codes. URL structure following REST principles. Consistent request/response formats with proper error handling.

### OpenAPI/Swagger Documentation
Complete OpenAPI 3.0/3.1 specifications serving as single source of truth. Comprehensive endpoint documentation with parameters, schemas, examples, and security definitions. Reusable components for schemas, responses, and parameters. Auto-generated interactive documentation.

### GraphQL Schema Design
Well-structured GraphQL schemas with proper type definitions. Relay-style cursor-based pagination. Input types for mutations with error handling. Nullable vs non-nullable fields carefully considered. Comprehensive field descriptions and deprecation notices.

### API Versioning Strategies
URL versioning, header versioning, and query parameter approaches. Clear guidelines on when to create new versions. Major/minor/patch versioning semantics. Deprecation policies with sunset dates and migration guides.

### Backward Compatibility
Rules for safe API evolution without breaking existing clients. Adding optional fields vs breaking changes. Deprecation strategies with proper communication. Migration paths for version upgrades.

## Key Features

**Developer Experience First**: APIs designed to be intuitive, consistent, and easy to use. Clear error messages with actionable information. Comprehensive examples and use cases.

**Industry Standards**: Follows OpenAPI specification, JSON:API, GraphQL spec, and relevant RFCs. Uses established patterns for pagination, filtering, sorting, and bulk operations.

**Security Built-in**: Authentication and authorization strategies (JWT, OAuth 2.0, API keys). Input validation and sanitization. Rate limiting and abuse prevention. HTTPS enforcement and data protection.

**Performance Optimized**: Caching strategies with proper headers. Pagination for large datasets. Field selection for sparse fieldsets. Compression and conditional requests.

**Long-term Evolution**: Designed for change without breaking clients. Clear versioning and deprecation policies. Migration guides and sunset dates. Monitoring of deprecated endpoint usage.

## Usage

Load the agent configuration file `api-designer.md` in Augment Code CLI. The agent will help you design API contracts, write OpenAPI/GraphQL specifications, plan versioning strategies, and ensure backward compatibility.

## Design Process

The agent follows a systematic approach: understanding requirements and use cases, modeling resources and relationships, designing API contracts with proper HTTP semantics, documenting with OpenAPI or GraphQL schemas, planning versioning strategy, reviewing for best practices, and providing implementation guidance.

## API Patterns

Covers essential patterns including offset and cursor-based pagination, filtering and sorting, rate limiting with headers, bulk operations, webhooks, field selection, caching strategies, and conditional requests.

## Best Practices

Emphasizes consistency across endpoints, proper HTTP semantics, comprehensive error handling, security considerations, performance optimization, and exceptional developer experience. Provides concrete examples and explains trade-offs between different approaches.

## Technical Approach

Applies REST principles, OpenAPI standards, GraphQL best practices, and HTTP specifications. Balances theoretical ideals with practical implementation constraints. Considers both API provider and consumer perspectives.

