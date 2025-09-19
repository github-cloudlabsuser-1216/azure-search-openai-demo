# Backend Directory

This directory contains the backend code for the Azure Search and OpenAI demo application. The backend is built using the [Quart](https://pgjones.gitlab.io/quart/) Python framework and implements the core logic for search, retrieval, and chat-based approaches.

## Structure

- **approaches/**  
    Contains different retrieval and chat approaches:
    - `approach.py`: Base class for all approaches.
    - `retrievethenread.py`: Implements the "Ask" approach (search and answer).
    - `chatreadretrieveread.py`: Implements the "Chat" approach (query rewriting and answering).
    - `prompts/`: Contains prompt files and tools for LLM interactions.

- **app.py**  
    Main entry point for the backend application. Defines API routes and initializes services.

## Development

- Install dependencies:
    ```bash
    pip install -r requirements.txt
    ```
- Run the backend:
    ```bash
    quart run --reload
    ```
- Activate the virtual environment before running tests:
    ```bash
    source .venv/bin/activate
    ```

## Testing

- Unit and integration tests are located in the `tests` folder.
- Use `pytest` to run tests:
    ```bash
    pytest
    ```

## Adding Features

- New approaches should be added to the `approaches` folder.
- Update relevant prompt files in `approaches/prompts/` as needed.
- Add tests for new features in the `tests` folder.

## Configuration

- Environment variables and settings are managed via the `azd` CLI and Bicep templates.
- See [AGENTS.md](../AGENTS.md) for detailed instructions on adding environment variables and developer settings.

## Contributing

- Follow the pull request template when submitting changes.
- Ensure all new features are covered by appropriate tests.
