# Project Structure

This document provides a comprehensive overview of the project structure, describing the purpose of each file and directory.

## Root Directory
```
d:\LangGraph\langchain-academy\teste/
├── README.md                           # Main project documentation and setup guide
├── LICENSE                            # MIT License file
├── Makefile                           # Build automation and development tasks
├── .codespellignore                   # Codespell ignore patterns file
└── PROJECT_STRUCTURE.md               # This file - project structure documentation
```

## Tests Directory
```
tests/
├── unit_tests/
│   └── __init__.py                    # Unit tests package initializer
└── integration_tests/
    └── __init__.py                    # Integration tests package initializer
```

## File Descriptions

### Root Level Files

#### README.md
- **Purpose**: Main project documentation
- **Contents**: 
  - Project overview and description
  - Setup instructions for LangGraph Studio
  - Customization guidelines
  - Development workflow
  - Badge links for CI/CD status

#### LICENSE
- **Purpose**: Legal license file
- **Type**: MIT License
- **Copyright**: 2024 LangChain

#### Makefile
- **Purpose**: Build automation and development workflow
- **Targets**:
  - `test`: Run unit tests
  - `integration_tests`: Run integration tests
  - `test_watch`: Run tests in watch mode
  - `lint`: Code linting and type checking
  - `format`: Code formatting
  - `spell_check`: Spell checking
- **Dependencies**: Uses pytest, ruff, mypy, codespell

#### .codespellignore
- **Purpose**: Configuration file for codespell
- **Contents**: Currently empty - patterns to ignore during spell checking

### Test Structure

#### tests/unit_tests/__init__.py
- **Purpose**: Package initializer for unit tests
- **Contents**: Placeholder documentation for unit test definitions

#### tests/integration_tests/__init__.py
- **Purpose**: Package initializer for integration tests  
- **Contents**: Placeholder documentation for integration test definitions

## Missing Directories (Expected in LangGraph Projects)

Based on the README.md references, the following directories are expected but not present in the current file listing:

```
src/                                   # Main source code directory (referenced in README)
├── agent/
│   ├── configuration.py              # System prompt and agent configuration
│   └── graph.py                      # Core chatbot logic and LangGraph implementation
└── ...

static/                               # Static assets directory (referenced in README)
└── studio_ui.png                    # LangGraph Studio UI screenshot

.env.example                          # Environment variables template
.env                                  # Environment variables (user-created)
```

## Dependencies and Relationships

### Development Dependencies
- **pytest**: Testing framework (used by Makefile targets)
- **ruff**: Code formatting and linting
- **mypy**: Static type checking
- **codespell**: Spell checking
- **ptw**: pytest-watch for continuous testing

### Project Dependencies (Expected)
- **LangGraph**: Core framework for building stateful agents
- **LangChain**: Language model integration
- **Anthropic/OpenAI**: LLM providers (as mentioned in README)

## Configuration Files

### Makefile Configuration
- **PYTHON_FILES**: Configurable target for linting/formatting (defaults to `src/`)
- **TEST_FILE**: Configurable test path (defaults to `tests/unit_tests/`)
- **MYPY_CACHE**: Type checking cache directory

## Development Workflow

1. **Setup**: Copy `.env.example` to `.env` and configure API keys
2. **Development**: Use `make test_watch` for continuous testing
3. **Quality**: Use `make lint` and `make format` for code quality
4. **Testing**: Use `make test` for unit tests, `make integration_tests` for integration tests
5. **Studio**: Open project in LangGraph Studio for visual development

## Notes

- This appears to be a LangGraph chatbot template project
- The project follows standard Python package structure
- CI/CD is configured via GitHub Actions (referenced in README badges)
- LangGraph Studio integration is a key feature
- The project supports both unit and integration testing workflows
```
