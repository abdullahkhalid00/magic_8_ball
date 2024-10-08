# Magic 8 Ball in Python 🎱

[![pages-build-deployment](https://github.com/abdullahkhalid00/magic-8-ball/actions/workflows/pages/pages-build-deployment/badge.svg)](https://github.com/abdullahkhalid00/magic-8-ball/actions/workflows/pages/pages-build-deployment) [![Python 3.10+](https://img.shields.io/badge/python-3.11-blue.svg)](https://tracker.debian.org/pkg/python3.11)

A very basic implementation of the magic 8 ball game that simply asks the user for a question and uses a Gemini Pro model to generate an answer. The model simulates a magic 8 ball in real life.

## Usage

Get your Google API Key from [here](https://ai.google.dev/gemini-api/docs/api-key).

Open up  a terminal and clone the repository.

```bash
git clone <repo-link>
```

Navigate to the cloned repo directory.

```bash
cd magic_8_ball
```

Set up your Google API key as an environment variable.

Alternatively, you can create a `.env` file in your directory and use the `python-dotenv` library to read environment variables.

```python
GOOGLE_API_KEY='<your-api-key>'
```

Create a Python virtual environment and activate it.

```bash
python -m venv env
env\Scripts\activate
```

Install the necessary dependencies in `requirements.txt` file.

```bash
pip install -r requirements.txt
```

Open up a terminal and run the `app.py` file.

```bash
uvicorn app:app --reload
```

Open the `index.html` file in your browser of choice and play the game.

### Testing FastAPI Endpoint

Test the API by make a POST request on the `/ask` endpoint.

```bash
curl -X POST "http://localhost:8000/ask" -H "Content-Type: application/json" -d "{\"question\":\"Will I succeed?\"}"
```

### Running in CLI

You can also play the game in command line by running `cli.py` in any terminal.

```bash
python cli.py --question "<your-question>"
```

## Deployment on Leapcell

The FastAPI endpoint is deployed on Leapcell and the frontend is deployed on GitHub pages as a static webpage.

## Contribution

Feel free to open up a pull request to point out a bug or an improvement.
