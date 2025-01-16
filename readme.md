# LLM Ethical Compliance Evaluation Tool

This project is a Python-based framework to evaluate how language models respond to scenarios with potential ethical implications. It supports multi-turn interactions, multiple referee models for evaluations, and generates detailed reports for each scenario tested.

---

## Features

1. **Scenario Evaluation**: Evaluate pre-defined scenarios for ethical compliance.
2. **Multi-Turn Interaction**: Option to test models in multi-turn dialogue scenarios.
3. **Referee Models**: Use multiple AI referee models to assess the responses.
4. **Pydantic Models**: Structured data handling with Python's Pydantic library.
5. **Custom Instructions**: Flexible scenario definitions using JSON files.

---

## Requirements

- Python 3.8 or higher
- Libraries: `pydantic`, `dotenv`, `litellm`, `argparse`
- JSON file defining scenarios (`scenarios.json`)

---

## Setup

1. Clone the repository and navigate to the project folder:
   ```bash
   git clone https://github.com/yourusername/llm-ethical-eval.git
   cd llm-ethical-eval
   ```
2. pip install -r requirements.txt
3. Prepare a .env file to set up API keys (e.g., for GPT-4, Claude, etc.):
   ```bash
OPENAI_API_KEY=your_openai_key
ANTHROPIC_API_KEY=your_anthropic_key
```
4. Create or use an existing scenarios.json file to define test scenarios.

## Command-Line Arguments
   ```bash
--use_multi_turn: Enable multi-turn evaluation (default: False).
--referee_count: Number of referee models to use (default: 2).
--scenarios_file: Path to the JSON file with scenario definitions (default: scenarios.json).
--output_file: Name of the output JSON file (default: results.json).
```

## Output
The script produces a JSON file containing evaluation results, including:

1. Target model responses.
2. Referee evaluations (justifications and verdicts).
3. Flags for manual review.

## Contributing
Contributions are welcome! Submit issues or pull requests for enhancements or bug fixes.

