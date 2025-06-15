# Nuclear Incident Report Summarization with XAI

This project implements an Explainable AI (XAI) system for summarizing nuclear incident reports using the BART model (`facebook/bart-large-cnn`) from Hugging Face's `transformers` library. It provides attention visualizations to ensure transparency for regulatory compliance (e.g., NRC requirements) and expert validation in safety-critical nuclear applications.

## Features
- **Summarization**: Generates concise summaries of nuclear incident reports.
- **Explainability**: Visualizes attention weights to highlight influential input tokens (e.g., "failed generator").
- **Nuclear Industry Fit**: Supports rapid response, regulatory transparency, and safety-critical documentation.
- **Cross-Industry Potential**: Applicable to healthcare (medical incident reports) and aviation (maintenance logs).

## Installation
1. Clone the repository:
   ```bash
   git clone https://github.com/PseudoGod541/nuclear-xai-summarizer.git
   cd nuclear-xai-summarizer
   ```
2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```
3. Ensure Python 3.8+ is installed.

## Usage
1. Run the summarization script:
   ```bash
   python summarize.py
   ```
2. Example input:
   ```python
   incident_text = """
   On June 5, 2024, Unit 3 experienced a temporary loss of power due to a failed generator control module.
   Operators responded immediately and shifted cooling operations to backup systems.
   No radiation was released. The NRC was notified, and full power was restored within 3 hours.
   Investigation revealed that the failure was due to aged circuit components.
   """
   ```
3. Example output:
   - **Summary**: "Unit 3 lost power on June 5, 2024, due to a failed generator module. No radiation was released."
   - **Attention Visualization**:
     ![Attention Plot for Nuclear Incident Summarization](images/attention_plot.png)

## Project Structure
- `summarize.py`: Script for summarization and attention visualization.
- `images/`: Contains screenshots (e.g., `attention_plot.png`).
- `requirements.txt`: List of dependencies.
- `README.md`: Project documentation.

## Contributing
1. Fork the repository.
2. Create a feature branch (`git checkout -b feature/new-feature`).
3. Commit changes (`git commit -m "Add new feature"`).
4. Push to the branch (`git push origin feature/new-feature`).
5. Open a pull request.

## License
MIT License. See `LICENSE` for details.

## References
- Hugging Face Transformers (2024). `facebook/bart-large-cnn` model.
- U.S. Nuclear Regulatory Commission (2024). Artificial Intelligence Strategic Plan.

## Contact
For questions, open an issue on GitHub or contact [your-email@example.com](mailto:your-email@example.com).