# Backend Directory

This directory contains the Python backend code for the Azure Search and OpenAI demo application. The backend is built using the Quart framework and implements various approaches for integrating Azure Search and OpenAI.

## Structure

- **approaches/**: Contains different retrieval and chat approaches.
    - `approach.py`: Base class for all approaches.
    - `retrievethenread.py`: Implements the "Ask" approach (search and answer).
    - `chatreadretrieveread.py`: Implements the "Chat" approach (query rewriting and answering).
    - `prompts/`: Contains prompt files and tools for the approaches.
- **app.py**: Main entry point for the backend application.

## Development

- Ensure you have a Python environment set up (see project root for instructions).
- Approaches are modular; add new approaches in the `approaches/` folder.
- Update prompt files in `approaches/prompts/` as needed.

## Testing

- All tests are in the `tests/` folder at the project root.
- Use pytest for unit and integration tests.
- Activate the virtual environment before running tests:
    ```bash
    source .venv/bin/activate
    ```

## Adding Features

- For new approaches, create a new file in `approaches/` and inherit from `approach.py`.
- Update prompt files or add new ones in `approaches/prompts/`.
- Add tests for new features in the appropriate test files.

## Configuration

- Environment variables and settings are managed via the azd CLI and Bicep templates.
- See the project root and `AGENTS.md` for instructions on adding new environment variables or developer settings.

## Resources

- See [`AGENTS.md`](../AGENTS.md) for detailed coding instructions and development guidelines.
- For frontend code, see `../frontend/`.



