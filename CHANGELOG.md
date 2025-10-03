# Changelog

## [Unreleased]

### Added
- **`create_model` tool**: Create new empty GO-CAM models with optional titles
  - Generates new model IDs automatically
  - Returns model ID for use with other tools
  - Integrates with `get_noctua_url` from gocam-ai for easy access to Noctua editor

### Enhanced
- **Comprehensive examples in all tool docstrings**:
  - Each tool now has 3-12 practical examples
  - Examples use real GO terms, UniProt IDs, and RO relations
  - Common evidence codes (ECO) documented with use cases
  - Relationship types explained with their meanings

- **New example scripts**:
  - `examples/demo_create_model.py` - Demonstrates model creation workflow
  - `examples/show_tools.py` - Lists all tools with their documentation
  - `examples/usage_examples.md` - Comprehensive usage guide

### Changed
- Refactored to use gocam-ai as the core library
- MCP server is now a thin shim layer over gocam-ai
- All business logic moved to upstream gocam-ai library

### Fixed
- Live tests now properly skip when BARISTA_TOKEN is invalid
- Tests marked with `@pytest.mark.live` for easy exclusion

### Testing
- Added comprehensive unit tests for create_model functionality
- 34 tests pass (excluding live tests)
- Tests cover all major functionality including model creation

## Dependencies
- Now depends on gocam-ai library (local path)
- Requires BARISTA_TOKEN environment variable for privileged operations