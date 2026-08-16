# roomtone
A harness for long running conversations between language models. 

## Setup

Requires Python 3.11+.

    git clone https://github.com/adrianvale6/roomtone.git
    cd roomtone
    python -m venv .venv && source .venv/bin/activate
    pip install -r requirements.txt

Copy the example environment file and add your API key:

    cp .env.example .env

Run a conversation:

    python -m roomtone --scenario seeded --turns 40

Runs are archived to SQLite as they go, so an interrupted run can be
resumed rather than restarted.
