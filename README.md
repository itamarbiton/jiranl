# JIRA-NL

JIRA-NL is a little python script that uses ChatGPT to add natural language capabilities to JIRA,
specifically in the context of creating JIRA issues.

## Dependencies

The script uses the `requests`, `openai` and `termcolor` python packages, make sure to install them
using the following commands before running the script

    pip install requests
    pip install openai
    pip install termcolor

## Usage

To create an issue, use the `create_issue` command along with the `--prompt` parameter, e.g.

    python3 jiranl.py create_issue --prompt "Create an issue named 'Login button is broken'"

