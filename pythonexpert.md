# Instructions for Python Experts

These instructions are intended for experienced Python developers to maintain high standards of code quality, performance, and maintainability within our projects.

## 1. Code Style and Quality

*   **Adhere to PEP 8**: Follow the official Python style guide consistently. Use tools like `flake8`, `black`, or `ruff` for automated formatting and linting.
*   **Type Hinting**: Utilize type hints (`mypy`) for all function signatures, variable declarations, and complex data structures to improve code readability, maintainability, and catch potential errors early.
*   **Docstrings**: Write clear, concise, and comprehensive docstrings for all modules, classes, methods, and functions, following PEP 257.
*   **Readability**: Prioritize clear, self-documenting code. Avoid overly clever or obscure constructs.

## 2. Performance Optimization

*   **Profiling**: Use `cProfile` or other profiling tools to identify performance bottlenecks.
*   **Efficient Algorithms & Data Structures**: Choose appropriate algorithms and data structures for the task at hand. Understand the time and space complexity implications.
*   **Avoid Premature Optimization**: Optimize only when necessary, backed by profiling data.
*   **Understand Python's Internals**: Be aware of how Python handles memory, the GIL (Global Interpreter Lock), and common performance pitfalls.
*   **Leverage Built-ins and Libraries**: Prefer optimized built-in functions and standard library modules (e.g., `collections`, `itertools`) over custom implementations where appropriate.
*   **Vectorization (for numerical tasks)**: For numerical heavy lifting, utilize libraries like NumPy and Pandas which are highly optimized.

## 3. Testing

*   **Comprehensive Test Suite**: Write unit, integration, and end-to-end tests for all new features and bug fixes.
*   **Test Frameworks**: Use `pytest` for writing tests.
*   **Coverage**: Strive for high test coverage, but prioritize meaningful tests over simply increasing a percentage. Use `coverage.py` to measure.
*   **CI/CD Integration**: Ensure tests are run automatically as part of the CI/CD pipeline.

## 4. Documentation

*   **README.md**: Maintain an up-to-date `README.md` with clear setup instructions, project overview, and usage examples.
*   **API Documentation**: Generate API documentation (e.g., using Sphinx or MkDocs) for libraries and complex modules.
*   **Diagrams**: Use diagrams (e.g., UML, flowcharts) for complex architectures or workflows.

## 5. Dependency Management

*   **Virtual Environments**: Always use virtual environments (`venv`, `conda`) for project dependencies.
*   **`requirements.txt` / `pyproject.toml`**: Precisely pin dependencies in `requirements.txt` (for applications) or specify broader ranges in `pyproject.toml` (for libraries). Use `pip-tools` or Poetry for managing dependencies.

## 6. Error Handling

*   **Specific Exceptions**: Catch specific exceptions rather than broad `Exception` catches.
*   **Custom Exceptions**: Define custom exception classes for application-specific errors.
*   **Logging**: Use the `logging` module for effective debugging and operational insights. Avoid excessive print statements.
*   **Clear Error Messages**: Provide informative error messages for easier debugging and user comprehension.

## 7. Security Considerations

*   **Input Validation**: Always validate and sanitize user inputs to prevent injection attacks and other vulnerabilities.
*   **Secret Management**: Never hardcode sensitive information (API keys, passwords). Use environment variables, a secret management system, or a `.env` file (excluded from version control).
*   **Dependency Audits**: Regularly audit third-party dependencies for known vulnerabilities.

## 8. Version Control

*   **Git Best Practices**: Follow a consistent Git branching strategy (e.g., Gitflow, GitHub Flow).
*   **Atomic Commits**: Make small, focused commits with clear, descriptive messages.
*   **Code Reviews**: Actively participate in code reviews to ensure quality and knowledge sharing.

## 9. Advanced Topics (when applicable)

*   **Concurrency/Parallelism**: Understand and correctly apply `threading`, `multiprocessing`, `asyncio` for concurrent operations.
*   **Metaprogramming**: Use decorators, metaclasses, and dynamic code generation judiciously and only when the benefits clearly outweigh the complexity.
*   **C Extensions**: Consider writing C extensions for performance-critical sections if Python alone is insufficient, using `ctypes`, `Cython`, or the C API.
