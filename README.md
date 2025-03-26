# LLM Response Evaluation Platform

This project provides a platform for evaluating LLM responses in the context of Job Safety Analysis (JSA) for construction tasks. The platform offers two evaluation methods:

1. **Human Evaluation**: Compare JSA reports generated by different LLM systems and vote on which one is better
2. **LLM-based Evaluation**: Use a judge LLM to evaluate JSA reports from different systems

![image](https://github.com/user-attachments/assets/e8277444-715e-436a-bfd1-a7ac112b42e6)

## Features

- Blind comparison of JSA reports from:
  - **Dragonshield**: A multi-agent system using `GPT-4-1106-preview` with specialized agents
  - **JSA Advisor**: A single-agent system using `GPT-4-1106-preview`
- Multi-agent Dragonshield system with specialized agents:
  - Project Manager Agent
  - Safety Inspector Agent
  - Risk Assessment Agent
  - Feedbacker Agent
  - Risk Management Agent
  - Reporter Agent
    
 ![image](https://github.com/user-attachments/assets/606bfffe-fec1-4aaa-9a66-810d165a4a1a)

- Side-by-side comparison of JSA reports
- Automated evaluation using an impartial LLM judge

## Getting Started

### Prerequisites

- Python 3.8+
- OpenAI API key (required for generating responses)

### Installation

1. Clone the repository:
   ```
   git clone https://github.com/Khashayarghorab/LLMEval.git
   cd LLMEval
   ```

2. Install dependencies:
   ```
   pip install -r requirements.txt
   ```

3. Run the application:
   ```
   streamlit run Home.py
   ```

### Usage

1. Launch the application and select either "Human Evaluator" or "LLM Evaluator"
2. Provide your OpenAI API key
3. Enter your own construction task for JSA analysis
4. View and compare the JSA reports generated by different systems
5. For human evaluation, vote on which response is better
6. For LLM evaluation, review the comprehensive analysis and compare systems

## Project Structure

- `Home.py`: Landing page with options for human or LLM evaluation
- `pages/human_evaluator.py`: Interface for human evaluation of LLM responses
- `pages/llm_evaluator.py`: Interface for LLM-based automatic evaluation
- `utils.py`: Utility functions for displaying responses
- `.streamlit/config.toml`: Streamlit configuration settings

## Models Used

- **Dragonshield**: A multi-agent system using OpenAI's `GPT-4-1106-preview` with specialized agent roles
- **JSA Advisor**: A single-agent system using OpenAI's `GPT-4-1106-preview`
- **JSA Judge**: An impartial evaluator using `GPT-4-1106-preview` to compare responses

## License

This project is licensed under the MIT License - see the LICENSE file for details.
