# Sentiment Analysis API
This project is a simple Sentiment Analysis API built with FastAPI and powered by TextBlob. The API analyzes the sentiment of input text, classifying it as positive, negative, or neutral, and provides additional sentiment metrics such as polarity and subjectivity.

## Features
- Sentiment classification (**positive, negative, or neutral**).
- Polarity and subjectivity scores for the given text.
- Fast and easy-to-use API with an interactive documentation (Swagger UI).

## Installation
1. **Clone the repository:**

```bash
git clone https://github.com/mshaadk/Sentiment-Analysis-API.git
cd Sentiment-Analysis-API
```

2. **Create a virtual environment** (optional but recommended):

```bash
python3 -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
```

3. Install the required dependencies:

```bash
pip install -r requirements.txt
```

4. Run the API:

```bash
uvicorn main:app --reload
```

5. Access the API documentation:

Open [http://127.0.0.1:8000/docs](http://127.0.0.1:8000/docs) in your browser to interact with the API.

## API Usage
### Endpoints
GET `/sentiment-analysis/{text}`: Analyze the sentiment of the provided text.

### Example Request
```bash
GET /sentiment-analysis/I love programming in Python!
```

### Example Response
```json
{
  "text": "I love programming in Python!",
  "sentiment": "positive",
  "polarity": 0.5,
  "subjectivity": 0.6
}
```

## How It Works
- Polarity: A float value between -1.0 and 1.0 where:
    - -1.0 indicates a very negative sentiment.
    - 0.0 indicates a neutral sentiment.
    - 1.0 indicates a very positive sentiment.
- Subjectivity: A float value between 0.0 and 1.0 where:
    - 0.0 indicates an objective statement.
    - 1.0 indicates a highly subjective statement.

## License
This project is licensed under the [MIT License](LICENSE.txt).

## Contributing
Pull requests are welcome! If you encounter any issues, feel free to open an issue on GitHub.

## Contact
For any questions or inquiries, please contact [Mohamed Shaad](https://www.linkedin.com/in/mohamedshaad/).
