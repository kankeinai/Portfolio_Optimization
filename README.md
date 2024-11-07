
# Portfolio Optimization Bot

This project provides a portfolio optimization solution through a Telegram bot interface, focusing on investment decisions with stochastic factors, constraints, and dependencies between projects. Users can interact with the bot to upload data, define parameters, and receive an optimization report.

## Features

- **Optimization**: Maximize portfolio revenue within a budget, considering each project's cost, benefit, and risk of failure.
- **Stochastic Modeling**: Account for scenarios of project success/failure, modeling uncertainty in outcomes.
- **Dependency Constraints**: Ensures that projects with dependencies are selected accordingly.
- **Analysis**: Provides insight into revenue distributions, expected value of perfect information, and price of stochastic solutions.
- **User-Friendly Bot Interface**: Telegram bot assists users in submitting project data and retrieving a detailed report.

## Getting Started

### Prerequisites

- Python 3.x
- Required packages listed in `requirements.txt`
- Telegram account and API credentials

### Installation

1. Clone this repository:
   ```bash
   git clone https://github.com/yourusername/Portfolio_Optimization.git
   ```
2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

3. Set up your Telegram bot credentials by creating a `.env` file or by updating `config.py`.

### Usage

1. **Prepare Input Data**: Ensure that your input file (`.xlsx` or `.csv`) contains the columns: `project`, `benefit`, `cost`, `risk`, `dependence`. Refer to the example format in `instructions.pdf`.

2. **Run the Bot**: Execute the bot with:
   ```bash
   python bot.py
   ```

3. **Interact via Telegram**: 
   - Upload your input file to the bot.
   - Set the required optimization parameters.
   - Receive the generated report.

### Output

The bot generates an automatically formatted report (`sample_report.pdf` for reference) that includes:

- Project selection based on optimization
- Expected revenue analysis for each scenario
- Graphical distribution of revenue for training and test sets
- Calculations of stochastic solution metrics

### Example Report

A sample report is provided in `sample_report.pdf`. This document demonstrates the final output structure, including revenue distributions, budget utilization, and recommended project investments.

## Files Overview

- **bot.py**: The main bot script to handle Telegram interactions.
- **config.py**: Configuration file for API credentials and settings.
- **utils.py**: Helper functions for data processing.
- **keyboards.py**: Defines custom keyboards for the Telegram bot interface.
- **script.jl**: Julia script for computationally intensive tasks.
- **instructions.pdf**: Detailed explanation of the model, constraints, and usage instructions.

## Project Structure

- **`/src`**: Contains main scripts and helper functions.
- **`/reports`**: Folder where generated reports are saved.
- **`/data`**: Sample data files and required input templates.

## Contributing

1. Fork the repository.
2. Create your feature branch (`git checkout -b feature/YourFeature`).
3. Commit your changes (`git commit -m 'Add your feature'`).
4. Push to the branch (`git push origin feature/YourFeature`).
5. Open a pull request.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Contact

For questions or suggestions, contact [Your Name](mailto:youremail@example.com).