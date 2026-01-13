# AI Agent Backend – FastAPI

## Setup Instructions

1. Create virtual environment
   python -m venv venv
   source venv/bin/activate

2. Install dependencies
   pip install fastapi uvicorn sqlalchemy pydantic

3. Run server
   uvicorn main:app --reload

## API Endpoint

POST /agent/query

### Examples

1. Calculator
{
  "prompt": "What is 10 plus 5?"
}

2. Save Memory
{
  "prompt": "Remember my cat's name is Fluffy"
}

3. Recall Memory
{
  "prompt": "What is my cat's name?"
}

## Notes
- SQLite used instead of PostgreSQL for POC
- Calculator uses AST parsing (safe, no eval)
