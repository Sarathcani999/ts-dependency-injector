# TypeScript Dependency Injector

A lightweight and intuitive library for implementing **Dependency Injection (DI)** in TypeScript using **decorators**, designed to enhance the scalability, maintainability, and testability of your codebase.

## Key Features
- **Decorator-Based DI:** Simplifies the implementation of dependency injection with powerful and easy-to-use TypeScript decorators.
- **Scalability:** Helps you structure your application for growth by managing dependencies effectively.
- **Testability:** Makes your codebase easier to test by promoting loose coupling and enabling mock dependencies.
- **Lightweight and Performant:** Designed with minimal overhead to ensure high performance in production environments.
- **Type Safety:** Fully leverages TypeScript's type system for compile-time checks, reducing runtime errors.

## Getting Started
### Installation
Install the library via npm:
```bash
npm install typescript-dependency-injector
```

### Basic Usage
Here's a quick example to get started:

```typescript
import { Injectable, Inject } from 'typescript-dependency-injector';

@Injectable()
class ServiceA {
  getMessage() {
    return 'Hello from ServiceA!';
  }
}

@Injectable()
class ServiceB {
  constructor(@Inject() private serviceA: ServiceA) {}

  logMessage() {
    console.log(this.serviceA.getMessage());
  }
}

// Create and resolve the dependencies
const serviceB = new ServiceB();
serviceB.logMessage();
```

## Why Use Dependency Injection?
Dependency Injection is a design pattern that promotes:

- Separation of Concerns: Components only depend on the interfaces or services they need, without managing their own dependencies.
- Reusability: Decoupled components can be reused across different projects.
- Testability: Dependencies can be easily mocked or stubbed in unit tests.
## Contribution

We welcome contributions! Please feel free to open issues, suggest features, or create pull requests to improve this library.