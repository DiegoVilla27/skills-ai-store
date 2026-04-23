---
description: 'Automated API Documentation with Swagger/OpenAPI'
author: 'Diego Villanueva'
trigger: 'When documenting REST APIs, defining DTOs, or setting up Swagger UI.'
---

# NestJS OpenAPI (Swagger)

Standardized implementation of API contracts and interactive documentation.

## ✅ ALWAYS
- Use `@nestjs/swagger` and the Swagger CLI Plugin for automatic metadata generation.
- Use `@ApiProperty()` to describe DTO fields and validation rules.
- Define `@ApiTags()` to group controllers logically.
- Use `@ApiOperation()` and `@ApiResponse()` for detailed endpoint descriptions.
- Set up a standard path (e.g., `/docs`) for the Swagger UI.

## ❌ NEVER
- Leave endpoints undocumented in production-ready APIs.
- Manually write the OpenAPI JSON; let NestJS generate it from your code.
- Expose the documentation in production without proper environment checks.

## 🛠 Patterns
- **DTO Inheritance**: Using `PartialType`, `PickType`, and `OmitType` to keep documentation dry.
- **Security Definitions**: Documenting JWT or OAuth authentication requirements.
