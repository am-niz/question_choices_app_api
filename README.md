# Question Choices API

This is a RESTful API built with FastAPI that allows users to create questions with multiple choices, retrieve questions, and their corresponding choices from the database.

## Features

- Create questions with multiple choices.
- Retrieve a specific question and its details.
- List all choices for a specific question.

## Technologies

- FastAPI
- SQLAlchemy
- Pydantic

## Getting Started

These instructions will get you a copy of the project up and running on your local machine for development and testing purposes.

### Prerequisites

Before you begin, ensure you have met the following requirements:

- Python 3.8+
- pip

### Installation

1. Clone the repository:
```sh
git clone https://github.com/am-niz/question_choices_app_api.git
cd question_choices_app_api
```

2. Install the required packages:
```sh
pip install -r requirements.txt
```

3. Create a `.env` file in the root directory of the project and add your database URL:
```plaintext
DATABASE_URL="sqlite:///./test.db"
```
(Replace the value with the connection string appropriate for your database.)

4. Run the application:
```sh
uvicorn main:app --reload
```

The API will be available at [http://localhost:8000](http://localhost:8000).

## Usage

### Create a Question with Choices

`POST /questions/`

Request body:
```json
{
  "question_text": "What is the capital of France?",
  "choices": [
    {"choice_text": "Paris", "is_correct": true},
    {"choice_text": "Berlin", "is_correct": false},
    {"choice_text": "Madrid", "is_correct": false}
  ]
}
```

### Get a Specific Question

`GET /questions/{question_id}`

Replace `{question_id}` with the id of the question you want to retrieve.

### Get Choices for a Specific Question

`GET /choices/{question_id}`

Replace `{question_id}` with the id of the question for which you want to list all choices.

## Contributing

Contributions are what make the open source community such an amazing place to learn, inspire, and create. Any contributions you make are **greatly appreciated**.

## License

Distributed under the MIT License. See `LICENSE` for more information.

## Contact

Gamil: - nizamudheenmj@gmail.com

Project Link: [https://github.com/am-niz/question_choices_app_api](https://github.com/am-niz/question_choices_app_api)
```
