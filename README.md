# Week 4 Starter: Math Agent

Video Link: <https://youtu.be/QrWDkMlX7TY>

A ReAct agent that solves questions using tool calls.

## Setup

1. Install [uv](https://docs.astral.sh/uv/getting-started/installation/).

2. Copy `.env.example` to `.env` and add your API key:

   ```bash
   cp .env.example .env
   ```

   Then edit `.env` and replace `your-key-here` with your key from [Google AI Studio](https://aistudio.google.com/apikey).

   To use a different provider, change the `MODEL` variable in `agent.py` and set the matching key in `.env`.

3. Make sure `.env` is in `.gitignore` so you don't commit your key.

## Run

```bash
uv run agent.py
```

uv will install dependencies automatically on first run.

The agent will work through each question in `math_questions.md` and print the ReAct trace (Reason / Act / Result) for each one.

## Results

The agent successfully solves all 8 questions:

- Questions 1–4: solved using the calculator tool
- Questions 5–8: solved using the product_lookup tool

The ReAct reasoning traces (Reason / Act / Result) are printed in the terminal output.

## Files

- `agent.py` - the main ReAct agent implementation
- `calculator.py` – tool for mathematical calculations
- `products.json` – product catalog with prices
- `math_questions.md` – input questions for the agent
- `.env.example` – template for API key setup
